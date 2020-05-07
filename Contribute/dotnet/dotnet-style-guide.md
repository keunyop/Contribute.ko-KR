---
title: .NET 문서용 템플릿 및 치트 시트
description: 이 문서에는 .NET 문서 리포지토리에 대한 새 문서를 작성하는 데 사용할 수 있는 편리한 템플릿이 포함되어 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: a520112cd77f4c4807e7719c2c4dbd43a762f062
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "80759567"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="b3c0f-103">.NET 문서용 메타데이터 및 Markdown 템플릿</span><span class="sxs-lookup"><span data-stu-id="b3c0f-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="b3c0f-104">이 dotnet/docs 템플릿에는 Markdown 구문의 예와 메타데이터 설정에 대한 지침이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="b3c0f-105">Markdown 파일을 만들 때 포함된 템플릿을 새 파일로 복사하여 아래 지정된 대로 메타데이터를 채우고 위의 H1 제목을 문서 제목으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="b3c0f-106">메타데이터</span><span class="sxs-lookup"><span data-stu-id="b3c0f-106">Metadata</span></span>

<span data-ttu-id="b3c0f-107">필요한 메타데이터 블록은 다음 샘플 메타데이터 블록에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="b3c0f-108">콜론(:)과 메타데이터 요소의 값 사이에는 공백이 **있어야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="b3c0f-109">값의 콜론(예: 제목)이 메타데이터 구문 분석기를 중단시킵니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="b3c0f-110">이 경우 제목을 큰따옴표로 둘러쌉니다(예: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="b3c0f-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="b3c0f-111">**title**: 검색 엔진 결과에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="b3c0f-112">제목은 H1 제목의 제목과 동일해서는 안 되며 60자 이하여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="b3c0f-113">**description**: 문서의 내용을 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="b3c0f-114">일반적으로 검색 결과 페이지에 표시되지만 검색 순위 지정에는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="b3c0f-115">길이는 공백을 포함하여 115-145자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="b3c0f-116">**author**: 작성자 필드에는 작성자의 **GitHub 사용자 이름**이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="b3c0f-117">**ms.date**: 마지막 중요 업데이트 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="b3c0f-118">전체 문서를 검토하고 업데이트한 경우 기존 문서에서 이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="b3c0f-119">오타와 같은 작은 수정 사항은 업데이트를 보증하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="b3c0f-120">각 문서에 다른 메타데이터가 연결되어 있지만 일반적으로 **docfx.json**에 지정된 폴더 수준에서 대부분의 메타데이터 값을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="b3c0f-121">기본 Markdown, GFM 및 특수 문자</span><span class="sxs-lookup"><span data-stu-id="b3c0f-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="b3c0f-122">[Markdown 참조](../markdown-reference.md) 문서에서 Markdown, GFM(GitHub Flavored Markdown) 및 OPS 관련 확장에 대한 기본 사항을 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="b3c0f-123">Markdown은 서식 지정에 \*, \` 및 \#과 같은 특수 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="b3c0f-124">콘텐츠에 이러한 문자 중 하나를 포함하려면 다음 두 가지 작업 중 하나를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="b3c0f-125">특수 문자 앞에 백슬래시를 두어 “이스케이프”합니다(예:\*의 경우 `\*`).</span><span class="sxs-lookup"><span data-stu-id="b3c0f-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="b3c0f-126">문자에 대해 [HTML 엔터티 코드](http://www.ascii.cl/htmlcodes.htm)를 사용합니다(예:&#42;의 경우 `&#42;`).</span><span class="sxs-lookup"><span data-stu-id="b3c0f-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="b3c0f-127">파일 이름</span><span class="sxs-lookup"><span data-stu-id="b3c0f-127">File names</span></span>

<span data-ttu-id="b3c0f-128">파일 이름에는 다음 규칙이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-128">File names use the following rules:</span></span>

* <span data-ttu-id="b3c0f-129">소문자, 숫자 및 하이픈만 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="b3c0f-130">공백 또는 문장 부호를 사용하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="b3c0f-131">파일 이름에서 단어와 숫자를 구분하려면 하이픈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="b3c0f-132">개발, 구매, 빌드, 문제 해결과 같은 특정 동작을 나타내는 동사를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="b3c0f-133">-ing 형식의 단어는 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-133">No -ing words.</span></span>
* <span data-ttu-id="b3c0f-134">짧은 단어는 사용하지 않습니다. a, and, the, in, or 등은 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="b3c0f-135">Markdown에 있어야 하며 .md 파일 확장명을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="b3c0f-136">파일 이름을 합리적으로 짧게 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-136">Keep file names reasonably short.</span></span> <span data-ttu-id="b3c0f-137">이는 문서에 대한 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="b3c0f-138">제목</span><span class="sxs-lookup"><span data-stu-id="b3c0f-138">Headings</span></span>

<span data-ttu-id="b3c0f-139">문장 스타일의 대문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="b3c0f-140">제목의 첫 단어를 항상 대문자로 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="b3c0f-141">텍스트 스타일 지정</span><span class="sxs-lookup"><span data-stu-id="b3c0f-141">Text styling</span></span>

<span data-ttu-id="b3c0f-142">*기울임꼴* 파일, 폴더, 경로(긴 항목의 경우, 해당 행으로 분리), 새 용어에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="b3c0f-143">**Bold** UI 요소에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="b3c0f-144">`Code`인라인 코드, 언어 키워드, NuGet 패키지 이름, 명령줄 명령, 데이터베이스 테이블과 열 이름 및 클릭하지 않을 URL에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="b3c0f-145">링크</span><span class="sxs-lookup"><span data-stu-id="b3c0f-145">Links</span></span>

<span data-ttu-id="b3c0f-146">앵커, 내부 링크, 다른 문서에 대한 링크, 코드 포함 및 외부 링크에 대한 정보는 [링크](../how-to-write-links.md)에 대한 일반 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-146">See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="b3c0f-147">.NET 문서 팀은 다음 규칙을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="b3c0f-148">대부분의 경우 상대 링크는 GitHub의 소스에서 해결되기 때문에 상대 링크를 사용하고, 링크에서 `~/`의 사용을 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="b3c0f-149">그러나 종속 리포지토리의 파일에 연결할 때마다 `~/` 문자를 사용하여 경로를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="b3c0f-150">종속 리포지토리에 있는 파일은 GitHub의 다른 위치에 있기 때문에 링크는 작성된 방법에 관계없이 상대 링크로 올바르게 해결되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="b3c0f-151">C# 언어 사양 및 Visual Basic 언어 사양은 언어 리포지토리의 원본을 포함하여 .NET 문서에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="b3c0f-152">markdown 원본은 [csharplang](https://github.com/dotnet/csharplang) 및 [vblang](https://github.com/dotnet/vblang) 리포지토리에서 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="b3c0f-153">사양에 대한 링크는 해당 사양이 포함된 원본 디렉터리를 가리켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="b3c0f-154">다음 예제와 같이 C#의 경우 **~/_csharplang/spec**이고, VB의 경우 **~/_vblang/spec**입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="b3c0f-155">API에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="b3c0f-155">Links to APIs</span></span>

<span data-ttu-id="b3c0f-156">빌드 시스템에는 외부 링크를 사용하지 않고도 .NET API에 연결할 수 있는 몇 가지 확장 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="b3c0f-157">다음 구문 중 하나를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="b3c0f-158">자동 연결: `<xref:UID>` 또는 `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="b3c0f-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="b3c0f-159">`displayProperty` 쿼리 매개 변수는 정규화된 링크 텍스트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="b3c0f-160">기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="b3c0f-161">Markdown 링크: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="b3c0f-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="b3c0f-162">표시되는 링크 텍스트를 사용자 지정하려면 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="b3c0f-163">예제:</span><span class="sxs-lookup"><span data-stu-id="b3c0f-163">Examples:</span></span>

- <span data-ttu-id="b3c0f-164">`<xref:System.String>`은 [String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="b3c0f-165">`<xref:System.String?displayProperty=nameWithType>`은 [System.String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="b3c0f-166">`[String class](xref:System.String)`은 [String 클래스](https://docs.microsoft.com/dotnet/api/system.string)로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="b3c0f-167">이 표기법 사용에 대한 자세한 내용은 [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)(상호 참조 사용)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="b3c0f-168">일부 UID에는 특수 문자 \`, \# 또는 \*이 포함되어 있으며, UID 값은 각각 `%60`, `%23` 및 `%2A`로 인코딩된 HTML이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="b3c0f-169">때때로 괄호 인코딩을 보게 되겠지만 이는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="b3c0f-170">예제:</span><span class="sxs-lookup"><span data-stu-id="b3c0f-170">Examples:</span></span>

- <span data-ttu-id="b3c0f-171">System.Threading.Tasks.Task\`1은 `System.Threading.Tasks.Task%601`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="b3c0f-172">System.Exception.\#ctor은 `System.Exception.%23ctor`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="b3c0f-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode)은 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="b3c0f-174">`https://xref.docs.microsoft.com/autocomplete`에서 형식, 멤버 오버로드 목록 또는 특정 오버로드된 멤버의 UID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="b3c0f-175">쿼리 문자열 `?text=*\<type-member-name>*`은 UID를 보려는 형식 또는 멤버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="b3c0f-176">예를 들어 `https://xref.docs.microsoft.com/autocomplete?text=string.format`은 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 오버로드를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="b3c0f-177">도구는 UID의 모든 부분에서 제공된 `text` 쿼리 매개 변수를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="b3c0f-178">예를 들어 멤버 이름(ToString), 부분 멤버 이름(ToStri), 형식 및 멤버 이름(Double.ToString) 등을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="b3c0f-179">UID 뒤에 \*(또는 `%2A`)를 추가하면 링크는 특정 API가 아닌 오버로드 페이지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="b3c0f-180">예를 들어 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_)처럼 특정 오버로드 대신 일반적인 방법으로 [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) 페이지에 연결하려는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="b3c0f-181">또한 멤버가 오버로드되지 않은 경우 \*를 사용하여 구성원 페이지에 연결할 수 있습니다. 이렇게 하면 매개 변수 목록을 UID에 포함하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="b3c0f-182">특정 메서드 오버로드에 연결하려면 각 메서드 매개 변수의 정규화된 형식 이름을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="b3c0f-183">예를 들어 \<xref:System.DateTime.ToString>은 매개 변수가 없는 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 메서드에 연결되는 반면 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)>은 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 메서드에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="b3c0f-184">[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)와 같은 제네릭 형식에 연결하려면 \`(`%60`) 문자 다음에 제네릭 형식 매개 변수의 수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="b3c0f-185">예를 들어 `<xref:System.Nullable%601>`은 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 형식에 연결되는 반면 `<xref:System.Func%602>`는 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 대리자에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="b3c0f-186">코드</span><span class="sxs-lookup"><span data-stu-id="b3c0f-186">Code</span></span>

<span data-ttu-id="b3c0f-187">코드를 포함하기 위한 가장 좋은 방법은 작동하는 샘플의 코드 조각을 포함하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="b3c0f-188">[.NET에 참여](dotnet-contribute.md#contributing-to-samples) 문서의 지침에 따라 샘플을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contributing-to-samples) article.</span></span> <span data-ttu-id="b3c0f-189">코드 포함에 대한 기본 규칙은 [코드](../code-in-docs.md)에 대한 일반 지침에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-189">The basic rules for including code are located in the general guidance on [code](../code-in-docs.md).</span></span>

<span data-ttu-id="b3c0f-190">다음 구문을 사용하여 코드를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="b3c0f-191">`-<language>`(*선택 사항*이지만 *권장됨*)</span><span class="sxs-lookup"><span data-stu-id="b3c0f-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="b3c0f-192">참조되고 있는 코드 조각의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-192">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="b3c0f-193">`<name>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="b3c0f-193">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="b3c0f-194">코드 조각의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-194">Name for the code snippet.</span></span> <span data-ttu-id="b3c0f-195">출력 HTML에는 아무런 영향이 없지만, 이를 사용하여 Markdown 소스의 가독성을 개선할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-195">It doesn't have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="b3c0f-196">`<pathToFile>`(*필수*)</span><span class="sxs-lookup"><span data-stu-id="b3c0f-196">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="b3c0f-197">참조할 코드 조각 파일을 나타내는, 파일 시스템의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-197">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="b3c0f-198">이는 .NET 문서 집합을 구성하는 다양한 리포지토리에 의해 복잡해질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-198">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="b3c0f-199">.NET 샘플은 dotnet/samples 리포지토리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-199">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="b3c0f-200">모든 코드 조각 경로는 `~/samples`로 시작하고 나머지 경로는 해당 리포지토리의 루트에서 소스에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-200">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="b3c0f-201">`<queryoption>`(*선택 사항*)</span><span class="sxs-lookup"><span data-stu-id="b3c0f-201">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="b3c0f-202">파일에서 코드를 검색하는 방법을 지정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-202">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="b3c0f-203">`#`: `#{tagname}`(태그 이름) ‘또는’ `#L{startlinenumber}-L{endlinenumber}`(줄 범위). </span><span class="sxs-lookup"><span data-stu-id="b3c0f-203">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="b3c0f-204">매우 약하기 때문에 줄 번호를 사용하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-204">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="b3c0f-205">태그 이름은 코드 조각 참조의 기본 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-205">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="b3c0f-206">의미 있는 태그 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-206">Use meaningful tag names.</span></span> <span data-ttu-id="b3c0f-207">(이전 플랫폼에서 많은 코드 조각을 마이그레이션했으며 태그에 `Snippet1`, `Snippet2` 등의 이름이 있습니다. 이러한 실행은 유지하기가 훨씬 더 어렵습니다.)</span><span class="sxs-lookup"><span data-stu-id="b3c0f-207">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="b3c0f-208">`range`: `?range=1,3-5` 줄 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-208">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="b3c0f-209">이 예제는 1, 3, 4 및 5 줄을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-209">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="b3c0f-210">가능할 때마다 태그 이름 옵션을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-210">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="b3c0f-211">태그 이름은 소스 코드에 있는 `Snippettagname` 형식의 지역 이름 또는 코드 주석 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-211">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="b3c0f-212">다음 예제에서는 태그 이름 `BasicThrow`를 참조하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-212">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="b3c0f-213">**dotnet/samples** 리포지토리의 소스에 대한 상대 경로는 `~/samples` 경로를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-213">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="b3c0f-214">그리고 코드 조각 태그가 [이 원본 파일](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)에서 어떻게 구성되었는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-214">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="b3c0f-215">코드 조각 소스의 태그 이름 표현에 대한 자세한 내용을 언어별로 보려면 [DocFX 지침](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-215">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="b3c0f-216">다음 예제는 세 개의 .NET 언어에 포함된 코드를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-216">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

<span data-ttu-id="b3c0f-217">전체 프로그램에서 코드 조각을 포함하면 모든 코드가 CI(연속 통합) 시스템을 통해 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-217">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="b3c0f-218">그러나 컴파일 시간 또는 런타임 오류를 일으키는 요소를 표시해야 하는 경우 인라인 코드 블록을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-218">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="b3c0f-219">이미지</span><span class="sxs-lookup"><span data-stu-id="b3c0f-219">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="b3c0f-220">정적 이미지 또는 애니메이션 GIF</span><span class="sxs-lookup"><span data-stu-id="b3c0f-220">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="b3c0f-221">연결된 이미지</span><span class="sxs-lookup"><span data-stu-id="b3c0f-221">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="b3c0f-222">동영상</span><span class="sxs-lookup"><span data-stu-id="b3c0f-222">Videos</span></span>

<span data-ttu-id="b3c0f-223">현재 Channel 9 및 YouTube 비디오를 다음 구문과 함께 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-223">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="b3c0f-224">Channel9</span><span class="sxs-lookup"><span data-stu-id="b3c0f-224">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="b3c0f-225">비디오의 올바른 URL을 가져오려면 비디오 프레임 아래의 **포함** 탭을 선택하고 `<iframe>` 요소에서 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-225">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="b3c0f-226">예:</span><span class="sxs-lookup"><span data-stu-id="b3c0f-226">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="b3c0f-227">YouTube</span><span class="sxs-lookup"><span data-stu-id="b3c0f-227">YouTube</span></span>

<span data-ttu-id="b3c0f-228">비디오의 올바른 URL을 가져오려면 비디오를 마우스 오른쪽 단추로 클릭하여 **포함 코드 복사**를 선택하고 `<iframe>` 요소에서 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-228">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="b3c0f-229">예:</span><span class="sxs-lookup"><span data-stu-id="b3c0f-229">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="b3c0f-230">docs.microsoft 확장명</span><span class="sxs-lookup"><span data-stu-id="b3c0f-230">docs.microsoft extensions</span></span>

<span data-ttu-id="b3c0f-231">docs.microsoft는 GitHub Flavored Markdown에 몇 가지 추가 확장 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-231">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="b3c0f-232">확인된 목록</span><span class="sxs-lookup"><span data-stu-id="b3c0f-232">Checked lists</span></span>

<span data-ttu-id="b3c0f-233">목록에 사용자 지정 스타일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-233">A custom style is available for lists.</span></span> <span data-ttu-id="b3c0f-234">녹색 확인 표시가 있는 목록을 렌더링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-234">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="b3c0f-235">이는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-235">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="b3c0f-236">.NET Core 앱을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="b3c0f-236">How to create a .NET Core app</span></span>
> * <span data-ttu-id="b3c0f-237">Microsoft.XmlSerializer.Generator 패키지에 참조를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="b3c0f-237">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="b3c0f-238">MyApp.csproj를 편집하여 종속성을 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="b3c0f-238">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="b3c0f-239">클래스 및 XmlSerializer를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="b3c0f-239">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="b3c0f-240">애플리케이션을 빌드 및 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="b3c0f-240">How to build and run the application</span></span>

<span data-ttu-id="b3c0f-241">[.NET Core 문서](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)에서 실행 중인 확인 목록의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-241">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="b3c0f-242">Buttons</span><span class="sxs-lookup"><span data-stu-id="b3c0f-242">Buttons</span></span>

<span data-ttu-id="b3c0f-243">Button 링크:</span><span class="sxs-lookup"><span data-stu-id="b3c0f-243">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="b3c0f-244">이는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-244">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="b3c0f-245">단추 링크</span><span class="sxs-lookup"><span data-stu-id="b3c0f-245">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="b3c0f-246">[Visual Studio 문서](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)에서 실행 중인 단추의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-246">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="b3c0f-247">단계별</span><span class="sxs-lookup"><span data-stu-id="b3c0f-247">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="b3c0f-248">[C# 가이드](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)에서 실행 중인 단계별 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c0f-248">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
