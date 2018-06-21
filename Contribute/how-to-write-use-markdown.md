---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
ms.date: 07/13/2017
ms.openlocfilehash: dca1ccba2ae4ebd08b6039f5d780e7a7ac92e79f
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238969"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="46362-103">Markdown을 사용하여 Docs를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="46362-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="46362-104">Docs.microsoft.com 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="46362-105">그렇기 때문에 신속하게 산업 표준이 되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="46362-106">Docs 콘텐츠가 GitHub에 저장되기 때문에 일반적인 형식 요구 사항에 추가 기능을 제공하는 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)이라는 Markdown의 상위 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="46362-107">또한 OPS(Open Publishing Services)는 Markdig Markdown Parser를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="46362-108">Markdig은 GFM(GitHub Flavored Markdown)과 호환성이 뛰어나 Docs 전용 기능을 사용할 수 있는 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="46362-109">Markdig은 빠르고 강력하며 CommonMark와 호환되며 .NET에 대해 확장 가능한 Markdown 프로세서입니다.</span><span class="sxs-lookup"><span data-stu-id="46362-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="46362-110">커뮤니티 지원 향상</span><span class="sxs-lookup"><span data-stu-id="46362-110">Better community support</span></span>
* <span data-ttu-id="46362-111">표준 지원 향상</span><span class="sxs-lookup"><span data-stu-id="46362-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="46362-112">Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="46362-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="46362-113">제목</span><span class="sxs-lookup"><span data-stu-id="46362-113">Headings</span></span>

<span data-ttu-id="46362-114">제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="46362-115">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="46362-115">Bold and italic text</span></span>

<span data-ttu-id="46362-116">텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="46362-117">텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="46362-118">텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="46362-119">목록</span><span class="sxs-lookup"><span data-stu-id="46362-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="46362-120">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="46362-120">Unordered list</span></span>

<span data-ttu-id="46362-121">정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="46362-122">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="46362-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="46362-123">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-123">will be rendered as:</span></span>

- <span data-ttu-id="46362-124">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="46362-124">List item 1</span></span>
- <span data-ttu-id="46362-125">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="46362-125">List item 2</span></span>
- <span data-ttu-id="46362-126">목록 항목 3</span><span class="sxs-lookup"><span data-stu-id="46362-126">List item 3</span></span>

<span data-ttu-id="46362-127">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="46362-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="46362-128">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="46362-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="46362-129">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-129">will be rendered as:</span></span>

- <span data-ttu-id="46362-130">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="46362-130">List item 1</span></span>
  - <span data-ttu-id="46362-131">목록 항목 A</span><span class="sxs-lookup"><span data-stu-id="46362-131">List item A</span></span>
  - <span data-ttu-id="46362-132">목록 항목 B</span><span class="sxs-lookup"><span data-stu-id="46362-132">List item B</span></span>
- <span data-ttu-id="46362-133">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="46362-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="46362-134">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="46362-134">Ordered list</span></span>

<span data-ttu-id="46362-135">정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="46362-136">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="46362-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="46362-137">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-137">will be rendered as:</span></span>

1. <span data-ttu-id="46362-138">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="46362-138">First instruction</span></span>
2. <span data-ttu-id="46362-139">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="46362-139">Second instruction</span></span>
3. <span data-ttu-id="46362-140">세 번째 지침</span><span class="sxs-lookup"><span data-stu-id="46362-140">Third instruction</span></span>

<span data-ttu-id="46362-141">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="46362-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="46362-142">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="46362-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="46362-143">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-143">will be rendered as:</span></span>

1. <span data-ttu-id="46362-144">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="46362-144">First instruction</span></span>
    1. <span data-ttu-id="46362-145">하위 지침</span><span class="sxs-lookup"><span data-stu-id="46362-145">Sub-instruction</span></span>
    2. <span data-ttu-id="46362-146">하위 지침</span><span class="sxs-lookup"><span data-stu-id="46362-146">Sub-instruction</span></span>
2. <span data-ttu-id="46362-147">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="46362-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="46362-148">보세요.</span><span class="sxs-lookup"><span data-stu-id="46362-148">Tables</span></span>

<span data-ttu-id="46362-149">테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="46362-150">파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="46362-151">하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="46362-152">테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="46362-153">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="46362-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="46362-154">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-154">will be rendered as:</span></span>

| <span data-ttu-id="46362-155">테이블을</span><span class="sxs-lookup"><span data-stu-id="46362-155">Fun</span></span>                  | <span data-ttu-id="46362-156">사용해</span><span class="sxs-lookup"><span data-stu-id="46362-156">With</span></span>                 | <span data-ttu-id="46362-157">보세요.</span><span class="sxs-lookup"><span data-stu-id="46362-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="46362-158">왼쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="46362-158">left-aligned column</span></span>  | <span data-ttu-id="46362-159">오른쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="46362-159">right-aligned column</span></span> | <span data-ttu-id="46362-160">가운데 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="46362-160">centered column</span></span> |
| <span data-ttu-id="46362-161">$100</span><span class="sxs-lookup"><span data-stu-id="46362-161">$100</span></span>                 | <span data-ttu-id="46362-162">$100</span><span class="sxs-lookup"><span data-stu-id="46362-162">$100</span></span>                 | <span data-ttu-id="46362-163">$100</span><span class="sxs-lookup"><span data-stu-id="46362-163">$100</span></span>            |
| <span data-ttu-id="46362-164">$10</span><span class="sxs-lookup"><span data-stu-id="46362-164">$10</span></span>                  | <span data-ttu-id="46362-165">$10</span><span class="sxs-lookup"><span data-stu-id="46362-165">$10</span></span>                  | <span data-ttu-id="46362-166">$10</span><span class="sxs-lookup"><span data-stu-id="46362-166">$10</span></span>             |
| <span data-ttu-id="46362-167">$1</span><span class="sxs-lookup"><span data-stu-id="46362-167">$1</span></span>                   | <span data-ttu-id="46362-168">$1</span><span class="sxs-lookup"><span data-stu-id="46362-168">$1</span></span>                   | <span data-ttu-id="46362-169">$1</span><span class="sxs-lookup"><span data-stu-id="46362-169">$1</span></span>              |

<span data-ttu-id="46362-170">테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46362-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="46362-171">넓은 테이블의 서식을 지정하는 데 도움이 되는 Markdig [테이블 래핑 기능](#table-wrapping)</span><span class="sxs-lookup"><span data-stu-id="46362-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="46362-172">GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="46362-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="46362-173">[Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱</span><span class="sxs-lookup"><span data-stu-id="46362-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="46362-174">Adam Pritchard의 Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="46362-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="46362-175">Michel Fortin의 Markdown 추가 자료</span><span class="sxs-lookup"><span data-stu-id="46362-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="46362-176">HTML 테이블을 Markdown으로 전환</span><span class="sxs-lookup"><span data-stu-id="46362-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="46362-177">링크</span><span class="sxs-lookup"><span data-stu-id="46362-177">Links</span></span>

<span data-ttu-id="46362-178">인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="46362-179">연결에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46362-179">For more information on linking, see:</span></span>

- <span data-ttu-id="46362-180">Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)</span><span class="sxs-lookup"><span data-stu-id="46362-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="46362-181">이 가이드의 [링크](how-to-write-links.md) 페이지에 Markdig에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="46362-182">코드 조각</span><span class="sxs-lookup"><span data-stu-id="46362-182">Code snippets</span></span>

<span data-ttu-id="46362-183">Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="46362-184">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46362-184">For details, see:</span></span>

- [<span data-ttu-id="46362-185">코드 블록에 대한 Markdown의 네이티브 지원</span><span class="sxs-lookup"><span data-stu-id="46362-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="46362-186">코드 펜싱 및 구문 강조 표시에 대한 GFM 지원</span><span class="sxs-lookup"><span data-stu-id="46362-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="46362-187">펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="46362-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="46362-188">펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="46362-189">처음 세 개의 \` 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="46362-190">Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="46362-191">이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="46362-192">이름</span><span class="sxs-lookup"><span data-stu-id="46362-192">Name</span></span>|<span data-ttu-id="46362-193">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="46362-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="46362-194">.NET 콘솔</span><span class="sxs-lookup"><span data-stu-id="46362-194">.NET Console</span></span>|<span data-ttu-id="46362-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="46362-195">dotnetcli</span></span>|
|<span data-ttu-id="46362-196">ASP.NET(C#)</span><span class="sxs-lookup"><span data-stu-id="46362-196">ASP.NET (C#)</span></span>|<span data-ttu-id="46362-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="46362-197">aspx-csharp</span></span>|
|<span data-ttu-id="46362-198">ASP.NET(VB)</span><span class="sxs-lookup"><span data-stu-id="46362-198">ASP.NET (VB)</span></span>|<span data-ttu-id="46362-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="46362-199">aspx-vb</span></span>|
|<span data-ttu-id="46362-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="46362-200">AzCopy</span></span>|<span data-ttu-id="46362-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="46362-201">azcopy</span></span>|
|<span data-ttu-id="46362-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="46362-202">Azure CLI</span></span>|<span data-ttu-id="46362-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="46362-203">azurecli</span></span>|
|<span data-ttu-id="46362-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="46362-204">Azure PowerShell</span></span>|<span data-ttu-id="46362-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="46362-205">azurepowershell</span></span>|
|<span data-ttu-id="46362-206">C++</span><span class="sxs-lookup"><span data-stu-id="46362-206">C++</span></span>|<span data-ttu-id="46362-207">cpp</span><span class="sxs-lookup"><span data-stu-id="46362-207">cpp</span></span>|
|<span data-ttu-id="46362-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="46362-208">C++/CX</span></span>|<span data-ttu-id="46362-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="46362-209">cppcx</span></span>|
|<span data-ttu-id="46362-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="46362-210">C++/WinRT</span></span>|<span data-ttu-id="46362-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="46362-211">cppwinrt</span></span>|
|<span data-ttu-id="46362-212">C#</span><span class="sxs-lookup"><span data-stu-id="46362-212">C#</span></span>|<span data-ttu-id="46362-213">csharp</span><span class="sxs-lookup"><span data-stu-id="46362-213">csharp</span></span>|
|<span data-ttu-id="46362-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="46362-214">CSHTML</span></span>|<span data-ttu-id="46362-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="46362-215">cshtml</span></span>|
|<span data-ttu-id="46362-216">DAX</span><span class="sxs-lookup"><span data-stu-id="46362-216">DAX</span></span>|<span data-ttu-id="46362-217">dax</span><span class="sxs-lookup"><span data-stu-id="46362-217">dax</span></span>|
|<span data-ttu-id="46362-218">F#</span><span class="sxs-lookup"><span data-stu-id="46362-218">F#</span></span>|<span data-ttu-id="46362-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="46362-219">fsharp</span></span>|
|<span data-ttu-id="46362-220">Go</span><span class="sxs-lookup"><span data-stu-id="46362-220">Go</span></span>|<span data-ttu-id="46362-221">go</span><span class="sxs-lookup"><span data-stu-id="46362-221">go</span></span>|
|<span data-ttu-id="46362-222">HTML</span><span class="sxs-lookup"><span data-stu-id="46362-222">HTML</span></span>|<span data-ttu-id="46362-223">html</span><span class="sxs-lookup"><span data-stu-id="46362-223">html</span></span>|
|<span data-ttu-id="46362-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="46362-224">HTTP</span></span>|<span data-ttu-id="46362-225">http</span><span class="sxs-lookup"><span data-stu-id="46362-225">http</span></span>|
|<span data-ttu-id="46362-226">Java</span><span class="sxs-lookup"><span data-stu-id="46362-226">Java</span></span>|<span data-ttu-id="46362-227">java</span><span class="sxs-lookup"><span data-stu-id="46362-227">java</span></span>|
|<span data-ttu-id="46362-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="46362-228">JavaScript</span></span>|<span data-ttu-id="46362-229">javascript</span><span class="sxs-lookup"><span data-stu-id="46362-229">javascript</span></span>|
|<span data-ttu-id="46362-230">JSON</span><span class="sxs-lookup"><span data-stu-id="46362-230">JSON</span></span>|<span data-ttu-id="46362-231">json</span><span class="sxs-lookup"><span data-stu-id="46362-231">json</span></span>|
|<span data-ttu-id="46362-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="46362-232">Markdown</span></span>|<span data-ttu-id="46362-233">md</span><span class="sxs-lookup"><span data-stu-id="46362-233">md</span></span>|
|<span data-ttu-id="46362-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="46362-234">NodeJS</span></span>|<span data-ttu-id="46362-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="46362-235">nodejs</span></span>|
|<span data-ttu-id="46362-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="46362-236">Objective-C</span></span>|<span data-ttu-id="46362-237">objc</span><span class="sxs-lookup"><span data-stu-id="46362-237">objc</span></span>|
|<span data-ttu-id="46362-238">OData</span><span class="sxs-lookup"><span data-stu-id="46362-238">OData</span></span>|<span data-ttu-id="46362-239">odata</span><span class="sxs-lookup"><span data-stu-id="46362-239">odata</span></span>|
|<span data-ttu-id="46362-240">PHP</span><span class="sxs-lookup"><span data-stu-id="46362-240">PHP</span></span>|<span data-ttu-id="46362-241">php</span><span class="sxs-lookup"><span data-stu-id="46362-241">php</span></span>|
|<span data-ttu-id="46362-242">Power Apps 수식</span><span class="sxs-lookup"><span data-stu-id="46362-242">Power Apps Formula</span></span>|<span data-ttu-id="46362-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="46362-243">powerappsfl</span></span>|
|<span data-ttu-id="46362-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="46362-244">PowerShell</span></span>|<span data-ttu-id="46362-245">powershell</span><span class="sxs-lookup"><span data-stu-id="46362-245">powershell</span></span>|
|<span data-ttu-id="46362-246">Python</span><span class="sxs-lookup"><span data-stu-id="46362-246">Python</span></span>|<span data-ttu-id="46362-247">python</span><span class="sxs-lookup"><span data-stu-id="46362-247">python</span></span>|
|<span data-ttu-id="46362-248">Q#</span><span class="sxs-lookup"><span data-stu-id="46362-248">Q#</span></span>|<span data-ttu-id="46362-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="46362-249">qsharp</span></span>|
|<span data-ttu-id="46362-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="46362-250">Ruby</span></span>|<span data-ttu-id="46362-251">ruby</span><span class="sxs-lookup"><span data-stu-id="46362-251">ruby</span></span>|
|<span data-ttu-id="46362-252">SQL</span><span class="sxs-lookup"><span data-stu-id="46362-252">SQL</span></span>|<span data-ttu-id="46362-253">sql</span><span class="sxs-lookup"><span data-stu-id="46362-253">sql</span></span>|
|<span data-ttu-id="46362-254">Swift</span><span class="sxs-lookup"><span data-stu-id="46362-254">Swift</span></span>|<span data-ttu-id="46362-255">swift</span><span class="sxs-lookup"><span data-stu-id="46362-255">swift</span></span>|
|<span data-ttu-id="46362-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="46362-256">TypeScript</span></span>|<span data-ttu-id="46362-257">typescript</span><span class="sxs-lookup"><span data-stu-id="46362-257">typescript</span></span>|
|<span data-ttu-id="46362-258">VB</span><span class="sxs-lookup"><span data-stu-id="46362-258">VB</span></span>|<span data-ttu-id="46362-259">vb</span><span class="sxs-lookup"><span data-stu-id="46362-259">vb</span></span>|
|<span data-ttu-id="46362-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="46362-260">VSTS CLI</span></span>|<span data-ttu-id="46362-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="46362-261">vstscli</span></span>|
|<span data-ttu-id="46362-262">XAML</span><span class="sxs-lookup"><span data-stu-id="46362-262">XAML</span></span>|<span data-ttu-id="46362-263">xaml</span><span class="sxs-lookup"><span data-stu-id="46362-263">xaml</span></span>|
|<span data-ttu-id="46362-264">XML</span><span class="sxs-lookup"><span data-stu-id="46362-264">XML</span></span>|<span data-ttu-id="46362-265">xml</span><span class="sxs-lookup"><span data-stu-id="46362-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="46362-266">예: C\#</span><span class="sxs-lookup"><span data-stu-id="46362-266">Example: C\#</span></span>

<span data-ttu-id="46362-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="46362-267">__Markdown__</span></span>

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

<span data-ttu-id="46362-268">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="46362-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="46362-269">예: SQL</span><span class="sxs-lookup"><span data-stu-id="46362-269">Example: SQL</span></span>

<span data-ttu-id="46362-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="46362-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="46362-271">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="46362-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="46362-272">OPS 사용자 지정 Markdown 확장</span><span class="sxs-lookup"><span data-stu-id="46362-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="46362-273">OPS(Open Publishing Services)는 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="46362-274">Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="46362-275">이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="46362-276">(예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="46362-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="46362-277">Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="46362-278">더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="46362-279">참고 블록</span><span class="sxs-lookup"><span data-stu-id="46362-279">Note blocks</span></span>
- <span data-ttu-id="46362-280">포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="46362-280">Includes</span></span>
- <span data-ttu-id="46362-281">선택기</span><span class="sxs-lookup"><span data-stu-id="46362-281">Selectors</span></span>
- <span data-ttu-id="46362-282">포함된 비디오</span><span class="sxs-lookup"><span data-stu-id="46362-282">Embedded videos</span></span>
- <span data-ttu-id="46362-283">코드 조각/샘플</span><span class="sxs-lookup"><span data-stu-id="46362-283">Code snippets/samples</span></span>

<span data-ttu-id="46362-284">전체 목록은 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46362-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="46362-285">참고 블록</span><span class="sxs-lookup"><span data-stu-id="46362-285">Note blocks</span></span>

<span data-ttu-id="46362-286">특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="46362-287">참고</span><span class="sxs-lookup"><span data-stu-id="46362-287">NOTE</span></span>
- <span data-ttu-id="46362-288">경고</span><span class="sxs-lookup"><span data-stu-id="46362-288">WARNING</span></span>
- <span data-ttu-id="46362-289">팁</span><span class="sxs-lookup"><span data-stu-id="46362-289">TIP</span></span>
- <span data-ttu-id="46362-290">중요</span><span class="sxs-lookup"><span data-stu-id="46362-290">IMPORTANT</span></span>

<span data-ttu-id="46362-291">일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="46362-292">참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="46362-293">포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="46362-293">Includes</span></span>

<span data-ttu-id="46362-294">문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는 내용" 파일에 대한 참조를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="46362-295">이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46362-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="46362-296">콘텐츠를 재사용하기 위해 사용 가능한 포함되는 내용에는 3가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="46362-297">인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="46362-298">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="46362-299">이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="46362-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="46362-300">인라인 또는 블록 포함되는 내용은 간단한 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="46362-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="46362-301">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="46362-302">포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="46362-303">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="46362-304">포함되는 내용의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="46362-305">여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 내용을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="46362-306">블록 포함되는 내용은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="46362-307">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="46362-308">포함되는 내용은 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="46362-309">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="46362-310">포함되는 내용의 모든 텍스트가 문서에서 포함되는 내용을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="46362-311">이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="46362-312">다른 포함되는 내용 내에 포함되는 내용을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="46362-313">지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-313">They are not supported.</span></span>
- <span data-ttu-id="46362-314">미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더).</span><span class="sxs-lookup"><span data-stu-id="46362-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="46362-315">미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="46362-316">포함되는 내용에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="46362-317">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="46362-318">각 포함되는 내용 및 문서에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="46362-319">포함되는 내용과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="46362-320">포함되는 내용을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="46362-321">포함되는 내용은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="46362-322">선택기</span><span class="sxs-lookup"><span data-stu-id="46362-322">Selectors</span></span>

<span data-ttu-id="46362-323">동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼에서 구현 중에 차이점을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="46362-324">이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="46362-325">Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="46362-326">동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기가 포함되는 내용에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="46362-327">그런 다음 동일한 선택기를 사용하는 모든 문서에서 해당 포함되는 내용을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="46362-328">코드 조각</span><span class="sxs-lookup"><span data-stu-id="46362-328">Code snippets</span></span>

<span data-ttu-id="46362-329">Markdig은 해당 코드 조각 확장을 통해 문서에 대한 고급 코드 포함 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="46362-330">이 기능은 프로그래밍 언어 선택과 구문 색 지정 및 다음과 같은 멋진 기능을 기반으로 하는 GFM 기능에서 빌드하는 고급 렌더링을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="46362-331">외부 리포지토리에서 중앙 집중식 코드 샘플/코드 조각 포함</span><span class="sxs-lookup"><span data-stu-id="46362-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="46362-332">다른 언어로 여러 버전의 코드 샘플을 표시하는 탭 UI</span><span class="sxs-lookup"><span data-stu-id="46362-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="46362-333">과제 및 문제 해결</span><span class="sxs-lookup"><span data-stu-id="46362-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="46362-334">대체 텍스트</span><span class="sxs-lookup"><span data-stu-id="46362-334">Alt text</span></span>

<span data-ttu-id="46362-335">밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="46362-336">예를 들어 아래 텍스트를 사용하는 대신</span><span class="sxs-lookup"><span data-stu-id="46362-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="46362-337">다음과 같이 밑줄을 이스케이프 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="46362-338">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="46362-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="46362-339">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46362-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="46362-340">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="46362-341">그렇지 않을 경우 파일이 게시되면 Itâ€™s와 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46362-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="46362-342">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="46362-343">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="46362-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="46362-344">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="46362-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="46362-345">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="46362-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="46362-346">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="46362-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="46362-347">대괄호</span><span class="sxs-lookup"><span data-stu-id="46362-347">Angle brackets</span></span>

<span data-ttu-id="46362-348">예를 들어 자리 표시자를 나타내는 것과 같이 파일에 있는 텍스트(코드 아님)에서 대괄호를 사용하는 경우 대괄호를 수동으로 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="46362-349">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="46362-350">예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="46362-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="46362-351">참고 항목</span><span class="sxs-lookup"><span data-stu-id="46362-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="46362-352">Markdown 리소스</span><span class="sxs-lookup"><span data-stu-id="46362-352">Markdown resources</span></span>

- [<span data-ttu-id="46362-353">Markdown 소개</span><span class="sxs-lookup"><span data-stu-id="46362-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="46362-354">Docs Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="46362-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="46362-355">GitHub의 Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="46362-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
