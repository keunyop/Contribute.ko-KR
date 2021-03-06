---
title: docs.microsoft.com에 대한 Markdown 참조
description: Microsoft Docs 플랫폼에서 사용되는 Markdown 기능 및 구문을 알아봅니다.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624721"
---
# <a name="docs-markdown-reference"></a>Docs Markdown 참조

이 문서에서는 Docs(docs.microsoft.com) Markdown을 작성하기 위한 사전순 참조를 제공합니다.

[Markdown](https://daringfireball.net/projects/markdown/)은 일반 텍스트 서식 구문을 사용하는 경량 생성 언어입니다. Docs는 [Markdig](https://github.com/lunet-io/markdig) 구문 분석 엔진을 통해 구문 분석된 [CommonMark](https://commonmark.org/) 규격 Markdown을 지원합니다. Docs 사이트에서 더욱 풍부한 콘텐츠를 제공하는 사용자 지정 Markdown 확장도 지원합니다.

Markdown을 작성하는 데는 어떤 텍스트 편집기든 사용할 수 있으나 [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack)이 포함된 [Visual Studio Code](https://code.visualstudio.com/)를 사용하는 것이 좋습니다. Docs Authoring Pack은 편집 도구와 미리 보기 기능을 제공하므로 Docs에서 렌더링하는 경우 문서 모양을 확인할 수 있습니다.

## <a name="alerts-note-tip-important-caution-warning"></a>경고(Note, Tip, Important, Caution, Warning)

경고는 콘텐츠의 중요도를 나타내는 색과 아이콘을 사용하여 docs.microsoft.com에서 렌더링되는 블록 따옴표를 만들기 위한 Markdown 확장입니다. 다음과 같은 경고 유형이 지원됩니다.

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

이러한 경고는 docs.microsoft.com에서 다음과 같이 보입니다.

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>대괄호

예를 들어 자리 표시자를 나타내는 것과 같이 파일에 있는 텍스트에서 꺾쇠 괄호를 사용하는 경우 꺾쇠 괄호를 수동으로 인코딩해야 합니다. 그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.

예를 들어 `<script name>`을 `&lt;script name&gt;` 또는 `\<script name>`으로 인코딩합니다.

인라인 코드 또는 코드 블록으로 서식 지정된 텍스트에서는 꺾쇠 괄호를 이스케이프할 필요가 없습니다.

## <a name="apostrophes-and-quotation-marks"></a>아포스트로피 및 큰따옴표

Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다. 이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다. 그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ&euro;&trade;s

이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.

- 왼쪽(열린) 큰따옴표: `&#8220;`
- 오른쪽(닫힌) 큰따옴표: `&#8221;`
- 오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`
- 왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`

## <a name="blockquotes"></a>Blockquotes

Blockquotes는 `>` 문자를 사용하여 생성됩니다.

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

앞의 예는 다음과 같이 렌더링됩니다.

> 블록 따옴표입니다. 일반적으로 들여쓰기되고 다른 배경색을 사용하도록 렌더링됩니다.

## <a name="bold-and-italic-text"></a>굵게 기울임꼴 텍스트

텍스트에 **굵게** 서식을 지정하려면 두 개의 별표로 텍스트를 묶습니다.

```markdown
This text is **bold**.
```

텍스트에 ‘기울임꼴’ 서식을 지정하려면 한 개의 별표로 텍스트를 묶습니다. 

```markdown
This text is *italic*.
```

텍스트에 ***굵게 및 기울임꼴*** 서식을 둘 다 지정하려면 세 개의 별표로 텍스트를 묶습니다.

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>코드 조각

Docs Markdown에서는 코드 조각을 한 문장 내에 인라인으로 배치하는 것과 문장 사이에 별도의 “펜싱된” 블록으로 배치하는 것을 둘 다 지원합니다. 자세한 내용은 [docs에 코드를 추가하는 방법](code-in-docs.md)을 참조하세요.

## <a name="columns"></a>열

**열** Markdown 확장은 진정한 표 형식 데이터에만 적합한 기본 Markdown 테이블보다 더 유연하고 강력한 열 기반 콘텐츠 레이아웃 추가 기능을 Docs 작성자에게 제공합니다. 최대 네 개의 열을 추가하고 선택적 `span` 특성을 사용하여 두 개 이상의 열을 병합할 수 있습니다.

열에 대한 구문은 다음과 같습니다.

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

열에는 이미지를 비롯하여 기본 Markdown만 포함되어야 합니다. 제목, 테이블, 탭 및 기타 복잡한 구조는 포함되지 않아야 합니다. 행에는 열 외부에 있는 콘텐츠가 포함될 수 없습니다.

예를 들어 다음 Markdown에서는 열 너비 두 개와 표준(`span` 없음) 열 한 개 범위의 열 하나를 만듭니다.

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

이것은 다음과 같이 렌더링됩니다.

:::row:::
   :::column span="2":::
      **텍스트가 많이 포함된 두 개 범위의 열입니다.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **이미지가 포함된 한 개 범위의 열입니다.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>제목

Docs는 6가지 수준의 Markdown 제목을 지원합니다.

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 마지막 `#`과 제목 텍스트 사이에는 공백이 있어야 합니다.
- 각 Markdown 파일에는 H1 제목이 하나만 있어야 합니다.
- H1 제목은 파일에서 YML 메타데이터 블록 다음의 첫 번째 콘텐츠여야 합니다.
- H2 제목은 게시된 파일의 오른쪽 탐색 메뉴에 자동으로 표시됩니다. 더 낮은 수준의 제목은 표시되지 않으므로 H2를 전략적으로 사용하여 독자의 콘텐츠 탐색을 돕습니다.
- `<h1>`과 같은 HTML 제목은 사용하지 않는 것이 좋으며 경우에 따라 빌드 경고가 발생합니다.
- [책갈피 링크](how-to-write-links.md#explicit-anchor-links)를 통해 파일의 개별 제목에 연결할 수 있습니다.

## <a name="html"></a>HTML

Markdown에서는 인라인 HTML을 지원하지만 HTML은 Docs에 게시하는 데 사용하지 않는 것이 좋으며 제한된 값 목록을 제외하고는 빌드 오류 또는 경고가 발생합니다.

## <a name="images"></a>이미지

기본적으로 이미지에 대해 다음 파일 형식이 지원됩니다.

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>표준 개념 이미지(기본 Markdown)

이미지를 포함하기 위한 기본 Markdown 구문은 다음과 같습니다.

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

여기서 `<alt text>`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다. 시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다. 또한 이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.

백슬래시(`\_`)를 접두사로 사용하여 이스케이프하지 않는 경우 대체 텍스트의 밑줄이 제대로 렌더링되지 않습니다. 하지만 파일 이름을 대체 텍스트로 사용하기 위해 복사하지 마세요. 예를 들어 다음은 사용하지 마세요.

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

다음과 같이 작성하세요.

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>표준 개념 이미지(Docs Markdown)

Docs 사용자 지정 `:::image:::` 확장에서는 표준 이미지, 복잡한 이미지 및 아이콘을 지원합니다.

표준 이미지에 계속 이전 Markdown 구문을 사용할 수 있으나 새 확장에서는 부모 항목과 다른 지역화 범위 지정과 같은 더 강력한 기능을 지원하므로 새 확장을 사용하는 것이 좋습니다. 로컬 이미지를 지정하지 않고 공유 이미지 갤러리에서 선택하는 것과 같은 다른 고급 기능은 나중에 사용할 수 있습니다. 새 구문은 다음과 같습니다.

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

`type="content"`(기본값)이면 `source`와 `alt-text`가 둘 다 필요합니다.

### <a name="complex-images-with-long-descriptions"></a>긴 설명이 포함된 복잡한 이미지

이 확장을 사용하여 화면 읽기 프로그램에서 읽을 수 있으나 게시된 페이지에서 시각적으로 렌더링되지 않는 긴 설명이 포함된 이미지도 추가할 수 있습니다. 그래프와 같은 복잡한 이미지의 접근성을 높이기 위해서는 긴 설명이 필요합니다. 구문은 다음과 같습니다.

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

`type="complex"`인 경우 `source`, `alt-text`, 긴 설명 및 `:::image-end:::` 태그가 모두 필요합니다.

### <a name="specifying-loc-scope"></a>loc-scope 지정

이미지가 포함된 문서 또는 모듈의 지역화 범위와 해당 이미지의 지역화 범위가 서로 다른 경우가 있습니다. 이로 인해 글로벌 환경이 잘못되는 경우가 발생할 수 있습니다. 예를 들어 제품의 스크린샷이 해당 제품을 사용할 수 없는 언어로 잘못 지역화되는 경우가 있습니다. 이러한 문제를 방지하기 위해 `content` 및 `complex` 형식의 이미지에 선택적 `loc-scope` 특성을 지정할 수 있습니다.

### <a name="icons"></a>아이콘

이미지 확장에서는 아이콘을 지원합니다. 아이콘은 장식용 이미지이며 대체 텍스트를 포함하지 않아야 합니다. 아이콘 구문은 다음과 같습니다.

```Markdown
:::image type="icon" source="<folderPath>":::
```

`type="icon"`인 경우 `source`만 지정되어야 합니다.

## <a name="included-markdown-files"></a>포함된 Markdown 파일

Markdown 파일이 여러 문서에서 반복되어야 하는 경우 포함 파일을 사용할 수 있습니다. 포함 기능은 빌드할 때 참조를 포함 파일의 콘텐츠로 바꾸도록 Docs에 지시합니다. 포함 기능은 다음과 같은 방법으로 사용할 수 있습니다.

- 인라인: 한 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.
- 블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.

인라인 또는 블록 포함 파일은 Markdown(.md) 파일입니다. 유효한 Markdown을 포함할 수 있습니다. 포함 파일은 대개 리포지토리 루트에 있는 일반적인 ‘포함’ 하위 디렉터리에 있습니다.  문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.

### <a name="includes-syntax"></a>포함 구문

블록 포함은 자체 줄로 표시됩니다.

```markdown
[!INCLUDE [<title>](<filepath>)]
```

인라인 포함은 줄 내에 표시됩니다.

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

여기서, `<title>`은 파일의 이름이고 `<filepath>`는 파일의 상대 경로입니다. `INCLUDE`는 대문자여야 하며 `<title>` 앞에는 공백이 있어야 합니다.

포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.

- 블록 포함되는 내용은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다. 문장보다 작은 단위에 사용하지 않습니다.
- 포함은 Docs 확장을 기반으로 하므로 문서의 GitHub로 렌더링된 보기에서 렌더링되지 않습니다. 게시 후에만 렌더링됩니다.
- 포함 파일의 모든 텍스트는 포함을 참조하는 문서의 앞 텍스트나 뒤 텍스트에 종속되지 않는 완전한 문장 또는 구문으로 작성되어야 합니다. 이 지침을 무시하면 문서에 번역할 수 없는 문자열이 발생합니다.
- 포함 파일이 다른 포함 파일 내에 포함되지 않도록 합니다.
- 미디어 파일을 포함 하위 디렉터리의 미디어 폴더(예: `<repo>` */includes/media* 폴더)에 배치합니다. ‘미디어’ 디렉터리는 해당 루트에 이미지를 포함하지 않아야 합니다.  포함에 이미지가 없는 경우 해당 ‘미디어’ 디렉터리가 필요하지 않습니다. 
- 정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다. 각 포함되는 내용 및 문서에 고유한 이름을 가진 별도의 파일을 사용합니다. 포함되는 내용과 연결된 미디어 폴더에 미디어 파일을 저장합니다.
- 포함되는 내용을 문서의 유일한 콘텐츠로 사용하지 않습니다.  포함되는 내용은 나머지 문서에서 콘텐츠를 보충해야 합니다.

## <a name="links"></a>링크

링크 구문에 대한 자세한 내용은 [설명서에서 링크 사용](how-to-write-links.md)을 참조하세요.

## <a name="lists-numbered-bulleted-checklist"></a>목록(번호 매김, 글머리 기호, 검사 목록)

### <a name="numbered-list"></a>번호 매기기 목록

번호 매기기 목록을 만들기 위해 모두 1을 사용할 수 있습니다. 번호는 게시될 때 오름차순의 순차적 목록으로 렌더링됩니다. 소스 가독성을 높이기 위해 수동으로 목록을 증분할 수 있습니다.

중첩 목록을 포함하여 목록에 문자를 사용하지 마세요. 문자는 Docs에 게시할 때 제대로 렌더링되지 않습니다. 숫자를 사용하여 중첩된 목록은 게시될 때 소문자로 렌더링됩니다. 예:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

이것은 다음과 같이 렌더링됩니다.

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>글머리 기호 목록

글머리 기호 목록을 만들려면 각 줄의 시작 위치에 `-` 또는 `*`와 공백을 사용합니다.

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

이것은 다음과 같이 렌더링됩니다.

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

어떤 구문을 사용하든 문서 내에서 `-` 또는 `*`를 일관성 있게 사용하세요.

### <a name="checklist"></a>검사 목록

검사 목록은 사용자 지정 Markdown 확장을 통해 Docs에서 사용할 수 있습니다.

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

이 예제에서는 다음과 같이 Docs에서 렌더링합니다.

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

문서의 처음이나 끝에 있는 검사 목록을 사용하여 “학습할 내용” 또는 “학습한 내용” 콘텐츠를 요약합니다. 문서 전체에 임의의 검사 목록을 추가하지 마세요.

## <a name="next-step-action"></a>다음 단계 작업

사용자 지정 확장을 사용하여 Docs 페이지에 다음 단계 작업 단추를 추가할 수 있습니다.

구문은 다음과 같습니다.

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

예:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

이것은 다음과 같이 렌더링됩니다.

> [!div class="nextstepaction"]
> [문서에 코드를 추가하는 방법 알아보기](code-in-docs.md)

다른 웹 페이지에 대한 Markdown 링크를 포함하여 다음 단계 작업에서 지원되는 링크를 사용할 수 있습니다. 대부분의 경우 다음 작업 링크는 동일한 문서 집합에 있는 다른 파일에 대한 상대 링크입니다.

## <a name="non-localized-strings"></a>지역화되지 않은 문자열

사용자 지정 `no-loc` Markdown 확장을 사용하여 지역화 프로세스에서 무시할 콘텐츠 문자열을 식별할 수 있습니다.

호출되는 모든 문자열은 대/소문자를 구분합니다. 즉, 지역화에서 무시되려면 문자열이 정확하게 일치해야 합니다.

개별 문자열을 지역화 불가능으로 표시하려면 다음 구문을 사용합니다.

```markdown
:::no-loc text="String":::
```

예를 들어 다음에서 `Document`의 단일 인스턴스만 지역화 프로세스 중에 무시됩니다.

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> `\`를 사용하여 특수 문자를 이스케이프하세요.
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

YAML 헤더의 메타데이터를 사용하여 현재 Markdown 파일 내에 있는 한 문자열의 모든 인스턴스를 지역화 불가능으로 표시할 수도 있습니다.

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> no-loc 메타데이터는 *docfx.json* 파일의 글로벌 메타데이터로 지원되지 않습니다. 지역화 파이프라인에서 *docfx.json* 파일을 읽지 않으므로 각 개별 소스 파일에 no-loc 메타데이터를 추가해야 합니다.

다음 예제에서는 메타데이터 `title` 및 Markdown 헤더 둘 다에서 지역화 프로세스 중에 `Document`라는 단어를 무시합니다.

메타데이터 `description` 및 Markdown 주 콘텐츠에 있는 `document` 단어는 대문자 `D`로 시작하지 않기 때문에 지역화됩니다.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>선택기

선택기는 사용자가 동일한 문서의 여러 버전 간에 전환할 수 있도록 해주는 UI 요소입니다. 일부 문서 집합에서는 기술 또는 플랫폼 간의 구현 차이를 해결하는 데 사용됩니다. 선택기는 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.

동일한 선택기 Markdown은 선택기를 사용하는 각 문서 파일에 포함되므로 문서 선택기를 포함 파일에 배치하는 것이 좋습니다. 그러면 동일한 선택기를 사용하는 모든 문서 파일에서 해당 포함 파일을 참조할 수 있습니다.

선택기의 종류에는 단일 선택기와 다중 선택기 두 가지가 있습니다.

### <a name="single-selector"></a>단일 선택기

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

다음과 같이 렌더링됩니다.

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>다중 선택기

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

다음과 같이 렌더링됩니다.

> [!div class="op_multi_selector" title1="플랫폼" title2="백 엔드"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>아래 첨자 및 위 첨자

아래 첨자나 위 첨자는 수학적 수식에 대한 문서를 작성하는 경우와 같이 기술적 정확도를 위해 필요한 경우에만 사용해야 합니다. 각주와 같은 비표준 스타일에는 사용하지 마세요.

아래 첨자 및 위 첨자 둘 다 HTML을 사용합니다.

```html
Hello <sub>This is subscript!</sub>
```

이것은 다음과 같이 렌더링됩니다.

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

이것은 다음과 같이 렌더링됩니다.

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Tables

Markdown에서 테이블을 만드는 가장 간단한 방법은 파이프 및 줄을 사용하는 것입니다. 헤더가 있는 표준 테이블을 만들려면 첫 번째 선을 파선으로 그립니다.

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

이것은 다음과 같이 렌더링됩니다.

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

콜론을 사용하여 열을 정렬할 수 있습니다.

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

다음과 같이 렌더링됩니다.

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> VS Code용 Docs Authoring Extension을 사용하면 기본 Markdown 테이블을 쉽게 추가할 수 있습니다!
>
> [온라인 테이블 생성기](http://www.tablesgenerator.com/markdown_tables)를 사용할 수도 있습니다.

### <a name="line-breaks-within-words-in-any-table-cell"></a>테이블 셀에 있는 단어 내 줄 바꿈

Markdown 테이블에 긴 단어가 있으면 테이블이 오른쪽 탐색으로 확장되어 읽지 못하게 될 수도 있습니다. 필요한 경우 Docs 렌더링에서 단어 내에 줄 바꿈을 자동으로 삽입하도록 허용하여 이 문제를 해결할 수 있습니다. `[!div class="mx-tdBreakAll"]` 사용자 지정 클래스로 테이블을 래핑하기만 하면 됩니다.

다음은 클래스 이름이 `mx-tdBreakAll`인 `div`로 래핑될 행이 세 개인 테이블의 Markdown 샘플입니다.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

다음과 같이 렌더링됩니다.

> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>두 번째 열 테이블 셀에 있는 단어 내 줄 바꿈

테이블의 두 번째 열에 있는 단어 내에서만 줄 바꿈이 자동으로 삽입되도록 할 수 있습니다. 줄 바꿈을 두 번째 열로 제한하려면 앞에 표시된 대로 `div` 래퍼 구문을 사용하여 `mx-tdCol2BreakAll` 클래스를 적용합니다.

### <a name="data-matrix-tables"></a>데이터 행렬 테이블

데이터 행렬 테이블에는 헤더와 첫 번째 가중 열이 둘 다 있으므로 왼쪽 상단에 빈 셀이 있는 행렬을 만듭니다. 문서에는 데이터 행렬 테이블에 대한 사용자 지정 Markdown이 있습니다.

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

첫 번째 열의 모든 항목은 '굵게'(`**bold**`)로 스타일을 지정해야 합니다. 그렇지 않으면 화면 읽기 프로그램에서 테이블에 액세스할 수 없거나 문서가 유효하지 않습니다.

### <a name="html-tables"></a>HTML 테이블

HTML 테이블은 docs.microsoft.com에 사용하지 않는 것이 좋습니다. 사용자가 소스를 읽을 수 없습니다. 사용자가 소스를 읽을 수 없도록 하는 것이 Markdown의 핵심 원칙입니다.
