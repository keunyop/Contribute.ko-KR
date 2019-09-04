---
title: ms-date-missing
description: Docs 빌드 문제 ms-date-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236265"
---
# <a name="ms-date-missing"></a><span data-ttu-id="a2769-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="a2769-103">ms-date-missing</span></span>

## <a name="warning"></a><span data-ttu-id="a2769-104">경고</span><span class="sxs-lookup"><span data-stu-id="a2769-104">Warning</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="a2769-105">일부 콘텐츠 그룹은 “유효 시간”(문서의 관련성, 정확성, 올바른 스크린샷 및 작업 링크가 마지막으로 검토된 시간)을 나타내는 `ms.date`가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a2769-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a2769-106">이는 `ms.date`가 명시적으로 지정되지 않은 경우 페이지에 표시될, 문서가 ‘게시된’ 마지막 날짜와 동일하지 않습니다. </span><span class="sxs-lookup"><span data-stu-id="a2769-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2769-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="a2769-107">Resolution</span></span>

<span data-ttu-id="a2769-108">문서가 손상된 콘텐츠 없이 최신 상태인지 확인한 후 YYYY/MM/DD 형식으로 유효한 날짜를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a2769-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
