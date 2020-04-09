---
title: 설명서에서 링크를 사용하는 방법
description: 이 문서에서는 docs.microsoft.com 내의 콘텐츠에 대한 링크를 만드는 방법에 대한 지침을 제공합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624786"
---
# <a name="use-links-in-documentation"></a>설명서에서 링크 사용

이 문서에서는 docs.microsoft.com에서 호스팅되는 페이지의 하이퍼 링크를 사용하는 방법에 대해 설명합니다. 링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다. 사용자는 링크를 통해 같은 페이지, 인접한 다른 페이지 또는 외부 사이트 및 URL의 콘텐츠로 이동할 수 있습니다.

docs.microsoft.com 사이트 백 엔드는 [Markdig][] 구문 분석 엔진을 통해 구문 분석되는 [CommonMark][] 규격 markdown을 지원하는 OPS(Open Publishing Services)를 사용합니다. 해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)][GFM]과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다. 추가 기능은 Markdown 확장을 통해 추가됩니다.

> [!IMPORTANT]
> 대상이 링크를 지원하는 경우(대부분 지원) 모든 링크는 보안 링크여야 합니다(`https` 및 `http`).

## <a name="link-text"></a>링크 텍스트

링크 텍스트에 포함하는 단어는 친근해야 합니다. 즉, 일반적인 영어(한국어) 단어 또는 연결하는 페이지의 제목이어야 합니다.

> [!IMPORTANT]
> "여기를 클릭하세요."를 사용하지 않습니다. 검색 엔진 최적화에 좋지 않으며 대상을 적절하게 설명하지 못합니다.

**올바름:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**잘못됨:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>하나의 문서에서 다른 문서로 링크

게시 시스템에서 지원되는 두 가지 유형의 하이퍼링크는 **URL**과 **파일 링크**입니다.

URL 링크는 docs.microsoft.com의 루트를 기준으로 한 URL 경로이거나, 전체 URL 구문을 포함하는 절대 URL(예: `https://github.com/MicrosoftDocs/PowerShell-Docs`)일 수 있습니다.

- 현재 _docset_ 외부의 콘텐츠에 연결하거나 docset 내의 자동 생성된 참조 및 개념 문서 간에 연결하는 경우 URL 링크를 사용합니다.
- 상대 링크를 만드는 가장 간단한 방법은 브라우저에서 URL을 복사한 후 markdown에 붙여넣은 값에서 `https://docs.microsoft.com/en-us`를 제거하는 것입니다.
   - Microsoft 속성에 대한 로캘은 URL에 포함하지 않습니다(예: URL에서 “/en-us” 제거).

파일 링크는 docset 내 한 문서에서 다른 문서로 연결하는 데 사용됩니다.

- 모든 파일 경로에는 백슬래시 문자 대신 슬래시(`/`) 문자를 사용합니다.
- 문서는 같은 디렉터리의 다른 문서에 연결됩니다.

  `[link text](article-name.md)`

- 문서는 현재 디렉터리의 부모 디렉터리에 있는 문서에 연결됩니다.

  `[link text](../article-name.md)`

- 문서는 현재 디렉터리의 하위 디렉터리에 있는 문서에 연결됩니다.

  `[link text](directory/article-name.md)`

- 문서는 현재 디렉터리의 부모 디렉터리에 있는 하위 디렉터리의 문서에 연결됩니다.

  `[link text](../directory/article-name.md)`

> [!NOTE]
> 앞의 예제에서는 `~/`를 링크의 일부로 사용하지 않습니다. 리포지토리의 루트에서 시작하는 절대 경로에 연결하려면 `/`로 링크를 시작합니다. GitHub에서 원본 리포지토리로 이동할 때 `~/`를 포함하면 유효하지 않은 링크가 생성됩니다. `/`로 경로를 시작하면 올바르게 해결됩니다.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>docs.microsoft.com의 링크 구조

docs.microsoft.com에 게시된 콘텐츠의 URL 구조는 다음과 같습니다.

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

예제:

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` - 문서의 언어를 식별함(예: en-us 또는 de-de)
- `<product-service>` - 제품 또는 서비스의 이름(예: powershell, dotnet 또는 azure)
- `[<feature-service>]` - (선택 사항) 제품 기능 또는 하위 서비스의 이름(예: csharp 또는 load-balancer)
- `[<subfolder>]` - (선택 사항) 기능 내 하위 폴더의 이름
- `<topic>` - 토픽에 대한 문서 파일의 이름(예: load-balancer-overview 또는 overview)
- `[?view=\<view-name>]` - (선택 사항) 사용할 수 있는 버전이 여러 개인 콘텐츠의 버전 선택기에서 사용되는 보기 이름(예: azps-3.5.0)

> [!TIP]
> 대부분 경우, 같은 _docset_의 문서는 `<product-service>` URL 조각이 같습니다. 예:
> - 같은 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - 다른 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>책갈피 링크

‘현재’ 파일의 제목에 대한 책갈피 링크를 사용하려면 해시 기호 다음에 제목의 소문자 단어를 사용합니다.  제목에서 문장 부호를 제거하고 공백을 대시로 바꿉니다.

```markdown
[Managed Disks](#managed-disks)
```

다른 문서의 책갈피 제목에 연결하려면 파일 관련 또는 사이트 관련 링크 다음에 해시 기호를 사용하고 그 뒤에 제목의 단어를 사용합니다. 제목에서 문장 부호를 제거하고 공백을 대시로 바꿉니다.

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

URL에서 책갈피 링크를 복사할 수도 있습니다. URL을 찾으려면 docs.microsoft.com의 제목 줄을 마우스로 가리킵니다. 링크 아이콘이 표시됩니다.

![문서 제목의 링크 아이콘](media/how-to-write-links/bookmark-link.png)

링크 아이콘을 클릭한 후 URL에서 책갈피 앵커 텍스트(즉, 해시 뒤에 있는 부분)를 복사합니다.

> [!NOTE]
> 또한 Docs 확장에 링크를 만드는 데 유용한 도구가 있습니다.

### <a name="explicit-anchor-links"></a>명시적 앵커 링크

허브 및 시작 페이지를 제외하고는 `<a>` HTML 태그를 사용한 명시적 앵커 링크 추가는 필요하거나 권장되지 않습니다. 대신 [책갈피 링크](#bookmark-links)에 설명된 대로 자동 생성된 책갈피를 사용합니다. 허브 및 시작 페이지의 경우 다음과 같이 앵커를 선언합니다.

```markdown
## <a id="anchortext" />Header text
```

또는

```markdown
## <a name="anchortext" />Header text
```

다음을 앵커 링크에 추가합니다.

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> 앵커 텍스트는 항상 소문자이고 공백을 포함하지 않아야 합니다.

## <a name="xref-cross-reference-links"></a>XRef(상호 참조) 링크

XRef 링크는 빌드할 때 유효성 검사가 수행되므로 API에 연결하는 데 권장되는 방법입니다. 현재 docset 또는 다른 docset의 자동 생성된 API 참조 페이지에 연결하려면 형식 또는 멤버의 [UID](#determine-the-uid)(고유 ID)가 포함된 XRef 링크를 사용합니다.

> [!TIP]
> [VS Code용 Docs Markdown 확장][docsextension](Docs Authoring Pack의 일부)을 사용하여 [.NET API 브라우저][]에 표시되는 .NET XRref 링크를 삽입할 수 있습니다.

[.NET API 브라우저][] 또는 [Windows UWP][] 검색 상자에 전체 이름의 전부 또는 일부를 입력하여 연결하려는 API가 [docs.microsoft.com][docs]에 있는지 확인합니다. 표시되는 결과가 없으면 해당 형식이 아직 docs.microsoft.com에 없는 것입니다.

다음 구문 중 하나를 사용할 수 있습니다.

- 자동 링크:

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다. 선택적 `displayProperty=nameWithType` 쿼리 매개 변수는 정규화된 링크 텍스트 즉, 형식의 경우 **namespace.type**을, 형식 멤버(열거형 형식 멤버 포함)의 경우 **type.member**를 생성합니다.

- Markdown 스타일 링크:

   ```markdown
   [link text](xref:UID)
   ```

   표시되는 링크 텍스트를 사용자 지정하려면 XRef에 Markdown 스타일 링크를 사용합니다.

예제:

- **\<xref:System.String>** 은 <xref:System.String>으로 표시됨

- **\<xref:System.String?displayProperty=nameWithType>** 은 <xref:System.String?displayProperty=nameWithType>으로 표시됨

- **\[String class](xref:System.String)** 은 [String 클래스](xref:System.String)로 표시됨

`displayProperty=fullName` 쿼리 매개 변수는 클래스에 대해 `displayProperty=nameWithType`과 같은 방식으로 작동합니다. 즉, 링크 텍스트가 **namespace.classname**이 됩니다. 그러나 멤버의 경우 링크 텍스트는 바람직하지 않을 수도 있는 **namespace.classname.membername**으로 표시됩니다.

> [!NOTE]
> UID는 대/소문자를 구분합니다. 예를 들어 `<xref:System.Object>`는 올바르게 확인되지만, `<xref:system.object>`는 그렇지 않습니다.

### <a name="xref-build-warnings-and-incremental-builds"></a>XRef 빌드 경고 및 증분 빌드

증분 빌드는 변경되었거나 변경의 영향을 받은 파일만 빌드합니다. 잘못된 XREF 링크에 대한 빌드 경고가 표시되지만, 이 링크가 실제로 유효한 경우 빌드가 증분이었기 때문일 수 있습니다. 경고를 발생시키는 파일이 변경되지 않았으므로 빌드되지 않았으며 지난 경고가 재생되었습니다. 파일이 변경되거나 전체 빌드를 트리거하면 경고가 사라집니다(ops.microsoft.com에서 전체 빌드를 시작할 수 있음). 이는 DocFX가 XREF 서비스 내에서 데이터 업데이트를 검색할 수 없어서 발생하는 증분 빌드의 단점입니다.

### <a name="determine-the-uid"></a>UID 확인

UID는 일반적으로 정규화된 클래스 또는 멤버 이름입니다. UID를 확인하는 방법은 다음과 같은 두 가지 이상이 있습니다.

- 형식 또는 멤버의 [Docs][docs] 페이지를 마우스 오른쪽 단추로 클릭하고 **소스 보기**를 선택한 다음 **ms.assetid**의 **content** 값을 복사합니다.

  ![웹 페이지 소스의 ms.assetid](media/how-to-write-links/ms-assetid.png)

- 형식 이름의 일부 또는 전부를 URL에 추가하여 [자동 완성 사이트][]를 사용합니다. 예를 들어 브라우저의 주소 표시줄에 `https://xref.docs.microsoft.com/autocomplete?text=Writeline`을 입력하면 해당 이름에 **Writeline**이 포함된 모든 형식과 메서드가 해당 UID와 함께 표시됩니다.

#### <a name="verify-the-uid"></a>UID 검증

UID가 올바른지 테스트하려면 다음 URL의 **System.String**을 해당 UID로 바꾼 후 브라우저의 주소 표시줄에 붙여넣습니다.

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> URL의 UID는 대/소문자를 구분하고, 메서드 오버로드 UID를 확인하는 경우 매개 변수 형식 사이에 공백을 포함하지 마세요.

다음과 같은 내용이 표시되면 UID가 올바른 것입니다.

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

페이지에 `[]`가 표시되면 UID가 잘못된 것입니다.

### <a name="percent-encoding-of-urls"></a>URL의 백분율 인코딩

UID의 특수 문자는 다음과 같이 HTML로 인코딩해야 합니다.

| 문자 | HTML 인코딩 |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

[백분율 코드](https://en.wikipedia.org/wiki/Percent-encoding)의 전체 목록을 참조하세요.

인코딩 예:

- `System.Threading.Tasks.Task``1`은 `System.Threading.Tasks.Task%601`로 인코딩됨([제네릭 형식에 대한 섹션](#generic-types) 참조)

- `System.Exception.#ctor`은 `System.Exception.%23ctor`로 인코딩됨

- `System.Object.Equals*`는 `System.Object.Equals%2A`로 인코딩됨

### <a name="generic-types"></a>제네릭 형식

제네릭 형식은 `System.Collections.Generic.List<T>`와 같은 형식입니다. [.NET API 브라우저](https://docs.microsoft.com/dotnet/api/)에서 이 형식을 검색하여 해당 URL을 살펴보면, `<T>`가 URL에서 `-1`(실제로 **`1**을 나타냄)로 작성된 것을 볼 수 있습니다.

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

**List\<T>** 같은 제네릭 형식에 연결하려면 다음 예에 표시된 것처럼 **\`** 억음 악센트 기호 문자를 **%60**으로 인코딩합니다.

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>메서드

메서드에 연결하려면 메서드 이름 뒤에 별표(`*`)를 추가하여 일반 메서드 페이지에 연결하거나 특정 오버로드에 할 수 있습니다. 예를 들어 특정 매개 변수 형식 없이 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 메서드에 연결하려면 일반 페이지를 사용합니다. 별표 문자는 `%2A`로 인코딩됩니다. 예:

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>`은 <xref:System.Object.Equals%2A?displayProperty=nameWithType>에 연결됨

특정 오버로드에 연결하려면 메서드 이름 뒤에 괄호를 추가하고 각 매개 변수의 전체 형식 이름을 포함합니다. 형식 이름 사이에 공백 문자를 넣지 마세요. 넣으면 링크가 작동하지 않습니다. 예:

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>`은 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>에 연결됨

## <a name="links-from-includes"></a>포함되는 내용의 링크

포함되는 파일은 다른 디렉토리에 위치하기 때문에 더 긴 상대 경로를 사용해야 합니다. 포함되는 파일의 문서에 연결하려면 이 형식을 사용합니다.

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> Visual Studio Code용 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 확장을 사용하면, 경로를 확인하는 번거로움 없이 상대 링크와 책갈피를 올바르게 삽입할 수 있습니다.

## <a name="links-in-selectors"></a>선택기의 링크

선택기는 설명서 문서에 드롭다운 목록으로 표시되는 탐색 구성 요소입니다. reader가 드롭다운에서 값을 선택하면 브라우저가 선택한 문서를 엽니다. 일반적으로 선택기 목록에는 밀접하게 관련된 문서에 대한 링크가 포함되어 있습니다(예: 여러 프로그래밍 언어의 동일한 주제 또는 밀접하게 관련된 문서 시리즈).

포함되는 내용에 포함된 선택기가 있는 경우 다음과 같은 링크 구조체를 사용합니다.

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>참조 스타일 링크

소스 콘텐츠를 쉽게 읽을 수 있도록 참조 스타일 링크를 사용할 수 있습니다. 참조 스타일 링크는 인라인 링크 구문을, 긴 URL을 문서 끝으로 이동시킨 간소화된 구문으로 바꿉니다. [Daring Fireball](https://daringfireball.net/projects/markdown/)의 예제는 다음과 같습니다.

인라인 텍스트:

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

문서 끝의 링크 참조:

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

링크 앞에 쉼표 뒤에 공백이 있어야 합니다. 다른 기술 문서에 연결할 때 공백을 포함하지 못한 경우 게시된 문서에서 링크가 작동하지 않습니다.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>기술 문서 집합의 일부가 아닌 페이지에 대한 링크

다른 Microsoft 속성의 페이지(가격 책정 페이지, SLA 페이지 또는 설명서 문서가 아닌 다른 페이지)에 연결하려면 절대 URL을 사용하지만 로캘을 생략합니다. 여기서 목적은 링크가 GitHub 및 렌더링된 사이트에서 작동하는 것입니다.

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>타사 사이트에 대한 링크

멋진 사용자 환경은 사용자를 다른 사이트에 보내는 작업을 최소화합니다. 따라서 간혹 필요한 타사 사이트에 대한 링크는 다음 정보를 기반으로 합니다.

- **책임감**: 공유하려는 정보가 타사 정보인 경우 타사 콘텐츠에 연결합니다. 예를 들어 사용자에게 Android 개발자 도구를 사용하는 방법을 알려주는 것은 Microsoft이 해야 할 일이 아닙니다. 해당 작업은 Google에서 담당하게 됩니다. 필요한 경우 Azure*에서* Android 개발자 도구를 사용하는 방법을 설명할 수 있지만 Google에서도 해당 도구를 사용하는 방법을 설명해야 합니다.
- **PM 승인**: 타사 콘텐츠에 대해 Microsoft에서 승인하도록 요청합니다. 링크를 설정한다는 것은 Microsoft가 해당 사이트를 신뢰한다는 것을 의미하며 사람들이 지침을 따를 경우 Microsoft에도 의무가 있다는 것을 나타냅니다.
- **유효 시간 검토**: 타사 정보가 여전히 최신 정보이고 정확하며 관련성이 있는지 확인하고 링크가 변경되지 않았는지 확인합니다.
- **오프사이트**: 사용자가 다른 사이트로 이동한다는 점을 인식하도록 합니다. 이에 대한 명확한 내용이 없을 경우 설명하는 문구를 추가합니다. 예: “필수 구성 요소에는 Android Studio 사이트에서 다운로드할 수 있는 Android 개발자 도구가 포함됩니다.”
- **다음 단계**: “다음 단계” 섹션에 MVP 블로그 같은 링크를 추가해도 됩니다. 다시 한번 말하지만, 사용자가 사이트를 벗어난다는 점을 이해하도록 합니다.
- **법적 정보**: 모든 microsoft.com 페이지의 **사용 약관** 바닥글에 **타사 사이트에 대한 링크**의 법적 정보가 설명되어 있습니다.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 브라우저]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[자동 완성 사이트]: https://xref.docs.microsoft.com/autocomplete?text=
