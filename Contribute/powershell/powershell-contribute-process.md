---
title: PowerShell 문서 리포지토리에 대한 기여 프로세스
description: 이 문서에서는 PowerShell 문서 리포지토리에 기여에 대한 간략한 소개를 제공합니다. 사용된 리포지토리, 콘텐츠를 구성하는 프로세스, 코드 샘플 및 기타 자산을 관리하기 위한 정책을 알아봅니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290199"
---
# <a name="process-for-contributing-to-powershell-docs"></a><span data-ttu-id="49666-104">PowerShell 문서에 기여하는 프로세스</span><span class="sxs-lookup"><span data-stu-id="49666-104">Process for contributing to PowerShell docs</span></span>

<span data-ttu-id="49666-105">문서에 대한 커뮤니티 기여에 감사드립니다. 다음 목록에서는 PowerShell 문서에 기여할 때 주의해야 할 몇 가지 지침 규칙을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49666-105">We appreciate community contributions to docs. The following list shows some guiding rules that you should keep in mind when you're contributing to the PowerShell documentation:</span></span>

- <span data-ttu-id="49666-106">많은 끌어오기 요청으로 놀라게 **하지 마세요**.</span><span class="sxs-lookup"><span data-stu-id="49666-106">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="49666-107">대신, 많은 시간을 투자하기 전에 문제를 제기하고 토론을 시작하여 하나의 방향에 동의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-107">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="49666-108">**DO**는 이 지침과 [코드](powershell-style-code.md) 및 [참조](powershell-style-reference.md) 스타일 가이드를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="49666-108">**DO** follow these instructions and the [code](powershell-style-code.md) and [reference](powershell-style-reference.md) style guides..</span></span>
- <span data-ttu-id="49666-109">**DO**는 [템플릿](powershell-style-basic-markdown.md) 파일을 작업의 시작점으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-109">**DO** use the [template](powershell-style-basic-markdown.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="49666-110">**DO**는 문서를 작업하기 전에 포크에 별도의 분기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49666-110">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="49666-111">**DO**는 [GitHub Flow 워크플로](../how-to-write-workflows-major.md)를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="49666-111">**DO** follow the [GitHub Flow workflow](../how-to-write-workflows-major.md).</span></span>
- <span data-ttu-id="49666-112">**DO**에서 참여에 대해 자주 블로그 및 트윗(또는 기타)을 하세요.</span><span class="sxs-lookup"><span data-stu-id="49666-112">**DO** blog and tweet (or whatever) about your contributions, frequently!</span></span>

<span data-ttu-id="49666-113">이 지침을 따르면 모두에게 더 나은 환경이 조성됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-113">Following these guidelines ensures a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-powershell-docs"></a><span data-ttu-id="49666-114">PowerShell 문서에 기여하기</span><span class="sxs-lookup"><span data-stu-id="49666-114">Make a contribution to PowerShell docs</span></span>

<span data-ttu-id="49666-115">기존 [이슈](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose) 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-115">You can choose from existing [issues](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).</span></span>
<span data-ttu-id="49666-116">관심사와 책임 수준에 따라 작업이 다음 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-116">Depending on your interests and level of commitment, the efforts fall into the following categories:</span></span>

- <span data-ttu-id="49666-117">**작은 변경 내용**.</span><span class="sxs-lookup"><span data-stu-id="49666-117">**Small changes**.</span></span> <span data-ttu-id="49666-118">작은 변경 내용은 기여자 가이드의 [홈 페이지](../index.md#quick-edits-to-existing-documents)에서 GitHub의 편집 지침을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49666-118">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span> <span data-ttu-id="49666-119">작은 변경 내용에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-119">Small changes include:</span></span>

  - <span data-ttu-id="49666-120">오타 및 맞춤법 오류 수정</span><span class="sxs-lookup"><span data-stu-id="49666-120">Fixing typos and spelling errors</span></span>
  - <span data-ttu-id="49666-121">문법 또는 서식 지정 개선</span><span class="sxs-lookup"><span data-stu-id="49666-121">Improving grammar or formatting</span></span>
  - <span data-ttu-id="49666-122">사소한 기술 또는 팩트 편집</span><span class="sxs-lookup"><span data-stu-id="49666-122">Minor technical or factual edits</span></span>

- <span data-ttu-id="49666-123">**유지 관리**.</span><span class="sxs-lookup"><span data-stu-id="49666-123">**Maintenance**.</span></span> <span data-ttu-id="49666-124">이 범주에는 끊어진 링크 또는 잘못된 링크 수정, 누락된 코드 예제 추가 또는 제한된 콘텐츠 문제 해결과 같은 매우 간단한 기여가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-124">This category includes fairly simple contributions, such as fixing broken or incorrect links, adding missing code examples, or addressing limited content issues.</span></span> <span data-ttu-id="49666-125">경우에 따라 이러한 문제는 많은 수의 파일과 관련될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-125">In some cases, these issues may concern large numbers of files.</span></span> <span data-ttu-id="49666-126">이 경우 시작하기 전에 어떤 작업을 수행하는지 알려주세요.</span><span class="sxs-lookup"><span data-stu-id="49666-126">In that case, you should let us know what you'd like to work on before you begin.</span></span> <span data-ttu-id="49666-127">문제에 대한 주석을 추가하여 작업 진행 중임을 알려주세요.</span><span class="sxs-lookup"><span data-stu-id="49666-127">Add a comment on the issue to tell us that you are working on it.</span></span>

- <span data-ttu-id="49666-128">**콘텐츠 업데이트**.</span><span class="sxs-lookup"><span data-stu-id="49666-128">**Content updates**.</span></span> <span data-ttu-id="49666-129">문서 집합의 엄청난 양을 감안할 때 콘텐츠는 쉽게 구식이 되어 개정이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-129">Given the enormity of the doc set, content easily becomes outdated and requires revision.</span></span> <span data-ttu-id="49666-130">또한 여러 가지 이유로 인해 일부 콘텐츠가 중복되거나 심지어 삼중으로 복제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-130">In addition, for a variety of reason, some content has been duplicated or even triplicated.</span></span> <span data-ttu-id="49666-131">콘텐츠를 업데이트하려면 개별 항목이 최신인지 확인하거나 기능 영역의 콘텐츠를 수정하여 중복을 제거하고 모든 고유한 콘텐츠를 더 작은 문서 집합에 보존해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-131">Updating content involves making sure that individual topics are current or revising content in a feature area to eliminate duplication and ensure that all unique content is preserved in the smaller documentation set.</span></span>

- <span data-ttu-id="49666-132">**새 콘텐츠 작성**.</span><span class="sxs-lookup"><span data-stu-id="49666-132">**New content authoring**.</span></span> <span data-ttu-id="49666-133">고유의 항목을 작성하는 데 관심이 있는 경우 이러한 문제에는 문서 집합에 추가하려는 항목이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-133">If you're interested in authoring your own topic, these issues list topics that we know we'd like to add to our doc set.</span></span> <span data-ttu-id="49666-134">하지만 항목에 대한 작업을 시작하기 전에 알려주세요.</span><span class="sxs-lookup"><span data-stu-id="49666-134">Let us know before you begin working on a topic, though.</span></span> <span data-ttu-id="49666-135">여기에 나열되지 않은 항목을 작성하는 데 관심이 있다면 문제를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="49666-135">If you're interested in writing a topic that isn't listed here, open an issue.</span></span>

<span data-ttu-id="49666-136">수행할 작업을 선택한 후 [시작하기](../get-started-setup-github.md) 가이드에 따라 GitHub 계정을 만들고 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-136">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and setup your environment.</span></span>

### <a name="making-large-changes"></a><span data-ttu-id="49666-137">크게 변경</span><span class="sxs-lookup"><span data-stu-id="49666-137">Making large changes</span></span>

<span data-ttu-id="49666-138">**1단계:** 새 콘텐츠를 작성하거나 기존 콘텐츠를 완전히 개정하려는 경우 수행할 작업을 설명하는 이슈를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="49666-138">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an issue describing what you want to do.</span></span>

<span data-ttu-id="49666-139">**2단계:** `MicrosoftDocs/PowerShell-Docs` 리포지토리를 포크하고 변경 내용에 대한 작업 분기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49666-139">**Step 2:** Fork the `MicrosoftDocs/PowerShell-Docs` repository and create a working branch for your changes.</span></span>

<span data-ttu-id="49666-140">**3단계:** 이 새로운 분기를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-140">**Step 3:** Make the changes in this new branch.</span></span>

<span data-ttu-id="49666-141">새 항목인 경우 이 [스타일 가이드](powershell-style-basic-markdown.md)의 템플릿을 시작점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-141">If it's a new topic, use the template in the [style guide](powershell-style-basic-markdown.md) as your starting point.</span></span> <span data-ttu-id="49666-142">스타일 가이드는 작성 지침을 포함하며 각 문서에 필요한 메타데이터도 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-142">The style guide contains the writing guidelines and explains the metadata required for each article.</span></span>

<span data-ttu-id="49666-143">1단계에서 문서에 대해 결정된 TOC 위치에 해당하는 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-143">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span>
<span data-ttu-id="49666-144">이 폴더에는 해당 섹션의 모든 문서에 대한 Markdown 파일이 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-144">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="49666-145">필요한 경우 콘텐츠용 파일을 배치할 새 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49666-145">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="49666-146">해당 섹션의 주요 문서는 *index.md*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-146">The main article for that section is called *index.md*.</span></span>
<span data-ttu-id="49666-147">이미지 및 기타 정적 리소스의 경우 문서를 포함하는 폴더 내에 **미디어**라는 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49666-147">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="49666-148">**미디어** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다(인덱스 파일 제외).</span><span class="sxs-lookup"><span data-stu-id="49666-148">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="49666-149">올바른 Markdown 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="49666-149">Be sure to follow the proper Markdown syntax.</span></span> <span data-ttu-id="49666-150">자세한 지침 및 예제는 [스타일 가이드](powershell-style-basic-markdown.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49666-150">Please read the [style guide](powershell-style-basic-markdown.md) for detailed instructions and examples.</span></span>

<span data-ttu-id="49666-151">**예제 구조**</span><span class="sxs-lookup"><span data-stu-id="49666-151">**Example structure**</span></span>

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

<span data-ttu-id="49666-152">**4단계:** 작업 분기에서 ‘스테이징’ 분기로 PR(끌어오기 요청)을 제출합니다. </span><span class="sxs-lookup"><span data-stu-id="49666-152">**Step 4:** Submit a Pull Request (PR) from your working branch to the *staging* branch.</span></span>

<span data-ttu-id="49666-153">일반적으로 PR은 한 번에 하나의 이슈를 해결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-153">Normally, a PR should address one issue at a time.</span></span> <span data-ttu-id="49666-154">PR은 하나 또는 여러 개의 파일을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-154">The PR can modify one or multiple files.</span></span> <span data-ttu-id="49666-155">다른 파일의 여러 수정 사항을 해결하는 경우 PR을 별도로 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-155">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span>

<span data-ttu-id="49666-156">PR에서 기존 이슈를 해결하는 경우 커밋 메시지 또는 PR 설명에 `Fixes #Issue_Number` 키워드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-156">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="49666-157">이렇게 하면 PR이 병합될 때 이 이슈가 자동으로 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="49666-157">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="49666-158">자세한 내용은 [커밋 메시지를 통해 이슈 닫기](https://help.github.com/articles/closing-issues-via-commit-messages/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49666-158">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="49666-159">PowerShell 팀은 PR을 검토하고 승인을 위해 필요한 다른 변경 내용이 있는지 알려 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49666-159">The PowerShell team reviews your PR and lets you know if there are any other changes necessary in order to approve it.</span></span>

<span data-ttu-id="49666-160">**5단계:** 팀과 논의한 대로 분기에 필요한 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-160">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="49666-161">PR이 승인되면 유지 관리자는 PR을 ‘스테이징’ 분기에 병합합니다. </span><span class="sxs-lookup"><span data-stu-id="49666-161">Once the PR is approved, the maintainers merge your PR into the *staging* branch.</span></span> <span data-ttu-id="49666-162">주기적으로 ‘스테이징’ 분기의 모든 커밋을 ‘라이브’ 분기로 푸시합니다.  </span><span class="sxs-lookup"><span data-stu-id="49666-162">We periodically push all commits from *staging* branch into the *live* branch.</span></span> <span data-ttu-id="49666-163">기여가 라이브 상태이면 [PowerShell 문서 사이트](https://docs.microsoft.com/PowerShell/)에서 해당 기여를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-163">Once your contribution is live, you can see it in the [PowerShell docs site](https://docs.microsoft.com/PowerShell/).</span></span> <span data-ttu-id="49666-164">일반적으로 업무 주간 동안 2~3회 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-164">Typically, we publish a two to three times during the work week.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="49666-165">기여자 라이선스 계약</span><span class="sxs-lookup"><span data-stu-id="49666-165">Contributor license agreement</span></span>

<span data-ttu-id="49666-166">PR이 병합되기 전에 [CLA(Contribution License Agreement)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs)에 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49666-166">You must sign the [Contribution License Agreement (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) before your PR is merged.</span></span> <span data-ttu-id="49666-167">이는 문서에 기여하는 경우 일회성 요구 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="49666-167">This is a one-time requirement when contributing to our documentation.</span></span>

<span data-ttu-id="49666-168">미리 계약서에 서명할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-168">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="49666-169">평소대로 PR을 복제, 포크 및 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49666-169">You can clone, fork, and submit your PR as usual.</span></span>
<span data-ttu-id="49666-170">PR이 생성되면 CLA 봇에 의해 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-170">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="49666-171">변경 내용이 작은 경우(예:오타를 수정한 경우) PR에 `cla-not-required`로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-171">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="49666-172">그렇지 않으면 `cla-required`로 분류됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-172">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="49666-173">CLA에 서명하면 현재 및 향후의 모든 끌어오기 요청은 `cla-signed`로 레이블이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="49666-173">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
