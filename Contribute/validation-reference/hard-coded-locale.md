---
title: hard-coded-locale
description: Docs 빌드 문제 hard-coded-locale에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166838"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="aacbf-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="aacbf-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aacbf-104">콘텐츠 팀이 시간을 두고 영향을 가늠하고 리포지토리를 정리할 계획을 세우도록 처음에 이 규칙을 “제안”으로 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="aacbf-105">**그러나 2019년 12월 20일에는 “제안”이 “경고”로 상향 조정됩니다**.</span><span class="sxs-lookup"><span data-stu-id="aacbf-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="aacbf-106">제안</span><span class="sxs-lookup"><span data-stu-id="aacbf-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="aacbf-107">`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="aacbf-108">영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="aacbf-109">예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="aacbf-110">다음 사이트는 이 유효성 검사의 범위에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="aacbf-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aacbf-111">azure.microsoft.com</span></span>
- <span data-ttu-id="aacbf-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aacbf-112">docs.microsoft.com</span></span>
- <span data-ttu-id="aacbf-113">msdn.microsoft.com(올바른 포럼이 연결되도록 하기 위해 로캘이 필요한 social.msdn.com 제외)</span><span class="sxs-lookup"><span data-stu-id="aacbf-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="aacbf-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="aacbf-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="aacbf-115">해결 방법</span><span class="sxs-lookup"><span data-stu-id="aacbf-115">Resolution</span></span>

<span data-ttu-id="aacbf-116">Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="aacbf-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="aacbf-117">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-117">The following is an example.</span></span>

<span data-ttu-id="aacbf-118">이전:</span><span class="sxs-lookup"><span data-stu-id="aacbf-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="aacbf-119">이후:</span><span class="sxs-lookup"><span data-stu-id="aacbf-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="aacbf-120">VS Code에 대한 Docs Markdown에는 Microsoft 링크의 정리 스크립트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="aacbf-121">이 스크립트는 리포지퇴에서 Microsoft 사이트의 모든 링크를 확인하여 링크가 `http` 대신 `https`로 시작하며 `en-us`와 같은 로캘 코드를 포함하지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="aacbf-122">스크립트를 실행하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="aacbf-123">VS Code용 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="aacbf-124">Alt+M을 클릭하여 Markdown 메뉴를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="aacbf-125">**정리**를 선택한 후 **Microsoft 링크**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="aacbf-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
