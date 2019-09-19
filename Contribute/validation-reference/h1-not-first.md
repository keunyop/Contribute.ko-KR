---
title: h1-not-first
description: Docs 빌드 문제 h1-not-first에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895465"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Markdown content is not allowed before H1.`

markdown 파일에서 YAML 메타데이터 헤더만 H1 앞에 올 수 있습니다. 예를 들어, 문서 맨 위에 추가하려는 메모나 이미지는 H1 뒤에 와야 합니다. 다음은 허용되지 않습니다.

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

대신 다음을 수행합니다.

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

본 문제의 다른 일반적인 원인으로는 YAML 헤더 앞에 오는 [BOM(바이트 순서 표시)](http://www.websina.com/bugzero/kb/unicode-bom.html)이 있습니다. 콘텐츠를 리포지토리에 커밋할 때 가끔 이러한 BOM에 인코딩 문제가 발생합니다. 이로 인해 GitHub에서 잘못된 렌더링이 발생하므로 해당 BOM을 제거해야 합니다.

## <a name="resolution"></a>해결 방법

H1 앞에 오는 YAML 메타데이터 헤더를 제외한 모든 콘텐츠를 제거합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
