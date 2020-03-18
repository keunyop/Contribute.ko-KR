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
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336481"
---
# <a name="how-to-include-code-in-docs"></a><span data-ttu-id="94192-103">문서에 코드를 포함하는 방법</span><span class="sxs-lookup"><span data-stu-id="94192-103">How to include code in docs</span></span>

<span data-ttu-id="94192-104">docs.microsoft.com에 게시되는 문서에 코드를 포함하는 다음 몇 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-104">There are several ways to include code in an article published on docs.microsoft.com:</span></span>

* <span data-ttu-id="94192-105">한 줄에 개별 요소(단어) 포함</span><span class="sxs-lookup"><span data-stu-id="94192-105">Individual elements (words) within a line.</span></span>

  <span data-ttu-id="94192-106">다음은 `code` 스타일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-106">Here's an example of `code` style.</span></span>

  <span data-ttu-id="94192-107">텍스트에서 근접한 코드 블록의 명명된 매개 변수 및 변수를 참조하는 경우 코드 서식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-107">Use code format when referring to named parameters and variables in a nearby code block in your text.</span></span> <span data-ttu-id="94192-108">속성, 메서드, 클래스 및 언어 키워드에도 코드 서식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-108">Code format may also be used for properties, methods, classes, and language keywords.</span></span> <span data-ttu-id="94192-109">자세한 내용은 이 문서의 뒷부분에서 [코드 요소](#code-elements)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-109">For more information, see [Code elements](#code-elements) later in this article..</span></span>

* <span data-ttu-id="94192-110">문서 Markdown 파일에 코드 블록 포함</span><span class="sxs-lookup"><span data-stu-id="94192-110">Code blocks in the article Markdown file.</span></span>

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  <span data-ttu-id="94192-111">코드 파일을 참조하여 코드를 표시하는 것이 비실용적인 경우 인라인 코드 블록을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-111">Use inline code blocks when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="94192-112">자세한 내용은 이 문서의 뒷부분에서 [코드 블록](#inline-code-blocks)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-112">For more information, see [Code blocks](#inline-code-blocks) later in this article.</span></span>

* <span data-ttu-id="94192-113">로컬 리포지토리의 코드 파일을 참조하여 코드 블록 포함</span><span class="sxs-lookup"><span data-stu-id="94192-113">Code blocks by reference to a code file in the local repository.</span></span>

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  <span data-ttu-id="94192-114">자세한 내용은 이 문서의 뒷부분에서 [리포지토리 내부 코드 조각 참조](#in-repo-snippet-references)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-114">For more information, see [In-repo snippet references](#in-repo-snippet-references) later in this article.</span></span>

* <span data-ttu-id="94192-115">다른 리포지토리의 코드 파일을 참조하여 코드 블록 포함</span><span class="sxs-lookup"><span data-stu-id="94192-115">Code blocks by reference to a code file in another repository.</span></span>

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  <span data-ttu-id="94192-116">자세한 내용은 이 문서의 뒷부분에서 [리포지토리 외부 코드 조각 참조](#out-of-repo-snippet-references)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-116">For more information, see [Out-of-repo snippet references](#out-of-repo-snippet-references) later in this article.</span></span>
  
* <span data-ttu-id="94192-117">사용자가 브라우저에서 코드를 실행할 수 있는 코드 블록 포함</span><span class="sxs-lookup"><span data-stu-id="94192-117">Code blocks that let the user execute code in the browser.</span></span>

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  <span data-ttu-id="94192-118">자세한 내용은 이 문서의 뒷부분에서 [대화형 코드 조각](#interactive-code-snippets)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-118">For more information, see [Interactive code snippets](#interactive-code-snippets) later in this article.</span></span>

<span data-ttu-id="94192-119">이 문서는 이러한 각 코드 포함 방법에 대한 Markdown 설명은 물론, [모든 코드 블록에 대한 몇 가지 일반적인 지침](#code-blocks)도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-119">Besides explaining the Markdown for each of these ways to include code, the article provides some [general guidance for all code blocks](#code-blocks).</span></span>

## <a name="code-elements"></a><span data-ttu-id="94192-120">코드 요소</span><span class="sxs-lookup"><span data-stu-id="94192-120">Code elements</span></span>

<span data-ttu-id="94192-121">“코드 요소”는 프로그래밍 언어 키워드, 클래스 이름, 속성 이름 등입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-121">A "code element" is a programming language keyword, class name, property name, and so forth.</span></span> <span data-ttu-id="94192-122">코드로 간주되는 요소가 항상 명확한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="94192-122">It's not always obvious what qualifies as code.</span></span> <span data-ttu-id="94192-123">예를 들어 NuGet 패키지 이름은 코드로 처리되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-123">For example, NuGet package names should be treated as code.</span></span> <span data-ttu-id="94192-124">확실하지 않은 경우 [텍스트 서식 지정 지침](text-formatting-guidelines.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-124">When in doubt, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>

### <a name="inline-code-style"></a><span data-ttu-id="94192-125">인라인 코드 스타일</span><span class="sxs-lookup"><span data-stu-id="94192-125">Inline code style</span></span>

<span data-ttu-id="94192-126">문서 텍스트에 코드 요소를 포함하려면 backtick(\`)으로 둘러싸서 코드 스타일을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94192-126">To include a code element in article text, surround it with backticks (\`) to indicate code style.</span></span>
<span data-ttu-id="94192-127">인라인 코드 스타일에서는 세 개의 억음 악센트 기호 서식을 사용하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-127">Inline code style shouldn't use the triple-backtick format.</span></span>

|<span data-ttu-id="94192-128">Markdown</span><span class="sxs-lookup"><span data-stu-id="94192-128">Markdown</span></span> |<span data-ttu-id="94192-129">렌더링됨</span><span class="sxs-lookup"><span data-stu-id="94192-129">Rendered</span></span> |
|---------|---------|
|<span data-ttu-id="94192-130">기본적으로 Entity Framework에서 \`Id\` 또는 \`ClassnameID\`라는 속성을 기본 키로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-130">By default, the Entity Framework interprets a property that's named \`Id\` or \`ClassnameID\` as the primary key.</span></span>|<span data-ttu-id="94192-131">기본적으로 Entity Framework에서 `Id` 또는 `ClassnameID`라는 속성을 기본 키로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-131">By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>|

<span data-ttu-id="94192-132">문서를 지역화(다른 언어로 번역)할 때 코드 스타일이 지정된 텍스트는 번역되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-132">When an article is localized (translated into other languages), text styled as code is left untranslated.</span></span> <span data-ttu-id="94192-133">코드 스타일을 사용하지 않으면 지역화되지 않도록 하려는 경우 [지역화되지 않은 문자열](markdown-reference.md#non-localized-strings)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-133">If you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>

### <a name="bold-style"></a><span data-ttu-id="94192-134">굵게 스타일</span><span class="sxs-lookup"><span data-stu-id="94192-134">Bold style</span></span>

<span data-ttu-id="94192-135">일부 이전 스타일에서는 인라인 코드에 굵게가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-135">Some older style guides specify bold for inline code.</span></span> <span data-ttu-id="94192-136">굵게는 코드 스타일이 너무 두드러져서 가독성이 저하되는 경우에 사용할 수 있는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-136">Bold is an option when code style is so obtrusive as to compromise readability.</span></span> <span data-ttu-id="94192-137">예를 들어 대부분 코드 요소로 채워진 Markdown 테이블에서는 코드 스타일이 과도하게 적용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-137">For example, a Markdown table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="94192-138">굵게 스타일을 사용하도록 선택하는 경우 [지역화되지 않은 문자열 구문](markdown-reference.md#non-localized-strings)을 사용하여 코드가 지역화되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-138">If you choose to use bold style, use [non-localized strings syntax](markdown-reference.md#non-localized-strings) to make sure that code is not localized.</span></span>

### <a name="links"></a><span data-ttu-id="94192-139">링크</span><span class="sxs-lookup"><span data-stu-id="94192-139">Links</span></span>

<span data-ttu-id="94192-140">일부 컨텍스트에서는 코드 서식보다 참조 설명서 링크가 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-140">A link to reference documentation may be more helpful than code format in some contexts.</span></span> <span data-ttu-id="94192-141">링크를 사용하는 경우 링크 텍스트에 코드 서식을 적용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="94192-141">If you use a link, don't apply code format to the link text.</span></span> <span data-ttu-id="94192-142">링크에 코드 스타일을 지정하면 텍스트가 링크인지 구분하기 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-142">Styling a link as code can obscure the fact that the text is a link.</span></span>

<span data-ttu-id="94192-143">링크를 사용하고 나중에 동일한 컨텍스트에서 동일한 요소를 참조하는 경우 후속 인스턴스는 링크가 아닌 코드 서식으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94192-143">If you use a link and refer to the same element later in the same context, make the subsequent instances code format rather than links.</span></span>

### <a name="placeholders"></a><span data-ttu-id="94192-144">자리 표시자</span><span class="sxs-lookup"><span data-stu-id="94192-144">Placeholders</span></span>

<span data-ttu-id="94192-145">사용자가 표시된 코드 섹션을 고유한 값으로 바꾸도록 하려면 꺾쇠 괄호 또는 중괄호로 표시된 자리 표시자 텍스트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-145">If you want the user to replace a section of displayed code with their own values, use placeholder text marked off by angle brackets or curly braces.</span></span> <span data-ttu-id="94192-146">`az group delete -n <ResourceGroupName>`를 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-146">For example: `az group delete -n <ResourceGroupName>`.</span></span> <span data-ttu-id="94192-147">실제 값을 대체하는 경우 꺾쇠 괄호 또는 중괄호가 제거되어야 함을 설명하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-147">Explain that the brackets or braces must be removed when substituting real values.</span></span>

## <a name="code-blocks"></a><span data-ttu-id="94192-148">코드 블록</span><span class="sxs-lookup"><span data-stu-id="94192-148">Code blocks</span></span>

<span data-ttu-id="94192-149">문서에 코드를 포함하는 구문은 코드가 있는 위치에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="94192-149">The syntax for including code in a doc depends on where the code is located:</span></span>

* [<span data-ttu-id="94192-150">문서 Markdown 파일에 있는 경우</span><span class="sxs-lookup"><span data-stu-id="94192-150">In the article Markdown file</span></span>](#inline-code-blocks)
* [<span data-ttu-id="94192-151">동일한 리포지토리의 코드 파일에 있는 경우</span><span class="sxs-lookup"><span data-stu-id="94192-151">In a code file in the same repository</span></span>](#in-repo-snippet-references)
* [<span data-ttu-id="94192-152">다른 리포지토리의 코드 파일에 있는 경우</span><span class="sxs-lookup"><span data-stu-id="94192-152">In a code file in a different repository</span></span>](#out-of-repo-snippet-references)

<span data-ttu-id="94192-153">다음은 세 가지 유형의 코드 블록에 모두 적용되는 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-153">Following are guidelines that apply to all three types of code blocks:</span></span>

* [<span data-ttu-id="94192-154">코드 유효성 검사 자동화</span><span class="sxs-lookup"><span data-stu-id="94192-154">Automate code validation.</span></span>](#code-validation)
* [<span data-ttu-id="94192-155">주요 코드 줄 강조 표시</span><span class="sxs-lookup"><span data-stu-id="94192-155">Highlight key lines of code.</span></span>](#highlighting)
* [<span data-ttu-id="94192-156">가로 스크롤 막대 사용 금지</span><span class="sxs-lookup"><span data-stu-id="94192-156">Avoid horizontal scroll bars.</span></span>](#horizontal-scroll-bars)

### <a name="screenshots"></a><span data-ttu-id="94192-157">스크린샷</span><span class="sxs-lookup"><span data-stu-id="94192-157">Screenshots</span></span>

<span data-ttu-id="94192-158">이전 섹션에 나온 방법은 모두 사용 가능한 코드 블록을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-158">All of the methods listed in the preceding section result in usable code blocks:</span></span>

* <span data-ttu-id="94192-159">복사하여 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-159">You can copy and paste from them.</span></span>
* <span data-ttu-id="94192-160">검색 엔진에서 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-160">They're indexed by search engines.</span></span>
* <span data-ttu-id="94192-161">화면 읽기 프로그램에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-161">They're accessible to screen readers.</span></span>

<span data-ttu-id="94192-162">이는 문서에 코드를 포함하는 방법으로 IDE 스크린샷이 권장되지 않는 이유 중 일부분에 불과합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-162">These are just a few of the reasons why IDE screenshots aren't recommended as a method of including code in an article.</span></span> <span data-ttu-id="94192-163">IDE 스크린샷은 IntelliSense와 같이 IDE 자체에 대한 어떤 정보를 표시하는 경우에만 코드용으로 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-163">Use IDE screenshots for code only if you're showing something about the IDE itself, like IntelliSense.</span></span> <span data-ttu-id="94192-164">색 지정 및 강조 표시를 보여 주는 데는 스크린샷을 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="94192-164">Don't use screenshots just to show colorization and highlighting.</span></span>

### <a name="code-validation"></a><span data-ttu-id="94192-165">코드 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="94192-165">Code validation</span></span>

<span data-ttu-id="94192-166">일부 리포지토리에는 모든 샘플 코드를 자동으로 컴파일하여 오류를 확인하는 프로세스가 구현되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-166">Some repositories have implemented processes that automatically compile all sample code to check for errors.</span></span> <span data-ttu-id="94192-167">.NET 리포지토리에서도 이렇게 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-167">The .NET repository does this.</span></span> <span data-ttu-id="94192-168">자세한 내용은 .NET 리포지토리의 [기여](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-168">For more information, see [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) in the .NET repository.</span></span>

<span data-ttu-id="94192-169">다른 리포지토리의 코드 블록을 포함하는 경우 코드 유지 관리 전략에 따라 소유자와 협력하여 코드에서 사용하는 라이브러리의 새 버전이 제공되어도 포함된 코드가 나뉘거나 최신 상태를 유지하지 못하는 일이 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-169">If you are including code blocks from another repository, work with the owners on a maintenance strategy for the code so that your included code does not break or go out of date as new versions of the libraries the code uses are shipped.</span></span>

### <a name="highlighting"></a><span data-ttu-id="94192-170">강조 표시</span><span class="sxs-lookup"><span data-stu-id="94192-170">Highlighting</span></span>

<span data-ttu-id="94192-171">일반적으로 코드 조각은 컨텍스트를 제공하는 데 필요한 것보다 많은 코드를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-171">Snippets typically include more code than necessary in order to provide context.</span></span> <span data-ttu-id="94192-172">이 예제와 같이 코드 조각에서 중점을 두는 주요 줄을 강조 표시하면 가독성에 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-172">It helps readability when you highlight the key lines that you're focusing on in the snippet, as in this example:</span></span>

![강조 표시된 코드를 보여주는 예제](media/code-in-docs/highlighted-code.png)

<span data-ttu-id="94192-174">문서 Markdown 파일에 포함할 때는 코드를 강조 표시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-174">You can't highlight code when you include it in the article Markdown file.</span></span> <span data-ttu-id="94192-175">코드 파일을 참조하여 포함된 코드 조각에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-175">It works only for code snippets included by reference to a code file.</span></span>

### <a name="horizontal-scroll-bars"></a><span data-ttu-id="94192-176">가로 스크롤 막대</span><span class="sxs-lookup"><span data-stu-id="94192-176">Horizontal scroll bars</span></span>

<span data-ttu-id="94192-177">긴 줄을 나눠서 가로 스크롤 막대가 표시되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-177">Break up long lines to avoid horizontal scroll bars.</span></span> <span data-ttu-id="94192-178">코드 블록에 스크롤 막대가 있으면 코드를 읽기 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-178">Scroll bars on code blocks make code hard to read.</span></span> <span data-ttu-id="94192-179">특히 스크롤 막대와 읽으려는 줄을 동시에 볼 수 없는 긴 코드 블록에서 문제가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-179">They're especially problematic on longer code blocks, where it may be impossible to see the scroll bar and the line you want to read at the same time.</span></span>

<span data-ttu-id="94192-180">코드 블록에서 가로 스크롤 막대를 최소화하는 좋은 방법은 85자보다 긴 코드 줄을 나누는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-180">A good practice for minimizing horizontal scroll bars on code blocks is to break up code lines longer than 85 characters.</span></span> <span data-ttu-id="94192-181">하지만 스크롤 막대의 유무가 가독성의 유일한 기준은 아니라는 점에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-181">But keep in mind that the presence or absence of a scroll bar isn't the only criterion of readability.</span></span> <span data-ttu-id="94192-182">줄을 85자 미만으로 나누면 가독성이나 복사-붙여넣기 편의성이 손상되는 경우 얼마든지 줄을 85자 이상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-182">If breaking a line before 85 hurts readability or copy-paste convenience, feel free to go over 85.</span></span>

## <a name="inline-code-blocks"></a><span data-ttu-id="94192-183">인라인 코드 블록</span><span class="sxs-lookup"><span data-stu-id="94192-183">Inline code blocks</span></span>

<span data-ttu-id="94192-184">코드 파일을 참조하여 코드를 표시하는 것이 비실용적인 경우에만 인라인 코드 블록을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-184">Use inline code blocks only when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="94192-185">인라인 코드는 일반적으로 전체 프로젝트의 일부인 코드 파일보다 테스트 및 최신 상태 유지가 더 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-185">Inline code is generally more difficult to test and keep up to date compared to a code file that is part of a complete project.</span></span>  <span data-ttu-id="94192-186">인라인 코드에는 개발자가 코드를 이해하고 사용하는 데 도움이 되는 컨텍스트가 생략될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-186">And inline code may omit context that could help the developer to understand and use the code.</span></span> <span data-ttu-id="94192-187">이러한 고려 사항은 주로 프로그래밍 언어에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-187">These considerations apply mainly to programming languages.</span></span> <span data-ttu-id="94192-188">인라인 코드 블록은 출력 및 입력(예: JSON), 쿼리 언어(예: SQL), 스크립팅 언어(예: PowerShell)에도 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-188">Inline code blocks can also be used for outputs and inputs (such as JSON), query languages (such as SQL), and scripting languages (such as PowerShell).</span></span>
  
<span data-ttu-id="94192-189">문서 파일에서 텍스트 섹션을 나타내는 두 가지 방법은 backtick 3개(\`\`\`)로 ‘펜싱’하거나 들여쓰기를 사용한 코드 블록입니다. </span><span class="sxs-lookup"><span data-stu-id="94192-189">There are two ways to indicate a section of text in an article file is a code block: by *fencing* it in triple-backticks (\`\`\`) or by indenting it.</span></span> <span data-ttu-id="94192-190">언어를 지정할 수 있는 펜싱을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-190">Fencing is preferred because it lets you specify the language.</span></span> <span data-ttu-id="94192-191">들여쓰기는 너무 간단하여 실수하기가 쉽고 다른 작성자가 문서를 편집해야 할 때 원래 작성자의 의도를 이해하기 어려울 수 있으므로 사용하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-191">Avoid using indentation because it's too easy to get wrong and it may be hard for another writer to understand your intent when they need to edit your article.</span></span>

<span data-ttu-id="94192-192">언어 표시기는 다음 예제와 같이 여는 backtick 3개 바로 뒤에 옵니다.</span><span class="sxs-lookup"><span data-stu-id="94192-192">Language indicators are placed immediately after the opening triple-backticks, as in the following example:</span></span>

<span data-ttu-id="94192-193">Markdown:</span><span class="sxs-lookup"><span data-stu-id="94192-193">Markdown:</span></span>

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

<span data-ttu-id="94192-194">렌더링됨:</span><span class="sxs-lookup"><span data-stu-id="94192-194">Rendered:</span></span>

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

<span data-ttu-id="94192-195">언어 표시기로 사용할 수 있는 값에 대한 자세한 내용은 [언어 이름 및 별칭](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-195">For information about the values you can use as language indicators, see [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span></span>

<span data-ttu-id="94192-196">세 개의 억음 악센트 기호(\`\`\`) 뒤에 지원되지 않는 언어 또는 환경 단어를 사용하는 경우 해당 단어가 렌더링된 페이지의 코드 섹션 제목 표시줄에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-196">If you use a language or environment word after the triple-backticks (\`\`\`) that isn't supported, that word appears in the code section title bar on the rendered page.</span></span> <span data-ttu-id="94192-197">가능한 한 언어 또는 환경 표시기를 인라인 코드 블록에 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-197">Whenever possible, use a language or environment indicator in your inline code blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="94192-198">Word 문서에서 코드를 복사하여 붙여넣는 경우 코드에 유효하지 않은 “둥근 따옴표”(예: `“` 및 `’`)가 없는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-198">If you copy and paste code from a Word document, make sure it has no "curly quotes," which aren't valid in code (for example, `“` and `’`).</span></span> <span data-ttu-id="94192-199">둥근 따옴표가 있으면 일반 따옴표(`'` 및 `"`)로 다시 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-199">If it does, change them back to normal quotes (`'` and `"`).</span></span> <span data-ttu-id="94192-200">또는 Docs Authoring Pack의 [둥근 따옴표 바꾸기 기능](docs-authoring/smart-quote-replacement.md)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-200">Alternatively, rely on the Docs Authoring Pack, [smart quotes replacement feature](docs-authoring/smart-quote-replacement.md).</span></span>

## <a name="in-repo-snippet-references"></a><span data-ttu-id="94192-201">리포지토리 내부 코드 조각 참조</span><span class="sxs-lookup"><span data-stu-id="94192-201">In-repo snippet references</span></span>

<span data-ttu-id="94192-202">프로그래밍 언어에 필요한 코드 조각을 문서에 포함하려면 코드 파일을 참조하는 방법을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-202">The preferred way to include code snippets for programming languages in docs is by reference to a code file.</span></span> <span data-ttu-id="94192-203">이 방법을 사용하면 코드 줄을 강조 표시할 수 있고 개발자가 GitHub에서 더 넓은 범위의 코드 조각 컨텍스트를 사용하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-203">This method gives you the ability to highlight lines of code and makes the wider context of the snippet available on GitHub for developers to use.</span></span> <span data-ttu-id="94192-204">수동으로 또는 Visual Studio Code에서 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 지원을 통해 세 개의 콜론 서식(:\:\:)을 사용하여 코드를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-204">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="94192-205">Visual Studio Code에서 <kbd>Alt + M</kbd> 또는 <kbd>Option + M</kbd>을 클릭하고 코드 조각을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-205">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="94192-206">코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-206">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="94192-207">로컬에서 검색하려면 전체 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-207">To search locally, select Full Search.</span></span>
3. <span data-ttu-id="94192-208">검색 용어를 입력하여 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-208">Enter a search term to find the file.</span></span> <span data-ttu-id="94192-209">파일을 찾으면 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-209">Once you've found the file, select the file.</span></span>
4. <span data-ttu-id="94192-210">다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-210">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="94192-211">옵션은 **ID**, **범위**, **없음**입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-211">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="94192-212">4단계에서 선택한 옵션에 따라 필요한 경우 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-212">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="94192-213">전체 코드 파일 표시:</span><span class="sxs-lookup"><span data-stu-id="94192-213">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="94192-214">줄 번호를 지정하여 코드 파일의 일부 표시:</span><span class="sxs-lookup"><span data-stu-id="94192-214">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="94192-215">코드 조각 이름을 지정하여 코드 파일의 일부 표시:</span><span class="sxs-lookup"><span data-stu-id="94192-215">Display part of a code file by specifying a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="94192-216">다음 섹션에서는 이러한 예제를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-216">The following sections explain these examples:</span></span>

* [<span data-ttu-id="94192-217">코드 파일의 상대 경로 사용</span><span class="sxs-lookup"><span data-stu-id="94192-217">Use a relative path to the code file</span></span>](#path-to-code-file)
* [<span data-ttu-id="94192-218">선택한 줄 번호만 포함</span><span class="sxs-lookup"><span data-stu-id="94192-218">Include only selected line numbers</span></span>](#selected-line-numbers)
* [<span data-ttu-id="94192-219">명명된 코드 조각 참조</span><span class="sxs-lookup"><span data-stu-id="94192-219">Refer to a named snippet</span></span>](#named-snippet)
* [<span data-ttu-id="94192-220">선택한 줄 강조 표시</span><span class="sxs-lookup"><span data-stu-id="94192-220">Highlight selected lines</span></span>](#highlighting-selected-lines)

<span data-ttu-id="94192-221">자세한 내용은 이 문서의 뒷부분에서 [코드 조각 구문 참조](#snippet-syntax-reference)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-221">For more information, see [Snippet syntax reference](#snippet-syntax-reference) later in this article.</span></span>

### <a name="path-to-code-file"></a><span data-ttu-id="94192-222">코드 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="94192-222">Path to code file</span></span>

<span data-ttu-id="94192-223">예제:</span><span class="sxs-lookup"><span data-stu-id="94192-223">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="94192-224">이 예제는 ASP.NET 문서 리포지토리, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 문서 파일에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-224">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="94192-225">코드 파일은 동일한 리포지토리에 있는 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs)의 상대 경로로 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-225">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

### <a name="selected-line-numbers"></a><span data-ttu-id="94192-226">선택한 줄 번호</span><span class="sxs-lookup"><span data-stu-id="94192-226">Selected line numbers</span></span>

<span data-ttu-id="94192-227">예제:</span><span class="sxs-lookup"><span data-stu-id="94192-227">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="94192-228">위 예제에서는 *StudentController.cs* 코드 파일의 줄 2~24와 26만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-228">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="94192-229">다음 섹션에 설명된 대로 하드 코드된 줄 번호보다 명명된 코드 조각을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-229">Prefer named snippets over hard-coded line numbers, as explained in the next section.</span></span>

### <a name="named-snippet"></a><span data-ttu-id="94192-230">명명된 코드 조각</span><span class="sxs-lookup"><span data-stu-id="94192-230">Named snippet</span></span>

<span data-ttu-id="94192-231">예제:</span><span class="sxs-lookup"><span data-stu-id="94192-231">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="94192-232">이름에는 문자와 밑줄만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-232">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="94192-233">이 예제는 코드 파일의 `snippet_Create` 섹션을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-233">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="94192-234">이 예제의 코드 파일에는 C# 코드의 주석에 코드 조각 태그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-234">The code file for this example has snippet tags in comments in the C# code:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="94192-235">가능한 한, 줄 번호를 지정하지 말고 명명된 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-235">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="94192-236">코드 파일은 필연적으로 변경되고, 이 경우 줄 번호도 변경되기 때문에 줄 번호 참조는 불안정합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-236">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="94192-237">항상 이러한 변경에 대한 알림을 받는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="94192-237">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="94192-238">결국 문서에서 잘못된 줄이 나타나기 시작해도 무엇이 변경되었는지 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-238">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

### <a name="highlighting-selected-lines"></a><span data-ttu-id="94192-239">선택한 줄 강조 표시</span><span class="sxs-lookup"><span data-stu-id="94192-239">Highlighting selected lines</span></span>

<span data-ttu-id="94192-240">예제:</span><span class="sxs-lookup"><span data-stu-id="94192-240">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="94192-241">이 예제에서는 표시된 코드 조각의 처음부터 줄 2와 5를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-241">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="94192-242">강조 표시할 줄 번호가 코드 파일의 처음부터 계산되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-242">Line numbers to highlight don't count from the start of the code file.</span></span> <span data-ttu-id="94192-243">즉, 코드 파일의 줄 3과 6이 강조 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-243">In other words, lines 3 and 6 of the code file are highlighted.</span></span>

## <a name="out-of-repo-snippet-references"></a><span data-ttu-id="94192-244">리포지토리 외부 코드 조각 참조</span><span class="sxs-lookup"><span data-stu-id="94192-244">Out-of-repo snippet references</span></span>

<span data-ttu-id="94192-245">참조하려는 코드 파일이 다른 리포지토리에 있으면 코드 리포지토리를 ‘종속 리포지토리’로 설정합니다. </span><span class="sxs-lookup"><span data-stu-id="94192-245">If the code file you want to reference is in a different repository, set up the code repository as a *dependent repository*.</span></span> <span data-ttu-id="94192-246">이 경우 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-246">When you do that, you specify a name for it.</span></span> <span data-ttu-id="94192-247">이 이름은 코드 참조를 위해 폴더 이름과 같이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-247">That name then acts like a folder name for purposes of code references.</span></span>

<span data-ttu-id="94192-248">예를 들어 문서 리포지토리는 *Azure/azure-docs*이고, 코드 리포지토리는 *Azure/azure-functions-durable-extension*입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-248">For example, the docs repository is *Azure/azure-docs*, and the code repository is *Azure/azure-functions-durable-extension*.</span></span>

<span data-ttu-id="94192-249">*azure-docs*의 루트 폴더에 있는 *.openpublishing.publish.config.json*에 다음 섹션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-249">In the root folder of *azure-docs*, add the following section in *.openpublishing.publish.config.json*:</span></span>

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

<span data-ttu-id="94192-250">이제 *azure-docs*에 있는 폴더처럼 *sample-durable-functions*를 참조할 때 실제로는 *azure-functions-durable-extension* 리포지토리에 있는 루트 폴더를 참조하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-250">Now when you refer to *samples-durable-functions* as if it were a folder in *azure-docs*, you're actually referring to the root folder in the *azure-functions-durable-extension* repository.</span></span>

<span data-ttu-id="94192-251">수동으로 또는 Visual Studio Code에서 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 지원을 통해 세 개의 콜론 서식(:\:\:)을 사용하여 코드를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-251">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="94192-252">Visual Studio Code에서 <kbd>Alt + M</kbd> 또는 <kbd>Option + M</kbd>을 클릭하고 코드 조각을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-252">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="94192-253">코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-253">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="94192-254">리포지토리에서 검색하려면 리포지토리 간 참조를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-254">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="94192-255">*.openpublishing.publish.config.json*에 있는 리포지토리에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-255">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="94192-256">리포지토리를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-256">Select a repository.</span></span>
4. <span data-ttu-id="94192-257">검색 용어를 입력하여 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-257">Enter a search term to find the file.</span></span> <span data-ttu-id="94192-258">파일을 찾으면 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-258">Once you've found the file, select the file.</span></span>
5. <span data-ttu-id="94192-259">다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-259">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="94192-260">옵션은 **ID**, **범위**, **없음**입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-260">The options are: **ID**, **Range** and **None**.</span></span>
6. <span data-ttu-id="94192-261">5단계에서 선택한 옵션에 따라 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-261">Based on your selection from Step 5, provide a value.</span></span>

<span data-ttu-id="94192-262">코드 조각 참조는 다음과 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-262">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

<span data-ttu-id="94192-263">*azure-functions-durable-extension* 리포지토리에서 해당 코드 파일은 *samples/csx/shared* 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-263">In the *azure-functions-durable-extension* repository, that code file is in the *samples/csx/shared* folder.</span></span> <span data-ttu-id="94192-264">[앞에서](#highlighting-selected-lines) 설명했듯이 강조 표시할 줄 번호는 파일의 시작이 아니라 코드 조각의 시작 부분을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-264">As noted [earlier](#highlighting-selected-lines), line numbers for highlighting are relative to the start of the snippet rather than the start of the file.</span></span>

> [!NOTE]
> <span data-ttu-id="94192-265">종속 리포지토리에 할당되는 이름은 기본 리포지토리 루트를 기준으로 하지만 물결표(~)는 문서 집합 루트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94192-265">The name you assign to the dependent repository is relative to the root of the main repository, but the tilde (~) refers to the root of the doc set.</span></span> <span data-ttu-id="94192-266">문서 집합 루트는 *.openpublishing.publish.config.json*의 `build_source_folder`에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-266">The doc set root is determined by `build_source_folder` in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="94192-267">`build_source_folder`가 리포 루트(`.`)를 나타내므로 앞의 예제에서 코드 조각의 경로는 azure-docs 리포지토리에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-267">The path to the snippet in the preceding example works in the azure-docs repo because `build_source_folder` refers to the repo root (`.`).</span></span> <span data-ttu-id="94192-268">`build_source_folder`가 `articles`면 경로는 `~/samples-durable-functions`가 아니라 `~/../samples-durable-functions`로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-268">If `build_source_folder` were `articles`, the path would start with `~/../samples-durable-functions` instead of `~/samples-durable-functions`.</span></span>

## <a name="interactive-code-snippets"></a><span data-ttu-id="94192-269">대화형 코드 조각</span><span class="sxs-lookup"><span data-stu-id="94192-269">Interactive code snippets</span></span>

### <a name="inline-interactive-code-blocks"></a><span data-ttu-id="94192-270">인라인 대화형 코드 블록</span><span class="sxs-lookup"><span data-stu-id="94192-270">Inline interactive code blocks</span></span>

<span data-ttu-id="94192-271">다음 언어의 경우 브라우저 창에서 코드 조각을 실행 가능하게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-271">For the following languages, code snippets can be made executable in the browser window:</span></span>

* <span data-ttu-id="94192-272">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="94192-272">Azure Cloud Shell</span></span>
* <span data-ttu-id="94192-273">Azure PowerShell Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="94192-273">Azure PowerShell Cloud Shell</span></span>
* <span data-ttu-id="94192-274">C# REPL</span><span class="sxs-lookup"><span data-stu-id="94192-274">C# REPL</span></span>

<span data-ttu-id="94192-275">대화형 모드를 사용하도록 설정한 경우 렌더링된 코드 상자에 **시도** 또는 **실행** 단추가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-275">When interactive mode is enabled, the rendered code boxes have a **Try It** or **Run** button.</span></span> <span data-ttu-id="94192-276">예:</span><span class="sxs-lookup"><span data-stu-id="94192-276">For example:</span></span>

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

<span data-ttu-id="94192-277">은(는) 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-277">renders as follows:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

<span data-ttu-id="94192-278">특정 코드 블록에 대해 이 기능을 켜려면 특수 언어 식별자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-278">To turn on this feature for a particular code block, use a special language identifier.</span></span> <span data-ttu-id="94192-279">사용 가능한 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-279">The available options are:</span></span>

* <span data-ttu-id="94192-280">`azurepowershell-interactive` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-280">`azurepowershell-interactive` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="94192-281">`azurecli-interactive` - Azure Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-281">`azurecli-interactive` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="94192-282">`csharp-interactive` - C# REPL을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-282">`csharp-interactive` - Enables the C# REPL</span></span>

<span data-ttu-id="94192-283">Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-283">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

### <a name="code-snippets-included-by-reference"></a><span data-ttu-id="94192-284">참조하여 포함된 코드 조각</span><span class="sxs-lookup"><span data-stu-id="94192-284">Code snippets included by reference</span></span>

<span data-ttu-id="94192-285">참조를 통해 포함된 코드 조각에 대해 대화형 모드를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-285">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="94192-286">예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-286">Here are examples:</span></span>

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="94192-287">특정 코드 블록을 대상으로 이 기능을 켜려면 `interactive` 특성을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-287">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="94192-288">사용 가능한 특성 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-288">The available attribute values are:</span></span>

* <span data-ttu-id="94192-289">`cloudshell-powershell` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-289">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="94192-290">`cloudshell-bash` - Azure Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-290">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="94192-291">`try-dotnet` - Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-291">`try-dotnet` - Enables Try .NET</span></span>
* <span data-ttu-id="94192-292">`try-dotnet-class` - 클래스 스캐폴딩으로 Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-292">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
* <span data-ttu-id="94192-293">`try-dotnet-method` - 메서드 스캐폴딩으로 Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="94192-293">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="94192-294">Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-294">For the Azure Cloud Shell and PowerShell Cloud Shell, users can only run commands against their own Azure account.</span></span>

## <a name="snippet-syntax-reference"></a><span data-ttu-id="94192-295">코드 조각 구문 참조</span><span class="sxs-lookup"><span data-stu-id="94192-295">Snippet syntax reference</span></span>

<span data-ttu-id="94192-296">구문:</span><span class="sxs-lookup"><span data-stu-id="94192-296">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="94192-297">이 구문은 블록 Markdown 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-297">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="94192-298">자체 줄에 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-298">It must be used on its own line.</span></span>

* <span data-ttu-id="94192-299">`<language>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="94192-299">`<language>` (*optional*)</span></span>
  * <span data-ttu-id="94192-300">코드 조각의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-300">Language of the code snippet.</span></span> <span data-ttu-id="94192-301">자세한 내용은 본 문서의 아래에 있는 [지원되는 언어](#supported-languages) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-301">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

* <span data-ttu-id="94192-302">`<path>`(*필수*)</span><span class="sxs-lookup"><span data-stu-id="94192-302">`<path>` (*mandatory*)</span></span>
  * <span data-ttu-id="94192-303">참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-303">Relative path in the file system that indicates the code snippet file to reference.</span></span>

* <span data-ttu-id="94192-304">`<attribute>` 및 `<attribute-value>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="94192-304">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  * <span data-ttu-id="94192-305">파일에서 코드를 검색하는 방법과 표시하는 방법을 지정하는 데 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="94192-305">Used together to specify how the code should be retrieved from the file and how it should be displayed:</span></span>
    * <span data-ttu-id="94192-306">`range`: `1,3-5` 줄 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-306">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="94192-307">이 예제는 1, 3, 4 및 5 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-307">This example includes lines 1, 3, 4, and 5.</span></span>
    * <span data-ttu-id="94192-308">`id`: `snippet_Create` 코드 파일에서 삽입해야 하는 코드 조각의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-308">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="94192-309">이 값은 범위와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-309">This value cannot co-exist with range.</span></span>
    * <span data-ttu-id="94192-310">`highlight`: `2-4,6` 생성된 코드 조각에서 강조 표시해야 하는 범위 및/또는 줄 수입니다.</span><span class="sxs-lookup"><span data-stu-id="94192-310">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="94192-311">번호 매기기는 파일이 아니라 표시된 줄(범위 또는 ID로 지정됨)을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-311">The numbering is relative to the lines displayed (as specified by range or id), not the file.</span></span>
    * <span data-ttu-id="94192-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` 문자열 값은 어떤 종류의 대화형 작업이 사용하도록 설정되는지를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>
    * <span data-ttu-id="94192-313">코드 조각 소스의 태그 이름 표현에 대한 자세한 내용을 언어별로 보려면 [DocFX 지침](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-313">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="94192-314">지원되는 언어</span><span class="sxs-lookup"><span data-stu-id="94192-314">Supported languages</span></span>

<span data-ttu-id="94192-315">[Docs Authoring Pack](how-to-write-docs-auth-pack.md)에는 코드 펜스 블록에 사용할 수 있는 언어 식별자에 대한 문 완성 및 유효성 검사를 제공하는 기능이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94192-315">The [Docs Authoring Pack](how-to-write-docs-auth-pack.md) includes a feature to provide statement completion and validation of the available language identifiers for code fence blocks.</span></span>

### <a name="fenced-code-blocks"></a><span data-ttu-id="94192-316">펜싱된 코드 블록</span><span class="sxs-lookup"><span data-stu-id="94192-316">Fenced code blocks</span></span>

| <span data-ttu-id="94192-317">Name</span><span class="sxs-lookup"><span data-stu-id="94192-317">Name</span></span>                           | <span data-ttu-id="94192-318">유효한 별칭</span><span class="sxs-lookup"><span data-stu-id="94192-318">Valid aliases</span></span>                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="94192-319">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="94192-319">.NET Core CLI</span></span>                  | `dotnetcli`                                                                    |
| <span data-ttu-id="94192-320">1C</span><span class="sxs-lookup"><span data-stu-id="94192-320">1C</span></span>                             | `1c`                                                                           |
| <span data-ttu-id="94192-321">ABNF</span><span class="sxs-lookup"><span data-stu-id="94192-321">ABNF</span></span>                           | `abnf`                                                                         |
| <span data-ttu-id="94192-322">Access logs</span><span class="sxs-lookup"><span data-stu-id="94192-322">Access logs</span></span>                    | `accesslog`                                                                    |
| <span data-ttu-id="94192-323">Ada</span><span class="sxs-lookup"><span data-stu-id="94192-323">Ada</span></span>                            | `ada`                                                                          |
| <span data-ttu-id="94192-324">ARM assembler</span><span class="sxs-lookup"><span data-stu-id="94192-324">ARM assembler</span></span>                  | <span data-ttu-id="94192-325">`armasm`, `arm`</span><span class="sxs-lookup"><span data-stu-id="94192-325">`armasm`, `arm`</span></span>                                                                |
| <span data-ttu-id="94192-326">AVR assembler</span><span class="sxs-lookup"><span data-stu-id="94192-326">AVR assembler</span></span>                  | `avrasm`                                                                       |
| <span data-ttu-id="94192-327">ActionScript</span><span class="sxs-lookup"><span data-stu-id="94192-327">ActionScript</span></span>                   | <span data-ttu-id="94192-328">`actionscript`, `as`</span><span class="sxs-lookup"><span data-stu-id="94192-328">`actionscript`, `as`</span></span>                                                           |
| <span data-ttu-id="94192-329">Alan</span><span class="sxs-lookup"><span data-stu-id="94192-329">Alan</span></span>                           | <span data-ttu-id="94192-330">`alan`, `i`</span><span class="sxs-lookup"><span data-stu-id="94192-330">`alan`, `i`</span></span>                                                                    |
| <span data-ttu-id="94192-331">AngelScript</span><span class="sxs-lookup"><span data-stu-id="94192-331">AngelScript</span></span>                    | <span data-ttu-id="94192-332">`angelscript`, `asc`</span><span class="sxs-lookup"><span data-stu-id="94192-332">`angelscript`, `asc`</span></span>                                                           |
| <span data-ttu-id="94192-333">ANTLR</span><span class="sxs-lookup"><span data-stu-id="94192-333">ANTLR</span></span>                          | `antlr`                                                                        |
| <span data-ttu-id="94192-334">Apache</span><span class="sxs-lookup"><span data-stu-id="94192-334">Apache</span></span>                         | <span data-ttu-id="94192-335">`apache`, `apacheconf`</span><span class="sxs-lookup"><span data-stu-id="94192-335">`apache`, `apacheconf`</span></span>                                                         |
| <span data-ttu-id="94192-336">AppleScript</span><span class="sxs-lookup"><span data-stu-id="94192-336">AppleScript</span></span>                    | <span data-ttu-id="94192-337">`applescript`, `osascript`</span><span class="sxs-lookup"><span data-stu-id="94192-337">`applescript`, `osascript`</span></span>                                                     |
| <span data-ttu-id="94192-338">Arcade</span><span class="sxs-lookup"><span data-stu-id="94192-338">Arcade</span></span>                         | `arcade`                                                                       |
| <span data-ttu-id="94192-339">AsciiDoc</span><span class="sxs-lookup"><span data-stu-id="94192-339">AsciiDoc</span></span>                       | <span data-ttu-id="94192-340">`asciidoc`, `adoc`</span><span class="sxs-lookup"><span data-stu-id="94192-340">`asciidoc`, `adoc`</span></span>                                                             |
| <span data-ttu-id="94192-341">AspectJ</span><span class="sxs-lookup"><span data-stu-id="94192-341">AspectJ</span></span>                        | `aspectj`                                                                      |
| <span data-ttu-id="94192-342">ASPX</span><span class="sxs-lookup"><span data-stu-id="94192-342">ASPX</span></span>                           | `aspx`                                                                         |
| <span data-ttu-id="94192-343">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="94192-343">ASP.NET (C#)</span></span>                   | `aspx-csharp`                                                                  |
| <span data-ttu-id="94192-344">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="94192-344">ASP.NET (VB)</span></span>                   | `aspx-vb`                                                                      |
| <span data-ttu-id="94192-345">AutoHotkey</span><span class="sxs-lookup"><span data-stu-id="94192-345">AutoHotkey</span></span>                     | `autohotkey`                                                                   |
| <span data-ttu-id="94192-346">AutoIt</span><span class="sxs-lookup"><span data-stu-id="94192-346">AutoIt</span></span>                         | `autoit`                                                                       |
| <span data-ttu-id="94192-347">Awk</span><span class="sxs-lookup"><span data-stu-id="94192-347">Awk</span></span>                            | <span data-ttu-id="94192-348">`awk`, `mawk`, `nawk`, `gawk`</span><span class="sxs-lookup"><span data-stu-id="94192-348">`awk`, `mawk`, `nawk`, `gawk`</span></span>                                                  |
| <span data-ttu-id="94192-349">Axapta</span><span class="sxs-lookup"><span data-stu-id="94192-349">Axapta</span></span>                         | `axapta`                                                                       |
| <span data-ttu-id="94192-350">AzCopy</span><span class="sxs-lookup"><span data-stu-id="94192-350">AzCopy</span></span>                         | `azcopy`                                                                       |
| <span data-ttu-id="94192-351">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="94192-351">Azure CLI</span></span>                      | `azurecli`                                                                     |
| <span data-ttu-id="94192-352">Azure CLI (Interactive)</span><span class="sxs-lookup"><span data-stu-id="94192-352">Azure CLI (Interactive)</span></span>        | `azurecli-interactive`                                                         |
| <span data-ttu-id="94192-353">Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="94192-353">Azure Powershell</span></span>               | `azurepowershell`                                                              |
| <span data-ttu-id="94192-354">Azure Powershell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="94192-354">Azure Powershell (Interactive)</span></span> | `azurepowershell-interactive`                                                  |
| <span data-ttu-id="94192-355">Bash</span><span class="sxs-lookup"><span data-stu-id="94192-355">Bash</span></span>                           | <span data-ttu-id="94192-356">`bash`, `sh`, `zsh`</span><span class="sxs-lookup"><span data-stu-id="94192-356">`bash`, `sh`, `zsh`</span></span>                                                            |
| <span data-ttu-id="94192-357">Basic</span><span class="sxs-lookup"><span data-stu-id="94192-357">Basic</span></span>                          | `basic`                                                                        |
| <span data-ttu-id="94192-358">BNF</span><span class="sxs-lookup"><span data-stu-id="94192-358">BNF</span></span>                            | `bnf`                                                                          |
| <span data-ttu-id="94192-359">C</span><span class="sxs-lookup"><span data-stu-id="94192-359">C</span></span>                              | `c`                                                                            |
| <span data-ttu-id="94192-360">C#</span><span class="sxs-lookup"><span data-stu-id="94192-360">C#</span></span>                             | <span data-ttu-id="94192-361">`csharp`, `cs`</span><span class="sxs-lookup"><span data-stu-id="94192-361">`csharp`, `cs`</span></span>                                                                 |
| <span data-ttu-id="94192-362">C# (Interactive)</span><span class="sxs-lookup"><span data-stu-id="94192-362">C# (Interactive)</span></span>               | `csharp-interactive`                                                           |
| <span data-ttu-id="94192-363">C++</span><span class="sxs-lookup"><span data-stu-id="94192-363">C++</span></span>                            | <span data-ttu-id="94192-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span><span class="sxs-lookup"><span data-stu-id="94192-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span></span>                                     |
| <span data-ttu-id="94192-365">C++/CX</span><span class="sxs-lookup"><span data-stu-id="94192-365">C++/CX</span></span>                         | `cppcx`                                                                        |
| <span data-ttu-id="94192-366">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="94192-366">C++/WinRT</span></span>                      | `cppwinrt`                                                                     |
| <span data-ttu-id="94192-367">C/AL</span><span class="sxs-lookup"><span data-stu-id="94192-367">C/AL</span></span>                           | `cal`                                                                          |
| <span data-ttu-id="94192-368">Cache Object Script</span><span class="sxs-lookup"><span data-stu-id="94192-368">Cache Object Script</span></span>            | <span data-ttu-id="94192-369">`cos`, `cls`</span><span class="sxs-lookup"><span data-stu-id="94192-369">`cos`, `cls`</span></span>                                                                   |
| <span data-ttu-id="94192-370">CMake</span><span class="sxs-lookup"><span data-stu-id="94192-370">CMake</span></span>                          | <span data-ttu-id="94192-371">`cmake`, `cmake.in`</span><span class="sxs-lookup"><span data-stu-id="94192-371">`cmake`, `cmake.in`</span></span>                                                            |
| <span data-ttu-id="94192-372">Coq</span><span class="sxs-lookup"><span data-stu-id="94192-372">Coq</span></span>                            | `coq`                                                                          |
| <span data-ttu-id="94192-373">CSP</span><span class="sxs-lookup"><span data-stu-id="94192-373">CSP</span></span>                            | `csp`                                                                          |
| <span data-ttu-id="94192-374">CSS</span><span class="sxs-lookup"><span data-stu-id="94192-374">CSS</span></span>                            | `css`                                                                          |
| <span data-ttu-id="94192-375">Cap’n Proto</span><span class="sxs-lookup"><span data-stu-id="94192-375">Cap'n Proto</span></span>                    | <span data-ttu-id="94192-376">`capnproto`, `capnp`</span><span class="sxs-lookup"><span data-stu-id="94192-376">`capnproto`, `capnp`</span></span>                                                           |
| <span data-ttu-id="94192-377">Clojure</span><span class="sxs-lookup"><span data-stu-id="94192-377">Clojure</span></span>                        | <span data-ttu-id="94192-378">`clojure`, `clj`</span><span class="sxs-lookup"><span data-stu-id="94192-378">`clojure`, `clj`</span></span>                                                               |
| <span data-ttu-id="94192-379">CoffeeScript</span><span class="sxs-lookup"><span data-stu-id="94192-379">CoffeeScript</span></span>                   | <span data-ttu-id="94192-380">`coffeescript`, `coffee`, `cson`, `iced`</span><span class="sxs-lookup"><span data-stu-id="94192-380">`coffeescript`, `coffee`, `cson`, `iced`</span></span>                                       |
| <span data-ttu-id="94192-381">Crmsh</span><span class="sxs-lookup"><span data-stu-id="94192-381">Crmsh</span></span>                          | <span data-ttu-id="94192-382">`crmsh`, `crm`, `pcmk`</span><span class="sxs-lookup"><span data-stu-id="94192-382">`crmsh`, `crm`, `pcmk`</span></span>                                                         |
| <span data-ttu-id="94192-383">Crystal</span><span class="sxs-lookup"><span data-stu-id="94192-383">Crystal</span></span>                        | <span data-ttu-id="94192-384">`crystal`, `cr`</span><span class="sxs-lookup"><span data-stu-id="94192-384">`crystal`, `cr`</span></span>                                                                |
| <span data-ttu-id="94192-385">Cypher (Neo4j)</span><span class="sxs-lookup"><span data-stu-id="94192-385">Cypher (Neo4j)</span></span>                 | `cypher`                                                                       |
| <span data-ttu-id="94192-386">D</span><span class="sxs-lookup"><span data-stu-id="94192-386">D</span></span>                              | `d`                                                                            |
| <span data-ttu-id="94192-387">DAX Power BI</span><span class="sxs-lookup"><span data-stu-id="94192-387">DAX Power BI</span></span>                   | `dax`                                                                          |
| <span data-ttu-id="94192-388">DNS Zone file</span><span class="sxs-lookup"><span data-stu-id="94192-388">DNS Zone file</span></span>                  | <span data-ttu-id="94192-389">`dns`, `zone`, `bind`</span><span class="sxs-lookup"><span data-stu-id="94192-389">`dns`, `zone`, `bind`</span></span>                                                          |
| <span data-ttu-id="94192-390">DOS</span><span class="sxs-lookup"><span data-stu-id="94192-390">DOS</span></span>                            | <span data-ttu-id="94192-391">`dos`, `bat`, `cmd`</span><span class="sxs-lookup"><span data-stu-id="94192-391">`dos`, `bat`, `cmd`</span></span>                                                            |
| <span data-ttu-id="94192-392">Dart</span><span class="sxs-lookup"><span data-stu-id="94192-392">Dart</span></span>                           | `dart`                                                                         |
| <span data-ttu-id="94192-393">Delphi</span><span class="sxs-lookup"><span data-stu-id="94192-393">Delphi</span></span>                         | <span data-ttu-id="94192-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span><span class="sxs-lookup"><span data-stu-id="94192-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span></span> |
| <span data-ttu-id="94192-395">Diff</span><span class="sxs-lookup"><span data-stu-id="94192-395">Diff</span></span>                           | <span data-ttu-id="94192-396">`diff`, `patch`</span><span class="sxs-lookup"><span data-stu-id="94192-396">`diff`, `patch`</span></span>                                                                |
| <span data-ttu-id="94192-397">Django</span><span class="sxs-lookup"><span data-stu-id="94192-397">Django</span></span>                         | <span data-ttu-id="94192-398">`django`, `jinja`</span><span class="sxs-lookup"><span data-stu-id="94192-398">`django`, `jinja`</span></span>                                                              |
| <span data-ttu-id="94192-399">Dockerfile</span><span class="sxs-lookup"><span data-stu-id="94192-399">Dockerfile</span></span>                     | <span data-ttu-id="94192-400">`dockerfile`, `docker`</span><span class="sxs-lookup"><span data-stu-id="94192-400">`dockerfile`, `docker`</span></span>                                                         |
| <span data-ttu-id="94192-401">dsconfig</span><span class="sxs-lookup"><span data-stu-id="94192-401">dsconfig</span></span>                       | `dsconfig`                                                                     |
| <span data-ttu-id="94192-402">DTS (Device Tree)</span><span class="sxs-lookup"><span data-stu-id="94192-402">DTS (Device Tree)</span></span>              | `dts`                                                                          |
| <span data-ttu-id="94192-403">Dust</span><span class="sxs-lookup"><span data-stu-id="94192-403">Dust</span></span>                           | <span data-ttu-id="94192-404">`dust`, `dst`</span><span class="sxs-lookup"><span data-stu-id="94192-404">`dust`, `dst`</span></span>                                                                  |
| <span data-ttu-id="94192-405">Dylan</span><span class="sxs-lookup"><span data-stu-id="94192-405">Dylan</span></span>                          | `dylan`                                                                        |
| <span data-ttu-id="94192-406">EBNF</span><span class="sxs-lookup"><span data-stu-id="94192-406">EBNF</span></span>                           | `ebnf`                                                                         |
| <span data-ttu-id="94192-407">Elixir</span><span class="sxs-lookup"><span data-stu-id="94192-407">Elixir</span></span>                         | `elixir`                                                                       |
| <span data-ttu-id="94192-408">Elm</span><span class="sxs-lookup"><span data-stu-id="94192-408">Elm</span></span>                            | `elm`                                                                          |
| <span data-ttu-id="94192-409">Erlang</span><span class="sxs-lookup"><span data-stu-id="94192-409">Erlang</span></span>                         | <span data-ttu-id="94192-410">`erlang`, `erl`</span><span class="sxs-lookup"><span data-stu-id="94192-410">`erlang`, `erl`</span></span>                                                                |
| <span data-ttu-id="94192-411">Excel</span><span class="sxs-lookup"><span data-stu-id="94192-411">Excel</span></span>                          | <span data-ttu-id="94192-412">`excel`, `xls`, `xlsx`</span><span class="sxs-lookup"><span data-stu-id="94192-412">`excel`, `xls`, `xlsx`</span></span>                                                         |
| <span data-ttu-id="94192-413">Extempore</span><span class="sxs-lookup"><span data-stu-id="94192-413">Extempore</span></span>                      | <span data-ttu-id="94192-414">`extempore`, `xtlang`, `xtm`</span><span class="sxs-lookup"><span data-stu-id="94192-414">`extempore`, `xtlang`, `xtm`</span></span>                                                   |
| <span data-ttu-id="94192-415">F#</span><span class="sxs-lookup"><span data-stu-id="94192-415">F#</span></span>                             | <span data-ttu-id="94192-416">`fsharp`, `fs`</span><span class="sxs-lookup"><span data-stu-id="94192-416">`fsharp`, `fs`</span></span>                                                                 |
| <span data-ttu-id="94192-417">FIX</span><span class="sxs-lookup"><span data-stu-id="94192-417">FIX</span></span>                            | `fix`                                                                          |
| <span data-ttu-id="94192-418">Fortran</span><span class="sxs-lookup"><span data-stu-id="94192-418">Fortran</span></span>                        | <span data-ttu-id="94192-419">`fortran`, `f90`, `f95`</span><span class="sxs-lookup"><span data-stu-id="94192-419">`fortran`, `f90`, `f95`</span></span>                                                        |
| <span data-ttu-id="94192-420">G-Code</span><span class="sxs-lookup"><span data-stu-id="94192-420">G-Code</span></span>                         | <span data-ttu-id="94192-421">`gcode`, `nc`</span><span class="sxs-lookup"><span data-stu-id="94192-421">`gcode`, `nc`</span></span>                                                                  |
| <span data-ttu-id="94192-422">Gams</span><span class="sxs-lookup"><span data-stu-id="94192-422">Gams</span></span>                           | <span data-ttu-id="94192-423">`gams`, `gms`</span><span class="sxs-lookup"><span data-stu-id="94192-423">`gams`, `gms`</span></span>                                                                  |
| <span data-ttu-id="94192-424">GAUSS</span><span class="sxs-lookup"><span data-stu-id="94192-424">GAUSS</span></span>                          | <span data-ttu-id="94192-425">`gauss`, `gss`</span><span class="sxs-lookup"><span data-stu-id="94192-425">`gauss`, `gss`</span></span>                                                                 |
| <span data-ttu-id="94192-426">GDScript</span><span class="sxs-lookup"><span data-stu-id="94192-426">GDScript</span></span>                       | <span data-ttu-id="94192-427">`godot`, `gdscript`</span><span class="sxs-lookup"><span data-stu-id="94192-427">`godot`, `gdscript`</span></span>                                                            |
| <span data-ttu-id="94192-428">Gherkin</span><span class="sxs-lookup"><span data-stu-id="94192-428">Gherkin</span></span>                        | `gherkin`                                                                      |
| <span data-ttu-id="94192-429">GN for Ninja</span><span class="sxs-lookup"><span data-stu-id="94192-429">GN for Ninja</span></span>                   | <span data-ttu-id="94192-430">`gn`, `gni`</span><span class="sxs-lookup"><span data-stu-id="94192-430">`gn`, `gni`</span></span>                                                                    |
| <span data-ttu-id="94192-431">Go</span><span class="sxs-lookup"><span data-stu-id="94192-431">Go</span></span>                             | <span data-ttu-id="94192-432">`go`, `golang`</span><span class="sxs-lookup"><span data-stu-id="94192-432">`go`, `golang`</span></span>                                                                 |
| <span data-ttu-id="94192-433">Golo</span><span class="sxs-lookup"><span data-stu-id="94192-433">Golo</span></span>                           | <span data-ttu-id="94192-434">`golo`, `gololang`</span><span class="sxs-lookup"><span data-stu-id="94192-434">`golo`, `gololang`</span></span>                                                             |
| <span data-ttu-id="94192-435">Gradle</span><span class="sxs-lookup"><span data-stu-id="94192-435">Gradle</span></span>                         | `gradle`                                                                       |
| <span data-ttu-id="94192-436">Groovy</span><span class="sxs-lookup"><span data-stu-id="94192-436">Groovy</span></span>                         | `groovy`                                                                       |
| <span data-ttu-id="94192-437">HTML</span><span class="sxs-lookup"><span data-stu-id="94192-437">HTML</span></span>                           | <span data-ttu-id="94192-438">`html`, `xhtml`</span><span class="sxs-lookup"><span data-stu-id="94192-438">`html`, `xhtml`</span></span>                                                                |
| <span data-ttu-id="94192-439">HTTP</span><span class="sxs-lookup"><span data-stu-id="94192-439">HTTP</span></span>                           | <span data-ttu-id="94192-440">`http`, `https`</span><span class="sxs-lookup"><span data-stu-id="94192-440">`http`, `https`</span></span>                                                                |
| <span data-ttu-id="94192-441">Haml</span><span class="sxs-lookup"><span data-stu-id="94192-441">Haml</span></span>                           | `haml`                                                                         |
| <span data-ttu-id="94192-442">Handlebars</span><span class="sxs-lookup"><span data-stu-id="94192-442">Handlebars</span></span>                     | <span data-ttu-id="94192-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span><span class="sxs-lookup"><span data-stu-id="94192-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span></span>                             |
| <span data-ttu-id="94192-444">Haskell</span><span class="sxs-lookup"><span data-stu-id="94192-444">Haskell</span></span>                        | <span data-ttu-id="94192-445">`haskell`, `hs`</span><span class="sxs-lookup"><span data-stu-id="94192-445">`haskell`, `hs`</span></span>                                                                |
| <span data-ttu-id="94192-446">Haxe</span><span class="sxs-lookup"><span data-stu-id="94192-446">Haxe</span></span>                           | <span data-ttu-id="94192-447">`haxe`, `hx`</span><span class="sxs-lookup"><span data-stu-id="94192-447">`haxe`, `hx`</span></span>                                                                   |
| <span data-ttu-id="94192-448">Hy</span><span class="sxs-lookup"><span data-stu-id="94192-448">Hy</span></span>                             | <span data-ttu-id="94192-449">`hy`, `hylang`</span><span class="sxs-lookup"><span data-stu-id="94192-449">`hy`, `hylang`</span></span>                                                                 |
| <span data-ttu-id="94192-450">Ini</span><span class="sxs-lookup"><span data-stu-id="94192-450">Ini</span></span>                            | `ini`                                                                          |
| <span data-ttu-id="94192-451">Inform7</span><span class="sxs-lookup"><span data-stu-id="94192-451">Inform7</span></span>                        | <span data-ttu-id="94192-452">`inform7`, `i7`</span><span class="sxs-lookup"><span data-stu-id="94192-452">`inform7`, `i7`</span></span>                                                                |
| <span data-ttu-id="94192-453">IRPF90</span><span class="sxs-lookup"><span data-stu-id="94192-453">IRPF90</span></span>                         | `irpf90`                                                                       |
| <span data-ttu-id="94192-454">JSON</span><span class="sxs-lookup"><span data-stu-id="94192-454">JSON</span></span>                           | `json`                                                                         |
| <span data-ttu-id="94192-455">Java</span><span class="sxs-lookup"><span data-stu-id="94192-455">Java</span></span>                           | <span data-ttu-id="94192-456">`java`, `jsp`</span><span class="sxs-lookup"><span data-stu-id="94192-456">`java`, `jsp`</span></span>                                                                  |
| <span data-ttu-id="94192-457">JavaScript</span><span class="sxs-lookup"><span data-stu-id="94192-457">JavaScript</span></span>                     | <span data-ttu-id="94192-458">`javascript`, `js`, `jsx`</span><span class="sxs-lookup"><span data-stu-id="94192-458">`javascript`, `js`, `jsx`</span></span>                                                      |
| <span data-ttu-id="94192-459">Kotlin</span><span class="sxs-lookup"><span data-stu-id="94192-459">Kotlin</span></span>                         | <span data-ttu-id="94192-460">`kotlin`, `kt`</span><span class="sxs-lookup"><span data-stu-id="94192-460">`kotlin`, `kt`</span></span>                                                                 |
| <span data-ttu-id="94192-461">Kusto</span><span class="sxs-lookup"><span data-stu-id="94192-461">Kusto</span></span>                          | `kusto`                                                                        |
| <span data-ttu-id="94192-462">Leaf</span><span class="sxs-lookup"><span data-stu-id="94192-462">Leaf</span></span>                           | `leaf`                                                                         |
| <span data-ttu-id="94192-463">Lasso</span><span class="sxs-lookup"><span data-stu-id="94192-463">Lasso</span></span>                          | <span data-ttu-id="94192-464">`lasso`, `ls`, `lassoscript`</span><span class="sxs-lookup"><span data-stu-id="94192-464">`lasso`, `ls`, `lassoscript`</span></span>                                                   |
| <span data-ttu-id="94192-465">Less</span><span class="sxs-lookup"><span data-stu-id="94192-465">Less</span></span>                           | `less`                                                                         |
| <span data-ttu-id="94192-466">LDIF</span><span class="sxs-lookup"><span data-stu-id="94192-466">LDIF</span></span>                           | `ldif`                                                                         |
| <span data-ttu-id="94192-467">Lisp</span><span class="sxs-lookup"><span data-stu-id="94192-467">Lisp</span></span>                           | `lisp`                                                                         |
| <span data-ttu-id="94192-468">LiveCode Server</span><span class="sxs-lookup"><span data-stu-id="94192-468">LiveCode Server</span></span>                | `livecodeserver`                                                               |
| <span data-ttu-id="94192-469">LiveScript</span><span class="sxs-lookup"><span data-stu-id="94192-469">LiveScript</span></span>                     | <span data-ttu-id="94192-470">`livescript`, `ls`</span><span class="sxs-lookup"><span data-stu-id="94192-470">`livescript`, `ls`</span></span>                                                             |
| <span data-ttu-id="94192-471">Lua</span><span class="sxs-lookup"><span data-stu-id="94192-471">Lua</span></span>                            | `lua`                                                                          |
| <span data-ttu-id="94192-472">Makefile</span><span class="sxs-lookup"><span data-stu-id="94192-472">Makefile</span></span>                       | <span data-ttu-id="94192-473">`makefile`, `mk`, `mak`</span><span class="sxs-lookup"><span data-stu-id="94192-473">`makefile`, `mk`, `mak`</span></span>                                                        |
| <span data-ttu-id="94192-474">Markdown</span><span class="sxs-lookup"><span data-stu-id="94192-474">Markdown</span></span>                       | <span data-ttu-id="94192-475">`markdown`, `md`, `mkdown`, `mkd`</span><span class="sxs-lookup"><span data-stu-id="94192-475">`markdown`, `md`, `mkdown`, `mkd`</span></span>                                              |
| <span data-ttu-id="94192-476">Mathematica</span><span class="sxs-lookup"><span data-stu-id="94192-476">Mathematica</span></span>                    | <span data-ttu-id="94192-477">`mathematica`, `mma`, `wl`</span><span class="sxs-lookup"><span data-stu-id="94192-477">`mathematica`, `mma`, `wl`</span></span>                                                     |
| <span data-ttu-id="94192-478">Matlab</span><span class="sxs-lookup"><span data-stu-id="94192-478">Matlab</span></span>                         | `matlab`                                                                       |
| <span data-ttu-id="94192-479">Maxima</span><span class="sxs-lookup"><span data-stu-id="94192-479">Maxima</span></span>                         | `maxima`                                                                       |
| <span data-ttu-id="94192-480">Maya Embedded Language</span><span class="sxs-lookup"><span data-stu-id="94192-480">Maya Embedded Language</span></span>         | `mel`                                                                          |
| <span data-ttu-id="94192-481">Mercury</span><span class="sxs-lookup"><span data-stu-id="94192-481">Mercury</span></span>                        | `mercury`                                                                      |
| <span data-ttu-id="94192-482">mIRC Scripting Language</span><span class="sxs-lookup"><span data-stu-id="94192-482">mIRC Scripting Language</span></span>        | <span data-ttu-id="94192-483">`mirc`, `mrc`</span><span class="sxs-lookup"><span data-stu-id="94192-483">`mirc`, `mrc`</span></span>                                                                  |
| <span data-ttu-id="94192-484">Mizar</span><span class="sxs-lookup"><span data-stu-id="94192-484">Mizar</span></span>                          | `mizar`                                                                        |
| <span data-ttu-id="94192-485">Managed Object Format</span><span class="sxs-lookup"><span data-stu-id="94192-485">Managed Object Format</span></span>          | `mof`                                                                          |
| <span data-ttu-id="94192-486">Mojolicious</span><span class="sxs-lookup"><span data-stu-id="94192-486">Mojolicious</span></span>                    | `mojolicious`                                                                  |
| <span data-ttu-id="94192-487">Monkey</span><span class="sxs-lookup"><span data-stu-id="94192-487">Monkey</span></span>                         | `monkey`                                                                       |
| <span data-ttu-id="94192-488">Moonscript</span><span class="sxs-lookup"><span data-stu-id="94192-488">Moonscript</span></span>                     | <span data-ttu-id="94192-489">`moonscript`, `moon`</span><span class="sxs-lookup"><span data-stu-id="94192-489">`moonscript`, `moon`</span></span>                                                           |
| <span data-ttu-id="94192-490">MS Graph (Interactive)</span><span class="sxs-lookup"><span data-stu-id="94192-490">MS Graph (Interactive)</span></span>         | `msgraph-interactive`                                                          |
| <span data-ttu-id="94192-491">N1QL</span><span class="sxs-lookup"><span data-stu-id="94192-491">N1QL</span></span>                           | `n1ql`                                                                         |
| <span data-ttu-id="94192-492">NSIS</span><span class="sxs-lookup"><span data-stu-id="94192-492">NSIS</span></span>                           | `nsis`                                                                         |
| <span data-ttu-id="94192-493">Nginx</span><span class="sxs-lookup"><span data-stu-id="94192-493">Nginx</span></span>                          | <span data-ttu-id="94192-494">`nginx`, `nginxconf`</span><span class="sxs-lookup"><span data-stu-id="94192-494">`nginx`, `nginxconf`</span></span>                                                           |
| <span data-ttu-id="94192-495">Nimrod</span><span class="sxs-lookup"><span data-stu-id="94192-495">Nimrod</span></span>                         | <span data-ttu-id="94192-496">`nimrod`, `nim`</span><span class="sxs-lookup"><span data-stu-id="94192-496">`nimrod`, `nim`</span></span>                                                                |
| <span data-ttu-id="94192-497">Nix</span><span class="sxs-lookup"><span data-stu-id="94192-497">Nix</span></span>                            | `nix`                                                                          |
| <span data-ttu-id="94192-498">OCaml</span><span class="sxs-lookup"><span data-stu-id="94192-498">OCaml</span></span>                          | <span data-ttu-id="94192-499">`ocaml`, `ml`</span><span class="sxs-lookup"><span data-stu-id="94192-499">`ocaml`, `ml`</span></span>                                                                  |
| <span data-ttu-id="94192-500">Objective C</span><span class="sxs-lookup"><span data-stu-id="94192-500">Objective C</span></span>                    | <span data-ttu-id="94192-501">`objectivec`, `mm`, `objc`, `obj-c`</span><span class="sxs-lookup"><span data-stu-id="94192-501">`objectivec`, `mm`, `objc`, `obj-c`</span></span>                                            |
| <span data-ttu-id="94192-502">OpenGL Shading Language</span><span class="sxs-lookup"><span data-stu-id="94192-502">OpenGL Shading Language</span></span>        | `glsl`                                                                         |
| <span data-ttu-id="94192-503">OpenSCAD</span><span class="sxs-lookup"><span data-stu-id="94192-503">OpenSCAD</span></span>                       | <span data-ttu-id="94192-504">`openscad`, `scad`</span><span class="sxs-lookup"><span data-stu-id="94192-504">`openscad`, `scad`</span></span>                                                             |
| <span data-ttu-id="94192-505">Oracle Rules Language</span><span class="sxs-lookup"><span data-stu-id="94192-505">Oracle Rules Language</span></span>          | `ruleslanguage`                                                                |
| <span data-ttu-id="94192-506">Oxygene</span><span class="sxs-lookup"><span data-stu-id="94192-506">Oxygene</span></span>                        | `oxygene`                                                                      |
| <span data-ttu-id="94192-507">PF</span><span class="sxs-lookup"><span data-stu-id="94192-507">PF</span></span>                             | <span data-ttu-id="94192-508">`pf`, `pf.conf`</span><span class="sxs-lookup"><span data-stu-id="94192-508">`pf`, `pf.conf`</span></span>                                                                |
| <span data-ttu-id="94192-509">PHP</span><span class="sxs-lookup"><span data-stu-id="94192-509">PHP</span></span>                            | <span data-ttu-id="94192-510">`php`, `php3`, `php4`, `php5`, `php6`</span><span class="sxs-lookup"><span data-stu-id="94192-510">`php`, `php3`, `php4`, `php5`, `php6`</span></span>                                          |
| <span data-ttu-id="94192-511">Parser3</span><span class="sxs-lookup"><span data-stu-id="94192-511">Parser3</span></span>                        | `parser3`                                                                      |
| <span data-ttu-id="94192-512">Perl</span><span class="sxs-lookup"><span data-stu-id="94192-512">Perl</span></span>                           | <span data-ttu-id="94192-513">`perl`, `pl`, `pm`</span><span class="sxs-lookup"><span data-stu-id="94192-513">`perl`, `pl`, `pm`</span></span>                                                             |
| <span data-ttu-id="94192-514">Plaintext no highlight</span><span class="sxs-lookup"><span data-stu-id="94192-514">Plaintext no highlight</span></span>         | `plaintext`                                                                    |
| <span data-ttu-id="94192-515">Pony</span><span class="sxs-lookup"><span data-stu-id="94192-515">Pony</span></span>                           | `pony`                                                                         |
| <span data-ttu-id="94192-516">PostgreSQL & PL/pgSQL</span><span class="sxs-lookup"><span data-stu-id="94192-516">PostgreSQL & PL/pgSQL</span></span>          | <span data-ttu-id="94192-517">`pgsql`, `postgres`, `postgresql`</span><span class="sxs-lookup"><span data-stu-id="94192-517">`pgsql`, `postgres`, `postgresql`</span></span>                                              |
| <span data-ttu-id="94192-518">PowerShell</span><span class="sxs-lookup"><span data-stu-id="94192-518">PowerShell</span></span>                     | <span data-ttu-id="94192-519">`powershell`, `ps`</span><span class="sxs-lookup"><span data-stu-id="94192-519">`powershell`, `ps`</span></span>                                                             |
| <span data-ttu-id="94192-520">PowerShell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="94192-520">PowerShell (Interactive)</span></span>       | `powershell-interactive`                                                       |
| <span data-ttu-id="94192-521">Processing</span><span class="sxs-lookup"><span data-stu-id="94192-521">Processing</span></span>                     | `processing`                                                                   |
| <span data-ttu-id="94192-522">Prolog</span><span class="sxs-lookup"><span data-stu-id="94192-522">Prolog</span></span>                         | `prolog`                                                                       |
| <span data-ttu-id="94192-523">Properties</span><span class="sxs-lookup"><span data-stu-id="94192-523">Properties</span></span>                     | `properties`                                                                   |
| <span data-ttu-id="94192-524">Protocol Buffers</span><span class="sxs-lookup"><span data-stu-id="94192-524">Protocol Buffers</span></span>               | `protobuf`                                                                     |
| <span data-ttu-id="94192-525">Puppet</span><span class="sxs-lookup"><span data-stu-id="94192-525">Puppet</span></span>                         | <span data-ttu-id="94192-526">`puppet`, `pp`</span><span class="sxs-lookup"><span data-stu-id="94192-526">`puppet`, `pp`</span></span>                                                                 |
| <span data-ttu-id="94192-527">Python</span><span class="sxs-lookup"><span data-stu-id="94192-527">Python</span></span>                         | <span data-ttu-id="94192-528">`python`, `py`, `gyp`</span><span class="sxs-lookup"><span data-stu-id="94192-528">`python`, `py`, `gyp`</span></span>                                                          |
| <span data-ttu-id="94192-529">Python profiler results</span><span class="sxs-lookup"><span data-stu-id="94192-529">Python profiler results</span></span>        | `profile`                                                                      |
| <span data-ttu-id="94192-530">Q#</span><span class="sxs-lookup"><span data-stu-id="94192-530">Q#</span></span>                             | `qsharp`                                                                       |
| <span data-ttu-id="94192-531">Q</span><span class="sxs-lookup"><span data-stu-id="94192-531">Q</span></span>                              | <span data-ttu-id="94192-532">`k`, `kdb`</span><span class="sxs-lookup"><span data-stu-id="94192-532">`k`, `kdb`</span></span>                                                                     |
| <span data-ttu-id="94192-533">QML</span><span class="sxs-lookup"><span data-stu-id="94192-533">QML</span></span>                            | `qml`                                                                          |
| <span data-ttu-id="94192-534">R</span><span class="sxs-lookup"><span data-stu-id="94192-534">R</span></span>                              | `r`                                                                            |
| <span data-ttu-id="94192-535">Razor CSHTML</span><span class="sxs-lookup"><span data-stu-id="94192-535">Razor CSHTML</span></span>                   | <span data-ttu-id="94192-536">`cshtml`, `razor`, `razor-cshtml`</span><span class="sxs-lookup"><span data-stu-id="94192-536">`cshtml`, `razor`, `razor-cshtml`</span></span>                                              |
| <span data-ttu-id="94192-537">ReasonML</span><span class="sxs-lookup"><span data-stu-id="94192-537">ReasonML</span></span>                       | <span data-ttu-id="94192-538">`reasonml`, `re`</span><span class="sxs-lookup"><span data-stu-id="94192-538">`reasonml`, `re`</span></span>                                                               |
| <span data-ttu-id="94192-539">RenderMan RIB</span><span class="sxs-lookup"><span data-stu-id="94192-539">RenderMan RIB</span></span>                  | `rib`                                                                          |
| <span data-ttu-id="94192-540">RenderMan RSL</span><span class="sxs-lookup"><span data-stu-id="94192-540">RenderMan RSL</span></span>                  | `rsl`                                                                          |
| <span data-ttu-id="94192-541">Roboconf</span><span class="sxs-lookup"><span data-stu-id="94192-541">Roboconf</span></span>                       | <span data-ttu-id="94192-542">`graph`, `instances`</span><span class="sxs-lookup"><span data-stu-id="94192-542">`graph`, `instances`</span></span>                                                           |
| <span data-ttu-id="94192-543">Robot Framework</span><span class="sxs-lookup"><span data-stu-id="94192-543">Robot Framework</span></span>                | <span data-ttu-id="94192-544">`robot`, `rf`</span><span class="sxs-lookup"><span data-stu-id="94192-544">`robot`, `rf`</span></span>                                                                  |
| <span data-ttu-id="94192-545">RPM spec files</span><span class="sxs-lookup"><span data-stu-id="94192-545">RPM spec files</span></span>                 | <span data-ttu-id="94192-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span><span class="sxs-lookup"><span data-stu-id="94192-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span></span>                          |
| <span data-ttu-id="94192-547">Ruby</span><span class="sxs-lookup"><span data-stu-id="94192-547">Ruby</span></span>                           | <span data-ttu-id="94192-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span><span class="sxs-lookup"><span data-stu-id="94192-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span></span>                              |
| <span data-ttu-id="94192-549">Rust</span><span class="sxs-lookup"><span data-stu-id="94192-549">Rust</span></span>                           | <span data-ttu-id="94192-550">`rust`, `rs`</span><span class="sxs-lookup"><span data-stu-id="94192-550">`rust`, `rs`</span></span>                                                                   |
| <span data-ttu-id="94192-551">SAS</span><span class="sxs-lookup"><span data-stu-id="94192-551">SAS</span></span>                            | <span data-ttu-id="94192-552">`SAS`, `sas`</span><span class="sxs-lookup"><span data-stu-id="94192-552">`SAS`, `sas`</span></span>                                                                   |
| <span data-ttu-id="94192-553">SCSS</span><span class="sxs-lookup"><span data-stu-id="94192-553">SCSS</span></span>                           | `scss`                                                                         |
| <span data-ttu-id="94192-554">SQL</span><span class="sxs-lookup"><span data-stu-id="94192-554">SQL</span></span>                            | `sql`                                                                          |
| <span data-ttu-id="94192-555">STEP Part 21</span><span class="sxs-lookup"><span data-stu-id="94192-555">STEP Part 21</span></span>                   | <span data-ttu-id="94192-556">`p21`, `step`, `stp`</span><span class="sxs-lookup"><span data-stu-id="94192-556">`p21`, `step`, `stp`</span></span>                                                           |
| <span data-ttu-id="94192-557">Scala</span><span class="sxs-lookup"><span data-stu-id="94192-557">Scala</span></span>                          | `scala`                                                                        |
| <span data-ttu-id="94192-558">Scheme</span><span class="sxs-lookup"><span data-stu-id="94192-558">Scheme</span></span>                         | `scheme`                                                                       |
| <span data-ttu-id="94192-559">Scilab</span><span class="sxs-lookup"><span data-stu-id="94192-559">Scilab</span></span>                         | <span data-ttu-id="94192-560">`scilab`, `sci`</span><span class="sxs-lookup"><span data-stu-id="94192-560">`scilab`, `sci`</span></span>                                                                |
| <span data-ttu-id="94192-561">Shape Expressions</span><span class="sxs-lookup"><span data-stu-id="94192-561">Shape Expressions</span></span>              | `shexc`                                                                        |
| <span data-ttu-id="94192-562">Shell</span><span class="sxs-lookup"><span data-stu-id="94192-562">Shell</span></span>                          | <span data-ttu-id="94192-563">`shell`, `console`</span><span class="sxs-lookup"><span data-stu-id="94192-563">`shell`, `console`</span></span>                                                             |
| <span data-ttu-id="94192-564">Smali</span><span class="sxs-lookup"><span data-stu-id="94192-564">Smali</span></span>                          | `smali`                                                                        |
| <span data-ttu-id="94192-565">Smalltalk</span><span class="sxs-lookup"><span data-stu-id="94192-565">Smalltalk</span></span>                      | <span data-ttu-id="94192-566">`smalltalk`, `st`</span><span class="sxs-lookup"><span data-stu-id="94192-566">`smalltalk`, `st`</span></span>                                                              |
| <span data-ttu-id="94192-567">Solidity</span><span class="sxs-lookup"><span data-stu-id="94192-567">Solidity</span></span>                       | <span data-ttu-id="94192-568">`solidity`, `sol`</span><span class="sxs-lookup"><span data-stu-id="94192-568">`solidity`, `sol`</span></span>                                                              |
| <span data-ttu-id="94192-569">Stan</span><span class="sxs-lookup"><span data-stu-id="94192-569">Stan</span></span>                           | `stan`                                                                         |
| <span data-ttu-id="94192-570">Stata</span><span class="sxs-lookup"><span data-stu-id="94192-570">Stata</span></span>                          | `stata`                                                                        |
| <span data-ttu-id="94192-571">Structured Text</span><span class="sxs-lookup"><span data-stu-id="94192-571">Structured Text</span></span>                | <span data-ttu-id="94192-572">`iecst`, `scl`, `stl`, `structured-text`</span><span class="sxs-lookup"><span data-stu-id="94192-572">`iecst`, `scl`, `stl`, `structured-text`</span></span>                                       |
| <span data-ttu-id="94192-573">Stylus</span><span class="sxs-lookup"><span data-stu-id="94192-573">Stylus</span></span>                         | <span data-ttu-id="94192-574">`stylus`, `styl`</span><span class="sxs-lookup"><span data-stu-id="94192-574">`stylus`, `styl`</span></span>                                                               |
| <span data-ttu-id="94192-575">SubUnit</span><span class="sxs-lookup"><span data-stu-id="94192-575">SubUnit</span></span>                        | `subunit`                                                                      |
| <span data-ttu-id="94192-576">Supercollider</span><span class="sxs-lookup"><span data-stu-id="94192-576">Supercollider</span></span>                  | <span data-ttu-id="94192-577">`supercollider`, `sc`</span><span class="sxs-lookup"><span data-stu-id="94192-577">`supercollider`, `sc`</span></span>                                                          |
| <span data-ttu-id="94192-578">Swift</span><span class="sxs-lookup"><span data-stu-id="94192-578">Swift</span></span>                          | `swift`                                                                        |
| <span data-ttu-id="94192-579">Tcl</span><span class="sxs-lookup"><span data-stu-id="94192-579">Tcl</span></span>                            | <span data-ttu-id="94192-580">`tcl`, `tk`</span><span class="sxs-lookup"><span data-stu-id="94192-580">`tcl`, `tk`</span></span>                                                                    |
| <span data-ttu-id="94192-581">Terraform (HCL)</span><span class="sxs-lookup"><span data-stu-id="94192-581">Terraform (HCL)</span></span>                | <span data-ttu-id="94192-582">`terraform`, `tf`, `hcl`</span><span class="sxs-lookup"><span data-stu-id="94192-582">`terraform`, `tf`, `hcl`</span></span>                                                       |
| <span data-ttu-id="94192-583">Test Anything Protocol</span><span class="sxs-lookup"><span data-stu-id="94192-583">Test Anything Protocol</span></span>         | `tap`                                                                          |
| <span data-ttu-id="94192-584">TeX</span><span class="sxs-lookup"><span data-stu-id="94192-584">TeX</span></span>                            | `tex`                                                                          |
| <span data-ttu-id="94192-585">Thrift</span><span class="sxs-lookup"><span data-stu-id="94192-585">Thrift</span></span>                         | `thrift`                                                                       |
| <span data-ttu-id="94192-586">TOML</span><span class="sxs-lookup"><span data-stu-id="94192-586">TOML</span></span>                           | `toml`                                                                         |
| <span data-ttu-id="94192-587">TP</span><span class="sxs-lookup"><span data-stu-id="94192-587">TP</span></span>                             | `tp`                                                                           |
| <span data-ttu-id="94192-588">Twig</span><span class="sxs-lookup"><span data-stu-id="94192-588">Twig</span></span>                           | <span data-ttu-id="94192-589">`twig`, `craftcms`</span><span class="sxs-lookup"><span data-stu-id="94192-589">`twig`, `craftcms`</span></span>                                                             |
| <span data-ttu-id="94192-590">TypeScript</span><span class="sxs-lookup"><span data-stu-id="94192-590">TypeScript</span></span>                     | <span data-ttu-id="94192-591">`typescript`, `ts`</span><span class="sxs-lookup"><span data-stu-id="94192-591">`typescript`, `ts`</span></span>                                                             |
| <span data-ttu-id="94192-592">VB.NET</span><span class="sxs-lookup"><span data-stu-id="94192-592">VB.NET</span></span>                         | <span data-ttu-id="94192-593">`vbnet`, `vb`</span><span class="sxs-lookup"><span data-stu-id="94192-593">`vbnet`, `vb`</span></span>                                                                  |
| <span data-ttu-id="94192-594">VBScript</span><span class="sxs-lookup"><span data-stu-id="94192-594">VBScript</span></span>                       | <span data-ttu-id="94192-595">`vbscript`, `vbs`</span><span class="sxs-lookup"><span data-stu-id="94192-595">`vbscript`, `vbs`</span></span>                                                              |
| <span data-ttu-id="94192-596">VHDL</span><span class="sxs-lookup"><span data-stu-id="94192-596">VHDL</span></span>                           | `vhdl`                                                                         |
| <span data-ttu-id="94192-597">Vala</span><span class="sxs-lookup"><span data-stu-id="94192-597">Vala</span></span>                           | `vala`                                                                         |
| <span data-ttu-id="94192-598">Verilog</span><span class="sxs-lookup"><span data-stu-id="94192-598">Verilog</span></span>                        | <span data-ttu-id="94192-599">`verilog`, `v`</span><span class="sxs-lookup"><span data-stu-id="94192-599">`verilog`, `v`</span></span>                                                                 |
| <span data-ttu-id="94192-600">Vim Script</span><span class="sxs-lookup"><span data-stu-id="94192-600">Vim Script</span></span>                     | `vim`                                                                          |
| <span data-ttu-id="94192-601">X++</span><span class="sxs-lookup"><span data-stu-id="94192-601">X++</span></span>                            | `xpp`                                                                          |
| <span data-ttu-id="94192-602">x86 Assembly</span><span class="sxs-lookup"><span data-stu-id="94192-602">x86 Assembly</span></span>                   | `x86asm`                                                                       |
| <span data-ttu-id="94192-603">XL</span><span class="sxs-lookup"><span data-stu-id="94192-603">XL</span></span>                             | <span data-ttu-id="94192-604">`xl`, `tao`</span><span class="sxs-lookup"><span data-stu-id="94192-604">`xl`, `tao`</span></span>                                                                    |
| <span data-ttu-id="94192-605">XQuery</span><span class="sxs-lookup"><span data-stu-id="94192-605">XQuery</span></span>                         | <span data-ttu-id="94192-606">`xquery`, `xpath`, `xq`</span><span class="sxs-lookup"><span data-stu-id="94192-606">`xquery`, `xpath`, `xq`</span></span>                                                        |
| <span data-ttu-id="94192-607">XAML</span><span class="sxs-lookup"><span data-stu-id="94192-607">XAML</span></span>                           | `xaml`                                                                         |
| <span data-ttu-id="94192-608">XML</span><span class="sxs-lookup"><span data-stu-id="94192-608">XML</span></span>                            | <span data-ttu-id="94192-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span><span class="sxs-lookup"><span data-stu-id="94192-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span></span>                    |
| <span data-ttu-id="94192-610">YAML</span><span class="sxs-lookup"><span data-stu-id="94192-610">YAML</span></span>                           | <span data-ttu-id="94192-611">`yml`, `yaml`</span><span class="sxs-lookup"><span data-stu-id="94192-611">`yml`, `yaml`</span></span>                                                                  |
| <span data-ttu-id="94192-612">Zephir</span><span class="sxs-lookup"><span data-stu-id="94192-612">Zephir</span></span>                         | <span data-ttu-id="94192-613">`zephir`, `zep`</span><span class="sxs-lookup"><span data-stu-id="94192-613">`zephir`, `zep`</span></span>                                                                |

> [!TIP]
> <span data-ttu-id="94192-614">Docs Authoring Pack의 [개발자 언어 완성 기능](docs-authoring/dev-lang-completion.md)은 여러 별칭을 사용할 수 있는 경우 첫 번째 유효한 별칭을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94192-614">The Docs Authoring Pack, [Dev Lang Completion feature](docs-authoring/dev-lang-completion.md) uses the first valid alias when multiple aliases are available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94192-615">다음 단계</span><span class="sxs-lookup"><span data-stu-id="94192-615">Next steps</span></span>

<span data-ttu-id="94192-616">코드 이외의 콘텐츠 유형 텍스트 서식 지정에 대한 자세한 내용은 [텍스트 서식 지정 지침](text-formatting-guidelines.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94192-616">For information on text formatting for content types other than code, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>
