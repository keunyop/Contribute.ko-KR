---
title: yaml-header-invalid
description: Docs 빌드 문제 yaml-header-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459030"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>경고

`Invalid YAML header: Improper use of a colon in a metadata entry.`

일반적으로 YAML 헤더의 따옴표가 없는 메타데이터 값에는 콜론이나 다른 특수 문자가 포함됩니다. 키/값 쌍의 콜론 뒤에 공백이 누락되었다는 것을 의미할 수도 있습니다.

## <a name="resolution"></a>해결 방법

YAML 헤더를 검토합니다. 다음 오류를 찾습니다.

따옴표가 없는 값의 콜론:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

변경 대상:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

키/값 쌍의 콜론 뒤에 공백 없음:

```yml
---
title:I omitted a space.
---
```

변경 대상:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
