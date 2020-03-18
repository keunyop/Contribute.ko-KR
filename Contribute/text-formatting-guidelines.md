---
title: 텍스트 서식 지정 지침
description: docs.microsoft.com 사이트에 게시된 문서에서 굵게, 기울임꼴, 코드 및 다른 텍스트 스타일을 사용하는 경우에 대해 알아봅니다.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336491"
---
# <a name="text-formatting-guidelines"></a>텍스트 서식 지정 지침

텍스트 요소에 대해 굵게, 기울임꼴 및 코드 스타일을 일관되고 적절하게 사용하면 가독성이 향상되고 잘못 이해하지 않도록 방지할 수 있습니다.

## <a name="bold"></a>굵게

메뉴 선택, 대화 상자 이름 및 입력 필드 이름과 같은 UI 요소에 굵게를 사용합니다.

### <a name="examples"></a>예제

* **적용됨**: **솔루션 탐색기**에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 **추가 > 새 항목**을 차례로 선택합니다.
* **적용되지 않음**: 솔루션 탐색기에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 [추가 > 새 항목]을 차례로 선택합니다.
* **적용되지 않음**: ‘솔루션 탐색기’에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 ‘추가 > 새 항목’을 차례로 선택합니다.  

## <a name="italics"></a>기울임꼴

기울임꼴을 사용하는 항목은 다음과 같습니다.

* 정의 또는 설명과 함께 소개하는 새 용어
* 파일 이름, 폴더 이름, 경로
* 사용자 입력

### <a name="examples"></a>예제

* **적용됨**: App Service에서는 앱이 ‘App Service 계획’에서 실행됩니다.  App Service 계획은 웹앱이 실행될 컴퓨팅 리소스 집합을 정의합니다.
* **적용되지 않음**: App Service에서는 앱이 “App Service 계획”에서 실행됩니다. App Service 계획은 웹앱이 실행될 컴퓨팅 리소스 집합을 정의합니다.
* **적용됨**: *HttpTriggerCSharp.cs*의 코드를 다음 코드로 바꿉니다.
* **적용되지 않음**: `HttpTriggerCSharp.cs`의 코드를 다음 코드로 바꿉니다.
* **적용됨**: **이름**에 *ContosoUniversity*를 입력하고 **추가**를 선택합니다.
* **적용되지 않음**: **이름**에 “ContosoUniversity”를 입력하고 **추가**를 선택합니다.

## <a name="code-style"></a>코드 스타일

코드 스타일을 사용하는 항목은 다음과 같습니다.

* 메서드 이름, 속성 이름 및 언어 키워드와 같은 코드 요소
* SQL 명령
* NuGet 패키지 이름
* 명령줄 명령
* 데이터베이스 테이블 및 열 이름
* 지역화되지 않아야 하는 리소스 이름(예: 가상 머신 이름)
* 클릭할 수 없게 하려는 URL

**적용 근거** 이전 스타일 가이드에서는 이러한 텍스트 요소 중 다수에 대해 굵게를 지정합니다. 하지만 대부분의 문서는 지역화되며, 코드 스타일은 텍스트의 해당 부분을 번역하지 않도록 번역기에 지시합니다.

코드 스타일은 여러 줄로 되어 있는 ‘인라인’ 코드 블록(\`로 묶임)이거나 ‘펜싱된’ 코드 블록(\`\`\`로 묶임)일 수 있습니다.   긴 코드 조각과 경로는 펜스를 친 코드 블록에 넣습니다.

### <a name="examples-using-inline-styles"></a>인라인 스타일을 사용하는 예제

* **적용됨**: 기본적으로 Entity Framework에서 `Id` 또는 `ClassnameID`라는 속성을 기본 키로 해석합니다.
* **적용되지 않음**: 기본적으로 Entity Framework에서 *Id* 또는 *ClassnameID*라는 속성을 기본 키로 해석합니다.
* **적용됨**: `Microsoft.EntityFrameworkCore` 패키지는 EF Core에 대한 런타임 지원을 제공합니다.
* **적용되지 않음**: *Microsoft.EntityFrameworkCore* 패키지는 EF Core에 대한 런타임 지원을 제공합니다.

### <a name="examples-of-fenced-code-blocks"></a>펜스를 친 코드 블록의 예

* **적용됨**: 다음 코드와 같이 `IQueryable`만 변경하는 명령문으로는 어떤 명령도 데이터베이스로 보낼 수 없습니다.

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **적용되지 않음**: **var students = context.Students.Where(s => s.LastName == "Davolio")** 와 같이 **IQueryable**만 변경하는 명령문으로는 어떤 명령도 데이터베이스로 보낼 수 없습니다.

* **적용됨**: 예를 들어 `C:\Scripts` 디렉터리에서 `Get-ServiceLog.ps1` 스크립트를 실행하려면 다음과 같이 입력합니다.

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **적용되지 않음**: 예를 들어 **C:\Scripts** 디렉터리에서 **Get-ServiceLog.ps1** 스크립트를 실행하려면 “C:\Scripts\Get-ServiceLog.ps1”을 입력합니다.

* 펜싱된 코드 블록 **모두**에 승인된 언어 태그가 있어야 합니다. 지원 언어 태그 목록은 [문서에 코드를 포함하는 방법](./code-in-docs.md#supported-languages)을 참조하세요.

## <a name="headings-and-link-text"></a>제목 및 링크 텍스트

제목이나 하이퍼링크 텍스트에는 기울임꼴, 굵게 또는 코드와 같은 인라인 스타일을 적용하지 않습니다.

**적용 근거**

사용자는 표준 하이퍼링크 텍스트를 사용하여 텍스트 요소를 클릭 가능한 링크로 식별합니다. 예를 들어 링크의 스타일을 코드로 지정하면 텍스트가 링크임을 이해하기 어렵게 만들 수 있습니다. 제목에는 자체의 스타일이 있으며, 다른 스타일과 혼합되면 보기에 좋지 않습니다.

### <a name="examples"></a>예제

* **적용됨**: *function.json* 파일이 [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) NuGet 패키지에서 생성됩니다.
* **적용되지 않음**: *function.json* 파일은 [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) NuGet 패키지에서 생성됩니다.

* **적용됨**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **적용되지 않음**:

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>키 및 바로 가기 키

키 또는 키 조합을 나타내는 경우 다음 규칙을 따릅니다.

* 키 이름의 첫 글자는 대문자로 표시합니다.
* 기울임꼴, 굵게 또는 코드와 같은 인라인 스타일을 적용하지 않습니다.
* 동시에 누르는 키를 조인하려면 “+”를 사용합니다.

### <a name="examples"></a>예제

* **적용됨**: Alt+Ctrl+S를 선택합니다.
* **적용되지 않음**: **Alt+Ctrl+S**를 누릅니다.
* **적용되지 않음**: `ALT+CTRL+S`를 누릅니다.

자세한 내용은 [UI 조작 설명](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472)을 참조하세요.

## <a name="exceptions"></a>예외

스타일 지침은 엄격한 규칙이 아닙니다. 지침을 따르면 가독성이 손상되는 컨텍스트에서는 다른 방식으로 작업을 수행하세요. 예를 들어 대부분 코드 요소로 채워진 HTML 테이블에는 어디서나 코드 스타일이 아주 많이 적용될 수 있습니다. 해당 컨텍스트에서는 굵게 스타일 지정을 선택할 수 있습니다.

일반적으로 코드가 호출되는 다른 텍스트 스타일을 선택하는 경우 문서의 지역화된 버전으로 텍스트를 번역할 수 있는지 확인합니다. 코드는 번역을 자동으로 방지하는 유일한 스타일입니다. 코드 스타일을 사용하지 않고도 지역화를 방지하려는 시나리오의 경우 [지역화되지 않은 문자열](markdown-reference.md#non-localized-strings)을 참조하세요.
