---
title: docs.microsoft.com에 대한 Markdown 참조
description: Microsoft Docs 플랫폼에서 사용되는 Markdown 기능 및 구문을 알아봅니다.
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: c1568264c687ebaf26048f5432fdea7d5132c012
ms.sourcegitcommit: 216ef77ca2cd1eeb31c6c89d96778b178fc0d540
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2020
ms.locfileid: "80070069"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="d09bc-103">Docs Markdown 참조</span><span class="sxs-lookup"><span data-stu-id="d09bc-103">Docs Markdown reference</span></span>

<span data-ttu-id="d09bc-104">이 문서에서는 Docs(docs.microsoft.com) Markdown을 작성하기 위한 사전순 참조를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="d09bc-105">[Markdown](https://daringfireball.net/projects/markdown/)은 일반 텍스트 서식 구문을 사용하는 경량 생성 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="d09bc-106">Docs는 [Markdig](https://github.com/lunet-io/markdig) 구문 분석 엔진을 통해 구문 분석된 [CommonMark](https://commonmark.org/) 규격 Markdown을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="d09bc-107">Docs 사이트에서 더욱 풍부한 콘텐츠를 제공하는 사용자 지정 Markdown 확장도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="d09bc-108">Markdown을 작성하는 데는 어떤 텍스트 편집기든 사용할 수 있으나 [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack)이 포함된 [Visual Studio Code](https://code.visualstudio.com/)를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="d09bc-109">Docs Authoring Pack은 편집 도구와 미리 보기 기능을 제공하므로 Docs에서 렌더링하는 경우 문서 모양을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="d09bc-110">경고(Note, Tip, Important, Caution, Warning)</span><span class="sxs-lookup"><span data-stu-id="d09bc-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="d09bc-111">경고는 콘텐츠의 중요도를 나타내는 색과 아이콘을 사용하여 docs.microsoft.com에서 렌더링되는 블록 따옴표를 만들기 위한 Markdown 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="d09bc-112">다음과 같은 경고 유형이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-112">The following alert types are supported:</span></span>

```markdown
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

<span data-ttu-id="d09bc-113">이러한 경고는 docs.microsoft.com에서 다음과 같이 보입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="d09bc-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="d09bc-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="d09bc-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="d09bc-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d09bc-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="d09bc-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="d09bc-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="d09bc-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="d09bc-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="d09bc-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d09bc-119">대괄호</span><span class="sxs-lookup"><span data-stu-id="d09bc-119">Angle brackets</span></span>

<span data-ttu-id="d09bc-120">예를 들어 자리 표시자를 나타내는 것과 같이 파일에 있는 텍스트에서 꺾쇠 괄호를 사용하는 경우 꺾쇠 괄호를 수동으로 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="d09bc-121">그렇지 않으면 Markdown에서는 해당 기호가 HTML 태그로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d09bc-122">예를 들어 `<script name>`을 `&lt;script name&gt;` 또는 `\<script name>`으로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="d09bc-123">인라인 코드 또는 코드 블록으로 서식 지정된 텍스트에서는 꺾쇠 괄호를 이스케이프할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d09bc-124">아포스트로피 및 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="d09bc-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d09bc-125">Word에서 Markdown 편집기로 복사하는 경우 텍스트에 "스마트"(둥근) 아포스트로피 및 큰따옴표가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d09bc-126">이러한 기호는 인코딩하거나 기본 아포스트로피 또는 큰따옴표로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d09bc-127">그렇지 않을 경우 파일이 게시되면 다음과 같이 표시됩니다. Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="d09bc-127">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d09bc-128">이러한 "스마트" 버전 문장 부호를 다음과 같이 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d09bc-129">왼쪽(열린) 큰따옴표: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="d09bc-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d09bc-130">오른쪽(닫힌) 큰따옴표: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="d09bc-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d09bc-131">오른쪽(닫힌) 작은 따옴표 또는 아포스트로피: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="d09bc-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d09bc-132">왼쪽(열린) 작은 따옴표(거의 사용 안 함): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="d09bc-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="d09bc-133">Blockquotes</span><span class="sxs-lookup"><span data-stu-id="d09bc-133">Blockquotes</span></span>

<span data-ttu-id="d09bc-134">Blockquotes는 `>` 문자를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="d09bc-135">앞의 예는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="d09bc-136">블록 따옴표입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-136">This is a blockquote.</span></span> <span data-ttu-id="d09bc-137">일반적으로 들여쓰기되고 다른 배경색을 사용하도록 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="d09bc-138">굵게 기울임꼴 텍스트</span><span class="sxs-lookup"><span data-stu-id="d09bc-138">Bold and italic text</span></span>

<span data-ttu-id="d09bc-139">텍스트에 **굵게** 서식을 지정하려면 두 개의 별표로 텍스트를 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="d09bc-140">텍스트에 ‘기울임꼴’ 서식을 지정하려면 한 개의 별표로 텍스트를 묶습니다. </span><span class="sxs-lookup"><span data-stu-id="d09bc-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="d09bc-141">텍스트에 ***굵게 및 기울임꼴*** 서식을 둘 다 지정하려면 세 개의 별표로 텍스트를 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="d09bc-142">코드 조각</span><span class="sxs-lookup"><span data-stu-id="d09bc-142">Code snippets</span></span>

<span data-ttu-id="d09bc-143">Docs Markdown에서는 코드 조각을 한 문장 내에 인라인으로 배치하는 것과 문장 사이에 별도의 “펜싱된” 블록으로 배치하는 것을 둘 다 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d09bc-144">자세한 내용은 [docs에 코드를 추가하는 방법](code-in-docs.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="d09bc-145">열</span><span class="sxs-lookup"><span data-stu-id="d09bc-145">Columns</span></span>

<span data-ttu-id="d09bc-146">**열** Markdown 확장은 진정한 표 형식 데이터에만 적합한 기본 Markdown 테이블보다 더 유연하고 강력한 열 기반 콘텐츠 레이아웃 추가 기능을 Docs 작성자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="d09bc-147">최대 네 개의 열을 추가하고 선택적 `span` 특성을 사용하여 두 개 이상의 열을 병합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="d09bc-148">열에 대한 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="d09bc-149">열에는 이미지를 비롯하여 기본 Markdown만 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="d09bc-150">제목, 테이블, 탭 및 기타 복잡한 구조는 포함되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="d09bc-151">행에는 열 외부에 있는 콘텐츠가 포함될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="d09bc-152">예를 들어 다음 Markdown에서는 열 너비 두 개와 표준(`span` 없음) 열 한 개 범위의 열 하나를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="d09bc-153">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="d09bc-154">**텍스트가 많이 포함된 두 개 범위의 열입니다.**</span><span class="sxs-lookup"><span data-stu-id="d09bc-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="d09bc-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="d09bc-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="d09bc-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="d09bc-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="d09bc-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="d09bc-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="d09bc-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="d09bc-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d09bc-159">**이미지가 포함된 한 개 범위의 열입니다.**</span><span class="sxs-lookup"><span data-stu-id="d09bc-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="d09bc-161">제목</span><span class="sxs-lookup"><span data-stu-id="d09bc-161">Headings</span></span>

<span data-ttu-id="d09bc-162">Docs는 6가지 수준의 Markdown 제목을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="d09bc-163">마지막 `#`과 제목 텍스트 사이에는 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="d09bc-164">각 Markdown 파일에는 H1 제목이 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="d09bc-165">H1 제목은 파일에서 YML 메타데이터 블록 다음의 첫 번째 콘텐츠여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="d09bc-166">H2 제목은 게시된 파일의 오른쪽 탐색 메뉴에 자동으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="d09bc-167">더 낮은 수준의 제목은 표시되지 않으므로 H2를 전략적으로 사용하여 독자의 콘텐츠 탐색을 돕습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="d09bc-168">`<h1>`과 같은 HTML 제목은 사용하지 않는 것이 좋으며 경우에 따라 빌드 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="d09bc-169">[책갈피 링크](how-to-write-links.md#links-to-anchors)를 통해 파일의 개별 제목에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#links-to-anchors).</span></span>

## <a name="html"></a><span data-ttu-id="d09bc-170">HTML</span><span class="sxs-lookup"><span data-stu-id="d09bc-170">HTML</span></span>

<span data-ttu-id="d09bc-171">Markdown에서는 인라인 HTML을 지원하지만 HTML은 Docs에 게시하는 데 사용하지 않는 것이 좋으며 제한된 값 목록을 제외하고는 빌드 오류 또는 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> 

## <a name="images"></a><span data-ttu-id="d09bc-172">이미지</span><span class="sxs-lookup"><span data-stu-id="d09bc-172">Images</span></span>

<span data-ttu-id="d09bc-173">기본적으로 이미지에 대해 다음 파일 형식이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="d09bc-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="d09bc-174">.jpg</span></span>
- <span data-ttu-id="d09bc-175">.png</span><span class="sxs-lookup"><span data-stu-id="d09bc-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="d09bc-176">표준 개념 이미지(기본 Markdown)</span><span class="sxs-lookup"><span data-stu-id="d09bc-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="d09bc-177">이미지를 포함하기 위한 기본 Markdown 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="d09bc-178">여기서 `<alt text>`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="d09bc-179">시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="d09bc-180">또한 이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="d09bc-181">백슬래시(`\_`)를 접두사로 사용하여 이스케이프하지 않는 경우 대체 텍스트의 밑줄이 제대로 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="d09bc-182">하지만 파일 이름을 대체 텍스트로 사용하기 위해 복사하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="d09bc-183">예를 들어 다음은 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d09bc-184">다음과 같이 작성하세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="d09bc-185">표준 개념 이미지(Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="d09bc-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="d09bc-186">Docs 사용자 지정 `:::image:::` 확장에서는 표준 이미지, 복잡한 이미지 및 아이콘을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="d09bc-187">표준 이미지에 계속 이전 Markdown 구문을 사용할 수 있으나 새 확장에서는 부모 항목과 다른 지역화 범위 지정과 같은 더 강력한 기능을 지원하므로 새 확장을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="d09bc-188">로컬 이미지를 지정하지 않고 공유 이미지 갤러리에서 선택하는 것과 같은 다른 고급 기능은 나중에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="d09bc-189">새 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="d09bc-190">`type="content"`(기본값)이면 `source`와 `alt-text`가 둘 다 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="d09bc-191">긴 설명이 포함된 복잡한 이미지</span><span class="sxs-lookup"><span data-stu-id="d09bc-191">Complex images with long descriptions</span></span>

<span data-ttu-id="d09bc-192">이 확장을 사용하여 화면 읽기 프로그램에서 읽을 수 있으나 게시된 페이지에서 시각적으로 렌더링되지 않는 긴 설명이 포함된 이미지도 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="d09bc-193">그래프와 같은 복잡한 이미지의 접근성을 높이기 위해서는 긴 설명이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="d09bc-194">구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="d09bc-195">`type="complex"`인 경우 `source`, `alt-text`, 긴 설명 및 `:::image-end:::` 태그가 모두 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="d09bc-196">loc-scope 지정</span><span class="sxs-lookup"><span data-stu-id="d09bc-196">Specifying loc-scope</span></span>

<span data-ttu-id="d09bc-197">이미지가 포함된 문서 또는 모듈의 지역화 범위와 해당 이미지의 지역화 범위가 서로 다른 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="d09bc-198">이로 인해 글로벌 환경이 잘못되는 경우가 발생할 수 있습니다. 예를 들어 제품의 스크린샷이 해당 제품을 사용할 수 없는 언어로 잘못 지역화되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="d09bc-199">이러한 문제를 방지하기 위해 `content` 및 `complex` 형식의 이미지에 선택적 `loc-scope` 특성을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="d09bc-200">아이콘</span><span class="sxs-lookup"><span data-stu-id="d09bc-200">Icons</span></span>

<span data-ttu-id="d09bc-201">이미지 확장에서는 아이콘을 지원합니다. 아이콘은 장식용 이미지이며 대체 텍스트를 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="d09bc-202">아이콘 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="d09bc-203">`type="icon"`인 경우 `source`만 지정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="d09bc-204">포함된 Markdown 파일</span><span class="sxs-lookup"><span data-stu-id="d09bc-204">Included Markdown files</span></span>

<span data-ttu-id="d09bc-205">Markdown 파일이 여러 문서에서 반복되어야 하는 경우 포함 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="d09bc-206">포함 기능은 빌드할 때 참조를 포함 파일의 콘텐츠로 바꾸도록 Docs에 지시합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="d09bc-207">포함 기능은 다음과 같은 방법으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="d09bc-208">인라인: 한 문장 내에서 일반적인 텍스트 코드 조각 인라인을 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="d09bc-209">블록: 전체 Markdown 파일을 문서의 섹션 내에 중첩된 블록으로 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="d09bc-210">인라인 또는 블록 포함 파일은 Markdown(.md) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="d09bc-211">유효한 Markdown을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="d09bc-212">포함 파일은 대개 리포지토리 루트에 있는 일반적인 ‘포함’ 하위 디렉터리에 있습니다. </span><span class="sxs-lookup"><span data-stu-id="d09bc-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="d09bc-213">문서가 게시되는 경우 포함되는 파일은 게시 문서에 원활하게 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="d09bc-214">포함 구문</span><span class="sxs-lookup"><span data-stu-id="d09bc-214">Includes syntax</span></span>

<span data-ttu-id="d09bc-215">블록 포함은 자체 줄로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="d09bc-216">인라인 포함은 줄 내에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="d09bc-217">여기서, `<title>`은 파일의 이름이고 `<filepath>`는 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="d09bc-218">`INCLUDE`는 대문자여야 하며 `<title>` 앞에는 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="d09bc-219">포함되는 파일의 요구 사항 및 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="d09bc-220">블록 포함되는 내용은 한두 개의 단락, 공유 프로시저 또는 공유 섹션과 같은 많은 양의 콘텐츠에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d09bc-221">문장보다 작은 단위에 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d09bc-222">포함은 Docs 확장을 기반으로 하므로 문서의 GitHub로 렌더링된 보기에서 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="d09bc-223">게시 후에만 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d09bc-224">포함 파일의 모든 텍스트는 포함을 참조하는 문서의 앞 텍스트나 뒤 텍스트에 종속되지 않는 완전한 문장 또는 구문으로 작성되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="d09bc-225">이 지침을 무시하면 문서에 번역할 수 없는 문자열이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="d09bc-226">포함 파일이 다른 포함 파일 내에 포함되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="d09bc-227">미디어 파일을 포함 하위 디렉터리의 미디어 폴더(예: `<repo>` */includes/media* 폴더)에 배치합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="d09bc-228">‘미디어’ 디렉터리는 해당 루트에 이미지를 포함하지 않아야 합니다. </span><span class="sxs-lookup"><span data-stu-id="d09bc-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="d09bc-229">포함에 이미지가 없는 경우 해당 ‘미디어’ 디렉터리가 필요하지 않습니다. </span><span class="sxs-lookup"><span data-stu-id="d09bc-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="d09bc-230">정규 문서에서 포함되는 내용 파일 간에 미디어를 공유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d09bc-231">각 포함되는 내용 및 문서에 고유한 이름을 가진 별도의 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="d09bc-232">포함되는 내용과 연결된 미디어 폴더에 미디어 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="d09bc-233">포함되는 내용을 문서의 유일한 콘텐츠로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="d09bc-234">포함되는 내용은 나머지 문서에서 콘텐츠를 보충해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="d09bc-235">링크</span><span class="sxs-lookup"><span data-stu-id="d09bc-235">Links</span></span>

<span data-ttu-id="d09bc-236">링크 구문에 대한 자세한 내용은 [설명서에서 링크 사용](how-to-write-links.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="d09bc-237">목록(번호 매김, 글머리 기호, 검사 목록)</span><span class="sxs-lookup"><span data-stu-id="d09bc-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="d09bc-238">번호 매기기 목록</span><span class="sxs-lookup"><span data-stu-id="d09bc-238">Numbered list</span></span>

<span data-ttu-id="d09bc-239">번호 매기기 목록을 만들기 위해 모두 1을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="d09bc-240">번호는 게시될 때 오름차순의 순차적 목록으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="d09bc-241">소스 가독성을 높이기 위해 수동으로 목록을 증분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="d09bc-242">중첩 목록을 포함하여 목록에 문자를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="d09bc-243">문자는 Docs에 게시할 때 제대로 렌더링되지 않습니다. 숫자를 사용하여 중첩된 목록은 게시될 때 소문자로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="d09bc-244">예:</span><span class="sxs-lookup"><span data-stu-id="d09bc-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="d09bc-245">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-245">This renders as follows:</span></span>

1. <span data-ttu-id="d09bc-246">This is</span><span class="sxs-lookup"><span data-stu-id="d09bc-246">This is</span></span>
1. <span data-ttu-id="d09bc-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="d09bc-247">a parent numbered list</span></span>
   1. <span data-ttu-id="d09bc-248">and this is</span><span class="sxs-lookup"><span data-stu-id="d09bc-248">and this is</span></span>
   1. <span data-ttu-id="d09bc-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="d09bc-249">a nested numbered list</span></span>
1. <span data-ttu-id="d09bc-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="d09bc-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="d09bc-251">글머리 기호 목록</span><span class="sxs-lookup"><span data-stu-id="d09bc-251">Bulleted list</span></span>

<span data-ttu-id="d09bc-252">글머리 기호 목록을 만들려면 각 줄의 시작 위치에 `-` 또는 `*`와 공백을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="d09bc-253">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-253">This renders as follows:</span></span>

- <span data-ttu-id="d09bc-254">This is</span><span class="sxs-lookup"><span data-stu-id="d09bc-254">This is</span></span>
- <span data-ttu-id="d09bc-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="d09bc-255">a parent bulleted list</span></span>
  - <span data-ttu-id="d09bc-256">and this is</span><span class="sxs-lookup"><span data-stu-id="d09bc-256">and this is</span></span>
  - <span data-ttu-id="d09bc-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="d09bc-257">a nested bulleted list</span></span>
- <span data-ttu-id="d09bc-258">All done!</span><span class="sxs-lookup"><span data-stu-id="d09bc-258">All done!</span></span>

<span data-ttu-id="d09bc-259">어떤 구문을 사용하든 문서 내에서 `-` 또는 `*`를 일관성 있게 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="d09bc-260">검사 목록</span><span class="sxs-lookup"><span data-stu-id="d09bc-260">Checklist</span></span>

<span data-ttu-id="d09bc-261">검사 목록은 사용자 지정 Markdown 확장을 통해 Docs에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="d09bc-262">이 예제에서는 다음과 같이 Docs에서 렌더링합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d09bc-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="d09bc-263">List item 1</span></span>
> * <span data-ttu-id="d09bc-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="d09bc-264">List item 2</span></span>
> * <span data-ttu-id="d09bc-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="d09bc-265">List item 3</span></span>

<span data-ttu-id="d09bc-266">문서의 처음이나 끝에 있는 검사 목록을 사용하여 “학습할 내용” 또는 “학습한 내용” 콘텐츠를 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="d09bc-267">문서 전체에 임의의 검사 목록을 추가하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="d09bc-268">다음 단계 작업</span><span class="sxs-lookup"><span data-stu-id="d09bc-268">Next step action</span></span>

<span data-ttu-id="d09bc-269">사용자 지정 확장을 사용하여 Docs 페이지에 다음 단계 작업 단추를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="d09bc-270">구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="d09bc-271">예:</span><span class="sxs-lookup"><span data-stu-id="d09bc-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="d09bc-272">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d09bc-273">문서에 코드를 추가하는 방법 알아보기</span><span class="sxs-lookup"><span data-stu-id="d09bc-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="d09bc-274">다른 웹 페이지에 대한 Markdown 링크를 포함하여 다음 단계 작업에서 지원되는 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="d09bc-275">대부분의 경우 다음 작업 링크는 동일한 문서 집합에 있는 다른 파일에 대한 상대 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="d09bc-276">지역화되지 않은 문자열</span><span class="sxs-lookup"><span data-stu-id="d09bc-276">Non-localized strings</span></span>

<span data-ttu-id="d09bc-277">사용자 지정 `no-loc` Markdown 확장을 사용하여 지역화 프로세스에서 무시할 콘텐츠 문자열을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="d09bc-278">호출되는 모든 문자열은 대/소문자를 구분합니다. 즉, 지역화에서 무시되려면 문자열이 정확하게 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="d09bc-279">개별 문자열을 지역화 불가능으로 표시하려면 다음 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="d09bc-280">예를 들어 다음에서 `Document`의 단일 인스턴스만 지역화 프로세스 중에 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="d09bc-281">`\`를 사용하여 특수 문자를 이스케이프하세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="d09bc-282">YAML 헤더의 메타데이터를 사용하여 현재 Markdown 파일 내에 있는 한 문자열의 모든 인스턴스를 지역화 불가능으로 표시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="d09bc-283">no-loc 메타데이터는 *docfx.json* 파일의 글로벌 메타데이터로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="d09bc-284">지역화 파이프라인에서 *docfx.json* 파일을 읽지 않으므로 각 개별 소스 파일에 no-loc 메타데이터를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="d09bc-285">다음 예제에서는 메타데이터 `title` 및 Markdown 헤더 둘 다에서 지역화 프로세스 중에 `Document`라는 단어를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="d09bc-286">메타데이터 `description` 및 Markdown 주 콘텐츠에 있는 `document` 단어는 대문자 `D`로 시작하지 않기 때문에 지역화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="d09bc-287">선택기</span><span class="sxs-lookup"><span data-stu-id="d09bc-287">Selectors</span></span>

<span data-ttu-id="d09bc-288">선택기는 사용자가 동일한 문서의 여러 버전 간에 전환할 수 있도록 해주는 UI 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="d09bc-289">일부 문서 집합에서는 기술 또는 플랫폼 간의 구현 차이를 해결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d09bc-290">선택기는 일반적으로 개발자를 위한 모바일 플랫폼 콘텐츠에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="d09bc-291">동일한 선택기 Markdown은 선택기를 사용하는 각 문서 파일에 포함되므로 문서 선택기를 포함 파일에 배치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="d09bc-292">그러면 동일한 선택기를 사용하는 모든 문서 파일에서 해당 포함 파일을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="d09bc-293">선택기의 종류에는 단일 선택기와 다중 선택기 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="d09bc-294">단일 선택기</span><span class="sxs-lookup"><span data-stu-id="d09bc-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="d09bc-295">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="d09bc-304">다중 선택기</span><span class="sxs-lookup"><span data-stu-id="d09bc-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="d09bc-305">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="플랫폼" title2="백 엔드"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universal C# | .NET)](how-to-write-links.md)
> - [(Windows universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="d09bc-318">아래 첨자 및 위 첨자</span><span class="sxs-lookup"><span data-stu-id="d09bc-318">Subscript and superscript</span></span>

<span data-ttu-id="d09bc-319">아래 첨자나 위 첨자는 수학적 수식에 대한 문서를 작성하는 경우와 같이 기술적 정확도를 위해 필요한 경우에만 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="d09bc-320">각주와 같은 비표준 스타일에는 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d09bc-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="d09bc-321">아래 첨자 및 위 첨자 둘 다 HTML을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="d09bc-322">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-322">This renders as follows:</span></span>

<span data-ttu-id="d09bc-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="d09bc-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="d09bc-324">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-324">This renders as follows:</span></span>

<span data-ttu-id="d09bc-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="d09bc-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="d09bc-326">Tables</span><span class="sxs-lookup"><span data-stu-id="d09bc-326">Tables</span></span>

<span data-ttu-id="d09bc-327">Markdown에서 테이블을 만드는 가장 간단한 방법은 파이프 및 줄을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="d09bc-328">헤더가 있는 표준 테이블을 만들려면 첫 번째 선을 파선으로 그립니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="d09bc-329">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-329">This renders as follows:</span></span>

|<span data-ttu-id="d09bc-330">This is</span><span class="sxs-lookup"><span data-stu-id="d09bc-330">This is</span></span>   |<span data-ttu-id="d09bc-331">a simple</span><span class="sxs-lookup"><span data-stu-id="d09bc-331">a simple</span></span>   |<span data-ttu-id="d09bc-332">table header</span><span class="sxs-lookup"><span data-stu-id="d09bc-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="d09bc-333">table</span><span class="sxs-lookup"><span data-stu-id="d09bc-333">table</span></span>     |<span data-ttu-id="d09bc-334">data</span><span class="sxs-lookup"><span data-stu-id="d09bc-334">data</span></span>       |<span data-ttu-id="d09bc-335">here</span><span class="sxs-lookup"><span data-stu-id="d09bc-335">here</span></span>        |
|<span data-ttu-id="d09bc-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="d09bc-336">it doesn't</span></span>|<span data-ttu-id="d09bc-337">actually</span><span class="sxs-lookup"><span data-stu-id="d09bc-337">actually</span></span>   |<span data-ttu-id="d09bc-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="d09bc-338">have to line up nicely!</span></span>||

<span data-ttu-id="d09bc-339">콜론을 사용하여 열을 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d09bc-340">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-340">Renders as follows:</span></span>

| <span data-ttu-id="d09bc-341">Fun</span><span class="sxs-lookup"><span data-stu-id="d09bc-341">Fun</span></span>                  | <span data-ttu-id="d09bc-342">With</span><span class="sxs-lookup"><span data-stu-id="d09bc-342">With</span></span>                 | <span data-ttu-id="d09bc-343">Tables</span><span class="sxs-lookup"><span data-stu-id="d09bc-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d09bc-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d09bc-344">left-aligned column</span></span>  | <span data-ttu-id="d09bc-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d09bc-345">right-aligned column</span></span> | <span data-ttu-id="d09bc-346">centered column</span><span class="sxs-lookup"><span data-stu-id="d09bc-346">centered column</span></span> |
| <span data-ttu-id="d09bc-347">$100</span><span class="sxs-lookup"><span data-stu-id="d09bc-347">$100</span></span>                 | <span data-ttu-id="d09bc-348">$100</span><span class="sxs-lookup"><span data-stu-id="d09bc-348">$100</span></span>                 | <span data-ttu-id="d09bc-349">$100</span><span class="sxs-lookup"><span data-stu-id="d09bc-349">$100</span></span>            |
| <span data-ttu-id="d09bc-350">$10</span><span class="sxs-lookup"><span data-stu-id="d09bc-350">$10</span></span>                  | <span data-ttu-id="d09bc-351">$10</span><span class="sxs-lookup"><span data-stu-id="d09bc-351">$10</span></span>                  | <span data-ttu-id="d09bc-352">$10</span><span class="sxs-lookup"><span data-stu-id="d09bc-352">$10</span></span>             |
| <span data-ttu-id="d09bc-353">$1</span><span class="sxs-lookup"><span data-stu-id="d09bc-353">$1</span></span>                   | <span data-ttu-id="d09bc-354">$1</span><span class="sxs-lookup"><span data-stu-id="d09bc-354">$1</span></span>                   | <span data-ttu-id="d09bc-355">$1</span><span class="sxs-lookup"><span data-stu-id="d09bc-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="d09bc-356">VS Code용 Docs Authoring Extension을 사용하면 기본 Markdown 테이블을 쉽게 추가할 수 있습니다!</span><span class="sxs-lookup"><span data-stu-id="d09bc-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="d09bc-357">[온라인 테이블 생성기](http://www.tablesgenerator.com/markdown_tables)를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="d09bc-358">테이블 셀에 있는 단어 내 줄 바꿈</span><span class="sxs-lookup"><span data-stu-id="d09bc-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="d09bc-359">Markdown 테이블에 긴 단어가 있으면 테이블이 오른쪽 탐색으로 확장되어 읽지 못하게 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="d09bc-360">필요한 경우 Docs 렌더링에서 단어 내에 줄 바꿈을 자동으로 삽입하도록 허용하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="d09bc-361">`[!div class="mx-tdBreakAll"]` 사용자 지정 클래스로 테이블을 래핑하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="d09bc-362">다음은 클래스 이름이 `mx-tdBreakAll`인 `div`로 래핑될 행이 세 개인 테이블의 Markdown 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="d09bc-363">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="d09bc-364">Name</span><span class="sxs-lookup"><span data-stu-id="d09bc-364">Name</span></span>|<span data-ttu-id="d09bc-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="d09bc-365">Syntax</span></span>|<span data-ttu-id="d09bc-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="d09bc-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="d09bc-367">Description</span><span class="sxs-lookup"><span data-stu-id="d09bc-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="d09bc-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="d09bc-368">Quiet</span></span>|<span data-ttu-id="d09bc-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="d09bc-369">/quiet</span></span>|<span data-ttu-id="d09bc-370">Yes</span><span class="sxs-lookup"><span data-stu-id="d09bc-370">Yes</span></span>|<span data-ttu-id="d09bc-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="d09bc-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="d09bc-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="d09bc-372">NoRestart</span></span>|<span data-ttu-id="d09bc-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="d09bc-373">/norestart</span></span>|<span data-ttu-id="d09bc-374">No</span><span class="sxs-lookup"><span data-stu-id="d09bc-374">No</span></span>|<span data-ttu-id="d09bc-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="d09bc-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="d09bc-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="d09bc-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="d09bc-377">Help</span><span class="sxs-lookup"><span data-stu-id="d09bc-377">Help</span></span>|<span data-ttu-id="d09bc-378">/help</span><span class="sxs-lookup"><span data-stu-id="d09bc-378">/help</span></span>|<span data-ttu-id="d09bc-379">No</span><span class="sxs-lookup"><span data-stu-id="d09bc-379">No</span></span>|<span data-ttu-id="d09bc-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="d09bc-380">Provides help and quick reference.</span></span> <span data-ttu-id="d09bc-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="d09bc-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="d09bc-382">두 번째 열 테이블 셀에 있는 단어 내 줄 바꿈</span><span class="sxs-lookup"><span data-stu-id="d09bc-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="d09bc-383">테이블의 두 번째 열에 있는 단어 내에서만 줄 바꿈이 자동으로 삽입되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="d09bc-384">줄 바꿈을 두 번째 열로 제한하려면 앞에 표시된 대로 `div` 래퍼 구문을 사용하여 `mx-tdCol2BreakAll` 클래스를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="d09bc-385">데이터 행렬 테이블</span><span class="sxs-lookup"><span data-stu-id="d09bc-385">Data matrix tables</span></span>

<span data-ttu-id="d09bc-386">데이터 행렬 테이블에는 헤더와 첫 번째 가중 열이 둘 다 있으므로 왼쪽 상단에 빈 셀이 있는 행렬을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="d09bc-387">문서에는 데이터 행렬 테이블에 대한 사용자 지정 Markdown이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="d09bc-388">첫 번째 열의 모든 항목은 '굵게'(`**bold**`)로 스타일을 지정해야 합니다. 그렇지 않으면 화면 읽기 프로그램에서 테이블에 액세스할 수 없거나 문서가 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="d09bc-389">HTML 테이블</span><span class="sxs-lookup"><span data-stu-id="d09bc-389">HTML Tables</span></span>

<span data-ttu-id="d09bc-390">HTML 테이블은 docs.microsoft.com에 사용하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="d09bc-391">사용자가 소스를 읽을 수 없습니다. 사용자가 소스를 읽을 수 없도록 하는 것이 Markdown의 핵심 원칙입니다.</span><span class="sxs-lookup"><span data-stu-id="d09bc-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
