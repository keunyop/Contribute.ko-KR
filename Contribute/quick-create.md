---
title: '빠른 시작: Azure Key Vault에서 비밀을 설정하고 검색 | Microsoft Docs'
description: '빠른 시작: Azure Key Vault에서 비밀을 설정하고 검색'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308827"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>빠른 시작: Azure Key Vault에서 비밀을 설정하고 검색

이 빠른 시작에서는 Key Vault에 비밀을 저장하는 방법 및 웹앱을 사용하여 비밀을 검색하는 방법을 보여줍니다. 비밀 값을 확인하려면 Azure에서 다음을 실행해야 합니다. 이 빠른 시작에서는 Node.js 및 MSI(관리 서비스 ID)를 사용합니다.

> [!div class="checklist"]
> * Key Vault를 만듭니다.
> * Key Vault에 비밀을 저장합니다.
> * Key Vault에서 비밀을 검색합니다.
> * Azure 웹 응용 프로그램을 만듭니다.
> * [관리 서비스 ID를 사용하도록 설정](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)합니다.
> * 웹 응용 프로그램이 Key Vault에서 데이터를 읽는 데 필요한 권한을 부여합니다.

계속 진행하기 전에 [기본 개념](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)을 숙지하시기 바랍니다.

> [!NOTE]
> 아래 자습서가 모범 사례인 이유를 이해하려면 몇 가지 개념을 이해해야 합니다. Key Vault는 프로그래밍 방식으로 비밀을 저장하는 중앙 리포지토리입니다. 하지만 이렇게 하려면 응용 프로그램/사용자가 먼저 Key Vault에 인증해야 합니다. 즉, 비밀을 입력해야 합니다. 보안 모범 사례를 따르기 위해 이 첫 번째 비밀도 정기적으로 순환해야 합니다. 하지만 [관리 서비스 ID](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)를 사용하면 Azure에서 실행되는 응용 프로그램에 Azure에서 자동으로 관리하는 ID가 제공됩니다. 이렇게 하면 **비밀 도입 문제**가 해결되므로 사용자/응용 프로그램이 모범 사례를 준수할 수 있고 첫 번째 비밀의 순환에 대해 걱정할 필요가 없습니다.

## <a name="prerequisites"></a>필수 조건

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"
* 다음 작업을 지원하는 [Visual Studio 2017 버전 15.7.3 이상](https://www.microsoft.com/net/download/windows):
  * ASP.NET 및 웹 개발
  * .NET Core 플랫폼 간 개발
* [.NET Core 2.1 SDK 이상](https://www.microsoft.com/net/download/windows) :::zone-end
* Git([다운로드](https://git-scm.com/downloads)).
* Azure 구독. Azure 구독이 없는 경우 시작하기 전에 [체험 계정](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)을 만듭니다.
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 버전 2.0.4 이상을 사용하세요. Windows, Mac 및 Linux에서 사용할 수 있습니다.

## <a name="login-to-azure"></a>Azure에 로그인

CLI를 사용하여 Azure에 로그인하려면 다음을 입력합니다.

```azurecli
az login
```

## <a name="create-resource-group"></a>리소스 그룹 만들기

[az group create](/cli/azure/group#az-group-create) 명령을 사용하여 리소스 그룹을 만듭니다. Azure 리소스 그룹은 Azure 리소스가 배포되고 관리되는 논리 컨테이너입니다.

리소스 그룹 이름을 선택하고 자리 표시자를 입력하세요.
다음 예에서는 *eastus* 위치에 *<YourResourceGroupName>* 이라는 리소스 그룹을 만듭니다.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

방금 만든 리소스 그룹은 이 자습서 전체에서 사용됩니다.

## <a name="create-an-azure-key-vault"></a>Azure Key Vault 만들기

다음으로 이전 단계에서 만든 리소스 그룹을 사용하여 Key Vault를 만듭니다. 이 문서에서는 Key Vault의 이름으로 “ContosoKeyVault”를 사용하고 있지만, 여러분은 각자 고유한 이름을 사용해야 합니다. 다음 정보를 제공하세요.

* Vault 이름 - **여기서 Key Vault 이름을 선택하세요**.
* 리소스 그룹 이름 - **여기서 리소스 그룹 이름을 선택하세요**.
* 위치 - **미국 동부**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

이때 사용자의 Azure 계정은 이 새 Vault에서 모든 작업을 수행할 권한이 있는 유일한 계정입니다.

## <a name="add-a-secret-to-key-vault"></a>Key Vault에 비밀 추가

이 작업을 설명하기 위한 비밀을 추가하고 있습니다. 안전하게 유지하면서 응용 프로그램에서 사용할 수 있도록 하는 데 필요한 SQL 연결 문자열 또는 기타 정보를 저장할 수 있습니다. 이 자습서에서 암호는 **AppSecret**이고, 그 안에 **MySecret** 값이 저장됩니다.

아래 명령을 입력하여 값 **MySecret**을 저장하는 **AppSecret**이라는 비밀을 Key Vault에 만듭니다.

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

비밀에 들어 있는 값을 일반 텍스트로 보려면:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

이 명령은 URI를 포함한 비밀 정보를 표시합니다. 이러한 단계를 완료하면 Azure Key Vault의 비밀에 대한 URI이 생깁니다. 이 정보를 적어 둡니다. 나중에 필요합니다.

## <a name="clone-the-repo"></a>리포지토리 복제

소스를 편집할 로컬 복사본을 만들려면 다음 명령을 실행하여 리포지토리를 복제합니다.

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>종속성 설치

여기서 종속성을 설치합니다. cd key-vault-node-quickstart npm install 명령을 실행합니다.

이 프로젝트에서는 다음 2개 노드 모듈을 사용합니다.

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Azure에 웹 응용 프로그램 게시

다음은 수행해야 할 몇 가지 단계입니다.

* 첫 번째 단계는 [Azure App Service](https://azure.microsoft.com/services/app-service/) 계획을 만드는 것입니다. 이 계획에 여러 웹앱을 저장할 수 있습니다.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* 다음으로 웹앱을 만듭니다. 다음 예제에서는 <app_name>을 전역적으로 고유한 앱 이름으로 바꿉니다(유효한 문자는 a-z, 0-9 및 -). 런타임은 NODE|6.9로 설정됩니다. 지원되는 모든 런타임을 보려면 az webapp list-runtimes를 실행합니다.

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    웹앱이 만들어지면 Azure CLI는 다음 예제와 비슷한 출력을 표시합니다.

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    새로 만든 웹앱으로 이동하면 작동하는 웹앱이 표시됩니다. <app_name>을 고유한 앱 이름으로 바꿉니다.

    ```text
    http://<app name>.azurewebsites.net
    ```
    또한 위의 명령은 로컬 git에서 Azure에 배포할 수 있는 Git 지원 앱을 만듭니다. 
    로컬 git은 ‘ https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git’ url로 구성됩니다.

* 이전 명령이 완료된 후에 배포 사용자를 만들면 로컬 Git 리포지토리에 Azure 원격을 추가할 수 있습니다. <url>을 앱에 대해 Git 사용에서 가져온 Git 원격의 URL로 바꿉니다.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>솔루션 열기 및 편집

특정 Key Vault 이름으로 샘플을 실행하도록 program.cs 파일을 편집합니다.

1. key-vault-dotnet-core-quickstart 폴더로 이동합니다.
2. Visual Studio 2017에서 key-vault-dotnet-core-quickstart.sln 파일을 엽니다.
3. Program.cs 파일을 열고, *YourKeyVaultName* 자리 표시자를 앞에서 만든 Key Vault의 이름으로 업데이트합니다.

이 솔루션에서는 [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) 및 [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet 라이브러리를 사용합니다.

## <a name="run-the-app"></a>앱 실행

Visual Studio 2017의 주 메뉴에서 디버깅하지 않고 **디버그** > **시작**을 선택합니다. 브라우저가 표시되면 **정보** 페이지로 이동합니다. **AppSecret**에 대한 값이 표시됩니다.

## <a name="publish-the-web-application-to-azure"></a>Azure에 웹 응용 프로그램 게시

이 앱을 Azure에 게시하여 웹앱으로 라이브로 표시하고 비밀 값을 가져올 수 있는지 확인합니다.

1. Visual Studio에서 **key-vault-dotnet-core-quickstart** 프로젝트를 선택합니다.
2. **게시** > **시작**을 선택합니다.
3. 새 **App Service**를 만든 다음, **게시**를 선택합니다.
4. 앱 이름을 **keyvaultdotnetcorequickstart**로 변경합니다.
5. **만들기**를 선택합니다.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>관리 서비스 ID 사용

Azure Key Vault를 사용하면 자격 증명과 기타 키 및 비밀을 안전하게 저장할 수 있습니다. 하지만 이러한 자격 증명과 키 및 비밀을 검색하려면 코드가 Azure Key Vault에 인증해야 합니다. 관리 서비스 ID를 사용하면 Azure AD(Azure Active Directory)에서 자동으로 관리되는 ID를 Azure 서비스에 제공하여 이 작업을 더 쉽게 수행할 수 있습니다. 이 ID를 사용하면 Key Vault를 비롯하여 Azure AD 인증을 지원하는 모든 서비스에 인증할 수 있으므로 코드에 자격 증명을 포함할 필요가 없습니다.

1. Azure CLI로 돌아갑니다.
2. 이 응용 프로그램에 대한 ID를 만들려면 assign-identity 명령을 실행합니다.

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>이 절차의 명령은 포털로 이동하여 웹 응용 프로그램 속성에서 **관리 서비스 ID**를 **켜기**로 전환하는 것과 같습니다.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>응용 프로그램에 Key Vault에서 비밀을 읽을 수 있는 권한 할당

Azure에 응용 프로그램을 게시할 때 출력을 적어 두세요. 다음과 같은 형식이어야 합니다.

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

그런 다음, Key Vault의 이름 및 **PrincipalId** 값을 사용하여 다음 명령을 실행합니다.

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Azure에 노드 앱을 배포하고 비밀 값 검색

이제 모든 것이 설정되었습니다. 다음 명령을 실행하여 Azure에 앱을 배포하세요.

```bash
git push azure master
```

그런 다음 https://<app_name>.azurewebsites.net을 검색하면 비밀 값을 볼 수 있습니다.
<YourKeyVaultName> 이름을 해당 자격 증명 모음 이름으로 바꿔야 합니다.

::: zone-end

::: zone pivot="dotnet" 이제 응용 프로그램을 실행하면 검색된 비밀 값이 표시됩니다.
::: zone-end

## <a name="next-steps"></a>다음 단계

::: zone pivot="nodejs"
* [Azure Key Vault 홈페이지](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault 설명서](https://docs.microsoft.com/azure/key-vault/)
* [Node용 Azure SDK](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/)(Azure REST API 참조) ::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault 홈페이지](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault 설명서](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For .NET](https://github.com/Azure/azure-sdk-for-net)(.NET용 Azure SDK)
* [Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/)(Azure REST API 참조) ::: zone-end
