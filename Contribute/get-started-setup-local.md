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
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "72288599"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>설명서를 위한 Git 리포지토리 로컬로 설정

이 문서에서는 Microsoft 설명서에 참가하기 위해 로컬 컴퓨터에서 Git 리포지토리를 설정하는 단계를 설명합니다. 참가자는 로컬로 복제된 리포지토리를 사용하여 새 문서를 추가하거나, 기존 문서에 대해 주요 편집 작업을 수행하거나, 아트워크를 변경할 수 있습니다.

이러한 일회성 설정 활동을 실행하여 다음과 같은 참가를 시작합니다.
> [!div class="checklist"]
> * 적절한 리포지토리 확인
> * GitHub 계정에 리포지토리 포크
> * 복제된 파일의 로컬 폴더 선택
> * 로컬 컴퓨터에 리포지토리 복제
> * 업스트림 원격 값 구성

> [!IMPORTANT]
> 문서의 사소한 내용만 변경하는 경우 이 문서의 단계를 완료하지 *않아도* 됩니다. 바로 [빠른 변경 내용 워크플로](index.md#quick-edits-to-existing-documents)를 계속할 수 있습니다.
>

## <a name="overview"></a>개요

Microsoft의 설명서 사이트에 참여하려면 해당 설명서 리포지토리를 복제하여 Markdown 파일을 로컬로 만들고 편집하면 됩니다. Microsoft에서는 제안된 변경 내용을 저장하기 위한 읽기/쓰기 권한이 있도록 적절한 리포지토리를 고유의 GitHub 계정에 포크하도록 요구합니다. 그런 다음, 끌어오기 요청을 사용하여 변경 내용을 읽기 전용 중앙 공유 리포지토리에 병합합니다.

![GitHub Triangle](./media/git-and-github-initial-setup.png)

GitHub에 익숙하지 않은 경우 아래 비디오를 시청하고 분기 및 복제 프로세스 개념에 대해 간략히 알아보세요.

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>리포지토리 확인

[docs.microsoft.com](https://docs.microsoft.com)에 호스트된 설명서는 [github.com](https://www.github.com)의 다양한 리포지토리에 있습니다.

1. 사용할 리포지토리를 잘 모르는 경우 웹 브라우저를 사용하여 [docs.microsoft.com](https://docs.microsoft.com)에 있는 문서를 방문합니다. 문서의 오른쪽 위에 있는 **편집** 링크(연필 아이콘)를 선택합니다.

   ![편집을 클릭하여 리포지토리 및 파일 위치를 확인합니다.](media/index/edit-article.png)

2. 해당 링크를 사용하면 적절한 리포지토리에 있는 해당 Markdown 파일에 대한 github.com 위치로 이동합니다. URL에 주목하여 리포지토리 이름을 확인합니다.

   ![URL에 주목하여 리포지토리 위치를 확인합니다.](media/public-repo.png)

   예를 들어 다음과 같은 인기 있는 리포지토리는 공공의 참가가 가능합니다.
   - Azure 설명서 [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - SQL Server 설명서 [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Visual Studio 설명서 [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - .NET 설명서 [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Azure .Net SDK 설명서 [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   - ConfigMgr 설명서 [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)

## <a name="fork-the-repository"></a>리포지토리 포크
GitHub 웹 사이트를 통해 적절한 리포지토리를 사용하여 자신의 GitHub 계정에 리포지토리 포크를 만듭니다.

모든 기본 문서 리포지토리는 읽기 전용 액세스를 제공하므로 개인 포크가 필요합니다. 변경하려면 [끌어오기 요청](git-github-fundamentals.md#pull-requests)을 포크에서 기본 리포지토리로 제출해야 합니다. 이 프로세스를 용이하게 하려면 먼저 쓰기 액세스 권한이 있는 리포지토리의 복사본이 필요합니다. GitHub *포크*로 이 작업을 수행할 수 있습니다.

1. 기본 리포지토리의 GitHub 페이지로 이동하여 오른쪽 상단의 **포크** 단추를 클릭합니다.

   ![GitHub 프로필 예제](./media/contribute-get-started-setup-local/fork.png)

2. 메시지가 표시되면 포크를 만들 대상으로 GitHub 계정 타일을 선택합니다. 이 프롬프트는 GitHub 계정 내에서 포크라고 하는 리포지토리의 복사본을 만듭니다.

## <a name="choose-a-local-folder"></a>로컬 폴더 선택
리포지토리의 복사본을 로컬로 보관할 로컬 폴더를 만듭니다. 일부 리포지토리는 클 수 있습니다(예: azure-docs의 경우 최대 5GB). 사용 가능한 디스크 공간이 있는 위치를 선택합니다.

1. 기억하고 입력하기 쉬운 폴더 이름을 선택합니다. 예를 들어 `C:\docs\` 루트 폴더를 고려하거나 `~/Documents/docs/` 사용자 프로필 디렉터리에 폴더를 만듭니다.

   > [!IMPORTANT]
   > 다른 git 리포지토리 폴더 위치 안에 중첩된 로컬 폴더 경로는 선택하지 마세요. 복제된 git 폴더를 서로 인접하여 저장하도록 허용되지만 서로의 내부에 git 폴더가 중첩되면 파일 추적 오류가 발생합니다.

2. Git Bash 시작

   ![Git Bash 시작](./media/contribute-get-started-setup-local/gitbash-start.png)

   Git Bash가 시작되는 기본 위치는 일반적으로 Windows OS의 홈 디렉터리(~) 또는 `/c/users/<Windows-user-account>/`입니다.

   현재 디렉터리를 확인하려면 $ 프롬프트에서 `pwd`를 입력합니다. 

3. 리포지토리를 로컬로 호스팅하기 위해 만든 폴더로 디렉터리를 변경합니다(cd). Git Bash는 폴더 경로에 백슬래시 대신 슬래시를 사용하는 Linux 규칙을 사용합니다.

   예를 들어 `cd /c/docs/ ` 또는 `cd ~/Documents/docs/`와 같습니다.

## <a name="create-a-local-clone"></a>로컬 복제 만들기

Git Bash를 사용하는 경우 **clone** 명령을 실행하여 리포지토리(포크)의 복사본을 현재 디렉터리의 디바이스로 끌어오도록 준비합니다. 

### <a name="authenticate-by-using-git-credential-manager"></a>Git 자격 증명 관리자를 사용하여 인증
Windows용 Git의 최신 버전을 설치하고 기본 설치에 동의한 경우 기본적으로 Git 자격 증명 관리자가 사용됩니다. Git 자격 증명 관리자에서는 GitHub에서 인증된 연결 및 원격을 다시 설정할 때 개인용 액세스 토큰을 다시 호출할 필요가 없으므로 인증을 훨씬 간단하게 수행할 수 있습니다.

1. 리포지토리 이름을 제공하여 **clone** 명령을 실행합니다. 복제는 로컬 컴퓨터에서 포크된 리포지토리를 다운로드(복제)합니다. 

    > [!Tip]
    > GitHub UI의 **복제 또는 다운로드** 단추를 누르면 복제 명령에 대한 포크의 GitHub URL을 확인할 수 있습니다.
    >
    > ![복제 또는 다운로드](./media/contribute-get-started-setup-local/clone-or-download.png)

    복제를 진행하는 동안 포크를 만든 기본 리포지토리가 아닌 *포크*에 대한 경로를 지정하도록 합니다. 그렇지 않으면 변경 내용을 제공할 수 없습니다. 포크는 개인 GitHub 사용자 계정(예: `github.com/<github-username>/<repo>`)을 통해 참조됩니다.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    복제 명령은 다음 예제와 비슷하게 표시됩니다.

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. 메시지가 표시되면 GitHub 자격 증명을 입력합니다.

    ![GitHub 로그인](./media/contribute-get-started-setup-local/github-login.png)

3. 메시지가 표시되면 2단계 인증 코드를 입력합니다.

    ![GitHub 2단계 인증](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > 자격 증명은 저장된 다음 나중에 GitHub 요청을 인증하는 데 사용됩니다. 이 인증은 컴퓨터마다 한 번만 수행해야 합니다. 

4. clone 명령은 포크에서 로컬 디스크의 새 폴더로 리포지토리 파일 복사본을 실행하고 다운로드합니다. 현재 폴더 내에 새 폴더가 만들어집니다. 리포지토리 크기에 따라 몇 분 정도 걸릴 수 있습니다. 폴더가 완성되면 폴더를 탐색하여 구조를 볼 수 있습니다.

## <a name="configure-remote-upstream"></a>원격 업스트림 구성
리포지토리가 복제되면 **upstream**이라는 기본 리포지토리에 읽기 전용 원격 연결을 설정합니다. 업스트림 URL을 사용하면 로컬 리포지토리를 다른 사용자가 수행한 최근 변경 내용과 동기화된 상태로 유지됩니다. **git remote** 명령은 구성 값을 설정하는 데 사용됩니다. **fetch** 명령을 사용하여 업스트림 리포지토리에서 분기 정보를 새로 고칩니다.

1. **Git 자격 증명 관리자**를 사용하는 경우 다음 명령을 사용합니다. \<repo\> 및 \<organization\> 자리 표시자를 바꿉니다.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. 구성된 값을 보고 URL이 올바른지 확인합니다. **원본** URL이 개인 포크를 가리키는지 확인합니다. **업스트림** URL이 MicrosoftDocs 또는 Azure와 같은 기본 리포지토리를 가리키는지 확인합니다. 
   ```bash
   git remote -v 
   ```

   원격 출력 예제가 표시됩니다. MyGitAccount라는 가상의 git 계정은 개인 액세스 토큰을 사용하여 azure-docs 리포지토리에 액세스하도록 구성됩니다.
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. 실수한 경우 원격 값을 제거할 수 있습니다. upstream 값을 제거하려면 `git remote remove upstream` 명령을 실행합니다.

## <a name="next-steps"></a>다음 단계
- 콘텐츠를 추가하고 업데이트하는 방법에 대해 자세히 알아보려면 [GitHub 참여 워크플로](how-to-write-workflows-major.md) 페이지로 계속 진행하세요.
