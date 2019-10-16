---
title: 로컬로 Git 리포지토리 설정
description: 이 문서에서는 로컬 Git 리포지토리를 만들고, 포크 및 복제 프로세스를 포함하여 문서화에 참여하기 위한 지침을 제공합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: e73c60c439285f901c5c83e538f8971d795bd6c4
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288599"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="b56f3-103">설명서를 위한 Git 리포지토리 로컬로 설정</span><span class="sxs-lookup"><span data-stu-id="b56f3-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="b56f3-104">이 문서에서는 Microsoft 설명서에 참가하기 위해 로컬 컴퓨터에서 Git 리포지토리를 설정하는 단계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="b56f3-105">참가자는 로컬로 복제된 리포지토리를 사용하여 새 문서를 추가하거나, 기존 문서에 대해 주요 편집 작업을 수행하거나, 아트워크를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="b56f3-106">이러한 일회성 설정 활동을 실행하여 다음과 같은 참가를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-106">You run these one-time setup activities to start contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="b56f3-107">적절한 리포지토리 확인</span><span class="sxs-lookup"><span data-stu-id="b56f3-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="b56f3-108">GitHub 계정에 리포지토리 포크</span><span class="sxs-lookup"><span data-stu-id="b56f3-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="b56f3-109">복제된 파일의 로컬 폴더 선택</span><span class="sxs-lookup"><span data-stu-id="b56f3-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="b56f3-110">로컬 컴퓨터에 리포지토리 복제</span><span class="sxs-lookup"><span data-stu-id="b56f3-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="b56f3-111">업스트림 원격 값 구성</span><span class="sxs-lookup"><span data-stu-id="b56f3-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b56f3-112">문서의 사소한 내용만 변경하는 경우 이 문서의 단계를 완료하지 *않아도* 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="b56f3-113">바로 [빠른 변경 내용 워크플로](index.md#quick-edits-to-existing-documents)를 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="b56f3-114">개요</span><span class="sxs-lookup"><span data-stu-id="b56f3-114">Overview</span></span>

<span data-ttu-id="b56f3-115">Microsoft의 설명서 사이트에 참여하려면 해당 설명서 리포지토리를 복제하여 Markdown 파일을 로컬로 만들고 편집하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="b56f3-116">Microsoft에서는 제안된 변경 내용을 저장하기 위한 읽기/쓰기 권한이 있도록 적절한 리포지토리를 고유의 GitHub 계정에 포크하도록 요구합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="b56f3-117">그런 다음, 끌어오기 요청을 사용하여 변경 내용을 읽기 전용 중앙 공유 리포지토리에 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub Triangle](./media/git-and-github-initial-setup.png)

<span data-ttu-id="b56f3-119">GitHub에 익숙하지 않은 경우 아래 비디오를 시청하고 분기 및 복제 프로세스 개념에 대해 간략히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="b56f3-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="b56f3-120">리포지토리 확인</span><span class="sxs-lookup"><span data-stu-id="b56f3-120">Determine the repository</span></span>

<span data-ttu-id="b56f3-121">[docs.microsoft.com](https://docs.microsoft.com)에 호스트된 설명서는 [github.com](https://www.github.com)의 다양한 리포지토리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="b56f3-122">사용할 리포지토리를 잘 모르는 경우 웹 브라우저를 사용하여 [docs.microsoft.com](https://docs.microsoft.com)에 있는 문서를 방문합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="b56f3-123">문서의 오른쪽 위에 있는 **편집** 링크(연필 아이콘)를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![편집을 클릭하여 리포지토리 및 파일 위치를 확인합니다.](media/index/edit-article.png)

2. <span data-ttu-id="b56f3-125">해당 링크를 사용하면 적절한 리포지토리에 있는 해당 Markdown 파일에 대한 github.com 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="b56f3-126">URL에 주목하여 리포지토리 이름을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-126">Note the URL to view the repository name.</span></span>

   ![URL에 주목하여 리포지토리 위치를 확인합니다.](media/public-repo.png)

   <span data-ttu-id="b56f3-128">예를 들어 다음과 같은 인기 있는 리포지토리는 공공의 참가가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="b56f3-129">Azure 설명서 [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="b56f3-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="b56f3-130">SQL Server 설명서 [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="b56f3-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="b56f3-131">Visual Studio 설명서 [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="b56f3-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="b56f3-132">.NET 설명서 [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="b56f3-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="b56f3-133">Azure .Net SDK 설명서 [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="b56f3-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>
   - <span data-ttu-id="b56f3-134">ConfigMgr 설명서 [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span><span class="sxs-lookup"><span data-stu-id="b56f3-134">ConfigMgr documentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="b56f3-135">리포지토리 포크</span><span class="sxs-lookup"><span data-stu-id="b56f3-135">Fork the repository</span></span>
<span data-ttu-id="b56f3-136">GitHub 웹 사이트를 통해 적절한 리포지토리를 사용하여 자신의 GitHub 계정에 리포지토리 포크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-136">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="b56f3-137">모든 기본 문서 리포지토리는 읽기 전용 액세스를 제공하므로 개인 포크가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-137">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="b56f3-138">변경하려면 [끌어오기 요청](git-github-fundamentals.md#pull-requests)을 포크에서 기본 리포지토리로 제출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-138">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="b56f3-139">이 프로세스를 용이하게 하려면 먼저 쓰기 액세스 권한이 있는 리포지토리의 복사본이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-139">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="b56f3-140">GitHub *포크*로 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-140">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="b56f3-141">기본 리포지토리의 GitHub 페이지로 이동하여 오른쪽 상단의 **포크** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-141">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![GitHub 프로필 예제](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="b56f3-143">메시지가 표시되면 포크를 만들 대상으로 GitHub 계정 타일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-143">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="b56f3-144">이 프롬프트는 GitHub 계정 내에서 포크라고 하는 리포지토리의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-144">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="b56f3-145">로컬 폴더 선택</span><span class="sxs-lookup"><span data-stu-id="b56f3-145">Choose a local folder</span></span>
<span data-ttu-id="b56f3-146">리포지토리의 복사본을 로컬로 보관할 로컬 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-146">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="b56f3-147">일부 리포지토리는 클 수 있습니다(예: azure-docs의 경우 최대 5GB).</span><span class="sxs-lookup"><span data-stu-id="b56f3-147">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="b56f3-148">사용 가능한 디스크 공간이 있는 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-148">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="b56f3-149">기억하고 입력하기 쉬운 폴더 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-149">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="b56f3-150">예를 들어 `C:\docs\` 루트 폴더를 고려하거나 `~/Documents/docs/` 사용자 프로필 디렉터리에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-150">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="b56f3-151">다른 git 리포지토리 폴더 위치 안에 중첩된 로컬 폴더 경로는 선택하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b56f3-151">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="b56f3-152">복제된 git 폴더를 서로 인접하여 저장하도록 허용되지만 서로의 내부에 git 폴더가 중첩되면 파일 추적 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-152">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="b56f3-153">Git Bash를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-153">Launch Git Bash</span></span>

   ![Git Bash 시작](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="b56f3-155">Git Bash가 시작되는 기본 위치는 일반적으로 Windows OS의 홈 디렉터리(~) 또는 `/c/users/<Windows-user-account>/`입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-155">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="b56f3-156">현재 디렉터리를 확인하려면 $ 프롬프트에서 `pwd`를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-156">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="b56f3-157">리포지토리를 로컬로 호스팅하기 위해 만든 폴더로 디렉터리를 변경합니다(cd).</span><span class="sxs-lookup"><span data-stu-id="b56f3-157">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="b56f3-158">Git Bash는 폴더 경로에 백슬래시 대신 슬래시를 사용하는 Linux 규칙을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-158">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="b56f3-159">예를 들어 `cd /c/docs/ ` 또는 `cd ~/Documents/docs/`와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-159">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="b56f3-160">로컬 복제 만들기</span><span class="sxs-lookup"><span data-stu-id="b56f3-160">Create a local clone</span></span>

<span data-ttu-id="b56f3-161">Git Bash를 사용하는 경우 **clone** 명령을 실행하여 리포지토리(포크)의 복사본을 현재 디렉터리의 디바이스로 끌어오도록 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-161">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="b56f3-162">Git 자격 증명 관리자를 사용하여 인증</span><span class="sxs-lookup"><span data-stu-id="b56f3-162">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="b56f3-163">Windows용 Git의 최신 버전을 설치하고 기본 설치에 동의한 경우 기본적으로 Git 자격 증명 관리자가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-163">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="b56f3-164">Git 자격 증명 관리자에서는 GitHub에서 인증된 연결 및 원격을 다시 설정할 때 개인용 액세스 토큰을 다시 호출할 필요가 없으므로 인증을 훨씬 간단하게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-164">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="b56f3-165">리포지토리 이름을 제공하여 **clone** 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-165">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="b56f3-166">복제는 로컬 컴퓨터에서 포크된 리포지토리를 다운로드(복제)합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-166">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="b56f3-167">GitHub UI의 **복제 또는 다운로드** 단추를 누르면 복제 명령에 대한 포크의 GitHub URL을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-167">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![복제 또는 다운로드](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="b56f3-169">복제를 진행하는 동안 포크를 만든 기본 리포지토리가 아닌 *포크*에 대한 경로를 지정하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-169">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="b56f3-170">그렇지 않으면 변경 내용을 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-170">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="b56f3-171">포크는 개인 GitHub 사용자 계정(예: `github.com/<github-username>/<repo>`)을 통해 참조됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-171">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="b56f3-172">복제 명령은 다음 예제와 비슷하게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-172">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="b56f3-173">메시지가 표시되면 GitHub 자격 증명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-173">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub 로그인](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="b56f3-175">메시지가 표시되면 2단계 인증 코드를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-175">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub 2단계 인증](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="b56f3-177">자격 증명은 저장된 다음 나중에 GitHub 요청을 인증하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-177">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="b56f3-178">이 인증은 컴퓨터마다 한 번만 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-178">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="b56f3-179">clone 명령은 포크에서 로컬 디스크의 새 폴더로 리포지토리 파일 복사본을 실행하고 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-179">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="b56f3-180">현재 폴더 내에 새 폴더가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-180">A new folder is made within the current folder.</span></span> <span data-ttu-id="b56f3-181">리포지토리 크기에 따라 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-181">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="b56f3-182">폴더가 완성되면 폴더를 탐색하여 구조를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-182">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="b56f3-183">원격 업스트림 구성</span><span class="sxs-lookup"><span data-stu-id="b56f3-183">Configure remote upstream</span></span>
<span data-ttu-id="b56f3-184">리포지토리가 복제되면 **upstream**이라는 기본 리포지토리에 읽기 전용 원격 연결을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-184">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="b56f3-185">업스트림 URL을 사용하면 로컬 리포지토리를 다른 사용자가 수행한 최근 변경 내용과 동기화된 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-185">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="b56f3-186">**git remote** 명령은 구성 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-186">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="b56f3-187">**fetch** 명령을 사용하여 업스트림 리포지토리에서 분기 정보를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-187">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="b56f3-188">**Git 자격 증명 관리자**를 사용하는 경우 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-188">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="b56f3-189">\<repo\> 및 \<organization\> 자리 표시자를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-189">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="b56f3-190">구성된 값을 보고 URL이 올바른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-190">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="b56f3-191">**원본** URL이 개인 포크를 가리키는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-191">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="b56f3-192">**업스트림** URL이 MicrosoftDocs 또는 Azure와 같은 기본 리포지토리를 가리키는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-192">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="b56f3-193">원격 출력 예제가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-193">Example remote output is shown.</span></span> <span data-ttu-id="b56f3-194">MyGitAccount라는 가상의 git 계정은 개인 액세스 토큰을 사용하여 azure-docs 리포지토리에 액세스하도록 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-194">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="b56f3-195">실수한 경우 원격 값을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-195">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="b56f3-196">upstream 값을 제거하려면 `git remote remove upstream` 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f3-196">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b56f3-197">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b56f3-197">Next steps</span></span>
- <span data-ttu-id="b56f3-198">콘텐츠를 추가하고 업데이트하는 방법에 대해 자세히 알아보려면 [GitHub 참여 워크플로](how-to-write-workflows-major.md) 페이지로 계속 진행하세요.</span><span class="sxs-lookup"><span data-stu-id="b56f3-198">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
