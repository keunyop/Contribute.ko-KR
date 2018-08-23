---
title: 설명서에서 링크를 사용하는 방법
description: 이 문서에서는 docs.microsoft.com 내의 콘텐츠에 대한 링크를 만드는 방법에 대한 지침을 제공합니다.
ms.date: 06/29/2017
ms.openlocfilehash: dad0460cfb36594c17cef1b079c5fc14191f56f7
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251486"
---
# <a name="using-links-in-documentation"></a>설명서에서 링크 사용
이 문서에서는 docs.microsoft.com에서 호스팅되는 페이지의 하이퍼 링크를 사용하는 방법에 대해 설명합니다. 링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다. 사용자는 링크를 통해 동일한 페이지의 콘텐츠를 가리키거나, 인접한 다른 페이지를 가리키거나, 외부 사이트 및 URL을 가리킬 수 있습니다.

docs.microsoft.com 사이트 백 엔드에서는 DFM(DocFX Flavored Markdown)을 구현하는 OPS(Open Publishing Services)를 사용합니다. DFM은 GFM(GitHub Flavored Markdown)과 잘 호환되며, Markdown 확장을 통해 추가 기능을 추가합니다.

> [!IMPORTANT]
> 대상이 링크를 지원하는 경우(대부분 지원) 모든 링크는 보안 링크여야 합니다(`https` 및 `http`).

## <a name="link-text"></a>링크 텍스트

링크 텍스트에 포함하는 단어는 친근해야 합니다. 즉, 일반적인 영어(한국어) 단어 또는 연결하는 페이지의 제목이어야 합니다.

> [!IMPORTANT]
> "여기를 클릭하세요."를 사용하지 않습니다. SEO에 올바르지 않고 대상을 적절하게 설명하지 않습니다.

**올바름:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**잘못됨:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>하나의 문서에서 다른 문서로 링크

한 Docs 기술 문서에서 동일한 docset 내의 다른 Docs 기술 문서로의 인라인 링크를 만들려면 다음과 같은 링크 구문을 사용합니다.

- 디렉토리의 문서는 동일한 디렉토리에 있는 다른 문서로 연결됩니다.

  `[link text](article-name.md)`

- 문서는 하위 디렉토리에서 루트 디렉터리에 있는 문서로 연결됩니다.

  `[link text](../article-name.md)`

- 루트 디렉터리의 문서는 하위 디렉토리에 있는 문서로 연결됩니다.

  `[link text](./directory/article-name.md)`

- 하위 디렉토리의 문서는 다른 하위 디렉토리에 있는 문서로 연결됩니다.

  `[link text](../directory/article-name.md)`

- docset 간에 연결하는 문서(동일한 리포지토리에 있는 경우도 해당): `[link text](./directory/article-name)`

> [!IMPORTANT]
> 위의 예제에서는 `~/`를 링크의 일부로 사용하지 않습니다. 리포지토리의 루트에서 경로에 연결하는 경우 `/`로 시작합니다. GitHub에서 원본 리포지토리로 이동할 때 `~/`를 포함하면 유효하지 않은 링크가 생성됩니다. `/`로 경로를 시작하면 올바르게 해결됩니다.

## <a name="links-to-anchors"></a>앵커에 대한 링크

앵커를 만들 필요가 없습니다. 앵커는 모든 H2 제목에서 게시 시간에 자동으로 생성됩니다. H2 섹션에 대한 링크를 만들기만 하면 됩니다.

- 동일한 문서 내의 제목에 연결하려면

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- 동일한 하위 디렉토리의 다른 문서에 있는 앵커에 연결하려면

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- 다른 서비스 하위 디렉토리에 있는 앵커에 연결하려면

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>포함되는 내용의 링크

포함되는 파일은 다른 디렉토리에 위치하기 때문에 더 긴 상대 경로를 사용해야 합니다. 포함되는 파일의 문서에 연결하려면 이 형식을 사용합니다.

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>선택기의 링크

Azure 문서 팀이 수행하는 대로 포함되는 내용에 포함된 선택기가 있는 경우 다음과 같은 링크 구조체를 사용합니다.

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Text1 | Example1 )](../articles/folder/article-name1.md)
    - [(Text1 | Example2 )](../articles/folder/article-name2.md)
    - [(Text2 | Example3 )](../articles/folder/article-name3.md)
    - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>참조 스타일 링크

소스 콘텐츠를 쉽게 읽을 수 있도록 참조 스타일 링크를 사용할 수 있습니다. 참조 스타일 링크는 인라인 링크 구문을, 긴 URL을 문서 끝으로 이동시킨 간소화된 구문으로 바꿉니다. [Daring Fireball](https://daringfireball.net/projects/markdown/)의 예제는 다음과 같습니다.

인라인 텍스트:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

문서 끝의 링크 참조:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

링크 앞에 쉼표 뒤에 공백이 있어야 합니다. 다른 기술 문서에 연결할 때 공백을 포함하지 못한 경우 게시된 문서에서 링크가 작동하지 않습니다.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>기술 문서 집합의 일부가 아닌 페이지에 대한 링크

다른 Microsoft 속성의 페이지(가격 책정 페이지, SLA 페이지 또는 설명서 문서가 아닌 다른 페이지)에 연결하려면 절대 URL을 사용하지만 로캘을 생략합니다. 여기서 목적은 링크가 GitHub 및 렌더링된 사이트에서 작동하는 것입니다.

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>타사 사이트에 대한 링크

멋진 사용자 환경은 사용자를 다른 사이트에 보내는 작업을 최소화합니다. 따라서 간혹 필요한 타사 사이트에 대한 링크는 다음 정보를 기반으로 합니다.

- **책임성:** 공유하려는 정보가 타사 정보인 경우 타사 콘텐츠에 연결합니다. 예를 들어 사용자에게 Android 개발자 도구를 사용하는 방법을 알려주는 것은 Microsoft이 해야 할 일이 아닙니다. 해당 작업은 Google에서 담당하게 됩니다. 필요한 경우 Azure*에서* Android 개발자 도구를 사용하는 방법을 설명할 수 있지만 Google에서도 해당 도구를 사용하는 방법을 설명해야 합니다.
- **PM 승인**: 타사 콘텐츠에 대해 Microsoft에서 승인하도록 요청합니다. 링크를 설정한다는 것은 Microsoft가 해당 사이트를 신뢰한다는 것을 의미하며 사람들이 지침을 따를 경우 Microsoft에도 의무가 있다는 것을 나타냅니다.
- **유효 시간 검토:** 타사 정보가 최신 정보이고 정확하며 관련성이 있는지 확인하고 링크가 변경되지 않도록 합니다.
- **오프사이트:** 사용자가 다른 사이트로 이동한다는 점을 인식하도록 합니다. 이에 대한 명확한 내용이 없을 경우 설명하는 문구를 추가합니다. 예: "필수 조건에는 Android 개발자 도구가 포함되며 Android Studio 사이트에서 다운로드할 수 있습니다."
- **다음 단계:** "다음 단계" 섹션에서 예를 들어 MVP 블로그에 대한 링크를 추가할 수 있습니다. 다시 한 번 사용자가 사이트를 벗어난다는 점을 인식하도록 합니다.
- **법적 정보:** 모든 ms.com 페이지의 **사용 조건** 바닥글에 **타사 사이트에 대한 링크**의 법적 정보가 설명되어 있습니다.

## <a name="links-to-msdn-or-technet"></a>MSDN 또는 TechNet에 대한 링크

MSDN 또는 TechNet에 연결해야 하는 경우 항목에 대한 전체 링크를 사용하고 링크에서 "en-us" 언어 로캘을 제거합니다.

## <a name="links-to-azure-powershell-reference-content"></a>Azure PowerShell 참조 콘텐츠에 대한 링크

Azure PowerShell 참조 콘텐츠는 2016년 11월부터 몇 가지 내용이 변경되었습니다. docs.microsoft.com의 다른 문서에서 이 콘텐츠에 연결하는 다음 지침을 사용하니다.

URL의 구조체:

* cmdlet의 경우:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* 개념 항목의 경우:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

&lt;moniker-name&gt; 부분은 선택 사항입니다. 생략된 경우 콘텐츠의 최신 버전으로 이동합니다. &lt;service-name&gt; 부분은 다음과 같은 기본 URL에 표시되는 예제의 하나입니다.

- Azure PowerShell(AzureRM) 콘텐츠: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Azure PowerShell(ASM) 콘텐츠: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- AzureAD(Azure Active Directory) PowerShell 콘텐츠: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- Azure Elastic DB 작업 PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

이러한 URL을 사용하는 경우 콘텐츠의 최신 버전으로 이동합니다. 이러한 방식으로 버전 모니커를 지정할 필요가 없습니다. 그러면 버전이 변경될 때 업데이트되어야 하는 개념 콘텐츠에 대한 링크가 표시되지 않습니다.

올바른 링크를 만들려면 브라우저에서 연결하려는 페이지를 찾고 URL을 복사합니다.
그런 다음, “https://docs.microsoft.com” 및 로캘 정보를 제거합니다.

TOC에서 연결하는 경우 로캘 정보 없이 전체 URL을 사용해야 합니다.

예제 Markdown:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
