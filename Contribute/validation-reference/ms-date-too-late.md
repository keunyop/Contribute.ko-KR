---
title: ms-date-too-late
description: Docs 빌드 문제 ms-date-too-late에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637394"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="0dbd0-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="0dbd0-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="0dbd0-104">경고</span><span class="sxs-lookup"><span data-stu-id="0dbd0-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="0dbd0-105">`ms.date` 특성은 “유효 시간”(문서의 관련성, 정확성, 올바른 스크린샷 및 작업 링크가 마지막으로 검토된 시간)을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="0dbd0-106">따라서 미래의 날짜를 지정할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="0dbd0-107">주요 이벤트를 준비하면서 QA 콘텐츠가 동결되는 경우와 같이 5일의 릴리스 시간을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="0dbd0-108">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0dbd0-108">Resolution</span></span>

<span data-ttu-id="0dbd0-109">YYYY/MM/DD 형식으로 오늘부터 5일 이내의 `ms.date`를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
