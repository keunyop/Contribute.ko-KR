---
title: 설명서에서 링크를 사용하는 방법
description: 이 문서에서는 docs.microsoft.com 내의 콘텐츠에 대한 링크를 만드는 방법에 대한 지침을 제공합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624786"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="4c9dd-103">설명서에서 링크 사용</span><span class="sxs-lookup"><span data-stu-id="4c9dd-103">Use links in documentation</span></span>

<span data-ttu-id="4c9dd-104">이 문서에서는 docs.microsoft.com에서 호스팅되는 페이지의 하이퍼 링크를 사용하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="4c9dd-105">링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="4c9dd-106">사용자는 링크를 통해 같은 페이지, 인접한 다른 페이지 또는 외부 사이트 및 URL의 콘텐츠로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="4c9dd-107">docs.microsoft.com 사이트 백 엔드는 [Markdig][] 구문 분석 엔진을 통해 구문 분석되는 [CommonMark][] 규격 markdown을 지원하는 OPS(Open Publishing Services)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="4c9dd-108">해당 markdown 유형은 대부분 [GFM(GitHub Flavored Markdown)][GFM]과 호환되므로, 대부분의 문서가 GitHub에 저장되고 GitHub에서 편집 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="4c9dd-109">추가 기능은 Markdown 확장을 통해 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c9dd-110">대상이 링크를 지원하는 경우(대부분 지원) 모든 링크는 보안 링크여야 합니다(`https` 및 `http`).</span><span class="sxs-lookup"><span data-stu-id="4c9dd-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="4c9dd-111">링크 텍스트</span><span class="sxs-lookup"><span data-stu-id="4c9dd-111">Link text</span></span>

<span data-ttu-id="4c9dd-112">링크 텍스트에 포함하는 단어는 친근해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="4c9dd-113">즉, 일반적인 영어(한국어) 단어 또는 연결하는 페이지의 제목이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c9dd-114">"여기를 클릭하세요."를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-114">Do not use "click here."</span></span> <span data-ttu-id="4c9dd-115">검색 엔진 최적화에 좋지 않으며 대상을 적절하게 설명하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="4c9dd-116">**올바름:**</span><span class="sxs-lookup"><span data-stu-id="4c9dd-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="4c9dd-117">**잘못됨:**</span><span class="sxs-lookup"><span data-stu-id="4c9dd-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="4c9dd-118">하나의 문서에서 다른 문서로 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-118">Links from one article to another</span></span>

<span data-ttu-id="4c9dd-119">게시 시스템에서 지원되는 두 가지 유형의 하이퍼링크는 **URL**과 **파일 링크**입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="4c9dd-120">URL 링크는 docs.microsoft.com의 루트를 기준으로 한 URL 경로이거나, 전체 URL 구문을 포함하는 절대 URL(예: `https://github.com/MicrosoftDocs/PowerShell-Docs`)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="4c9dd-121">현재 _docset_ 외부의 콘텐츠에 연결하거나 docset 내의 자동 생성된 참조 및 개념 문서 간에 연결하는 경우 URL 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="4c9dd-122">상대 링크를 만드는 가장 간단한 방법은 브라우저에서 URL을 복사한 후 markdown에 붙여넣은 값에서 `https://docs.microsoft.com/en-us`를 제거하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="4c9dd-123">Microsoft 속성에 대한 로캘은 URL에 포함하지 않습니다(예: URL에서 “/en-us” 제거).</span><span class="sxs-lookup"><span data-stu-id="4c9dd-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="4c9dd-124">파일 링크는 docset 내 한 문서에서 다른 문서로 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="4c9dd-125">모든 파일 경로에는 백슬래시 문자 대신 슬래시(`/`) 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="4c9dd-126">문서는 같은 디렉터리의 다른 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="4c9dd-127">문서는 현재 디렉터리의 부모 디렉터리에 있는 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="4c9dd-128">문서는 현재 디렉터리의 하위 디렉터리에 있는 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="4c9dd-129">문서는 현재 디렉터리의 부모 디렉터리에 있는 하위 디렉터리의 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="4c9dd-130">앞의 예제에서는 `~/`를 링크의 일부로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="4c9dd-131">리포지토리의 루트에서 시작하는 절대 경로에 연결하려면 `/`로 링크를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="4c9dd-132">GitHub에서 원본 리포지토리로 이동할 때 `~/`를 포함하면 유효하지 않은 링크가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="4c9dd-133">`/`로 경로를 시작하면 올바르게 해결됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="4c9dd-134">docs.microsoft.com의 링크 구조</span><span class="sxs-lookup"><span data-stu-id="4c9dd-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="4c9dd-135">docs.microsoft.com에 게시된 콘텐츠의 URL 구조는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="4c9dd-136">예제:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="4c9dd-137">`<locale>` - 문서의 언어를 식별함(예: en-us 또는 de-de)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="4c9dd-138">`<product-service>` - 제품 또는 서비스의 이름(예: powershell, dotnet 또는 azure)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="4c9dd-139">`[<feature-service>]` - (선택 사항) 제품 기능 또는 하위 서비스의 이름(예: csharp 또는 load-balancer)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="4c9dd-140">`[<subfolder>]` - (선택 사항) 기능 내 하위 폴더의 이름</span><span class="sxs-lookup"><span data-stu-id="4c9dd-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="4c9dd-141">`<topic>` - 토픽에 대한 문서 파일의 이름(예: load-balancer-overview 또는 overview)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="4c9dd-142">`[?view=\<view-name>]` - (선택 사항) 사용할 수 있는 버전이 여러 개인 콘텐츠의 버전 선택기에서 사용되는 보기 이름(예: azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="4c9dd-143">대부분 경우, 같은 _docset_의 문서는 `<product-service>` URL 조각이 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="4c9dd-144">예:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-144">For example:</span></span>
> - <span data-ttu-id="4c9dd-145">같은 docset</span><span class="sxs-lookup"><span data-stu-id="4c9dd-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="4c9dd-146">다른 docset</span><span class="sxs-lookup"><span data-stu-id="4c9dd-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="4c9dd-147">책갈피 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-147">Bookmark links</span></span>

<span data-ttu-id="4c9dd-148">‘현재’ 파일의 제목에 대한 책갈피 링크를 사용하려면 해시 기호 다음에 제목의 소문자 단어를 사용합니다. </span><span class="sxs-lookup"><span data-stu-id="4c9dd-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="4c9dd-149">제목에서 문장 부호를 제거하고 공백을 대시로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="4c9dd-150">다른 문서의 책갈피 제목에 연결하려면 파일 관련 또는 사이트 관련 링크 다음에 해시 기호를 사용하고 그 뒤에 제목의 단어를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="4c9dd-151">제목에서 문장 부호를 제거하고 공백을 대시로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="4c9dd-152">URL에서 책갈피 링크를 복사할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="4c9dd-153">URL을 찾으려면 docs.microsoft.com의 제목 줄을 마우스로 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="4c9dd-154">링크 아이콘이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-154">You should see a link icon appear:</span></span>

![문서 제목의 링크 아이콘](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="4c9dd-156">링크 아이콘을 클릭한 후 URL에서 책갈피 앵커 텍스트(즉, 해시 뒤에 있는 부분)를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="4c9dd-157">또한 Docs 확장에 링크를 만드는 데 유용한 도구가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="4c9dd-158">명시적 앵커 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-158">Explicit anchor links</span></span>

<span data-ttu-id="4c9dd-159">허브 및 시작 페이지를 제외하고는 `<a>` HTML 태그를 사용한 명시적 앵커 링크 추가는 필요하거나 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="4c9dd-160">대신 [책갈피 링크](#bookmark-links)에 설명된 대로 자동 생성된 책갈피를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="4c9dd-161">허브 및 시작 페이지의 경우 다음과 같이 앵커를 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="4c9dd-162">또는</span><span class="sxs-lookup"><span data-stu-id="4c9dd-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="4c9dd-163">다음을 앵커 링크에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="4c9dd-164">앵커 텍스트는 항상 소문자이고 공백을 포함하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="4c9dd-165">XRef(상호 참조) 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-165">XRef (cross reference) links</span></span>

<span data-ttu-id="4c9dd-166">XRef 링크는 빌드할 때 유효성 검사가 수행되므로 API에 연결하는 데 권장되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="4c9dd-167">현재 docset 또는 다른 docset의 자동 생성된 API 참조 페이지에 연결하려면 형식 또는 멤버의 [UID](#determine-the-uid)(고유 ID)가 포함된 XRef 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="4c9dd-168">[VS Code용 Docs Markdown 확장][docsextension](Docs Authoring Pack의 일부)을 사용하여 [.NET API 브라우저][]에 표시되는 .NET XRref 링크를 삽입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="4c9dd-169">[.NET API 브라우저][] 또는 [Windows UWP][] 검색 상자에 전체 이름의 전부 또는 일부를 입력하여 연결하려는 API가 [docs.microsoft.com][docs]에 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="4c9dd-170">표시되는 결과가 없으면 해당 형식이 아직 docs.microsoft.com에 없는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="4c9dd-171">다음 구문 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="4c9dd-172">자동 링크:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="4c9dd-173">기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="4c9dd-174">선택적 `displayProperty=nameWithType` 쿼리 매개 변수는 정규화된 링크 텍스트 즉, 형식의 경우 **namespace.type**을, 형식 멤버(열거형 형식 멤버 포함)의 경우 **type.member**를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="4c9dd-175">Markdown 스타일 링크:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="4c9dd-176">표시되는 링크 텍스트를 사용자 지정하려면 XRef에 Markdown 스타일 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="4c9dd-177">예제:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-177">Examples:</span></span>

- <span data-ttu-id="4c9dd-178">**\<xref:System.String>** 은 <xref:System.String>으로 표시됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="4c9dd-179">**\<xref:System.String?displayProperty=nameWithType>** 은 <xref:System.String?displayProperty=nameWithType>으로 표시됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="4c9dd-180">**\[String class](xref:System.String)** 은 [String 클래스](xref:System.String)로 표시됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="4c9dd-181">`displayProperty=fullName` 쿼리 매개 변수는 클래스에 대해 `displayProperty=nameWithType`과 같은 방식으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="4c9dd-182">즉, 링크 텍스트가 **namespace.classname**이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="4c9dd-183">그러나 멤버의 경우 링크 텍스트는 바람직하지 않을 수도 있는 **namespace.classname.membername**으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="4c9dd-184">UID는 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-184">UIDs are case sensitive.</span></span> <span data-ttu-id="4c9dd-185">예를 들어 `<xref:System.Object>`는 올바르게 확인되지만, `<xref:system.object>`는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="4c9dd-186">XRef 빌드 경고 및 증분 빌드</span><span class="sxs-lookup"><span data-stu-id="4c9dd-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="4c9dd-187">증분 빌드는 변경되었거나 변경의 영향을 받은 파일만 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="4c9dd-188">잘못된 XREF 링크에 대한 빌드 경고가 표시되지만, 이 링크가 실제로 유효한 경우 빌드가 증분이었기 때문일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="4c9dd-189">경고를 발생시키는 파일이 변경되지 않았으므로 빌드되지 않았으며 지난 경고가 재생되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="4c9dd-190">파일이 변경되거나 전체 빌드를 트리거하면 경고가 사라집니다(ops.microsoft.com에서 전체 빌드를 시작할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="4c9dd-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="4c9dd-191">이는 DocFX가 XREF 서비스 내에서 데이터 업데이트를 검색할 수 없어서 발생하는 증분 빌드의 단점입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="4c9dd-192">UID 확인</span><span class="sxs-lookup"><span data-stu-id="4c9dd-192">Determine the UID</span></span>

<span data-ttu-id="4c9dd-193">UID는 일반적으로 정규화된 클래스 또는 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="4c9dd-194">UID를 확인하는 방법은 다음과 같은 두 가지 이상이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="4c9dd-195">형식 또는 멤버의 [Docs][docs] 페이지를 마우스 오른쪽 단추로 클릭하고 **소스 보기**를 선택한 다음 **ms.assetid**의 **content** 값을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![웹 페이지 소스의 ms.assetid](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="4c9dd-197">형식 이름의 일부 또는 전부를 URL에 추가하여 [자동 완성 사이트][]를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="4c9dd-198">예를 들어 브라우저의 주소 표시줄에 `https://xref.docs.microsoft.com/autocomplete?text=Writeline`을 입력하면 해당 이름에 **Writeline**이 포함된 모든 형식과 메서드가 해당 UID와 함께 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="4c9dd-199">UID 검증</span><span class="sxs-lookup"><span data-stu-id="4c9dd-199">Verify the UID</span></span>

<span data-ttu-id="4c9dd-200">UID가 올바른지 테스트하려면 다음 URL의 **System.String**을 해당 UID로 바꾼 후 브라우저의 주소 표시줄에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="4c9dd-201">URL의 UID는 대/소문자를 구분하고, 메서드 오버로드 UID를 확인하는 경우 매개 변수 형식 사이에 공백을 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="4c9dd-202">다음과 같은 내용이 표시되면 UID가 올바른 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="4c9dd-203">페이지에 `[]`가 표시되면 UID가 잘못된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="4c9dd-204">URL의 백분율 인코딩</span><span class="sxs-lookup"><span data-stu-id="4c9dd-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="4c9dd-205">UID의 특수 문자는 다음과 같이 HTML로 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="4c9dd-206">문자</span><span class="sxs-lookup"><span data-stu-id="4c9dd-206">Character</span></span> | <span data-ttu-id="4c9dd-207">HTML 인코딩</span><span class="sxs-lookup"><span data-stu-id="4c9dd-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="4c9dd-208">%60</span><span class="sxs-lookup"><span data-stu-id="4c9dd-208">%60</span></span>           |
| `#`       | <span data-ttu-id="4c9dd-209">%23</span><span class="sxs-lookup"><span data-stu-id="4c9dd-209">%23</span></span>           |
| `*`       | <span data-ttu-id="4c9dd-210">%2A</span><span class="sxs-lookup"><span data-stu-id="4c9dd-210">%2A</span></span>           |

<span data-ttu-id="4c9dd-211">[백분율 코드](https://en.wikipedia.org/wiki/Percent-encoding)의 전체 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="4c9dd-212">인코딩 예:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-212">Encoding examples:</span></span>

- <span data-ttu-id="4c9dd-213">`System.Threading.Tasks.Task``1`은 `System.Threading.Tasks.Task%601`로 인코딩됨([제네릭 형식에 대한 섹션](#generic-types) 참조)</span><span class="sxs-lookup"><span data-stu-id="4c9dd-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="4c9dd-214">`System.Exception.#ctor`은 `System.Exception.%23ctor`로 인코딩됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="4c9dd-215">`System.Object.Equals*`는 `System.Object.Equals%2A`로 인코딩됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="4c9dd-216">제네릭 형식</span><span class="sxs-lookup"><span data-stu-id="4c9dd-216">Generic types</span></span>

<span data-ttu-id="4c9dd-217">제네릭 형식은 `System.Collections.Generic.List<T>`와 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="4c9dd-218">[.NET API 브라우저](https://docs.microsoft.com/dotnet/api/)에서 이 형식을 검색하여 해당 URL을 살펴보면, `<T>`가 URL에서 `-1`(실제로 **\`1**을 나타냄)로 작성된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="4c9dd-219">**List\<T>** 같은 제네릭 형식에 연결하려면 다음 예에 표시된 것처럼 **\`** 억음 악센트 기호 문자를 **%60**으로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="4c9dd-220">메서드</span><span class="sxs-lookup"><span data-stu-id="4c9dd-220">Methods</span></span>

<span data-ttu-id="4c9dd-221">메서드에 연결하려면 메서드 이름 뒤에 별표(`*`)를 추가하여 일반 메서드 페이지에 연결하거나 특정 오버로드에 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="4c9dd-222">예를 들어 특정 매개 변수 형식 없이 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 메서드에 연결하려면 일반 페이지를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="4c9dd-223">별표 문자는 `%2A`로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="4c9dd-224">예:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-224">For example:</span></span>

<span data-ttu-id="4c9dd-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>`은 <xref:System.Object.Equals%2A?displayProperty=nameWithType>에 연결됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="4c9dd-226">특정 오버로드에 연결하려면 메서드 이름 뒤에 괄호를 추가하고 각 매개 변수의 전체 형식 이름을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="4c9dd-227">형식 이름 사이에 공백 문자를 넣지 마세요. 넣으면 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="4c9dd-228">예:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-228">For example:</span></span>

<span data-ttu-id="4c9dd-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>`은 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>에 연결됨</span><span class="sxs-lookup"><span data-stu-id="4c9dd-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="4c9dd-230">포함되는 내용의 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-230">Links from includes</span></span>

<span data-ttu-id="4c9dd-231">포함되는 파일은 다른 디렉토리에 위치하기 때문에 더 긴 상대 경로를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="4c9dd-232">포함되는 파일의 문서에 연결하려면 이 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="4c9dd-233">Visual Studio Code용 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 확장을 사용하면, 경로를 확인하는 번거로움 없이 상대 링크와 책갈피를 올바르게 삽입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="4c9dd-234">선택기의 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-234">Links in selectors</span></span>

<span data-ttu-id="4c9dd-235">선택기는 설명서 문서에 드롭다운 목록으로 표시되는 탐색 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="4c9dd-236">reader가 드롭다운에서 값을 선택하면 브라우저가 선택한 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="4c9dd-237">일반적으로 선택기 목록에는 밀접하게 관련된 문서에 대한 링크가 포함되어 있습니다(예: 여러 프로그래밍 언어의 동일한 주제 또는 밀접하게 관련된 문서 시리즈).</span><span class="sxs-lookup"><span data-stu-id="4c9dd-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="4c9dd-238">포함되는 내용에 포함된 선택기가 있는 경우 다음과 같은 링크 구조체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="4c9dd-239">참조 스타일 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-239">Reference-style links</span></span>

<span data-ttu-id="4c9dd-240">소스 콘텐츠를 쉽게 읽을 수 있도록 참조 스타일 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="4c9dd-241">참조 스타일 링크는 인라인 링크 구문을, 긴 URL을 문서 끝으로 이동시킨 간소화된 구문으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="4c9dd-242">[Daring Fireball](https://daringfireball.net/projects/markdown/)의 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="4c9dd-243">인라인 텍스트:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="4c9dd-244">문서 끝의 링크 참조:</span><span class="sxs-lookup"><span data-stu-id="4c9dd-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="4c9dd-245">링크 앞에 쉼표 뒤에 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="4c9dd-246">다른 기술 문서에 연결할 때 공백을 포함하지 못한 경우 게시된 문서에서 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="4c9dd-247">기술 문서 집합의 일부가 아닌 페이지에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="4c9dd-248">다른 Microsoft 속성의 페이지(가격 책정 페이지, SLA 페이지 또는 설명서 문서가 아닌 다른 페이지)에 연결하려면 절대 URL을 사용하지만 로캘을 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="4c9dd-249">여기서 목적은 링크가 GitHub 및 렌더링된 사이트에서 작동하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="4c9dd-250">타사 사이트에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="4c9dd-250">Links to third-party sites</span></span>

<span data-ttu-id="4c9dd-251">멋진 사용자 환경은 사용자를 다른 사이트에 보내는 작업을 최소화합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="4c9dd-252">따라서 간혹 필요한 타사 사이트에 대한 링크는 다음 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="4c9dd-253">**책임감**: 공유하려는 정보가 타사 정보인 경우 타사 콘텐츠에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="4c9dd-254">예를 들어 사용자에게 Android 개발자 도구를 사용하는 방법을 알려주는 것은 Microsoft이 해야 할 일이 아닙니다. 해당 작업은 Google에서 담당하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="4c9dd-255">필요한 경우 Azure*에서* Android 개발자 도구를 사용하는 방법을 설명할 수 있지만 Google에서도 해당 도구를 사용하는 방법을 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="4c9dd-256">**PM 승인**: 타사 콘텐츠에 대해 Microsoft에서 승인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="4c9dd-257">링크를 설정한다는 것은 Microsoft가 해당 사이트를 신뢰한다는 것을 의미하며 사람들이 지침을 따를 경우 Microsoft에도 의무가 있다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="4c9dd-258">**유효 시간 검토**: 타사 정보가 여전히 최신 정보이고 정확하며 관련성이 있는지 확인하고 링크가 변경되지 않았는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="4c9dd-259">**오프사이트**: 사용자가 다른 사이트로 이동한다는 점을 인식하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="4c9dd-260">이에 대한 명확한 내용이 없을 경우 설명하는 문구를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="4c9dd-261">예: “필수 구성 요소에는 Android Studio 사이트에서 다운로드할 수 있는 Android 개발자 도구가 포함됩니다.”</span><span class="sxs-lookup"><span data-stu-id="4c9dd-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="4c9dd-262">**다음 단계**: “다음 단계” 섹션에 MVP 블로그 같은 링크를 추가해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="4c9dd-263">다시 한번 말하지만, 사용자가 사이트를 벗어난다는 점을 이해하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="4c9dd-264">**법적 정보**: 모든 microsoft.com 페이지의 **사용 약관** 바닥글에 **타사 사이트에 대한 링크**의 법적 정보가 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9dd-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 브라우저]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[자동 완성 사이트]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
