---
title: docs.microsoft.com에 대한 Markdown 참조
description: Microsoft Docs 플랫폼에서 사용되는 Markdown 기능 및 구문을 알아봅니다.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 452cbf97db748532ae2b0e09b4bb558c8f757a61
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188261"
---
# <a name="markdown-reference"></a>Markdown 참조

Markdown은 일반 텍스트 서식 구문을 사용하는 경량 생성 언어입니다. Docs 플랫폼은 Markdown에 대한 CommonMark 표준과 docs.microsoft.com에서 더 풍부한 콘텐츠를 제공하도록 설계된 사용자 지정 Markdown 확장을 지원합니다. 이 문서에서는 docs.microsoft.com에 대해 Markdown을 사용하기 위한 사전순 참조를 제공합니다.

텍스트 편집기를 사용하여 Markdown을 작성할 수 있습니다. 표준 Markdown 구문과 사용자 지정 Docs 확장을 쉽게 삽입할 수 있는 편집기의 경우 [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack)이 설치된 [VS Code](https://code.visualstudio.com/)를 사용하는 것이 좋습니다.

Docs에서는 Markdig Markdown 엔진을 사용합니다. [https://babelmark.github.io/](https://babelmark.github.io/)에서 Markdig 및 기타 엔진에 대한 Markdown의 렌더링을 테스트할 수 있습니다.

## <a name="alerts-note-tip-important-caution-warning"></a>경고(Note, Tip, Important, Caution, Warning)

Docs Markdown 확장을 경고하여 docs.microsoft.com에서 콘텐츠의 중요도를 색과 아이콘으로 표시하여 렌더링하는 블록 따옴표를 만듭니다. 다음과 같은 경고 유형이 지원됩니다.

```md
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

![게시된 Docs 페이지에서 이전 예제의 경고가 다른 아이콘 및 색으로 어떻게 표시되는지를 보여 주는 이미지](media/alerts-rendering.png)

## <a name="code-snippets"></a>코드 조각

Markdown 파일에 코드 조각을 포함할 수 있습니다.

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>제목

Docs는 6가지 수준의 Markdown 제목을 지원합니다.

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 마지막 `#`과 제목 텍스트 사이에는 공백이 있어야 합니다.
- 각 Markdown 파일에는 H1이 하나만 있어야 합니다.
- H1은 파일에서 YML 메타데이터 블록 다음의 첫 번째 콘텐츠여야 합니다.
- H2는 게시된 파일의 오른쪽 탐색 메뉴에 자동으로 나타납니다. 하위 수준의 제목은 그렇지 않으므로 H2를 전략적으로 사용하여 독자가 콘텐츠를 탐색하는 것을 돕습니다.
- `<h1>`과 같은 HTML 제목은 권장되지 않으며 경우에 따라 빌드 경고가 발생합니다.
- [책갈피](#bookmark-links)를 통해 파일의 개별 제목에 연결할 수 있습니다.

## <a name="html"></a>HTML

Markdown은 인라인 HTML을 지원하지만 HTML은 Docs에 게시하도록 권장되지 않으며 제한된 값 목록을 제외하고는 빌드 오류 또는 경고가 발생합니다.

## <a name="images"></a>이미지

이미지를 포함하는 구문은 다음과 같습니다.

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

여기서 `alt text`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다. 시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다. 또한 이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.

이미지는 문서 집합 내의 `/media` 폴더에 저장해야 합니다. 기본적으로 이미지에 대해 다음 파일 형식이 지원됩니다.

- .jpg
- .png

문서 세트의 docfx.json 파일에 리소스로 추가하여 다른 이미지 형식에 대한 지원을<!--add link to reference when available--> 추가할 수 있습니다.

## <a name="links"></a>링크

대부분의 경우 Docs는 다른 파일 및 페이지에 대한 표준 Markdown 링크를 사용합니다. 링크 유형은 아래의 하위 섹션에서 설명합니다.

> [!TIP]
> VS Code용 Docs Authoring Pack은 경로를 찾는 번거로움 없이 상대 링크와 책갈피를 올바르게 삽입하는 데 도움을 줄 수 있습니다.

> [!IMPORTANT]
> Microsoft 사이트에 대한 링크에 ko-kr와 같은 로캘 코드를 포함하지 마세요. 하드 코딩된 로캘 코드는 지역화된 콘텐츠가 렌더링되지 못하게 합니다. 이는 다른 로캘의 사용자에게 좋지 않은 고객 환경이며 상당한 지역화 비용이 발생합니다. 브라우저에서 URL을 복사하면 로캘 코드가 기본적으로 포함되므로 링크를 만들 때 수동으로 삭제해야 합니다. 예를 들어 다음을 사용합니다.
>
> `[Microsoft](https://www.microsoft.com)`
>
> 다음을 사용하지 않습니다.
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>동일한 문서 집합에서 파일에 대한 상대 링크

상대 경로는 현재 파일을 기준으로 대상 파일에 대한 경로입니다. Docs에서는 상대 경로를 사용하여 동일한 문서 세트 내의 다른 파일에 연결할 수 있습니다. 상대 경로에 대한 구문은 다음과 같습니다.

```md
[link text](../../folder/filename.md)
```

여기서 `../`는 계층 구조에서 한 수준 위를 나타냅니다.

- 상대 경로는 빌드 중에 .md 확장명 제거를 포함하여 확인됩니다.
- “../”를 사용하여 부모 폴더의 파일에 연결할 수 있지만, 해당 파일이 같은 문서 집합에 있어야 합니다. “../”를 사용하여 다른 문서 집합 폴더의 파일에 연결할 수는 없습니다.
- Docs는 또한 "~"로 시작하는 특별한 양식의 상대 경로(예: ~/foo/bar.md)도 지원됩니다. 이 구문은 문서 집합의 루트 폴더를 기준으로 한 파일임을 나타냅니다. 이러한 종류의 경로도 빌드 중에 유효성이 검사되고 확인됩니다.

> [!IMPORTANT]
> 상대 경로에 파일 확장명을 포함합니다. 빌드는 상대 경로의 대상 파일이 있는지를 확인합니다. 상대 경로에 파일 확장명이 포함되어 있지 않으면 빌드가 끊어진 링크 경고를 보고합니다. 예를 들어 다음을 사용합니다.
>
> `[link text](../../folder/filename.md)`
>
> 다음을 사용하지 않습니다.
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Docs의 다른 파일에 대한 사이트 상대 경로

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

파일 확장명(.md)을 포함하지 마세요. 이것은 Azure “articles” 문서 집합 외부의 Linux 개요 파일에 연결됩니다.

### <a name="links-to-external-sites"></a>외부 사이트로 연결

```md
[Microsoft](https://www.microsoft.com)
```

다른 웹 페이지로 URL 기반 연결(https://를 포함해야 함)입니다.

### <a name="bookmark-links"></a>책갈피 링크

같은 리포지토리의 다른 파일 제목에 대한 책갈피 링크입니다. 예:

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

현재 파일의 제목에 대한 책갈피 링크

```md
[Managed Disks](#managed-disks)
```

`#` 해시 표시 뒤에 제목의 단어를 사용합니다. 제목 텍스트를 링크 텍스트로 변경하려면 다음을 적용합니다.
- 모두 소문자 사용
- 문장 부호 제거
- 공백을 대시로 바꾸기

예를 들어, 제목 이름이 "2.2 Security concerns"인 경우 책갈피 링크 텍스트는 "#22-security-concerns"입니다.

### <a name="explicit-anchor-links"></a>명시적 앵커 링크

허브 및 방문 페이지를 제외하고는 `<a>` HTML 태그를 사용하는 명시적 앵커 링크가 **필요하거나 권장되지 않습니다.** 일반 Markdown 파일에 위에서 설명한 대로 책갈피를 사용하세요. 허브 및 방문 페이지의 경우 다음과 같이 앵커를 사용하세요.

`## <a id="AnchorText"> </a>Header text` 또는 `## <a name="AnchorText"> </a>Header text`

명시적 앵커에 연결하려면 다음 구문을 사용합니다.

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>XREF(상호 참조) 링크

현재 문서 집합 또는 다른 문서 집합에서 자동 생성된 API 참조 페이지에 연결하려면 UID(고유한 ID)와 함께 XREF 링크를 사용합니다.

> [!NOTE]
> 다른 문서 집합에서 API 참조 페이지를 참조하려면 `docfx.json` 파일에서 `xrefService` 구성을 추가해야 합니다.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

UID는 정규화된 클래스 및 멤버 이름과 같습니다. UID 뒤에 *를 추가하면 링크는 특정 API가 아닌 오버로드 페이지를 나타냅니다. 예를 들어 `List<T>.BinarySearch*`를 사용하여 `List<T>.BinarySearch(T, IComparer<T>)`와 같은 특정 과부하로 연결하는 대신 BinarySearch 메서드 페이지에 연결합니다.

다음 구문 중 하나를 사용할 수 있습니다.

- 자동 연결: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  선택적 `displayProperty` 쿼리 매개 변수는 정규화된 링크 텍스트를 생성합니다. 기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.

- Markdown 링크: `[link text](xref:UID)`
  
  표시되는 링크 텍스트를 사용자 지정하려면 사용합니다.

예제:

- `<xref:System.String>`은 “String”으로 렌더링됩니다.
- `<xref:System.String?displayProperty=nameWithType>`은 “System.String”으로 렌더링됩니다.
- `[String class](xref:System.String)`는 “String class”로 렌더링됩니다.

지금은 UID를 쉽게 찾는 방법이 없습니다. <!-- ? -->API의 UID를 찾는 가장 좋은 방법은 연결하려는 API 페이지의 소스를 보고 ms.assetid 값을 찾는 것입니다. 개별 오버로드 값은 소스에 표시되지 않습니다. Microsoft는 시스템 개선을 위해 노력하고 있습니다.

UID에 특수 문자 \`, \# 또는 \*이 포함되는 경우 UID 값을 `%60`, `%23` 및 `%2A`로 각각 HTML 인코딩해야 합니다. 때때로 괄호 인코딩을 보게 되겠지만 이는 필요하지 않습니다.

예제:

- System.Threading.Tasks.Task\`1은 `System.Threading.Tasks.Task%601`이 됩니다.
- System.Exception.\#ctor은 `System.Exception.%23ctor`이 됩니다.
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode)은 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`가 됩니다.

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>목록(번호 매김, 글머리 기호, 검사 목록)

### <a name="numbered-list"></a>번호 매기기 목록

번호 매기기 목록을 만들려면, 모두 1을 사용할 수 있으며 이것은 게시할 때 순차 목록으로 렌더링됩니다. 소스 가독성을 높이기 위해 목록을 증가시킬 수 있습니다.

중첩 목록을 포함하여 목록에 문자를 사용하지 마세요. Docs에 게시할 때 올바르게 렌더링되지 않습니다. 숫자를 사용하여 중첩된 목록은 게시될 때 소문자로 렌더링됩니다. 예:

```md
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

글머리 기호 목록을 만들려면 각 줄의 시작 위치에 `-`와 공백을 사용합니다.

```md
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

### <a name="checklist"></a>검사 목록

검사 목록은 사용자 지정 Markdown 확장을 통해 docs.microsoft.com에서만 사용할 수 있습니다.

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

이 예제는 다음과 같이 docs.microsoft.com에서 렌더링됩니다.

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

문서의 처음이나 끝에 있는 검사 목록을 사용하여 “학습할 내용” 또는 “학습한 내용” 콘텐츠를 요약합니다. 문서 전체에 임의의 검사 목록을 추가하지 마세요.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>다음 단계 작업

사용자 지정 확장 프로그램을 사용하여 docs.microsoft.com의 페이지에만 다음 단계 작업 단추를 추가할 수 있습니다.

구문은 다음과 같습니다.

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

예:

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

이것은 다음과 같이 렌더링됩니다.

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

다른 웹 페이지에 대한 Markdown 링크를 포함하여 다음 단계 작업에서 지원되는 링크를 사용할 수 있습니다. 대부분의 경우 다음 작업 링크는 동일한 문서 집합에 있는 다른 파일에 대한 상대 링크입니다.

## <a name="section-definition"></a>섹션 정의

<!-- more info about this would be helpful! -->
섹션을 정의해야 하는 경우가 있습니다. 이 구문은 대개 코드 테이블에 사용됩니다.
다음 예제를 참조하세요.

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

앞의 blockquote Markdown 텍스트는 다음과 같이 렌더링됩니다.
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>선택기

<!-- could be more clear! -->
같은 문서의 다른 페이지에 연결할 때 선택기를 사용할 수 있습니다. 그러면 독자는 해당 페이지 간에 전환할 수 있습니다.

> [!NOTE]
> 이 확장은 docs.microsoft.com과 MSDN에서 서로 다르게 작동합니다. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>단일 선택기

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

다음과 같이 렌더링됩니다.

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>다중 선택기

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

다음과 같이 렌더링됩니다.

> [!div class="op_multi_selector" title1="플랫폼" title2="백 엔드"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a>테이블

Markdown에서 테이블을 만드는 가장 간단한 방법은 파이프 및 줄을 사용하는 것입니다. 헤더가 있는 표준 테이블을 만들려면 첫 번째 선을 파선으로 그립니다.

```md
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

헤더가 없는 테이블을 만들 수도 있습니다. 예를 들어 다중 열 목록을 만들려면:

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

다음과 같이 렌더링됩니다.

|   |   |
| - | - |
| This | table |
| has no | header |

콜론을 사용하여 열을 정렬할 수 있습니다.

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

다음과 같이 렌더링됩니다.

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> VS Code용 Docs Authoring Extension을 사용하면 기본 Markdown 테이블을 쉽게 추가할 수 있습니다!
>
> [온라인 테이블 생성기](http://www.tablesgenerator.com/markdown_tables)를 사용할 수도 있습니다.

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> 이것은 docs.microsoft.com 사이트에서만 작동합니다.

Markdown에서 테이블을 만드는 경우 테이블이 오른쪽 탐색으로 확장되어 읽을 수 없게 될 수도 있습니다. 필요한 경우 문서 렌더링에서 테이블을 나눌 수 있도록 허용하여 이 문제를 해결할 수 있습니다. `[!div class="mx-tdBreakAll"]` 사용자 지정 클래스로 테이블을 래핑하기만 하면 됩니다.

다음은 클래스 이름이 `mx-tdBreakAll`인 `div`로 래핑될 행이 세 개인 테이블의 Markdown 샘플입니다.

```md
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

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> 이것은 docs.microsoft.com 사이트에서만 작동합니다.

때때로 테이블의 두 번째 열에 매우 긴 단어가 표시될 수 있습니다. 이것을 깔끔하게 분리하려면 앞서 보았듯이 `div` 래퍼 구문을 사용하여 `mx-tdCol2BreakAll` 클래스를 적용하면 됩니다.

### <a name="html-tables"></a>HTML 테이블

HTML 테이블은 docs.microsoft.com에 사용하지 않는 것이 좋습니다. 소스에서 사람이 읽을 수 없으며 이것이 Markdown의 핵심 원칙입니다.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>비디오

### <a name="embedding-videos-into-a-markdown-page"></a>Markdown 페이지에 비디오 포함

현재 Docs는 다음 3개 위치 중 하나에 게시된 비디오를 지원할 수 있습니다.

- YouTube
- Channel9
- Microsoft 고유 'One Player' 시스템

다음 구문으로 비디오를 포함할 수 있으며, 그러면 Docs에서 렌더링합니다.

```md
> [!VIDEO <embedded_video_link>]
```

예제:

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

다음과 같이 렌더링됩니다.

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

그리고 게시된 페이지에 다음과 같이 표시됩니다.

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> CH9 비디오 URL은 `https`로 시작하고 `/player`로 끝나야 합니다. 그렇지 않으면 비디오만이 아니라 전체 페이지를 포함하게 됩니다.

### <a name="uploading-new-videos"></a>새 비디오 업로딩

모든 새 비디오는 다음 프로세스에 따라 업로드해야 합니다.

1. IDWEB에서 **docs_video_users** 그룹에 조인합니다.
1. [https://aka.ms/VideoUploadRequest](https://aka.ms/VideoUploadRequest )로 이동하고 비디오에 대한 세부 사항을 입력합니다. 다음이 필요합니다(이러한 항목은 공개되지 않음).
    1. 비디오의 제목
    1. 비디오가 관련된 제품/서비스 목록
    1. 비디오가 호스트되는 대상 페이지 또는 (아직 페이지가 없는 경우) 문서 집합
    1. 비디오에 대한 MP4 파일 링크(파일을 배치할 위치가 없으면 임시로 여기에 배치할 수 있음: `\\scratch2\scratch\apex`). MP4 파일은 720p 이상이어야 합니다.
    1. 비디오 설명
1. 항목을 제출(저장)합니다.
1. 2 영업일 이내에 비디오가 업로드됩니다. 포함에 필요한 링크가 작업 항목에 배치되고 확인되어 *전달됩니다*.
1. 비디오 링크를 얻었으면 작업 항목을 닫습니다.
1. 다음 구문을 사용하여 비디오 링크를 게시물에 추가할 수 있습니다.

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
