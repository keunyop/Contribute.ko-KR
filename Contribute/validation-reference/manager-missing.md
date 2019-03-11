---
title: manager-missing
description: Docs 빌드 문제 manager-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427827"
---
# <a name="manager-missing"></a>manager-missing

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

일부 콘텐츠 그룹에는 작성자의 관리자를 식별할 수 있는 `manager` 속성이 필요합니다.

## <a name="resolution"></a>해결 방법

`manager`에 대해 유효한 Microsoft 별칭을 추가합니다.

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
