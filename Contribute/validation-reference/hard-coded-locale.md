---
title: hard-coded-locale
description: Docs 빌드 문제 hard-coded-locale에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427672"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="b4c13-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="b4c13-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="b4c13-104">경고</span><span class="sxs-lookup"><span data-stu-id="b4c13-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="b4c13-105">`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c13-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="b4c13-106">영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c13-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="b4c13-107">예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4c13-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="b4c13-108">다음 사이트는 이 유효성 검사의 범위에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4c13-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="b4c13-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4c13-109">azure.microsoft.com</span></span>
- <span data-ttu-id="b4c13-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4c13-110">docs.microsoft.com</span></span>
- <span data-ttu-id="b4c13-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4c13-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="b4c13-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4c13-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="b4c13-113">해결 방법</span><span class="sxs-lookup"><span data-stu-id="b4c13-113">Resolution</span></span>

<span data-ttu-id="b4c13-114">Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="b4c13-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="b4c13-115">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c13-115">The following is an example.</span></span>

<span data-ttu-id="b4c13-116">이전:</span><span class="sxs-lookup"><span data-stu-id="b4c13-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="b4c13-117">이후:</span><span class="sxs-lookup"><span data-stu-id="b4c13-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]