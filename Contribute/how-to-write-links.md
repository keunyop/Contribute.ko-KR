---
title: 설명서에서 링크를 사용하는 방법
description: 이 문서에서는 docs.microsoft.com 내의 콘텐츠에 대한 링크를 만드는 방법에 대한 지침을 제공합니다.
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: e56bc0fe3a5428af2a79641a8959b4da21270d53
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609433"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="52582-103">설명서에서 링크 사용</span><span class="sxs-lookup"><span data-stu-id="52582-103">Using links in documentation</span></span>
<span data-ttu-id="52582-104">이 문서에서는 docs.microsoft.com에서 호스팅되는 페이지의 하이퍼 링크를 사용하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="52582-105">링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="52582-106">사용자는 링크를 통해 동일한 페이지의 콘텐츠를 가리키거나, 인접한 다른 페이지를 가리키거나, 외부 사이트 및 URL을 가리킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="52582-107">docs.microsoft.com 사이트 백 엔드에서는 DFM(DocFX Flavored Markdown)을 구현하는 OPS(Open Publishing Services)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="52582-108">DFM은 GFM(GitHub Flavored Markdown)과 잘 호환되며, Markdown 확장을 통해 추가 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52582-109">대상이 링크를 지원하는 경우(대부분 지원) 모든 링크는 보안 링크여야 합니다(`https` 및 `http`).</span><span class="sxs-lookup"><span data-stu-id="52582-109">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="52582-110">링크 텍스트</span><span class="sxs-lookup"><span data-stu-id="52582-110">Link text</span></span>

<span data-ttu-id="52582-111">링크 텍스트에 포함하는 단어는 친근해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-111">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="52582-112">즉, 일반적인 영어(한국어) 단어 또는 연결하는 페이지의 제목이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-112">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52582-113">"여기를 클릭하세요."를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-113">Do not use "click here."</span></span> <span data-ttu-id="52582-114">검색 엔진 최적화에 좋지 않으며 대상을 적절하게 설명하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-114">It's bad for search engine optimization, and doesn't adequately describe the target.</span></span>

<span data-ttu-id="52582-115">**올바름:**</span><span class="sxs-lookup"><span data-stu-id="52582-115">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="52582-116">**잘못됨:**</span><span class="sxs-lookup"><span data-stu-id="52582-116">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="52582-117">하나의 문서에서 다른 문서로 링크</span><span class="sxs-lookup"><span data-stu-id="52582-117">Links from one article to another</span></span>

<span data-ttu-id="52582-118">한 Docs 기술 문서에서 동일한 docset 내의 다른 Docs 기술 문서로의 인라인 링크를 만들려면 다음과 같은 링크 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-118">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="52582-119">디렉토리의 문서는 동일한 디렉토리에 있는 다른 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-119">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="52582-120">문서는 하위 디렉토리에서 루트 디렉터리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-120">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="52582-121">루트 디렉터리의 문서는 하위 디렉토리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-121">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="52582-122">하위 디렉토리의 문서는 다른 하위 디렉토리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-122">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="52582-123">docset 간에 연결하는 문서(동일한 리포지토리에 있는 경우도 해당):  `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="52582-123">An article linking across docsets (even if in the same repository):  `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52582-124">위의 예제에서는 `~/`를 링크의 일부로 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-124">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="52582-125">리포지토리의 루트에서 경로에 연결하는 경우 `/`로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-125">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="52582-126">GitHub에서 원본 리포지토리로 이동할 때 `~/`를 포함하면 유효하지 않은 링크가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="52582-127">`/`로 경로를 시작하면 올바르게 해결됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-127">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="52582-128">앵커에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="52582-128">Links to anchors</span></span>

<span data-ttu-id="52582-129">앵커를 만들 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-129">You do not have to create anchors.</span></span> <span data-ttu-id="52582-130">앵커는 모든 H2 제목에서 게시 시간에 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-130">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="52582-131">H2 섹션에 대한 링크를 만들기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-131">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="52582-132">동일한 문서 내의 제목에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="52582-132">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="52582-133">동일한 하위 디렉토리의 다른 문서에 있는 앵커에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="52582-133">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="52582-134">다른 서비스 하위 디렉토리에 있는 앵커에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="52582-134">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="52582-135">포함되는 내용의 링크</span><span class="sxs-lookup"><span data-stu-id="52582-135">Links from includes</span></span>

<span data-ttu-id="52582-136">포함되는 파일은 다른 디렉토리에 위치하기 때문에 더 긴 상대 경로를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-136">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="52582-137">포함되는 파일의 문서에 연결하려면 이 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-137">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="52582-138">선택기의 링크</span><span class="sxs-lookup"><span data-stu-id="52582-138">Links in selectors</span></span>

<span data-ttu-id="52582-139">선택기는 설명서 문서에 드롭다운 목록으로 표시되는 탐색 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="52582-139">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="52582-140">reader가 드롭다운에서 값을 선택하면 브라우저가 선택한 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="52582-140">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="52582-141">일반적으로 선택기 목록에는 밀접하게 관련된 문서에 대한 링크가 포함되어 있습니다(예: 여러 프로그래밍 언어의 동일한 주제 또는 밀접하게 관련된 문서 시리즈).</span><span class="sxs-lookup"><span data-stu-id="52582-141">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="52582-142">포함되는 내용에 포함된 선택기가 있는 경우 다음과 같은 링크 구조체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-142">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="52582-143">참조 스타일 링크</span><span class="sxs-lookup"><span data-stu-id="52582-143">Reference-style links</span></span>

<span data-ttu-id="52582-144">소스 콘텐츠를 쉽게 읽을 수 있도록 참조 스타일 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-144">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="52582-145">참조 스타일 링크는 인라인 링크 구문을, 긴 URL을 문서 끝으로 이동시킨 간소화된 구문으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="52582-145">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="52582-146">[Daring Fireball](https://daringfireball.net/projects/markdown/)의 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-146">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="52582-147">인라인 텍스트:</span><span class="sxs-lookup"><span data-stu-id="52582-147">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="52582-148">문서 끝의 링크 참조:</span><span class="sxs-lookup"><span data-stu-id="52582-148">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="52582-149">링크 앞에 쉼표 뒤에 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-149">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="52582-150">다른 기술 문서에 연결할 때 공백을 포함하지 못한 경우 게시된 문서에서 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-150">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="52582-151">기술 문서 집합의 일부가 아닌 페이지에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="52582-151">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="52582-152">다른 Microsoft 속성의 페이지(가격 책정 페이지, SLA 페이지 또는 설명서 문서가 아닌 다른 페이지)에 연결하려면 절대 URL을 사용하지만 로캘을 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-152">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="52582-153">여기서 목적은 링크가 GitHub 및 렌더링된 사이트에서 작동하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="52582-153">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="52582-154">타사 사이트에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="52582-154">Links to third-party sites</span></span>

<span data-ttu-id="52582-155">멋진 사용자 환경은 사용자를 다른 사이트에 보내는 작업을 최소화합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-155">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="52582-156">따라서 간혹 필요한 타사 사이트에 대한 링크는 다음 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-156">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="52582-157">**책임성:** 공유하려는 정보가 타사 정보인 경우 타사 콘텐츠에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-157">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="52582-158">예를 들어 사용자에게 Android 개발자 도구를 사용하는 방법을 알려주는 것은 Microsoft이 해야 할 일이 아닙니다. 해당 작업은 Google에서 담당하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52582-158">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="52582-159">필요한 경우 Azure*에서* Android 개발자 도구를 사용하는 방법을 설명할 수 있지만 Google에서도 해당 도구를 사용하는 방법을 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-159">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="52582-160">**PM 승인**: 타사 콘텐츠에 대해 Microsoft에서 승인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-160">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="52582-161">링크를 설정한다는 것은 Microsoft가 해당 사이트를 신뢰한다는 것을 의미하며 사람들이 지침을 따를 경우 Microsoft에도 의무가 있다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="52582-161">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="52582-162">**유효 시간 검토:** 타사 정보가 최신 정보이고 정확하며 관련성이 있는지 확인하고 링크가 변경되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-162">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="52582-163">**오프사이트:** 사용자가 다른 사이트로 이동한다는 점을 인식하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-163">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="52582-164">이에 대한 명확한 내용이 없을 경우 설명하는 문구를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-164">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="52582-165">예: "필수 조건에는 Android 개발자 도구가 포함되며 Android Studio 사이트에서 다운로드할 수 있습니다."</span><span class="sxs-lookup"><span data-stu-id="52582-165">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="52582-166">**다음 단계:** "다음 단계" 섹션에서 예를 들어 MVP 블로그에 대한 링크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-166">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="52582-167">다시 한 번 사용자가 사이트를 벗어난다는 점을 인식하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-167">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="52582-168">**법적 정보:** 모든 ms.com 페이지의 **사용 조건** 바닥글에 **타사 사이트에 대한 링크**의 법적 정보가 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-168">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="52582-169">MSDN 또는 TechNet에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="52582-169">Links to MSDN or TechNet</span></span>

<span data-ttu-id="52582-170">MSDN 또는 TechNet에 연결해야 하는 경우 항목에 대한 전체 링크를 사용하고 링크에서 "en-us" 언어 로캘을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-170">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="52582-171">Azure PowerShell 참조 콘텐츠에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="52582-171">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="52582-172">Azure PowerShell 참조 콘텐츠는 2016년 11월부터 몇 가지 내용이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-172">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="52582-173">docs.microsoft.com의 다른 문서에서 이 콘텐츠에 연결하는 다음 지침을 사용하니다.</span><span class="sxs-lookup"><span data-stu-id="52582-173">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="52582-174">URL의 구조체:</span><span class="sxs-lookup"><span data-stu-id="52582-174">Structure of the URL:</span></span>

* <span data-ttu-id="52582-175">cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="52582-175">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="52582-176">개념 항목의 경우:</span><span class="sxs-lookup"><span data-stu-id="52582-176">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="52582-177">`<moniker-name>` 부분은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="52582-177">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="52582-178">생략된 경우 콘텐츠의 최신 버전으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-178">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="52582-179">`<service-name>` 부분은 다음과 같은 기본 URL에 표시되는 예제의 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="52582-179">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="52582-180">Azure PowerShell(AzureRM) 콘텐츠: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="52582-180">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="52582-181">Azure PowerShell(ASM) 콘텐츠: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="52582-181">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="52582-182">AzureAD(Azure Active Directory) PowerShell 콘텐츠: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="52582-182">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="52582-183">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="52582-183">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="52582-184">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="52582-184">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="52582-185">Azure Elastic DB 작업 PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="52582-185">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="52582-186">이러한 URL을 사용하는 경우 콘텐츠의 최신 버전으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-186">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="52582-187">이러한 방식으로 버전 모니커를 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-187">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="52582-188">그러면 버전이 변경될 때 업데이트되어야 하는 개념 콘텐츠에 대한 링크가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52582-188">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="52582-189">올바른 링크를 만들려면 브라우저에서 연결하려는 페이지를 찾고 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-189">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="52582-190">그런 다음, `https://docs.microsoft.com` 및 로캘 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-190">Then, remove  `https://docs.microsoft.com` and the locale info.</span></span>

<span data-ttu-id="52582-191">TOC에서 연결하는 경우 로캘 정보 없이 전체 URL을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52582-191">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="52582-192">예제 Markdown:</span><span class="sxs-lookup"><span data-stu-id="52582-192">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
