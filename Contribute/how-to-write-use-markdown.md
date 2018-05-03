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
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="e7c33-103">Markdown을 사용하여 Docs를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7c33-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="e7c33-104">Docs.microsoft.com 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="e7c33-105">그렇기 때문에 신속하게 산업 표준이 되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="e7c33-106">Docs 콘텐츠가 GitHub에 저장되기 때문에 일반적인 형식 요구 사항에 추가 기능을 제공하는 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)이라는 Markdown의 상위 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="e7c33-107">또한 OPS(Open Publishing Services)는 DFM(DocFX Flavored Markdown)을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="e7c33-108">DFM은 GFM(GitHub Flavored Markdown)과 호환성이 뛰어나 Docs 전용 기능을 사용할 수 있는 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="e7c33-109">Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="e7c33-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="e7c33-110">제목</span><span class="sxs-lookup"><span data-stu-id="e7c33-110">Headings</span></span>

<span data-ttu-id="e7c33-111">제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="e7c33-112">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="e7c33-112">Bold and italic text</span></span>

<span data-ttu-id="e7c33-113">텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="e7c33-114">텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="e7c33-115">텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="e7c33-116">목록</span><span class="sxs-lookup"><span data-stu-id="e7c33-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="e7c33-117">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="e7c33-117">Unordered list</span></span>

<span data-ttu-id="e7c33-118">정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="e7c33-119">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="e7c33-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="e7c33-120">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-120">will be rendered as:</span></span>

- <span data-ttu-id="e7c33-121">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="e7c33-121">List item 1</span></span>
- <span data-ttu-id="e7c33-122">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="e7c33-122">List item 2</span></span>
- <span data-ttu-id="e7c33-123">목록 항목 3</span><span class="sxs-lookup"><span data-stu-id="e7c33-123">List item 3</span></span>

<span data-ttu-id="e7c33-124">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="e7c33-125">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="e7c33-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="e7c33-126">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-126">will be rendered as:</span></span>

- <span data-ttu-id="e7c33-127">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="e7c33-127">List item 1</span></span>
  - <span data-ttu-id="e7c33-128">목록 항목 A</span><span class="sxs-lookup"><span data-stu-id="e7c33-128">List item A</span></span>
  - <span data-ttu-id="e7c33-129">목록 항목 B</span><span class="sxs-lookup"><span data-stu-id="e7c33-129">List item B</span></span>
- <span data-ttu-id="e7c33-130">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="e7c33-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="e7c33-131">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="e7c33-131">Ordered list</span></span>

<span data-ttu-id="e7c33-132">정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="e7c33-133">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="e7c33-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="e7c33-134">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-134">will be rendered as:</span></span>

1. <span data-ttu-id="e7c33-135">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-135">First instruction</span></span>
2. <span data-ttu-id="e7c33-136">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-136">Second instruction</span></span>
3. <span data-ttu-id="e7c33-137">세 번째 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-137">Third instruction</span></span>

<span data-ttu-id="e7c33-138">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="e7c33-139">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="e7c33-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="e7c33-140">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-140">will be rendered as:</span></span>

1. <span data-ttu-id="e7c33-141">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-141">First instruction</span></span>
    1. <span data-ttu-id="e7c33-142">하위 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-142">Sub-instruction</span></span>
    2. <span data-ttu-id="e7c33-143">하위 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-143">Sub-instruction</span></span>
2. <span data-ttu-id="e7c33-144">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="e7c33-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="e7c33-145">보세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-145">Tables</span></span>

<span data-ttu-id="e7c33-146">테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="e7c33-147">파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="e7c33-148">하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="e7c33-149">테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="e7c33-150">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="e7c33-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="e7c33-151">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-151">will be rendered as:</span></span>

| <span data-ttu-id="e7c33-152">테이블을</span><span class="sxs-lookup"><span data-stu-id="e7c33-152">Fun</span></span>                  | <span data-ttu-id="e7c33-153">사용해</span><span class="sxs-lookup"><span data-stu-id="e7c33-153">With</span></span>                 | <span data-ttu-id="e7c33-154">보세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="e7c33-155">왼쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="e7c33-155">left-aligned column</span></span>  | <span data-ttu-id="e7c33-156">오른쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="e7c33-156">right-aligned column</span></span> | <span data-ttu-id="e7c33-157">가운데 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="e7c33-157">centered column</span></span> |
| <span data-ttu-id="e7c33-158">$100</span><span class="sxs-lookup"><span data-stu-id="e7c33-158">$100</span></span>                 | <span data-ttu-id="e7c33-159">$100</span><span class="sxs-lookup"><span data-stu-id="e7c33-159">$100</span></span>                 | <span data-ttu-id="e7c33-160">$100</span><span class="sxs-lookup"><span data-stu-id="e7c33-160">$100</span></span>            |
| <span data-ttu-id="e7c33-161">$10</span><span class="sxs-lookup"><span data-stu-id="e7c33-161">$10</span></span>                  | <span data-ttu-id="e7c33-162">$10</span><span class="sxs-lookup"><span data-stu-id="e7c33-162">$10</span></span>                  | <span data-ttu-id="e7c33-163">$10</span><span class="sxs-lookup"><span data-stu-id="e7c33-163">$10</span></span>             |
| <span data-ttu-id="e7c33-164">$1</span><span class="sxs-lookup"><span data-stu-id="e7c33-164">$1</span></span>                   | <span data-ttu-id="e7c33-165">$1</span><span class="sxs-lookup"><span data-stu-id="e7c33-165">$1</span></span>                   | <span data-ttu-id="e7c33-166">$1</span><span class="sxs-lookup"><span data-stu-id="e7c33-166">$1</span></span>              |

<span data-ttu-id="e7c33-167">테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="e7c33-168">DFM [테이블 래핑 기능](#table-wrapping)은 넓은 테이블의 서식을 지정하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="e7c33-169">GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="e7c33-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="e7c33-170">[Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱</span><span class="sxs-lookup"><span data-stu-id="e7c33-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="e7c33-171">Adam Pritchard의 Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="e7c33-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="e7c33-172">Michel Fortin의 Markdown 추가 자료</span><span class="sxs-lookup"><span data-stu-id="e7c33-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="e7c33-173">HTML 테이블을 Markdown으로 전환</span><span class="sxs-lookup"><span data-stu-id="e7c33-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="e7c33-174">링크</span><span class="sxs-lookup"><span data-stu-id="e7c33-174">Links</span></span>

<span data-ttu-id="e7c33-175">인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="e7c33-176">연결에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-176">For more information on linking, see:</span></span>

- <span data-ttu-id="e7c33-177">Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)</span><span class="sxs-lookup"><span data-stu-id="e7c33-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="e7c33-178">이 가이드의 [링크](how-to-write-links.md) 페이지에 DFM에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="e7c33-179">코드 조각</span><span class="sxs-lookup"><span data-stu-id="e7c33-179">Code snippets</span></span>

<span data-ttu-id="e7c33-180">Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="e7c33-181">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-181">For details, see:</span></span>

- [<span data-ttu-id="e7c33-182">코드 블록에 대한 Markdown의 네이티브 지원</span><span class="sxs-lookup"><span data-stu-id="e7c33-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="e7c33-183">코드 펜싱 및 구문 강조 표시에 대한 GFM 지원</span><span class="sxs-lookup"><span data-stu-id="e7c33-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="e7c33-184">펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="e7c33-185">펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="e7c33-186">처음 세 개의 \` 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="e7c33-187">Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="e7c33-188">이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="e7c33-189">이름</span><span class="sxs-lookup"><span data-stu-id="e7c33-189">Name</span></span>|<span data-ttu-id="e7c33-190">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="e7c33-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="e7c33-191">.NET 콘솔</span><span class="sxs-lookup"><span data-stu-id="e7c33-191">.NET Console</span></span>|<span data-ttu-id="e7c33-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="e7c33-192">dotnetcli</span></span>|
|<span data-ttu-id="e7c33-193">ASP.NET(C#)</span><span class="sxs-lookup"><span data-stu-id="e7c33-193">ASP.NET (C#)</span></span>|<span data-ttu-id="e7c33-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="e7c33-194">aspx-csharp</span></span>|
|<span data-ttu-id="e7c33-195">ASP.NET(VB)</span><span class="sxs-lookup"><span data-stu-id="e7c33-195">ASP.NET (VB)</span></span>|<span data-ttu-id="e7c33-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="e7c33-196">aspx-vb</span></span>|
|<span data-ttu-id="e7c33-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="e7c33-197">AzCopy</span></span>|<span data-ttu-id="e7c33-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="e7c33-198">azcopy</span></span>|
|<span data-ttu-id="e7c33-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="e7c33-199">Azure CLI</span></span>|<span data-ttu-id="e7c33-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="e7c33-200">azurecli</span></span>|
|<span data-ttu-id="e7c33-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7c33-201">Azure PowerShell</span></span>|<span data-ttu-id="e7c33-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="e7c33-202">azurepowershell</span></span>|
|<span data-ttu-id="e7c33-203">C++</span><span class="sxs-lookup"><span data-stu-id="e7c33-203">C++</span></span>|<span data-ttu-id="e7c33-204">cpp</span><span class="sxs-lookup"><span data-stu-id="e7c33-204">cpp</span></span>|
|<span data-ttu-id="e7c33-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="e7c33-205">C++/CX</span></span>|<span data-ttu-id="e7c33-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="e7c33-206">cppcx</span></span>|
|<span data-ttu-id="e7c33-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="e7c33-207">C++/WinRT</span></span>|<span data-ttu-id="e7c33-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="e7c33-208">cppwinrt</span></span>|
|<span data-ttu-id="e7c33-209">C#</span><span class="sxs-lookup"><span data-stu-id="e7c33-209">C#</span></span>|<span data-ttu-id="e7c33-210">csharp</span><span class="sxs-lookup"><span data-stu-id="e7c33-210">csharp</span></span>|
|<span data-ttu-id="e7c33-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="e7c33-211">CSHTML</span></span>|<span data-ttu-id="e7c33-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="e7c33-212">cshtml</span></span>|
|<span data-ttu-id="e7c33-213">DAX</span><span class="sxs-lookup"><span data-stu-id="e7c33-213">DAX</span></span>|<span data-ttu-id="e7c33-214">dax</span><span class="sxs-lookup"><span data-stu-id="e7c33-214">dax</span></span>|
|<span data-ttu-id="e7c33-215">F#</span><span class="sxs-lookup"><span data-stu-id="e7c33-215">F#</span></span>|<span data-ttu-id="e7c33-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="e7c33-216">fsharp</span></span>|
|<span data-ttu-id="e7c33-217">Go</span><span class="sxs-lookup"><span data-stu-id="e7c33-217">Go</span></span>|<span data-ttu-id="e7c33-218">go</span><span class="sxs-lookup"><span data-stu-id="e7c33-218">go</span></span>|
|<span data-ttu-id="e7c33-219">HTML</span><span class="sxs-lookup"><span data-stu-id="e7c33-219">HTML</span></span>|<span data-ttu-id="e7c33-220">html</span><span class="sxs-lookup"><span data-stu-id="e7c33-220">html</span></span>|
|<span data-ttu-id="e7c33-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="e7c33-221">HTTP</span></span>|<span data-ttu-id="e7c33-222">http</span><span class="sxs-lookup"><span data-stu-id="e7c33-222">http</span></span>|
|<span data-ttu-id="e7c33-223">Java</span><span class="sxs-lookup"><span data-stu-id="e7c33-223">Java</span></span>|<span data-ttu-id="e7c33-224">java</span><span class="sxs-lookup"><span data-stu-id="e7c33-224">java</span></span>|
|<span data-ttu-id="e7c33-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e7c33-225">JavaScript</span></span>|<span data-ttu-id="e7c33-226">javascript</span><span class="sxs-lookup"><span data-stu-id="e7c33-226">javascript</span></span>|
|<span data-ttu-id="e7c33-227">JSON</span><span class="sxs-lookup"><span data-stu-id="e7c33-227">JSON</span></span>|<span data-ttu-id="e7c33-228">json</span><span class="sxs-lookup"><span data-stu-id="e7c33-228">json</span></span>|
|<span data-ttu-id="e7c33-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="e7c33-229">Markdown</span></span>|<span data-ttu-id="e7c33-230">md</span><span class="sxs-lookup"><span data-stu-id="e7c33-230">md</span></span>|
|<span data-ttu-id="e7c33-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="e7c33-231">NodeJS</span></span>|<span data-ttu-id="e7c33-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="e7c33-232">nodejs</span></span>|
|<span data-ttu-id="e7c33-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="e7c33-233">Objective-C</span></span>|<span data-ttu-id="e7c33-234">objc</span><span class="sxs-lookup"><span data-stu-id="e7c33-234">objc</span></span>|
|<span data-ttu-id="e7c33-235">OData</span><span class="sxs-lookup"><span data-stu-id="e7c33-235">OData</span></span>|<span data-ttu-id="e7c33-236">odata</span><span class="sxs-lookup"><span data-stu-id="e7c33-236">odata</span></span>|
|<span data-ttu-id="e7c33-237">PHP</span><span class="sxs-lookup"><span data-stu-id="e7c33-237">PHP</span></span>|<span data-ttu-id="e7c33-238">php</span><span class="sxs-lookup"><span data-stu-id="e7c33-238">php</span></span>|
|<span data-ttu-id="e7c33-239">Power Apps 수식</span><span class="sxs-lookup"><span data-stu-id="e7c33-239">Power Apps Formula</span></span>|<span data-ttu-id="e7c33-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="e7c33-240">powerappsfl</span></span>|
|<span data-ttu-id="e7c33-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7c33-241">PowerShell</span></span>|<span data-ttu-id="e7c33-242">powershell</span><span class="sxs-lookup"><span data-stu-id="e7c33-242">powershell</span></span>|
|<span data-ttu-id="e7c33-243">Python</span><span class="sxs-lookup"><span data-stu-id="e7c33-243">Python</span></span>|<span data-ttu-id="e7c33-244">python</span><span class="sxs-lookup"><span data-stu-id="e7c33-244">python</span></span>|
|<span data-ttu-id="e7c33-245">Q#</span><span class="sxs-lookup"><span data-stu-id="e7c33-245">Q#</span></span>|<span data-ttu-id="e7c33-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="e7c33-246">qsharp</span></span>|
|<span data-ttu-id="e7c33-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="e7c33-247">Ruby</span></span>|<span data-ttu-id="e7c33-248">ruby</span><span class="sxs-lookup"><span data-stu-id="e7c33-248">ruby</span></span>|
|<span data-ttu-id="e7c33-249">SQL</span><span class="sxs-lookup"><span data-stu-id="e7c33-249">SQL</span></span>|<span data-ttu-id="e7c33-250">sql</span><span class="sxs-lookup"><span data-stu-id="e7c33-250">sql</span></span>|
|<span data-ttu-id="e7c33-251">Swift</span><span class="sxs-lookup"><span data-stu-id="e7c33-251">Swift</span></span>|<span data-ttu-id="e7c33-252">swift</span><span class="sxs-lookup"><span data-stu-id="e7c33-252">swift</span></span>|
|<span data-ttu-id="e7c33-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="e7c33-253">TypeScript</span></span>|<span data-ttu-id="e7c33-254">typescript</span><span class="sxs-lookup"><span data-stu-id="e7c33-254">typescript</span></span>|
|<span data-ttu-id="e7c33-255">VB</span><span class="sxs-lookup"><span data-stu-id="e7c33-255">VB</span></span>|<span data-ttu-id="e7c33-256">vb</span><span class="sxs-lookup"><span data-stu-id="e7c33-256">vb</span></span>|
|<span data-ttu-id="e7c33-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="e7c33-257">VSTS CLI</span></span>|<span data-ttu-id="e7c33-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="e7c33-258">vstscli</span></span>|
|<span data-ttu-id="e7c33-259">XAML</span><span class="sxs-lookup"><span data-stu-id="e7c33-259">XAML</span></span>|<span data-ttu-id="e7c33-260">xaml</span><span class="sxs-lookup"><span data-stu-id="e7c33-260">xaml</span></span>|
|<span data-ttu-id="e7c33-261">XML</span><span class="sxs-lookup"><span data-stu-id="e7c33-261">XML</span></span>|<span data-ttu-id="e7c33-262">xml</span><span class="sxs-lookup"><span data-stu-id="e7c33-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="e7c33-263">예: C\#</span><span class="sxs-lookup"><span data-stu-id="e7c33-263">Example: C\#</span></span>

<span data-ttu-id="e7c33-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="e7c33-264">__Markdown__</span></span>

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

<span data-ttu-id="e7c33-265">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="e7c33-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="e7c33-266">예: SQL</span><span class="sxs-lookup"><span data-stu-id="e7c33-266">Example: SQL</span></span>

<span data-ttu-id="e7c33-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="e7c33-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="e7c33-268">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="e7c33-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="e7c33-269">OPS 사용자 지정 Markdown 확장</span><span class="sxs-lookup"><span data-stu-id="e7c33-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="e7c33-270">OPS(Open Publishing Services)는 GFM(GitHub Flavored Markdown)과 호환성이 높은 DFM(DocFX Flavored Markdown)을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="e7c33-271">DFM은 Markdown 확장을 통해 몇 가지 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="e7c33-272">이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="e7c33-273">예를 들어 목차에서 "DFM 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="e7c33-274">Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="e7c33-275">더 많은 형식의 경우 문서는 다음과 같은 DFM 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="e7c33-276">참고 블록</span><span class="sxs-lookup"><span data-stu-id="e7c33-276">Note blocks</span></span>
- <span data-ttu-id="e7c33-277">포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="e7c33-277">Includes</span></span>
- <span data-ttu-id="e7c33-278">선택기</span><span class="sxs-lookup"><span data-stu-id="e7c33-278">Selectors</span></span>
- <span data-ttu-id="e7c33-279">포함된 비디오</span><span class="sxs-lookup"><span data-stu-id="e7c33-279">Embedded videos</span></span>
- <span data-ttu-id="e7c33-280">코드 조각/샘플</span><span class="sxs-lookup"><span data-stu-id="e7c33-280">Code snippets/samples</span></span>

<span data-ttu-id="e7c33-281">전체 목록은 목차에서 "DFM 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c33-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="e7c33-282">참고 블록</span><span class="sxs-lookup"><span data-stu-id="e7c33-282">Note blocks</span></span>

<span data-ttu-id="e7c33-283">특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="e7c33-284">참고</span><span class="sxs-lookup"><span data-stu-id="e7c33-284">NOTE</span></span>
- <span data-ttu-id="e7c33-285">경고</span><span class="sxs-lookup"><span data-stu-id="e7c33-285">WARNING</span></span>
- <span data-ttu-id="e7c33-286">팁</span><span class="sxs-lookup"><span data-stu-id="e7c33-286">TIP</span></span>
- <span data-ttu-id="e7c33-287">중요</span><span class="sxs-lookup"><span data-stu-id="e7c33-287">IMPORTANT</span></span>

<span data-ttu-id="e7c33-288">일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="e7c33-289">참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="e7c33-290">포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="e7c33-290">Includes</span></span>

<span data-ttu-id="e7c33-291">문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 DFM 파일 포함 기능을 통해 "포함되는 내용" 파일에 대한 참조를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="e7c33-292">이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="e7c33-293">콘텐츠를 재사용하기 위해 사용 가능한 포함되는 내용에는 3가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="e7c33-294">인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="e7c33-295">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="e7c33-296">이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="e7c33-297">인라인 또는 블록 포함되는 내용은 간단한 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="e7c33-298">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="e7c33-299">포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="e7c33-300">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="e7c33-301">포함되는 내용의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="e7c33-302">여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 내용을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="e7c33-303">블록 포함되는 내용은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="e7c33-304">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="e7c33-305">포함되는 내용은 DFM 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="e7c33-306">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="e7c33-307">포함되는 내용의 모든 텍스트가 문서에서 포함되는 내용을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="e7c33-308">이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="e7c33-309">다른 포함되는 내용 내에 포함되는 내용을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="e7c33-310">지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-310">They are not supported.</span></span>
- <span data-ttu-id="e7c33-311">미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더).</span><span class="sxs-lookup"><span data-stu-id="e7c33-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="e7c33-312">미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="e7c33-313">포함되는 내용에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="e7c33-314">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="e7c33-315">각 포함되는 내용 및 문서에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="e7c33-316">포함되는 내용과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="e7c33-317">포함되는 내용을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="e7c33-318">포함되는 내용은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="e7c33-319">선택기</span><span class="sxs-lookup"><span data-stu-id="e7c33-319">Selectors</span></span>

<span data-ttu-id="e7c33-320">동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼에서 구현 중에 차이점을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="e7c33-321">이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="e7c33-322">DFM에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="e7c33-323">동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기가 포함되는 내용에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="e7c33-324">그런 다음 동일한 선택기를 사용하는 모든 문서에서 해당 포함되는 내용을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="e7c33-325">코드 조각</span><span class="sxs-lookup"><span data-stu-id="e7c33-325">Code snippets</span></span>

<span data-ttu-id="e7c33-326">DFM은 해당 코드 조각 확장을 통해 문서에 대한 고급 코드 포함 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="e7c33-327">이 기능은 프로그래밍 언어 선택과 구문 색 지정 및 다음과 같은 멋진 기능을 기반으로 하는 GFM 기능에서 빌드하는 고급 렌더링을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="e7c33-328">외부 리포지토리에서 중앙 집중식 코드 샘플/코드 조각 포함</span><span class="sxs-lookup"><span data-stu-id="e7c33-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="e7c33-329">다른 언어로 여러 버전의 코드 샘플을 표시하는 탭 UI</span><span class="sxs-lookup"><span data-stu-id="e7c33-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="e7c33-330">과제 및 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e7c33-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="e7c33-331">대체 텍스트</span><span class="sxs-lookup"><span data-stu-id="e7c33-331">Alt text</span></span>

<span data-ttu-id="e7c33-332">밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="e7c33-333">예를 들어 아래 텍스트를 사용하는 대신</span><span class="sxs-lookup"><span data-stu-id="e7c33-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="e7c33-334">다음과 같이 밑줄을 이스케이프 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="e7c33-335">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="e7c33-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="e7c33-336">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="e7c33-337">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="e7c33-338">그렇지 않을 경우 파일이 게시되면 Itâ€™s와 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="e7c33-339">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="e7c33-340">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="e7c33-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="e7c33-341">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="e7c33-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="e7c33-342">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="e7c33-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="e7c33-343">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="e7c33-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="e7c33-344">대괄호</span><span class="sxs-lookup"><span data-stu-id="e7c33-344">Angle brackets</span></span>

<span data-ttu-id="e7c33-345">예를 들어 자리 표시자를 나타내는 것과 같이 파일에 있는 텍스트(코드 아님)에서 대괄호를 사용하는 경우 대괄호를 수동으로 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="e7c33-346">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="e7c33-347">예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c33-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="e7c33-348">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e7c33-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="e7c33-349">Markdown 리소스</span><span class="sxs-lookup"><span data-stu-id="e7c33-349">Markdown resources</span></span>

- [<span data-ttu-id="e7c33-350">Markdown 소개</span><span class="sxs-lookup"><span data-stu-id="e7c33-350">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="e7c33-351">Docs Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="e7c33-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="e7c33-352">GitHub의 Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="e7c33-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
