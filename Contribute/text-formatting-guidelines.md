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
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336491"
---
# <a name="text-formatting-guidelines"></a><span data-ttu-id="8e3aa-103">텍스트 서식 지정 지침</span><span class="sxs-lookup"><span data-stu-id="8e3aa-103">Text formatting guidelines</span></span>

<span data-ttu-id="8e3aa-104">텍스트 요소에 대해 굵게, 기울임꼴 및 코드 스타일을 일관되고 적절하게 사용하면 가독성이 향상되고 잘못 이해하지 않도록 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-104">Consistent and appropriate use of bold, italic, and code style for text elements improves readability and helps avoid misunderstandings.</span></span>

## <a name="bold"></a><span data-ttu-id="8e3aa-105">굵게</span><span class="sxs-lookup"><span data-stu-id="8e3aa-105">Bold</span></span>

<span data-ttu-id="8e3aa-106">메뉴 선택, 대화 상자 이름 및 입력 필드 이름과 같은 UI 요소에 굵게를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-106">Use bold for UI elements, such as menu selections, dialog box names, and input field names.</span></span>

### <a name="examples"></a><span data-ttu-id="8e3aa-107">예제</span><span class="sxs-lookup"><span data-stu-id="8e3aa-107">Examples</span></span>

* <span data-ttu-id="8e3aa-108">**적용됨**: **솔루션 탐색기**에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 **추가 > 새 항목**을 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-108">**This**: In **Solution Explorer**, right-click the project node, and then select **Add > New Item**.</span></span>
* <span data-ttu-id="8e3aa-109">**적용되지 않음**: 솔루션 탐색기에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 [추가 > 새 항목]을 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-109">**Not this**: In Solution Explorer, right-click the project node, and then select Add > New Item.</span></span>
* <span data-ttu-id="8e3aa-110">**적용되지 않음**: ‘솔루션 탐색기’에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 ‘추가 > 새 항목’을 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-110">**Not this**: In *Solution Explorer*, right-click the project node, and then select *Add > New Item*.</span></span>

## <a name="italics"></a><span data-ttu-id="8e3aa-111">기울임꼴</span><span class="sxs-lookup"><span data-stu-id="8e3aa-111">Italics</span></span>

<span data-ttu-id="8e3aa-112">기울임꼴을 사용하는 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-112">Use italics for:</span></span>

* <span data-ttu-id="8e3aa-113">정의 또는 설명과 함께 소개하는 새 용어</span><span class="sxs-lookup"><span data-stu-id="8e3aa-113">Introducing new terms along with a definition or explanation.</span></span>
* <span data-ttu-id="8e3aa-114">파일 이름, 폴더 이름, 경로</span><span class="sxs-lookup"><span data-stu-id="8e3aa-114">File names, folder names, paths.</span></span>
* <span data-ttu-id="8e3aa-115">사용자 입력</span><span class="sxs-lookup"><span data-stu-id="8e3aa-115">User input.</span></span>

### <a name="examples"></a><span data-ttu-id="8e3aa-116">예제</span><span class="sxs-lookup"><span data-stu-id="8e3aa-116">Examples</span></span>

* <span data-ttu-id="8e3aa-117">**적용됨**: App Service에서는 앱이 ‘App Service 계획’에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-117">**This**: In App Service, an app runs in an *App Service plan*.</span></span> <span data-ttu-id="8e3aa-118">App Service 계획은 웹앱이 실행될 컴퓨팅 리소스 집합을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-118">An App Service plan defines a set of compute resources for a web app to run on.</span></span>
* <span data-ttu-id="8e3aa-119">**적용되지 않음**: App Service에서는 앱이 “App Service 계획”에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-119">**Not this**: In App Service, an app runs in an "App Service plan."</span></span> <span data-ttu-id="8e3aa-120">App Service 계획은 웹앱이 실행될 컴퓨팅 리소스 집합을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-120">An App Service plan defines a set of compute resources for a web app to run on.</span></span>
* <span data-ttu-id="8e3aa-121">**적용됨**: *HttpTriggerCSharp.cs*의 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-121">**This**: Replace the code in *HttpTriggerCSharp.cs* with the following code.</span></span>
* <span data-ttu-id="8e3aa-122">**적용되지 않음**: `HttpTriggerCSharp.cs`의 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-122">**Not this**: Replace the code in `HttpTriggerCSharp.cs` with the following code.</span></span>
* <span data-ttu-id="8e3aa-123">**적용됨**: **이름**에 *ContosoUniversity*를 입력하고 **추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-123">**This**: Enter *ContosoUniversity* for the **Name**, and then select **Add**.</span></span>
* <span data-ttu-id="8e3aa-124">**적용되지 않음**: **이름**에 “ContosoUniversity”를 입력하고 **추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-124">**Not this**: Enter "ContosoUniversity" for the **Name**, and then select **Add**.</span></span>

## <a name="code-style"></a><span data-ttu-id="8e3aa-125">코드 스타일</span><span class="sxs-lookup"><span data-stu-id="8e3aa-125">Code style</span></span>

<span data-ttu-id="8e3aa-126">코드 스타일을 사용하는 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-126">Use code style for:</span></span>

* <span data-ttu-id="8e3aa-127">메서드 이름, 속성 이름 및 언어 키워드와 같은 코드 요소</span><span class="sxs-lookup"><span data-stu-id="8e3aa-127">Code elements, such as method names, property names, and language keywords.</span></span>
* <span data-ttu-id="8e3aa-128">SQL 명령</span><span class="sxs-lookup"><span data-stu-id="8e3aa-128">SQL commands</span></span>
* <span data-ttu-id="8e3aa-129">NuGet 패키지 이름</span><span class="sxs-lookup"><span data-stu-id="8e3aa-129">NuGet package names</span></span>
* <span data-ttu-id="8e3aa-130">명령줄 명령</span><span class="sxs-lookup"><span data-stu-id="8e3aa-130">Command-line commands</span></span>
* <span data-ttu-id="8e3aa-131">데이터베이스 테이블 및 열 이름</span><span class="sxs-lookup"><span data-stu-id="8e3aa-131">Database table and column names</span></span>
* <span data-ttu-id="8e3aa-132">지역화되지 않아야 하는 리소스 이름(예: 가상 머신 이름)</span><span class="sxs-lookup"><span data-stu-id="8e3aa-132">Resource names that should not be localized (such as virtual machine names)</span></span>
* <span data-ttu-id="8e3aa-133">클릭할 수 없게 하려는 URL</span><span class="sxs-lookup"><span data-stu-id="8e3aa-133">URLs that you don't want to be clickable</span></span>

<span data-ttu-id="8e3aa-134">**적용 근거**</span><span class="sxs-lookup"><span data-stu-id="8e3aa-134">**Why?**</span></span> <span data-ttu-id="8e3aa-135">이전 스타일 가이드에서는 이러한 텍스트 요소 중 다수에 대해 굵게를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-135">Older style guides specify bold for many of these text elements.</span></span> <span data-ttu-id="8e3aa-136">하지만 대부분의 문서는 지역화되며, 코드 스타일은 텍스트의 해당 부분을 번역하지 않도록 번역기에 지시합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-136">However, most articles are localized, and code style tells the translator to leave that part of the text untranslated.</span></span>

<span data-ttu-id="8e3aa-137">코드 스타일은 여러 줄로 되어 있는 ‘인라인’ 코드 블록(\`로 묶임)이거나 ‘펜싱된’ 코드 블록(\`\`\`로 묶임)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-137">Code style can be *inline* (surrounded by \`) or *fenced* code blocks (surrounded by \`\`\`) that span multiple lines.</span></span> <span data-ttu-id="8e3aa-138">긴 코드 조각과 경로는 펜스를 친 코드 블록에 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-138">Put longer code snippets and paths in fenced code blocks.</span></span>

### <a name="examples-using-inline-styles"></a><span data-ttu-id="8e3aa-139">인라인 스타일을 사용하는 예제</span><span class="sxs-lookup"><span data-stu-id="8e3aa-139">Examples using inline styles</span></span>

* <span data-ttu-id="8e3aa-140">**적용됨**: 기본적으로 Entity Framework에서 `Id` 또는 `ClassnameID`라는 속성을 기본 키로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-140">**This**: By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>
* <span data-ttu-id="8e3aa-141">**적용되지 않음**: 기본적으로 Entity Framework에서 *Id* 또는 *ClassnameID*라는 속성을 기본 키로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-141">**Not this**: By default, the Entity Framework interprets a property that's named *Id* or *ClassnameID* as the primary key.</span></span>
* <span data-ttu-id="8e3aa-142">**적용됨**: `Microsoft.EntityFrameworkCore` 패키지는 EF Core에 대한 런타임 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-142">**This**: The `Microsoft.EntityFrameworkCore` package provides runtime support for EF Core.</span></span>
* <span data-ttu-id="8e3aa-143">**적용되지 않음**: *Microsoft.EntityFrameworkCore* 패키지는 EF Core에 대한 런타임 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-143">**Not this**: The *Microsoft.EntityFrameworkCore* package provides runtime support for EF Core.</span></span>

### <a name="examples-of-fenced-code-blocks"></a><span data-ttu-id="8e3aa-144">펜스를 친 코드 블록의 예</span><span class="sxs-lookup"><span data-stu-id="8e3aa-144">Examples of fenced code blocks</span></span>

* <span data-ttu-id="8e3aa-145">**적용됨**: 다음 코드와 같이 `IQueryable`만 변경하는 명령문으로는 어떤 명령도 데이터베이스로 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-145">**This**: No commands are sent to the database by statements that just change an `IQueryable`, such as the following code:</span></span>

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* <span data-ttu-id="8e3aa-146">**적용되지 않음**: **var students = context.Students.Where(s => s.LastName == "Davolio")** 와 같이 **IQueryable**만 변경하는 명령문으로는 어떤 명령도 데이터베이스로 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-146">**Not this**: No commands are sent to the database by statements that just change an **IQueryable**, such as **var students = context.Students.Where(s => s.LastName == "Davolio")**.</span></span>

* <span data-ttu-id="8e3aa-147">**적용됨**: 예를 들어 `C:\Scripts` 디렉터리에서 `Get-ServiceLog.ps1` 스크립트를 실행하려면 다음과 같이 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-147">**This**: For example, to run the `Get-ServiceLog.ps1` script in the `C:\Scripts` directory, type:</span></span>

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* <span data-ttu-id="8e3aa-148">**적용되지 않음**: 예를 들어 **C:\Scripts** 디렉터리에서 **Get-ServiceLog.ps1** 스크립트를 실행하려면 “C:\Scripts\Get-ServiceLog.ps1”을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-148">**Not this**: For example, to run the **Get-ServiceLog.ps1** script in the **C:\Scripts** directory, type: "C:\Scripts\Get-ServiceLog.ps1."</span></span>

* <span data-ttu-id="8e3aa-149">펜싱된 코드 블록 **모두**에 승인된 언어 태그가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-149">**All** fenced code blocks must have an approved language tag.</span></span> <span data-ttu-id="8e3aa-150">지원 언어 태그 목록은 [문서에 코드를 포함하는 방법](./code-in-docs.md#supported-languages)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-150">For a list of support language tags, see [How to include code in docs](./code-in-docs.md#supported-languages).</span></span>

## <a name="headings-and-link-text"></a><span data-ttu-id="8e3aa-151">제목 및 링크 텍스트</span><span class="sxs-lookup"><span data-stu-id="8e3aa-151">Headings and link text</span></span>

<span data-ttu-id="8e3aa-152">제목이나 하이퍼링크 텍스트에는 기울임꼴, 굵게 또는 코드와 같은 인라인 스타일을 적용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-152">Don't apply an inline style such as italics, bold, or code to headings or hyperlink text.</span></span>

<span data-ttu-id="8e3aa-153">**적용 근거**</span><span class="sxs-lookup"><span data-stu-id="8e3aa-153">**Why?**</span></span>

<span data-ttu-id="8e3aa-154">사용자는 표준 하이퍼링크 텍스트를 사용하여 텍스트 요소를 클릭 가능한 링크로 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-154">People rely on standard hyperlink text to identify text elements as clickable links.</span></span> <span data-ttu-id="8e3aa-155">예를 들어 링크의 스타일을 코드로 지정하면 텍스트가 링크임을 이해하기 어렵게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-155">Styling a link as code, for example, can obscure the fact that the text is a link.</span></span> <span data-ttu-id="8e3aa-156">제목에는 자체의 스타일이 있으며, 다른 스타일과 혼합되면 보기에 좋지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-156">Headings have their own styles and mixing other styles in them looks bad.</span></span>

### <a name="examples"></a><span data-ttu-id="8e3aa-157">예제</span><span class="sxs-lookup"><span data-stu-id="8e3aa-157">Examples</span></span>

* <span data-ttu-id="8e3aa-158">**적용됨**: *function.json* 파일이 [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) NuGet 패키지에서 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-158">**This**: The *function.json* file is generated by the NuGet package [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).</span></span>
* <span data-ttu-id="8e3aa-159">**적용되지 않음**: *function.json* 파일은 [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) NuGet 패키지에서 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-159">**Not this**: The *function.json* file is generated by the NuGet package [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).</span></span>

* <span data-ttu-id="8e3aa-160">**적용됨**:</span><span class="sxs-lookup"><span data-stu-id="8e3aa-160">**This**:</span></span>

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* <span data-ttu-id="8e3aa-161">**적용되지 않음**:</span><span class="sxs-lookup"><span data-stu-id="8e3aa-161">**Not this**:</span></span>

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a><span data-ttu-id="8e3aa-162">키 및 바로 가기 키</span><span class="sxs-lookup"><span data-stu-id="8e3aa-162">Keys and keyboard shortcuts</span></span>

<span data-ttu-id="8e3aa-163">키 또는 키 조합을 나타내는 경우 다음 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-163">When referring to keys or key combinations, follow these conventions:</span></span>

* <span data-ttu-id="8e3aa-164">키 이름의 첫 글자는 대문자로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-164">Capitalize the first letter of key names.</span></span>
* <span data-ttu-id="8e3aa-165">기울임꼴, 굵게 또는 코드와 같은 인라인 스타일을 적용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-165">Don't apply an inline style such as italics, bold, or code.</span></span>
* <span data-ttu-id="8e3aa-166">동시에 누르는 키를 조인하려면 “+”를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-166">Use "+" to join keys that are pressed at the same time.</span></span>

### <a name="examples"></a><span data-ttu-id="8e3aa-167">예제</span><span class="sxs-lookup"><span data-stu-id="8e3aa-167">Examples</span></span>

* <span data-ttu-id="8e3aa-168">**적용됨**: Alt+Ctrl+S를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-168">**This**: Select Alt+Ctrl+S.</span></span>
* <span data-ttu-id="8e3aa-169">**적용되지 않음**: **Alt+Ctrl+S**를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-169">**Not this**: Press **ALT+CTRL+S**.</span></span>
* <span data-ttu-id="8e3aa-170">**적용되지 않음**: `ALT+CTRL+S`를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-170">**Not this**: Hit `ALT+CTRL+S`.</span></span>

<span data-ttu-id="8e3aa-171">자세한 내용은 [UI 조작 설명](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-171">For more information, see [Describing interactions with UI](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472).</span></span>

## <a name="exceptions"></a><span data-ttu-id="8e3aa-172">예외</span><span class="sxs-lookup"><span data-stu-id="8e3aa-172">Exceptions</span></span>

<span data-ttu-id="8e3aa-173">스타일 지침은 엄격한 규칙이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-173">Style guidelines aren't rigid rules.</span></span> <span data-ttu-id="8e3aa-174">지침을 따르면 가독성이 손상되는 컨텍스트에서는 다른 방식으로 작업을 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-174">In contexts where they harm readability, do something different.</span></span> <span data-ttu-id="8e3aa-175">예를 들어 대부분 코드 요소로 채워진 HTML 테이블에는 어디서나 코드 스타일이 아주 많이 적용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-175">For example, an HTML table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="8e3aa-176">해당 컨텍스트에서는 굵게 스타일 지정을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-176">You might choose bold styling in that context.</span></span>

<span data-ttu-id="8e3aa-177">일반적으로 코드가 호출되는 다른 텍스트 스타일을 선택하는 경우 문서의 지역화된 버전으로 텍스트를 번역할 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-177">If you choose an alternate text style where code is normally called for, make sure it's okay for the text to be translated in localized versions of the article.</span></span> <span data-ttu-id="8e3aa-178">코드는 번역을 자동으로 방지하는 유일한 스타일입니다.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-178">Code is the only style that automatically prevents translation.</span></span> <span data-ttu-id="8e3aa-179">코드 스타일을 사용하지 않고도 지역화를 방지하려는 시나리오의 경우 [지역화되지 않은 문자열](markdown-reference.md#non-localized-strings)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e3aa-179">For scenarios where you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>
