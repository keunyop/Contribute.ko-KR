---
title: PowerShell 문서용 템플릿 및 치트 시트
description: 이 문서에는 PowerShell 문서에 대한 새 문서를 만드는 데 사용할 수 있는 편리한 템플릿이 포함되어 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331932"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="a321b-103">PowerShell-Docs에 대한 Markdown 스타일 가이드</span><span class="sxs-lookup"><span data-stu-id="a321b-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="a321b-104">이 문서에서는 PowerShell-Docs 콘텐츠에 관련된 몇 가지 스타일 지침을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="a321b-105">기타 쓰기 스타일 지침은 [Microsoft 스타일 가이드](https://docs.microsoft.com/style-guide/welcome/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="a321b-106">메타데이터</span><span class="sxs-lookup"><span data-stu-id="a321b-106">Metadata</span></span>

<span data-ttu-id="a321b-107">이 템플릿에는 Markdown 구문의 예와 메타데이터 설정에 대한 지침이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="a321b-108">Markdown 파일을 만들 때 포함된 템플릿을 새 파일로 복사하여 아래 지정된 대로 메타데이터를 채우고 위의 H1 제목을 문서 제목으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="a321b-109">필요한 메타데이터 블록은 다음 샘플 메타데이터 블록에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="a321b-110">콜론(:)과 메타데이터 요소의 값 사이에는 공백이 **있어야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="a321b-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="a321b-111">값의 콜론(예: 제목)이 메타데이터 구문 분석기를 중단시킵니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="a321b-112">이 경우 제목을 큰따옴표로 둘러쌉니다(예: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="a321b-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="a321b-113">**author**: 작성자 필드에는 작성자의 **GitHub 사용자 이름**이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="a321b-114">**description**: 문서의 내용을 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="a321b-115">일반적으로 검색 결과 페이지에 표시되지만 검색 순위 지정에는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="a321b-116">길이는 공백을 포함하여 115-145자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="a321b-117">**ms.date**: 마지막 중요 업데이트 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="a321b-118">전체 문서를 검토하고 업데이트한 경우 기존 문서에서 이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="a321b-119">오타와 같은 작은 수정 사항은 업데이트를 보증하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="a321b-120">**title**: 검색 엔진 결과에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="a321b-121">제목은 H1 제목의 제목과 동일해서는 안 되며 60자 이하여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="a321b-122">각 문서에 다른 메타데이터가 연결되어 있지만 일반적으로 **docfx.json**에 지정된 폴더 수준에서 대부분의 메타데이터 값을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="a321b-123">제품 용어</span><span class="sxs-lookup"><span data-stu-id="a321b-123">Product Terminology</span></span>

<span data-ttu-id="a321b-124">PowerShell의 여러 가지 변형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="a321b-125">이 표에서는 PowerShell 설명에 사용되는 몇 가지 용어를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="a321b-126">**PowerShell** - 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="a321b-127">PowerShell은 Microsoft에서 제공하는 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="a321b-128">PowerShell이라는 용어는 제품의 모든 버전을 설명하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="a321b-129">**PowerShell Core** - 지원되는 플랫폼용으로 .NET Core 공용 언어 런타임(CoreCLR)에 빌드된 PowerShell입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="a321b-130">**Windows PowerShell** - .NET Framework CLR(공용 언어 런타임)에 빌드된 PowerShell입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="a321b-131">Windows PowerShell은 Windows에서만 제공되며 전체 .NET Framework CLR이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="a321b-132">일반적으로 문서의 “Windows PowerShell”에 대한 참조는 “PowerShell”로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="a321b-133">Windows 특정 기술을 설명하는 동안 “Windows PowerShell”을 변경해서는 **안 됩니다**.</span><span class="sxs-lookup"><span data-stu-id="a321b-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="a321b-134">기본 Markdown, GFM 및 특수 문자</span><span class="sxs-lookup"><span data-stu-id="a321b-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="a321b-135">[Markdown 참조](../markdown-reference.md) 문서에서 Markdown, GFM(GitHub Flavored Markdown) 및 OPS 관련 확장에 대한 기본 사항을 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="a321b-136">Markdown은 서식 지정에 \*, \` 및 \#과 같은 특수 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="a321b-137">콘텐츠에 이러한 문자 중 하나를 포함하려면 다음 두 가지 작업 중 하나를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="a321b-138">특수 문자 앞에 백슬래시를 두어 “이스케이프”합니다(예:\*의 경우 `\*`).</span><span class="sxs-lookup"><span data-stu-id="a321b-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="a321b-139">문자에 대해 [HTML 엔터티 코드](http://www.ascii.cl/htmlcodes.htm)를 사용합니다(예:&#42;의 경우 `&#42;`).</span><span class="sxs-lookup"><span data-stu-id="a321b-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="a321b-140">Markdown 파일은 일반 ASCII 텍스트 또는 UTF-8 인코딩을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="a321b-141">그러나 다중 바이트 UTF-8 문자를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="a321b-142">대신, HTML 엔터티를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-142">Instead use an HTML entity.</span></span> <span data-ttu-id="a321b-143">예를 들어 저작권 기호에는 `&copy;`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="a321b-144">“&copy;”로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="a321b-145">하이퍼링크</span><span class="sxs-lookup"><span data-stu-id="a321b-145">Hyperlinks</span></span>

- <span data-ttu-id="a321b-146">Bare URL을 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-146">Avoid using bare URLs.</span></span> <span data-ttu-id="a321b-147">링크는 Markdown 구문 `[friendlyname](url-or-path)`를 사용해야 함</span><span class="sxs-lookup"><span data-stu-id="a321b-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="a321b-148">링크에는 일반적으로 연결된 항목의 제목인 식별 이름이 있어야 함</span><span class="sxs-lookup"><span data-stu-id="a321b-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="a321b-149">아래쪽 “관련 링크” 섹션에 있는 모든 항목은 하이퍼링크로 연결되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="a321b-150">**docs.microsoft.com**에서 호스트되는 다른 콘텐츠에 연결할 때 상대 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="a321b-151">하이퍼링크의 대괄호 안에 억음 악센트, 굵게 또는 기타 태그를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="a321b-152">연결에 대한 자세한 내용은 [문서에서 링크 사용](../how-to-write-links.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="a321b-153">파일 이름</span><span class="sxs-lookup"><span data-stu-id="a321b-153">Filenames</span></span>

<span data-ttu-id="a321b-154">파일 이름에는 다음 규칙이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="a321b-155">문자, 숫자 및 하이픈만 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="a321b-156">공백 또는 문장 부호를 사용하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="a321b-157">파일 이름에서 단어와 숫자를 구분하려면 하이픈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="a321b-158">개발, 구매, 빌드, 문제 해결과 같은 특정 동작을 나타내는 동사를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="a321b-159">-ing 형식의 단어는 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-159">No -ing words.</span></span>
- <span data-ttu-id="a321b-160">짧은 단어는 사용하지 않습니다. a, and, the, in, or 등은 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="a321b-161">Markdown에 있어야 하며 .md 파일 확장명을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="a321b-162">파일 이름을 합리적으로 짧게 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-162">Keep file names reasonably short.</span></span> <span data-ttu-id="a321b-163">이는 문서에 대한 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="a321b-164">빈 줄, 공백 및 탭</span><span class="sxs-lookup"><span data-stu-id="a321b-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="a321b-165">중복된 빈 줄을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="a321b-166">여러 빈 줄은 HTML에서 하나의 빈 줄로 렌더링되므로 여러 빈 줄을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="a321b-167">또한 빈 줄은 Markdown에서 블록의 끝을 알립니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="a321b-168">다양한 형식의 Markdown 블록 사이(예: 단락과 목록 또는 헤더 사이)에 하나의 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="a321b-169">Markdown에서는 간격이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="a321b-170">항상 하드 탭 대신 공백을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="a321b-171">줄 끝에서 추가 공백을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="a321b-172">제목</span><span class="sxs-lookup"><span data-stu-id="a321b-172">Titles and headings</span></span>

<span data-ttu-id="a321b-173">[ATX 제목][atx](# 스타일, `=` 또는 `-` 스타일 헤더가 아님)만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="a321b-174">문장 대/소문자 사용 - 적절한 명사 및 제목이나 헤더의 첫 번째 문자만 대문자로 시작되어야 함</span><span class="sxs-lookup"><span data-stu-id="a321b-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="a321b-175">`#`과 제목의 첫 번째 문자 사이에는 단일 공백이 있어야 함</span><span class="sxs-lookup"><span data-stu-id="a321b-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="a321b-176">제목은 하나의 빈 줄로 둘러싸야 함</span><span class="sxs-lookup"><span data-stu-id="a321b-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="a321b-177">문서당 하나의 H1만</span><span class="sxs-lookup"><span data-stu-id="a321b-177">Only one H1 per document</span></span>
- <span data-ttu-id="a321b-178">헤더 수준은 1씩 증가해야 함 - 수준을 건너뛰지 않음</span><span class="sxs-lookup"><span data-stu-id="a321b-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="a321b-179">억음 악센트, 굵게 또는 기타 태그를 사용하지 않음</span><span class="sxs-lookup"><span data-stu-id="a321b-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="a321b-180">cmdlet 참조를 위해 [PlatyPS][platyPS]가 적용한 스키마에는 특정 H2 및 H3 헤더가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="a321b-181">헤더를 추가하거나 제거하면 빌드가 중단될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="a321b-182">자세한 내용은 [cmdlet 참조 스타일 가이드](powershell-style-reference.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="a321b-183">줄 길이를 100자로 제한</span><span class="sxs-lookup"><span data-stu-id="a321b-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="a321b-184">이 항목은 차이 및 기록의 명령줄 출력을 간소화합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="a321b-185">이 규칙은 PowerShell-Docs의 많은 기존 콘텐츠에 적용되지 않지만 시간이 지나면서 관련 작업이 진행되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="a321b-186">자유롭게 지원할 수 있습니다. VSCode(Visual Studio Code)의 [재배치 확장][reflow]을 통해 이 제한에 따라 손쉽게 단락 서식을 다시 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="a321b-187">목록</span><span class="sxs-lookup"><span data-stu-id="a321b-187">Lists</span></span>

<span data-ttu-id="a321b-188">목록에 여러 문장이나 단락이 포함된 경우 목록이 아닌 하위 수준 헤더를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="a321b-189">목록은 하나의 빈 줄로 둘러싸야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="a321b-190">정렬되지 않은 목록</span><span class="sxs-lookup"><span data-stu-id="a321b-190">Unordered lists</span></span>

<span data-ttu-id="a321b-191">여러 문장이 포함되지 않은 경우에는 마침표로 목록 항목을 종료하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="a321b-192">목록 항목 글머리 기호에 하이픈 문자(`-`)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="a321b-193">이렇게 하면 별표[`*`]를 사용하는 굵게 또는 기울임꼴 태그와 혼동되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="a321b-194">글머리 기호 항목 아래에 단락이나 다른 요소를 포함하려면 줄 바꿈을 삽입하고 글머리 기호 뒤 첫 번째 문자에 들여쓰기를 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="a321b-195">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="a321b-196">이것은 글머리 기호 항목 아래에 하위 요소를 포함하는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="a321b-197">첫 번째 글머리 기호 항목</span><span class="sxs-lookup"><span data-stu-id="a321b-197">First bullet item</span></span>

  <span data-ttu-id="a321b-198">첫 번째 글머리 기호를 설명하는 문장입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="a321b-199">하위 머리 기호 항목</span><span class="sxs-lookup"><span data-stu-id="a321b-199">Sub-bullet item</span></span>

    <span data-ttu-id="a321b-200">하위 글머리 기호를 설명하는 문장입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="a321b-201">두 번째 글머리 기호 항목</span><span class="sxs-lookup"><span data-stu-id="a321b-201">Second bullet item</span></span>
- <span data-ttu-id="a321b-202">세 번째 글머리 기호 항목</span><span class="sxs-lookup"><span data-stu-id="a321b-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="a321b-203">정렬된 목록</span><span class="sxs-lookup"><span data-stu-id="a321b-203">Ordered lists</span></span>

<span data-ttu-id="a321b-204">번호가 매겨진 항목 아래에 단락이나 다른 요소를 포함하려면 항목 번호 뒤 첫 번째 문자에 들여쓰기를 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="a321b-205">이 출력을 가져오려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-205">to get this output:</span></span>

> 1. <span data-ttu-id="a321b-206">첫 번째 요소의 경우 1 뒤에 단일 공백을 삽입합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="a321b-207">긴 문장은 다음 줄로 래핑되어야 하며 번호가 매겨진 목록 마커 뒤 첫 번째 문자에 맞춰 정렬되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="a321b-208">이 요소 같은 두 번째 요소를 포함하려면 첫 번째 요소 뒤에 줄 바꿈을 삽입하고 들여쓰기를 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="a321b-209">두 번째 요소의 들여쓰기는 번호가 매겨진 목록 마커 뒤 첫 번째 문자에 맞춰 정렬되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="a321b-210">이 항목 같은 단일 숫자 항목의 경우 열 4로 들여 씁니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="a321b-211">2자리 숫자 항목(예: 항목 번호 10)의 경우 열 5로 들여 씁니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="a321b-212">번호가 매겨진 다음 항목이 여기에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-212">The next numbered item starts here.</span></span>

<span data-ttu-id="a321b-213">번호가 매겨진 목록의 모든 항목은 항목별로 증분하는 대신 숫자 `1.`를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="a321b-214">Markdown 렌더링은 값을 자동으로 증분합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="a321b-215">이로 인해 항목이 더 쉽게 다시 정렬되며 하위 콘텐츠의 들여쓰기가 표준화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="a321b-216">명령 구문 요소 서식 지정</span><span class="sxs-lookup"><span data-stu-id="a321b-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="a321b-217">PowerShell cmdlet 이름은 [파스칼식 대/소문자로 지정][pascal-case]됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="a321b-218">동사는 하이픈으로 명사와 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="a321b-219">cmdlet 및 매개 변수에는 항상 전체 파스칼 대/소문자 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="a321b-220">특별히 별칭을 설명하지 않는 경우에는 별칭을 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="a321b-221">단락 내에서 언어 키워드, cmdlet 이름 및 변수는 억음 악센트(`` ` ``) 문자로 래핑되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="a321b-222">속성, 매개 변수 및 클래스 이름은 **굵게** 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="a321b-223">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="a321b-224">이름으로 매개 변수를 참조하는 경우 이름은 **굵게** 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="a321b-225">하이픈 접두사로 매개 변수 사용을 나타내는 경우 매개 변수는 억음 악센트로 래핑되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="a321b-226">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="a321b-227">외부 명령(EXE, 스크립트 등)을 참조하는 경우 명령 이름은 굵게 표시되고, 모두 소문자이며(또는 문장의 시작 구분인 경우 대문자로 시작됨), 적절한 파일 확장명을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="a321b-228">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="a321b-229">외부 명령의 사용 예제를 표시하는 경우 예제는 억음 악센트로 래핑되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="a321b-230">별칭과 이름이 충돌하는 경우 명령 예제에 파일 확장명을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="a321b-231">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="a321b-232">개념 문서(참조 콘텐츠가 아님)를 작성하는 경우 cmdlet 이름의 첫 번째 인스턴스는 cmdlet 문서에 연결되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="a321b-233">하이퍼링크의 대괄호 안에 억음 악센트, 굵게 또는 기타 태그를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="a321b-234">예:</span><span class="sxs-lookup"><span data-stu-id="a321b-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="a321b-235">자세한 내용은 스타일 가이드의 [하이퍼링크](#hyperlinks) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a321b-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="a321b-236">이미지</span><span class="sxs-lookup"><span data-stu-id="a321b-236">Images</span></span>

<span data-ttu-id="a321b-237">이미지를 포함하는 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="a321b-238">예제:</span><span class="sxs-lookup"><span data-stu-id="a321b-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="a321b-239">여기서 `alt text`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="a321b-240">시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="a321b-241">이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="a321b-242">이미지는 문서를 포함하는 폴더 내의 `media/<article-name>` 폴더에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="a321b-243">이미지는 문서 간에 공유되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-243">Images should not be shared between articles.</span></span> <span data-ttu-id="a321b-244">`media` 폴더 아래 문서의 파일 이름과 일치하는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="a321b-245">해당 문서의 이미지를 해당하는 새 폴더로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="a321b-246">이미지가 여러 문서에서 사용되는 경우 각 이미지 폴더에는 해당 이미지 파일의 복사본이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="a321b-247">이 사례에서는 다른 문서에 영향을 주는 문서에서 이미지가 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="a321b-248">경우에 따라 여러 문서에서 로고 및 아이콘 같은 이미지를 공유하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="a321b-249">이 이미지는 리포지토리의 루트에 있는 `/media/shared` 폴더에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a321b-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="a321b-250">지원되는 이미지 파일 형식은 \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg임</span><span class="sxs-lookup"><span data-stu-id="a321b-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
