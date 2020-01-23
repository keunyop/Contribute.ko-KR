---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111051"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Markdown을 사용하여 Docs를 작성하는 방법

[Docs.microsoft.com](https://docs.microsoft.com) 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다. 그렇기 때문에 신속하게 산업 표준이 되고 있습니다. 문서 사이트는 Markdown의 [Markdig 유형](#markdown-flavor)을 사용합니다.


## <a name="markdown-basics"></a>Markdown 기본 사항

### <a name="headings"></a>제목

제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

제목은 atx-style을 사용하여 수행해야 합니다. 즉, 줄의 시작 부분에 1-6 해시 문자(#)를 사용하여 HTML 제목 수준 H1~H6에 해당하는 제목을 표시합니다. 위의 1~4번째 수준 헤더의 예가 사용됩니다.

항목에는 첫 번째 수준 제목(H1)이 하나만 **있어야 하며**, 해당 페이지 제목으로 표시됩니다.

제목이 `#` 문자로 끝나는 경우 제목을 올바르게 랜더링하려면 끝에 나머지 `#` 문자를 추가해야 합니다. 예: `# Async Programming in F# #`.

두 번째 수준 제목은 해당 페이지 제목 아래의 “이 문서의 내용” 섹션에 나타나는 해당 페이지의 TOC를 생성합니다.

### <a name="bold-and-italic-text"></a>굵게 기울임꼴 텍스트

텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.

```md
This text is **bold**.
```

텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.

```md
This text is *italic*.
```

텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Blockquotes

Blockquotes는 `>` 문자를 사용하여 생성됩니다.

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

앞의 예는 다음과 같이 렌더링됩니다.

> 가뭄은 지금 천만년 동안 지속되었고 끔찍한 도마뱀의 통치는 끝난 지 오래되었습니다. 언젠가 아프리카로 알려질 이 적도에서 생존을 위한 투쟁은 새로운 격렬한 절정에 이르렀고, 승자는 아직 보이지 않았습니다. 이 황량하고 메마른 땅에서는 작고 빠르거나 사나운 존재만이 번성하거나 생존할 수 있을 뿐입니다.

### <a name="lists"></a>목록

#### <a name="unordered-list"></a>정렬되지 않은 목록

정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다. 예를 들어 아래 Markdown은

```md
- List item 1
- List item 2
- List item 3
```

다음과 같이 렌더링됩니다.

- List item 1
- List item 2
- List item 3

다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다. 예를 들어 아래 Markdown은

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

다음과 같이 렌더링됩니다.

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>정렬된 목록

정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다. 예를 들어 아래 Markdown은

```md
1. First instruction
1. Second instruction
1. Third instruction
```

다음과 같이 렌더링됩니다.

1. First instruction
2. Second instruction
3. Third instruction

다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다. 예를 들어 아래 Markdown은

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

다음과 같이 렌더링됩니다.

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

'1'을 모든 항목에 대해 사용합니다. 최신 업데이트에 새 단계가 포함되거나 기존 단계가 제거될 때 더 쉽게 검토할 수 있습니다.

### <a name="tables"></a>Tables

테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다. 파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다. 하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다. 테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.

예를 들어 아래 Markdown은

```md
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

테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.

- GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)
- [Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱
- [Adam Pritchard의 Markdown 참고 자료](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Michel Fortin의 Markdown 추가 자료](https://michelf.ca/projects/php-markdown/extra/#table)
- [HTML 테이블을 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>링크

인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.

 `[link text](file-name.md)`

연결에 대한 자세한 내용은 다음을 참조하세요.

- Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)
- 이 가이드의 [링크](how-to-write-links.md) 페이지에 Markdig에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.

### <a name="code-snippets"></a>코드 조각

Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다. 자세한 내용은 다음을 참조하세요.

- [코드 블록에 대한 Markdown의 네이티브 지원](https://daringfireball.net/projects/markdown/syntax#precode)
- [코드 펜싱 및 구문 강조 표시에 대한 GFM 지원](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다. 펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.

    ```alias
    ...
    your code goes in here
    ...
    ```

처음 세 개의 억음 악센트 기호(\`) 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다. Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.

이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.

|Name|Markdown 레이블|
|-----|-------|
|.NET 콘솔|dotnetcli|
|ASP.NET(C#)|aspx-csharp|
|ASP.NET(VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|브라우저의 C#|csharp-interactive|
|콘솔|콘솔|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Kusto 쿼리 언어|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps(점 10진 구분 기호)|powerapps-dot|
|PowerApps(쉼표 10진 구분 기호)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

`csharp-interactive` 이름은 C# 언어와 브라우저에서 샘플을 실행하는 기능을 지정합니다. 이러한 코드 조각은 Docker 컨테이너에서 컴파일되고 실행되며, 해당 프로그램 실행 결과는 사용자의 브라우저 창에 표시됩니다.

#### <a name="example-c"></a>예제: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__렌더링__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>예제: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__렌더링__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a>Docs 사용자 지정 Markdown 확장

> [!NOTE]
> Docs.Microsoft.com(Docs)은 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다. Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다. 이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다. (예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)

Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다. 더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.

- 참고 블록
- 포함 파일
- 선택기
- 포함된 비디오
- 코드 조각/샘플

전체 목록은 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.

### <a name="note-blocks"></a>참고 블록

특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.

- 참고
- 경고
- 팁
- 중요

일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다. 참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.

예제:

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

### <a name="include-files"></a>포함되는 파일

문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는" 파일에 대한 참조를 사용할 수 있습니다. 이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다. 콘텐츠를 재사용하기 위해 사용 가능한 포함되는 참조에는 3가지 형식이 있습니다.

- 인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.
- 블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.
- 이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.

인라인 또는 블록에 포함되는 파일은 간단한 Markdown(.md) 파일입니다. 유효한 Markdown을 포함할 수 있습니다. 포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다. 문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.

포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.

- 여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 파일을 사용합니다.
- 블록에 포함되는 파일은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다. 문장보다 작은 단위에 사용하지 않습니다.
- 포함되는 참조는 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다. 게시 후에만 렌더링됩니다.
- 포함되는 파일의 모든 텍스트가 문서에서 포함되는 파일을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다. 이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.
- 다른 포함되는 파일 내에 포함되는 참조를 포함하지 않습니다. 지원되지 않습니다.
- 미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더). 미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다. 포함되는 파일에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.
- 정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다. 포함되는 파일 및 문서 각각에 고유한 이름을 가진 별도의 파일을 사용합니다. 포함되는 파일과 연결된 미디어 폴더에 미디어 파일을 저장합니다.
- 포함되는 파일을 문서의 유일한 콘텐츠로 사용하지 않습니다.  포함되는 파일은 나머지 문서에서 콘텐츠를 보충해야 합니다.

예제:

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>선택기

동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼 간의 구현 차이를 해결합니다. 이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다. Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.

동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기를 포함되는 파일에 배치하는 것이 좋습니다. 그런 다음, 동일한 선택기를 사용하는 모든 문서에서 포함되는 해당 파일을 참조할 수 있습니다.

다음은 예제 선택기입니다.

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

[Azure 문서](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)에서 실행 중인 선택기의 예를 볼 수 있습니다.

### <a name="code-include-references"></a>코드에 포함되는 참조

Docs 코드 조각 Markdown 확장을 사용하면 문서에 코드 샘플을 포함하고 언어별 구문 색 지정으로 렌더링할 수 있습니다. 현재 리포지토리 또는 다른 리포지토리의 코드를 포함할 수 있습니다. 아래 지침에서는 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)으로 해당 기능을 사용하는 방법에 대한 개요를 제공합니다. Visual Studio Code에서 **Preview**를 열어 코드 조각을 미리 볼 수 있습니다. 강조 표시 및 대화형 작업은 미리 보기에서 사용할 수 없습니다.

> [!NOTE]
> 확장을 사용하여 코드 콘텐츠를 인라인으로 포함할 수 없습니다. 이 작업은 표준 삼중 틱 Markdown 규칙을 통해 수행해야 합니다.

#### <a name="code-from-current-repository"></a>현재 리포지토리의 코드

1. Visual Studio Code에서 **Alt + M** 또는 **Option + M**을 클릭하고 코드 조각을 선택합니다.
2. 코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다. 로컬에서 검색하려면 전체 로컬 검색을 선택합니다.
3. 검색 용어를 입력하여 파일을 찾습니다. 파일을 찾으면 선택합니다.
4. 다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다. 옵션은 **ID**, **범위**, **없음**입니다.
5. 4단계에서 선택한 옵션에 따라 필요한 경우 값을 입력합니다.

전체 코드 파일 표시:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

줄 번호를 지정하여 코드 파일의 일부 표시:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

코드 조각 이름으로 코드 파일의 일부 표시:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>다른 리포지토리의 코드

1. Visual Studio Code에서 **Alt + M** 또는 **Option + M**을 클릭하고 코드 조각을 선택합니다.
2. 코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다. 리포지토리에서 검색하려면 리포지토리 간 참조를 선택합니다.
3. *.openpublishing.publish.config.json*에 있는 리포지토리에서 선택할 수 있습니다. 리포지토리를 선택합니다.
3. 검색 용어를 입력하여 파일을 찾습니다. 파일을 찾으면 선택합니다.
4. 다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다. 옵션은 **ID**, **범위**, **없음**입니다.
5. 5단계에서 선택한 옵션에 따라 필요한 경우 값을 입력합니다.

코드 조각 참조는 다음과 같이 표시됩니다.

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>코드 파일의 경로

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

이 예제는 ASP.NET 문서 리포지토리, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 문서 파일에서 가져온 것입니다. 코드 파일은 동일한 리포지토리에 있는 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs)의 상대 경로로 참조됩니다.

#### <a name="selected-line-numbers"></a>선택한 줄 번호

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

위 예제에서는 *StudentController.cs* 코드 파일의 줄 2~24와 26만 표시됩니다.

다음 섹션에 설명된 대로 하드 코드된 줄 번호보다 코드 조각을 사용하는 것이 좋습니다.

#### <a name="named-snippet"></a>명명된 코드 조각

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

이름에는 문자와 밑줄만 사용합니다.

이 예제는 코드 파일의 `snippet_Create` 섹션을 표시합니다. 이 예제의 코드 파일에는 `snippet_Create`라는 C# 영역이 있습니다.

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

가능한 한, 줄 번호를 지정하지 말고 명명된 섹션을 참조하세요. 코드 파일은 필연적으로 변경되고, 이 경우 줄 번호도 변경되기 때문에 줄 번호 참조는 불안정합니다.
항상 이러한 변경에 대한 알림을 받는 것은 아닙니다. 결국 문서에서 잘못된 줄이 나타나기 시작해도 무엇이 변경되었는지 알 수 없습니다.

#### <a name="highlighting-selected-lines"></a>선택한 줄 강조 표시

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

이 예제에서는 표시된 코드 조각의 처음부터 줄 2와 5를 강조 표시합니다. 강조 표시할 줄 번호가 코드 파일의 처음부터 계산되지 않습니다. 즉, 코드 파일의 줄 3과 6이 강조 표시됩니다.

#### <a name="interactive-code-snippets"></a>대화형 코드 조각

참조를 통해 포함된 코드 조각에 대해 대화형 모드를 사용하도록 설정할 수 있습니다. 예제는 다음과 같습니다.

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

특정 코드 블록을 대상으로 이 기능을 켜려면 `interactive` 특성을 사용합니다. 사용 가능한 특성 값은 다음과 같습니다.

- `cloudshell-powershell` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정
- `cloudshell-bash` - Azure Cloud Shell을 사용하도록 설정
- `try-dotnet` - Try .NET을 사용하도록 설정
- `try-dotnet-class` - 클래스 스캐폴딩으로 Try .NET을 사용하도록 설정
- `try-dotnet-method` - 메서드 스캐폴딩으로 Try .NET을 사용하도록 설정

호환되는 `language`와 `interactive`의 쌍이 있습니다. 예를 들어 `interactive`가 `try-dotnet`인 경우 언어는 `csharp`여야 합니다. 마찬가지로 `cloudshell-powershell`은 `powershell`과만, `cloudshell-bash`는 `bash`와만 언어로 호환됩니다.

Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.

[Try .NET](https://github.com/dotnet/try)을 사용하면 브라우저에서 .NET 코드(C#)를 대화형으로 실행할 수 있습니다. Try .NET에는 대화형 작업에 사용할 수 있는 세 가지 옵션(`try-dotnet`, `try-dotnet-class`, `try-dotnet-method`)이 있습니다. 이와 같은 옵션을 사용하는 데 코드 조각 내의 추가 구성이 필요하지 않습니다. 현재 기본적으로 사용할 수 있는 네임스페이스는 다음과 같습니다.

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

사용자는 `try-dotnet` 특성 값을 사용하여 사용자 지정 코드에서 코드를 래핑할 필요 없이 브라우저에서 C# 코드를 실행할 수 있습니다.

예제:

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

`try-dotnet-class` 값은 대화형 구성 요소에 전달된 코드에 클래스 수준 스캐폴딩을 적용합니다.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

예제:

클래스 스캐폴딩이 적용되지 않은 코드 조각

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

클래스 스캐폴딩이 적용된 코드 조각

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

`try-dotnet-method` 값은 대화형 구성 요소에 전달된 코드에 메서드 수준 스캐폴딩을 적용합니다.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

예제:

메서드 스캐폴딩이 적용되지 않은 코드 조각

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

메서드 스캐폴딩이 적용된 코드 조각

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>코드 조각 구문 참조

지정된 코드 언어를 사용하여 리포지토리에 저장된 코드 조각을 참조할 수 있습니다. 지정된 코드 경로 콘텐츠가 확장되어 파일에 포함됩니다.

코드 조각의 폴더 구조에 대한 제한은 없습니다. 코드 조각을 일반 소스 코드로 관리할 수 있습니다.

구문:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> 이 구문은 블록 Markdown 확장입니다. 자체 줄에 사용해야 합니다.

- `<language>`(*선택 사항*)
  - 코드 조각의 언어입니다. 자세한 내용은 본 문서의 아래에 있는 [지원되는 언어](#supported-languages) 섹션을 참조하세요.

- `<path>`(*필수*)
  - 참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다.

- `<attribute>` 및 `<attribute-value>`(*선택 사항*)
  - 파일에서 코드를 검색하는 방법을 지정하는 데 함께 사용됩니다.
    - `range`: `1,3-5` 줄 범위입니다. 이 예제는 1, 3, 4 및 5 줄을 포함합니다.
    - `id`: `snippet_Create` 코드 파일에서 삽입해야 하는 코드 조각의 ID입니다. 이 값은 범위와 함께 사용할 수 없습니다.
    - `highlight`: `2-4,6` 생성된 코드 조각에서 강조 표시해야 하는 범위 및/또는 줄 수입니다. 번호 매기기는 가져온 범위가 아니라 코드 조각 자체를 기준으로 합니다.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` 문자열 값은 어떤 종류의 대화형 작업이 사용하도록 설정되는지를 결정합니다.

#### <a name="supported-languages"></a>지원되는 언어

|Name|Markdown 레이블|
|-----|-------|
|.NET Core CLI|`dotnetcli`|
|ASP.NET 및 C#|`aspx-csharp`|
|ASP.NET 및 VB|`aspx-vb`|
|Azure CLI|`azurecli`|
|브라우저의 Azure CLI|`azurecli-interactive`|
|브라우저의 Azure PowerShell|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|브라우저의 C#|`csharp-interactive`|
|콘솔|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Kusto 쿼리 언어|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|파워 쿼리 M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>코드 확장

|Name|Markdown 레이블|파일 확장|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xaml|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>과제 및 문제 해결

### <a name="alt-text"></a>대체 텍스트

밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다. 예를 들어 아래 텍스트를 사용하는 대신

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

다음과 같이 밑줄을 이스케이프 처리합니다.

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>아포스트로피 및 큰따옴표

Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다. 이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다. 그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ€™s

이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.

- 왼쪽(열린) 큰따옴표: `&#8220;`
- 오른쪽(닫힌) 큰따옴표: `&#8221;`
- 오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`
- 왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`

### <a name="angle-brackets"></a>대괄호

자리 표시자를 나타내는 데 대괄호를 사용하는 것이 일반적입니다. 텍스트(코드 아님)에서 이 작업을 수행할 때는 대괄호를 인코딩해야 합니다. 그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.

예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.

## <a name="markdown-flavor"></a>Markdown 유형

docs.microsoft.com 사이트 백 엔드는 [Markdig](https://github.com/lunet-io/markdig) 구문 분석 엔진을 통해 구문 분석된 [CommonMark](https://commonmark.org/) 규격 Markdown을 지원합니다. 해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다. 추가 기능은 Markdown 확장을 통해 추가됩니다.

## <a name="see-also"></a>참고 항목:

### <a name="markdown-resources"></a>Markdown 리소스

- [Markdown 소개](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown 참고 자료](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub의 Markdown 기본 사항](https://help.github.com/articles/markdown-basics/)
- [Markdown 가이드](https://www.markdownguide.org/)
