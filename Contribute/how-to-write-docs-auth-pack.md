---
title: Visual Studio Code용 Docs Authoring Pack
description: 이 문서에서는 docs.microsoft.com용 Markdown 작성을 용이하게 하는 Visual Studio Code 확장 팩을 설명합니다.
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 00afafbbf16096ac6433c0ab276578d8d9084b51
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805657"
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code용 Docs Authoring Pack

Docs Authoring Pack은 docs.microsoft.com용 Markdown 작성을 지원하는 Visual Studio Code 확장 모음입니다. 이 팩은 [VS Code Marketplace에서 사용](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)할 수 있으며 포함된 확장은 다음과 같습니다.

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): David Anson이 개발한 인기 있는 Markdown linter이며, Markdown에서 모범 사례를 따르도록 보장합니다.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)(Code 맞춤법 검사기): Street Side Software에서 제공하는 완전한 오프라인 맞춤법 검사기입니다.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): 사용자 지정 Markdown을 포함하여 보다 정확한 Markdown 미리 보기를 위해 docs.microsoft.com CSS를 사용합니다.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): OPS(Open Publishing System)의 기본 Markdown 지원 및 사용자 지정 Markdown 구문 지원을 포함하여 OPS의 docs.microsoft.com 콘텐츠에 대한 Markdown 작성 지원을 제공합니다. 이 항목의 나머지 부분에서는 Docs Markdown 확장에 대해 설명합니다.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)(Docs 문서 템플릿): 사용자가 Markdown 스켈레톤 콘텐츠를 새 파일에 적용할 수 있습니다.

## <a name="prerequisites-and-assumptions"></a>필수 조건 및 가정

Docs Markdown 확장을 사용하여 상대 링크, 이미지 및 기타 포함된 콘텐츠를 정확하게 삽입하려면, VS Code 작업 영역을 복제된 OPS(Open Publishing System) 리포지토리의 루트 범위로 지정해야 합니다.

경고 및 코드 조각과 같이 확장에서 지원하는 일부 구문은 OPS용 사용자 지정 Markdown이며, OPS를 통해 게시하지 않으면 올바르게 렌더링되지 않습니다.

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown 확장을 사용하는 방법

Docs Markdown 메뉴에 액세스하려면 `ALT+M`을 입력합니다. 위쪽/아래쪽 화살표를 클릭하거나 사용하여 원하는 함수를 선택하거나, 입력하여 필터링을 시작하고 원하는 함수가 메뉴에서 강조 표시되면 `ENTER` 키를 누릅니다. 다음을 사용할 수 있습니다.

|기능     |설명           |
|-------------|----------------------|
|미리 보기      |Docs Preview 확장을 사용하여 나란히 있는 창에서 활성 항목을 미리 봅니다. 이 옵션은 Docs Preview가 설치된 경우에만 사용할 수 있습니다.|
|굵게         |텍스트를 **굵게** 서식으로 지정합니다.|
|기울임꼴       |텍스트를 *기울임꼴* 서식으로 지정합니다.|
|코드         |한 줄 이하가 선택되면 텍스트를 `inline code` 서식으로 지정합니다.<br><br>여러 줄이 선택되면 울타리가 있는 코드 블록으로 서식을 지정하고, 필요에 따라 OPS에서 지원하는 프로그래밍 언어를 선택할 수 있습니다.|
|경고        |메모, 중요, 경고 또는 팁을 삽입합니다.<br><br>메뉴에서 [경고]를 선택한 다음, 경고 유형을 선택합니다. 이전에 텍스트를 선택한 경우 해당 텍스트가 선택한 경고 구문으로 둘러싸입니다. 텍스트를 선택하지 않은 경우 자리 표시자 텍스트와 함께 새 경고가 추가됩니다.|
|번호 매기기 목록|새 번호 매기기 목록을 삽입합니다.<br><br> 여러 줄이 선택되면 각 줄이 목록 항목이 됩니다. 번호 매기기 목록은 Markdown에서 모두 1로 표시되지만, docs.microsoft.com에서 일련 번호로 또는 중첩된 목록의 경우 문자로 렌더링됩니다. 중첩된 번호 매기기 목록을 만들려면 부모 목록 내에 있는 탭을 선택합니다.|
|글머리 기호 목록|새 글머리 기호 목록을 삽입합니다.|
|테이블        |Markdown 테이블 구조를 삽입합니다.<br><br>테이블 명령이 선택되면 열과 행의 수를 3:4와 같이 열 수:행 수 형식으로 지정합니다. 이 확장을 통해 지정할 수 있는 최대 열 수는 5개이며 가독성을 높이는 데 권장되는 최댓값입니다.|
|리포지토리의 파일에 연결|동일한 리포지토리에 있는 다른 파일에 대한 상대 링크를 삽입합니다. 이 옵션이 선택되면 명령 창에 입력하여 파일 이름별로 파일을 필터링한 다음, 원하는 파일을 선택합니다. 이전에 텍스트를 선택한 경우에는 이 텍스트가 링크 텍스트가 됩니다. 텍스트를 선택하지 않은 경우 대상 파일의 H1이 링크 텍스트로 사용됩니다.|
|웹 페이지에 연결    |웹 페이지에 대한 링크를 삽입합니다. 이 옵션을 선택한 후 명령 창에 URI를 붙여넣거나 입력합니다. `https://`는 필수입니다. 이전에 텍스트를 선택한 경우에는 이 텍스트가 링크 텍스트가 됩니다. 텍스트를 선택하지 않은 경우 URI가 링크 텍스트로 사용됩니다.|
|제목에 연결     |리포지토리의 현재 파일이나 다른 파일에 있는 책갈피에 연결합니다.<br>`Bookmark in this file`: 현재 파일의 제목 목록에서 선택하여 올바른 형식의 책갈피를 삽입합니다.<br>`Bookmark in another file`: 먼저 파일 이름별로 필터링하고, 연결할 파일을 선택한 다음, 선택한 파일 내에서 적절한 제목을 선택합니다.|
|이미지        |대체 텍스트(내게 필요한 옵션에 필요)를 입력하고, 선택한 다음, 이 명령을 호출하여 리포지토리에서 지원되는 이미지 파일 목록을 필터링하고 원하는 파일을 선택합니다. 이 명령을 호출할 때 대체 텍스트를 선택하지 않은 경우 이미지 파일을 선택하기 전에 해당 텍스트를 입력하라는 메시지가 표시됩니다.|
|포함      |현재 파일에 포함할 파일을 찾습니다.|
|코드 조각      |리포지토리에서 현재 파일에 포함할 코드 조각을 찾습니다.|
|비디오        |포함된 비디오를 추가합니다.|
|템플릿     |새 파일을 만들고 Markdown 템플릿을 적용합니다. 자세한 내용은 아래 [템플릿](#how-to-use-docs-templates)을 참조하세요.|

## <a name="how-to-assign-keyboard-shortcuts"></a>바로 가기 키를 할당하는 방법

1. `CTRL+K`, `CTRL+S`를 차례로 입력하여 바로 가기 키 목록을 엽니다.
1. 사용자 지정 키 바인딩을 만들려는 명령(예: `formatBold`)을 검색합니다.
1. 줄 위로 마우스를 가져가면 명령 이름 근처에 표시되는 더하기 기호를 클릭합니다.
1. 새 입력 상자가 표시되면 해당 특정 명령에 바인딩하려는 바로 가기 키를 입력합니다. 예를 들어 '굵게'에 대한 일반 바로 가기를 사용하려면 `ctrl+b`를 입력합니다.
1. Markdown이 아닌 파일에서 사용할 수 없도록 키 바인딩에 `when` 절을 삽입하는 것이 좋습니다. 이렇게 하려면 *keybindings.json*을 열고 명령 이름 아래에 다음 줄을 삽입합니다(줄 사이에 쉼표를 추가해야 함).
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    keybindings.json에서 완성된 사용자 지정 키 바인딩은 다음과 같이 표시됩니다.

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. keybindings.json을 저장합니다.

자세한 내용은 VS Code Docs의 [키 바인딩](https://code.visualstudio.com/docs/getstarted/keybindings)을 참조하세요.

## <a name="how-to-show-the-legacy-toolbar"></a>레거시 도구 모음을 표시하는 방법

Docs Markdown 확장이 설치되면 이 확장의 시험판 버전 사용자에게 더 이상 제작 도구 모음이 VS Code 창 아래쪽에 표시되지 않습니다. 이는 VS Code 상태 표시줄에서 도구 모음이 많은 공간을 차지하고 확장 UX에 대한 모범 사례를 따르지 않았기 때문에 새 확장에서 더 이상 사용되지 않습니다. 그러나 필요에 따라 다음과 같이 VS Code settings.json 파일을 업데이트하여 도구 모음을 표시할 수도 있습니다.

1. VS Code에서 파일 -> 기본 설정 -> 설정(`CTRL+Comma`)으로 차례로 이동합니다.
1. [사용자 설정]을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나, [작업 영역 설정]을 변경하여 현재 작업 영역에 대해서만 변경합니다.
1. [기본 설정] 창에서 [Docs 제작 확장 구성]을 찾고, 원하는 설정 옆에 있는 연필 아이콘을 선택합니다. 다음으로, `true` 또는 `false` 중 하나를 선택하라는 메시지가 표시됩니다. 선택이 완료되면 VS Code에서 자동으로 settings.json 파일에 값을 추가하고, 변경 내용을 적용하기 위해 창을 다시 로드하라는 메시지가 표시됩니다.

## <a name="how-to-use-docs-templates"></a>Docs 템플릿을 사용하는 방법

Docs 문서 템플릿은 VS Code 작성자가 중앙 저장소의 Markdown 템플릿을 가져와서 파일에 적용할 수 있습니다. 템플릿은 필수 메타데이터가 문서에 포함되어 있는지, 콘텐츠 표준을 따랐는지 등을 확인하는 데 도움이 될 수 있습니다. 템플릿은 공용 GitHub 리포지토리에 Markdown 파일로 관리됩니다.

### <a name="to-apply-a-template-in-vs-code"></a>VS Code의 템플릿을 적용하려면

1. Docs Markdown 확장을 설치하지 않은 경우 F1 키를 눌러 명령 팔레트를 열고, 필터링할 “템플릿” 입력을 시작한 다음, `Docs: Template`을 클릭합니다. Docs Markdown을 설치한 경우 명령 팔레트를 사용하거나 `Alt+M`을 클릭하여 Docs Markdown QuickPick 메뉴를 표시한 다음, 목록에서 `Template`을 선택합니다.
1. 표시되는 목록에서 원하는 템플릿을 선택합니다.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>GitHub ID 및/또는 Microsoft 별칭을 VS Code 설정에 추가하려면

템플릿 확장은 세 가지 동적 메타데이터 필드(author, ms.author, ms.date)를 지원합니다. 즉, 템플릿 작성자가 Markdown 템플릿의 메타데이터 헤더에 이러한 필드를 사용하는 경우 템플릿을 적용하면 다음과 같이 필드가 파일에 자동으로 채워집니다.

|메타데이터  |값|
|----------|---------------|
|author    |VS Code 설정 파일에 지정한 경우 해당 GitHub ID.|
|ms.author |VS Code 설정 파일에 지정한 경우 해당 Microsoft 별칭. Microsoft 직원이 아닌 경우 지정되지 않은 채로 두세요.|
|ms.date   |Docs 지원 형식, MM/DD/YYYY의 현재 날짜. 이후에 파일을 업데이트하면 날짜가 자동으로 업데이트되지 않습니다. docs.microsoft.com 사이트에서 가장 최근의 게시 날짜를 나타내기 위해 ms.date 값을 수동으로 업데이트해야 합니다.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>author(GitHub ID) 및/또는 ms.author(Microsoft 별칭)를 설정하려면

1. VS Code에서 파일 -> 기본 설정 -> 설정(`CTRL+Comma`)으로 차례로 이동합니다.
1. [사용자 설정]을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나, [작업 영역 설정]을 선택하여 현재 작업 영역에 대한 설정만 변경합니다.
1. 왼쪽에 있는 [기본 설정] 창에서 Docs 문서 템플릿 확장 구성을 찾은 다음, 원하는 설정 옆에 있는 연필 아이콘을 클릭하고 [설정에서 바꾸기]를 클릭합니다.
1. [사용자 설정] 창이 나란히 열리고 맨 아래에 새 항목이 표시됩니다.
1. GitHub ID 또는 Microsoft 메일 별칭을 적절하게 추가하고 파일을 저장합니다.
1. 변경 사항을 적용하기 위해 VS Code를 닫고 다시 시작해야 할 수도 있습니다.
1. 이제 동적 필드를 사용하는 템플릿을 적용하면 GitHub ID 및/또는 Microsoft 별칭이 메타데이터 헤더에 자동으로 채워집니다.
