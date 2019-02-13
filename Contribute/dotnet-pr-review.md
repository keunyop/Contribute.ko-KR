---
title: .NET 문서 끌어오기 요청 검토 프로세스
description: .NET 문서의 경우 PR Merger 웹후크를 사용할 수 없습니다. 이 문서에서는 해당 리포지토리의 PR 프로세스에 대해 설명합니다.
ms.date: 01/-4/2019
ms.openlocfilehash: d8f35e328beffcbd5bac9f0f7313d8127fbeffb0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713571"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a><span data-ttu-id="6a593-104">.NET 문서 리포지토리에 대한 끌어오기 요청 검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="6a593-104">Pull request review process for the .NET docs repositories</span></span>

<span data-ttu-id="6a593-105">PR Merger 웹후크를 사용할 수 없는 리포지토리가 많아서 부 PR이 자동으로 병합됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-105">Many repositories don't have PR Merger webhooks enabled, which automatically merges minor PRs.</span></span> <span data-ttu-id="6a593-106">이 문서에서는 해당 리포지토리의 PR 검토 프로세스에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-106">This article describes the PR review process for those repositories.</span></span> <span data-ttu-id="6a593-107">PR 검토 프로세스는 다음과 같은 목표로 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-107">The PR review process was designed with these goals:</span></span>

1. <span data-ttu-id="6a593-108">팀, 제품 팀 구성원 및 커뮤니티 구성원의 고품질 콘텐츠를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-108">Publish high-quality content from our team, product team members, and community members.</span></span>
1. <span data-ttu-id="6a593-109">일관된 방식으로 적시에 조치 가능한 피드백을 작성자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-109">Provide timely, actionable feedback to authors in a consistent manner.</span></span>
1. <span data-ttu-id="6a593-110">작성자와 검토자 간의 토론을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-110">Facilitate discussion between authors and reviewers.</span></span>

<span data-ttu-id="6a593-111">팀이 혁신되고 플랫폼이 성숙해짐에 따라 프로세스도 계속 발전합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-111">The processes continue to evolve as teams innovate, and as the platform matures.</span></span>

## <a name="reviewers"></a><span data-ttu-id="6a593-112">검토자</span><span class="sxs-lookup"><span data-stu-id="6a593-112">Reviewers</span></span>

<span data-ttu-id="6a593-113">콘텐츠 팀 구성원 중 한 명이 모든 PR을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-113">One of the content team members reviews every PR.</span></span> <span data-ttu-id="6a593-114">콘텐츠 팀 구성원은 기술적 정확성을 확인하기 위해 특정 제품 팀 구성원의 검토를 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-114">Content team members may request a review from the specific product team members to verify technical accuracy.</span></span> <span data-ttu-id="6a593-115">콘텐츠 팀은 GitHub의 코드 소유권 기능을 사용하여 콘텐츠 팀 구성원의 검토를 자동으로 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-115">The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members.</span></span> <span data-ttu-id="6a593-116">이 프로세스의 일부로 검토자는 다른 팀 구성원에게 내부 PR을 검토하도록 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-116">As part of this process, a reviewer may tag other team members to review internal PRs.</span></span> <span data-ttu-id="6a593-117">팀 구성원은 동일한 큐에 있는 팀 구성원과 커뮤니티 구성원의 요청된 검토를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-117">Team members see requested reviews from team members and community members in the same queue.</span></span>

<span data-ttu-id="6a593-118">커뮤니티 구성원은 PR을 검토하고 피드백도 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-118">Community members can review PRs and provide feedback as well.</span></span> <span data-ttu-id="6a593-119">그러나 최소한 핵심 콘텐츠 팀의 구성원 한 명이 PR을 승인해야 병합됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-119">However, at least one member of the core content team must approve any PR before it is merged.</span></span>

## <a name="review-process"></a><span data-ttu-id="6a593-120">검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="6a593-120">Review process</span></span>

<span data-ttu-id="6a593-121">검토는 PR에 따라 다음 세 가지 경로 중 하나를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-121">Reviews follow one of the three paths based on the PR:</span></span>

- <span data-ttu-id="6a593-122">**작은 PR** - 작은 PR은 오타, 끊어진 링크, 작은 코드 변경 또는 유사한 변경과 같은 단일 버그 수정입니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-122">**Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.</span></span>
- <span data-ttu-id="6a593-123">**주요 기여** - 주요 기여는 기존 문서에 대한 상당한 편집, 새 문서 또는 여러 문서에 대한 편집입니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-123">**Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.</span></span>
- <span data-ttu-id="6a593-124">**진행 중인 작업** - 작성자는 제목에 “[WIP]” 태그를 포함해서 PR을 열어 진행 중인 작업 검토를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-124">**Work in progress** - Authors can request an in-progress review by opening a PR with the "[WIP]" tag in the title.</span></span> <span data-ttu-id="6a593-125">“WIP” 태그는 “진행 중인 작업”을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-125">The "WIP" tag stands for "Work in Progress."</span></span> 

<span data-ttu-id="6a593-126">CLA(Contributor License Agreement) 봇에서 사용되는 처리가 “작은” 기여와 “큰” 기여의 구분에 대한 좋은 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-126">The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions.</span></span> <span data-ttu-id="6a593-127">CLA의 서명이 필요하지 않은 PR은 “작은” PR일 가능성이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-127">PRs that do not require the CLA to be signed are likely "small."</span></span> <span data-ttu-id="6a593-128">CLA가 필요한 PR은 “큰” PR일 가능성이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-128">PRs that do require the CLA are likely "large."</span></span>

### <a name="small-prs"></a><span data-ttu-id="6a593-129">작은 PR</span><span class="sxs-lookup"><span data-stu-id="6a593-129">Small PRs</span></span>

<span data-ttu-id="6a593-130">작은 PR의 변경 내용은 정확성을 위해 검토되고 검토 사이트의 빌드를 사용하여 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-130">The changes in small PRs are reviewed for accuracy, and checked using the build on the review site.</span></span> <span data-ttu-id="6a593-131">이러한 PR은 작기 때문에 전체 문서의 검토를 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-131">Because they are small, these PRs do not trigger a review of the entire article.</span></span> 

<span data-ttu-id="6a593-132">검토자가 문서를 개선하는 다른 작은 변경 내용을 발견할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-132">Reviewers may notice other small changes that would improve an article.</span></span> <span data-ttu-id="6a593-133">이러한 변경 내용도 작은 경우에는 검토 주석으로 제안합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-133">If those changes are also small, suggest them as review comments.</span></span> <span data-ttu-id="6a593-134">제안한 변경 내용이 더 큰 검토를 트리거하는 경우 문제를 열고 나중에 이러한 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-134">If the suggested changes would trigger a larger review, open an issue and address those later.</span></span> 

### <a name="larger-changes"></a><span data-ttu-id="6a593-135">더 큰 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6a593-135">Larger changes</span></span>

<span data-ttu-id="6a593-136">PR이 클수록 보다 철저한 검토를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-136">Larger PRs undergo a more thorough review.</span></span> <span data-ttu-id="6a593-137">다음 사항이 모두 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-137">The following are all checked:</span></span>

- <span data-ttu-id="6a593-138">샘플 코드가 PR에 소스 및 다운로드 가능한 zip 파일로 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-138">Sample code must be included in the PR, in source and as a downloadable zip file.</span></span>
- <span data-ttu-id="6a593-139">샘플 코드가 올바르게 컴파일되고 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-139">Sample code compiles and runs correctly.</span></span>
- <span data-ttu-id="6a593-140">문서에서 독자를 위한 목표를 명확하게 설명하고 해당 목표가 충족되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-140">The article clearly describes the goals for the reader, and those goals are met.</span></span>
- <span data-ttu-id="6a593-141">이 문서는 [스타일 및 문법 지침](dotnet-style-guide.md)을 충족하고 [음성 및 어조 원칙](dotnet-voice-tone.md)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-141">The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).</span></span>
- <span data-ttu-id="6a593-142">모든 링크가 올바르게 확인되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-142">All links should resolve correctly.</span></span>

<span data-ttu-id="6a593-143">콘텐츠 팀 구성원이 PR을 검토하고 주석과 함께 검토를 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-143">Content team members will review the PR, and submit the review with comments.</span></span> <span data-ttu-id="6a593-144">사소한 변경만 요청되는 경우 팀 구성원이 피드백을 사용하여 PR을 “승인”할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-144">If only minor changes are requested, team members may "approve" the PR with the feedback.</span></span> <span data-ttu-id="6a593-145">그러면 작성자가 피드백을 처리하고 PR을 병합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-145">The author can then address the feedback and merge the PR.</span></span> <span data-ttu-id="6a593-146">대부분의 검토는 변경을 요청하고, 이러한 변경이 완료되면 검토자가 다시 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-146">Most reviews will request changes and when those changes are made, the reviewer will review again.</span></span>

<span data-ttu-id="6a593-147">편집에 기술적 검토가 필요한 경우 콘텐츠 팀 검토자가 해당 제품 팀 구성원의 검토를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-147">If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.</span></span>

### <a name="review-wip-pull-requests"></a><span data-ttu-id="6a593-148">“WIP” 끌어오기 요청 검토</span><span class="sxs-lookup"><span data-stu-id="6a593-148">Review "WIP" pull requests</span></span>

<span data-ttu-id="6a593-149">새 작성자가 프로세스의 초기 단계에서 피드백을 원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-149">New authors may want feedback earlier in the process.</span></span> <span data-ttu-id="6a593-150">이 경우 제목에 “[WIP]” 레이블을 추가하여 PR을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-150">They can open a PR adding the "[WIP]" label to the title.</span></span> <span data-ttu-id="6a593-151">주석에서 초기 검토를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-151">In a comment, they can request an early review.</span></span>

<span data-ttu-id="6a593-152">이러한 초기 검토는 전체 PR 검토만큼 철저하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-152">These early reviews are not as thorough as a full PR review.</span></span> <span data-ttu-id="6a593-153">콘텐츠 팀이 주석을 추가하지만 GitHub의 검토 기능을 사용하여 변경을 “승인” 또는 “요청”하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-153">The content team will comment, but will not "approve" or "request changes" using GitHub's review feature.</span></span> <span data-ttu-id="6a593-154">이러한 초기 검토는 개요, 전체 콘텐츠, 샘플 등의 문서 구조를 중점적으로 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-154">These early reviews focus on the structure of the article: the outline, the overall content, and the samples.</span></span> <span data-ttu-id="6a593-155">문법 및 올바른 링크에 대한 철저한 검사는 이러한 검토에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-155">These reviews do not include a thorough check for grammar and correct links.</span></span>

## <a name="respond-to-reviews"></a><span data-ttu-id="6a593-156">검토에 응답</span><span class="sxs-lookup"><span data-stu-id="6a593-156">Respond to reviews</span></span>

<span data-ttu-id="6a593-157">작성자는 PR을 업데이트하여 주석에 응답하고, 처리된 각 주석을 “+1” 반응으로 표시하여 처리되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-157">The author updates the PR to respond to comments marking each addressed comment with the "+1" reaction to indicate it was addressed.</span></span> <span data-ttu-id="6a593-158">작성자가 주석에 동의하지 않거나 주석을 다르게 처리하는 경우 변경 내용을 설명하는 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-158">If the author disagrees with the comment, or addresses the comment in a different, the author adds a comment explaining their change.</span></span>

<span data-ttu-id="6a593-159">작성자는 주석에서 원래 검토자를 @-mentions하여 새 검토를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-159">The author @-mentions the original reviewer in a comment to request a new review.</span></span> 

## <a name="response-time-expectations"></a><span data-ttu-id="6a593-160">예상 응답 시간</span><span class="sxs-lookup"><span data-stu-id="6a593-160">Response time expectations</span></span>

<span data-ttu-id="6a593-161">일반적으로 업무일 기준으로 2일 이내에 콘텐츠 팀 구성원이 새 PR을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-161">Content team members will typically review new PRs in under two business days.</span></span> <span data-ttu-id="6a593-162">검토 시간이 더 오래 걸리면, 팀 구성원 중 한 명이 주석을 추가하여 PR을 인정하고 예상 시간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-162">If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.</span></span>

<span data-ttu-id="6a593-163">작성자는 검토가 제출된 후 1주 이내에 주석에 응답해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-163">Once a review has been submitted, authors should try to respond to comments in a week or less.</span></span> <span data-ttu-id="6a593-164">다른 약정으로 인해 지원자가 이러한 예상 시간을 지키지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-164">Volunteers may not be able to meet these expectations because of other commitments.</span></span> <span data-ttu-id="6a593-165">이 경우 팀 구성원이 커뮤니티 작성자에게 PR을 업데이트할 것인지 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-165">In those cases, team members ask if the community author will update the PR.</span></span> <span data-ttu-id="6a593-166">아닌 경우 팀 구성원이 대신 PR을 업데이트하고 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="6a593-166">If not, the team member updates and merges the PR for them.</span></span>
