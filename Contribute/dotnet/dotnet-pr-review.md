---
title: .NET 문서 끌어오기 요청 검토 프로세스
description: .NET 문서의 경우 PR Merger 웹후크를 사용할 수 없습니다. 이 문서에서는 해당 리포지토리의 PR 프로세스에 대해 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/24/2020
ms.openlocfilehash: b2c0cbb0ed72948ba49a7456e16df5659057f5e6
ms.sourcegitcommit: 56505b3f7e670f6387d2c919f0326e9f4c571c8a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2020
ms.locfileid: "89201130"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a><span data-ttu-id="aa41e-104">.NET 문서 리포지토리에 대한 끌어오기 요청 검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="aa41e-104">Pull request review process for the .NET docs repositories</span></span>

<span data-ttu-id="aa41e-105">.NET 리포지토리를 비롯한 일부 리포지토리에는 부 PR을 자동으로 병합하는 “PR Merger” 웹후크가 사용하도록 설정되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-105">Some repositories, including the .NET repositories, don't have the "PR Merger" web hook enabled, which automatically merges minor PRs.</span></span> <span data-ttu-id="aa41e-106">이 문서에서는 해당 리포지토리의 PR 검토 프로세스에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-106">This article describes the PR review process for those repositories.</span></span> <span data-ttu-id="aa41e-107">PR 검토 프로세스는 다음과 같은 목표로 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-107">The PR review process was designed with these goals:</span></span>

- <span data-ttu-id="aa41e-108">팀, 제품 팀 구성원 및 커뮤니티 구성원의 고품질 콘텐츠를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-108">Publish high-quality content from our team, product team members, and community members.</span></span>
- <span data-ttu-id="aa41e-109">일관된 방식으로 적시에 조치 가능한 피드백을 작성자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-109">Provide timely, actionable feedback to authors in a consistent manner.</span></span>
- <span data-ttu-id="aa41e-110">작성자와 검토자 간의 토론을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-110">Facilitate discussion between authors and reviewers.</span></span>

<span data-ttu-id="aa41e-111">팀이 혁신하고 플랫폼이 성숙해짐에 따라 프로세스도 계속 발전합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-111">The processes continue to evolve as teams innovate and as the platform matures.</span></span>

## <a name="reviewers"></a><span data-ttu-id="aa41e-112">검토자</span><span class="sxs-lookup"><span data-stu-id="aa41e-112">Reviewers</span></span>

<span data-ttu-id="aa41e-113">콘텐츠 팀 구성원 중 한 명이 모든 PR을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-113">One of the content team members reviews every PR.</span></span> <span data-ttu-id="aa41e-114">콘텐츠 팀 구성원은 기술적 정확성을 확인하기 위해 특정 제품 팀 구성원의 검토를 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-114">Content team members may request a review from the specific product team members to verify technical accuracy.</span></span> <span data-ttu-id="aa41e-115">콘텐츠 팀은 GitHub의 코드 소유권 기능을 사용하여 콘텐츠 팀 구성원의 검토를 자동으로 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-115">The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members.</span></span> <span data-ttu-id="aa41e-116">이 프로세스의 일부로 검토자는 다른 팀 구성원에게 내부 PR을 검토하도록 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-116">As part of this process, a reviewer may tag other team members to review internal PRs.</span></span> <span data-ttu-id="aa41e-117">팀 구성원은 동일한 큐에 있는 팀 구성원과 커뮤니티 구성원의 요청된 검토를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-117">Team members see requested reviews from team members and community members in the same queue.</span></span>

<span data-ttu-id="aa41e-118">커뮤니티 구성원은 PR을 검토하고 피드백도 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-118">Community members can review PRs and provide feedback as well.</span></span> <span data-ttu-id="aa41e-119">그러나 최소한 핵심 콘텐츠 팀의 구성원 한 명이 PR을 승인해야 병합됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-119">However, at least one member of the core content team must approve any PR before it is merged.</span></span>

## <a name="review-process"></a><span data-ttu-id="aa41e-120">검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="aa41e-120">Review process</span></span>

<span data-ttu-id="aa41e-121">검토는 PR에 따라 다음 세 가지 경로 중 하나를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-121">Reviews follow one of the three paths based on the PR:</span></span>

- <span data-ttu-id="aa41e-122">**작은 PR** - 작은 PR은 오타, 끊어진 링크, 작은 코드 변경 또는 유사한 변경과 같은 단일 버그 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-122">**Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.</span></span>
- <span data-ttu-id="aa41e-123">**주요 기여** - 주요 기여는 기존 문서에 대한 상당한 편집, 새 문서 또는 여러 문서에 대한 편집입니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-123">**Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.</span></span>
- <span data-ttu-id="aa41e-124">**진행 중인 작업** - 작성자는 *초안* 끌어오기 요청을 열어 아직 검토할 준비가 되지 않은 것으로 표시된 PR을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-124">**Work in progress** - Authors can can create a PR that is marked as not ready for review yet by opening a *draft* pull request.</span></span>

<span data-ttu-id="aa41e-125">CLA(Contributor License Agreement) 봇에서 사용되는 처리가 “작은” 기여와 “큰” 기여의 구분에 대한 좋은 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-125">The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions.</span></span> <span data-ttu-id="aa41e-126">CLA의 서명이 필요하지 않은 PR은 “작은” PR일 가능성이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-126">PRs that do not require the CLA to be signed are likely "small."</span></span> <span data-ttu-id="aa41e-127">CLA가 필요한 PR은 “큰” PR일 가능성이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-127">PRs that do require the CLA are likely "large."</span></span>

### <a name="small-prs"></a><span data-ttu-id="aa41e-128">작은 PR</span><span class="sxs-lookup"><span data-stu-id="aa41e-128">Small PRs</span></span>

<span data-ttu-id="aa41e-129">작은 PR의 변경 내용은 정확성을 위해 검토되고 검토 사이트의 빌드를 사용하여 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-129">The changes in small PRs are reviewed for accuracy and checked using the build on the review site.</span></span> <span data-ttu-id="aa41e-130">이러한 PR은 작기 때문에 전체 문서의 검토를 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-130">Because they are small, these PRs do not trigger a review of the entire article.</span></span> 

<span data-ttu-id="aa41e-131">검토자가 문서를 개선하는 다른 작은 변경 내용을 발견할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-131">Reviewers may notice other small changes that would improve an article.</span></span> <span data-ttu-id="aa41e-132">이러한 변경 내용도 작은 경우에는 검토 주석으로 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-132">If those changes are also small, suggest them as review comments.</span></span> <span data-ttu-id="aa41e-133">제안한 변경 내용이 더 큰 검토를 트리거하는 경우 문제를 열고 나중에 이러한 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-133">If the suggested changes would trigger a larger review, open an issue and address those later.</span></span> 

### <a name="larger-changes"></a><span data-ttu-id="aa41e-134">더 큰 변경 내용</span><span class="sxs-lookup"><span data-stu-id="aa41e-134">Larger changes</span></span>

<span data-ttu-id="aa41e-135">PR이 클수록 보다 철저한 검토를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-135">Larger PRs undergo a more thorough review.</span></span> <span data-ttu-id="aa41e-136">다음 사항이 모두 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-136">The following are all checked:</span></span>

- <span data-ttu-id="aa41e-137">샘플 코드가 PR에 소스 및 다운로드 가능한 zip 파일로 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-137">Sample code must be included in the PR, in source and as a downloadable zip file.</span></span>
- <span data-ttu-id="aa41e-138">샘플 코드가 올바르게 컴파일되고 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-138">Sample code compiles and runs correctly.</span></span>
- <span data-ttu-id="aa41e-139">문서에서 독자를 위한 목표를 명확하게 설명하고 해당 목표가 충족되었습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-139">The article clearly describes the goals for the reader, and those goals are met.</span></span>
- <span data-ttu-id="aa41e-140">이 문서는 [스타일 및 문법 지침](dotnet-style-guide.md)을 충족하고 [음성 및 어조 원칙](dotnet-voice-tone.md)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-140">The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).</span></span>
- <span data-ttu-id="aa41e-141">모든 링크가 올바르게 확인되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-141">All links should resolve correctly.</span></span>

<span data-ttu-id="aa41e-142">콘텐츠 팀 구성원이 PR을 검토하고 주석과 함께 검토를 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-142">Content team members will review the PR and submit the review with comments.</span></span> <span data-ttu-id="aa41e-143">사소한 변경만 요청되는 경우 팀 구성원이 피드백을 사용하여 PR을 “승인”할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-143">If only minor changes are requested, team members may "approve" the PR with the feedback.</span></span> <span data-ttu-id="aa41e-144">그러면 작성자가 피드백을 처리하고 PR을 병합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-144">The author can then address the feedback and merge the PR.</span></span> <span data-ttu-id="aa41e-145">대부분의 검토는 변경을 요청하고, 이러한 변경이 완료되면 검토자가 다시 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-145">Most reviews will request changes and when those changes are made, the reviewer will review again.</span></span>

<span data-ttu-id="aa41e-146">편집에 기술적 검토가 필요한 경우 콘텐츠 팀 검토자가 해당 제품 팀 구성원의 검토를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-146">If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.</span></span>

### <a name="review-draft-pull-requests"></a><span data-ttu-id="aa41e-147">초안 끌어오기 요청 검토</span><span class="sxs-lookup"><span data-stu-id="aa41e-147">Review draft pull requests</span></span>

<span data-ttu-id="aa41e-148">프로세스의 초기 단계에서 피드백을 원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-148">You may want feedback earlier in the process.</span></span> <span data-ttu-id="aa41e-149">초안 PR을 열고 초기 검토를 요청하는 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-149">Open a draft PR and add a comment that requests an early review.</span></span> <span data-ttu-id="aa41e-150">이러한 초기 검토는 개요, 전체 콘텐츠, 샘플 등의 문서 구조를 중점적으로 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-150">These early reviews focus on the structure of the article: the outline, the overall content, and the samples.</span></span> <span data-ttu-id="aa41e-151">문법 및 올바른 링크에 대한 철저한 검사는 이러한 검토에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-151">These reviews do not include a thorough check for grammar and correct links.</span></span>

## <a name="explain-suggestions"></a><span data-ttu-id="aa41e-152">제안 사항 설명</span><span class="sxs-lookup"><span data-stu-id="aa41e-152">Explain suggestions</span></span>

<span data-ttu-id="aa41e-153">GitHub를 사용하여 diff로 표시되고 단추를 클릭하여 병합할 수 있는 `suggestion` 형식의 삼중 역따옴표(\`) 블록에 주석을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-153">GitHub lets you enter comments in triple-back-tick blocks of type `suggestion` that are displayed as a diff and can be merged by clicking a button.</span></span> <span data-ttu-id="aa41e-154">짧은 줄에서 GitHub는 변경 내용의 강조 표시를 잘 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-154">On short lines, GitHub does a good job of highlighting the changes.</span></span> <span data-ttu-id="aa41e-155">긴 줄에서(예: 텍스트 한 줄로 작성된 긴 단락) GitHub는 변경 내용을 강조 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-155">On longer lines, such as a long paragraph in one line of text, GitHub doesn't highlight the changes.</span></span> <span data-ttu-id="aa41e-156">긴 줄에 대한 제안 사항을 입력할 때 변경 내용이 명확하게 강조 표시되는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="aa41e-156">When entering a suggestion for a long line, notice whether your changes are clearly highlighted.</span></span> <span data-ttu-id="aa41e-157">변경 내용이 강조 표시되지 않으면 제안 블록 외부에 변경 내용을 설명하는 주석을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-157">If the changes aren't highlighted, include comments outside the suggestion block explaining what you changed.</span></span> <span data-ttu-id="aa41e-158">설명이 없으면 이후 검토자 또는 PR 작성자가 변경 내용을 파악하는 데 긴 시간이 소요되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-158">Without an explanation it's often time-consuming for subsequent reviewers or the PR author to figure out what the changes are.</span></span>

## <a name="respond-to-reviews"></a><span data-ttu-id="aa41e-159">검토에 응답</span><span class="sxs-lookup"><span data-stu-id="aa41e-159">Respond to reviews</span></span>

<span data-ttu-id="aa41e-160">작성자는 PR을 업데이트하여 주석에 응답하고, 처리된 각 주석을 “+1” 반응으로 표시하여 처리되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-160">The author updates the PR to respond to comments and marks each addressed comment with the "+1" reaction to indicate it was addressed.</span></span> <span data-ttu-id="aa41e-161">작성자가 주석에 동의하지 않거나 다른 PR의 주석을 처리하는 경우 변경 내용을 설명하는 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-161">If the author disagrees with the comment, or addresses the comment in a different PR, the author adds a comment explaining their change.</span></span>

<span data-ttu-id="aa41e-162">작성자는 주석에서 원래 검토자를 @-mentions하여 새 검토를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-162">The author @-mentions the original reviewer in a comment to request a new review.</span></span> 

## <a name="response-time-expectations"></a><span data-ttu-id="aa41e-163">예상 응답 시간</span><span class="sxs-lookup"><span data-stu-id="aa41e-163">Response time expectations</span></span>

<span data-ttu-id="aa41e-164">일반적으로 업무일 기준으로 2일 이내에 콘텐츠 팀 구성원이 새 PR을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-164">Content team members will typically review new PRs in under two business days.</span></span> <span data-ttu-id="aa41e-165">검토 시간이 더 오래 걸리면, 팀 구성원 중 한 명이 주석을 추가하여 PR을 인정하고 예상 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-165">If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.</span></span>

<span data-ttu-id="aa41e-166">작성자는 검토가 제출된 후 1주 이내에 주석에 응답해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-166">Once a review has been submitted, authors should try to respond to comments in a week or less.</span></span> <span data-ttu-id="aa41e-167">다른 약정으로 인해 지원자가 이러한 예상 시간을 지키지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-167">Volunteers may not be able to meet these expectations because of other commitments.</span></span> <span data-ttu-id="aa41e-168">이 경우 팀 구성원이 커뮤니티 작성자에게 PR을 업데이트할 것인지 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-168">In those cases, team members ask if the community author will update the PR.</span></span> <span data-ttu-id="aa41e-169">아닌 경우 팀 구성원이 대신 PR을 업데이트하고 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="aa41e-169">If not, the team member updates and merges the PR for them.</span></span>
