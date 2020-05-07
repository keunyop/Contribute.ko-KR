---
title: 콘텐츠 작성 도구 설치
description: 이 문서의 정보를 활용하여 Git 및 Markdown 파일 편집에 필요한 클라이언트 도구를 다운로드하고 설치할 수 있습니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
ms.openlocfilehash: ba7e511d756f43acfa5cfbbd228f793d7fbce727
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78331863"
---
# <a name="install-content-authoring-tools"></a>콘텐츠 작성 도구 설치

이 문서에서는 Git 클라이언트 도구 및 Visual Studio Code를 대화형으로 설치하는 단계를 설명합니다.
> [!div class="checklist"]
> * [Git](https://git-scm.com/) 설치
> * [Visual Studio Code](https://code.visualstudio.com/) 설치
> * [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 설치

>[!IMPORTANT]
> 아티클에서 사소한 내용을 변경하려는 경우 이 아티클의 단계를 완료할 필요 *없이* 바로 [빠른 변경 워크플로](index.md#quick-edits-to-existing-documents)를 계속 진행할 수 있습니다.
>
> 주요 참가자는 [중요한/장기 실행 변경 워크플로](how-to-write-workflows-major.md)를 사용할 수 있도록 이러한 단계를 완료하는 것이 좋습니다. 기본 리포지토리에 대한 쓰기 권한이 있는 경우에도 *리포지토리를 포크하고 복제하는 것이 좋습니다(이 가이드에서 이렇게 가정)* . 그러면 포크에서 제안된 변경 내용을 저장하기 위한 읽기/쓰기 권한이 있게 됩니다.

## <a name="install-git-client-tools"></a>Git 클라이언트 도구 설치 

 해당 플랫폼용 최신 버전의 [Software Freedom Conservancy Git 클라이언트 도구](https://git-scm.com/download/)를 설치합니다. 

* [Windows용 Git](https://git-scm.com/download/win). 이 설치에는 Git 버전 제어 시스템 및 로컬 Git 리포지토리와 상호 작용하는 데 사용하는 명령줄 앱인 Git Bash가 포함됩니다.
* Mac용 Git은 Xcode 명령줄 도구의 일부로 제공됩니다. 명령줄에서 `git`을 실행하면 됩니다. 필요한 경우 명령줄 도구를 설치하라는 메시지가 표시됩니다. Software Freedom Conservancy에서 [Mac용 Git](https://git-scm.com/download/mac)을 다운로드할 수도 있습니다.
* [Linux 및 Unix용 Git](https://git-scm.com/download/linux)

CLI(명령줄 인터페이스)보다 GUI(그래픽 사용자 인터페이스)를 선호하는 경우 [Software Freedom Conservancy의 사용 가능한 GUI 클라이언트 페이지](https://git-scm.com/downloads/guis), [GitHub의 GitHub 데스크톱](https://desktop.github.com/) 또는 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)에서 인기 있는 옵션을 참조하세요.

설치 및 구성에 대해 선택한 클라이언트의 지침을 따르세요.

다음 문서에서는 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)합니다.

   사용 가능한 추가 Git 리소스는 다음과 같습니다. [Git terminology](https://help.github.com/articles/github-glossary)(Git 용어) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)(Git 기본 사항) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)(Git 및 GitHub 알아보기)

## <a name="understand-markdown-editors"></a>Markdown 편집기 이해

Markdown은 읽기 쉽고 배우기 쉬운 가벼운 마크업 언어입니다. 따라서 빠르게 업계 표준이 되었습니다. Markdown으로 문서를 작성하려면 먼저 Markdown 편집기를 다운로드하고 설치하는 것이 좋습니다.  [Visual Studio Code](https://code.visualstudio.com/)는 Microsoft에서 Markdown 편집에 선호하는 도구입니다. [Atom](https://atom.io)은 Markdown을 편집하는 데 사용되는 또 다른 인기 있는 도구입니다.

Markdown 텍스트는 확장명이 .md인 파일에 저장됩니다.

Markdown 기본 사항과 OPS(Open Publishing Services) 사용자 지정 Markdown 확장에서 지원하는 기능을 포함하여 Markdown으로 작성하는 방법에 대한 추가 세부 정보는 [Markdown 참조](markdown-reference.md) 문서에서 다룹니다.

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/)(VS Code라고도 함)는 Windows, Linux 및 Mac에서 작동하는 경량 편집기입니다. 여기에는 Git 통합 및 확장에 대한 지원이 포함됩니다.

[VS Code](https://code.visualstudio.com/)를 다운로드하고 설치합니다. VS Code 홈페이지에서 사용자의 운영 체제를 올바르게 검색합니다.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> VS Code를 시작하고 현재 폴더를 열려면 명령줄 또는 Bash 셸에서 `code .` 명령을 실행합니다. 현재 폴더가 로컬 Git 리포지토리의 일부인 경우 GitHub 통합이 Visual Studio Code에 자동으로 나타납니다.

## <a name="docs-authoring-pack"></a>Docs Authoring Pack
Visual Studio Code용 Docs Authoring Pack을 설치합니다. 이 확장 집합에는 Markdown 작성 시 도움이 되는 기본 작성 지원과 미리 보기 기능이 포함되므로, Markdown 모양을 docs.microsoft.com 사이트의 스타일로 볼 수 있습니다.

   이 [Marketplace 페이지](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)를 방문하고 **설치**를 선택하거나 VS Code 창의 확장 목록에서 `docsmsft.docs-authoring-pack`을 검색합니다. 

   Docs Authoring Pack은 VS Code 내에서 Alt+M을 눌러서 액세스할 수 있습니다. 도구 모음은 기본적으로 숨겨져 있지만 표시할 수 있습니다. VS Code 설정(Control+쉼표) 및 사용자 추가 설정 `"markdown.showToolbar": true`을 편집하여 도구 모음을 표시합니다.

   자세한 내용은 [Docs Authoring Pack](how-to-write-docs-auth-pack.md) 페이지를 참조하세요.


## <a name="next-steps"></a>다음 단계

이제 [로컬 Git 리포지토리를 설정](get-started-setup-local.md)할 준비가 되었습니다.
