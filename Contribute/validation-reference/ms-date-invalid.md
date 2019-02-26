---
title: ms-date-invalid
description: Docs 빌드 문제 ms-date-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: e960bc2d8e9013e480f2bb391cdfa0c1da043b8b
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431510"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="d82a6-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="d82a6-103">ms-date-invalid</span></span>

<span data-ttu-id="d82a6-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="d82a6-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d82a6-105">제안</span><span class="sxs-lookup"><span data-stu-id="d82a6-105">Suggestion</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="d82a6-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="d82a6-106">Resolution</span></span>

<span data-ttu-id="d82a6-107">문서가 손상된 콘텐츠 없이 최신 상태인지 확인한 후 YYYY/MM/DD 형식으로 유효한 날짜를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d82a6-107">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
