---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
ms.date: 01/29/2019
ms.openlocfilehash: 5235189d11c8c20ac20c91572d8bafcf525fb7c0
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887301"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="21142-103">Markdown을 사용하여 Docs를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="21142-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="21142-104">[Docs.microsoft.com](http://docs.microsoft.com) 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="21142-105">그렇기 때문에 신속하게 산업 표준이 되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="21142-106">docs.microsoft.com 사이트 백 엔드에는 [Markdig](https://github.com/lunet-io/markdig)를 통해 구문 분석되는 [CommonMark](https://commonmark.org/) 규격 markdown을 지원하고 [DFM(DocFX Flavored Markdown)](https://dotnet.github.io/docfx/)도 지원하는 OPS(Open Publishing Services)가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="21142-107">해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-107">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="21142-108">추가 기능은 Markdown 확장을 통해 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-108">Additional functionality is added through Markdown extensions.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="21142-109">Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="21142-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="21142-110">제목</span><span class="sxs-lookup"><span data-stu-id="21142-110">Headings</span></span>

<span data-ttu-id="21142-111">제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="21142-112">제목은 atx-style을 사용하여 수행해야 합니다. 즉, 줄의 시작 부분에 1-6 해시 문자(#)를 사용하여 HTML 제목 수준 H1~H6에 해당하는 제목을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-112">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="21142-113">위의 1~4번째 수준 헤더의 예가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-113">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="21142-114">항목에는 첫 번째 수준 제목(H1)이 하나만 **있어야 하며**, 해당 페이지 제목으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-114">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="21142-115">제목이 `#` 문자로 끝나는 경우 제목을 올바르게 랜더링하려면 끝에 나머지 `#` 문자를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-115">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="21142-116">예: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="21142-116">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="21142-117">두 번째 수준 제목은 해당 페이지 제목 아래의 “이 문서의 내용” 섹션에 나타나는 해당 페이지의 TOC를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-117">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="21142-118">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="21142-118">Bold and italic text</span></span>

<span data-ttu-id="21142-119">텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-119">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="21142-120">텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-120">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="21142-121">텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-121">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="21142-122">Blockquotes</span><span class="sxs-lookup"><span data-stu-id="21142-122">Blockquotes</span></span>

<span data-ttu-id="21142-123">Blockquotes는 `>` 문자를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-123">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="21142-124">앞의 예는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-124">The preceding example renders as follows:</span></span>

> <span data-ttu-id="21142-125">가뭄은 지금 천만년 동안 지속되었고 끔찍한 도마뱀의 통치는 끝난 지 오래되었습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="21142-126">언젠가 아프리카로 알려질 이 적도에서 생존을 위한 투쟁은 새로운 격렬한 절정에 이르렀고, 승자는 아직 보이지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="21142-127">이 황량하고 메마른 땅에서는 작고 빠르거나 사나운 존재만이 번성하거나 생존할 수 있을 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="21142-128">목록</span><span class="sxs-lookup"><span data-stu-id="21142-128">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="21142-129">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="21142-129">Unordered list</span></span>

<span data-ttu-id="21142-130">정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-130">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="21142-131">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="21142-131">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="21142-132">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-132">will be rendered as:</span></span>

- <span data-ttu-id="21142-133">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="21142-133">List item 1</span></span>
- <span data-ttu-id="21142-134">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="21142-134">List item 2</span></span>
- <span data-ttu-id="21142-135">목록 항목 3</span><span class="sxs-lookup"><span data-stu-id="21142-135">List item 3</span></span>

<span data-ttu-id="21142-136">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="21142-136">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="21142-137">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="21142-137">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="21142-138">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-138">will be rendered as:</span></span>

- <span data-ttu-id="21142-139">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="21142-139">List item 1</span></span>
  - <span data-ttu-id="21142-140">목록 항목 A</span><span class="sxs-lookup"><span data-stu-id="21142-140">List item A</span></span>
  - <span data-ttu-id="21142-141">목록 항목 B</span><span class="sxs-lookup"><span data-stu-id="21142-141">List item B</span></span>
- <span data-ttu-id="21142-142">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="21142-142">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="21142-143">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="21142-143">Ordered list</span></span>

<span data-ttu-id="21142-144">정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-144">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="21142-145">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="21142-145">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="21142-146">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-146">will be rendered as:</span></span>

1. <span data-ttu-id="21142-147">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="21142-147">First instruction</span></span>
2. <span data-ttu-id="21142-148">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="21142-148">Second instruction</span></span>
3. <span data-ttu-id="21142-149">세 번째 지침</span><span class="sxs-lookup"><span data-stu-id="21142-149">Third instruction</span></span>

<span data-ttu-id="21142-150">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="21142-150">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="21142-151">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="21142-151">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="21142-152">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-152">will be rendered as:</span></span>

1. <span data-ttu-id="21142-153">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="21142-153">First instruction</span></span>
   1. <span data-ttu-id="21142-154">하위 지침</span><span class="sxs-lookup"><span data-stu-id="21142-154">Sub-instruction</span></span>
   2. <span data-ttu-id="21142-155">하위 지침</span><span class="sxs-lookup"><span data-stu-id="21142-155">Sub-instruction</span></span>
2. <span data-ttu-id="21142-156">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="21142-156">Second instruction</span></span>

<span data-ttu-id="21142-157">'1'을</span><span class="sxs-lookup"><span data-stu-id="21142-157">Note that we use '1.'</span></span> <span data-ttu-id="21142-158">모든 항목에 대해 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-158">for all entries.</span></span> <span data-ttu-id="21142-159">최신 업데이트에 새 단계가 포함되거나 기존 단계가 제거될 때 더 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-159">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="21142-160">보세요.</span><span class="sxs-lookup"><span data-stu-id="21142-160">Tables</span></span>

<span data-ttu-id="21142-161">테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-161">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="21142-162">파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-162">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="21142-163">하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-163">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="21142-164">테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-164">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="21142-165">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="21142-165">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="21142-166">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-166">will be rendered as:</span></span>

| <span data-ttu-id="21142-167">테이블을</span><span class="sxs-lookup"><span data-stu-id="21142-167">Fun</span></span>                  | <span data-ttu-id="21142-168">사용해</span><span class="sxs-lookup"><span data-stu-id="21142-168">With</span></span>                 | <span data-ttu-id="21142-169">보세요.</span><span class="sxs-lookup"><span data-stu-id="21142-169">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="21142-170">왼쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="21142-170">left-aligned column</span></span>  | <span data-ttu-id="21142-171">오른쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="21142-171">right-aligned column</span></span> | <span data-ttu-id="21142-172">가운데 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="21142-172">centered column</span></span> |
| <span data-ttu-id="21142-173">$100</span><span class="sxs-lookup"><span data-stu-id="21142-173">$100</span></span>                 | <span data-ttu-id="21142-174">$100</span><span class="sxs-lookup"><span data-stu-id="21142-174">$100</span></span>                 | <span data-ttu-id="21142-175">$100</span><span class="sxs-lookup"><span data-stu-id="21142-175">$100</span></span>            |
| <span data-ttu-id="21142-176">$10</span><span class="sxs-lookup"><span data-stu-id="21142-176">$10</span></span>                  | <span data-ttu-id="21142-177">$10</span><span class="sxs-lookup"><span data-stu-id="21142-177">$10</span></span>                  | <span data-ttu-id="21142-178">$10</span><span class="sxs-lookup"><span data-stu-id="21142-178">$10</span></span>             |
| <span data-ttu-id="21142-179">$1</span><span class="sxs-lookup"><span data-stu-id="21142-179">$1</span></span>                   | <span data-ttu-id="21142-180">$1</span><span class="sxs-lookup"><span data-stu-id="21142-180">$1</span></span>                   | <span data-ttu-id="21142-181">$1</span><span class="sxs-lookup"><span data-stu-id="21142-181">$1</span></span>              |

<span data-ttu-id="21142-182">테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21142-182">For more information on creating tables, see:</span></span>

- <span data-ttu-id="21142-183">넓은 테이블의 서식을 지정하는 데 도움이 되는 Markdig [테이블 래핑 기능](#table-wrapping)</span><span class="sxs-lookup"><span data-stu-id="21142-183">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="21142-184">GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="21142-184">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="21142-185">[Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱</span><span class="sxs-lookup"><span data-stu-id="21142-185">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="21142-186">[Adam Pritchard의 Markdown 참고 자료](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="21142-186">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="21142-187">[Michel Fortin의 Markdown 추가 자료](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="21142-187">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="21142-188">[HTML 테이블을 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="21142-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="21142-189">링크</span><span class="sxs-lookup"><span data-stu-id="21142-189">Links</span></span>

<span data-ttu-id="21142-190">인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-190">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="21142-191">연결에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21142-191">For more information on linking, see:</span></span>

- <span data-ttu-id="21142-192">Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)</span><span class="sxs-lookup"><span data-stu-id="21142-192">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="21142-193">이 가이드의 [링크](how-to-write-links.md) 페이지에 Markdig에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-193">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="21142-194">코드 조각</span><span class="sxs-lookup"><span data-stu-id="21142-194">Code snippets</span></span>

<span data-ttu-id="21142-195">Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-195">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="21142-196">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21142-196">For details, see:</span></span>

- [<span data-ttu-id="21142-197">코드 블록에 대한 Markdown의 네이티브 지원</span><span class="sxs-lookup"><span data-stu-id="21142-197">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="21142-198">코드 펜싱 및 구문 강조 표시에 대한 GFM 지원</span><span class="sxs-lookup"><span data-stu-id="21142-198">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="21142-199">펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-199">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="21142-200">펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-200">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="21142-201">처음 세 개의 \` 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-201">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="21142-202">Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-202">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="21142-203">이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-203">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="21142-204">이름</span><span class="sxs-lookup"><span data-stu-id="21142-204">Name</span></span>|<span data-ttu-id="21142-205">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="21142-205">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="21142-206">.NET 콘솔</span><span class="sxs-lookup"><span data-stu-id="21142-206">.NET Console</span></span>|<span data-ttu-id="21142-207">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="21142-207">dotnetcli</span></span>|
|<span data-ttu-id="21142-208">ASP.NET(C#)</span><span class="sxs-lookup"><span data-stu-id="21142-208">ASP.NET (C#)</span></span>|<span data-ttu-id="21142-209">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="21142-209">aspx-csharp</span></span>|
|<span data-ttu-id="21142-210">ASP.NET(VB)</span><span class="sxs-lookup"><span data-stu-id="21142-210">ASP.NET (VB)</span></span>|<span data-ttu-id="21142-211">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="21142-211">aspx-vb</span></span>|
|<span data-ttu-id="21142-212">AzCopy</span><span class="sxs-lookup"><span data-stu-id="21142-212">AzCopy</span></span>|<span data-ttu-id="21142-213">azcopy</span><span class="sxs-lookup"><span data-stu-id="21142-213">azcopy</span></span>|
|<span data-ttu-id="21142-214">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="21142-214">Azure CLI</span></span>|<span data-ttu-id="21142-215">azurecli</span><span class="sxs-lookup"><span data-stu-id="21142-215">azurecli</span></span>|
|<span data-ttu-id="21142-216">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="21142-216">Azure PowerShell</span></span>|<span data-ttu-id="21142-217">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="21142-217">azurepowershell</span></span>|
|<span data-ttu-id="21142-218">C++</span><span class="sxs-lookup"><span data-stu-id="21142-218">C++</span></span>|<span data-ttu-id="21142-219">cpp</span><span class="sxs-lookup"><span data-stu-id="21142-219">cpp</span></span>|
|<span data-ttu-id="21142-220">C++/CX</span><span class="sxs-lookup"><span data-stu-id="21142-220">C++/CX</span></span>|<span data-ttu-id="21142-221">cppcx</span><span class="sxs-lookup"><span data-stu-id="21142-221">cppcx</span></span>|
|<span data-ttu-id="21142-222">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="21142-222">C++/WinRT</span></span>|<span data-ttu-id="21142-223">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="21142-223">cppwinrt</span></span>|
|<span data-ttu-id="21142-224">C#</span><span class="sxs-lookup"><span data-stu-id="21142-224">C#</span></span>|<span data-ttu-id="21142-225">csharp</span><span class="sxs-lookup"><span data-stu-id="21142-225">csharp</span></span>|
|<span data-ttu-id="21142-226">브라우저의 C#</span><span class="sxs-lookup"><span data-stu-id="21142-226">C# in browser</span></span>|<span data-ttu-id="21142-227">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="21142-227">csharp-interactive</span></span>|
|<span data-ttu-id="21142-228">콘솔</span><span class="sxs-lookup"><span data-stu-id="21142-228">Console</span></span>|<span data-ttu-id="21142-229">콘솔</span><span class="sxs-lookup"><span data-stu-id="21142-229">console</span></span>|
|<span data-ttu-id="21142-230">CSHTML</span><span class="sxs-lookup"><span data-stu-id="21142-230">CSHTML</span></span>|<span data-ttu-id="21142-231">cshtml</span><span class="sxs-lookup"><span data-stu-id="21142-231">cshtml</span></span>|
|<span data-ttu-id="21142-232">DAX</span><span class="sxs-lookup"><span data-stu-id="21142-232">DAX</span></span>|<span data-ttu-id="21142-233">dax</span><span class="sxs-lookup"><span data-stu-id="21142-233">dax</span></span>|
|<span data-ttu-id="21142-234">Docker</span><span class="sxs-lookup"><span data-stu-id="21142-234">Docker</span></span>|<span data-ttu-id="21142-235">dockerfile</span><span class="sxs-lookup"><span data-stu-id="21142-235">dockerfile</span></span>|
|<span data-ttu-id="21142-236">F#</span><span class="sxs-lookup"><span data-stu-id="21142-236">F#</span></span>|<span data-ttu-id="21142-237">fsharp</span><span class="sxs-lookup"><span data-stu-id="21142-237">fsharp</span></span>|
|<span data-ttu-id="21142-238">Go</span><span class="sxs-lookup"><span data-stu-id="21142-238">Go</span></span>|<span data-ttu-id="21142-239">go</span><span class="sxs-lookup"><span data-stu-id="21142-239">go</span></span>|
|<span data-ttu-id="21142-240">HTML</span><span class="sxs-lookup"><span data-stu-id="21142-240">HTML</span></span>|<span data-ttu-id="21142-241">html</span><span class="sxs-lookup"><span data-stu-id="21142-241">html</span></span>|
|<span data-ttu-id="21142-242">HTTP</span><span class="sxs-lookup"><span data-stu-id="21142-242">HTTP</span></span>|<span data-ttu-id="21142-243">http</span><span class="sxs-lookup"><span data-stu-id="21142-243">http</span></span>|
|<span data-ttu-id="21142-244">Java</span><span class="sxs-lookup"><span data-stu-id="21142-244">Java</span></span>|<span data-ttu-id="21142-245">java</span><span class="sxs-lookup"><span data-stu-id="21142-245">java</span></span>|
|<span data-ttu-id="21142-246">JavaScript</span><span class="sxs-lookup"><span data-stu-id="21142-246">JavaScript</span></span>|<span data-ttu-id="21142-247">javascript</span><span class="sxs-lookup"><span data-stu-id="21142-247">javascript</span></span>|
|<span data-ttu-id="21142-248">JSON</span><span class="sxs-lookup"><span data-stu-id="21142-248">JSON</span></span>|<span data-ttu-id="21142-249">json</span><span class="sxs-lookup"><span data-stu-id="21142-249">json</span></span>|
|<span data-ttu-id="21142-250">Kusto 쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="21142-250">Kusto Query Language</span></span>|<span data-ttu-id="21142-251">kusto</span><span class="sxs-lookup"><span data-stu-id="21142-251">kusto</span></span>|
|<span data-ttu-id="21142-252">Markdown</span><span class="sxs-lookup"><span data-stu-id="21142-252">Markdown</span></span>|<span data-ttu-id="21142-253">md</span><span class="sxs-lookup"><span data-stu-id="21142-253">md</span></span>|
|<span data-ttu-id="21142-254">Objective-C</span><span class="sxs-lookup"><span data-stu-id="21142-254">Objective-C</span></span>|<span data-ttu-id="21142-255">objc</span><span class="sxs-lookup"><span data-stu-id="21142-255">objc</span></span>|
|<span data-ttu-id="21142-256">OData</span><span class="sxs-lookup"><span data-stu-id="21142-256">OData</span></span>|<span data-ttu-id="21142-257">odata</span><span class="sxs-lookup"><span data-stu-id="21142-257">odata</span></span>|
|<span data-ttu-id="21142-258">PHP</span><span class="sxs-lookup"><span data-stu-id="21142-258">PHP</span></span>|<span data-ttu-id="21142-259">php</span><span class="sxs-lookup"><span data-stu-id="21142-259">php</span></span>|
|<span data-ttu-id="21142-260">PowerApps(점 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="21142-260">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="21142-261">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="21142-261">powerapps-dot</span></span>|
|<span data-ttu-id="21142-262">PowerApps(쉼표 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="21142-262">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="21142-263">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="21142-263">powerapps-comma</span></span>|
|<span data-ttu-id="21142-264">PowerShell</span><span class="sxs-lookup"><span data-stu-id="21142-264">PowerShell</span></span>|<span data-ttu-id="21142-265">powershell</span><span class="sxs-lookup"><span data-stu-id="21142-265">powershell</span></span>|
|<span data-ttu-id="21142-266">Python</span><span class="sxs-lookup"><span data-stu-id="21142-266">Python</span></span>|<span data-ttu-id="21142-267">python</span><span class="sxs-lookup"><span data-stu-id="21142-267">python</span></span>|
|<span data-ttu-id="21142-268">Q#</span><span class="sxs-lookup"><span data-stu-id="21142-268">Q#</span></span>|<span data-ttu-id="21142-269">qsharp</span><span class="sxs-lookup"><span data-stu-id="21142-269">qsharp</span></span>|
|<span data-ttu-id="21142-270">R</span><span class="sxs-lookup"><span data-stu-id="21142-270">R</span></span>|<span data-ttu-id="21142-271">r</span><span class="sxs-lookup"><span data-stu-id="21142-271">r</span></span>|
|<span data-ttu-id="21142-272">Ruby</span><span class="sxs-lookup"><span data-stu-id="21142-272">Ruby</span></span>|<span data-ttu-id="21142-273">ruby</span><span class="sxs-lookup"><span data-stu-id="21142-273">ruby</span></span>|
|<span data-ttu-id="21142-274">SQL</span><span class="sxs-lookup"><span data-stu-id="21142-274">SQL</span></span>|<span data-ttu-id="21142-275">sql</span><span class="sxs-lookup"><span data-stu-id="21142-275">sql</span></span>|
|<span data-ttu-id="21142-276">Swift</span><span class="sxs-lookup"><span data-stu-id="21142-276">Swift</span></span>|<span data-ttu-id="21142-277">swift</span><span class="sxs-lookup"><span data-stu-id="21142-277">swift</span></span>|
|<span data-ttu-id="21142-278">TypeScript</span><span class="sxs-lookup"><span data-stu-id="21142-278">TypeScript</span></span>|<span data-ttu-id="21142-279">typescript</span><span class="sxs-lookup"><span data-stu-id="21142-279">typescript</span></span>|
|<span data-ttu-id="21142-280">VB</span><span class="sxs-lookup"><span data-stu-id="21142-280">VB</span></span>|<span data-ttu-id="21142-281">vb</span><span class="sxs-lookup"><span data-stu-id="21142-281">vb</span></span>|
|<span data-ttu-id="21142-282">XAML</span><span class="sxs-lookup"><span data-stu-id="21142-282">XAML</span></span>|<span data-ttu-id="21142-283">xaml</span><span class="sxs-lookup"><span data-stu-id="21142-283">xaml</span></span>|
|<span data-ttu-id="21142-284">XML</span><span class="sxs-lookup"><span data-stu-id="21142-284">XML</span></span>|<span data-ttu-id="21142-285">xml</span><span class="sxs-lookup"><span data-stu-id="21142-285">xml</span></span>|

<span data-ttu-id="21142-286">`csharp-interactive` 이름은 C# 언어와 브라우저에서 샘플을 실행하는 기능을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-286">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="21142-287">이러한 코드 조각은 Docker 컨테이너에서 컴파일되고 실행되며, 해당 프로그램 실행 결과는 사용자의 브라우저 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-287">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="21142-288">예제: C\#</span><span class="sxs-lookup"><span data-stu-id="21142-288">Example: C\#</span></span>

<span data-ttu-id="21142-289">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="21142-289">__Markdown__</span></span>

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

<span data-ttu-id="21142-290">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="21142-290">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="21142-291">예제: SQL</span><span class="sxs-lookup"><span data-stu-id="21142-291">Example: SQL</span></span>

<span data-ttu-id="21142-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="21142-292">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="21142-293">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="21142-293">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="21142-294">OPS 사용자 지정 Markdown 확장</span><span class="sxs-lookup"><span data-stu-id="21142-294">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="21142-295">OPS(Open Publishing Services)는 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-295">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="21142-296">Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-296">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="21142-297">이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-297">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="21142-298">(예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="21142-298">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="21142-299">Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-299">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="21142-300">더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-300">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="21142-301">참고 블록</span><span class="sxs-lookup"><span data-stu-id="21142-301">Note blocks</span></span>
- <span data-ttu-id="21142-302">포함 파일</span><span class="sxs-lookup"><span data-stu-id="21142-302">Include files</span></span>
- <span data-ttu-id="21142-303">선택기</span><span class="sxs-lookup"><span data-stu-id="21142-303">Selectors</span></span>
- <span data-ttu-id="21142-304">포함된 비디오</span><span class="sxs-lookup"><span data-stu-id="21142-304">Embedded videos</span></span>
- <span data-ttu-id="21142-305">코드 조각/샘플</span><span class="sxs-lookup"><span data-stu-id="21142-305">Code snippets/samples</span></span>

<span data-ttu-id="21142-306">전체 목록은 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21142-306">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="21142-307">참고 블록</span><span class="sxs-lookup"><span data-stu-id="21142-307">Note blocks</span></span>

<span data-ttu-id="21142-308">특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-308">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="21142-309">참고</span><span class="sxs-lookup"><span data-stu-id="21142-309">NOTE</span></span>
- <span data-ttu-id="21142-310">경고</span><span class="sxs-lookup"><span data-stu-id="21142-310">WARNING</span></span>
- <span data-ttu-id="21142-311">팁</span><span class="sxs-lookup"><span data-stu-id="21142-311">TIP</span></span>
- <span data-ttu-id="21142-312">중요</span><span class="sxs-lookup"><span data-stu-id="21142-312">IMPORTANT</span></span>

<span data-ttu-id="21142-313">일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-313">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="21142-314">참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-314">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="21142-315">예제:</span><span class="sxs-lookup"><span data-stu-id="21142-315">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="21142-316">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-316">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="21142-317">참고입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-317">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="21142-318">경고입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-318">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="21142-319">팁입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-319">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21142-320">중요합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-320">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="21142-321">포함 파일</span><span class="sxs-lookup"><span data-stu-id="21142-321">Include files</span></span>

<span data-ttu-id="21142-322">문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는 내용" 파일에 대한 참조를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-322">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="21142-323">이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21142-323">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="21142-324">콘텐츠를 재사용하기 위해 사용 가능한 포함되는 참조에는 3가지 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-324">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="21142-325">인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-325">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="21142-326">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-326">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="21142-327">이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-327">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="21142-328">인라인 또는 블록에 포함되는 파일은 간단한 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-328">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="21142-329">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-329">It can contain any valid Markdown.</span></span> <span data-ttu-id="21142-330">포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-330">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="21142-331">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-331">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="21142-332">포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-332">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="21142-333">여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-333">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="21142-334">블록에 포함되는 파일은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-334">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="21142-335">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-335">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="21142-336">포함되는 참조는 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-336">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="21142-337">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-337">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="21142-338">포함되는 파일의 모든 텍스트가 문서에서 포함되는 파일을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-338">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="21142-339">이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21142-339">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="21142-340">다른 포함되는 파일 내에 포함되는 참조를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-340">Don't embed include references within other include files.</span></span> <span data-ttu-id="21142-341">지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-341">They are not supported.</span></span>
- <span data-ttu-id="21142-342">미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더).</span><span class="sxs-lookup"><span data-stu-id="21142-342">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="21142-343">미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-343">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="21142-344">포함되는 파일에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-344">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="21142-345">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-345">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="21142-346">포함되는 파일 및 문서 각각에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-346">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="21142-347">포함되는 파일과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-347">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="21142-348">포함되는 파일을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-348">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="21142-349">포함되는 파일은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-349">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="21142-350">예제:</span><span class="sxs-lookup"><span data-stu-id="21142-350">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="21142-351">선택기</span><span class="sxs-lookup"><span data-stu-id="21142-351">Selectors</span></span>

<span data-ttu-id="21142-352">동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼 간의 구현 차이를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-352">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="21142-353">이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-353">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="21142-354">Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-354">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="21142-355">동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기를 포함되는 파일에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-355">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="21142-356">그런 다음, 동일한 선택기를 사용하는 모든 문서에서 포함되는 해당 파일을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-356">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="21142-357">다음은 예제 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-357">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="21142-358">[Azure 문서](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)에서 실행 중인 선택기의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-358">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="21142-359">코드에 포함되는 참조</span><span class="sxs-lookup"><span data-stu-id="21142-359">Code include references</span></span>

<span data-ttu-id="21142-360">Markdig은 해당 코드 조각 확장을 통해 문서에 대한 고급 코드 포함 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-360">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="21142-361">이 기능은 프로그래밍 언어 선택과 구문 색 지정 및 다음과 같은 멋진 기능을 기반으로 하는 GFM 기능에서 빌드하는 고급 렌더링을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-361">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="21142-362">외부 리포지토리에서 중앙 집중식 코드 샘플/코드 조각 포함</span><span class="sxs-lookup"><span data-stu-id="21142-362">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="21142-363">다른 언어로 여러 버전의 코드 샘플을 표시하는 탭 UI</span><span class="sxs-lookup"><span data-stu-id="21142-363">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="21142-364">과제 및 문제 해결</span><span class="sxs-lookup"><span data-stu-id="21142-364">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="21142-365">대체 텍스트</span><span class="sxs-lookup"><span data-stu-id="21142-365">Alt text</span></span>

<span data-ttu-id="21142-366">밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-366">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="21142-367">예를 들어 아래 텍스트를 사용하는 대신</span><span class="sxs-lookup"><span data-stu-id="21142-367">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="21142-368">다음과 같이 밑줄을 이스케이프 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-368">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="21142-369">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="21142-369">Apostrophes and quotation marks</span></span>

<span data-ttu-id="21142-370">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21142-370">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="21142-371">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-371">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="21142-372">그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="21142-372">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="21142-373">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-373">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="21142-374">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="21142-374">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="21142-375">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="21142-375">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="21142-376">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="21142-376">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="21142-377">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="21142-377">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="21142-378">대괄호</span><span class="sxs-lookup"><span data-stu-id="21142-378">Angle brackets</span></span>

<span data-ttu-id="21142-379">자리 표시자를 나타내는 데 대괄호를 사용하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="21142-379">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="21142-380">텍스트(코드 아님)에서 이 작업을 수행할 때는 대괄호를 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-380">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="21142-381">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-381">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="21142-382">예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="21142-382">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="21142-383">참고 항목:</span><span class="sxs-lookup"><span data-stu-id="21142-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="21142-384">Markdown 리소스</span><span class="sxs-lookup"><span data-stu-id="21142-384">Markdown resources</span></span>

- [<span data-ttu-id="21142-385">Markdown 소개</span><span class="sxs-lookup"><span data-stu-id="21142-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="21142-386">Docs Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="21142-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="21142-387">GitHub의 Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="21142-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="21142-388">Markdown 가이드</span><span class="sxs-lookup"><span data-stu-id="21142-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
