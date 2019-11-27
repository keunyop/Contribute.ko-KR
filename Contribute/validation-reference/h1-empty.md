---
title: h1-empty
description: Docs 빌드 문제 h1-empty에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528801"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>경고

`H1 is required. Add content to your top-level heading.`

H1은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다. H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.

## <a name="resolution"></a>해결 방법

이 문제를 해결하려면 H1에 해시뿐 아니라 콘텐츠도 포함되어 있는지 확인합니다.

나쁨:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

좋음:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
