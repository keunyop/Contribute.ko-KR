---
title: ms-date-missing
description: Docs 빌드 문제 ms-date-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713249"
---
# <a name="ms-date-missing"></a><span data-ttu-id="f4ea7-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="f4ea7-103">ms-date-missing</span></span>

<span data-ttu-id="f4ea7-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="f4ea7-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f4ea7-105">제안</span><span class="sxs-lookup"><span data-stu-id="f4ea7-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="f4ea7-106">이 날짜는 “유효 시간”(문서의 관련성, 정확성, 올바른 스크린샷 및 작업 링크가 마지막으로 검토된 시간)을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="f4ea7-107">이는 `ms.date`가 명시적으로 지정되지 않은 경우 페이지에 표시될, 문서가 ‘게시된’ 마지막 날짜와 동일하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="f4ea7-108">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f4ea7-108">Resolution</span></span>

<span data-ttu-id="f4ea7-109">문서가 손상된 콘텐츠 없이 최신 상태인지 확인한 후 YYYY/MM/DD 형식으로 유효한 날짜를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea7-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
