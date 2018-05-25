---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/23/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Markdown을 사용하여 Docs를 작성하는 방법

Docs.microsoft.com 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다. 그렇기 때문에 신속하게 산업 표준이 되고 있습니다.

Docs 콘텐츠가 GitHub에 저장되기 때문에 일반적인 형식 요구 사항에 추가 기능을 제공하는 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)이라는 Markdown의 상위 집합을 사용할 수 있습니다. 또한 OPS(Open Publishing Services)는 Markdig Markdown Parser를 구현합니다. Markdig은 GFM(GitHub Flavored Markdown)과 호환성이 뛰어나 Docs 전용 기능을 사용할 수 있는 기능을 추가합니다.

* Markdig은 빠르고 강력하며 CommonMark와 호환되며 .NET에 대해 확장 가능한 Markdown 프로세서입니다.
* https://github.com/lunet-io/markdig
* 커뮤니티 지원 향상
* 표준 지원 향상

## <a name="markdown-basics"></a>Markdown 기본 사항

### <a name="headings"></a>제목

제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>굵게 기울임꼴 텍스트

텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.

```markdown
    This text is **bold**.
```

텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.

```markdown
    This text is *italic*.
```

텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>목록

#### <a name="unordered-list"></a>정렬되지 않은 목록

정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다. 예를 들어 아래 Markdown은

```markdown
- List item 1
- List item 2
- List item 3
```

다음과 같이 렌더링됩니다.

- 목록 항목 1
- 목록 항목 2
- 목록 항목 3

다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다. 예를 들어 아래 Markdown은

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

다음과 같이 렌더링됩니다.

- 목록 항목 1
  - 목록 항목 A
  - 목록 항목 B
- 목록 항목 2

#### <a name="ordered-list"></a>정렬된 목록

정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다. 예를 들어 아래 Markdown은

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

다음과 같이 렌더링됩니다.

1. 첫 번째 지침
2. 두 번째 지침
3. 세 번째 지침

다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다. 예를 들어 아래 Markdown은

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

다음과 같이 렌더링됩니다.

1. 첫 번째 지침
    1. 하위 지침
    2. 하위 지침
2. 두 번째 지침

### <a name="tables"></a>보세요.

테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다. 파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다. 하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다. 테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.

예를 들어 아래 Markdown은

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

다음과 같이 렌더링됩니다.

| 테이블을                  | 사용해                 | 보세요.          |
| :------------------- | -------------------: |:---------------:|
| 왼쪽 정렬된 열  | 오른쪽 정렬된 열 | 가운데 정렬된 열 |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.

- 넓은 테이블의 서식을 지정하는 데 도움이 되는 Markdig [테이블 래핑 기능](#table-wrapping)
- GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)
- [Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱
- [Adam Pritchard의 Markdown 참고 자료](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Michel Fortin의 Markdown 추가 자료](https://michelf.ca/projects/php-markdown/extra/#table)
- [HTML 테이블을 Markdown으로 전환](https://jmalarcon.github.io/markdowntables/)

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

처음 세 개의 ` 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다. Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.

이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.

|이름|Markdown 레이블|
|-----|-------|
|.NET 콘솔|dotnetcli|
|ASP.NET(C#)|aspx-csharp|
|ASP.NET(VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps 수식|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>예: C\#

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

#### <a name="example-sql"></a>예: SQL

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

## <a name="ops-custom-markdown-extensions"></a>OPS 사용자 지정 Markdown 확장

> [!NOTE]
> OPS(Open Publishing Services)는 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다. Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다. 이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다. (예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)

Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다. 더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.

- 참고 블록
- 포함되는 내용
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

### <a name="includes"></a>포함되는 내용

문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는 내용" 파일에 대한 참조를 사용할 수 있습니다. 이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다. 콘텐츠를 재사용하기 위해 사용 가능한 포함되는 내용에는 3가지 유형이 있습니다.

- 인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.
- 블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.
- 이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.

인라인 또는 블록 포함되는 내용은 간단한 Markdown(.md) 파일입니다. 유효한 Markdown을 포함할 수 있습니다. 포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다. 문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.

포함되는 내용의 요구 사항 및 고려 사항은 다음과 같습니다.

- 여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 내용을 사용합니다.
- 블록 포함되는 내용은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다. 문장보다 작은 단위에 사용하지 않습니다.
- 포함되는 내용은 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다. 게시 후에만 렌더링됩니다.
- 포함되는 내용의 모든 텍스트가 문서에서 포함되는 내용을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다. 이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.
- 다른 포함되는 내용 내에 포함되는 내용을 포함하지 않습니다. 지원되지 않습니다.
- 미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더). 미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다. 포함되는 내용에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.
- 정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다. 각 포함되는 내용 및 문서에 고유한 이름을 가진 별도의 파일을 사용합니다. 포함되는 내용과 연결된 미디어 폴더에 미디어 파일을 저장합니다.
- 포함되는 내용을 문서의 유일한 콘텐츠로 사용하지 않습니다.  포함되는 내용은 나머지 문서에서 콘텐츠를 보충해야 합니다.

### <a name="selectors"></a>선택기

동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼에서 구현 중에 차이점을 해결합니다. 이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다. Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.

동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기가 포함되는 내용에 배치하는 것이 좋습니다. 그런 다음 동일한 선택기를 사용하는 모든 문서에서 해당 포함되는 내용을 참조할 수 있습니다.

### <a name="code-snippets"></a>코드 조각

Markdig은 해당 코드 조각 확장을 통해 문서에 대한 고급 코드 포함 기능을 지원합니다. 이 기능은 프로그래밍 언어 선택과 구문 색 지정 및 다음과 같은 멋진 기능을 기반으로 하는 GFM 기능에서 빌드하는 고급 렌더링을 제공합니다.

- 외부 리포지토리에서 중앙 집중식 코드 샘플/코드 조각 포함
- 다른 언어로 여러 버전의 코드 샘플을 표시하는 탭 UI

## <a name="gotchas-and-troubleshooting"></a>과제 및 문제 해결

### <a name="alt-text"></a>대체 텍스트

밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다. 예를 들어 아래 텍스트를 사용하는 대신

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

다음과 같이 밑줄을 이스케이프 처리합니다.

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>아포스트로피 및 큰따옴표

Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다. 이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다. 그렇지 않을 경우 파일이 게시되면 Itâ€™s와 같이 표시됩니다.

이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.

- 왼쪽(열린) 큰따옴표: `&#8220;`
- 오른쪽(닫힌) 큰따옴표: `&#8221;`
- 오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`
- 왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`

### <a name="angle-brackets"></a>대괄호

예를 들어 자리 표시자를 나타내는 것과 같이 파일에 있는 텍스트(코드 아님)에서 대괄호를 사용하는 경우 대괄호를 수동으로 인코딩해야 합니다. 그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.

예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.

## <a name="see-also"></a>참고 항목

### <a name="markdown-resources"></a>Markdown 리소스

- [Markdown 소개](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown 참고 자료](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub의 Markdown 기본 사항](https://help.github.com/articles/markdown-basics/)
