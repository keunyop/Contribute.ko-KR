---
title: h1-no-space
description: Docs 빌드 문제 h1-no-space에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528971"
---
# <a name="h1-no-space"></a>h1-no-space

## <a name="warning"></a>경고

`A space is required after the hash (#) in H1.`

H1은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다. H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다. 해시 뒤에 공백이 없으면 문서는 H1을 인식하지 못합니다.

## <a name="resolution"></a>해결 방법

이 오류를 해결하려면 H1의 해시 뒤에 공백을 추가합니다.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
