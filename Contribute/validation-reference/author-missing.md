---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236336"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>경고

`Missing attribute: author. Add the current author's GitHub ID.`

`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다. 

## <a name="resolution"></a>해결 방법

다음과 같이 현재 작성자의 GitHub ID를 YML 헤더에 추가합니다.

```yml
---
author: meganbradley
ms.author: mbradley
---
```

소유권이 변경된 경우 이는 원본 작성자가 아니라 문서의 *현재* 소유자이어야 합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
