---
title: 설명서용 Git 및 GitHub 기본 사항
description: 이 문서에서는 Git, GitHub 리포지토리 및 콘텐츠 구성 방법에 대한 개요와 docs.microsoft.com에 사용되는 명명 규칙에 대해 설명합니다.
ms.date: 06/30/2017
ms.openlocfilehash: 8a116067fdd7d031c560abfb7055236e0bfb1a3d
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36239805"
---
# <a name="git-and-github-essentials-for-docs"></a><span data-ttu-id="7915b-103">Docs용 Git 및 GitHub 기본 사항</span><span class="sxs-lookup"><span data-stu-id="7915b-103">Git and GitHub essentials for Docs</span></span>

## <a name="overview"></a><span data-ttu-id="7915b-104">개요</span><span class="sxs-lookup"><span data-stu-id="7915b-104">Overview</span></span>

<span data-ttu-id="7915b-105">Docs 콘텐츠 참여자는 여러 도구와 프로세스를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-105">As a contributor to Docs content, you will interact with multiple tools and processes.</span></span> <span data-ttu-id="7915b-106">동일한 프로젝트에서 다른 참여자와 동시에 작업하게 되며, 정확히 동일한 콘텐츠를 동시에 작업하게 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-106">You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time.</span></span> <span data-ttu-id="7915b-107">이러한 작업은 Git 및 GitHub 소프트웨어를 통해 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-107">This is all enabled through Git and GitHub software.</span></span>

<span data-ttu-id="7915b-108">Git은 오픈 소스 버전 제어 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-108">Git is an open-source version control system.</span></span> <span data-ttu-id="7915b-109">Git을 사용하면 *리포지토리*에 위치하는 파일의 *배포된 버전 제어*를 통해 이러한 유형의 프로젝트 공동 작업을 손쉽게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-109">It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*.</span></span> <span data-ttu-id="7915b-110">본질적으로 Git를 통해 지정된 리포지토리에서 시간에 따라 여러 참여자가 수행한 작업의 스트림을 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-110">In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.</span></span>

<span data-ttu-id="7915b-111">GitHub는 [docs.microsoft.com](https://docs.microsoft.com) 콘텐츠를 저장하는 데 사용되는 Git 리포지토리와 같은 Git 리포지토리용 웹 기반 호스팅 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-111">GitHub is a web-based hosting service for Git repositories, such as those used to store [docs.microsoft.com](https://docs.microsoft.com) content.</span></span> <span data-ttu-id="7915b-112">모든 프로젝트에서 GitHub는 기본 리포지토리를 호스트합니다. 여기에서 참여자는 각자 작업의 복사본을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-112">For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.</span></span>

## <a name="git"></a><span data-ttu-id="7915b-113">Git</span><span class="sxs-lookup"><span data-stu-id="7915b-113">Git</span></span>

<span data-ttu-id="7915b-114">중앙 집중식 버전 제어 시스템(예: Team Foundation Server, SharePoint 또는 Visual SourceSafe)에 익숙한 경우 Git에는 해당 배포 모델을 지원하는 고유한 참여 워크플로 및 용어가 있다는 점을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-114">If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you will notice that Git has a unique contribution workflow and terminology to support its distributed model.</span></span> <span data-ttu-id="7915b-115">예를 들어 일반적으로 체크 아웃/체크 인 작업과 연결된 파일 잠금이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-115">For instance, there is no file locking that is normally associated with check-out/check-in operations.</span></span> <span data-ttu-id="7915b-116">실제로 Git은 더욱 자세한 수준에서 변경 내용을 확인하고 파일을 바이트 단위로 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-116">As a matter of fact, Git is concerned about changes at an even finer level, comparing files byte by byte.</span></span>

<span data-ttu-id="7915b-117">또한 Git은 계층화된 구조체를 사용하여 프로젝트에 대한 콘텐츠를 저장하고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-117">Git also uses a tiered structure to store and manage content for a project:</span></span>

- <span data-ttu-id="7915b-118">*리포지토리*: *리포지토리*라고 하며 가장 높은 저장 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-118">*Repository*: Also known as a *repo*, this is the highest unit of storage.</span></span> <span data-ttu-id="7915b-119">리포지토리는 하나 이상의 분기를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-119">A repository contains one or more branches.</span></span>
- <span data-ttu-id="7915b-120">*분기*: 프로젝트의 콘텐츠 세트를 구성하는 파일과 폴더가 포함된 저장 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-120">*Branch*: A unit of storage that contains the files and  folders that make up a project's content set.</span></span> <span data-ttu-id="7915b-121">분기는 작업의 스트림(일반적으로 버전이라고 함)을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-121">Branches separate streams of work (typically referred to as versions).</span></span> <span data-ttu-id="7915b-122">언제나 기여가 이루어지며 특정 분기로 범위가 정해집니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-122">Contributions are always made and scoped to a specific branch.</span></span> <span data-ttu-id="7915b-123">모든 리포지토리는 기본 분기(일반적으로 "마스터"라고 함)를 포함하며 하나 이상의 분기는 마스터 분기에 병합되도록 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-123">All repositories contain a default branch (typically named "master") and one or more branches that are destined to be merged back into the master branch.</span></span> <span data-ttu-id="7915b-124">마스터 분기는 현재 버전의 역할을 하며 프로젝트에 대한 "정확한 정보를 확인할 수 있는 단일 소스"입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-124">The master branch serves as the current version and "single source of truth" for the project.</span></span> <span data-ttu-id="7915b-125">리포지토리의 나머지 분기들은 부모인 마스터 분기에서 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-125">It's the parent from which all other branches in the repository are created.</span></span>

<span data-ttu-id="7915b-126">참여자는 Git와 상호 작용하여 로컬 및 GitHub 수준에서 리포지토리를 업데이트하고 조작합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-126">Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:</span></span>

- <span data-ttu-id="7915b-127">로컬로 Git Bash 콘솔과 같은 도구를 통해 로컬 리포지토리를 관리하고 GitHub 리포지토리와 통신하는 Git 명령을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-127">Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories</span></span>
- <span data-ttu-id="7915b-128">Git과 통합된 [www.github.com](https://www.github.com)을 통해 기본 리포지토리로 다시 이동하는 참가 조정을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-128">Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository</span></span>

## <a name="github"></a><span data-ttu-id="7915b-129">GitHub</span><span class="sxs-lookup"><span data-stu-id="7915b-129">GitHub</span></span>

> [!NOTE]
> <span data-ttu-id="7915b-130">Docs 지침이 GitHub 사용을 기반으로 하지만 일부 팀에서는 Visual Studio Team Services를 사용하여 Git 리포지토리를 호스트합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-130">Although Docs guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories.</span></span> <span data-ttu-id="7915b-131">Visual Studio 팀 탐색기 클라이언트는 명령줄을 통해 Git 명령을 사용하는 대안으로 Team Services 리포지토리와 상호 작용하는 GUI를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-131">The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.</span></span>
> </br>
> <span data-ttu-id="7915b-132">또한 다음 중 대부분의 지침은 수년간 GitHub에서 Azure 서비스 콘텐츠를 호스트하는 동안 경험으로 확인된 모범 사례입니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-132">Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub.</span></span> <span data-ttu-id="7915b-133">일부 Docs 리포지토리에서 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-133">They might be required in some Docs repositories.</span></span>

<span data-ttu-id="7915b-134">모든 워크플로는 모든 Docs 프로젝트의 기본 리포지토리가 저장되는 GitHub 수준에서 시작하고 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-134">All workflows begin and end at the GitHub level, where the main repository for any Docs project is stored.</span></span> <span data-ttu-id="7915b-135">참여자가 직접 사용하기 위해 만드는 복사본은 여러 컴퓨터에 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-135">The copies that contributors create for their own use are distributed across multiple computers.</span></span> <span data-ttu-id="7915b-136">이러한 복사본은 결과적으로 프로젝트의 기본 GitHub 리포지토리로 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-136">These copies are eventually reconciled back into the project's main GitHub repository.</span></span>

### <a name="directory-organization"></a><span data-ttu-id="7915b-137">디렉토리 조직</span><span class="sxs-lookup"><span data-stu-id="7915b-137">Directory organization</span></span>

<span data-ttu-id="7915b-138">앞서 언급한 대로 프로젝트의 기본/마스터 분기는 프로젝트에 대한 현재 버전의 콘텐츠로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-138">As mentioned earlier, a project's default/master branch serves as the current version of content for the project.</span></span> <span data-ttu-id="7915b-139">마스터 분기 및 이 분기에서 생성된 분기의 콘텐츠는 해당 Docs 페이지의 문서 구성에 맞추어 대체적으로 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-139">The content in the master branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Docs pages.</span></span> <span data-ttu-id="7915b-140">하위 디렉토리는 유사 콘텐츠(예: 서비스), 미디어 콘텐츠(예: 이미지 파일) 및 "포함" 파일을 분리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-140">Subdirectories are used for separation of like content (such as services), media content (such as image files), and "include" files (which enable reuse of content).</span></span>

<span data-ttu-id="7915b-141">기본 `articles` 디렉터리는 일반적으로 리포지토리의 루트에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-141">You can typically find a main `articles` directory off the root of the repository.</span></span> <span data-ttu-id="7915b-142">문서 디렉터리에는 하위 디렉터리 집합이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-142">The articles directory contains a set of subdirectories.</span></span> <span data-ttu-id="7915b-143">하위 디렉터리의 문서는 *.md* 확장명을 사용하는 Markdown 파일로 서식이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-143">Articles in the subdirectories are formatted as Markdown files that use an *.md* extension.</span></span> <span data-ttu-id="7915b-144">여러 서비스를 지원하는 일부 리포지토리는 [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) 리포지토리와 같은 일반 `/articles` 하위 디렉터리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-144">Some repositories that support multiple services use a generic `/articles` subdirectory, such as the [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) repository.</span></span> <span data-ttu-id="7915b-145">다른 리포지토리는 `/IntuneDocs`를 사용하는 [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) 리포지토리와 같은 서비스 특정 이름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-145">Others might use a service-specific name, such as the [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) repository, which uses `/IntuneDocs`.</span></span>

<span data-ttu-id="7915b-146">이 디렉토리의 루트 내에서 전반적인 서비스 또는 제품과 관련된 일반적인 문서를 발견할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-146">Within the root of this directory, you can find general articles that relate to the overall service or product.</span></span> <span data-ttu-id="7915b-147">또한 일반적으로 기능/서비스 또는 일반적인 시나리오와 일치하는 다른 하위 디렉토리 시리즈를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-147">And typically, you can then find another series of subdirectories that match the features/services or common scenarios.</span></span> <span data-ttu-id="7915b-148">예를 들어 Azure "가상 머신" 문서는 `/virtual-machines` 하위 디렉터리에 있으며, Intune "이해 및 탐색" 문서는 `/understand-explore` 하위 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-148">For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.</span></span>

### <a name="media-subdirectory"></a><span data-ttu-id="7915b-149">미디어 하위 디렉토리</span><span class="sxs-lookup"><span data-stu-id="7915b-149">Media subdirectory</span></span>

<span data-ttu-id="7915b-150">각 문서 디렉터리에는 해당 미디어 파일의 `/media` 하위 디렉터리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-150">Each article directory contains a `/media` subdirectory for corresponding media files.</span></span> <span data-ttu-id="7915b-151">미디어 파일에는 이미지 참조가 있는 문서에서 사용하는 이미지가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-151">Media files contain images used by articles that have image references.</span></span>

### <a name="includes-subdirectory"></a><span data-ttu-id="7915b-152">포함되는 내용 하위 디렉토리</span><span class="sxs-lookup"><span data-stu-id="7915b-152">Includes subdirectory</span></span>

<span data-ttu-id="7915b-153">두 개 이상의 문서에서 공유되는 재사용 가능 콘텐츠는 언제나 기본 `articles` 디렉터리 아래 `/includes` 하위 디렉터리에 배치됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-153">Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory.</span></span> <span data-ttu-id="7915b-154">포함 파일을 사용하는 Markdown 파일에서 해당 "포함" Markdown 확장은 포함 파일을 참조해야 하는 위치에 배치됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-154">In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.</span></span>

<span data-ttu-id="7915b-155">추가적인 지침은 [Markdown 사용 방법 - 포함되는 내용](how-to-write-use-markdown.md#includes)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7915b-155">See [How to use Markdown: Includes](how-to-write-use-markdown.md#includes) for additional guidance.</span></span>

### <a name="markdown-file-template"></a><span data-ttu-id="7915b-156">Markdown 파일 템플릿</span><span class="sxs-lookup"><span data-stu-id="7915b-156">Markdown file template</span></span>

<span data-ttu-id="7915b-157">각 리포지토리의 루트 디렉터리에는 편의를 위해 일반적으로 `template.md`라는 Markdown 템플릿 파일이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-157">For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`.</span></span> <span data-ttu-id="7915b-158">리포지토리에 제출할 새 문서를 만들어야 하는 경우 이 템플릿 파일을 "스타터 파일"로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-158">You can use this template file as a "starter file" if you need to create a new article for submission to the repository.</span></span> <span data-ttu-id="7915b-159">파일에는 다음 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-159">The file contains:</span></span>

- <span data-ttu-id="7915b-160">파일 맨 위에서 2개의 3-하이픈 선으로 구분된 **메타데이터 헤더**.</span><span class="sxs-lookup"><span data-stu-id="7915b-160">A **metadata header** at the top of the file, delineated by two, 3-hyphen lines.</span></span> <span data-ttu-id="7915b-161">여기에는 문서와 관련된 정보를 추적하는 데 사용되는 다양한 태그가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-161">It contains the various tags used for tracking information related to the article.</span></span> <span data-ttu-id="7915b-162">문서 메타데이터를 통해 작성자 특성, 참여자 특성, 이동 경로, 문서 설명 등의 특정 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-162">Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions.</span></span> <span data-ttu-id="7915b-163">또한 Microsoft가 콘텐츠의 성능을 평가하는 데 사용하는 SEO 최적화 및 보고 프로세스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-163">It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content.</span></span> <span data-ttu-id="7915b-164">따라서 메타데이터는 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-164">So the metadata is important!</span></span>
- <span data-ttu-id="7915b-165">다양한 메타데이터 태그 및 값에 대해 설명하는 **메타데이터 섹션**.</span><span class="sxs-lookup"><span data-stu-id="7915b-165">A **metadata section** that describes the various metadata tags and values.</span></span> <span data-ttu-id="7915b-166">메타데이터 섹션에 사용할 값을 잘 모를 경우에는 해당 섹션을 비워두거나 선행 해시태그(#)를 사용하여 주석으로 처리할 수 있습니다. 그런 다음 리포지토리의 끌어오기 요청 검토자가 검토 및 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-166">If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.</span></span>
- <span data-ttu-id="7915b-167">다양한 **Markdown 사용 예**는 문서 요소의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-167">Various **examples of using Markdown** to format the elements of an article.</span></span>
- <span data-ttu-id="7915b-168">다양한 알림 형식에 사용할 수 있는 **Markdown 확장 사용에 대한 일반적인 지침**.</span><span class="sxs-lookup"><span data-stu-id="7915b-168">General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.</span></span>
- <span data-ttu-id="7915b-169">iframe을 사용하는 **포함 비디오** 예.</span><span class="sxs-lookup"><span data-stu-id="7915b-169">Examples of **embedding video** by using an iframe.</span></span>
- <span data-ttu-id="7915b-170">단추 및 선택기와 같은 특수한 컨트롤에 사용할 수 있는 **docs.microsoft.com 확장 사용에 대한 일반적인 지침**.</span><span class="sxs-lookup"><span data-stu-id="7915b-170">General **instructions on the use of docs.microsoft.com extensions**, which you can use for special controls such as buttons and selectors.</span></span>

## <a name="pull-requests"></a><span data-ttu-id="7915b-171">끌어오기 요청</span><span class="sxs-lookup"><span data-stu-id="7915b-171">Pull requests</span></span>

<span data-ttu-id="7915b-172">*끌어오기 요청*을 사용하면 참여자가 기본 분기에 적용할 일련의 변경 내용을 편리하게 제안할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-172">A *pull request* provides a convenient way for a contributor to propose a set of changes that will be applied to the default branch.</span></span> <span data-ttu-id="7915b-173">변경 내용(*커밋*이라고도 함)은 참여자의 분기에 저장되므로 GitHub는 가장 먼저 이러한 변경 내용을 기본 분기에 *병합*할 경우의 영향을 모델링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-173">The changes (also known as *commits*) are stored in a contributor's branch, so GitHub can first model the impact of *merging* them into the default branch.</span></span> <span data-ttu-id="7915b-174">끌어오기 요청은 참여자에게 빌드/유효성 검사 프로세스의 피드백을 제공하고, 변경 내용이 기본 분기에 병합되기 전에 끌어오기 요청 검토자가 잠재적인 문제 및 질문을 해결하는 매커니즘으로도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-174">A pull request also serves as a mechanism to provide the contributor with feedback from a build/validation process, the pull request reviewer, to resolve potential issues or questions before the changes are merged into the default branch.</span></span>

<span data-ttu-id="7915b-175">제안하려는 변경 내용의 크기에 따라 끌어오기 요청으로 참여하는 방법은 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-175">There are two ways to contribute by pull request, depending on the size of changes that you want to propose.</span></span> <span data-ttu-id="7915b-176">이 내용은 나중에 이 가이드의 [GitHub 워크플로](how-to-write-workflows-major.md) 섹션에서 자세히 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="7915b-176">We will cover this in detail later, in the [GitHub workflow](how-to-write-workflows-major.md) section of this guide.</span></span>

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
