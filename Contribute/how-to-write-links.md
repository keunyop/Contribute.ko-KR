---
title: 설명서에서 링크를 사용하는 방법
description: 이 문서에서는 docs.microsoft.com 내의 콘텐츠에 대한 링크를 만드는 방법에 대한 지침을 제공합니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="9e668-103">설명서에서 링크 사용</span><span class="sxs-lookup"><span data-stu-id="9e668-103">Using links in documentation</span></span>
<span data-ttu-id="9e668-104">이 문서에서는 docs.microsoft.com에서 호스팅되는 페이지의 하이퍼 링크를 사용하는 방법에 대해 설명합니다. 링크는 몇 가지 다양한 규칙을 사용하여 Markdown에 쉽게 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com. Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="9e668-105">사용자는 링크를 통해 동일한 페이지의 콘텐츠를 가리키거나, 인접한 다른 페이지를 가리키거나, 외부 사이트 및 URL을 가리킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-105">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="9e668-106">docs.microsoft.com 사이트 백 엔드에서는 DFM(DocFX Flavored Markdown)을 구현하는 OPS(Open Publishing Services)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="9e668-107">DFM은 GFM(GitHub Flavored Markdown)과 잘 호환되며, Markdown 확장을 통해 추가 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-107">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e668-108">대상이 링크를 지원하는 경우(대부분 지원) 모든 링크는 보안 링크여야 합니다(`https` 및 `http`).</span><span class="sxs-lookup"><span data-stu-id="9e668-108">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="9e668-109">링크 텍스트</span><span class="sxs-lookup"><span data-stu-id="9e668-109">Link text</span></span>

<span data-ttu-id="9e668-110">링크 텍스트에 포함하는 단어는 친근해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-110">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="9e668-111">즉, 일반적인 영어(한국어) 단어 또는 연결하는 페이지의 제목이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-111">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e668-112">"여기를 클릭하세요."를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-112">Do not use "click here."</span></span> <span data-ttu-id="9e668-113">SEO에 올바르지 않고 대상을 적절하게 설명하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-113">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="9e668-114">**올바름:**</span><span class="sxs-lookup"><span data-stu-id="9e668-114">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="9e668-115">**잘못됨:**</span><span class="sxs-lookup"><span data-stu-id="9e668-115">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="9e668-116">하나의 문서에서 다른 문서로 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-116">Links from one article to another</span></span>

<span data-ttu-id="9e668-117">한 Docs 기술 문서에서 동일한 docset 내의 다른 Docs 기술 문서로의 인라인 링크를 만들려면 다음과 같은 링크 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-117">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="9e668-118">디렉토리의 문서는 동일한 디렉토리에 있는 다른 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-118">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="9e668-119">문서는 하위 디렉토리에서 루트 디렉터리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-119">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="9e668-120">루트 디렉터리의 문서는 하위 디렉토리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-120">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="9e668-121">하위 디렉토리의 문서는 다른 하위 디렉토리에 있는 문서로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-121">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="9e668-122">docset 간에 연결하는 문서(동일한 리포지토리에 있는 경우도 해당): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="9e668-122">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="9e668-123">앵커에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-123">Links to anchors</span></span>

<span data-ttu-id="9e668-124">앵커를 만들 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-124">You do not have to create anchors.</span></span> <span data-ttu-id="9e668-125">앵커는 모든 H2 제목에서 게시 시간에 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-125">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="9e668-126">H2 섹션에 대한 링크를 만들기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-126">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="9e668-127">동일한 문서 내의 제목에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="9e668-127">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="9e668-128">동일한 하위 디렉토리의 다른 문서에 있는 앵커에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="9e668-128">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="9e668-129">다른 서비스 하위 디렉토리에 있는 앵커에 연결하려면</span><span class="sxs-lookup"><span data-stu-id="9e668-129">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="9e668-130">포함되는 내용의 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-130">Links from includes</span></span>

<span data-ttu-id="9e668-131">포함되는 파일은 다른 디렉토리에 위치하기 때문에 더 긴 상대 경로를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-131">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="9e668-132">포함되는 파일의 문서에 연결하려면 이 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-132">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="9e668-133">선택기의 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-133">Links in selectors</span></span>

<span data-ttu-id="9e668-134">Azure 문서 팀이 수행하는 대로 포함되는 내용에 포함된 선택기가 있는 경우 다음과 같은 링크 구조체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-134">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="9e668-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="9e668-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="9e668-136">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="9e668-136">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="9e668-137">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="9e668-137">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="9e668-138">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="9e668-138">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="9e668-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="9e668-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="9e668-140">참조 스타일 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-140">Reference-style links</span></span>

<span data-ttu-id="9e668-141">소스 콘텐츠를 쉽게 읽을 수 있도록 참조 스타일 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-141">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="9e668-142">참조 스타일 링크는 인라인 링크 구문을, 긴 URL을 문서 끝으로 이동시킨 간소화된 구문으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-142">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="9e668-143">[Daring Fireball](https://daringfireball.net/projects/markdown/)의 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-143">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="9e668-144">인라인 텍스트:</span><span class="sxs-lookup"><span data-stu-id="9e668-144">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="9e668-145">문서 끝의 링크 참조:</span><span class="sxs-lookup"><span data-stu-id="9e668-145">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="9e668-146">링크 앞에 쉼표 뒤에 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-146">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="9e668-147">다른 기술 문서에 연결할 때 공백을 포함하지 못한 경우 게시된 문서에서 링크가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-147">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="9e668-148">기술 문서 집합의 일부가 아닌 페이지에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-148">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="9e668-149">다른 Microsoft 속성의 페이지(가격 책정 페이지, SLA 페이지 또는 설명서 문서가 아닌 다른 페이지)에 연결하려면 절대 URL을 사용하지만 로캘을 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-149">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="9e668-150">여기서 목적은 링크가 GitHub 및 렌더링된 사이트에서 작동하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-150">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="9e668-151">타사 사이트에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-151">Links to third-party sites</span></span>

<span data-ttu-id="9e668-152">멋진 사용자 환경은 사용자를 다른 사이트에 보내는 작업을 최소화합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-152">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="9e668-153">따라서 간혹 필요한 타사 사이트에 대한 링크는 다음 정보를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-153">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="9e668-154">**책임성:** 공유하려는 정보가 타사 정보인 경우 타사 콘텐츠에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-154">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="9e668-155">예를 들어 사용자에게 Android 개발자 도구를 사용하는 방법을 알려주는 것은 Microsoft이 해야 할 일이 아닙니다. 해당 작업은 Google에서 담당하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-155">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="9e668-156">필요한 경우 Azure*에서* Android 개발자 도구를 사용하는 방법을 설명할 수 있지만 Google에서도 해당 도구를 사용하는 방법을 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-156">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="9e668-157">**PM 승인**: 타사 콘텐츠에 대해 Microsoft에서 승인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-157">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="9e668-158">링크를 설정한다는 것은 Microsoft가 해당 사이트를 신뢰한다는 것을 의미하며 사람들이 지침을 따를 경우 Microsoft에도 의무가 있다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-158">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="9e668-159">**유효 시간 검토:** 타사 정보가 최신 정보이고 정확하며 관련성이 있는지 확인하고 링크가 변경되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-159">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="9e668-160">**오프사이트:** 사용자가 다른 사이트로 이동한다는 점을 인식하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-160">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="9e668-161">이에 대한 명확한 내용이 없을 경우 설명하는 문구를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-161">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="9e668-162">예: "필수 조건에는 Android 개발자 도구가 포함되며 Android Studio 사이트에서 다운로드할 수 있습니다."</span><span class="sxs-lookup"><span data-stu-id="9e668-162">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="9e668-163">**다음 단계:** "다음 단계" 섹션에서 예를 들어 MVP 블로그에 대한 링크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-163">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="9e668-164">다시 한 번 사용자가 사이트를 벗어난다는 점을 인식하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-164">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="9e668-165">**법적 정보:** 모든 ms.com 페이지의 **사용 조건** 바닥글에 **타사 사이트에 대한 링크**의 법적 정보가 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-165">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="9e668-166">MSDN 또는 TechNet에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-166">Links to MSDN or TechNet</span></span>

<span data-ttu-id="9e668-167">MSDN 또는 TechNet에 연결해야 하는 경우 항목에 대한 전체 링크를 사용하고 링크에서 "en-us" 언어 로캘을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-167">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="9e668-168">Azure PowerShell 참조 콘텐츠에 대한 링크</span><span class="sxs-lookup"><span data-stu-id="9e668-168">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="9e668-169">Azure PowerShell 참조 콘텐츠는 2016년 11월부터 몇 가지 내용이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-169">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="9e668-170">docs.microsoft.com의 다른 문서에서 이 콘텐츠에 연결하는 다음 지침을 사용하니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-170">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="9e668-171">URL의 구조체:</span><span class="sxs-lookup"><span data-stu-id="9e668-171">Structure of the URL:</span></span>

* <span data-ttu-id="9e668-172">cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="9e668-172">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="9e668-173">개념 항목의 경우:</span><span class="sxs-lookup"><span data-stu-id="9e668-173">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="9e668-174">&lt;moniker-name&gt; 부분은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-174">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="9e668-175">생략된 경우 콘텐츠의 최신 버전으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-175">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="9e668-176">&lt;service-name&gt; 부분은 다음과 같은 기본 URL에 표시되는 예제의 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-176">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="9e668-177">Azure PowerShell(AzureRM) 콘텐츠: https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="9e668-177">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="9e668-178">Azure PowerShell(ASM) 콘텐츠: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="9e668-178">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="9e668-179">Azure Active Directory(AzureAD) PowerShell 콘텐츠: https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="9e668-179">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="9e668-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="9e668-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="9e668-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="9e668-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="9e668-182">Azure Elastic DB 작업 PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="9e668-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="9e668-183">이러한 URL을 사용하는 경우 콘텐츠의 최신 버전으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-183">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="9e668-184">이러한 방식으로 버전 모니커를 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-184">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="9e668-185">그러면 버전이 변경될 때 업데이트되어야 하는 개념 콘텐츠에 대한 링크가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-185">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="9e668-186">올바른 링크를 만들려면 브라우저에서 연결하려는 페이지를 찾고 URL을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-186">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="9e668-187">그런 다음, “https://docs.microsoft.com” 및 로캘 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-187">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="9e668-188">TOC에서 연결하는 경우 로캘 정보 없이 전체 URL을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e668-188">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="9e668-189">예제 Markdown:</span><span class="sxs-lookup"><span data-stu-id="9e668-189">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
