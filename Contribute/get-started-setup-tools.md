---
title: 콘텐츠 작성 도구 설치
description: 이 문서의 정보를 활용하여 Git 및 Markdown 파일 편집에 필요한 클라이언트 도구를 다운로드하고 설치할 수 있습니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="9ebe3-103">콘텐츠 작성 도구 설치</span><span class="sxs-lookup"><span data-stu-id="9ebe3-103">Install content authoring tools</span></span>

<span data-ttu-id="9ebe3-104">이 문서에서는 Git 클라이언트 도구 및 Visual Studio Code를 대화형으로 설치하는 단계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="9ebe3-105">[Git for Windows](https://git-scm.com/download/win) 설치</span><span class="sxs-lookup"><span data-stu-id="9ebe3-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="9ebe3-106">[Visual Studio Code](https://code.visualstudio.com/) 설치</span><span class="sxs-lookup"><span data-stu-id="9ebe3-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="9ebe3-107">아티클에서 사소한 내용을 변경하려는 경우 이 아티클의 단계를 완료할 필요 *없이* 바로 [빠른 변경 워크플로](index.md#quick-edits-to-existing-documents)를 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="9ebe3-108">주요 참가자는 [중요한/장기 실행 변경 워크플로](how-to-write-workflows-major.md)를 사용할 수 있도록 이러한 단계를 완료하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="9ebe3-109">기본 리포지토리에 대한 쓰기 권한이 있는 경우에도 *리포지토리를 포크하고 복제하는 것이 좋습니다(이 가이드에서 이렇게 가정)*. 그러면 포크에서 제안된 변경 내용을 저장하기 위한 읽기/쓰기 권한이 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="9ebe3-110">Windows에 Git 클라이언트 도구 설치</span><span class="sxs-lookup"><span data-stu-id="9ebe3-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="9ebe3-111">최신 버전의 [Software Freedom Conservancy Git 클라이언트 도구](https://git-scm.com/download/)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="9ebe3-112">설치에는 Git 버전 제어 시스템 및 로컬 Git 리포지토리와 상호 작용하는 데 사용하는 명령줄 앱인 Git Bash가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="9ebe3-113">CLI(명령줄 인터페이스)보다 GUI(그래픽 사용자 인터페이스)를 선호하는 경우 [Software Freedom Conservancy의 사용 가능한 GUI 클라이언트 페이지](https://git-scm.com/downloads/guis), [GitHub의 GitHub 데스크톱](https://desktop.github.com/) 또는 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)에서 인기 있는 옵션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="9ebe3-114">설치 및 구성에 대해 선택한 클라이언트의 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="9ebe3-115">다음 문서에서는 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="9ebe3-116">사용 가능한 추가 Git 리소스는 다음과 같습니다. [Git terminology](https://help.github.com/articles/github-glossary)(Git 용어) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)(Git 기본 사항) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)(Git 및 GitHub 알아보기)</span><span class="sxs-lookup"><span data-stu-id="9ebe3-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="9ebe3-117">Markdown 편집기 이해</span><span class="sxs-lookup"><span data-stu-id="9ebe3-117">Understand Markdown editors</span></span>

<span data-ttu-id="9ebe3-118">Markdown은 읽기 쉽고 배우기 쉬운 가벼운 마크업 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="9ebe3-119">따라서 빠르게 업계 표준이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="9ebe3-120">Markdown으로 문서를 작성하려면 먼저 Markdown 편집기를 다운로드하고 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="9ebe3-121">[Visual Studio Code](https://code.visualstudio.com/)는 Microsoft에서 Markdown 편집에 선호하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="9ebe3-122">[Atom](https://atom.io)은 Markdown을 편집하는 데 사용되는 또 다른 인기 있는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="9ebe3-123">Markdown 텍스트는 확장명이 .md인 파일에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="9ebe3-124">OPS 사용자 지정 Markdown 확장에서 지원하는 Markdown 기본 사항 및 기능을 포함하여 Markdown으로 작성하는 방법에 대한 추가 내용은 나중에 [Markdown 사용 방법](how-to-write-use-markdown.md) 문서에서 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="9ebe3-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9ebe3-125">Visual Studio Code</span></span>

<span data-ttu-id="9ebe3-126">[Visual Studio Code](https://code.visualstudio.com/)(VS Code라고도 함)는 Windows, Linux 및 Mac에서 작동하는 경량 편집기입니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="9ebe3-127">여기에는 Git 통합 및 확장에 대한 지원이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="9ebe3-128">[VS Code](https://code.visualstudio.com/)를 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="9ebe3-129">VS Code 홈페이지에서 사용자의 운영 체제를 올바르게 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="9ebe3-130">Windows</span><span class="sxs-lookup"><span data-stu-id="9ebe3-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="9ebe3-131">Mac</span><span class="sxs-lookup"><span data-stu-id="9ebe3-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="9ebe3-132">Linux</span><span class="sxs-lookup"><span data-stu-id="9ebe3-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="9ebe3-133">VS Code를 시작하고 현재 폴더를 열려면 명령줄 또는 Bash 셸에서 `code .` 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="9ebe3-134">현재 폴더가 로컬 Git 리포지토리의 일부인 경우 GitHub 통합이 Visual Studio Code에 자동으로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9ebe3-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="9ebe3-135">Next steps</span></span>

<span data-ttu-id="9ebe3-136">이제 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9ebe3-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
