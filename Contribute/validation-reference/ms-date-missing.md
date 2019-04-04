---
title: ms-date-missing
description: Docs 빌드 문제 ms-date-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637279"
---
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

일부 콘텐츠 그룹은 “유효 시간”(문서의 관련성, 정확성, 올바른 스크린샷 및 작업 링크가 마지막으로 검토된 시간)을 나타내는 `ms.date`가 필요합니다. 이는 `ms.date`가 명시적으로 지정되지 않은 경우 페이지에 표시될, 문서가 ‘게시된’ 마지막 날짜와 동일하지 않습니다.

## <a name="resolution"></a>해결 방법

문서가 손상된 콘텐츠 없이 최신 상태인지 확인한 후 YYYY/MM/DD 형식으로 유효한 날짜를 추가합니다.

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
