---
title: 중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로
description: 이 문서에서는 "중요한" 기여자 워크플로를 사용하여 docs.microsoft.com 문서에 참여하는 방법을 보여 줍니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 997f313e94e4858f37501736c1ec0be2fa8fd552
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188250"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a><span data-ttu-id="af481-103">중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로</span><span class="sxs-lookup"><span data-stu-id="af481-103">GitHub contribution workflow for major or long-running changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af481-104">docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 채택했습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="af481-105">자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="af481-106">또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="af481-107">공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="af481-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="af481-108">변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="af481-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="af481-109">끌어오기 요청을 병합하기 전에 온라인 양식을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-109">You will need to complete the online form before your pull request can be merged.</span></span>

## <a name="overview"></a><span data-ttu-id="af481-110">개요</span><span class="sxs-lookup"><span data-stu-id="af481-110">Overview</span></span>

<span data-ttu-id="af481-111">이 워크플로는 주요 변경 내용을 적용해야 하거나 리포지토리에 자주 참여할 참여자에게 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-111">This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository.</span></span> <span data-ttu-id="af481-112">자주 참여하는 사용자에게는 일반적으로 진행 중인(장기 실행) 변경 내용이 있습니다. 이 작업은 끌어오기 요청이 승인 및 병합되기 전에 여러 빌드/유효성 검사/스테이징 주기를 거치거나 여러 날에 걸쳐 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="af481-112">Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.</span></span>

<span data-ttu-id="af481-113">이러한 참여의 예제는 다음을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-113">Examples of these types of contributions include:</span></span>

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a><span data-ttu-id="af481-114">용어</span><span class="sxs-lookup"><span data-stu-id="af481-114">Terminology</span></span>

<span data-ttu-id="af481-115">시작하기 전에 이 워크플로에서 사용되는 Git/GitHub 용어 및 monikers의 일부를 검토하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-115">Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow.</span></span> <span data-ttu-id="af481-116">이 내용을 이제 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-116">Don't worry about understanding them now.</span></span> <span data-ttu-id="af481-117">이 내용에 대해 배우게 됩니다. 정의를 확인해야 하는 경우 이 섹션을 다시 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-117">Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.</span></span>

| <span data-ttu-id="af481-118">Name</span><span class="sxs-lookup"><span data-stu-id="af481-118">Name</span></span> | <span data-ttu-id="af481-119">설명</span><span class="sxs-lookup"><span data-stu-id="af481-119">Description</span></span> |
|-----------|-------------|
|<span data-ttu-id="af481-120">포크</span><span class="sxs-lookup"><span data-stu-id="af481-120">fork</span></span>|<span data-ttu-id="af481-121">기본 GitHub 리포지토리의 복사본을 참조하는 경우 일반적으로 명사로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="af481-121">Normally used as a noun, when referring to a copy of a main GitHub repository.</span></span> <span data-ttu-id="af481-122">실제로 포크는 다른 리포지토리일 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-122">In practice, a fork is just another repository.</span></span> <span data-ttu-id="af481-123">하지만 GitHub이 기본/부모 리포지토리에 다시 연결된다는 점에서 구별됩니다.</span><span class="sxs-lookup"><span data-stu-id="af481-123">But it's special in the sense that GitHub maintains a connection back to the main/parent repository.</span></span> <span data-ttu-id="af481-124">"먼저 리포지토리를 포크해야 합니다."에서와 같이 동사로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-124">It's sometimes used as a verb, as in "You must fork the repository first."</span></span>|
|<span data-ttu-id="af481-125">원격</span><span class="sxs-lookup"><span data-stu-id="af481-125">remote</span></span>|<span data-ttu-id="af481-126">"원본" 또는 "업스트림" 원격과 같이 원격 리포지토리에 대한 명명된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-126">A named connection to a remote repository, such as the "origin" or "upstream" remote.</span></span> <span data-ttu-id="af481-127">이 연결은 다른 컴퓨터에서 호스팅되는 리포지토리를 참조하는 데 사용되므로 Git에서는 이를 원격이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-127">Git refers to this as remote because it is used to reference a repository that's hosted on another computer.</span></span> <span data-ttu-id="af481-128">이 워크플로에서 원격은 항상 GitHub 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-128">In this workflow, a remote is always a GitHub repository.</span></span>|
|<span data-ttu-id="af481-129">원본</span><span class="sxs-lookup"><span data-stu-id="af481-129">origin</span></span>|<span data-ttu-id="af481-130">로컬 리포지토리와 복제 원본 리포지토리 간 연결에 할당된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-130">The name assigned to the connection between your local repository and the repository from which it was cloned.</span></span> <span data-ttu-id="af481-131">이 워크플로에서 원본은 포크에 대한 연결을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af481-131">In this workflow, origin represents the connection to your fork.</span></span> <span data-ttu-id="af481-132">"변경 내용을 원본으로 푸시합니다."에서와 같이 원본 리포지토리 자체의 모니커로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-132">It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."</span></span>|
|<span data-ttu-id="af481-133">업스트림</span><span class="sxs-lookup"><span data-stu-id="af481-133">upstream</span></span>|<span data-ttu-id="af481-134">원본 원격과 같이 업스트림은 다른 리포지토리에 대한 명명된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-134">Like the origin remote, upstream is a named connection to another repository.</span></span> <span data-ttu-id="af481-135">이 워크플로에서 업스트림은 로컬 리포지토리와 포크를 만든 기본 리포지토리 간에 연결을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af481-135">In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created.</span></span> <span data-ttu-id="af481-136">"변경 내용을 업스트림으로 끌어옵니다."에서와 같이 업스트림 리포지토리 자체에 모니커로 사용되는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-136">It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."</span></span>|

## <a name="workflow"></a><span data-ttu-id="af481-137">워크플로</span><span class="sxs-lookup"><span data-stu-id="af481-137">Workflow</span></span>

>[!IMPORTANT]
> <span data-ttu-id="af481-138">아직 [설정](get-started-setup-github.md) 단계를 완료하지 않은 경우 해당 단계를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-138">If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section.</span></span> <span data-ttu-id="af481-139">이 섹션은 GitHub 계정을 설정하고 Git Bash 및 Markdown 편집기를 설치하며 포크를 만들고 로컬 리포지토리를 설정하는 과정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-139">This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository.</span></span> <span data-ttu-id="af481-140">리포지토리 또는 분기와 같은 Git 및 GitHub 개념에 익숙하지 않은 경우 먼저 [Git 및 GitHub 기본 사항](git-github-fundamentals.md)을 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-140">If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).</span></span>

<span data-ttu-id="af481-141">이 워크플로에서 반복적인 주기에서 흐름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-141">In this workflow, changes flow in a repetitive cycle.</span></span> <span data-ttu-id="af481-142">디바이스의 로컬 리포지토리에서 시작하여 GitHub 포크로 이동하여 기본 GitHub 리포지토리로 이동한 다음 다른 참여자의 변경 내용을 포함하도록 다시 로컬로 돌아옵니다.</span><span class="sxs-lookup"><span data-stu-id="af481-142">Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.</span></span>

### <a name="use-github-flow"></a><span data-ttu-id="af481-143">GitHub Flow 사용</span><span class="sxs-lookup"><span data-stu-id="af481-143">Use GitHub flow</span></span>

<span data-ttu-id="af481-144">[Git 및 GitHub 기본 사항](git-github-fundamentals.md#git)에서 Git 리포지토리에는 마스터 분기와 마스터로 통합되지 않은 상태에서 진행 중인 추가 분기가 포함된다는 점을 상기하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-144">Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master.</span></span> <span data-ttu-id="af481-145">논리적으로 연결된 변경 내용 집합을 새로 지정할 때마다 워크플로를 통해 변경 내용을 관리하는 *작업 분기*를 만드는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-145">Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow.</span></span> <span data-ttu-id="af481-146">여기서 작업 분기라고 하는 이유는 변경 내용을 다시 마스터 분기로 통합하기 전까지 변경 내용을 반복/구체화하는 작업 영역이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-146">We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.</span></span>

<span data-ttu-id="af481-147">특정 분기에 연결된 변경 내용을 격리하면 해당 변경 내용을 독립적으로 제어하고 소개하고 게시 주기에 있는 특정 릴리스 시점에 대상으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-147">Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle.</span></span> <span data-ttu-id="af481-148">실제로, 작업 유형에 따라 리포지토리에 몇 개의 작업 분기를 쉽게 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-148">In reality, depending on the type of work you do, you can easily end up with several working branches in your repository.</span></span> <span data-ttu-id="af481-149">각각 다른 프로젝트를 나타내는 여러 분기에서 동시에 작업하는 것은 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-149">It's not uncommon to be working on multiple branches at the same time, each representing a different project.</span></span>

>[!TIP]
><span data-ttu-id="af481-150">마스터 분기에서 변경 내용을 지정하는 것은 적절하지 *않습니다*.</span><span class="sxs-lookup"><span data-stu-id="af481-150">Making your changes in the master branch is *not* a good practice.</span></span> <span data-ttu-id="af481-151">특정 시기에 기능을 릴리스하기 위해 마스터 분기를 사용하여 변경 내용을 적용하는 경우를 가정하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-151">Imagine that you use the master branch to introduce a set of changes for a timed feature release.</span></span> <span data-ttu-id="af481-152">변경 내용을 지정하고 릴리스되기를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-152">You finish the changes and are waiting to release them.</span></span> <span data-ttu-id="af481-153">그 사이에 어떤 문제를 해결해 달라는 긴급 요청을 받고 마스터 분기에 있는 파일을 변경한 다음 해당 변경 내용을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-153">Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change.</span></span> <span data-ttu-id="af481-154">이 예제에서는 특정 날짜에 릴리스하기 위해 유보하고 있던 수정 *및* 변경 내용을 의도치 않게 게시했습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-154">In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.</span></span>

<span data-ttu-id="af481-155">이제 로컬 리포지토리에서 새로운 작업 분기를 만들어 제안된 변경 내용을 캡처하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-155">Now let's create a new working branch in your local repository, to capture your proposed changes.</span></span> <span data-ttu-id="af481-156">Git Bash를 설치한 경우([콘텐츠 작성 도구 설치](get-started-setup-tools.md) 참조) 복제된 리포지토리 내에서 새 분기를 만들고 하나의 명령으로 해당 분기를 “체크 아웃”할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-156">If you've setup Git Bash (see [Install content authoring tools](get-started-setup-tools.md)), you can create a new branch and "checkout" that branch with one command from within your cloned repository:</span></span>

````
git checkout -b "branchname"
````

<span data-ttu-id="af481-157">Git 클라이언트는 각기 다르므로 원하는 클라이언트에 대한 도움말을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-157">Each git client is different, so consult the help for your preferred client.</span></span> <span data-ttu-id="af481-158">[GitHub Flow](https://guides.github.com/introduction/flow/)의 GitHub Guide에서 프로세스의 개요를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-158">You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>

## <a name="making-your-changes"></a><span data-ttu-id="af481-159">변경하기</span><span class="sxs-lookup"><span data-stu-id="af481-159">Making your changes</span></span>

<span data-ttu-id="af481-160">Microsoft 리포지토리의 복사본(“복제본”)이 있고 분기를 만들었으므로 이제 [콘텐츠 작성 도구 설치](get-started-setup-tools.md) 페이지에 설명된 대로 모든 텍스트 편집기 또는 Markdown editor를 사용하여 커뮤니티에 도움이 되는 변경 내용을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-160">Now that you have a copy ("clone") of the Microsoft repository and you've created a branch, you're now free to make whatever changes you think would benefit the community using any text or Markdown editor, as outlined on the [Install content authoring tools](get-started-setup-tools.md) page.</span></span>  <span data-ttu-id="af481-161">준비될 때까지 변경 내용을 Microsoft에 제출할 필요 없이 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-161">You can save your changes locally without needing to submit them to Microsoft until you're ready.</span></span>

## <a name="saving-changes-to-your-repository"></a><span data-ttu-id="af481-162">리포지토리에 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="af481-162">Saving changes to your repository</span></span>

<span data-ttu-id="af481-163">작성자에게 변경 내용을 보내기 전에 먼저 Github 리포지토리에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-163">Before sending your changes to the author, you must first save them to your Github repository.</span></span>  <span data-ttu-id="af481-164">모든 도구가 각기 다르지만 Git Bash 명령줄을 사용하는 경우 몇 가지 간단한 단계로 이 작업을 수행할 수 있음을 다시 한번 말씀드립니다.</span><span class="sxs-lookup"><span data-stu-id="af481-164">Again, while all tools are different, if you're using the Git Bash command line, this can be done in just a few easy steps.</span></span>

<span data-ttu-id="af481-165">먼저 리포지토리 내에서 모든 변경 내용을 커밋하려면 ‘스테이징’해야 합니다. </span><span class="sxs-lookup"><span data-stu-id="af481-165">First, from within the repository, you need to _stage_ all of your changes to be commmited.</span></span>  <span data-ttu-id="af481-166">다음을 실행하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-166">This can be done by executing:</span></span>

````
git add --all
````

<span data-ttu-id="af481-167">다음으로, 저장된 변경 내용을 로컬 리포지토리에 커밋해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-167">Next, you need to commit your saved changes to your local repository.</span></span>  <span data-ttu-id="af481-168">다음을 실행하여 Git Bash에서 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-168">This can be done in Git Bash by running:</span></span>

````
git commit -m "Short Description of Changes Made"
````

<span data-ttu-id="af481-169">마지막으로, 로컬 컴퓨터에서 이 분기를 만들었으므로 GitHub.com 계정의 포크에서 이 내용을 인식하도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-169">Finally, since you created this branch on your local computer, you need to let the fork in your GitHub.com account know about it.</span></span>  <span data-ttu-id="af481-170">Git Bash를 사용하는 경우 다음을 실행하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-170">If you're using Git Bash, this can be done by running:</span></span>

````
git push --set-upstream origin <branchname>
````

<span data-ttu-id="af481-171">작업을 완료했습니다!</span><span class="sxs-lookup"><span data-stu-id="af481-171">You've done it!</span></span>  <span data-ttu-id="af481-172">이제 코드가 GitHub 리포지토리에 있으며 끌어오기 요청을 만들 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-172">Your code is now up in your GitHub repository and ready for you to create a pull request.</span></span>  

>[!TIP]
> <span data-ttu-id="af481-173">변경 내용을 푸시할 때 변경 내용이 개인 GitHub 계정에 표시되더라도 즉시 끌어오기 요청을 제출해야 한다는 규칙은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-173">Even though your changes become visible in your personal GitHub account when you push them, there is no rule that you need to submit a pull request immediately.</span></span>  <span data-ttu-id="af481-174">지금 중지했다가 추가 조정을 위해 나중에 돌아오려는 경우 괜찮습니다!</span><span class="sxs-lookup"><span data-stu-id="af481-174">If you want to come stop and return at a later time to make additional tweaks, that's OK!</span></span>

<span data-ttu-id="af481-175">제출한 내용을 수정해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="af481-175">Need to fix something you submitted?</span></span>  <span data-ttu-id="af481-176">문제없습니다!</span><span class="sxs-lookup"><span data-stu-id="af481-176">No problem!</span></span>  <span data-ttu-id="af481-177">같은 분기에서 변경한 다음, 커밋한 후 다시 푸시하면 됩니다(같은 분기의 이후 푸시에 대해 업스트림 서버를 설정할 필요 없음).</span><span class="sxs-lookup"><span data-stu-id="af481-177">Just make your changes in the same branch and then commit and push again (no need to set the upstream server on subsequent pushes of the same branch).</span></span>

<span data-ttu-id="af481-178">이와 관련 없는 내용을 더 변경해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="af481-178">Got more changes you need to make unrelated to this one?</span></span>  <span data-ttu-id="af481-179">마스터 분기로 다시 전환하고 다른 새 분기를 체크 아웃하면 됩니다. Git Bash를 사용하는 경우 다음과 같이 간단합니다.</span><span class="sxs-lookup"><span data-stu-id="af481-179">Switch back to the master branch and checkout another fresh branch,  Using Git Bash, this is as easy as:</span></span>

````
git checkout master
git checkout -b "branchname"
````

<span data-ttu-id="af481-180">이제 다시 새 분기로 돌아왔으며 마스터 기여자가 되어 가는 과정을 잘하고 계십니다.</span><span class="sxs-lookup"><span data-stu-id="af481-180">You're now back in a new branch and you're well on your way to being a master contributer.</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="af481-181">다음 단계</span><span class="sxs-lookup"><span data-stu-id="af481-181">Next steps</span></span>

<span data-ttu-id="af481-182">이것으로 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="af481-182">That's it!</span></span> <span data-ttu-id="af481-183">여러분은 docs.microsoft.com 콘텐츠에 참여하셨습니다.</span><span class="sxs-lookup"><span data-stu-id="af481-183">You've made a contribution to docs.microsoft.com content!</span></span>

- <span data-ttu-id="af481-184">Markdwon, Markdown 확장 구문과 같은 항목에 대해 자세히 알아보려면 계속해서 [필수 항목 작성](how-to-write-use-markdown.md) 문서를 진행하세요.</span><span class="sxs-lookup"><span data-stu-id="af481-184">To learn more about topics such as Markdown and Markdown extensions syntax, continue to the [Writing essentials](how-to-write-use-markdown.md) article.</span></span>
