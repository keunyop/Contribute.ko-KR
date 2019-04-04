---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
ms.date: 03/26/2019
ms.openlocfilehash: eeb49961fbf530676b55ae4e42d4fca7b8d7edf7
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637486"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="a6715-103">Markdown을 사용하여 Docs를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a6715-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="a6715-104">[Docs.microsoft.com](http://docs.microsoft.com) 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="a6715-105">그렇기 때문에 신속하게 산업 표준이 되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="a6715-106">문서 사이트는 Markdown의 [Markdig 유형](#markdown-flavor)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="a6715-107">Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="a6715-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="a6715-108">제목</span><span class="sxs-lookup"><span data-stu-id="a6715-108">Headings</span></span>

<span data-ttu-id="a6715-109">제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="a6715-110">제목은 atx-style을 사용하여 수행해야 합니다. 즉, 줄의 시작 부분에 1-6 해시 문자(#)를 사용하여 HTML 제목 수준 H1~H6에 해당하는 제목을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="a6715-111">위의 1~4번째 수준 헤더의 예가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="a6715-112">항목에는 첫 번째 수준 제목(H1)이 하나만 **있어야 하며**, 해당 페이지 제목으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="a6715-113">제목이 `#` 문자로 끝나는 경우 제목을 올바르게 랜더링하려면 끝에 나머지 `#` 문자를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="a6715-114">예: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="a6715-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="a6715-115">두 번째 수준 제목은 해당 페이지 제목 아래의 “이 문서의 내용” 섹션에 나타나는 해당 페이지의 TOC를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="a6715-116">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="a6715-116">Bold and italic text</span></span>

<span data-ttu-id="a6715-117">텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="a6715-118">텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="a6715-119">텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="a6715-120">Blockquotes</span><span class="sxs-lookup"><span data-stu-id="a6715-120">Blockquotes</span></span>

<span data-ttu-id="a6715-121">Blockquotes는 `>` 문자를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-121">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="a6715-122">앞의 예는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="a6715-123">가뭄은 지금 천만년 동안 지속되었고 끔찍한 도마뱀의 통치는 끝난 지 오래되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="a6715-124">언젠가 아프리카로 알려질 이 적도에서 생존을 위한 투쟁은 새로운 격렬한 절정에 이르렀고, 승자는 아직 보이지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="a6715-125">이 황량하고 메마른 땅에서는 작고 빠르거나 사나운 존재만이 번성하거나 생존할 수 있을 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="a6715-126">목록</span><span class="sxs-lookup"><span data-stu-id="a6715-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="a6715-127">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="a6715-127">Unordered list</span></span>

<span data-ttu-id="a6715-128">정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="a6715-129">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="a6715-129">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="a6715-130">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-130">will be rendered as:</span></span>

- <span data-ttu-id="a6715-131">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="a6715-131">List item 1</span></span>
- <span data-ttu-id="a6715-132">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="a6715-132">List item 2</span></span>
- <span data-ttu-id="a6715-133">목록 항목 3</span><span class="sxs-lookup"><span data-stu-id="a6715-133">List item 3</span></span>

<span data-ttu-id="a6715-134">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="a6715-135">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="a6715-135">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="a6715-136">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-136">will be rendered as:</span></span>

- <span data-ttu-id="a6715-137">목록 항목 1</span><span class="sxs-lookup"><span data-stu-id="a6715-137">List item 1</span></span>
  - <span data-ttu-id="a6715-138">목록 항목 A</span><span class="sxs-lookup"><span data-stu-id="a6715-138">List item A</span></span>
  - <span data-ttu-id="a6715-139">목록 항목 B</span><span class="sxs-lookup"><span data-stu-id="a6715-139">List item B</span></span>
- <span data-ttu-id="a6715-140">목록 항목 2</span><span class="sxs-lookup"><span data-stu-id="a6715-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="a6715-141">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="a6715-141">Ordered list</span></span>

<span data-ttu-id="a6715-142">정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="a6715-143">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="a6715-143">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="a6715-144">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-144">will be rendered as:</span></span>

1. <span data-ttu-id="a6715-145">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-145">First instruction</span></span>
2. <span data-ttu-id="a6715-146">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-146">Second instruction</span></span>
3. <span data-ttu-id="a6715-147">세 번째 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-147">Third instruction</span></span>

<span data-ttu-id="a6715-148">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="a6715-149">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="a6715-149">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="a6715-150">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-150">will be rendered as:</span></span>

1. <span data-ttu-id="a6715-151">첫 번째 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-151">First instruction</span></span>
   1. <span data-ttu-id="a6715-152">하위 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-152">Sub-instruction</span></span>
   2. <span data-ttu-id="a6715-153">하위 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-153">Sub-instruction</span></span>
2. <span data-ttu-id="a6715-154">두 번째 지침</span><span class="sxs-lookup"><span data-stu-id="a6715-154">Second instruction</span></span>

<span data-ttu-id="a6715-155">'1'을</span><span class="sxs-lookup"><span data-stu-id="a6715-155">Note that we use '1.'</span></span> <span data-ttu-id="a6715-156">모든 항목에 대해 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-156">for all entries.</span></span> <span data-ttu-id="a6715-157">최신 업데이트에 새 단계가 포함되거나 기존 단계가 제거될 때 더 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="a6715-158">보세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-158">Tables</span></span>

<span data-ttu-id="a6715-159">테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="a6715-160">파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="a6715-161">하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="a6715-162">테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="a6715-163">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="a6715-163">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="a6715-164">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-164">will be rendered as:</span></span>

| <span data-ttu-id="a6715-165">테이블을</span><span class="sxs-lookup"><span data-stu-id="a6715-165">Fun</span></span>                  | <span data-ttu-id="a6715-166">사용해</span><span class="sxs-lookup"><span data-stu-id="a6715-166">With</span></span>                 | <span data-ttu-id="a6715-167">보세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="a6715-168">왼쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="a6715-168">left-aligned column</span></span>  | <span data-ttu-id="a6715-169">오른쪽 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="a6715-169">right-aligned column</span></span> | <span data-ttu-id="a6715-170">가운데 정렬된 열</span><span class="sxs-lookup"><span data-stu-id="a6715-170">centered column</span></span> |
| <span data-ttu-id="a6715-171">$100</span><span class="sxs-lookup"><span data-stu-id="a6715-171">$100</span></span>                 | <span data-ttu-id="a6715-172">$100</span><span class="sxs-lookup"><span data-stu-id="a6715-172">$100</span></span>                 | <span data-ttu-id="a6715-173">$100</span><span class="sxs-lookup"><span data-stu-id="a6715-173">$100</span></span>            |
| <span data-ttu-id="a6715-174">$10</span><span class="sxs-lookup"><span data-stu-id="a6715-174">$10</span></span>                  | <span data-ttu-id="a6715-175">$10</span><span class="sxs-lookup"><span data-stu-id="a6715-175">$10</span></span>                  | <span data-ttu-id="a6715-176">$10</span><span class="sxs-lookup"><span data-stu-id="a6715-176">$10</span></span>             |
| <span data-ttu-id="a6715-177">$1</span><span class="sxs-lookup"><span data-stu-id="a6715-177">$1</span></span>                   | <span data-ttu-id="a6715-178">$1</span><span class="sxs-lookup"><span data-stu-id="a6715-178">$1</span></span>                   | <span data-ttu-id="a6715-179">$1</span><span class="sxs-lookup"><span data-stu-id="a6715-179">$1</span></span>              |

<span data-ttu-id="a6715-180">테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="a6715-181">GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="a6715-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="a6715-182">[Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱</span><span class="sxs-lookup"><span data-stu-id="a6715-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="a6715-183">[Adam Pritchard의 Markdown 참고 자료](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="a6715-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="a6715-184">[Michel Fortin의 Markdown 추가 자료](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="a6715-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="a6715-185">[HTML 테이블을 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="a6715-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="a6715-186">링크</span><span class="sxs-lookup"><span data-stu-id="a6715-186">Links</span></span>

<span data-ttu-id="a6715-187">인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="a6715-188">연결에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-188">For more information on linking, see:</span></span>

- <span data-ttu-id="a6715-189">Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)</span><span class="sxs-lookup"><span data-stu-id="a6715-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="a6715-190">이 가이드의 [링크](how-to-write-links.md) 페이지에 Markdig에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="a6715-191">코드 조각</span><span class="sxs-lookup"><span data-stu-id="a6715-191">Code snippets</span></span>

<span data-ttu-id="a6715-192">Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="a6715-193">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-193">For details, see:</span></span>

- [<span data-ttu-id="a6715-194">코드 블록에 대한 Markdown의 네이티브 지원</span><span class="sxs-lookup"><span data-stu-id="a6715-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="a6715-195">코드 펜싱 및 구문 강조 표시에 대한 GFM 지원</span><span class="sxs-lookup"><span data-stu-id="a6715-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="a6715-196">펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="a6715-197">펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="a6715-198">처음 세 개의 \` 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="a6715-199">Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="a6715-200">이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="a6715-201">이름</span><span class="sxs-lookup"><span data-stu-id="a6715-201">Name</span></span>|<span data-ttu-id="a6715-202">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="a6715-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="a6715-203">.NET 콘솔</span><span class="sxs-lookup"><span data-stu-id="a6715-203">.NET Console</span></span>|<span data-ttu-id="a6715-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="a6715-204">dotnetcli</span></span>|
|<span data-ttu-id="a6715-205">ASP.NET(C#)</span><span class="sxs-lookup"><span data-stu-id="a6715-205">ASP.NET (C#)</span></span>|<span data-ttu-id="a6715-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="a6715-206">aspx-csharp</span></span>|
|<span data-ttu-id="a6715-207">ASP.NET(VB)</span><span class="sxs-lookup"><span data-stu-id="a6715-207">ASP.NET (VB)</span></span>|<span data-ttu-id="a6715-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="a6715-208">aspx-vb</span></span>|
|<span data-ttu-id="a6715-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="a6715-209">AzCopy</span></span>|<span data-ttu-id="a6715-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="a6715-210">azcopy</span></span>|
|<span data-ttu-id="a6715-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="a6715-211">Azure CLI</span></span>|<span data-ttu-id="a6715-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="a6715-212">azurecli</span></span>|
|<span data-ttu-id="a6715-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6715-213">Azure PowerShell</span></span>|<span data-ttu-id="a6715-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="a6715-214">azurepowershell</span></span>|
|<span data-ttu-id="a6715-215">Bash</span><span class="sxs-lookup"><span data-stu-id="a6715-215">Bash</span></span>|<span data-ttu-id="a6715-216">bash</span><span class="sxs-lookup"><span data-stu-id="a6715-216">bash</span></span>|
|<span data-ttu-id="a6715-217">C++</span><span class="sxs-lookup"><span data-stu-id="a6715-217">C++</span></span>|<span data-ttu-id="a6715-218">cpp</span><span class="sxs-lookup"><span data-stu-id="a6715-218">cpp</span></span>|
|<span data-ttu-id="a6715-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="a6715-219">C++/CX</span></span>|<span data-ttu-id="a6715-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="a6715-220">cppcx</span></span>|
|<span data-ttu-id="a6715-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="a6715-221">C++/WinRT</span></span>|<span data-ttu-id="a6715-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="a6715-222">cppwinrt</span></span>|
|<span data-ttu-id="a6715-223">C#</span><span class="sxs-lookup"><span data-stu-id="a6715-223">C#</span></span>|<span data-ttu-id="a6715-224">csharp</span><span class="sxs-lookup"><span data-stu-id="a6715-224">csharp</span></span>|
|<span data-ttu-id="a6715-225">브라우저의 C#</span><span class="sxs-lookup"><span data-stu-id="a6715-225">C# in browser</span></span>|<span data-ttu-id="a6715-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="a6715-226">csharp-interactive</span></span>|
|<span data-ttu-id="a6715-227">콘솔</span><span class="sxs-lookup"><span data-stu-id="a6715-227">Console</span></span>|<span data-ttu-id="a6715-228">콘솔</span><span class="sxs-lookup"><span data-stu-id="a6715-228">console</span></span>|
|<span data-ttu-id="a6715-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="a6715-229">CSHTML</span></span>|<span data-ttu-id="a6715-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="a6715-230">cshtml</span></span>|
|<span data-ttu-id="a6715-231">DAX</span><span class="sxs-lookup"><span data-stu-id="a6715-231">DAX</span></span>|<span data-ttu-id="a6715-232">dax</span><span class="sxs-lookup"><span data-stu-id="a6715-232">dax</span></span>|
|<span data-ttu-id="a6715-233">Docker</span><span class="sxs-lookup"><span data-stu-id="a6715-233">Docker</span></span>|<span data-ttu-id="a6715-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="a6715-234">dockerfile</span></span>|
|<span data-ttu-id="a6715-235">F#</span><span class="sxs-lookup"><span data-stu-id="a6715-235">F#</span></span>|<span data-ttu-id="a6715-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="a6715-236">fsharp</span></span>|
|<span data-ttu-id="a6715-237">Go</span><span class="sxs-lookup"><span data-stu-id="a6715-237">Go</span></span>|<span data-ttu-id="a6715-238">go</span><span class="sxs-lookup"><span data-stu-id="a6715-238">go</span></span>|
|<span data-ttu-id="a6715-239">HTML</span><span class="sxs-lookup"><span data-stu-id="a6715-239">HTML</span></span>|<span data-ttu-id="a6715-240">html</span><span class="sxs-lookup"><span data-stu-id="a6715-240">html</span></span>|
|<span data-ttu-id="a6715-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="a6715-241">HTTP</span></span>|<span data-ttu-id="a6715-242">http</span><span class="sxs-lookup"><span data-stu-id="a6715-242">http</span></span>|
|<span data-ttu-id="a6715-243">Java</span><span class="sxs-lookup"><span data-stu-id="a6715-243">Java</span></span>|<span data-ttu-id="a6715-244">java</span><span class="sxs-lookup"><span data-stu-id="a6715-244">java</span></span>|
|<span data-ttu-id="a6715-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a6715-245">JavaScript</span></span>|<span data-ttu-id="a6715-246">javascript</span><span class="sxs-lookup"><span data-stu-id="a6715-246">javascript</span></span>|
|<span data-ttu-id="a6715-247">JSON</span><span class="sxs-lookup"><span data-stu-id="a6715-247">JSON</span></span>|<span data-ttu-id="a6715-248">json</span><span class="sxs-lookup"><span data-stu-id="a6715-248">json</span></span>|
|<span data-ttu-id="a6715-249">Kusto 쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="a6715-249">Kusto Query Language</span></span>|<span data-ttu-id="a6715-250">kusto</span><span class="sxs-lookup"><span data-stu-id="a6715-250">kusto</span></span>|
|<span data-ttu-id="a6715-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="a6715-251">Markdown</span></span>|<span data-ttu-id="a6715-252">md</span><span class="sxs-lookup"><span data-stu-id="a6715-252">md</span></span>|
|<span data-ttu-id="a6715-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="a6715-253">Objective-C</span></span>|<span data-ttu-id="a6715-254">objc</span><span class="sxs-lookup"><span data-stu-id="a6715-254">objc</span></span>|
|<span data-ttu-id="a6715-255">OData</span><span class="sxs-lookup"><span data-stu-id="a6715-255">OData</span></span>|<span data-ttu-id="a6715-256">odata</span><span class="sxs-lookup"><span data-stu-id="a6715-256">odata</span></span>|
|<span data-ttu-id="a6715-257">PHP</span><span class="sxs-lookup"><span data-stu-id="a6715-257">PHP</span></span>|<span data-ttu-id="a6715-258">php</span><span class="sxs-lookup"><span data-stu-id="a6715-258">php</span></span>|
|<span data-ttu-id="a6715-259">PowerApps(점 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="a6715-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="a6715-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="a6715-260">powerapps-dot</span></span>|
|<span data-ttu-id="a6715-261">PowerApps(쉼표 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="a6715-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="a6715-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="a6715-262">powerapps-comma</span></span>|
|<span data-ttu-id="a6715-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6715-263">PowerShell</span></span>|<span data-ttu-id="a6715-264">powershell</span><span class="sxs-lookup"><span data-stu-id="a6715-264">powershell</span></span>|
|<span data-ttu-id="a6715-265">Python</span><span class="sxs-lookup"><span data-stu-id="a6715-265">Python</span></span>|<span data-ttu-id="a6715-266">python</span><span class="sxs-lookup"><span data-stu-id="a6715-266">python</span></span>|
|<span data-ttu-id="a6715-267">Q#</span><span class="sxs-lookup"><span data-stu-id="a6715-267">Q#</span></span>|<span data-ttu-id="a6715-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="a6715-268">qsharp</span></span>|
|<span data-ttu-id="a6715-269">R</span><span class="sxs-lookup"><span data-stu-id="a6715-269">R</span></span>|<span data-ttu-id="a6715-270">r</span><span class="sxs-lookup"><span data-stu-id="a6715-270">r</span></span>|
|<span data-ttu-id="a6715-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="a6715-271">Ruby</span></span>|<span data-ttu-id="a6715-272">ruby</span><span class="sxs-lookup"><span data-stu-id="a6715-272">ruby</span></span>|
|<span data-ttu-id="a6715-273">SQL</span><span class="sxs-lookup"><span data-stu-id="a6715-273">SQL</span></span>|<span data-ttu-id="a6715-274">sql</span><span class="sxs-lookup"><span data-stu-id="a6715-274">sql</span></span>|
|<span data-ttu-id="a6715-275">Swift</span><span class="sxs-lookup"><span data-stu-id="a6715-275">Swift</span></span>|<span data-ttu-id="a6715-276">swift</span><span class="sxs-lookup"><span data-stu-id="a6715-276">swift</span></span>|
|<span data-ttu-id="a6715-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="a6715-277">TypeScript</span></span>|<span data-ttu-id="a6715-278">typescript</span><span class="sxs-lookup"><span data-stu-id="a6715-278">typescript</span></span>|
|<span data-ttu-id="a6715-279">VB</span><span class="sxs-lookup"><span data-stu-id="a6715-279">VB</span></span>|<span data-ttu-id="a6715-280">vb</span><span class="sxs-lookup"><span data-stu-id="a6715-280">vb</span></span>|
|<span data-ttu-id="a6715-281">XAML</span><span class="sxs-lookup"><span data-stu-id="a6715-281">XAML</span></span>|<span data-ttu-id="a6715-282">xaml</span><span class="sxs-lookup"><span data-stu-id="a6715-282">xaml</span></span>|
|<span data-ttu-id="a6715-283">XML</span><span class="sxs-lookup"><span data-stu-id="a6715-283">XML</span></span>|<span data-ttu-id="a6715-284">xml</span><span class="sxs-lookup"><span data-stu-id="a6715-284">xml</span></span>|

<span data-ttu-id="a6715-285">`csharp-interactive` 이름은 C# 언어와 브라우저에서 샘플을 실행하는 기능을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="a6715-286">이러한 코드 조각은 Docker 컨테이너에서 컴파일되고 실행되며, 해당 프로그램 실행 결과는 사용자의 브라우저 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="a6715-287">예제: C\#</span><span class="sxs-lookup"><span data-stu-id="a6715-287">Example: C\#</span></span>

<span data-ttu-id="a6715-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="a6715-288">__Markdown__</span></span>

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

<span data-ttu-id="a6715-289">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="a6715-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="a6715-290">예제: SQL</span><span class="sxs-lookup"><span data-stu-id="a6715-290">Example: SQL</span></span>

<span data-ttu-id="a6715-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="a6715-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="a6715-292">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="a6715-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="a6715-293">OPS 사용자 지정 Markdown 확장</span><span class="sxs-lookup"><span data-stu-id="a6715-293">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="a6715-294">OPS(Open Publishing Services)는 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-294">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="a6715-295">Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="a6715-296">이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="a6715-297">(예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="a6715-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="a6715-298">Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="a6715-299">더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="a6715-300">참고 블록</span><span class="sxs-lookup"><span data-stu-id="a6715-300">Note blocks</span></span>
- <span data-ttu-id="a6715-301">포함 파일</span><span class="sxs-lookup"><span data-stu-id="a6715-301">Include files</span></span>
- <span data-ttu-id="a6715-302">선택기</span><span class="sxs-lookup"><span data-stu-id="a6715-302">Selectors</span></span>
- <span data-ttu-id="a6715-303">포함된 비디오</span><span class="sxs-lookup"><span data-stu-id="a6715-303">Embedded videos</span></span>
- <span data-ttu-id="a6715-304">코드 조각/샘플</span><span class="sxs-lookup"><span data-stu-id="a6715-304">Code snippets/samples</span></span>

<span data-ttu-id="a6715-305">전체 목록은 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6715-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="a6715-306">참고 블록</span><span class="sxs-lookup"><span data-stu-id="a6715-306">Note blocks</span></span>

<span data-ttu-id="a6715-307">특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="a6715-308">참고</span><span class="sxs-lookup"><span data-stu-id="a6715-308">NOTE</span></span>
- <span data-ttu-id="a6715-309">경고</span><span class="sxs-lookup"><span data-stu-id="a6715-309">WARNING</span></span>
- <span data-ttu-id="a6715-310">팁</span><span class="sxs-lookup"><span data-stu-id="a6715-310">TIP</span></span>
- <span data-ttu-id="a6715-311">중요</span><span class="sxs-lookup"><span data-stu-id="a6715-311">IMPORTANT</span></span>

<span data-ttu-id="a6715-312">일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="a6715-313">참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="a6715-314">예제:</span><span class="sxs-lookup"><span data-stu-id="a6715-314">Examples:</span></span>

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

<span data-ttu-id="a6715-315">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-315">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="a6715-316">참고입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-316">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="a6715-317">경고입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-317">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="a6715-318">팁입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-318">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6715-319">중요합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-319">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="a6715-320">포함 파일</span><span class="sxs-lookup"><span data-stu-id="a6715-320">Include files</span></span>

<span data-ttu-id="a6715-321">문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는 내용" 파일에 대한 참조를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-321">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="a6715-322">이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-322">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="a6715-323">콘텐츠를 재사용하기 위해 사용 가능한 포함되는 참조에는 3가지 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-323">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="a6715-324">인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-324">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="a6715-325">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-325">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="a6715-326">이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-326">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="a6715-327">인라인 또는 블록에 포함되는 파일은 간단한 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-327">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="a6715-328">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-328">It can contain any valid Markdown.</span></span> <span data-ttu-id="a6715-329">포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-329">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="a6715-330">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-330">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="a6715-331">포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-331">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="a6715-332">여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-332">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="a6715-333">블록에 포함되는 파일은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-333">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="a6715-334">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-334">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="a6715-335">포함되는 참조는 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-335">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="a6715-336">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-336">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="a6715-337">포함되는 파일의 모든 텍스트가 문서에서 포함되는 파일을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-337">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="a6715-338">이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-338">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="a6715-339">다른 포함되는 파일 내에 포함되는 참조를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-339">Don't embed include references within other include files.</span></span> <span data-ttu-id="a6715-340">지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-340">They are not supported.</span></span>
- <span data-ttu-id="a6715-341">미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더).</span><span class="sxs-lookup"><span data-stu-id="a6715-341">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="a6715-342">미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-342">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="a6715-343">포함되는 파일에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-343">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="a6715-344">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-344">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="a6715-345">포함되는 파일 및 문서 각각에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-345">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="a6715-346">포함되는 파일과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-346">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="a6715-347">포함되는 파일을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-347">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="a6715-348">포함되는 파일은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-348">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="a6715-349">예제:</span><span class="sxs-lookup"><span data-stu-id="a6715-349">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="a6715-350">선택기</span><span class="sxs-lookup"><span data-stu-id="a6715-350">Selectors</span></span>

<span data-ttu-id="a6715-351">동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼 간의 구현 차이를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-351">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="a6715-352">이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-352">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="a6715-353">Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-353">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="a6715-354">동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기를 포함되는 파일에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-354">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="a6715-355">그런 다음, 동일한 선택기를 사용하는 모든 문서에서 포함되는 해당 파일을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-355">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="a6715-356">다음은 예제 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-356">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="a6715-357">[Azure 문서](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)에서 실행 중인 선택기의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-357">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="a6715-358">코드에 포함되는 참조</span><span class="sxs-lookup"><span data-stu-id="a6715-358">Code include references</span></span>

<span data-ttu-id="a6715-359">Markdig은 해당 코드 조각 확장을 통해 문서에 대한 고급 코드 포함 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-359">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="a6715-360">이 기능은 프로그래밍 언어 선택과 구문 색 지정 및 다음과 같은 멋진 기능을 기반으로 하는 GFM 기능에서 빌드하는 고급 렌더링을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-360">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="a6715-361">외부 리포지토리에서 중앙 집중식 코드 샘플/코드 조각 포함</span><span class="sxs-lookup"><span data-stu-id="a6715-361">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="a6715-362">다른 언어로 여러 버전의 코드 샘플을 표시하는 탭 UI</span><span class="sxs-lookup"><span data-stu-id="a6715-362">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="a6715-363">과제 및 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a6715-363">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="a6715-364">대체 텍스트</span><span class="sxs-lookup"><span data-stu-id="a6715-364">Alt text</span></span>

<span data-ttu-id="a6715-365">밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-365">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="a6715-366">예를 들어 아래 텍스트를 사용하는 대신</span><span class="sxs-lookup"><span data-stu-id="a6715-366">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="a6715-367">다음과 같이 밑줄을 이스케이프 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-367">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="a6715-368">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="a6715-368">Apostrophes and quotation marks</span></span>

<span data-ttu-id="a6715-369">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-369">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="a6715-370">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-370">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="a6715-371">그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="a6715-371">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="a6715-372">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-372">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="a6715-373">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="a6715-373">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="a6715-374">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="a6715-374">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="a6715-375">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="a6715-375">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="a6715-376">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="a6715-376">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="a6715-377">대괄호</span><span class="sxs-lookup"><span data-stu-id="a6715-377">Angle brackets</span></span>

<span data-ttu-id="a6715-378">자리 표시자를 나타내는 데 대괄호를 사용하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-378">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="a6715-379">텍스트(코드 아님)에서 이 작업을 수행할 때는 대괄호를 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-379">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="a6715-380">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-380">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="a6715-381">예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-381">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="a6715-382">Markdown 유형</span><span class="sxs-lookup"><span data-stu-id="a6715-382">Markdown flavor</span></span>

<span data-ttu-id="a6715-383">docs.microsoft.com 사이트 백 엔드는 [Markdig](https://github.com/lunet-io/markdig) 구문 분석 엔진을 통해 구문 분석되는 [CommonMark](https://commonmark.org/) 규격 markdown을 지원하는 OPS(Open Publishing Services)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-383">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="a6715-384">해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-384">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="a6715-385">추가 기능은 Markdown 확장을 통해 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6715-385">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6715-386">참고 항목:</span><span class="sxs-lookup"><span data-stu-id="a6715-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="a6715-387">Markdown 리소스</span><span class="sxs-lookup"><span data-stu-id="a6715-387">Markdown resources</span></span>

- [<span data-ttu-id="a6715-388">Markdown 소개</span><span class="sxs-lookup"><span data-stu-id="a6715-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="a6715-389">Docs Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="a6715-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="a6715-390">GitHub의 Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="a6715-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="a6715-391">Markdown 가이드</span><span class="sxs-lookup"><span data-stu-id="a6715-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
