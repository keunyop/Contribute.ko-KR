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
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="541b4-103">빠른 시작: Azure Key Vault에서 비밀을 설정하고 검색</span><span class="sxs-lookup"><span data-stu-id="541b4-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="541b4-104">이 빠른 시작에서는 Key Vault에 비밀을 저장하는 방법 및 웹앱을 사용하여 비밀을 검색하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="541b4-105">비밀 값을 확인하려면 Azure에서 다음을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="541b4-106">이 빠른 시작에서는 Node.js 및 MSI(관리 서비스 ID)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="541b4-107">Key Vault를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="541b4-108">Key Vault에 비밀을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="541b4-109">Key Vault에서 비밀을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="541b4-110">Azure 웹 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="541b4-111">[관리 서비스 ID를 사용하도록 설정](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="541b4-112">웹 응용 프로그램이 Key Vault에서 데이터를 읽는 데 필요한 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="541b4-113">계속 진행하기 전에 [기본 개념](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)을 숙지하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="541b4-114">아래 자습서가 모범 사례인 이유를 이해하려면 몇 가지 개념을 이해해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="541b4-115">Key Vault는 프로그래밍 방식으로 비밀을 저장하는 중앙 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="541b4-116">하지만 이렇게 하려면 응용 프로그램/사용자가 먼저 Key Vault에 인증해야 합니다. 즉, 비밀을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="541b4-117">보안 모범 사례를 따르기 위해 이 첫 번째 비밀도 정기적으로 순환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="541b4-118">하지만 [관리 서비스 ID](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)를 사용하면 Azure에서 실행되는 응용 프로그램에 Azure에서 자동으로 관리하는 ID가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="541b4-119">이렇게 하면 **비밀 도입 문제**가 해결되므로 사용자/응용 프로그램이 모범 사례를 준수할 수 있고 첫 번째 비밀의 순환에 대해 걱정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="541b4-120">필수 조건</span><span class="sxs-lookup"><span data-stu-id="541b4-120">Prerequisites</span></span>

<span data-ttu-id="541b4-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="541b4-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="541b4-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="541b4-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="541b4-123">다음 작업을 지원하는 [Visual Studio 2017 버전 15.7.3 이상](https://www.microsoft.com/net/download/windows):</span><span class="sxs-lookup"><span data-stu-id="541b4-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="541b4-124">ASP.NET 및 웹 개발</span><span class="sxs-lookup"><span data-stu-id="541b4-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="541b4-125">.NET Core 플랫폼 간 개발</span><span class="sxs-lookup"><span data-stu-id="541b4-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="541b4-126">[.NET Core 2.1 SDK 이상](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="541b4-127">Git([다운로드](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="541b4-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="541b4-128">Azure 구독.</span><span class="sxs-lookup"><span data-stu-id="541b4-128">An Azure subscription.</span></span> <span data-ttu-id="541b4-129">Azure 구독이 없는 경우 시작하기 전에 [체험 계정](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="541b4-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) 버전 2.0.4 이상을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="541b4-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="541b4-131">Windows, Mac 및 Linux에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="541b4-132">Azure에 로그인</span><span class="sxs-lookup"><span data-stu-id="541b4-132">Login to Azure</span></span>

<span data-ttu-id="541b4-133">CLI를 사용하여 Azure에 로그인하려면 다음을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="541b4-134">리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="541b4-134">Create resource group</span></span>

<span data-ttu-id="541b4-135">[az group create](/cli/azure/group#az-group-create) 명령을 사용하여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="541b4-136">Azure 리소스 그룹은 Azure 리소스가 배포되고 관리되는 논리 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="541b4-137">리소스 그룹 이름을 선택하고 자리 표시자를 입력하세요.</span><span class="sxs-lookup"><span data-stu-id="541b4-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="541b4-138">다음 예에서는 *eastus* 위치에 *<YourResourceGroupName>* 이라는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="541b4-139">방금 만든 리소스 그룹은 이 자습서 전체에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="541b4-140">Azure Key Vault 만들기</span><span class="sxs-lookup"><span data-stu-id="541b4-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="541b4-141">다음으로 이전 단계에서 만든 리소스 그룹을 사용하여 Key Vault를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="541b4-142">이 문서에서는 Key Vault의 이름으로 “ContosoKeyVault”를 사용하고 있지만, 여러분은 각자 고유한 이름을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="541b4-143">다음 정보를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="541b4-143">Provide the following information:</span></span>

* <span data-ttu-id="541b4-144">Vault 이름 - **여기서 Key Vault 이름을 선택하세요**.</span><span class="sxs-lookup"><span data-stu-id="541b4-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="541b4-145">리소스 그룹 이름 - **여기서 리소스 그룹 이름을 선택하세요**.</span><span class="sxs-lookup"><span data-stu-id="541b4-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="541b4-146">위치 - **미국 동부**.</span><span class="sxs-lookup"><span data-stu-id="541b4-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="541b4-147">이때 사용자의 Azure 계정은 이 새 Vault에서 모든 작업을 수행할 권한이 있는 유일한 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="541b4-148">Key Vault에 비밀 추가</span><span class="sxs-lookup"><span data-stu-id="541b4-148">Add a secret to key vault</span></span>

<span data-ttu-id="541b4-149">이 작업을 설명하기 위한 비밀을 추가하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="541b4-150">안전하게 유지하면서 응용 프로그램에서 사용할 수 있도록 하는 데 필요한 SQL 연결 문자열 또는 기타 정보를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="541b4-151">이 자습서에서 암호는 **AppSecret**이고, 그 안에 **MySecret** 값이 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="541b4-152">아래 명령을 입력하여 값 **MySecret**을 저장하는 **AppSecret**이라는 비밀을 Key Vault에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="541b4-153">비밀에 들어 있는 값을 일반 텍스트로 보려면:</span><span class="sxs-lookup"><span data-stu-id="541b4-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="541b4-154">이 명령은 URI를 포함한 비밀 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="541b4-155">이러한 단계를 완료하면 Azure Key Vault의 비밀에 대한 URI이 생깁니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="541b4-156">이 정보를 적어 둡니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-156">Write this information down.</span></span> <span data-ttu-id="541b4-157">나중에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="541b4-158">리포지토리 복제</span><span class="sxs-lookup"><span data-stu-id="541b4-158">Clone the Repo</span></span>

<span data-ttu-id="541b4-159">소스를 편집할 로컬 복사본을 만들려면 다음 명령을 실행하여 리포지토리를 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="541b4-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="541b4-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="541b4-161">종속성 설치</span><span class="sxs-lookup"><span data-stu-id="541b4-161">Install dependencies</span></span>

<span data-ttu-id="541b4-162">여기서 종속성을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-162">Here we install the dependencies.</span></span> <span data-ttu-id="541b4-163">cd key-vault-node-quickstart npm install 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="541b4-164">이 프로젝트에서는 다음 2개 노드 모듈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-164">This project used 2 node modules:</span></span>

* [<span data-ttu-id="541b4-165">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="541b4-165">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="541b4-166">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="541b4-166">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="541b4-167">Azure에 웹 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="541b4-167">Publish the web application to Azure</span></span>

<span data-ttu-id="541b4-168">다음은 수행해야 할 몇 가지 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="541b4-169">첫 번째 단계는 [Azure App Service](https://azure.microsoft.com/services/app-service/) 계획을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="541b4-170">이 계획에 여러 웹앱을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="541b4-171">다음으로 웹앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-171">Next we create a web app.</span></span> <span data-ttu-id="541b4-172">다음 예제에서는 <app_name>을 전역적으로 고유한 앱 이름으로 바꿉니다(유효한 문자는 a-z, 0-9 및 -).</span><span class="sxs-lookup"><span data-stu-id="541b4-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="541b4-173">런타임은 NODE|6.9로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="541b4-174">지원되는 모든 런타임을 보려면 az webapp list-runtimes를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="541b4-175">웹앱이 만들어지면 Azure CLI는 다음 예제와 비슷한 출력을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="541b4-176">새로 만든 웹앱으로 이동하면 작동하는 웹앱이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="541b4-177"><app_name>을 고유한 앱 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="541b4-178">또한 위의 명령은 로컬 git에서 Azure에 배포할 수 있는 Git 지원 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="541b4-179">로컬 git은 ‘ https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git’ url로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="541b4-180">이전 명령이 완료된 후에 배포 사용자를 만들면 로컬 Git 리포지토리에 Azure 원격을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="541b4-181"><url>을 앱에 대해 Git 사용에서 가져온 Git 원격의 URL로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="541b4-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-182">::: zone-end</span></span>

<span data-ttu-id="541b4-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="541b4-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="541b4-184">솔루션 열기 및 편집</span><span class="sxs-lookup"><span data-stu-id="541b4-184">Open and edit the solution</span></span>

<span data-ttu-id="541b4-185">특정 Key Vault 이름으로 샘플을 실행하도록 program.cs 파일을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="541b4-186">key-vault-dotnet-core-quickstart 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="541b4-187">Visual Studio 2017에서 key-vault-dotnet-core-quickstart.sln 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="541b4-188">Program.cs 파일을 열고, *YourKeyVaultName* 자리 표시자를 앞에서 만든 Key Vault의 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="541b4-189">이 솔루션에서는 [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) 및 [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet 라이브러리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="541b4-190">앱 실행</span><span class="sxs-lookup"><span data-stu-id="541b4-190">Run the app</span></span>

<span data-ttu-id="541b4-191">Visual Studio 2017의 주 메뉴에서 디버깅하지 않고 **디버그** > **시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="541b4-192">브라우저가 표시되면 **정보** 페이지로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="541b4-193">**AppSecret**에 대한 값이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="541b4-194">Azure에 웹 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="541b4-194">Publish the web application to Azure</span></span>

<span data-ttu-id="541b4-195">이 앱을 Azure에 게시하여 웹앱으로 라이브로 표시하고 비밀 값을 가져올 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="541b4-196">Visual Studio에서 **key-vault-dotnet-core-quickstart** 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="541b4-197">**게시** > **시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="541b4-198">새 **App Service**를 만든 다음, **게시**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="541b4-199">앱 이름을 **keyvaultdotnetcorequickstart**로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="541b4-200">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="541b4-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="541b4-202">관리 서비스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="541b4-202">Enable managed service identities</span></span>

<span data-ttu-id="541b4-203">Azure Key Vault를 사용하면 자격 증명과 기타 키 및 비밀을 안전하게 저장할 수 있습니다. 하지만 이러한 자격 증명과 키 및 비밀을 검색하려면 코드가 Azure Key Vault에 인증해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="541b4-204">관리 서비스 ID를 사용하면 Azure AD(Azure Active Directory)에서 자동으로 관리되는 ID를 Azure 서비스에 제공하여 이 작업을 더 쉽게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="541b4-205">이 ID를 사용하면 Key Vault를 비롯하여 Azure AD 인증을 지원하는 모든 서비스에 인증할 수 있으므로 코드에 자격 증명을 포함할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="541b4-206">Azure CLI로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="541b4-207">이 응용 프로그램에 대한 ID를 만들려면 assign-identity 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="541b4-208">이 절차의 명령은 포털로 이동하여 웹 응용 프로그램 속성에서 **관리 서비스 ID**를 **켜기**로 전환하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="541b4-209">응용 프로그램에 Key Vault에서 비밀을 읽을 수 있는 권한 할당</span><span class="sxs-lookup"><span data-stu-id="541b4-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="541b4-210">Azure에 응용 프로그램을 게시할 때 출력을 적어 두세요.</span><span class="sxs-lookup"><span data-stu-id="541b4-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="541b4-211">다음과 같은 형식이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="541b4-212">그런 다음, Key Vault의 이름 및 **PrincipalId** 값을 사용하여 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="541b4-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="541b4-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="541b4-214">Azure에 노드 앱을 배포하고 비밀 값 검색</span><span class="sxs-lookup"><span data-stu-id="541b4-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="541b4-215">이제 모든 것이 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-215">Now that everything is set.</span></span> <span data-ttu-id="541b4-216">다음 명령을 실행하여 Azure에 앱을 배포하세요.</span><span class="sxs-lookup"><span data-stu-id="541b4-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="541b4-217">그런 다음 https://<app_name>.azurewebsites.net을 검색하면 비밀 값을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="541b4-218"><YourKeyVaultName> 이름을 해당 자격 증명 모음 이름으로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="541b4-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-219">::: zone-end</span></span>

<span data-ttu-id="541b4-220">::: zone pivot="dotnet" 이제 응용 프로그램을 실행하면 검색된 비밀 값이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="541b4-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="541b4-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="541b4-222">다음 단계</span><span class="sxs-lookup"><span data-stu-id="541b4-222">Next steps</span></span>

<span data-ttu-id="541b4-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="541b4-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="541b4-224">Azure Key Vault 홈페이지</span><span class="sxs-lookup"><span data-stu-id="541b4-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="541b4-225">Azure Key Vault 설명서</span><span class="sxs-lookup"><span data-stu-id="541b4-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="541b4-226">Node용 Azure SDK</span><span class="sxs-lookup"><span data-stu-id="541b4-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="541b4-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/)(Azure REST API 참조) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="541b4-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="541b4-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="541b4-229">Azure Key Vault 홈페이지</span><span class="sxs-lookup"><span data-stu-id="541b4-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="541b4-230">Azure Key Vault 설명서</span><span class="sxs-lookup"><span data-stu-id="541b4-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* <span data-ttu-id="541b4-231">[Azure SDK For .NET](https://github.com/Azure/azure-sdk-for-net)(.NET용 Azure SDK)</span><span class="sxs-lookup"><span data-stu-id="541b4-231">[Azure SDK For .NET](https://github.com/Azure/azure-sdk-for-net)</span></span>
* <span data-ttu-id="541b4-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/)(Azure REST API 참조) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="541b4-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
