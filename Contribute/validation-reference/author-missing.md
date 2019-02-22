---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431533"
---
# <a name="author-missing"></a>author-missing

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Missing attribute: author. Add a valid GitHub ID.`

`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다. 

## <a name="resolution"></a>해결 방법

다음과 같이 작성자의 GitHub ID를 YML 헤더에 추가합니다.

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]