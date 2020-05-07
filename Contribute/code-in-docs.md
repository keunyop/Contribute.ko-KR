---
title: 문서에 코드를 포함하는 방법
description: docs.microsoft.com에 게시되는 문서에 코드 요소와 코드 조각을 포함하는 방법을 알아봅니다.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336481"
---
# <a name="how-to-include-code-in-docs"></a>문서에 코드를 포함하는 방법

docs.microsoft.com에 게시되는 문서에 코드를 포함하는 다음 몇 가지 방법이 있습니다.

* 한 줄에 개별 요소(단어) 포함

  다음은 `code` 스타일의 예입니다.

  텍스트에서 근접한 코드 블록의 명명된 매개 변수 및 변수를 참조하는 경우 코드 서식을 사용합니다. 속성, 메서드, 클래스 및 언어 키워드에도 코드 서식을 사용할 수 있습니다. 자세한 내용은 이 문서의 뒷부분에서 [코드 요소](#code-elements)를 참조하세요.

* 문서 Markdown 파일에 코드 블록 포함

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  코드 파일을 참조하여 코드를 표시하는 것이 비실용적인 경우 인라인 코드 블록을 사용합니다. 자세한 내용은 이 문서의 뒷부분에서 [코드 블록](#inline-code-blocks)을 참조하세요.

* 로컬 리포지토리의 코드 파일을 참조하여 코드 블록 포함

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  자세한 내용은 이 문서의 뒷부분에서 [리포지토리 내부 코드 조각 참조](#in-repo-snippet-references)를 참조하세요.

* 다른 리포지토리의 코드 파일을 참조하여 코드 블록 포함

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  자세한 내용은 이 문서의 뒷부분에서 [리포지토리 외부 코드 조각 참조](#out-of-repo-snippet-references)를 참조하세요.
  
* 사용자가 브라우저에서 코드를 실행할 수 있는 코드 블록 포함

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  자세한 내용은 이 문서의 뒷부분에서 [대화형 코드 조각](#interactive-code-snippets)을 참조하세요.

이 문서는 이러한 각 코드 포함 방법에 대한 Markdown 설명은 물론, [모든 코드 블록에 대한 몇 가지 일반적인 지침](#code-blocks)도 제공합니다.

## <a name="code-elements"></a>코드 요소

“코드 요소”는 프로그래밍 언어 키워드, 클래스 이름, 속성 이름 등입니다. 코드로 간주되는 요소가 항상 명확한 것은 아닙니다. 예를 들어 NuGet 패키지 이름은 코드로 처리되어야 합니다. 확실하지 않은 경우 [텍스트 서식 지정 지침](text-formatting-guidelines.md)을 참조하세요.

### <a name="inline-code-style"></a>인라인 코드 스타일

문서 텍스트에 코드 요소를 포함하려면 backtick(\`)으로 둘러싸서 코드 스타일을 나타냅니다.
인라인 코드 스타일에서는 세 개의 억음 악센트 기호 서식을 사용하지 않아야 합니다.

|Markdown |렌더링됨 |
|---------|---------|
|기본적으로 Entity Framework에서 \`Id\` 또는 \`ClassnameID\`라는 속성을 기본 키로 해석합니다.|기본적으로 Entity Framework에서 `Id` 또는 `ClassnameID`라는 속성을 기본 키로 해석합니다.|

문서를 지역화(다른 언어로 번역)할 때 코드 스타일이 지정된 텍스트는 번역되지 않습니다. 코드 스타일을 사용하지 않으면 지역화되지 않도록 하려는 경우 [지역화되지 않은 문자열](markdown-reference.md#non-localized-strings)을 참조하세요.

### <a name="bold-style"></a>굵게 스타일

일부 이전 스타일에서는 인라인 코드에 굵게가 지정됩니다. 굵게는 코드 스타일이 너무 두드러져서 가독성이 저하되는 경우에 사용할 수 있는 옵션입니다. 예를 들어 대부분 코드 요소로 채워진 Markdown 테이블에서는 코드 스타일이 과도하게 적용될 수 있습니다. 굵게 스타일을 사용하도록 선택하는 경우 [지역화되지 않은 문자열 구문](markdown-reference.md#non-localized-strings)을 사용하여 코드가 지역화되지 않도록 합니다.

### <a name="links"></a>링크

일부 컨텍스트에서는 코드 서식보다 참조 설명서 링크가 유용할 수 있습니다. 링크를 사용하는 경우 링크 텍스트에 코드 서식을 적용하지 마세요. 링크에 코드 스타일을 지정하면 텍스트가 링크인지 구분하기 어려울 수 있습니다.

링크를 사용하고 나중에 동일한 컨텍스트에서 동일한 요소를 참조하는 경우 후속 인스턴스는 링크가 아닌 코드 서식으로 만듭니다.

### <a name="placeholders"></a>자리 표시자

사용자가 표시된 코드 섹션을 고유한 값으로 바꾸도록 하려면 꺾쇠 괄호 또는 중괄호로 표시된 자리 표시자 텍스트를 사용합니다. `az group delete -n <ResourceGroupName>`를 예로 들 수 있습니다. 실제 값을 대체하는 경우 꺾쇠 괄호 또는 중괄호가 제거되어야 함을 설명하세요.

## <a name="code-blocks"></a>코드 블록

문서에 코드를 포함하는 구문은 코드가 있는 위치에 따라 다릅니다.

* [문서 Markdown 파일에 있는 경우](#inline-code-blocks)
* [동일한 리포지토리의 코드 파일에 있는 경우](#in-repo-snippet-references)
* [다른 리포지토리의 코드 파일에 있는 경우](#out-of-repo-snippet-references)

다음은 세 가지 유형의 코드 블록에 모두 적용되는 지침입니다.

* [코드 유효성 검사 자동화](#code-validation)
* [주요 코드 줄 강조 표시](#highlighting)
* [가로 스크롤 막대 사용 금지](#horizontal-scroll-bars)

### <a name="screenshots"></a>스크린샷

이전 섹션에 나온 방법은 모두 사용 가능한 코드 블록을 생성합니다.

* 복사하여 붙여넣을 수 있습니다.
* 검색 엔진에서 인덱싱됩니다.
* 화면 읽기 프로그램에서 액세스할 수 있습니다.

이는 문서에 코드를 포함하는 방법으로 IDE 스크린샷이 권장되지 않는 이유 중 일부분에 불과합니다. IDE 스크린샷은 IntelliSense와 같이 IDE 자체에 대한 어떤 정보를 표시하는 경우에만 코드용으로 사용하세요. 색 지정 및 강조 표시를 보여 주는 데는 스크린샷을 사용하지 마세요.

### <a name="code-validation"></a>코드 유효성 검사

일부 리포지토리에는 모든 샘플 코드를 자동으로 컴파일하여 오류를 확인하는 프로세스가 구현되어 있습니다. .NET 리포지토리에서도 이렇게 합니다. 자세한 내용은 .NET 리포지토리의 [기여](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md)를 참조하세요.

다른 리포지토리의 코드 블록을 포함하는 경우 코드 유지 관리 전략에 따라 소유자와 협력하여 코드에서 사용하는 라이브러리의 새 버전이 제공되어도 포함된 코드가 나뉘거나 최신 상태를 유지하지 못하는 일이 없도록 합니다.

### <a name="highlighting"></a>강조 표시

일반적으로 코드 조각은 컨텍스트를 제공하는 데 필요한 것보다 많은 코드를 포함합니다. 이 예제와 같이 코드 조각에서 중점을 두는 주요 줄을 강조 표시하면 가독성에 도움이 됩니다.

![강조 표시된 코드를 보여주는 예제](media/code-in-docs/highlighted-code.png)

문서 Markdown 파일에 포함할 때는 코드를 강조 표시할 수 없습니다. 코드 파일을 참조하여 포함된 코드 조각에만 사용할 수 있습니다.

### <a name="horizontal-scroll-bars"></a>가로 스크롤 막대

긴 줄을 나눠서 가로 스크롤 막대가 표시되지 않도록 합니다. 코드 블록에 스크롤 막대가 있으면 코드를 읽기 어렵습니다. 특히 스크롤 막대와 읽으려는 줄을 동시에 볼 수 없는 긴 코드 블록에서 문제가 됩니다.

코드 블록에서 가로 스크롤 막대를 최소화하는 좋은 방법은 85자보다 긴 코드 줄을 나누는 것입니다. 하지만 스크롤 막대의 유무가 가독성의 유일한 기준은 아니라는 점에 유의하세요. 줄을 85자 미만으로 나누면 가독성이나 복사-붙여넣기 편의성이 손상되는 경우 얼마든지 줄을 85자 이상으로 할 수 있습니다.

## <a name="inline-code-blocks"></a>인라인 코드 블록

코드 파일을 참조하여 코드를 표시하는 것이 비실용적인 경우에만 인라인 코드 블록을 사용합니다. 인라인 코드는 일반적으로 전체 프로젝트의 일부인 코드 파일보다 테스트 및 최신 상태 유지가 더 어렵습니다.  인라인 코드에는 개발자가 코드를 이해하고 사용하는 데 도움이 되는 컨텍스트가 생략될 수도 있습니다. 이러한 고려 사항은 주로 프로그래밍 언어에 적용됩니다. 인라인 코드 블록은 출력 및 입력(예: JSON), 쿼리 언어(예: SQL), 스크립팅 언어(예: PowerShell)에도 사용될 수 있습니다.
  
문서 파일에서 텍스트 섹션을 나타내는 두 가지 방법은 backtick 3개(\`\`\`)로 ‘펜싱’하거나 들여쓰기를 사용한 코드 블록입니다. 언어를 지정할 수 있는 펜싱을 사용하는 것이 좋습니다. 들여쓰기는 너무 간단하여 실수하기가 쉽고 다른 작성자가 문서를 편집해야 할 때 원래 작성자의 의도를 이해하기 어려울 수 있으므로 사용하지 않는 것이 좋습니다.

언어 표시기는 다음 예제와 같이 여는 backtick 3개 바로 뒤에 옵니다.

Markdown:

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

렌더링됨:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

언어 표시기로 사용할 수 있는 값에 대한 자세한 내용은 [언어 이름 및 별칭](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases)을 참조하세요.

세 개의 억음 악센트 기호(\`\`\`) 뒤에 지원되지 않는 언어 또는 환경 단어를 사용하는 경우 해당 단어가 렌더링된 페이지의 코드 섹션 제목 표시줄에 표시됩니다. 가능한 한 언어 또는 환경 표시기를 인라인 코드 블록에 사용하세요.

> [!NOTE]
> Word 문서에서 코드를 복사하여 붙여넣는 경우 코드에 유효하지 않은 “둥근 따옴표”(예: `“` 및 `’`)가 없는지 확인합니다. 둥근 따옴표가 있으면 일반 따옴표(`'` 및 `"`)로 다시 변경합니다. 또는 Docs Authoring Pack의 [둥근 따옴표 바꾸기 기능](docs-authoring/smart-quote-replacement.md)을 사용합니다.

## <a name="in-repo-snippet-references"></a>리포지토리 내부 코드 조각 참조

프로그래밍 언어에 필요한 코드 조각을 문서에 포함하려면 코드 파일을 참조하는 방법을 사용하는 것이 좋습니다. 이 방법을 사용하면 코드 줄을 강조 표시할 수 있고 개발자가 GitHub에서 더 넓은 범위의 코드 조각 컨텍스트를 사용하도록 할 수 있습니다. 수동으로 또는 Visual Studio Code에서 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 지원을 통해 세 개의 콜론 서식(:\:\:)을 사용하여 코드를 포함할 수 있습니다.

1. Visual Studio Code에서 <kbd>Alt + M</kbd> 또는 <kbd>Option + M</kbd>을 클릭하고 코드 조각을 선택합니다.
2. 코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다. 로컬에서 검색하려면 전체 검색을 선택합니다.
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

코드 조각 이름을 지정하여 코드 파일의 일부 표시:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

다음 섹션에서는 이러한 예제를 설명합니다.

* [코드 파일의 상대 경로 사용](#path-to-code-file)
* [선택한 줄 번호만 포함](#selected-line-numbers)
* [명명된 코드 조각 참조](#named-snippet)
* [선택한 줄 강조 표시](#highlighting-selected-lines)

자세한 내용은 이 문서의 뒷부분에서 [코드 조각 구문 참조](#snippet-syntax-reference)를 참조하세요.

### <a name="path-to-code-file"></a>코드 파일의 경로

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

이 예제는 ASP.NET 문서 리포지토리, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 문서 파일에서 가져온 것입니다. 코드 파일은 동일한 리포지토리에 있는 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs)의 상대 경로로 참조됩니다.

### <a name="selected-line-numbers"></a>선택한 줄 번호

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

위 예제에서는 *StudentController.cs* 코드 파일의 줄 2~24와 26만 표시됩니다.

다음 섹션에 설명된 대로 하드 코드된 줄 번호보다 명명된 코드 조각을 사용하는 것이 좋습니다.

### <a name="named-snippet"></a>명명된 코드 조각

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

이름에는 문자와 밑줄만 사용합니다.

이 예제는 코드 파일의 `snippet_Create` 섹션을 표시합니다. 이 예제의 코드 파일에는 C# 코드의 주석에 코드 조각 태그가 있습니다.

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

가능한 한, 줄 번호를 지정하지 말고 명명된 섹션을 참조하세요. 코드 파일은 필연적으로 변경되고, 이 경우 줄 번호도 변경되기 때문에 줄 번호 참조는 불안정합니다.
항상 이러한 변경에 대한 알림을 받는 것은 아닙니다. 결국 문서에서 잘못된 줄이 나타나기 시작해도 무엇이 변경되었는지 알 수 없습니다.

### <a name="highlighting-selected-lines"></a>선택한 줄 강조 표시

예제:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

이 예제에서는 표시된 코드 조각의 처음부터 줄 2와 5를 강조 표시합니다. 강조 표시할 줄 번호가 코드 파일의 처음부터 계산되지 않습니다. 즉, 코드 파일의 줄 3과 6이 강조 표시됩니다.

## <a name="out-of-repo-snippet-references"></a>리포지토리 외부 코드 조각 참조

참조하려는 코드 파일이 다른 리포지토리에 있으면 코드 리포지토리를 ‘종속 리포지토리’로 설정합니다. 이 경우 이름을 지정합니다. 이 이름은 코드 참조를 위해 폴더 이름과 같이 작동합니다.

예를 들어 문서 리포지토리는 *Azure/azure-docs*이고, 코드 리포지토리는 *Azure/azure-functions-durable-extension*입니다.

*azure-docs*의 루트 폴더에 있는 *.openpublishing.publish.config.json*에 다음 섹션을 추가합니다.

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

이제 *azure-docs*에 있는 폴더처럼 *sample-durable-functions*를 참조할 때 실제로는 *azure-functions-durable-extension* 리포지토리에 있는 루트 폴더를 참조하게 됩니다.

수동으로 또는 Visual Studio Code에서 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 지원을 통해 세 개의 콜론 서식(:\:\:)을 사용하여 코드를 포함할 수 있습니다.

1. Visual Studio Code에서 <kbd>Alt + M</kbd> 또는 <kbd>Option + M</kbd>을 클릭하고 코드 조각을 선택합니다.
2. 코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다. 리포지토리에서 검색하려면 리포지토리 간 참조를 선택합니다.
3. *.openpublishing.publish.config.json*에 있는 리포지토리에서 선택할 수 있습니다. 리포지토리를 선택합니다.
4. 검색 용어를 입력하여 파일을 찾습니다. 파일을 찾으면 선택합니다.
5. 다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다. 옵션은 **ID**, **범위**, **없음**입니다.
6. 5단계에서 선택한 옵션에 따라 값을 입력합니다.

코드 조각 참조는 다음과 같이 표시됩니다.

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

*azure-functions-durable-extension* 리포지토리에서 해당 코드 파일은 *samples/csx/shared* 폴더에 있습니다. [앞에서](#highlighting-selected-lines) 설명했듯이 강조 표시할 줄 번호는 파일의 시작이 아니라 코드 조각의 시작 부분을 기준으로 합니다.

> [!NOTE]
> 종속 리포지토리에 할당되는 이름은 기본 리포지토리 루트를 기준으로 하지만 물결표(~)는 문서 집합 루트를 나타냅니다. 문서 집합 루트는 *.openpublishing.publish.config.json*의 `build_source_folder`에 따라 결정됩니다. `build_source_folder`가 리포 루트(`.`)를 나타내므로 앞의 예제에서 코드 조각의 경로는 azure-docs 리포지토리에 포함됩니다. `build_source_folder`가 `articles`면 경로는 `~/samples-durable-functions`가 아니라 `~/../samples-durable-functions`로 시작합니다.

## <a name="interactive-code-snippets"></a>대화형 코드 조각

### <a name="inline-interactive-code-blocks"></a>인라인 대화형 코드 블록

다음 언어의 경우 브라우저 창에서 코드 조각을 실행 가능하게 만들 수 있습니다.

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

대화형 모드를 사용하도록 설정한 경우 렌더링된 코드 상자에 **시도** 또는 **실행** 단추가 있습니다. 예:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

은(는) 다음과 같이 렌더링됩니다.

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

특정 코드 블록에 대해 이 기능을 켜려면 특수 언어 식별자를 사용합니다. 사용 가능한 옵션은 다음과 같습니다.

* `azurepowershell-interactive` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정
* `azurecli-interactive` - Azure Cloud Shell을 사용하도록 설정
* `csharp-interactive` - C# REPL을 사용하도록 설정

Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.

### <a name="code-snippets-included-by-reference"></a>참조하여 포함된 코드 조각

참조를 통해 포함된 코드 조각에 대해 대화형 모드를 사용하도록 설정할 수 있습니다. 예제는 다음과 같습니다.

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

특정 코드 블록을 대상으로 이 기능을 켜려면 `interactive` 특성을 사용합니다. 사용 가능한 특성 값은 다음과 같습니다.

* `cloudshell-powershell` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정
* `cloudshell-bash` - Azure Cloud Shell을 사용하도록 설정
* `try-dotnet` - Try .NET을 사용하도록 설정
* `try-dotnet-class` - 클래스 스캐폴딩으로 Try .NET을 사용하도록 설정
* `try-dotnet-method` - 메서드 스캐폴딩으로 Try .NET을 사용하도록 설정

Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.

## <a name="snippet-syntax-reference"></a>코드 조각 구문 참조

구문:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> 이 구문은 블록 Markdown 확장입니다. 자체 줄에 사용해야 합니다.

* `<language>`(*선택 사항*)
  * 코드 조각의 언어입니다. 자세한 내용은 본 문서의 아래에 있는 [지원되는 언어](#supported-languages) 섹션을 참조하세요.

* `<path>`(*필수*)
  * 참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다.

* `<attribute>` 및 `<attribute-value>`(*선택 사항*)
  * 파일에서 코드를 검색하는 방법과 표시하는 방법을 지정하는 데 함께 사용됩니다.
    * `range`: `1,3-5` 줄 범위입니다. 이 예제는 1, 3, 4 및 5 줄을 포함합니다.
    * `id`: `snippet_Create` 코드 파일에서 삽입해야 하는 코드 조각의 ID입니다. 이 값은 범위와 함께 사용할 수 없습니다.
    * `highlight`: `2-4,6` 생성된 코드 조각에서 강조 표시해야 하는 범위 및/또는 줄 수입니다. 번호 매기기는 파일이 아니라 표시된 줄(범위 또는 ID로 지정됨)을 기준으로 합니다.
    * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` 문자열 값은 어떤 종류의 대화형 작업이 사용하도록 설정되는지를 결정합니다.
    * 코드 조각 소스의 태그 이름 표현에 대한 자세한 내용을 언어별로 보려면 [DocFX 지침](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)을 참조하세요.

## <a name="supported-languages"></a>지원되는 언어

[Docs Authoring Pack](how-to-write-docs-auth-pack.md)에는 코드 펜스 블록에 사용할 수 있는 언어 식별자에 대한 문 완성 및 유효성 검사를 제공하는 기능이 포함되어 있습니다.

### <a name="fenced-code-blocks"></a>펜싱된 코드 블록

| Name                           | 유효한 별칭                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Access logs                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| ARM assembler                  | `armasm`, `arm`                                                                |
| AVR assembler                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET(C#)                   | `aspx-csharp`                                                                  |
| ASP.NET(VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap’n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| DNS Zone file                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (Device Tree)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| MOF(Managed Object Format)          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Plaintext no highlight         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| 속성                     | `properties`                                                                   |
| Protocol Buffers               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python profiler results        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM spec files                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| 셸                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Structured Text                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> Docs Authoring Pack의 [개발자 언어 완성 기능](docs-authoring/dev-lang-completion.md)은 여러 별칭을 사용할 수 있는 경우 첫 번째 유효한 별칭을 사용합니다.

## <a name="next-steps"></a>다음 단계

코드 이외의 콘텐츠 유형 텍스트 서식 지정에 대한 자세한 내용은 [텍스트 서식 지정 지침](text-formatting-guidelines.md)을 참조하세요.
