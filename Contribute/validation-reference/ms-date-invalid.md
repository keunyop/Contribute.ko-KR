---
title: ms-date-invalid
description: Docs 빌드 문제 ms-date-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2f34a0e510d7d006c598ae163217a117a72f1de2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236175"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="c5de9-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="c5de9-103">ms-date-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="c5de9-104">경고</span><span class="sxs-lookup"><span data-stu-id="c5de9-104">Warning</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="c5de9-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="c5de9-105">Resolution</span></span>

<span data-ttu-id="c5de9-106">문서가 손상된 콘텐츠 없이 최신 상태인지 확인한 후 YYYY/MM/DD 형식으로 유효한 날짜를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c5de9-106">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
