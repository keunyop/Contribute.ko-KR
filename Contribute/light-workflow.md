---
title: 사소하거나 자주 발생하지 않는 변경 내용에 대한 GitHub 참여 워크플로
description: 이 문서에서는 "사소한" 기여자 워크플로를 사용하여 docs.microsoft.com 문서에 참여하는 방법을 보여 줍니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a><span data-ttu-id="a64be-103">사소하거나 자주 발생하지 않는 변경 내용에 대한 GitHub 참여 워크플로</span><span class="sxs-lookup"><span data-stu-id="a64be-103">GitHub contribution workflow for minor or infrequent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a64be-104">docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 채택했습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="a64be-105">자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a64be-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="a64be-106">또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.</span><span class="sxs-lookup"><span data-stu-id="a64be-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="a64be-107">공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="a64be-108">변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="a64be-109">온라인 양식 작성을 먼저 완료해야 Microsoft에서 끌어오기 요청을 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-109">We need you to complete the online form before we can accept your pull request.</span></span>

## <a name="overview"></a><span data-ttu-id="a64be-110">개요</span><span class="sxs-lookup"><span data-stu-id="a64be-110">Overview</span></span>

<span data-ttu-id="a64be-111">Markdown이 워크플로는 사소하거나 자주 발생하지 않는 변경 내용에 적합하며 GitHub의 웹 기반 Markdown 편집기를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-111">This workflow is suitable for making minor or infrequent changes, by using GitHub's web-based Markdown editor.</span></span> <span data-ttu-id="a64be-112">UI가 일부 Git 작업 및 작성 시나리오를 지원하지 않으므로 GitHub 편집기에서 수행할 수 있는 작업은 제한되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-112">The GitHub editor is limited in terms of what you can do, because the UI does not support all Git operations and authoring scenarios.</span></span> <span data-ttu-id="a64be-113">크게 참여해야 하거나 고급 Git 기능(분기 관리, 고급 병합 충돌 해결)에 대한 지원이 필요한 경우 [중요 또는 장기 변경 워크플로](full-workflow.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a64be-113">If you need to make large contributions, or you need support for advanced Git features (such as branch management or advanced merge conflict resolution), refer to the [major or long-running changes workflow](full-workflow.md).</span></span>

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a><span data-ttu-id="a64be-114">GitHub 편집기를 사용하여 변경 내용을 제안하는 절차</span><span class="sxs-lookup"><span data-stu-id="a64be-114">Procedure for using the GitHub editor to propose your changes</span></span>

1. <span data-ttu-id="a64be-115">문서의 해당 GitHub 리포지토리 및 Markdown 파일을 탐색합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-115">Browse to the article's corresponding GitHub repository and Markdown file.</span></span> <span data-ttu-id="a64be-116">다음 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-116">You can use either of the following methods:</span></span>

   - <span data-ttu-id="a64be-117">관련된 GitHub 리포지토리에서 Markdown 파일을 탐색하여 문서를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-117">Find the article by browsing through the Markdown files in the related GitHub repository.</span></span>
   - <span data-ttu-id="a64be-118">[docs.microsoft.com](https://docs.microsoft.com/)에서 문서로 이동한 다음 페이지의 오른쪽 위 모서리에 있는 **편집** 링크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-118">Go to the article on [docs.microsoft.com](https://docs.microsoft.com/) and select the **Edit** link in the upper-right corner of the page.</span></span>

     ![편집 링크의 위치](./media/light-workflow/contributetogit.png)

2. <span data-ttu-id="a64be-120">**이 파일 편집** 연필 아이콘을 클릭하여 편집 모드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-120">Select the **Edit this file** pencil icon to go into edit mode:</span></span>

    ![연필 아이콘의 위치](./media/light-workflow/editicon.png)

3. <span data-ttu-id="a64be-122">**파일 편집** 탭에서 Markdown을 사용하여 변경하고 **변경 내용 미리 보기** 탭에서 변경 내용을 미리 봅니다. 편집기 사용 방법은 간단하지만 도움이 필요한 경우 다음 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a64be-122">Make changes by using Markdown on the **Edit file** tab, and preview your changes on the **Preview changes** tab. Using the editor is fairly straightforward, but if you need assistance, see the following guides:</span></span>

   - [<span data-ttu-id="a64be-123">Markdown 사용 방법</span><span class="sxs-lookup"><span data-stu-id="a64be-123">How to use Markdown</span></span>](how-to-write-use-markdown.md)
   - [<span data-ttu-id="a64be-124">GitHub에서 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="a64be-124">Creating files on GitHub</span></span>](https://github.com/blog/1327-creating-files-on-github)
   - [<span data-ttu-id="a64be-125">리포지토리에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="a64be-125">Upload files to your repositories</span></span>](https://github.com/blog/2105-upload-files-to-your-repositories)

4. <span data-ttu-id="a64be-126">페이지 아래로 스크롤하면 다음 중 하나를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-126">Scroll to the bottom of the page, where you see one of the following:</span></span>

   - <span data-ttu-id="a64be-127">**파일 변경 내용 제안**: [다른 사용자의 리포지토리에서 파일 편집](https://help.github.com/articles/editing-files-in-another-user-s-repository/)과 같은 리포지토리에 대한 읽기 전용 액세스 권한이 있는 경우 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-127">**Propose file change**: Appears when you have read-only access to the repository, such as [editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/).</span></span> <span data-ttu-id="a64be-128">이 경우에 GitHub는 리포지토리의 일부에서 "패치" 분기를 만듭니다(리포지토리의 포크가 없는 경우 만듬).</span><span class="sxs-lookup"><span data-stu-id="a64be-128">In this case, GitHub will create a "patch" branch in your fork of the repository (and automatically create a fork if it doesn't exist).</span></span> <span data-ttu-id="a64be-129">**파일 변경 제안**을 선택하면 변경 내용을 확인할 수 있는 **변경 내용 비교** 페이지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-129">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="a64be-130">그런 다음 **끌어오기 요청 만들기** 단추를 선택하여 끌어오기 요청 큐에 변경 내용을 제출하고 [다음 섹션](#pull-request-processing)으로 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-130">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

   - <span data-ttu-id="a64be-131">**변경 내용 커밋**: [고유한 리포지토리에서 파일 편집](https://help.github.com/articles/editing-files-in-your-repository/)과 같은 리포지토리에 대한 쓰기 권한이 있는 경우 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-131">**Commit changes**: Appears when you have write permissions to a repository, such as [editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/).</span></span> <span data-ttu-id="a64be-132">이 경우에 GitHub에는 변경 내용을 저장하는 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-132">In this case, GitHub gives you two options for saving your changes:</span></span>

     - <span data-ttu-id="a64be-133">**`<branch-name>` 분기에 직접 커밋**에서 `<branch-name>`은 **편집** 단추를 선택할 때 사용자가 위치한 분기의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-133">**Commit directly to the `<branch-name>` branch**, where `<branch-name>` is the name of the branch that you were on when you selected the **Edit** button.</span></span> <span data-ttu-id="a64be-134">그러면 끌어오기 요청을 사용하지 않고 분기에 직접 변경 내용을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-134">This applies your changes directly to the branch instead of using a pull request.</span></span> <span data-ttu-id="a64be-135">이 시점에서 작업이 마무리됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-135">At this point, you're finished!</span></span>

     - <span data-ttu-id="a64be-136">**이 커밋에 대한 새 분기 시작 및 끌어오기 요청 시작**은 새 분기를 만들기 위해 기본 이름에 대한 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-136">**Create a new branch for this commit and start a pull request**, which prompts you with a default name to create a new branch.</span></span> <span data-ttu-id="a64be-137">**파일 변경 제안**을 선택하면 변경 내용을 확인할 수 있는 **변경 내용 비교** 페이지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-137">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="a64be-138">그런 다음 **끌어오기 요청 만들기** 단추를 선택하여 끌어오기 요청 큐에 변경 내용을 제출하고 [다음 섹션](#pull-request-processing)으로 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="a64be-138">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="a64be-139">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a64be-139">Next steps</span></span>

- <span data-ttu-id="a64be-140">계속해서 "쓰기 기본 요소" 섹션에서 Markdown 및 Markdown 확장 구문 등과 같은 항목에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="a64be-140">Continue to the "Writing essentials" articles to learn more about Markdown, Markdown extensions syntax, and more.</span></span>
