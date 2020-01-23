---
title: Markdown을 사용하여 Docs를 작성하는 방법
description: 이 문서에서는 docs.microsoft.com 문서를 작성하는 데 사용되는 Markdown 언어에 대한 기본 사항 및 참조 정보를 제공합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111051"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="d7fd3-103">Markdown을 사용하여 Docs를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d7fd3-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="d7fd3-104">[Docs.microsoft.com](https://docs.microsoft.com) 문서는 읽기 쉽고 배우기 쉬운 [Markdown](https://daringfireball.net/projects/markdown/)이라는 가벼운 마크업 언어로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="d7fd3-105">그렇기 때문에 신속하게 산업 표준이 되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="d7fd3-106">문서 사이트는 Markdown의 [Markdig 유형](#markdown-flavor)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="d7fd3-107">Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="d7fd3-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="d7fd3-108">제목</span><span class="sxs-lookup"><span data-stu-id="d7fd3-108">Headings</span></span>

<span data-ttu-id="d7fd3-109">제목을 만들려면 다음과 같이 해시 표시(#)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="d7fd3-110">제목은 atx-style을 사용하여 수행해야 합니다. 즉, 줄의 시작 부분에 1-6 해시 문자(#)를 사용하여 HTML 제목 수준 H1~H6에 해당하는 제목을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="d7fd3-111">위의 1~4번째 수준 헤더의 예가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="d7fd3-112">항목에는 첫 번째 수준 제목(H1)이 하나만 **있어야 하며**, 해당 페이지 제목으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="d7fd3-113">제목이 `#` 문자로 끝나는 경우 제목을 올바르게 랜더링하려면 끝에 나머지 `#` 문자를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="d7fd3-114">예: `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="d7fd3-115">두 번째 수준 제목은 해당 페이지 제목 아래의 “이 문서의 내용” 섹션에 나타나는 해당 페이지의 TOC를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="d7fd3-116">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="d7fd3-116">Bold and italic text</span></span>

<span data-ttu-id="d7fd3-117">텍스트 서식을 **굵게** 지정하려면 두 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="d7fd3-118">텍스트 서식을 *기울임꼴*로 지정하려면 한 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="d7fd3-119">텍스트 서식을 ***굵게 기울임꼴***로 지정하려면 세 개의 별표로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="d7fd3-120">Blockquotes</span><span class="sxs-lookup"><span data-stu-id="d7fd3-120">Blockquotes</span></span>

<span data-ttu-id="d7fd3-121">Blockquotes는 `>` 문자를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="d7fd3-122">앞의 예는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="d7fd3-123">가뭄은 지금 천만년 동안 지속되었고 끔찍한 도마뱀의 통치는 끝난 지 오래되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="d7fd3-124">언젠가 아프리카로 알려질 이 적도에서 생존을 위한 투쟁은 새로운 격렬한 절정에 이르렀고, 승자는 아직 보이지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="d7fd3-125">이 황량하고 메마른 땅에서는 작고 빠르거나 사나운 존재만이 번성하거나 생존할 수 있을 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="d7fd3-126">목록</span><span class="sxs-lookup"><span data-stu-id="d7fd3-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="d7fd3-127">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="d7fd3-127">Unordered list</span></span>

<span data-ttu-id="d7fd3-128">정렬되지 않은/글머리 기호 목록의 형식을 지정하려면 별표나 대시를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="d7fd3-129">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="d7fd3-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="d7fd3-130">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-130">will be rendered as:</span></span>

- <span data-ttu-id="d7fd3-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="d7fd3-131">List item 1</span></span>
- <span data-ttu-id="d7fd3-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="d7fd3-132">List item 2</span></span>
- <span data-ttu-id="d7fd3-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="d7fd3-133">List item 3</span></span>

<span data-ttu-id="d7fd3-134">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d7fd3-135">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="d7fd3-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="d7fd3-136">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-136">will be rendered as:</span></span>

- <span data-ttu-id="d7fd3-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="d7fd3-137">List item 1</span></span>
  - <span data-ttu-id="d7fd3-138">List item A</span><span class="sxs-lookup"><span data-stu-id="d7fd3-138">List item A</span></span>
  - <span data-ttu-id="d7fd3-139">List item B</span><span class="sxs-lookup"><span data-stu-id="d7fd3-139">List item B</span></span>
- <span data-ttu-id="d7fd3-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="d7fd3-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="d7fd3-141">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="d7fd3-141">Ordered list</span></span>

<span data-ttu-id="d7fd3-142">정렬된/단계적인 목록의 형식을 지정하려면 해당하는 숫자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="d7fd3-143">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="d7fd3-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="d7fd3-144">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-144">will be rendered as:</span></span>

1. <span data-ttu-id="d7fd3-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-145">First instruction</span></span>
2. <span data-ttu-id="d7fd3-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-146">Second instruction</span></span>
3. <span data-ttu-id="d7fd3-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-147">Third instruction</span></span>

<span data-ttu-id="d7fd3-148">다른 목록 안에 목록을 중첩하려면 자식 목록 항목을 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d7fd3-149">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="d7fd3-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="d7fd3-150">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-150">will be rendered as:</span></span>

1. <span data-ttu-id="d7fd3-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-151">First instruction</span></span>
   1. <span data-ttu-id="d7fd3-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-152">Sub-instruction</span></span>
   2. <span data-ttu-id="d7fd3-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-153">Sub-instruction</span></span>
2. <span data-ttu-id="d7fd3-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d7fd3-154">Second instruction</span></span>

<span data-ttu-id="d7fd3-155">'1'을</span><span class="sxs-lookup"><span data-stu-id="d7fd3-155">Note that we use '1.'</span></span> <span data-ttu-id="d7fd3-156">모든 항목에 대해 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-156">for all entries.</span></span> <span data-ttu-id="d7fd3-157">최신 업데이트에 새 단계가 포함되거나 기존 단계가 제거될 때 더 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="d7fd3-158">Tables</span><span class="sxs-lookup"><span data-stu-id="d7fd3-158">Tables</span></span>

<span data-ttu-id="d7fd3-159">테이블은 주요 Markdown 사양의 일부가 아니지만 GFM은 테이블을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="d7fd3-160">파이프(|) 및 하이픈(-) 문자를 사용하여 테이블을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="d7fd3-161">하이픈은 각 열의 헤더를 만드는 데 반면 파이프는 각 열을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="d7fd3-162">테이블을 올바르게 렌더링하기 위해 테이블 앞에 빈 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="d7fd3-163">예를 들어 아래 Markdown은</span><span class="sxs-lookup"><span data-stu-id="d7fd3-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d7fd3-164">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-164">Will be rendered as:</span></span>

| <span data-ttu-id="d7fd3-165">Fun</span><span class="sxs-lookup"><span data-stu-id="d7fd3-165">Fun</span></span>                  | <span data-ttu-id="d7fd3-166">With</span><span class="sxs-lookup"><span data-stu-id="d7fd3-166">With</span></span>                 | <span data-ttu-id="d7fd3-167">Tables</span><span class="sxs-lookup"><span data-stu-id="d7fd3-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d7fd3-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d7fd3-168">left-aligned column</span></span>  | <span data-ttu-id="d7fd3-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d7fd3-169">right-aligned column</span></span> | <span data-ttu-id="d7fd3-170">centered column</span><span class="sxs-lookup"><span data-stu-id="d7fd3-170">centered column</span></span> |
| <span data-ttu-id="d7fd3-171">$100</span><span class="sxs-lookup"><span data-stu-id="d7fd3-171">$100</span></span>                 | <span data-ttu-id="d7fd3-172">$100</span><span class="sxs-lookup"><span data-stu-id="d7fd3-172">$100</span></span>                 | <span data-ttu-id="d7fd3-173">$100</span><span class="sxs-lookup"><span data-stu-id="d7fd3-173">$100</span></span>            |
| <span data-ttu-id="d7fd3-174">$10</span><span class="sxs-lookup"><span data-stu-id="d7fd3-174">$10</span></span>                  | <span data-ttu-id="d7fd3-175">$10</span><span class="sxs-lookup"><span data-stu-id="d7fd3-175">$10</span></span>                  | <span data-ttu-id="d7fd3-176">$10</span><span class="sxs-lookup"><span data-stu-id="d7fd3-176">$10</span></span>             |
| <span data-ttu-id="d7fd3-177">$1</span><span class="sxs-lookup"><span data-stu-id="d7fd3-177">$1</span></span>                   | <span data-ttu-id="d7fd3-178">$1</span><span class="sxs-lookup"><span data-stu-id="d7fd3-178">$1</span></span>                   | <span data-ttu-id="d7fd3-179">$1</span><span class="sxs-lookup"><span data-stu-id="d7fd3-179">$1</span></span>              |

<span data-ttu-id="d7fd3-180">테이블을 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="d7fd3-181">GitHub의 [테이블 구성 정보](https://help.github.com/articles/organizing-information-with-tables/)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="d7fd3-182">[Markdown 테이블 생성기](https://www.tablesgenerator.com/markdown_tables) 웹앱</span><span class="sxs-lookup"><span data-stu-id="d7fd3-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="d7fd3-183">[Adam Pritchard의 Markdown 참고 자료](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="d7fd3-184">[Michel Fortin의 Markdown 추가 자료](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="d7fd3-185">[HTML 테이블을 Markdown으로 변환](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="d7fd3-186">링크</span><span class="sxs-lookup"><span data-stu-id="d7fd3-186">Links</span></span>

<span data-ttu-id="d7fd3-187">인라인 링크의 Markdown 구문은 하이퍼링크되는 텍스트인 `[link text]` 부분과 연결되는 URL 또는 파일 이름인 `(file-name.md)` 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="d7fd3-188">연결에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-188">For more information on linking, see:</span></span>

- <span data-ttu-id="d7fd3-189">Markdown의 기반 연결 지원에 대한 자세한 내용은 [Markdown 구문 가이드](https://daringfireball.net/projects/markdown/syntax#link)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="d7fd3-190">이 가이드의 [링크](how-to-write-links.md) 페이지에 Markdig에서 제공하는 추가 연결 구문에 대한 자세한 내용이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="d7fd3-191">코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-191">Code snippets</span></span>

<span data-ttu-id="d7fd3-192">Markdown에서는 코드 조각을 문장에서 인라인으로 배치하거나 문장 사이에 별도의 "Fence" 블록으로 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d7fd3-193">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-193">For details, see:</span></span>

- [<span data-ttu-id="d7fd3-194">코드 블록에 대한 Markdown의 네이티브 지원</span><span class="sxs-lookup"><span data-stu-id="d7fd3-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="d7fd3-195">코드 펜싱 및 구문 강조 표시에 대한 GFM 지원</span><span class="sxs-lookup"><span data-stu-id="d7fd3-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="d7fd3-196">펜싱된 코드 블록은 코드 조각에 대한 구문을 쉽게 강조 표시할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="d7fd3-197">펜싱된 코드 블록에 대한 일반 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="d7fd3-198">처음 세 개의 억음 악센트 기호(\`) 문자 뒤에 있는 별칭은 사용할 구문 강조 표시를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="d7fd3-199">Docs 콘텐츠에서 일반적으로 사용되는 프로그래밍 언어 및 이에 대응되는 레이블에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="d7fd3-200">이러한 언어는 식별 이름을 지원하며, 대부분 언어를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="d7fd3-201">Name</span><span class="sxs-lookup"><span data-stu-id="d7fd3-201">Name</span></span>|<span data-ttu-id="d7fd3-202">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="d7fd3-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="d7fd3-203">.NET 콘솔</span><span class="sxs-lookup"><span data-stu-id="d7fd3-203">.NET Console</span></span>|<span data-ttu-id="d7fd3-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="d7fd3-204">dotnetcli</span></span>|
|<span data-ttu-id="d7fd3-205">ASP.NET(C#)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-205">ASP.NET (C#)</span></span>|<span data-ttu-id="d7fd3-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-206">aspx-csharp</span></span>|
|<span data-ttu-id="d7fd3-207">ASP.NET(VB)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-207">ASP.NET (VB)</span></span>|<span data-ttu-id="d7fd3-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="d7fd3-208">aspx-vb</span></span>|
|<span data-ttu-id="d7fd3-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="d7fd3-209">AzCopy</span></span>|<span data-ttu-id="d7fd3-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="d7fd3-210">azcopy</span></span>|
|<span data-ttu-id="d7fd3-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d7fd3-211">Azure CLI</span></span>|<span data-ttu-id="d7fd3-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="d7fd3-212">azurecli</span></span>|
|<span data-ttu-id="d7fd3-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-213">Azure PowerShell</span></span>|<span data-ttu-id="d7fd3-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-214">azurepowershell</span></span>|
|<span data-ttu-id="d7fd3-215">Bash</span><span class="sxs-lookup"><span data-stu-id="d7fd3-215">Bash</span></span>|<span data-ttu-id="d7fd3-216">bash</span><span class="sxs-lookup"><span data-stu-id="d7fd3-216">bash</span></span>|
|<span data-ttu-id="d7fd3-217">C++</span><span class="sxs-lookup"><span data-stu-id="d7fd3-217">C++</span></span>|<span data-ttu-id="d7fd3-218">cpp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-218">cpp</span></span>|
|<span data-ttu-id="d7fd3-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="d7fd3-219">C++/CX</span></span>|<span data-ttu-id="d7fd3-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="d7fd3-220">cppcx</span></span>|
|<span data-ttu-id="d7fd3-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="d7fd3-221">C++/WinRT</span></span>|<span data-ttu-id="d7fd3-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="d7fd3-222">cppwinrt</span></span>|
|<span data-ttu-id="d7fd3-223">C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-223">C#</span></span>|<span data-ttu-id="d7fd3-224">csharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-224">csharp</span></span>|
|<span data-ttu-id="d7fd3-225">브라우저의 C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-225">C# in browser</span></span>|<span data-ttu-id="d7fd3-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="d7fd3-226">csharp-interactive</span></span>|
|<span data-ttu-id="d7fd3-227">콘솔</span><span class="sxs-lookup"><span data-stu-id="d7fd3-227">Console</span></span>|<span data-ttu-id="d7fd3-228">콘솔</span><span class="sxs-lookup"><span data-stu-id="d7fd3-228">console</span></span>|
|<span data-ttu-id="d7fd3-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-229">CSHTML</span></span>|<span data-ttu-id="d7fd3-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-230">cshtml</span></span>|
|<span data-ttu-id="d7fd3-231">DAX</span><span class="sxs-lookup"><span data-stu-id="d7fd3-231">DAX</span></span>|<span data-ttu-id="d7fd3-232">dax</span><span class="sxs-lookup"><span data-stu-id="d7fd3-232">dax</span></span>|
|<span data-ttu-id="d7fd3-233">Docker</span><span class="sxs-lookup"><span data-stu-id="d7fd3-233">Docker</span></span>|<span data-ttu-id="d7fd3-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="d7fd3-234">dockerfile</span></span>|
|<span data-ttu-id="d7fd3-235">F#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-235">F#</span></span>|<span data-ttu-id="d7fd3-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-236">fsharp</span></span>|
|<span data-ttu-id="d7fd3-237">Go</span><span class="sxs-lookup"><span data-stu-id="d7fd3-237">Go</span></span>|<span data-ttu-id="d7fd3-238">go</span><span class="sxs-lookup"><span data-stu-id="d7fd3-238">go</span></span>|
|<span data-ttu-id="d7fd3-239">HTML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-239">HTML</span></span>|<span data-ttu-id="d7fd3-240">html</span><span class="sxs-lookup"><span data-stu-id="d7fd3-240">html</span></span>|
|<span data-ttu-id="d7fd3-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="d7fd3-241">HTTP</span></span>|<span data-ttu-id="d7fd3-242">http</span><span class="sxs-lookup"><span data-stu-id="d7fd3-242">http</span></span>|
|<span data-ttu-id="d7fd3-243">Java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-243">Java</span></span>|<span data-ttu-id="d7fd3-244">java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-244">java</span></span>|
|<span data-ttu-id="d7fd3-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-245">JavaScript</span></span>|<span data-ttu-id="d7fd3-246">javascript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-246">javascript</span></span>|
|<span data-ttu-id="d7fd3-247">JSON</span><span class="sxs-lookup"><span data-stu-id="d7fd3-247">JSON</span></span>|<span data-ttu-id="d7fd3-248">json</span><span class="sxs-lookup"><span data-stu-id="d7fd3-248">json</span></span>|
|<span data-ttu-id="d7fd3-249">Kusto 쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="d7fd3-249">Kusto Query Language</span></span>|<span data-ttu-id="d7fd3-250">kusto</span><span class="sxs-lookup"><span data-stu-id="d7fd3-250">kusto</span></span>|
|<span data-ttu-id="d7fd3-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="d7fd3-251">Markdown</span></span>|<span data-ttu-id="d7fd3-252">md</span><span class="sxs-lookup"><span data-stu-id="d7fd3-252">md</span></span>|
|<span data-ttu-id="d7fd3-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d7fd3-253">Objective-C</span></span>|<span data-ttu-id="d7fd3-254">objc</span><span class="sxs-lookup"><span data-stu-id="d7fd3-254">objc</span></span>|
|<span data-ttu-id="d7fd3-255">OData</span><span class="sxs-lookup"><span data-stu-id="d7fd3-255">OData</span></span>|<span data-ttu-id="d7fd3-256">odata</span><span class="sxs-lookup"><span data-stu-id="d7fd3-256">odata</span></span>|
|<span data-ttu-id="d7fd3-257">PHP</span><span class="sxs-lookup"><span data-stu-id="d7fd3-257">PHP</span></span>|<span data-ttu-id="d7fd3-258">php</span><span class="sxs-lookup"><span data-stu-id="d7fd3-258">php</span></span>|
|<span data-ttu-id="d7fd3-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="d7fd3-259">protobuf</span></span>|<span data-ttu-id="d7fd3-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="d7fd3-260">protobuf</span></span>|
|<span data-ttu-id="d7fd3-261">PowerApps(점 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="d7fd3-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="d7fd3-262">powerapps-dot</span></span>|
|<span data-ttu-id="d7fd3-263">PowerApps(쉼표 10진 구분 기호)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="d7fd3-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="d7fd3-264">powerapps-comma</span></span>|
|<span data-ttu-id="d7fd3-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-265">PowerShell</span></span>|<span data-ttu-id="d7fd3-266">powershell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-266">powershell</span></span>|
|<span data-ttu-id="d7fd3-267">Python</span><span class="sxs-lookup"><span data-stu-id="d7fd3-267">Python</span></span>|<span data-ttu-id="d7fd3-268">python</span><span class="sxs-lookup"><span data-stu-id="d7fd3-268">python</span></span>|
|<span data-ttu-id="d7fd3-269">Q#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-269">Q#</span></span>|<span data-ttu-id="d7fd3-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-270">qsharp</span></span>|
|<span data-ttu-id="d7fd3-271">R</span><span class="sxs-lookup"><span data-stu-id="d7fd3-271">R</span></span>|<span data-ttu-id="d7fd3-272">r</span><span class="sxs-lookup"><span data-stu-id="d7fd3-272">r</span></span>|
|<span data-ttu-id="d7fd3-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="d7fd3-273">Ruby</span></span>|<span data-ttu-id="d7fd3-274">ruby</span><span class="sxs-lookup"><span data-stu-id="d7fd3-274">ruby</span></span>|
|<span data-ttu-id="d7fd3-275">SQL</span><span class="sxs-lookup"><span data-stu-id="d7fd3-275">SQL</span></span>|<span data-ttu-id="d7fd3-276">sql</span><span class="sxs-lookup"><span data-stu-id="d7fd3-276">sql</span></span>|
|<span data-ttu-id="d7fd3-277">Swift</span><span class="sxs-lookup"><span data-stu-id="d7fd3-277">Swift</span></span>|<span data-ttu-id="d7fd3-278">swift</span><span class="sxs-lookup"><span data-stu-id="d7fd3-278">swift</span></span>|
|<span data-ttu-id="d7fd3-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-279">TypeScript</span></span>|<span data-ttu-id="d7fd3-280">typescript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-280">typescript</span></span>|
|<span data-ttu-id="d7fd3-281">VB</span><span class="sxs-lookup"><span data-stu-id="d7fd3-281">VB</span></span>|<span data-ttu-id="d7fd3-282">vb</span><span class="sxs-lookup"><span data-stu-id="d7fd3-282">vb</span></span>|
|<span data-ttu-id="d7fd3-283">XAML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-283">XAML</span></span>|<span data-ttu-id="d7fd3-284">xaml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-284">xaml</span></span>|
|<span data-ttu-id="d7fd3-285">XML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-285">XML</span></span>|<span data-ttu-id="d7fd3-286">xml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-286">xml</span></span>|

<span data-ttu-id="d7fd3-287">`csharp-interactive` 이름은 C# 언어와 브라우저에서 샘플을 실행하는 기능을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="d7fd3-288">이러한 코드 조각은 Docker 컨테이너에서 컴파일되고 실행되며, 해당 프로그램 실행 결과는 사용자의 브라우저 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="d7fd3-289">예제: C\#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-289">Example: C\#</span></span>

<span data-ttu-id="d7fd3-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d7fd3-290">__Markdown__</span></span>

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

<span data-ttu-id="d7fd3-291">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="d7fd3-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="d7fd3-292">예제: SQL</span><span class="sxs-lookup"><span data-stu-id="d7fd3-292">Example: SQL</span></span>

<span data-ttu-id="d7fd3-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d7fd3-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="d7fd3-294">__렌더링__</span><span class="sxs-lookup"><span data-stu-id="d7fd3-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="d7fd3-295">Docs 사용자 지정 Markdown 확장</span><span class="sxs-lookup"><span data-stu-id="d7fd3-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="d7fd3-296">Docs.Microsoft.com(Docs)은 GFM(GitHub Flavored Markdown)과 호환성이 높은 Markdig Parser for Markdown을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="d7fd3-297">Markdig은 Markdown 확장을 통해 몇 가지 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="d7fd3-298">이와 같이 이 가이드에는 전체 OPS 작성 가이드 중 참조할 수 있는 일부 문서가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="d7fd3-299">(예를 들어 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="d7fd3-300">Docs 문서는 문단, 링크, 목록, 제목 등 대부분의 문서 서식에 GFM를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="d7fd3-301">더 많은 형식의 경우 문서는 다음과 같은 Markdig 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="d7fd3-302">참고 블록</span><span class="sxs-lookup"><span data-stu-id="d7fd3-302">Note blocks</span></span>
- <span data-ttu-id="d7fd3-303">포함 파일</span><span class="sxs-lookup"><span data-stu-id="d7fd3-303">Include files</span></span>
- <span data-ttu-id="d7fd3-304">선택기</span><span class="sxs-lookup"><span data-stu-id="d7fd3-304">Selectors</span></span>
- <span data-ttu-id="d7fd3-305">포함된 비디오</span><span class="sxs-lookup"><span data-stu-id="d7fd3-305">Embedded videos</span></span>
- <span data-ttu-id="d7fd3-306">코드 조각/샘플</span><span class="sxs-lookup"><span data-stu-id="d7fd3-306">Code snippets/samples</span></span>

<span data-ttu-id="d7fd3-307">전체 목록은 목차에서 "Markdig 및 Markdown 확장" 및 "코드 조각"을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="d7fd3-308">참고 블록</span><span class="sxs-lookup"><span data-stu-id="d7fd3-308">Note blocks</span></span>

<span data-ttu-id="d7fd3-309">특정 콘텐츠에 주의를 집중하기 위해 4가지 형식의 참고 블록 중에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="d7fd3-310">참고</span><span class="sxs-lookup"><span data-stu-id="d7fd3-310">NOTE</span></span>
- <span data-ttu-id="d7fd3-311">경고</span><span class="sxs-lookup"><span data-stu-id="d7fd3-311">WARNING</span></span>
- <span data-ttu-id="d7fd3-312">팁</span><span class="sxs-lookup"><span data-stu-id="d7fd3-312">TIP</span></span>
- <span data-ttu-id="d7fd3-313">중요</span><span class="sxs-lookup"><span data-stu-id="d7fd3-313">IMPORTANT</span></span>

<span data-ttu-id="d7fd3-314">일반적으로 참고 블록은 문맥을 끊을 수 있기 때문에 제한적으로 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="d7fd3-315">참고 블록에 코드 블록, 이미지, 목록, 링크를 적용할 수는 있지만 참고 블록은 간단하고 단순하게 유지하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="d7fd3-316">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-316">Examples:</span></span>

```md
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="d7fd3-317">이러한 경고는 docs.microsoft.com에서 다음과 같이 보입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-317">These alerts look like this on docs.microsoft.com:</span></span>

![게시된 Docs 페이지에서 이전 예제의 경고가 다른 아이콘 및 색으로 어떻게 표시되는지를 보여 주는 이미지](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="d7fd3-319">포함되는 파일</span><span class="sxs-lookup"><span data-stu-id="d7fd3-319">Include files</span></span>

<span data-ttu-id="d7fd3-320">문서 파일에 포함되어야 하는 재사용 가능 텍스트 또는 이미지 파일이 있는 경우 Markdig 파일 포함 기능을 통해 "포함되는" 파일에 대한 참조를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="d7fd3-321">이 기능은 빌드 시 OPS에서 지정된 파일을 문서 파일에 포함하도록 지시하여 게시된 문서의 일부로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="d7fd3-322">콘텐츠를 재사용하기 위해 사용 가능한 포함되는 참조에는 3가지 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="d7fd3-323">인라인: 다른 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="d7fd3-324">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="d7fd3-325">이미지: 표준 이미지 포함이 Docs에서 구현되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="d7fd3-326">인라인 또는 블록에 포함되는 파일은 간단한 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="d7fd3-327">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="d7fd3-328">포함되는 내용 Markdown 파일은 모두 리포지토리의 루트에서 [일반적인 `/includes` 하위 디렉토리](git-github-fundamentals.md#includes-subdirectory)에 배치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="d7fd3-329">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="d7fd3-330">포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="d7fd3-331">여러 문서에서 나타나는 동일한 텍스트가 필요하면 언제든지 포함되는 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="d7fd3-332">블록에 포함되는 파일은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d7fd3-333">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d7fd3-334">포함되는 참조는 Markdig 확장에 의존하기 때문에 문서의 GitHub 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="d7fd3-335">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d7fd3-336">포함되는 파일의 모든 텍스트가 문서에서 포함되는 파일을 참조하는 앞의 텍스트 또는 뒤의 텍스트에 의존하지 않는 완전한 문장 또는 구로 작성되었는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="d7fd3-337">이 지침을 무시하면 문서에서 번역되지 않은 문자열이 발생하고 지역화된 환경을 중단하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="d7fd3-338">다른 포함되는 파일 내에 포함되는 참조를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="d7fd3-339">지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-339">They are not supported.</span></span>
- <span data-ttu-id="d7fd3-340">미디어 파일을 포함되는 내용 하위 디렉토리의 미디어 폴더에 저장합니다(예: `<repo>`/includes/media 폴더).</span><span class="sxs-lookup"><span data-stu-id="d7fd3-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="d7fd3-341">미디어 디렉토리는 해당 루트에서 이미지를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="d7fd3-342">포함되는 파일에 이미지가 없는 경우 해당하는 미디어 디렉터리가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="d7fd3-343">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d7fd3-344">포함되는 파일 및 문서 각각에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="d7fd3-345">포함되는 파일과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="d7fd3-346">포함되는 파일을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="d7fd3-347">포함되는 파일은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="d7fd3-348">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="d7fd3-349">선택기</span><span class="sxs-lookup"><span data-stu-id="d7fd3-349">Selectors</span></span>

<span data-ttu-id="d7fd3-350">동일한 문서의 다양한 버전을 작성하는 경우 기술 문서에서 선택기를 사용하여 기술 또는 플랫폼 간의 구현 차이를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d7fd3-351">이 기능은 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="d7fd3-352">Markdig에는 단일 선택기 및 다중 선택기라는 두 가지 종류의 선택기가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="d7fd3-353">동일한 선택기 Markdown은 선택 항목의 각 문서에 포함되므로 문서의 선택기를 포함되는 파일에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="d7fd3-354">그런 다음, 동일한 선택기를 사용하는 모든 문서에서 포함되는 해당 파일을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="d7fd3-355">다음은 예제 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="d7fd3-356">[Azure 문서](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)에서 실행 중인 선택기의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="d7fd3-357">코드에 포함되는 참조</span><span class="sxs-lookup"><span data-stu-id="d7fd3-357">Code include references</span></span>

<span data-ttu-id="d7fd3-358">Docs 코드 조각 Markdown 확장을 사용하면 문서에 코드 샘플을 포함하고 언어별 구문 색 지정으로 렌더링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="d7fd3-359">현재 리포지토리 또는 다른 리포지토리의 코드를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="d7fd3-360">아래 지침에서는 [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)으로 해당 기능을 사용하는 방법에 대한 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="d7fd3-361">Visual Studio Code에서 **Preview**를 열어 코드 조각을 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="d7fd3-362">강조 표시 및 대화형 작업은 미리 보기에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="d7fd3-363">확장을 사용하여 코드 콘텐츠를 인라인으로 포함할 수 없습니다. 이 작업은 표준 삼중 틱 Markdown 규칙을 통해 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="d7fd3-364">현재 리포지토리의 코드</span><span class="sxs-lookup"><span data-stu-id="d7fd3-364">Code from current repository</span></span>

1. <span data-ttu-id="d7fd3-365">Visual Studio Code에서 **Alt + M** 또는 **Option + M**을 클릭하고 코드 조각을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="d7fd3-366">코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="d7fd3-367">로컬에서 검색하려면 전체 로컬 검색을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="d7fd3-368">검색 용어를 입력하여 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-368">Enter a search term to find the file.</span></span> <span data-ttu-id="d7fd3-369">파일을 찾으면 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="d7fd3-370">다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="d7fd3-371">옵션은 **ID**, **범위**, **없음**입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="d7fd3-372">4단계에서 선택한 옵션에 따라 필요한 경우 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="d7fd3-373">전체 코드 파일 표시:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="d7fd3-374">줄 번호를 지정하여 코드 파일의 일부 표시:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="d7fd3-375">코드 조각 이름으로 코드 파일의 일부 표시:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="d7fd3-376">다른 리포지토리의 코드</span><span class="sxs-lookup"><span data-stu-id="d7fd3-376">Code from another repository</span></span>

1. <span data-ttu-id="d7fd3-377">Visual Studio Code에서 **Alt + M** 또는 **Option + M**을 클릭하고 코드 조각을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="d7fd3-378">코드 조각을 선택하면 전체 검색, 범위 지정 검색 또는 리포지토리 간 참조를 선택하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="d7fd3-379">리포지토리에서 검색하려면 리포지토리 간 참조를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="d7fd3-380">*.openpublishing.publish.config.json*에 있는 리포지토리에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="d7fd3-381">리포지토리를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-381">Select a repository.</span></span>
3. <span data-ttu-id="d7fd3-382">검색 용어를 입력하여 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-382">Enter a search term to find the file.</span></span> <span data-ttu-id="d7fd3-383">파일을 찾으면 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="d7fd3-384">다음으로, 코드 조각에 포함되어야 하는 코드 줄을 결정하기 위한 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="d7fd3-385">옵션은 **ID**, **범위**, **없음**입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="d7fd3-386">5단계에서 선택한 옵션에 따라 필요한 경우 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="d7fd3-387">코드 조각 참조는 다음과 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="d7fd3-388">코드 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="d7fd3-388">Path to code file</span></span>

<span data-ttu-id="d7fd3-389">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="d7fd3-390">이 예제는 ASP.NET 문서 리포지토리, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) 문서 파일에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="d7fd3-391">코드 파일은 동일한 리포지토리에 있는 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs)의 상대 경로로 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="d7fd3-392">선택한 줄 번호</span><span class="sxs-lookup"><span data-stu-id="d7fd3-392">Selected line numbers</span></span>

<span data-ttu-id="d7fd3-393">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="d7fd3-394">위 예제에서는 *StudentController.cs* 코드 파일의 줄 2~24와 26만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="d7fd3-395">다음 섹션에 설명된 대로 하드 코드된 줄 번호보다 코드 조각을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="d7fd3-396">명명된 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-396">Named snippet</span></span>

<span data-ttu-id="d7fd3-397">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="d7fd3-398">이름에는 문자와 밑줄만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="d7fd3-399">이 예제는 코드 파일의 `snippet_Create` 섹션을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="d7fd3-400">이 예제의 코드 파일에는 `snippet_Create`라는 C# 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="d7fd3-401">가능한 한, 줄 번호를 지정하지 말고 명명된 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="d7fd3-402">코드 파일은 필연적으로 변경되고, 이 경우 줄 번호도 변경되기 때문에 줄 번호 참조는 불안정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="d7fd3-403">항상 이러한 변경에 대한 알림을 받는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="d7fd3-404">결국 문서에서 잘못된 줄이 나타나기 시작해도 무엇이 변경되었는지 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="d7fd3-405">선택한 줄 강조 표시</span><span class="sxs-lookup"><span data-stu-id="d7fd3-405">Highlighting selected lines</span></span>

<span data-ttu-id="d7fd3-406">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="d7fd3-407">이 예제에서는 표시된 코드 조각의 처음부터 줄 2와 5를 강조 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="d7fd3-408">강조 표시할 줄 번호가 코드 파일의 처음부터 계산되지 않습니다. 즉, 코드 파일의 줄 3과 6이 강조 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="d7fd3-409">대화형 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-409">Interactive code snippets</span></span>

<span data-ttu-id="d7fd3-410">참조를 통해 포함된 코드 조각에 대해 대화형 모드를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="d7fd3-411">예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="d7fd3-412">특정 코드 블록을 대상으로 이 기능을 켜려면 `interactive` 특성을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="d7fd3-413">사용 가능한 특성 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-413">The available attribute values are:</span></span>

- <span data-ttu-id="d7fd3-414">`cloudshell-powershell` - 앞의 예제와 같이 Azure PowerShell Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d7fd3-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="d7fd3-415">`cloudshell-bash` - Azure Cloud Shell을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d7fd3-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="d7fd3-416">`try-dotnet` - Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d7fd3-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="d7fd3-417">`try-dotnet-class` - 클래스 스캐폴딩으로 Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d7fd3-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="d7fd3-418">`try-dotnet-method` - 메서드 스캐폴딩으로 Try .NET을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d7fd3-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="d7fd3-419">호환되는 `language`와 `interactive`의 쌍이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="d7fd3-420">예를 들어 `interactive`가 `try-dotnet`인 경우 언어는 `csharp`여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="d7fd3-421">마찬가지로 `cloudshell-powershell`은 `powershell`과만, `cloudshell-bash`는 `bash`와만 언어로 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="d7fd3-422">Azure Cloud Shell 및 PowerShell Cloud Shell의 경우 사용자가 자신의 Azure 계정에 대해서만 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="d7fd3-423">[Try .NET](https://github.com/dotnet/try)을 사용하면 브라우저에서 .NET 코드(C#)를 대화형으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="d7fd3-424">Try .NET에는 대화형 작업에 사용할 수 있는 세 가지 옵션(`try-dotnet`, `try-dotnet-class`, `try-dotnet-method`)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="d7fd3-425">이와 같은 옵션을 사용하는 데 코드 조각 내의 추가 구성이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="d7fd3-426">현재 기본적으로 사용할 수 있는 네임스페이스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="d7fd3-427">System</span><span class="sxs-lookup"><span data-stu-id="d7fd3-427">System</span></span>
- <span data-ttu-id="d7fd3-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="d7fd3-428">System.Linq</span></span>
- <span data-ttu-id="d7fd3-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="d7fd3-429">System.Collections.Generic</span></span>
- <span data-ttu-id="d7fd3-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="d7fd3-430">System.Text</span></span>
- <span data-ttu-id="d7fd3-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="d7fd3-431">System.Globalization</span></span>
- <span data-ttu-id="d7fd3-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="d7fd3-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="d7fd3-433">사용자는 `try-dotnet` 특성 값을 사용하여 사용자 지정 코드에서 코드를 래핑할 필요 없이 브라우저에서 C# 코드를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="d7fd3-434">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="d7fd3-435">`try-dotnet-class` 값은 대화형 구성 요소에 전달된 코드에 클래스 수준 스캐폴딩을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="d7fd3-436">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-436">Example:</span></span>

<span data-ttu-id="d7fd3-437">클래스 스캐폴딩이 적용되지 않은 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-437">Code Snippet without Class Scaffolding Applied</span></span>

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="d7fd3-438">클래스 스캐폴딩이 적용된 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-438">Code Snippet with Class Scaffolding Applied</span></span>

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="d7fd3-439">`try-dotnet-method` 값은 대화형 구성 요소에 전달된 코드에 메서드 수준 스캐폴딩을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="d7fd3-440">예제:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-440">Example:</span></span>

<span data-ttu-id="d7fd3-441">메서드 스캐폴딩이 적용되지 않은 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="d7fd3-442">메서드 스캐폴딩이 적용된 코드 조각</span><span class="sxs-lookup"><span data-stu-id="d7fd3-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="d7fd3-443">코드 조각 구문 참조</span><span class="sxs-lookup"><span data-stu-id="d7fd3-443">Snippet syntax reference</span></span>

<span data-ttu-id="d7fd3-444">지정된 코드 언어를 사용하여 리포지토리에 저장된 코드 조각을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="d7fd3-445">지정된 코드 경로 콘텐츠가 확장되어 파일에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="d7fd3-446">코드 조각의 폴더 구조에 대한 제한은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="d7fd3-447">코드 조각을 일반 소스 코드로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="d7fd3-448">구문:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="d7fd3-449">이 구문은 블록 Markdown 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="d7fd3-450">자체 줄에 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-450">It must be used on its own line.</span></span>

- <span data-ttu-id="d7fd3-451">`<language>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="d7fd3-452">코드 조각의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-452">Language of the code snippet.</span></span> <span data-ttu-id="d7fd3-453">자세한 내용은 본 문서의 아래에 있는 [지원되는 언어](#supported-languages) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="d7fd3-454">`<path>`(*필수*)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="d7fd3-455">참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="d7fd3-456">`<attribute>` 및 `<attribute-value>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="d7fd3-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="d7fd3-457">파일에서 코드를 검색하는 방법을 지정하는 데 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="d7fd3-458">`range`: `1,3-5` 줄 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="d7fd3-459">이 예제는 1, 3, 4 및 5 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="d7fd3-460">`id`: `snippet_Create` 코드 파일에서 삽입해야 하는 코드 조각의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="d7fd3-461">이 값은 범위와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="d7fd3-462">`highlight`: `2-4,6` 생성된 코드 조각에서 강조 표시해야 하는 범위 및/또는 줄 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="d7fd3-463">번호 매기기는 가져온 범위가 아니라 코드 조각 자체를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="d7fd3-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` 문자열 값은 어떤 종류의 대화형 작업이 사용하도록 설정되는지를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="d7fd3-465">지원되는 언어</span><span class="sxs-lookup"><span data-stu-id="d7fd3-465">Supported languages</span></span>

|<span data-ttu-id="d7fd3-466">Name</span><span class="sxs-lookup"><span data-stu-id="d7fd3-466">Name</span></span>|<span data-ttu-id="d7fd3-467">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="d7fd3-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="d7fd3-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="d7fd3-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="d7fd3-469">ASP.NET 및 C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="d7fd3-470">ASP.NET 및 VB</span><span class="sxs-lookup"><span data-stu-id="d7fd3-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="d7fd3-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d7fd3-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="d7fd3-472">브라우저의 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d7fd3-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="d7fd3-473">브라우저의 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="d7fd3-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="d7fd3-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="d7fd3-475">Bash</span><span class="sxs-lookup"><span data-stu-id="d7fd3-475">Bash</span></span>|`bash`|
|<span data-ttu-id="d7fd3-476">C++</span><span class="sxs-lookup"><span data-stu-id="d7fd3-476">C++</span></span>|`cpp`|
|<span data-ttu-id="d7fd3-477">C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-477">C#</span></span>|`csharp`|
|<span data-ttu-id="d7fd3-478">브라우저의 C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="d7fd3-479">콘솔</span><span class="sxs-lookup"><span data-stu-id="d7fd3-479">Console</span></span>|`console`|
|<span data-ttu-id="d7fd3-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="d7fd3-481">DAX</span><span class="sxs-lookup"><span data-stu-id="d7fd3-481">DAX</span></span>|`dax`|
|<span data-ttu-id="d7fd3-482">Docker</span><span class="sxs-lookup"><span data-stu-id="d7fd3-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="d7fd3-483">F#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="d7fd3-484">HTML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-484">HTML</span></span>|`html`|
|<span data-ttu-id="d7fd3-485">Java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-485">Java</span></span>|`java`|
|<span data-ttu-id="d7fd3-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="d7fd3-487">JSON</span><span class="sxs-lookup"><span data-stu-id="d7fd3-487">JSON</span></span>|`json`|
|<span data-ttu-id="d7fd3-488">Kusto 쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="d7fd3-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="d7fd3-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="d7fd3-489">Markdown</span></span>|`md`|
|<span data-ttu-id="d7fd3-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d7fd3-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="d7fd3-491">PHP</span><span class="sxs-lookup"><span data-stu-id="d7fd3-491">PHP</span></span>|`php`|
|<span data-ttu-id="d7fd3-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7fd3-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="d7fd3-493">파워 쿼리 M</span><span class="sxs-lookup"><span data-stu-id="d7fd3-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="d7fd3-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="d7fd3-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="d7fd3-495">Python</span><span class="sxs-lookup"><span data-stu-id="d7fd3-495">Python</span></span>|`python`|
|<span data-ttu-id="d7fd3-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="d7fd3-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="d7fd3-497">SQL</span><span class="sxs-lookup"><span data-stu-id="d7fd3-497">SQL</span></span>|`sql`|
|<span data-ttu-id="d7fd3-498">Swift</span><span class="sxs-lookup"><span data-stu-id="d7fd3-498">Swift</span></span>|`swift`|
|<span data-ttu-id="d7fd3-499">VB</span><span class="sxs-lookup"><span data-stu-id="d7fd3-499">VB</span></span>|`vb`|
|<span data-ttu-id="d7fd3-500">XAML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="d7fd3-501">XML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-501">XML</span></span>|`xml`|
|<span data-ttu-id="d7fd3-502">YAML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="d7fd3-503">코드 확장</span><span class="sxs-lookup"><span data-stu-id="d7fd3-503">Code extensions</span></span>

|<span data-ttu-id="d7fd3-504">Name</span><span class="sxs-lookup"><span data-stu-id="d7fd3-504">Name</span></span>|<span data-ttu-id="d7fd3-505">Markdown 레이블</span><span class="sxs-lookup"><span data-stu-id="d7fd3-505">Markdown label</span></span>|<span data-ttu-id="d7fd3-506">파일 확장</span><span class="sxs-lookup"><span data-stu-id="d7fd3-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="d7fd3-507">C#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-507">C#</span></span>|<span data-ttu-id="d7fd3-508">csharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-508">csharp</span></span>|<span data-ttu-id="d7fd3-509">.cs, .csx</span><span class="sxs-lookup"><span data-stu-id="d7fd3-509">.cs, .csx</span></span>|
|<span data-ttu-id="d7fd3-510">C++</span><span class="sxs-lookup"><span data-stu-id="d7fd3-510">C++</span></span>|<span data-ttu-id="d7fd3-511">cpp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-511">cpp</span></span>|<span data-ttu-id="d7fd3-512">.cpp, .h</span><span class="sxs-lookup"><span data-stu-id="d7fd3-512">.cpp, .h</span></span>|
|<span data-ttu-id="d7fd3-513">F#</span><span class="sxs-lookup"><span data-stu-id="d7fd3-513">F#</span></span>|<span data-ttu-id="d7fd3-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="d7fd3-514">fsharp</span></span>|<span data-ttu-id="d7fd3-515">.fs</span><span class="sxs-lookup"><span data-stu-id="d7fd3-515">.fs</span></span>|
|<span data-ttu-id="d7fd3-516">Java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-516">Java</span></span>|<span data-ttu-id="d7fd3-517">java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-517">java</span></span>|<span data-ttu-id="d7fd3-518">.java</span><span class="sxs-lookup"><span data-stu-id="d7fd3-518">.java</span></span>|
|<span data-ttu-id="d7fd3-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-519">JavaScript</span></span>|<span data-ttu-id="d7fd3-520">javascript</span><span class="sxs-lookup"><span data-stu-id="d7fd3-520">javascript</span></span>|<span data-ttu-id="d7fd3-521">.js</span><span class="sxs-lookup"><span data-stu-id="d7fd3-521">.js</span></span>|
|<span data-ttu-id="d7fd3-522">Python</span><span class="sxs-lookup"><span data-stu-id="d7fd3-522">Python</span></span>|<span data-ttu-id="d7fd3-523">python</span><span class="sxs-lookup"><span data-stu-id="d7fd3-523">python</span></span>|<span data-ttu-id="d7fd3-524">.py</span><span class="sxs-lookup"><span data-stu-id="d7fd3-524">.py</span></span>|
|<span data-ttu-id="d7fd3-525">SQL</span><span class="sxs-lookup"><span data-stu-id="d7fd3-525">SQL</span></span>|<span data-ttu-id="d7fd3-526">sql</span><span class="sxs-lookup"><span data-stu-id="d7fd3-526">sql</span></span>|<span data-ttu-id="d7fd3-527">.sql</span><span class="sxs-lookup"><span data-stu-id="d7fd3-527">.sql</span></span>|
|<span data-ttu-id="d7fd3-528">VB</span><span class="sxs-lookup"><span data-stu-id="d7fd3-528">VB</span></span>|<span data-ttu-id="d7fd3-529">vb</span><span class="sxs-lookup"><span data-stu-id="d7fd3-529">vb</span></span>|<span data-ttu-id="d7fd3-530">.vb</span><span class="sxs-lookup"><span data-stu-id="d7fd3-530">.vb</span></span>|
|<span data-ttu-id="d7fd3-531">XAML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-531">XAML</span></span>|<span data-ttu-id="d7fd3-532">xaml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-532">xaml</span></span>|<span data-ttu-id="d7fd3-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-533">.xaml</span></span>|
|<span data-ttu-id="d7fd3-534">XML</span><span class="sxs-lookup"><span data-stu-id="d7fd3-534">XML</span></span>|<span data-ttu-id="d7fd3-535">xml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-535">xml</span></span>|<span data-ttu-id="d7fd3-536">.xml</span><span class="sxs-lookup"><span data-stu-id="d7fd3-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="d7fd3-537">과제 및 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d7fd3-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="d7fd3-538">대체 텍스트</span><span class="sxs-lookup"><span data-stu-id="d7fd3-538">Alt text</span></span>

<span data-ttu-id="d7fd3-539">밑줄이 포함된 대체 텍스트를 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="d7fd3-540">예를 들어 아래 텍스트를 사용하는 대신</span><span class="sxs-lookup"><span data-stu-id="d7fd3-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d7fd3-541">다음과 같이 밑줄을 이스케이프 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d7fd3-542">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="d7fd3-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d7fd3-543">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d7fd3-544">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d7fd3-545">그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="d7fd3-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d7fd3-546">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d7fd3-547">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="d7fd3-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d7fd3-548">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="d7fd3-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d7fd3-549">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="d7fd3-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d7fd3-550">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="d7fd3-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d7fd3-551">대괄호</span><span class="sxs-lookup"><span data-stu-id="d7fd3-551">Angle brackets</span></span>

<span data-ttu-id="d7fd3-552">자리 표시자를 나타내는 데 대괄호를 사용하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="d7fd3-553">텍스트(코드 아님)에서 이 작업을 수행할 때는 대괄호를 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="d7fd3-554">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d7fd3-555">예를 들어 `<script name>`을 `&lt;script name&gt;`로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="d7fd3-556">Markdown 유형</span><span class="sxs-lookup"><span data-stu-id="d7fd3-556">Markdown flavor</span></span>

<span data-ttu-id="d7fd3-557">docs.microsoft.com 사이트 백 엔드는 [Markdig](https://github.com/lunet-io/markdig) 구문 분석 엔진을 통해 구문 분석된 [CommonMark](https://commonmark.org/) 규격 Markdown을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="d7fd3-558">해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/)과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="d7fd3-559">추가 기능은 Markdown 확장을 통해 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7fd3-560">참고 항목:</span><span class="sxs-lookup"><span data-stu-id="d7fd3-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="d7fd3-561">Markdown 리소스</span><span class="sxs-lookup"><span data-stu-id="d7fd3-561">Markdown resources</span></span>

- [<span data-ttu-id="d7fd3-562">Markdown 소개</span><span class="sxs-lookup"><span data-stu-id="d7fd3-562">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="d7fd3-563">Docs Markdown 참고 자료</span><span class="sxs-lookup"><span data-stu-id="d7fd3-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="d7fd3-564">GitHub의 Markdown 기본 사항</span><span class="sxs-lookup"><span data-stu-id="d7fd3-564">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="d7fd3-565">Markdown 가이드</span><span class="sxs-lookup"><span data-stu-id="d7fd3-565">The Markdown Guide</span></span>](https://www.markdownguide.org/)
