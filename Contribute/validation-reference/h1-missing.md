---
title: h1-missing
description: Docs 빌드 문제 h1-missing에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459122"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>경고

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
> 이 규칙은 포함된 파일에는 적용되지 않습니다. 포함된 파일에 H1 경고를 받게 되면 포함된 파일을 `includes` 폴더로 이동해야 합니다. `includes` 폴더는 파일 경로의 모든 수준에 있을 수 있습니다. 경로에 따라 문서 빌드는 파일을 포함된 파일로 인식하고 H1 유효성 검사는 실행되지 않습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]