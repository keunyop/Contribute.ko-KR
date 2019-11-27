---
title: h1-missing
description: Docs 빌드 문제 h1-missing에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528887"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다. H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.

## <a name="resolution"></a>해결 방법

이 문제를 해결하려면 파일의 YML 메타데이터 블록 다음에 H1을 첫 번째 콘텐츠로 추가합니다.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> 이 규칙은 포함된 파일에는 적용되지 않습니다. 포함된 파일에 H1 결과를 받게 되면 포함된 파일을 `includes` 폴더로 이동해야 합니다. `includes` 폴더는 파일 경로의 모든 수준에 있을 수 있습니다. 경로에 따라 문서 빌드는 파일을 포함된 파일로 인식하고 H1 유효성 검사는 실행되지 않습니다.
>
> 부모 파일에서 H1이 누락되는 일반적인 원인으로 포함된 파일의 잘못된 사용이 있습니다. 즉, H1이 포함된 파일에 있지만 부모 파일에는 없는 경우입니다. 이 경우는 허용되지 않습니다. 포함된 파일에서 H1을 사용하는 것은 부모 파일에 중복된 H1이 있거나, 포함된 파일을 한 번만 사용함을 의미하기 때문입니다. H1은 콘텐츠 세트 내에서 고유해야 하며, 여러 파일 간에 콘텐츠를 공유하는 데만 포함된 파일을 사용해야 합니다. H1이 포함된 파일에 있어서 `h1-missing` 결과를 받는 경우에는 H1뿐만 아니라 포함된 모든 콘텐츠(포함된 파일을 한 번만 사용하는 경우)를 부모 파일로 이동하여 해결할 수 있습니다. Docs의 포함된 파일에 대한 자세한 내용은 Microsoft 내부 문서인 [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)(문서에서 재사용 가능 콘텐츠 포함)를 참조하세요.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
