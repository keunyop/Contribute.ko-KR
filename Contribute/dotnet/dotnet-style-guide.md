---
title: .NET 문서용 템플릿 및 치트 시트
description: 이 문서에는 .NET 문서 리포지토리에 대한 새 문서를 작성하는 데 사용할 수 있는 편리한 템플릿이 포함되어 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: a520112cd77f4c4807e7719c2c4dbd43a762f062
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2020
ms.locfileid: "80759567"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>.NET 문서용 메타데이터 및 Markdown 템플릿

이 dotnet/docs 템플릿에는 Markdown 구문의 예와 메타데이터 설정에 대한 지침이 포함되어 있습니다.

Markdown 파일을 만들 때 포함된 템플릿을 새 파일로 복사하여 아래 지정된 대로 메타데이터를 채우고 위의 H1 제목을 문서 제목으로 설정해야 합니다.

## <a name="metadata"></a>메타데이터

필요한 메타데이터 블록은 다음 샘플 메타데이터 블록에 있습니다.

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 콜론(:)과 메타데이터 요소의 값 사이에는 공백이 **있어야 합니다**.
- 값의 콜론(예: 제목)이 메타데이터 구문 분석기를 중단시킵니다. 이 경우 제목을 큰따옴표로 둘러쌉니다(예: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title**: 검색 엔진 결과에 나타납니다. 제목은 H1 제목의 제목과 동일해서는 안 되며 60자 이하여야 합니다.
- **description**: 문서의 내용을 요약합니다. 일반적으로 검색 결과 페이지에 표시되지만 검색 순위 지정에는 사용되지 않습니다. 길이는 공백을 포함하여 115-145자여야 합니다.
- **author**: 작성자 필드에는 작성자의 **GitHub 사용자 이름**이 포함되어야 합니다.
- **ms.date**: 마지막 중요 업데이트 날짜입니다. 전체 문서를 검토하고 업데이트한 경우 기존 문서에서 이를 업데이트합니다. 오타와 같은 작은 수정 사항은 업데이트를 보증하지 않습니다.

각 문서에 다른 메타데이터가 연결되어 있지만 일반적으로 **docfx.json**에 지정된 폴더 수준에서 대부분의 메타데이터 값을 적용합니다.

## <a name="basic-markdown-gfm-and-special-characters"></a>기본 Markdown, GFM 및 특수 문자

[Markdown 참조](../markdown-reference.md) 문서에서 Markdown, GFM(GitHub Flavored Markdown) 및 OPS 관련 확장에 대한 기본 사항을 알아볼 수 있습니다.

Markdown은 서식 지정에 \*, \` 및 \#과 같은 특수 문자를 사용합니다. 콘텐츠에 이러한 문자 중 하나를 포함하려면 다음 두 가지 작업 중 하나를 수행해야 합니다.

- 특수 문자 앞에 백슬래시를 두어 “이스케이프”합니다(예:\*의 경우 `\*`).
- 문자에 대해 [HTML 엔터티 코드](http://www.ascii.cl/htmlcodes.htm)를 사용합니다(예:&#42;의 경우 `&#42;`).

## <a name="file-names"></a>파일 이름

파일 이름에는 다음 규칙이 사용됩니다.

* 소문자, 숫자 및 하이픈만 포함합니다.
* 공백 또는 문장 부호를 사용하면 안 됩니다. 파일 이름에서 단어와 숫자를 구분하려면 하이픈을 사용합니다.
* 개발, 구매, 빌드, 문제 해결과 같은 특정 동작을 나타내는 동사를 사용합니다. -ing 형식의 단어는 사용하지 마세요.
* 짧은 단어는 사용하지 않습니다. a, and, the, in, or 등은 포함하지 마세요.
* Markdown에 있어야 하며 .md 파일 확장명을 사용해야 합니다.
* 파일 이름을 합리적으로 짧게 유지합니다. 이는 문서에 대한 URL의 일부입니다.

## <a name="headings"></a>제목

문장 스타일의 대문자를 사용합니다. 제목의 첫 단어를 항상 대문자로 시작하세요.

## <a name="text-styling"></a>텍스트 스타일 지정

*기울임꼴* 파일, 폴더, 경로(긴 항목의 경우, 해당 행으로 분리), 새 용어에 사용합니다.

**Bold** UI 요소에 사용합니다.

`Code`인라인 코드, 언어 키워드, NuGet 패키지 이름, 명령줄 명령, 데이터베이스 테이블과 열 이름 및 클릭하지 않을 URL에 사용합니다.

## <a name="links"></a>링크

앵커, 내부 링크, 다른 문서에 대한 링크, 코드 포함 및 외부 링크에 대한 정보는 [링크](../how-to-write-links.md)에 대한 일반 문서를 참조하세요.

.NET 문서 팀은 다음 규칙을 사용합니다.

- 대부분의 경우 상대 링크는 GitHub의 소스에서 해결되기 때문에 상대 링크를 사용하고, 링크에서 `~/`의 사용을 권장하지 않습니다. 그러나 종속 리포지토리의 파일에 연결할 때마다 `~/` 문자를 사용하여 경로를 제공합니다. 종속 리포지토리에 있는 파일은 GitHub의 다른 위치에 있기 때문에 링크는 작성된 방법에 관계없이 상대 링크로 올바르게 해결되지 않습니다.
- C# 언어 사양 및 Visual Basic 언어 사양은 언어 리포지토리의 원본을 포함하여 .NET 문서에 포함됩니다. markdown 원본은 [csharplang](https://github.com/dotnet/csharplang) 및 [vblang](https://github.com/dotnet/vblang) 리포지토리에서 관리됩니다.

사양에 대한 링크는 해당 사양이 포함된 원본 디렉터리를 가리켜야 합니다. 다음 예제와 같이 C#의 경우 **~/_csharplang/spec**이고, VB의 경우 **~/_vblang/spec**입니다.

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>API에 대한 링크

빌드 시스템에는 외부 링크를 사용하지 않고도 .NET API에 연결할 수 있는 몇 가지 확장 기능이 있습니다. 다음 구문 중 하나를 사용합니다.

1. 자동 연결: `<xref:UID>` 또는 `<xref:UID?displayProperty=nameWithType>`

   `displayProperty` 쿼리 매개 변수는 정규화된 링크 텍스트를 생성합니다. 기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.

2. Markdown 링크: `[link text](xref:UID)`

   표시되는 링크 텍스트를 사용자 지정하려면 사용합니다.

예제:

- `<xref:System.String>`은 [String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.
- `<xref:System.String?displayProperty=nameWithType>`은 [System.String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.
- `[String class](xref:System.String)`은 [String 클래스](https://docs.microsoft.com/dotnet/api/system.string)로 렌더링됩니다.

이 표기법 사용에 대한 자세한 내용은 [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)(상호 참조 사용)를 참조하세요.

일부 UID에는 특수 문자 \`, \# 또는 \*이 포함되어 있으며, UID 값은 각각 `%60`, `%23` 및 `%2A`로 인코딩된 HTML이어야 합니다. 때때로 괄호 인코딩을 보게 되겠지만 이는 필요하지 않습니다.

예제:

- System.Threading.Tasks.Task\`1은 `System.Threading.Tasks.Task%601`이 됩니다.
- System.Exception.\#ctor은 `System.Exception.%23ctor`이 됩니다.
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode)은 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`가 됩니다.

`https://xref.docs.microsoft.com/autocomplete`에서 형식, 멤버 오버로드 목록 또는 특정 오버로드된 멤버의 UID를 찾을 수 있습니다. 쿼리 문자열 `?text=*\<type-member-name>*`은 UID를 보려는 형식 또는 멤버를 식별합니다. 예를 들어 `https://xref.docs.microsoft.com/autocomplete?text=string.format`은 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 오버로드를 검색합니다. 도구는 UID의 모든 부분에서 제공된 `text` 쿼리 매개 변수를 검색합니다. 예를 들어 멤버 이름(ToString), 부분 멤버 이름(ToStri), 형식 및 멤버 이름(Double.ToString) 등을 검색할 수 있습니다.

UID 뒤에 \*(또는 `%2A`)를 추가하면 링크는 특정 API가 아닌 오버로드 페이지를 나타냅니다. 예를 들어 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_)처럼 특정 오버로드 대신 일반적인 방법으로 [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) 페이지에 연결하려는 경우 사용할 수 있습니다. 또한 멤버가 오버로드되지 않은 경우 \*를 사용하여 구성원 페이지에 연결할 수 있습니다. 이렇게 하면 매개 변수 목록을 UID에 포함하지 않아도 됩니다.

특정 메서드 오버로드에 연결하려면 각 메서드 매개 변수의 정규화된 형식 이름을 포함해야 합니다. 예를 들어 \<xref:System.DateTime.ToString>은 매개 변수가 없는 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 메서드에 연결되는 반면 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)>은 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 메서드에 연결됩니다.

[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)와 같은 제네릭 형식에 연결하려면 \`(`%60`) 문자 다음에 제네릭 형식 매개 변수의 수를 사용합니다. 예를 들어 `<xref:System.Nullable%601>`은 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 형식에 연결되는 반면 `<xref:System.Func%602>`는 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 대리자에 연결됩니다.

## <a name="code"></a>코드

코드를 포함하기 위한 가장 좋은 방법은 작동하는 샘플의 코드 조각을 포함하는 것입니다. [.NET에 참여](dotnet-contribute.md#contributing-to-samples) 문서의 지침에 따라 샘플을 만듭니다. 코드 포함에 대한 기본 규칙은 [코드](../code-in-docs.md)에 대한 일반 지침에 있습니다.

다음 구문을 사용하여 코드를 포함할 수 있습니다.

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>`(*선택 사항*이지만 *권장됨*)
  * 참조되고 있는 코드 조각의 언어입니다.

* `<name>`(*선택 사항*)
  * 코드 조각의 이름입니다. 출력 HTML에는 아무런 영향이 없지만, 이를 사용하여 Markdown 소스의 가독성을 개선할 수 있습니다.

* `<pathToFile>`(*필수*)
  * 참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다. 이는 .NET 문서 집합을 구성하는 다양한 리포지토리에 의해 복잡해질 수 있습니다. .NET 샘플은 dotnet/samples 리포지토리에 있습니다. 모든 코드 조각 경로는 `~/samples`로 시작하고 나머지 경로는 해당 리포지토리의 루트에서 소스에 대한 경로입니다.

* `<queryoption>`(*선택 사항*)
  * 파일에서 코드를 검색하는 방법을 지정하는 데 사용됩니다.
    * `#`: `#{tagname}`(태그 이름) ‘또는’ `#L{startlinenumber}-L{endlinenumber}`(줄 범위). 
    매우 약하기 때문에 줄 번호를 사용하지 않는 것이 좋습니다. 태그 이름은 코드 조각 참조의 기본 방법입니다. 의미 있는 태그 이름을 사용합니다. (이전 플랫폼에서 많은 코드 조각을 마이그레이션했으며 태그에 `Snippet1`, `Snippet2` 등의 이름이 있습니다. 이러한 실행은 유지하기가 훨씬 더 어렵습니다.)
    * `range`: `?range=1,3-5` 줄 범위입니다. 이 예제는 1, 3, 4 및 5 줄을 포함합니다.

가능할 때마다 태그 이름 옵션을 사용하는 것이 좋습니다. 태그 이름은 소스 코드에 있는 `Snippettagname` 형식의 지역 이름 또는 코드 주석 이름입니다. 다음 예제에서는 태그 이름 `BasicThrow`를 참조하는 방법을 보여줍니다.

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

**dotnet/samples** 리포지토리의 소스에 대한 상대 경로는 `~/samples` 경로를 따릅니다.

그리고 코드 조각 태그가 [이 원본 파일](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)에서 어떻게 구성되었는지 확인할 수 있습니다. 코드 조각 소스의 태그 이름 표현에 대한 자세한 내용을 언어별로 보려면 [DocFX 지침](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)을 참조하세요.

다음 예제는 세 개의 .NET 언어에 포함된 코드를 보여줍니다.

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

전체 프로그램에서 코드 조각을 포함하면 모든 코드가 CI(연속 통합) 시스템을 통해 실행될 수 있습니다. 그러나 컴파일 시간 또는 런타임 오류를 일으키는 요소를 표시해야 하는 경우 인라인 코드 블록을 사용할 수 있습니다.

## <a name="images"></a>이미지

### <a name="static-image-or-animated-gif"></a>정적 이미지 또는 애니메이션 GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>연결된 이미지

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>동영상

현재 Channel 9 및 YouTube 비디오를 다음 구문과 함께 포함할 수 있습니다.

### <a name="channel-9"></a>Channel9

```markdown
> [!VIDEO <channel9_video_link>]
```

비디오의 올바른 URL을 가져오려면 비디오 프레임 아래의 **포함** 탭을 선택하고 `<iframe>` 요소에서 URL을 복사합니다. 예:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

비디오의 올바른 URL을 가져오려면 비디오를 마우스 오른쪽 단추로 클릭하여 **포함 코드 복사**를 선택하고 `<iframe>` 요소에서 URL을 복사합니다.

```markdown
> [!VIDEO <youtube_video_link>]
```

예:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>docs.microsoft 확장명

docs.microsoft는 GitHub Flavored Markdown에 몇 가지 추가 확장 기능을 제공합니다.

### <a name="checked-lists"></a>확인된 목록

목록에 사용자 지정 스타일을 사용할 수 있습니다. 녹색 확인 표시가 있는 목록을 렌더링할 수 있습니다.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

이는 다음과 같이 렌더링됩니다.

> [!div class="checklist"]
> * .NET Core 앱을 만드는 방법
> * Microsoft.XmlSerializer.Generator 패키지에 참조를 추가하는 방법
> * MyApp.csproj를 편집하여 종속성을 추가하는 방법
> * 클래스 및 XmlSerializer를 추가하는 방법
> * 애플리케이션을 빌드 및 실행하는 방법

[.NET Core 문서](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)에서 실행 중인 확인 목록의 예를 볼 수 있습니다.

### <a name="buttons"></a>Buttons

Button 링크:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

이는 다음과 같이 렌더링됩니다.

> [!div class="button"]
> [단추 링크](dotnet-contribute.md)

[Visual Studio 문서](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)에서 실행 중인 단추의 예를 볼 수 있습니다.

### <a name="step-by-steps"></a>단계별

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

[C# 가이드](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)에서 실행 중인 단계별 예를 볼 수 있습니다.
