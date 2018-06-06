---
title: 콘텐츠 작성 도구 설치
description: 이 문서의 정보를 활용하여 Git 및 Markdown 파일 편집에 필요한 클라이언트 도구를 다운로드하고 설치할 수 있습니다.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1011c3fc829202a3df134ddc80eb05b8959b7bf6
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469374"
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="b3ee7-103">콘텐츠 작성 도구 설치</span><span class="sxs-lookup"><span data-stu-id="b3ee7-103">Install content authoring tools</span></span>

<span data-ttu-id="b3ee7-104">이 문서에서는 Git 클라이언트 도구 및 Visual Studio Code를 대화형으로 설치하는 단계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="b3ee7-105">[Git for Windows](https://git-scm.com/download/win) 설치</span><span class="sxs-lookup"><span data-stu-id="b3ee7-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="b3ee7-106">[Visual Studio Code](https://code.visualstudio.com/) 설치</span><span class="sxs-lookup"><span data-stu-id="b3ee7-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="b3ee7-107">[Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 설치</span><span class="sxs-lookup"><span data-stu-id="b3ee7-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="b3ee7-108">아티클에서 사소한 내용을 변경하려는 경우 이 아티클의 단계를 완료할 필요 *없이* 바로 [빠른 변경 워크플로](index.md#quick-edits-to-existing-documents)를 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="b3ee7-109">주요 참가자는 [중요한/장기 실행 변경 워크플로](how-to-write-workflows-major.md)를 사용할 수 있도록 이러한 단계를 완료하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="b3ee7-110">기본 리포지토리에 대한 쓰기 권한이 있는 경우에도 *리포지토리를 포크하고 복제하는 것이 좋습니다(이 가이드에서 이렇게 가정)*. 그러면 포크에서 제안된 변경 내용을 저장하기 위한 읽기/쓰기 권한이 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="b3ee7-111">Windows에 Git 클라이언트 도구 설치</span><span class="sxs-lookup"><span data-stu-id="b3ee7-111">Install Git client tools on Windows</span></span>

 <span data-ttu-id="b3ee7-112">최신 버전의 [Software Freedom Conservancy Git 클라이언트 도구](https://git-scm.com/download/)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="b3ee7-113">설치에는 Git 버전 제어 시스템 및 로컬 Git 리포지토리와 상호 작용하는 데 사용하는 명령줄 앱인 Git Bash가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-113">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="b3ee7-114">CLI(명령줄 인터페이스)보다 GUI(그래픽 사용자 인터페이스)를 선호하는 경우 [Software Freedom Conservancy의 사용 가능한 GUI 클라이언트 페이지](https://git-scm.com/downloads/guis), [GitHub의 GitHub 데스크톱](https://desktop.github.com/) 또는 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)에서 인기 있는 옵션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-114">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="b3ee7-115">설치 및 구성에 대해 선택한 클라이언트의 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-115">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="b3ee7-116">다음 문서에서는 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-116">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="b3ee7-117">사용 가능한 추가 Git 리소스는 다음과 같습니다. [Git terminology](https://help.github.com/articles/github-glossary)(Git 용어) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)(Git 기본 사항) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)(Git 및 GitHub 알아보기)</span><span class="sxs-lookup"><span data-stu-id="b3ee7-117">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="b3ee7-118">Markdown 편집기 이해</span><span class="sxs-lookup"><span data-stu-id="b3ee7-118">Understand Markdown editors</span></span>

<span data-ttu-id="b3ee7-119">Markdown은 읽기 쉽고 배우기 쉬운 가벼운 마크업 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-119">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="b3ee7-120">따라서 빠르게 업계 표준이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-120">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="b3ee7-121">Markdown으로 문서를 작성하려면 먼저 Markdown 편집기를 다운로드하고 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-121">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="b3ee7-122">[Visual Studio Code](https://code.visualstudio.com/)는 Microsoft에서 Markdown 편집에 선호하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-122">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="b3ee7-123">[Atom](https://atom.io)은 Markdown을 편집하는 데 사용되는 또 다른 인기 있는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-123">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="b3ee7-124">Markdown 텍스트는 확장명이 .md인 파일에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-124">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="b3ee7-125">OPS 사용자 지정 Markdown 확장에서 지원하는 Markdown 기본 사항 및 기능을 포함하여 Markdown으로 작성하는 방법에 대한 추가 내용은 나중에 [Markdown 사용 방법](how-to-write-use-markdown.md) 문서에서 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-125">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="b3ee7-126">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b3ee7-126">Visual Studio Code</span></span>

<span data-ttu-id="b3ee7-127">[Visual Studio Code](https://code.visualstudio.com/)(VS Code라고도 함)는 Windows, Linux 및 Mac에서 작동하는 경량 편집기입니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-127">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="b3ee7-128">여기에는 Git 통합 및 확장에 대한 지원이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-128">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="b3ee7-129">[VS Code](https://code.visualstudio.com/)를 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-129">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="b3ee7-130">VS Code 홈페이지에서 사용자의 운영 체제를 올바르게 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-130">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="b3ee7-131">Windows</span><span class="sxs-lookup"><span data-stu-id="b3ee7-131">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="b3ee7-132">Mac</span><span class="sxs-lookup"><span data-stu-id="b3ee7-132">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="b3ee7-133">Linux</span><span class="sxs-lookup"><span data-stu-id="b3ee7-133">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="b3ee7-134">VS Code를 시작하고 현재 폴더를 열려면 명령줄 또는 Bash 셸에서 `code .` 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-134">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="b3ee7-135">현재 폴더가 로컬 Git 리포지토리의 일부인 경우 GitHub 통합이 Visual Studio Code에 자동으로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-135">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="b3ee7-136">Docs Authoring Pack</span><span class="sxs-lookup"><span data-stu-id="b3ee7-136">Docs Authoring Pack</span></span>
<span data-ttu-id="b3ee7-137">Visual Studio Code용 Docs Authoring Pack을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-137">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="b3ee7-138">이 확장 집합에는 Markdown 작성 시 도움이 되는 기본 작성 지원과 미리 보기 기능이 포함되므로, Markdown 모양을 docs.microsoft.com 사이트의 스타일로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-138">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="b3ee7-139">이 [Marketplace 페이지](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)를 방문하고 **설치**를 선택하거나 VS Code 창의 확장 목록에서 `docsmsft.docs-authoring-pack`을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-139">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="b3ee7-140">Docs Authoring Pack은 VS Code 내에서 Alt+M을 눌러서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-140">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="b3ee7-141">도구 모음은 기본적으로 숨겨져 있지만 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-141">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="b3ee7-142">VS Code 설정(Control+쉼표) 및 사용자 추가 설정 `"markdown.showToolbar": true`을 편집하여 도구 모음을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-142">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="b3ee7-143">자세한 내용은 [Docs Authoring Pack](how-to-write-docs-auth-pack.md) 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-143">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="b3ee7-144">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b3ee7-144">Next steps</span></span>

<span data-ttu-id="b3ee7-145">이제 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b3ee7-145">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
