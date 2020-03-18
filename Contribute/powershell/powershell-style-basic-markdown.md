---
title: PowerShell 문서용 템플릿 및 치트 시트
description: 이 문서에는 PowerShell 문서에 대한 새 문서를 만드는 데 사용할 수 있는 편리한 템플릿이 포함되어 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331932"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>PowerShell-Docs에 대한 Markdown 스타일 가이드

이 문서에서는 PowerShell-Docs 콘텐츠에 관련된 몇 가지 스타일 지침을 제공합니다.

기타 쓰기 스타일 지침은 [Microsoft 스타일 가이드](https://docs.microsoft.com/style-guide/welcome/)를 참조하세요.

## <a name="metadata"></a>메타데이터

이 템플릿에는 Markdown 구문의 예와 메타데이터 설정에 대한 지침이 포함되어 있습니다.
Markdown 파일을 만들 때 포함된 템플릿을 새 파일로 복사하여 아래 지정된 대로 메타데이터를 채우고 위의 H1 제목을 문서 제목으로 설정해야 합니다.

필요한 메타데이터 블록은 다음 샘플 메타데이터 블록에 있습니다.

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 콜론(:)과 메타데이터 요소의 값 사이에는 공백이 **있어야 합니다**.
- 값의 콜론(예: 제목)이 메타데이터 구문 분석기를 중단시킵니다. 이 경우 제목을 큰따옴표로 둘러쌉니다(예: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author**: 작성자 필드에는 작성자의 **GitHub 사용자 이름**이 포함되어야 합니다.
- **description**: 문서의 내용을 요약합니다. 일반적으로 검색 결과 페이지에 표시되지만 검색 순위 지정에는 사용되지 않습니다. 길이는 공백을 포함하여 115-145자여야 합니다.
- **ms.date**: 마지막 중요 업데이트 날짜입니다. 전체 문서를 검토하고 업데이트한 경우 기존 문서에서 이를 업데이트합니다. 오타와 같은 작은 수정 사항은 업데이트를 보증하지 않습니다.
- **title**: 검색 엔진 결과에 나타납니다. 제목은 H1 제목의 제목과 동일해서는 안 되며 60자 이하여야 합니다.

각 문서에 다른 메타데이터가 연결되어 있지만 일반적으로 **docfx.json**에 지정된 폴더 수준에서 대부분의 메타데이터 값을 적용합니다.

## <a name="product-terminology"></a>제품 용어

PowerShell의 여러 가지 변형이 있습니다. 이 표에서는 PowerShell 설명에 사용되는 몇 가지 용어를 정의합니다.

- **PowerShell** - 기본값입니다. PowerShell은 Microsoft에서 제공하는 제품입니다. PowerShell이라는 용어는 제품의 모든 버전을 설명하는 데 사용할 수 있습니다.
- **PowerShell Core** - 지원되는 플랫폼용으로 .NET Core 공용 언어 런타임(CoreCLR)에 빌드된 PowerShell입니다.
- **Windows PowerShell** - .NET Framework CLR(공용 언어 런타임)에 빌드된 PowerShell입니다. Windows PowerShell은 Windows에서만 제공되며 전체 .NET Framework CLR이 필요합니다.

일반적으로 문서의 “Windows PowerShell”에 대한 참조는 “PowerShell”로 변경할 수 있습니다.
Windows 특정 기술을 설명하는 동안 “Windows PowerShell”을 변경해서는 **안 됩니다**.

## <a name="basic-markdown-gfm-and-special-characters"></a>기본 Markdown, GFM 및 특수 문자

[Markdown 참조](../markdown-reference.md) 문서에서 Markdown, GFM(GitHub Flavored Markdown) 및 OPS 관련 확장에 대한 기본 사항을 알아볼 수 있습니다.

Markdown은 서식 지정에 \*, \` 및 \#과 같은 특수 문자를 사용합니다. 콘텐츠에 이러한 문자 중 하나를 포함하려면 다음 두 가지 작업 중 하나를 수행해야 합니다.

- 특수 문자 앞에 백슬래시를 두어 “이스케이프”합니다(예:\*의 경우 `\*`).
- 문자에 대해 [HTML 엔터티 코드](http://www.ascii.cl/htmlcodes.htm)를 사용합니다(예:&#42;의 경우 `&#42;`).
- Markdown 파일은 일반 ASCII 텍스트 또는 UTF-8 인코딩을 사용해야 합니다. 그러나 다중 바이트 UTF-8 문자를 사용하지 마세요. 대신, HTML 엔터티를 사용합니다. 예를 들어 저작권 기호에는 `&copy;`를 사용합니다.
  “&copy;”로 렌더링됩니다.

## <a name="hyperlinks"></a>하이퍼링크

- Bare URL을 사용하지 마세요. 링크는 Markdown 구문 `[friendlyname](url-or-path)`를 사용해야 함
- 링크에는 일반적으로 연결된 항목의 제목인 식별 이름이 있어야 함
- 아래쪽 “관련 링크” 섹션에 있는 모든 항목은 하이퍼링크로 연결되어야 합니다.
- **docs.microsoft.com**에서 호스트되는 다른 콘텐츠에 연결할 때 상대 링크를 사용합니다.
- 하이퍼링크의 대괄호 안에 억음 악센트, 굵게 또는 기타 태그를 사용하지 마세요.

연결에 대한 자세한 내용은 [문서에서 링크 사용](../how-to-write-links.md)을 참조하세요.

## <a name="filenames"></a>파일 이름

파일 이름에는 다음 규칙이 사용됩니다.

- 문자, 숫자 및 하이픈만 포함합니다.
- 공백 또는 문장 부호를 사용하면 안 됩니다. 파일 이름에서 단어와 숫자를 구분하려면 하이픈을 사용합니다.
- 개발, 구매, 빌드, 문제 해결과 같은 특정 동작을 나타내는 동사를 사용합니다. -ing 형식의 단어는 사용하지 마세요.
- 짧은 단어는 사용하지 않습니다. a, and, the, in, or 등은 포함하지 마세요.
- Markdown에 있어야 하며 .md 파일 확장명을 사용해야 합니다.
- 파일 이름을 합리적으로 짧게 유지합니다. 이는 문서에 대한 URL의 일부입니다.

## <a name="blank-lines-spaces-and-tabs"></a>빈 줄, 공백 및 탭

중복된 빈 줄을 제거합니다. 여러 빈 줄은 HTML에서 하나의 빈 줄로 렌더링되므로 여러 빈 줄을 사용할 필요가 없습니다.

또한 빈 줄은 Markdown에서 블록의 끝을 알립니다. 다양한 형식의 Markdown 블록 사이(예: 단락과 목록 또는 헤더 사이)에 하나의 공백이 있어야 합니다.

> [!NOTE]
> Markdown에서는 간격이 중요합니다. 항상 하드 탭 대신 공백을 사용합니다. 줄 끝에서 추가 공백을 제거합니다.

## <a name="titles-and-headings"></a>제목

[ATX 제목][atx](# 스타일, `=` 또는 `-` 스타일 헤더가 아님)만 사용합니다.

- 문장 대/소문자 사용 - 적절한 명사 및 제목이나 헤더의 첫 번째 문자만 대문자로 시작되어야 함
- `#`과 제목의 첫 번째 문자 사이에는 단일 공백이 있어야 함
- 제목은 하나의 빈 줄로 둘러싸야 함
- 문서당 하나의 H1만
- 헤더 수준은 1씩 증가해야 함 - 수준을 건너뛰지 않음
- 억음 악센트, 굵게 또는 기타 태그를 사용하지 않음

> [!CAUTION]
> cmdlet 참조를 위해 [PlatyPS][platyPS]가 적용한 스키마에는 특정 H2 및 H3 헤더가 필요합니다. 헤더를 추가하거나 제거하면 빌드가 중단될 수 있습니다. 자세한 내용은 [cmdlet 참조 스타일 가이드](powershell-style-reference.md)를 참조하세요.

## <a name="limit-line-length-to-100-characters"></a>줄 길이를 100자로 제한

이 항목은 차이 및 기록의 명령줄 출력을 간소화합니다.

이 규칙은 PowerShell-Docs의 많은 기존 콘텐츠에 적용되지 않지만 시간이 지나면서 관련 작업이 진행되고 있습니다. 자유롭게 지원할 수 있습니다. VSCode(Visual Studio Code)의 [재배치 확장][reflow]을 통해 이 제한에 따라 손쉽게 단락 서식을 다시 지정할 수 있습니다.

## <a name="lists"></a>목록

목록에 여러 문장이나 단락이 포함된 경우 목록이 아닌 하위 수준 헤더를 사용하는 것이 좋습니다.

목록은 하나의 빈 줄로 둘러싸야 합니다.

### <a name="unordered-lists"></a>정렬되지 않은 목록

여러 문장이 포함되지 않은 경우에는 마침표로 목록 항목을 종료하지 마세요. 목록 항목 글머리 기호에 하이픈 문자(`-`)를 사용합니다. 이렇게 하면 별표[`*`]를 사용하는 굵게 또는 기울임꼴 태그와 혼동되지 않습니다. 글머리 기호 항목 아래에 단락이나 다른 요소를 포함하려면 줄 바꿈을 삽입하고 글머리 기호 뒤 첫 번째 문자에 들여쓰기를 맞춥니다.

예:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

이것은 글머리 기호 항목 아래에 하위 요소를 포함하는 목록입니다.

- 첫 번째 글머리 기호 항목

  첫 번째 글머리 기호를 설명하는 문장입니다.

  - 하위 머리 기호 항목

    하위 글머리 기호를 설명하는 문장입니다.

- 두 번째 글머리 기호 항목
- 세 번째 글머리 기호 항목

### <a name="ordered-lists"></a>정렬된 목록

번호가 매겨진 항목 아래에 단락이나 다른 요소를 포함하려면 항목 번호 뒤 첫 번째 문자에 들여쓰기를 맞춥니다.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

이 출력을 가져오려면 다음을 수행합니다.

> 1. 첫 번째 요소의 경우 1 뒤에 단일 공백을 삽입합니다. 긴 문장은 다음 줄로 래핑되어야 하며 번호가 매겨진 목록 마커 뒤 첫 번째 문자에 맞춰 정렬되어야 합니다.
>
>    이 요소 같은 두 번째 요소를 포함하려면 첫 번째 요소 뒤에 줄 바꿈을 삽입하고 들여쓰기를 맞춥니다. 두 번째 요소의 들여쓰기는 번호가 매겨진 목록 마커 뒤 첫 번째 문자에 맞춰 정렬되어야 합니다. 이 항목 같은 단일 숫자 항목의 경우 열 4로 들여 씁니다. 2자리 숫자 항목(예: 항목 번호 10)의 경우 열 5로 들여 씁니다.
>
> 1. 번호가 매겨진 다음 항목이 여기에서 시작됩니다.

번호가 매겨진 목록의 모든 항목은 항목별로 증분하는 대신 숫자 `1.`를 사용해야 합니다.
Markdown 렌더링은 값을 자동으로 증분합니다. 이로 인해 항목이 더 쉽게 다시 정렬되며 하위 콘텐츠의 들여쓰기가 표준화됩니다.

## <a name="formatting-command-syntax-elements"></a>명령 구문 요소 서식 지정

- PowerShell cmdlet 이름은 [파스칼식 대/소문자로 지정][pascal-case]됩니다. 동사는 하이픈으로 명사와 구분됩니다. cmdlet 및 매개 변수에는 항상 전체 파스칼 대/소문자 이름을 사용합니다. 특별히 별칭을 설명하지 않는 경우에는 별칭을 사용하지 마세요.

- 단락 내에서 언어 키워드, cmdlet 이름 및 변수는 억음 악센트(`` ` ``) 문자로 래핑되어야 합니다. 속성, 매개 변수 및 클래스 이름은 **굵게** 표시되어야 합니다.

  예:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- 이름으로 매개 변수를 참조하는 경우 이름은 **굵게** 표시되어야 합니다. 하이픈 접두사로 매개 변수 사용을 나타내는 경우 매개 변수는 억음 악센트로 래핑되어야 합니다. 예:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- 외부 명령(EXE, 스크립트 등)을 참조하는 경우 명령 이름은 굵게 표시되고, 모두 소문자이며(또는 문장의 시작 구분인 경우 대문자로 시작됨), 적절한 파일 확장명을 포함해야 합니다. 예:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- 외부 명령의 사용 예제를 표시하는 경우 예제는 억음 악센트로 래핑되어야 합니다.
  별칭과 이름이 충돌하는 경우 명령 예제에 파일 확장명을 포함해야 합니다. 예:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- 개념 문서(참조 콘텐츠가 아님)를 작성하는 경우 cmdlet 이름의 첫 번째 인스턴스는 cmdlet 문서에 연결되어야 합니다. 하이퍼링크의 대괄호 안에 억음 악센트, 굵게 또는 기타 태그를 사용하지 마세요.

  예:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  자세한 내용은 스타일 가이드의 [하이퍼링크](#hyperlinks) 섹션을 참조하세요.

## <a name="images"></a>이미지

이미지를 포함하는 구문은 다음과 같습니다.

```Syntax
![[alt text]](<folderPath>)
```

예제:

```markdown
![Introduction](./media/overview/Introduction.png)
```

여기서 `alt text`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다. 시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다. 이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.

이미지는 문서를 포함하는 폴더 내의 `media/<article-name>` 폴더에 저장해야 합니다. 이미지는 문서 간에 공유되지 않아야 합니다. `media` 폴더 아래 문서의 파일 이름과 일치하는 폴더를 만듭니다. 해당 문서의 이미지를 해당하는 새 폴더로 복사합니다. 이미지가 여러 문서에서 사용되는 경우 각 이미지 폴더에는 해당 이미지 파일의 복사본이 있어야 합니다. 이 사례에서는 다른 문서에 영향을 주는 문서에서 이미지가 변경되지 않습니다.

경우에 따라 여러 문서에서 로고 및 아이콘 같은 이미지를 공유하려고 합니다. 이 이미지는 리포지토리의 루트에 있는 `/media/shared` 폴더에 저장됩니다.

지원되는 이미지 파일 형식은 *.png", *.gif", *.jpeg", *.jpg", *.svg임

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
