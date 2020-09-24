---
title: .NET 문서용 템플릿 및 치트 시트
description: 이 문서에는 .NET 문서 리포지토리에 대한 새 문서를 작성하는 데 사용할 수 있는 편리한 템플릿이 포함되어 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 15288ccb1831e994fd078f47788ad4c2f502775c
ms.sourcegitcommit: 92d06515af1d9d0e5abf632fc3b6425c487174d5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90837215"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="368c6-103">.NET 문서용 메타데이터 및 Markdown 템플릿</span><span class="sxs-lookup"><span data-stu-id="368c6-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="368c6-104">이 dotnet/docs 템플릿에는 Markdown 구문의 예와 메타데이터 설정에 대한 지침이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-104">This dotnet/docs template contains examples of Markdown syntax and guidance on setting the metadata.</span></span>

<span data-ttu-id="368c6-105">Markdown 파일을 만들 때 포함된 템플릿을 새 파일로 복사하여 아래 지정된 대로 메타데이터를 채우고 위의 H1 제목을 문서 제목으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-105">When creating a Markdown file, copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="368c6-106">메타데이터</span><span class="sxs-lookup"><span data-stu-id="368c6-106">Metadata</span></span>

<span data-ttu-id="368c6-107">필요한 메타데이터 블록은 다음 샘플 메타데이터 블록에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="368c6-108">콜론(:)과 메타데이터 요소의 값 사이에는 공백이 **있어야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="368c6-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="368c6-109">값의 콜론(예: 제목)이 메타데이터 구문 분석기를 중단시킵니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="368c6-110">이 경우 제목을 큰따옴표로 둘러쌉니다(예: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="368c6-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="368c6-111">**title**: 검색 엔진 결과에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="368c6-112">제목은 H1 제목의 제목과 동일해서는 안 되며 60자 이하여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="368c6-113">**description**: 문서의 내용을 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="368c6-114">일반적으로 검색 결과 페이지에 표시되지만 검색 순위 지정에는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="368c6-115">길이는 공백을 포함하여 115-145자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="368c6-116">**author**: 작성자 필드에는 작성자의 **GitHub 사용자 이름**이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="368c6-117">**ms.date**: 마지막 중요 업데이트 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="368c6-118">전체 문서를 검토하고 업데이트한 경우 기존 문서에서 이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="368c6-119">오타와 같은 작은 수정 사항은 업데이트를 보증하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="368c6-120">각 문서에 다른 메타데이터가 연결되어 있지만 일반적으로 **docfx.json**에 지정된 폴더 수준에서 대부분의 메타데이터 값을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="368c6-121">기본 Markdown, GFM 및 특수 문자</span><span class="sxs-lookup"><span data-stu-id="368c6-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="368c6-122">[Markdown 참조](../markdown-reference.md) 문서에서 Markdown, GFM(GitHub Flavored Markdown) 및 OPS 관련 확장에 대한 기본 사항을 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS-specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="368c6-123">Markdown은 서식 지정에 \*, \` 및 \#과 같은 특수 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="368c6-124">콘텐츠에 이러한 문자 중 하나를 포함하려면 다음 두 가지 작업 중 하나를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="368c6-125">특수 문자 앞에 백슬래시를 두어 “이스케이프”합니다(예: \*의 경우 `\*`).</span><span class="sxs-lookup"><span data-stu-id="368c6-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*).</span></span>
- <span data-ttu-id="368c6-126">문자에 대해 [HTML 엔터티 코드](http://www.ascii.cl/htmlcodes.htm)를 사용합니다(예:&#42;의 경우 `&#42;`).</span><span class="sxs-lookup"><span data-stu-id="368c6-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="368c6-127">파일 이름</span><span class="sxs-lookup"><span data-stu-id="368c6-127">File names</span></span>

<span data-ttu-id="368c6-128">파일 이름에는 다음 규칙이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-128">File names use the following rules:</span></span>

* <span data-ttu-id="368c6-129">소문자, 숫자 및 하이픈만 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="368c6-130">공백 또는 문장 부호를 사용하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="368c6-131">파일 이름에서 단어와 숫자를 구분하려면 하이픈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="368c6-132">개발, 구매, 빌드, 문제 해결과 같은 특정 동작을 나타내는 동사를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="368c6-133">-ing 형식의 단어는 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-133">No -ing words.</span></span>
* <span data-ttu-id="368c6-134">짧은 단어는 사용하지 않습니다. a, and, the, in, or 등은 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="368c6-135">Markdown에 있어야 하며 .md 파일 확장명을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="368c6-136">파일 이름을 합리적으로 짧게 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-136">Keep file names reasonably short.</span></span> <span data-ttu-id="368c6-137">이는 문서에 대한 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="368c6-138">제목</span><span class="sxs-lookup"><span data-stu-id="368c6-138">Headings</span></span>

<span data-ttu-id="368c6-139">문장 스타일의 대문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="368c6-140">제목의 첫 단어를 항상 대문자로 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="368c6-141">텍스트 스타일 지정</span><span class="sxs-lookup"><span data-stu-id="368c6-141">Text styling</span></span>

<span data-ttu-id="368c6-142">*기울임꼴*</span><span class="sxs-lookup"><span data-stu-id="368c6-142">*Italics*</span></span>\
<span data-ttu-id="368c6-143">파일, 폴더, 경로(긴 항목의 경우, 해당 행으로 분리), 새 용어에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-143">Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="368c6-144">**굵게**</span><span class="sxs-lookup"><span data-stu-id="368c6-144">**Bold**</span></span>\
<span data-ttu-id="368c6-145">UI 요소에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-145">Use for UI elements.</span></span>

`Code`\
<span data-ttu-id="368c6-146">인라인 코드, 언어 키워드, NuGet 패키지 이름, 명령줄 명령, 데이터베이스 테이블과 열 이름 및 클릭 가능한 것으로 설정하지 않을 URL에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-146">Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="368c6-147">링크</span><span class="sxs-lookup"><span data-stu-id="368c6-147">Links</span></span>

<span data-ttu-id="368c6-148">앵커, 내부 링크, 다른 문서에 대한 링크, 코드 포함 및 외부 링크에 대한 정보는 [링크](../how-to-write-links.md)에 대한 일반 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-148">See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="368c6-149">.NET 문서 팀은 다음 규칙을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-149">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="368c6-150">대부분의 경우 상대 링크는 GitHub의 소스에서 해결되기 때문에 상대 링크를 사용하고, 링크에서 `~/`의 사용을 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-150">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="368c6-151">그러나 종속 리포지토리의 파일에 연결할 때마다 `~/` 문자를 사용하여 경로를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-151">However, whenever we link to a file in a dependent repo, we use the `~/` character to provide the path.</span></span> <span data-ttu-id="368c6-152">종속 리포지토리에 있는 파일은 GitHub의 다른 위치에 있기 때문에 링크는 작성된 방법에 관계없이 상대 링크로 올바르게 해결되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-152">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="368c6-153">C# 언어 사양 및 Visual Basic 언어 사양은 언어 리포지토리의 원본을 포함하여 .NET 문서에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-153">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="368c6-154">markdown 원본은 [csharplang](https://github.com/dotnet/csharplang) 및 [vblang](https://github.com/dotnet/vblang) 리포지토리에서 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-154">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="368c6-155">사양에 대한 링크는 해당 사양이 포함된 원본 디렉터리를 가리켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-155">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="368c6-156">다음 예제와 같이 C#의 경우 **~/_csharplang/spec**이고, VB의 경우 **~/_vblang/spec**입니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-156">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="368c6-157">API에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="368c6-157">Links to APIs</span></span>

<span data-ttu-id="368c6-158">빌드 시스템에는 외부 링크를 사용하지 않고도 .NET API에 연결할 수 있는 몇 가지 확장 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-158">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="368c6-159">다음 구문 중 하나를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-159">You use one of the following syntax:</span></span>

1. <span data-ttu-id="368c6-160">자동 연결: `<xref:UID>` 또는 `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="368c6-160">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="368c6-161">`displayProperty` 쿼리 매개 변수는 정규화된 링크 텍스트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-161">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="368c6-162">기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-162">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="368c6-163">Markdown 링크: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="368c6-163">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="368c6-164">표시되는 링크 텍스트를 사용자 지정하려면 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-164">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="368c6-165">예제:</span><span class="sxs-lookup"><span data-stu-id="368c6-165">Examples:</span></span>

- <span data-ttu-id="368c6-166">`<xref:System.String>`은 [String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-166">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="368c6-167">`<xref:System.String?displayProperty=nameWithType>`은 [System.String](https://docs.microsoft.com/dotnet/api/system.string)으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-167">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="368c6-168">`[String class](xref:System.String)`은 [String 클래스](https://docs.microsoft.com/dotnet/api/system.string)로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-168">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="368c6-169">이 표기법 사용에 대한 자세한 내용은 [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)(상호 참조 사용)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-169">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="368c6-170">일부 UID에는 특수 문자 \`, \# 또는 \*이 포함되어 있으며, UID 값은 각각 `%60`, `%23` 및 `%2A`로 인코딩된 HTML이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-170">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="368c6-171">때때로 괄호 인코딩을 보게 되겠지만 이는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-171">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="368c6-172">예제:</span><span class="sxs-lookup"><span data-stu-id="368c6-172">Examples:</span></span>

- <span data-ttu-id="368c6-173">System.Threading.Tasks.Task\`1은 `System.Threading.Tasks.Task%601`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-173">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="368c6-174">System.Exception.\#ctor은 `System.Exception.%23ctor`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-174">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="368c6-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode)은 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="368c6-176">`https://xref.docs.microsoft.com/autocomplete`에서 형식, 멤버 오버로드 목록 또는 특정 오버로드된 멤버의 UID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-176">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="368c6-177">쿼리 문자열 `?text=*\<type-member-name>*`은 UID를 보려는 형식 또는 멤버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-177">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="368c6-178">예를 들어 `https://xref.docs.microsoft.com/autocomplete?text=string.format`은 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 오버로드를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-178">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="368c6-179">도구는 UID의 모든 부분에서 제공된 `text` 쿼리 매개 변수를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-179">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="368c6-180">예를 들어 멤버 이름(ToString), 부분 멤버 이름(ToStri), 형식 및 멤버 이름(Double.ToString) 등을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-180">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="368c6-181">UID 뒤에 \*(또는 `%2A`)를 추가하면 링크는 특정 API가 아닌 오버로드 페이지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-181">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="368c6-182">예를 들어 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_)처럼 특정 오버로드 대신 일반적인 방법으로 [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) 페이지에 연결하려는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-182">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="368c6-183">또한 멤버가 오버로드되지 않은 경우 \*를 사용하여 구성원 페이지에 연결할 수 있습니다. 이렇게 하면 매개 변수 목록을 UID에 포함하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-183">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="368c6-184">특정 메서드 오버로드에 연결하려면 각 메서드 매개 변수의 정규화된 형식 이름을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-184">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="368c6-185">예를 들어 \<xref:System.DateTime.ToString>은 매개 변수가 없는 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 메서드에 연결되는 반면, \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)>는 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 메서드에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-185">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="368c6-186">[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1) 같은 제네릭 형식에 연결하려면 \`(`%60`) 문자 다음에 제네릭 형식 매개 변수의 수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-186">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="368c6-187">예를 들어 `<xref:System.Nullable%601>`은 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 형식에 연결되는 반면, `<xref:System.Func%602>`는 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 대리자에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-187">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="368c6-188">코드</span><span class="sxs-lookup"><span data-stu-id="368c6-188">Code</span></span>

<span data-ttu-id="368c6-189">코드를 포함하기 위한 가장 좋은 방법은 작동하는 샘플의 코드 조각을 포함하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-189">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="368c6-190">[.NET에 참여](dotnet-contribute.md#contribute-to-samples) 문서의 지침에 따라 샘플을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-190">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contribute-to-samples) article.</span></span> <span data-ttu-id="368c6-191">전체 프로그램에서 코드 조각을 포함하면 모든 코드가 CI(연속 통합) 시스템을 통해 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-191">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="368c6-192">그러나 컴파일 시간 또는 런타임 오류를 일으키는 요소를 표시해야 하는 경우 인라인 코드 블록을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-192">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

<span data-ttu-id="368c6-193">문서에서 코드를 표시하는 Markdown 구문에 대한 자세한 내용은 [문서에 코드를 포함하는 방법](../code-in-docs.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="368c6-193">For information about the Markdown syntax for showing code in docs, see [How to include code in docs](../code-in-docs.md).</span></span>

## <a name="images"></a><span data-ttu-id="368c6-194">이미지</span><span class="sxs-lookup"><span data-stu-id="368c6-194">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="368c6-195">정적 이미지 또는 애니메이션 GIF</span><span class="sxs-lookup"><span data-stu-id="368c6-195">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="368c6-196">연결된 이미지</span><span class="sxs-lookup"><span data-stu-id="368c6-196">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="368c6-197">동영상</span><span class="sxs-lookup"><span data-stu-id="368c6-197">Videos</span></span>

<span data-ttu-id="368c6-198">현재 Channel 9 및 YouTube 비디오를 다음 구문과 함께 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-198">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="368c6-199">Channel9</span><span class="sxs-lookup"><span data-stu-id="368c6-199">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="368c6-200">비디오의 올바른 URL을 가져오려면 비디오 프레임 아래의 **포함** 탭을 선택하고 `<iframe>` 요소에서 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-200">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="368c6-201">예:</span><span class="sxs-lookup"><span data-stu-id="368c6-201">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="368c6-202">YouTube</span><span class="sxs-lookup"><span data-stu-id="368c6-202">YouTube</span></span>

<span data-ttu-id="368c6-203">비디오의 올바른 URL을 가져오려면 비디오를 마우스 오른쪽 단추로 클릭하여 **포함 코드 복사**를 선택하고 `<iframe>` 요소에서 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-203">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="368c6-204">예:</span><span class="sxs-lookup"><span data-stu-id="368c6-204">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="368c6-205">docs.microsoft 확장명</span><span class="sxs-lookup"><span data-stu-id="368c6-205">docs.microsoft extensions</span></span>

<span data-ttu-id="368c6-206">docs.microsoft는 GitHub Flavored Markdown에 몇 가지 추가 확장 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-206">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="368c6-207">확인된 목록</span><span class="sxs-lookup"><span data-stu-id="368c6-207">Checked lists</span></span>

<span data-ttu-id="368c6-208">목록에 사용자 지정 스타일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-208">A custom style is available for lists.</span></span> <span data-ttu-id="368c6-209">녹색 확인 표시가 있는 목록을 렌더링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-209">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="368c6-210">이는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-210">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="368c6-211">.NET Core 앱을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="368c6-211">How to create a .NET Core app</span></span>
> * <span data-ttu-id="368c6-212">Microsoft.XmlSerializer.Generator 패키지에 참조를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="368c6-212">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="368c6-213">MyApp.csproj를 편집하여 종속성을 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="368c6-213">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="368c6-214">클래스 및 XmlSerializer를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="368c6-214">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="368c6-215">애플리케이션을 빌드 및 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="368c6-215">How to build and run the application</span></span>

<span data-ttu-id="368c6-216">[.NET Core 문서](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)에서 실행 중인 확인 목록의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-216">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="368c6-217">Buttons</span><span class="sxs-lookup"><span data-stu-id="368c6-217">Buttons</span></span>

<span data-ttu-id="368c6-218">Button 링크:</span><span class="sxs-lookup"><span data-stu-id="368c6-218">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="368c6-219">이는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-219">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="368c6-220">단추 링크</span><span class="sxs-lookup"><span data-stu-id="368c6-220">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="368c6-221">[Visual Studio 문서](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)에서 실행 중인 단추의 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-221">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="368c6-222">단계별</span><span class="sxs-lookup"><span data-stu-id="368c6-222">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="368c6-223">[C# 가이드](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)에서 실행 중인 단계별 예를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="368c6-223">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
