---
title: VS Code용 Docs Authoring Pack
description: 이 문서에서는 docs.microsoft.com용 Markdown 작성을 용이하게 하는 VS Code 확장 팩을 설명합니다.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d0d61db2faf88598ecd2c800fb5fbe8df8ec44f5
ms.sourcegitcommit: 7b668124f25b8ad0442937a3ad05b19a47af5970
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/03/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code용 Docs Authoring Pack

Docs Authoring Pack은 docs.microsoft.com용 Markdown 작성을 지원하는 VS Code 확장 모음입니다. 이 팩은 [VS Code Marketplace에서 사용](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)할 수 있으며 포함된 확장은 다음과 같습니다.

- **DocFx:** docs.microsoft.com 관련 Markdown 미리 보기를 제공합니다. 자세한 내용은 [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX)를 참조하세요.
- **markdownlint:** David Anson이 개발한 인기 있는 Markdown Linter이며, Markdown에서 모범 사례를 따르도록 보장합니다. 자세한 내용은 [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)를 참조하세요.
- **Docs Markdown:** OPS(Open Publishing System)의 기본 Markdown 지원 및 사용자 지정 Markdown 구문 지원을 포함하여 OPS의 docs.microsoft.com 콘텐츠에 대한 Markdown 작성 지원을 제공합니다. 이 항목의 나머지 부분에서는 Docs Markdown 확장에 대해 설명합니다.

## <a name="prerequisites-and-assumptions"></a>필수 조건 및 가정

Docs Markdown 확장을 사용하여 상대 링크, 이미지 및 기타 포함된 콘텐츠를 정확하게 삽입하려면, VS Code 작업 영역을 복제된 OPS 리포지토리의 루트 범위로 지정해야 합니다.

경고 및 코드 조각과 같이 확장에서 지원하는 일부 구문은 OPS용 사용자 지정 Markdown이며, OPS를 통해 게시하지 않으면 올바르게 렌더링되지 않습니다.

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown 확장을 사용하는 방법

Docs Markdown 메뉴에 액세스하려면 `ALT+M`을 입력합니다. 위쪽/아래쪽 화살표를 클릭하거나 사용하여 원하는 함수를 선택하거나, 입력하여 필터링을 시작하고 원하는 함수가 메뉴에서 강조 표시되면 `ENTER` 키를 누릅니다. 다음을 사용할 수 있습니다.

|기능     |명령             |설명           |
|-------------|--------------------|----------------------|
|굵게         |`formatBold`        |텍스트를 **굵게** 서식으로 지정합니다.|
|기울임꼴       |`formatItalic`      |텍스트를 *기울임꼴* 서식으로 지정합니다.|
|코드         |`formatCode`        |한 줄 이하가 선택되면 텍스트를 `inline code` 서식으로 지정합니다.<br><br>여러 줄이 선택되면 울타리가 있는 코드 블록으로 서식을 지정하고, 필요에 따라 OPS에서 지원하는 프로그래밍 언어를 선택할 수 있습니다.|
|경고        |`insertAlert`       |메모, 중요, 경고 또는 팁을 삽입합니다.<br><br>메뉴에서 [경고]를 선택한 다음, 경고 유형을 선택합니다. 이전에 텍스트를 선택한 경우 해당 텍스트가 선택한 경고 구문으로 둘러싸입니다. 텍스트를 선택하지 않은 경우 자리 표시자 텍스트와 함께 새 경고가 추가됩니다.|
|번호 매기기 목록|`insertNumberedList` |새 번호 매기기 목록을 삽입합니다.<br><br> 여러 줄이 선택되면 각 줄이 목록 항목이 됩니다. 번호 매기기 목록은 Markdown에서 모두 1로 표시되지만, docs.microsoft.com에서 일련 번호로 또는 중첩된 목록의 경우 문자로 렌더링됩니다. 중첩된 번호 매기기 목록을 만들려면 부모 목록 내에 있는 탭을 선택합니다.|
|글머리 기호 목록|`insertBulletedList` |새 글머리 기호 목록을 삽입합니다.|
|테이블        |`insertTable`        |Markdown 테이블 구조를 삽입합니다.<br><br>테이블 명령이 선택되면 열과 행의 수를 3:4와 같이 열 수:행 수 형식으로 지정합니다. 이 확장을 통해 지정할 수 있는 최대 열 수는 5개이며 가독성을 높이는 데 권장되는 최댓값입니다.|
|링크         |`selectLinkType`      |링크를 삽입합니다. 이 명령이 선택되면 표시되는 하위 메뉴는 다음과 같습니다.<br><br>`External`: URI를 통해 웹 페이지에 연결합니다. "http" 또는 "https"가 포함되어야 합니다.<br>`Internal`: 동일한 리포지토리에 있는 다른 파일에 대한 상대 링크를 삽입합니다. 이 옵션이 선택되면 명령 창에 입력하여 파일 이름별로 파일을 필터링한 다음, 원하는 파일을 선택합니다. <br>`Bookmark in this file`: 현재 파일의 제목 목록에서 선택하여 올바른 형식의 책갈피를 삽입합니다.<br>`Bookmark in another file`: 먼저 파일 이름별로 필터링하고, 연결할 파일을 선택한 다음, 선택한 파일 내에서 적절한 제목을 선택합니다.|
|이미지        |`insertImage`     |대체 텍스트(내게 필요한 옵션에 필요)를 입력하고, 선택한 다음, 이 명령을 호출하여 리포지토리에서 지원되는 이미지 파일 목록을 필터링하고 원하는 파일을 선택합니다. 이 명령을 호출할 때 대체 텍스트를 선택하지 않은 경우 이미지 파일을 선택하기 전에 해당 텍스트를 입력하라는 메시지가 표시됩니다.|
|포함      |`insertInclude`   |현재 파일에 포함할 파일을 찾습니다.|
|코드 조각      |`insertSnippet`   |리포지토리에서 현재 파일에 포함할 코드 조각을 찾습니다.|
|비디오        |`insertVideo`     |포함된 비디오를 추가합니다.|
|미리 보기      |`previewTopic`    |DocFX 확장을 사용하여 나란히 있는 창에서 활성 항목을 미리 봅니다.  DocFX 확장이 설치되어 있지 않거나 설치되어 있지만 사용할 수 없는 경우 해당 항목이 렌더링되지 않습니다.


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

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>레거시 "Gauntlet" 도구 모음을 표시하는 방법

Docs Markdown 확장이 설치되면 "Gauntlet"이라는 확장 코드의 이전 사용자는 더 이상 제작 도구 모음이 VS Code 창 아래쪽에 표시되지 않는다는 사실을 알게 됩니다. 이는 VS Code 상태 표시줄에서 도구 모음이 많은 공간을 차지하고 확장 UX에 대한 모범 사례를 따르지 않았기 때문에 새 확장에서 더 이상 사용되지 않습니다. 그러나 필요에 따라 다음과 같이 VS Code settings.json 파일을 업데이트하여 도구 모음을 표시할 수도 있습니다.

1. VS Code에서 파일 -> 기본 설정 -> 설정(`CTRL+Comma`)으로 차례로 이동합니다.
1. [사용자 설정]을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나, [작업 영역 설정]을 변경하여 현재 작업 영역에 대해서만 변경합니다.
1. [기본 설정] 창에서 [Docs 제작 확장 구성]을 찾고, 원하는 설정 옆에 있는 연필 아이콘을 선택합니다. 다음으로, `true` 또는 `false` 중 하나를 선택하라는 메시지가 표시됩니다. 선택이 완료되면 VS Code에서 자동으로 settings.json 파일에 값을 추가하고, 변경 내용을 적용하기 위해 창을 다시 로드하라는 메시지가 표시됩니다.

## <a name="known-issues"></a>알려진 문제

- DocFX 미리 보기: MacOS 및 Linux에서 DocFX 미리 보기가 미리 보기를 제대로 시작하지 않습니다. 이러한 플랫폼에 대한 미리 보기는 기본적으로 VS Code Markdown 미리 보기로 설정되어 있습니다.
- DocFx 미리 보기: 모든 플랫폼에서 API에 대한 xref(상호 참조) 링크와 같은 일부 구문은 미리 보기에서 제대로 렌더링되지 않으며, 경우에 따라 콘텐츠 부족이 발생합니다.
- 외부 책갈피: Linux에서 파일 목록이 표시되지만 선택할 제목이 표시되지 않습니다.
- 포함: Linux에서 파일 목록이 표시되지만 선택이 완료되면 링크가 추가되지 않습니다.
