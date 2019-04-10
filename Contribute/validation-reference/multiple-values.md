---
title: multiple-values
description: Docs 빌드 문제 multiple-values에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899662"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

값이 하나만 허용되는 특성에 둘 이상의 값을 지정했습니다.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

둘 이상의 값이 허용되지 않는 특성은 단일 값(스칼라) YML 형식으로 지정해야 합니다.

## <a name="resolution"></a>해결 방법

다중 값 배열이 단일 값 특성(여러 값이 포함되었거나 배열의 단일 값)에 사용될 때마다 이 제안을 받습니다.

YML은 다중 값 특성(예: `ms.custom`)에 다음과 같은 배열 형식을 지원합니다.

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

해당 형식은 단일 값 특성(예: `author`)에는 유효하지 않습니다.

다중 값을 지정한 경우 지정된 값을 검토하고 어떤 값이 올바른지 확인합니다. 다른 값을 제거하고 다음과 같이 대괄호 없이 특성과 같은 줄에 단일 값을 지정합니다.

```yml
---
author: meganbradley
---
```

단일 값 배열이 있는 경우 위의 스칼라 형식으로 변경합니다.

## <a name="attributes-in-scope"></a>범위 내 특성

다음 특성은 단일 값이어야 합니다.

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
