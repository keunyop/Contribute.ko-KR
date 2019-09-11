---
title: multiple-h1
description: Docs 빌드 문제 multiple-h1에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848593"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다. H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다. 각 파일에는 하나의 H1만 있을 수 있습니다.

## <a name="resolution"></a>해결 방법

이 문제를 해결하려면 후속 H1의 제목 수준을 H2(`##`)로 변경하거나 그렇지 않으면 파일을 재구성합니다. H3에서 H1을 팔로우하는 것과 같이 제목 수준을 건너뛰는 것은 허용되지 않습니다.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]