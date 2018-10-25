---
title: Markdown 제목
description: Markdown 제목에 필요한 요구 사항을 설명합니다.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084558"
---
# <a name="markdown-headings"></a>Markdown 제목

다음 유효성 검사 요구 사항이 OPS Markdown 파일의 제목에 적용됩니다.

## <a name="h1"></a>H1

`H1`은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.

H1은 단일 해시(`#`), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다. 예를 들어 이 문서의 H1은 다음과 같습니다.

```md
# Markdown headings
```

H1 제목에는 다음 규칙이 적용됩니다.

- 파일에 H1이 있어야 합니다.
- 하나의 H1만 사용할 수 있습니다.
- H1에 콘텐츠가 있어야 합니다.

  ```markdown
  # 
  This is not allowed.
  ```
- `#`과 H1 콘텐츠 사이에 공백이 있어야 합니다. 공백이 없는 H1은 게시된 페이지에서 제목으로 렌더링되지 않습니다.

  ```markdown
  #This looks bad on the site.
  ```
- H1은 파일에서 YML 메타데이터 헤더 다음의 첫 번째 콘텐츠여야 합니다. 텍스트나 이미지와 같은 콘텐츠는 YML 헤더의 끝과 H1 사이에 사용할 수 없습니다.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- 첫 번째 수준 제목에 대한 HTML 요소 `<h1>`은 사용하지 않아야 합니다. Markdown 구문(`# `)을 사용하세요.
- H1은 100자 이하여야 합니다. 스타일 지침입니다.

## <a name="h2---h6"></a>H2 - H6

H2(`## `)-H6(`###### `)는 OPS에서 사용할 수 있습니다. 제목을 만들려면 HTML(`<h2>` - `<h6>`)을 사용하지 말고 Markdown 헤더를 사용하세요.
