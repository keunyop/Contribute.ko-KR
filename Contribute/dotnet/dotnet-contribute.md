---
title: .NET 문서 리포지토리에 참여
description: 이 문서에서는 .NET 설명서에서 구성되는 리포지토리의 문서 및 코드 샘플에 참여하는 프로세스를 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
ms.openlocfilehash: d1631f34ef9a3ceb10178792842421376fea97b0
ms.sourcegitcommit: 3774d06ddc1f92b2bdb4c1d8babbd18357229298
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/28/2020
ms.locfileid: "87264812"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a><span data-ttu-id="1faa8-103">.NET 문서 리포지토리에 참여하는 방법 알아보기</span><span class="sxs-lookup"><span data-stu-id="1faa8-103">Learn how to contribute to the .NET docs repositories</span></span>

<span data-ttu-id="1faa8-104">.NET 문서에 참여해 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-104">Thank you for your interest in contributing to the .NET documentation!</span></span>

<span data-ttu-id="1faa8-105">이 문서에서는 [.NET 문서 사이트](https://docs.microsoft.com/dotnet)에서 호스팅되는 문서 및 코드 샘플에 참여하는 프로세스를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-105">This document covers the process for contributing to the articles and code samples that are hosted on the [.NET documentation site](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="1faa8-106">기여는 오타 수정만큼 간단하거나 새로운 문서처럼 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="1faa8-107">.NET 문서 사이트는 여러 리포지토리에서 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-107">The .NET documentation site is built from multiple repositories:</span></span>

- [<span data-ttu-id="1faa8-108">.NET 개념 문서 및 코드 조각</span><span class="sxs-lookup"><span data-stu-id="1faa8-108">.NET conceptual articles and code snippets</span></span>](https://github.com/dotnet/docs)
- [<span data-ttu-id="1faa8-109">코드 샘플 및 코드 조각</span><span class="sxs-lookup"><span data-stu-id="1faa8-109">Code samples and snippets</span></span>](https://github.com/dotnet/samples)
- [<span data-ttu-id="1faa8-110">.NET 표준, .NET Core, .NET Framework API 참조</span><span class="sxs-lookup"><span data-stu-id="1faa8-110">.NET Standard, .NET Core, .NET Framework API reference</span></span>](https://github.com/dotnet/dotnet-api-docs)
- [<span data-ttu-id="1faa8-111">.NET Compiler Platform SDK 참조</span><span class="sxs-lookup"><span data-stu-id="1faa8-111">.NET Compiler Platform SDK reference</span></span>](https://github.com/dotnet/roslyn-api-docs)
- [<span data-ttu-id="1faa8-112">ML.NET API 참조</span><span class="sxs-lookup"><span data-stu-id="1faa8-112">ML.NET API reference</span></span>](https://github.com/dotnet/ml-api-docs)

<span data-ttu-id="1faa8-113">이 리포지토리 모두에 대한 문제는 [dotnet/docs](https://github.com/dotnet/docs/issues) 리포지토리에서 추적됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-113">Issues for all these repositories are tracked in the [dotnet/docs](https://github.com/dotnet/docs/issues) repository.</span></span>

## <a name="guidelines-for-contributions"></a><span data-ttu-id="1faa8-114">기여 지침</span><span class="sxs-lookup"><span data-stu-id="1faa8-114">Guidelines for contributions</span></span>

<span data-ttu-id="1faa8-115">문서에 대한 커뮤니티 기여에 감사드립니다. 다음 목록에서는 .NET 설명서에 기여할 때 주의해야 할 몇 가지 지침 규칙을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-115">We appreciate community contributions to docs. The following list shows some guiding rules to keep in mind when you're contributing to the .NET documentation:</span></span>

- <span data-ttu-id="1faa8-116">많은 끌어오기 요청으로 놀라게 **하지 마세요**.</span><span class="sxs-lookup"><span data-stu-id="1faa8-116">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="1faa8-117">대신, 많은 시간을 투자하기 전에 문제를 제기하고 토론을 시작하여 하나의 방향에 동의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-117">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="1faa8-118">**DO**는 다음 지침과 [음성 및 톤](dotnet-voice-tone.md) 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-118">**DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.</span></span>
- <span data-ttu-id="1faa8-119">**DO**는 [템플릿](dotnet-style-guide.md) 파일을 작업의 시작점으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-119">**DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="1faa8-120">**DO**는 문서를 작업하기 전에 포크에 별도의 분기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-120">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="1faa8-121">[GitHub 흐름](https://guides.github.com/introduction/flow/)을 **따릅니다**.</span><span class="sxs-lookup"><span data-stu-id="1faa8-121">**DO** follow the [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>
- <span data-ttu-id="1faa8-122">원하는 경우 기여에 관해 블로그 및 트윗(또는 기타)을 **합니다**.</span><span class="sxs-lookup"><span data-stu-id="1faa8-122">**DO** blog and tweet (or whatever) about your contributions if you like!</span></span>

<span data-ttu-id="1faa8-123">이러한 지침을 따르면 모두에게 더 나은 환경을 제공할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-123">Following these guidelines will ensure a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-net-docs"></a><span data-ttu-id="1faa8-124">.NET 문서에 기여하기</span><span class="sxs-lookup"><span data-stu-id="1faa8-124">Make a contribution to .NET docs</span></span>

<span data-ttu-id="1faa8-125">**1단계:** 새 콘텐츠를 작성하거나 기존 콘텐츠를 완전히 개정하려는 경우 수행할 작업을 설명하는 [문제](https://github.com/dotnet/docs/issues)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-125">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do.</span></span> <span data-ttu-id="1faa8-126">**문서** 폴더 내의 콘텐츠는 TOC(목차)에 반영된 섹션으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-126">The content inside the **docs** folder is organized into sections that are reflected in the Table of Contents (TOC).</span></span> <span data-ttu-id="1faa8-127">토픽에서 TOC에 있는 위치를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-127">Define where the topic will be located in the TOC.</span></span> <span data-ttu-id="1faa8-128">제안에 대한 피드백을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-128">Get feedback on your proposal.</span></span>

<span data-ttu-id="1faa8-129">-또는-</span><span class="sxs-lookup"><span data-stu-id="1faa8-129">-or-</span></span>

<span data-ttu-id="1faa8-130">기존 문제를 선택하고 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-130">Choose an existing issue and address it.</span></span> <span data-ttu-id="1faa8-131">다음과 같은 방법으로, [미해결 문제](https://github.com/dotnet/docs/issues) 목록을 보고 관심 있는 분야의 문제 해결에 자발적으로 참여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-131">You can look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in:</span></span>

- <span data-ttu-id="1faa8-132">[good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 레이블로 필터링하여 적절한 첫 번째 문제를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-132">Filter by the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) label for, well, good first issues.</span></span>
- <span data-ttu-id="1faa8-133">[up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 레이블로 필터링하여 커뮤니티 기여에 적합한 문제를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-133">Filter by the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label for issues appropriate for community contribution.</span></span> <span data-ttu-id="1faa8-134">이 문제는 일반적으로 최소한의 컨텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-134">These issues usually require minimal context.</span></span>
- <span data-ttu-id="1faa8-135">숙련된 기여자는 관심 있는 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-135">Experienced contributors can tackle any issues of interest.</span></span>

<span data-ttu-id="1faa8-136">참여할 문제를 찾았으면 해당 문제가 미해결 상태인지 확인하기 위한 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-136">When you find an issue to work on, add a comment to ask if it's open.</span></span>

<span data-ttu-id="1faa8-137">참여할 작업을 선택한 후 [시작하기](../get-started-setup-github.md) 가이드에 따라 GitHub 계정을 만들고 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-137">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and set up your environment.</span></span>

<span data-ttu-id="1faa8-138">**2단계:** 필요한 경우 `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` 또는 `dotnet/ml-api-docs` 리포지토리를 선택하여 변경 내용에 대한 분기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-138">**Step 2:** Fork the `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs`, or `dotnet/ml-api-docs` repos as needed and create a branch for your changes.</span></span>

<span data-ttu-id="1faa8-139">작은 변경 내용은 기여자 가이드의 [홈 페이지](../index.md#quick-edits-to-existing-documents)에서 GitHub의 편집 지침을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-139">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span>

<span data-ttu-id="1faa8-140">**3단계:** 이 새 분기를 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-140">**Step 3:** Make the changes on this new branch.</span></span>

<span data-ttu-id="1faa8-141">새 항목인 경우 이 [템플릿 파일](dotnet-style-guide.md)을 시작점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-141">If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point.</span></span> <span data-ttu-id="1faa8-142">작성 지침이 포함되어 있으며 작성자 정보와 같이 각 문서에 필요한 메타데이터도 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-142">It contains the writing guidelines and also explains the metadata required for each article, such as author information.</span></span> <span data-ttu-id="1faa8-143">docs.microsoft.com 사이트에서 사용되는 Markdown 구문에 대한 자세한 내용은 [Markdown 참조](../markdown-reference.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-143">For more information on the Markdown syntax used in the docs.microsoft.com site, see [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="1faa8-144">1단계에서 문서에 대해 결정된 TOC 위치에 해당하는 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-144">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span> <span data-ttu-id="1faa8-145">이 폴더에는 해당 섹션의 모든 문서에 대한 Markdown 파일이 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-145">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="1faa8-146">필요한 경우 콘텐츠용 파일을 배치할 새 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-146">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="1faa8-147">해당 섹션의 주요 문서는 *index.md*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-147">The main article for that section is called *index.md*.</span></span>

<span data-ttu-id="1faa8-148">이미지 및 기타 정적 리소스의 경우 문서를 포함하는 폴더 내에 **미디어**라는 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-148">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="1faa8-149">**미디어** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다(인덱스 파일 제외).</span><span class="sxs-lookup"><span data-stu-id="1faa8-149">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="1faa8-150">**코드 조각**의 경우 문서를 포함하는 폴더 내에 **조각**이라는 하위 폴더를 만듭니다(아직 없는 경우).</span><span class="sxs-lookup"><span data-stu-id="1faa8-150">For **code snippets**, create a subfolder called **snippets** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="1faa8-151">**조각** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-151">Inside the **snippets** folder, create a subfolder with the article name.</span></span> <span data-ttu-id="1faa8-152">대부분의 경우 주요 .NET 언어인 C#, F# 및 Visual Basic 등 세 가지 모두의 코드 조각이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-152">In most cases, you'll have code snippets for all three of the main .NET languages, C#, F#, and Visual Basic.</span></span> <span data-ttu-id="1faa8-153">이 경우 세 프로젝트 각각에 대해 **csharp**, **fsharp**, **vb**라는 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-153">In that case, create subfolders named **csharp**, **fsharp**, and **vb** for each of the three projects.</span></span> <span data-ttu-id="1faa8-154">[docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp) 또는 [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) 폴더 아래에 각 문서에 대한 코드 조각을 만드는 경우 해당 코드 조각은 한 언어로만 작성되므로 언어 하위 폴더를 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-154">If you're creating a snippet for an article under the [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp), or [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) folders, the snippet will only be in one language so you can omit the language subfolder.</span></span>

<span data-ttu-id="1faa8-155">코드 조각은 문서에 설명된 개념을 예시하는 요약된 작은 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-155">Code snippets are small, focused examples of code that demonstrate the concepts covered in an article.</span></span> <span data-ttu-id="1faa8-156">다운로드 및 탐색을 위한 큰 프로그램은 [dotnet/samples](https://github.com/dotnet/samples) 리포지토리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-156">Larger programs intended for download and exploration should be located in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="1faa8-157">전체 샘플은 [샘플에 참여](#contribute-to-samples)의 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-157">Full samples are covered in the section on [Contributing to samples](#contribute-to-samples).</span></span>

## <a name="example-folder-structure"></a><span data-ttu-id="1faa8-158">폴더 구조의 예</span><span class="sxs-lookup"><span data-stu-id="1faa8-158">Example folder structure</span></span>

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
```

<span data-ttu-id="1faa8-159">위의 구조에는 이미지 1개(*portability_report.png*) 및 *porting-overview.md* 문서에 포함된 **코드 조각**을 포함하는 코드 프로젝트 3개가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-159">The structure shown above includes one image, *portability_report.png*, and three code projects that include **code snippets** that are included in the *porting-overview.md* article.</span></span> <span data-ttu-id="1faa8-160">허용되는 대체 구조에는 언어별로 해당 폴더의 모든 문서에 대한 모든 코드 조각을 포함하는 프로젝트 1개가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-160">An accepted alternative structure contains one project per language that contains all snippets for all articles in that folder.</span></span> <span data-ttu-id="1faa8-161">이 대체 구조는 언어 구문을 예시하는 아주 작은 조각으로 인해 언어 참조 영역에서 사용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-161">This alternative has been used in the language reference areas because of very small snippets to demonstrate language syntax.</span></span> <span data-ttu-id="1faa8-162">다른 영역에는 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-162">It is discouraged in other areas.</span></span>

<span data-ttu-id="1faa8-163">포함된 조각 대부분이 기록을 위해 *dotnet/docs* 리포지토리의 */samples* 폴더 아래에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-163">For historical reasons, many of the included snippets are stored under the */samples* folder in the *dotnet/docs* repository.</span></span> <span data-ttu-id="1faa8-164">문서에 중대한 변경 내용을 적용하는 경우 해당 코드 조각을 새 구조로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-164">If you're making major changes to an article, those snippets should be moved to the new structure.</span></span> <span data-ttu-id="1faa8-165">소소한 변경인 경우에는 코드 조각을 이동하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-165">Do not move snippets for small changes.</span></span>

<span data-ttu-id="1faa8-166">**4단계:** 분기에서 마스터 분기로 PR(끌어오기 요청)을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-166">**Step 4:** Submit a Pull Request (PR) from your branch to the master branch.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1faa8-167">지금은 [주석 자동화](../how-to-write-workflows-major.md#review-and-sign-off) 기능을 .NET 리포지토리에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-167">The [comment automation](../how-to-write-workflows-major.md#review-and-sign-off) functionality is not available on any of the .NET docs repositories at this time.</span></span> <span data-ttu-id="1faa8-168">.NET 문서 팀의 구성원이 PR을 검토하고 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-168">Members of the .NET docs team will review and merge your PR.</span></span>

<span data-ttu-id="1faa8-169">각 PR은 일반적으로 한 번에 하나씩 문제를 해결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-169">Each PR should usually address one issue at a time.</span></span> <span data-ttu-id="1faa8-170">PR은 하나 또는 여러 개의 파일을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-170">The PR can modify one or multiple files.</span></span> <span data-ttu-id="1faa8-171">다른 파일의 여러 수정 사항을 해결하는 경우 PR을 별도로 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-171">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span> <span data-ttu-id="1faa8-172">markdown을 업데이트할 뿐만 아니라 샘플을 만드는 경우 샘플에 대해 별도의 PR을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-172">If you're creating samples as well as updating markdown, you'll need to create a separate PR for samples.</span></span>

<span data-ttu-id="1faa8-173">PR에서 기존 문제를 해결하는 경우 커밋 메시지 또는 PR 설명에 `Fixes #Issue_Number` 키워드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-173">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="1faa8-174">이렇게 하면 PR이 병합될 때 이 문제가 자동으로 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-174">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="1faa8-175">자세한 내용은 [커밋 메시지를 통해 문제 닫기](https://help.github.com/articles/closing-issues-via-commit-messages/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1faa8-175">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="1faa8-176">.NET 팀은 PR을 검토하고 승인을 위해 필요한 다른 업데이트/변경 내용이 있는지 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-176">The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.</span></span>

<span data-ttu-id="1faa8-177">**5단계:** 팀과 논의한 대로 분기에 필요한 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-177">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="1faa8-178">유지관리자는 피드백이 적용되고 변경 내용이 승인되면 PR을 마스터 분기 내에 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-178">The maintainers will merge your PR into the master branch once feedback has been applied and your change is approved.</span></span>

<span data-ttu-id="1faa8-179">정기적으로 마스터 분기의 모든 커밋을 라이브 분기로 푸시하면 https://docs.microsoft.com/dotnet/ 에서 라이브로 기여한 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-179">We regularly push all commits from master branch into the live branch and then you'll be able to see your contribution live at https://docs.microsoft.com/dotnet/.</span></span> <span data-ttu-id="1faa8-180">일반적으로 업무 주간 동안 매일 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-180">We typically publish daily during the work week.</span></span>

## <a name="contribute-to-samples"></a><span data-ttu-id="1faa8-181">샘플에 기여</span><span class="sxs-lookup"><span data-stu-id="1faa8-181">Contribute to samples</span></span>

<span data-ttu-id="1faa8-182">콘텐츠를 지원하는 코드는 다음과 같이 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-182">We make the following distinction for code that supports our content:</span></span>

- <span data-ttu-id="1faa8-183">샘플: readers는 샘플을 다운로드하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-183">Samples: readers can download and run the samples.</span></span> <span data-ttu-id="1faa8-184">모든 샘플은 완전한 애플리케이션 또는 라이브러리여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-184">All samples should be complete applications or libraries.</span></span> <span data-ttu-id="1faa8-185">샘플이 라이브러리를 작성하는 곳에서는 readers가 코드를 실행할 수 있는 단위 테스트 또는 애플리케이션을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-185">Where the sample creates a library, it should include unit tests or an application that lets readers run the code.</span></span> <span data-ttu-id="1faa8-186">종종 둘 이상의 기술, 기능 또는 도구 키트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-186">They often use more than one technology, feature, or toolkit.</span></span> <span data-ttu-id="1faa8-187">각 샘플의 readme.md 파일은 문서를 참조하므로 각 샘플에서 다루는 개념에 대해 자세히 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-187">The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.</span></span>
- <span data-ttu-id="1faa8-188">코드 조각: 더 작은 개념이나 작업을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-188">Snippets: illustrate a smaller concept or task.</span></span> <span data-ttu-id="1faa8-189">컴파일되지만 완전한 애플리케이션을 위한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-189">They compile but they are not intended to be complete applications.</span></span> <span data-ttu-id="1faa8-190">올바르게 실행되어야 하지만 일반적인 시나리오의 예제 애플리케이션은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-190">They should run correctly, but aren't an example application for a typical scenario.</span></span> <span data-ttu-id="1faa8-191">대신 단일 개념이나 기능을 설명하기 위해 가능한 한 작게 설계됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-191">Instead, they are designed to be as small as possible to illustrate a single concept or feature.</span></span> <span data-ttu-id="1faa8-192">단일 코드 화면을 초과하면 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-192">These should be no more than a single screen of code.</span></span>

<span data-ttu-id="1faa8-193">샘플은 [dotnet/samples](https://github.com/dotnet/samples) 리포지토리에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-193">Samples are stored in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="1faa8-194">샘플 폴더 구조는 문서 폴더 구조와 일치하는 모델로 작업하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-194">We are working toward a model where our samples folder structure matches our docs folder structure.</span></span> <span data-ttu-id="1faa8-195">따르는 표준은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-195">Standards that we follow are:</span></span>

- <span data-ttu-id="1faa8-196">최상위 폴더는 *docs* 리포지토리의 최상위 폴더와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-196">Top-level folders match the top level folders in the *docs* repository.</span></span> <span data-ttu-id="1faa8-197">예를 들어 문서 리포지토리에는 *machine-learning/tutorials* 폴더가 있고, 기계 학습 자습서 샘플은 *samples/machine-learning/tutorials* 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-197">For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.</span></span>

<span data-ttu-id="1faa8-198">또한 *핵심* 및 *표준* 폴더 아래의 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼에서 빌드하고 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-198">In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core.</span></span> <span data-ttu-id="1faa8-199">CI 빌드 시스템이 이를 시행할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-199">Our CI build system will enforce that.</span></span> <span data-ttu-id="1faa8-200">최상위 수준 *프레임워크* 폴더에는 Windows에서만 빌드되고 유효성을 검사한 샘플이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-200">The top level *framework* folder contains samples that are only built and validated on Windows.</span></span>

<span data-ttu-id="1faa8-201">샘플 프로젝트는 지정된 샘플에 대해 가능한 가장 광범위한 플랫폼에서 빌드하고 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-201">Sample projects should build and run on the widest set of platforms possible for the given sample.</span></span> <span data-ttu-id="1faa8-202">실제로, 가능한 경우 .NET Core 기반 콘솔 애플리케이션을 빌드하는 것을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-202">In practice, that means building .NET Core-based console applications where possible.</span></span> <span data-ttu-id="1faa8-203">웹 또는 UI 프레임워크와 관련된 샘플은 필요에 따라 해당 도구를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-203">Samples that are specific to the web or a UI framework should add those tools as needed.</span></span> <span data-ttu-id="1faa8-204">예를 들어 웹 애플리케이션, 모바일 앱, WPF 또는 WinForms 앱 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-204">Examples include web applications, mobile apps, WPF or WinForms apps, and so on.</span></span>

<span data-ttu-id="1faa8-205">모든 코드에 대한 CI 시스템을 갖추기 위해 노력하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-205">We are working toward having a CI system in place for all code.</span></span> <span data-ttu-id="1faa8-206">샘플을 업데이트할 때 각 업데이트가 빌드 가능한 프로젝트의 일부인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-206">When you make any updates to samples, make sure each update is part of a buildable project.</span></span> <span data-ttu-id="1faa8-207">이상적으로 샘플의 정확성에 대한 테스트도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-207">Ideally, add tests for correctness on samples as well.</span></span>

<span data-ttu-id="1faa8-208">만드는 모든 샘플에는 *readme.md* 파일이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-208">Each complete sample that you create should contain a *readme.md* file.</span></span> <span data-ttu-id="1faa8-209">이 파일에는 샘플에 대한 간략한 설명(하나 또는 두 개의 단락)이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-209">This file should contain a short description of the sample (one or two paragraphs).</span></span> <span data-ttu-id="1faa8-210">*readme.md*에서는 readers에게 이 샘플을 탐구함으로써 무엇을 배울 것인지를 알려주어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-210">Your *readme.md* should tell readers what they will learn by exploring this sample.</span></span> <span data-ttu-id="1faa8-211">*readme.md* 파일에는 [.NET 문서 사이트](https://docs.microsoft.com/dotnet/welcome)에 있는 라이브 문서에 대한 링크도 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-211">The *readme.md* file should also contain a link to the live document on the [.NET documentation site](https://docs.microsoft.com/dotnet/welcome).</span></span> <span data-ttu-id="1faa8-212">리포지토리의 지정된 파일이 해당 사이트에 매핑되는 위치를 확인하려면 리포지토리 경로의 `/docs`를 `https://docs.microsoft.com/dotnet`으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-212">To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `https://docs.microsoft.com/dotnet`.</span></span>

<span data-ttu-id="1faa8-213">항목에는 샘플에 대한 링크도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-213">Your topic will also contain links to the sample.</span></span> <span data-ttu-id="1faa8-214">GitHub의 샘플 폴더에 직접 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-214">Link directly to the sample's folder on GitHub.</span></span>

### <a name="write-a-new-sample"></a><span data-ttu-id="1faa8-215">새 샘플 작성</span><span class="sxs-lookup"><span data-stu-id="1faa8-215">Write a new sample</span></span>

<span data-ttu-id="1faa8-216">샘플은 다운로드를 위한 전체 프로그램 및 라이브러리입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-216">Samples are full programs and libraries meant for download.</span></span> <span data-ttu-id="1faa8-217">샘플의 범위는 작을 수 있지만, 사용자가 직접 살펴보고 실험해 볼 수 있는 방법으로 개념을 예시합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-217">They may be small in scope, but they demonstrate concepts in a manner that enables people to explore and experiment on their own.</span></span> <span data-ttu-id="1faa8-218">예제에 대한 지침에 따라 독자는 다운로드하고 살펴볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-218">The guidelines for samples ensure readers can download and explore.</span></span> <span data-ttu-id="1faa8-219">각 지침의 예제로 [PLINQ(병렬 LINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) 샘플을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-219">Examine the [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) samples as an example of each of the guidelines.</span></span>

1. <span data-ttu-id="1faa8-220">샘플은 **빌드 가능한 프로젝트의 일부여야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="1faa8-220">Your sample **must be part of a buildable project**.</span></span> <span data-ttu-id="1faa8-221">가능한 경우 프로젝트는 .NET Core에서 지원하는 모든 플랫폼에 빌드되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-221">Where possible, the projects should build on all platforms supported by .NET Core.</span></span> <span data-ttu-id="1faa8-222">이에 대한 예외는 플랫폼별 기능 또는 플랫폼별 도구를 보여주는 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-222">Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.</span></span>

2. <span data-ttu-id="1faa8-223">샘플이 일관성을 유지하려면 [corefx 코딩 스타일](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md)을 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-223">Your sample should conform to the [corefx coding style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) to maintain consistency.</span></span>

   <span data-ttu-id="1faa8-224">또한 새 개체를 인스턴스화할 필요가 없는 것을 시연할 때 인스턴스 메서드보다 `static` 메서드를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-224">Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.</span></span>

3. <span data-ttu-id="1faa8-225">샘플에는 **적절한 예외 처리**가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-225">Your sample should include **appropriate exception handling**.</span></span> <span data-ttu-id="1faa8-226">샘플의 컨텍스트에서 throw될 수 있는 모든 예외를 처리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-226">It should handle all exceptions that are likely to be thrown in the context of the sample.</span></span> <span data-ttu-id="1faa8-227">예를 들어 사용자 입력을 검색하기 위해 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 메서드를 호출하는 샘플은 메서드에 대한 인수로 문자열을 전달할 때 적절한 예외 처리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-227">For example, a sample that calls the [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method.</span></span> <span data-ttu-id="1faa8-228">마찬가지로 샘플에서 메서드 호출이 실패할 것으로 예상되는 경우 결과 예외를 처리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-228">Similarly, if your sample expects a method call to fail, the resulting exception must be handled.</span></span> <span data-ttu-id="1faa8-229">[예외](https://docs.microsoft.com/dotnet/api/system.exception) 또는 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception)과 같은 기본 클래스 예외가 아닌 메서드가 throw한 특정 예외를 항상 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-229">Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](https://docs.microsoft.com/dotnet/api/system.exception) or [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).</span></span>

4. <span data-ttu-id="1faa8-230">샘플이 독립 실행형 패키지를 빌드하는 경우 샘플에서 사용하는 런타임 외에도 CI 빌드 시스템에서 사용하는 런타임을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-230">If your sample builds a standalone package, you must include the runtimes used by our CI build system, in addition to any runtimes used by your sample:</span></span>
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

<span data-ttu-id="1faa8-231">이러한 프로젝트를 곧 빌드할 수 있는 CI 시스템을 배치하게 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-231">We will have a CI system in place to build these projects shortly.</span></span>

<span data-ttu-id="1faa8-232">샘플을 만들려면:</span><span class="sxs-lookup"><span data-stu-id="1faa8-232">To create a sample:</span></span>

1. <span data-ttu-id="1faa8-233">[문제](https://github.com/dotnet/docs/issues)를 제출하거나 작업 중인 기존 보고서에 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-233">File an [issue](https://github.com/dotnet/docs/issues) or add a comment to an existing one that you are working on it.</span></span>
2. <span data-ttu-id="1faa8-234">샘플에 설명된 개념을 설명하는 항목을 작성합니다(예: `docs/standard/linq/where-clause.md`).</span><span class="sxs-lookup"><span data-stu-id="1faa8-234">Write the topic that explains the concepts demonstrated in your sample (example: `docs/standard/linq/where-clause.md`).</span></span>
3. <span data-ttu-id="1faa8-235">샘플을 작성합니다(예: `WhereClause-Sample1.cs`).</span><span class="sxs-lookup"><span data-stu-id="1faa8-235">Write your sample (example: `WhereClause-Sample1.cs`).</span></span>
4. <span data-ttu-id="1faa8-236">샘플을 호출하는 주 진입점이 있는 Program.cs를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-236">Create a Program.cs with a Main entry point that calls your samples.</span></span> <span data-ttu-id="1faa8-237">이미 있는 경우에는 샘플에 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-237">If there is already one there, add the call to your sample:</span></span>

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

<span data-ttu-id="1faa8-238">[.NET Core SDK](https://www.microsoft.com/net/download)와 함께 설치할 수 있는 .NET Core CLI를 사용하여 .NET Core 코드 조각 또는 샘플을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-238">You build any .NET Core snippet or sample using the .NET Core CLI, which can be installed with [the .NET Core SDK](https://www.microsoft.com/net/download).</span></span> <span data-ttu-id="1faa8-239">샘플을 빌드하고 실행하려면:</span><span class="sxs-lookup"><span data-stu-id="1faa8-239">To build and run your sample:</span></span>

1. <span data-ttu-id="1faa8-240">샘플 폴더로 이동하여 오류를 확인하기 위해 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-240">Go to the sample folder and build to check for errors:</span></span>

    ```console
    dotnet build
    ```
2. <span data-ttu-id="1faa8-241">다음과 같이 샘플을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-241">Run your sample:</span></span>

    ```console
    dotnet run
    ```

3. <span data-ttu-id="1faa8-242">샘플의 루트 디렉터리에 readme.md를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-242">Add a readme.md to the root directory of your sample.</span></span>

   <span data-ttu-id="1faa8-243">여기에는 코드에 대한 간략한 설명이 포함되어야 하며 샘플을 참조하는 문서를 참조해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-243">This should include a brief description of the code, and refer people to the article that references the sample.</span></span> <span data-ttu-id="1faa8-244">*readme.md*의 맨 위에는 [샘플 브라우저](https://docs.microsoft.com/samples)에 필요한 메타데이터가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-244">The top of the *readme.md* must have the metadata required for the [samples browser](https://docs.microsoft.com/samples).</span></span> <span data-ttu-id="1faa8-245">헤더 블록에는 다음 필드가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-245">The header block should contain the following fields:</span></span>

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - <span data-ttu-id="1faa8-246">`languages` 컬렉션에는 샘플에 사용할 수 있는 언어만 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-246">The `languages` collection should include only those languages available for your sample.</span></span>
   - <span data-ttu-id="1faa8-247">`products` 컬렉션에는 샘플과 관련된 제품만 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-247">The `products` collection should include only those products relevant to your sample.</span></span>

<span data-ttu-id="1faa8-248">명시된 경우를 제외하고 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼의 명령줄에서 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-248">Except where noted, all samples build from the command line on any platform supported by .NET Core.</span></span> <span data-ttu-id="1faa8-249">Visual Studio와 관련된 샘플이 몇 가지 있으며 Visual Studio 2017 이상이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-249">There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later.</span></span> <span data-ttu-id="1faa8-250">또한 일부 샘플은 플랫폼별 기능을 나타내며 특정 플랫폼이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-250">In addition, some samples show platform specific features and will require a specific platform.</span></span> <span data-ttu-id="1faa8-251">다른 샘플 및 코드 조각에는 .NET Framework가 필요하고, Windows 플랫폼에서 실행되며, 대상 Framework 버전용 Developer Pack이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-251">Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.</span></span>

## <a name="the-c-interactive-experience"></a><span data-ttu-id="1faa8-252">C# 대화형 환경</span><span class="sxs-lookup"><span data-stu-id="1faa8-252">The C# interactive experience</span></span>

<span data-ttu-id="1faa8-253">문서에 포함된 모든 샘플은 [언어 태그](../code-in-docs.md)를 사용하여 원본 언어를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-253">All samples included in an article use a [language tag](../code-in-docs.md) to indicate the source language.</span></span> <span data-ttu-id="1faa8-254">C#의 짧은 코드 샘플은 `csharp-interactive` 언어 태그를 사용하여 브라우저에서 실행되는 C# 샘플을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-254">Short code samples in C# can use the `csharp-interactive` language tag to specify a C# sample that runs in the browser.</span></span> <span data-ttu-id="1faa8-255">(인라인 코드 샘플은 `csharp-interactive` 태그를 사용하고, 소스에서 포함된 코드 조각의 경우 `code-csharp-interactive` 태그를 사용합니다.) 이러한 코드 샘플은 문서에 코드 창과 출력창을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-255">(Inline code samples use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code samples display a code window and an output window in the article.</span></span> <span data-ttu-id="1faa8-256">출력 창은 사용자가 샘플을 실행한 후 대화형 코드를 실행할 때의 모든 출력을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-256">The output window displays any output from executing the interactive code once the user has run the sample.</span></span>

<span data-ttu-id="1faa8-257">C# 대화형 환경은 샘플 작업 방법을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-257">The C# interactive experience changes how we work with samples.</span></span> <span data-ttu-id="1faa8-258">방문자는 샘플을 실행하여 결과를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-258">Visitors can run the sample to see the results.</span></span> <span data-ttu-id="1faa8-259">샘플 또는 해당 텍스트에 출력에 대한 정보가 포함되어야 하는지 여부를 결정하는 데 많은 요인이 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-259">A number of factors help determine if the sample or corresponding text should include information about the output.</span></span>

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a><span data-ttu-id="1faa8-260">샘플을 실행하지 않고 예상 출력을 표시하는 시기</span><span class="sxs-lookup"><span data-stu-id="1faa8-260">When to display the expected output without running the sample</span></span>

- <span data-ttu-id="1faa8-261">초보자를 위한 문서는 readers가 작업의 출력을 예상된 답변과 비교할 수 있도록 출력을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-261">Articles intended for beginners should provide output so that readers can compare the output of their work with the expected answer.</span></span>
- <span data-ttu-id="1faa8-262">출력이 항목에 통합되어 있는 샘플에는 해당 출력이 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-262">Samples where the output is integral to the topic should display that output.</span></span> <span data-ttu-id="1faa8-263">예를 들어 서식이 지정된 텍스트의 문서는 샘플을 실행하지 않고 텍스트 서식을 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-263">For example, articles on formatted text should show the text format without running the sample.</span></span>
- <span data-ttu-id="1faa8-264">샘플 및 예상 출력이 모두 짧을 경우 출력을 표시하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-264">When both the sample and the expected output is short, consider showing the output.</span></span> <span data-ttu-id="1faa8-265">이는 약간의 시간을 절약합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-265">It saves a bit of time.</span></span>
- <span data-ttu-id="1faa8-266">현재 문화권 또는 고정 문화권이 출력에 어떤 영향을 미치는지 설명하는 문서는 예상되는 결과를 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-266">Articles explaining how current culture or invariant culture affect output should explain the expected output.</span></span> <span data-ttu-id="1faa8-267">대화형 REPL(Read Evaluate Print Loop)은 Linux 기반 호스트에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-267">The interactive REPL (Read Evaluate Print Loop) runs on a Linux-based host.</span></span> <span data-ttu-id="1faa8-268">기본 문화권 및 고정 문화권은 다른 운영 체제와 머신에서 서로 다른 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-268">The default culture, and the invariant culture produce different output on different operating systems and machines.</span></span> <span data-ttu-id="1faa8-269">이 문서에서는 Windows, Linux 및 Mac 시스템의 출력을 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-269">The article should explain the output in Windows, Linux, and Mac systems.</span></span>

### <a name="when-to-exclude-expected-output-from-the-sample"></a><span data-ttu-id="1faa8-270">예상 출력을 샘플에서 제외할 시기</span><span class="sxs-lookup"><span data-stu-id="1faa8-270">When to exclude expected output from the sample</span></span>

- <span data-ttu-id="1faa8-271">샘플이 더 큰 출력을 생성하는 문서에서는 주석에 이를 포함해서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-271">Articles where the sample generates a larger output should not include that in comments.</span></span> <span data-ttu-id="1faa8-272">샘플이 실행되면 코드가 숨겨집니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-272">It obscures the code once the sample has been run.</span></span>
- <span data-ttu-id="1faa8-273">샘플에서 항목을 설명하는 문서이지만 출력이 해당 항목을 이해하는 데 필수적인 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-273">Articles where the sample demonstrates a topic, but the output isn't integral to understanding it.</span></span> <span data-ttu-id="1faa8-274">예를 들어 쿼리 구문을 설명한 다음, 출력 컬렉션의 모든 항목을 표시하는 LINQ 쿼리를 실행하는 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-274">For example, code that runs a LINQ query to explain query syntax and then display every item in the output collection.</span></span>

> [!NOTE]
> <span data-ttu-id="1faa8-275">일부 항목은 현재 여기에 지정된 지침을 따르지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-275">You might notice that some of the topics are not currently following all the guidelines specified here.</span></span> <span data-ttu-id="1faa8-276">사이트 전반에 걸쳐 일관성을 유지하기 위해 노력하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-276">We're working towards achieving consistency throughout the site.</span></span> <span data-ttu-id="1faa8-277">특정 목적에 대해 현재 추적 중인 [미해결 문제](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) 목록을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-277">Check the list of [open issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) we're currently tracking for that specific goal.</span></span>

### <a name="contributing-to-international-content"></a><span data-ttu-id="1faa8-278">국가별 콘텐츠 기여</span><span class="sxs-lookup"><span data-stu-id="1faa8-278">Contributing to International content</span></span>

<span data-ttu-id="1faa8-279">MT(기계 번역) 콘텐츠에 대한 기여는 현재 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-279">Contributions for Machine Translated (MT) content are currently not accepted.</span></span> <span data-ttu-id="1faa8-280">MT 콘텐츠의 품질을 개선하기 위해 인공신경망 MT 엔진으로 전환되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-280">In an effort to improve the quality of MT content, we've transitioned to a Neural MT engine.</span></span> <span data-ttu-id="1faa8-281">인공신경망 MT 엔진을 학습시키는 데 사용되는 HT(사람이 한 번역) 콘텐츠에 대한 기여는 허용 및 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-281">We accept and encourage contributions for Human Translated (HT) content, which is used to train the Neural MT engine.</span></span> <span data-ttu-id="1faa8-282">따라서 시간을 두고 점차 HT 콘텐츠에 대한 기여가 HT 및 MT 모두의 품질을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-282">So over time, contributions to HT content will improve the quality of both HT and MT.</span></span> <span data-ttu-id="1faa8-283">MT 토픽에는 토픽의 일부가 MT일 수 있음을 나타내는 고지 사항이 있으며, 편집을 사용할 수 없으므로 **편집** 단추가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-283">MT topics will have a disclaimer stating that part of the topic may be MT, and the **Edit** button won't be displayed, as editing is disabled.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="1faa8-284">기여자 라이선스 계약</span><span class="sxs-lookup"><span data-stu-id="1faa8-284">Contributor license agreement</span></span>

<span data-ttu-id="1faa8-285">PR이 병합되기 전에 [.NET Foundation CLA(Contribution License Agreement)](https://cla.dotnetfoundation.org)에 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-285">You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged.</span></span> <span data-ttu-id="1faa8-286">이는 .NET Foundation의 프로젝트에 대한 일회성 요구 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-286">This is a one-time requirement for projects in the .NET Foundation.</span></span> <span data-ttu-id="1faa8-287">Wikipedia에서 [CLA(Contribution License Agreements)](http://en.wikipedia.org/wiki/Contributor_License_Agreement)에 대한 자세한 내용을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-287">You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.</span></span>

<span data-ttu-id="1faa8-288">계약: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span><span class="sxs-lookup"><span data-stu-id="1faa8-288">The agreement: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span></span>

<span data-ttu-id="1faa8-289">미리 계약서에 서명할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-289">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="1faa8-290">평소대로 PR을 복제, 포크 및 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-290">You can clone, fork, and submit your PR as usual.</span></span> <span data-ttu-id="1faa8-291">PR이 생성되면 CLA 봇에 의해 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-291">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="1faa8-292">변경 내용이 작은 경우(예:오타를 수정한 경우) PR에 `cla-not-required`로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-292">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="1faa8-293">그렇지 않으면 `cla-required`로 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-293">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="1faa8-294">CLA에 서명하면 현재 및 향후의 모든 끌어오기 요청은 `cla-signed`로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1faa8-294">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
