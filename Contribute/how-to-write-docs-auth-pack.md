---
title: Visual Studio Code용 Docs Authoring Pack
description: 이 문서에서는 docs.microsoft.com용 Markdown 작성을 용이하게 하는 Visual Studio Code 확장 팩을 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336416"
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code용 Docs Authoring Pack

Docs Authoring Pack은 docs.microsoft.com용 Markdown 작성을 지원하는 VS Code 확장 모음입니다. 이 팩은 [VS Code Marketplace에서 사용](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)할 수 있으며 포함된 확장은 다음과 같습니다.

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): 경고, 코드 조각, 지역화 불가능한 텍스트 등 Docs(docs.microsoft.com)의 기본 Markdown 지원 및 사용자 지정 Markdown 구문 지원을 포함하여 Docs 콘텐츠에 대한 Markdown 작성 지원을 제공합니다. 이제 TOC 항목 삽입과 같은 몇 가지 기본 YAML 작성 지원도 포함되었습니다.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): David Anson이 개발한 인기 있는 Markdown Linter이며, Markdown이 유효하도록 보장합니다.
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)(Code 맞춤법 검사기): Street Side Software에서 제공하는 완전한 오프라인 맞춤법 검사기입니다.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): 사용자 지정 Markdown을 포함하여 보다 정확한 Markdown 미리 보기를 위해 docs.microsoft.com CSS를 사용합니다.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)(Docs 문서 템플릿): 사용자가 학습 모듈을 스캐폴드하고 Markdown 스켈레톤 콘텐츠를 새 파일에 적용할 수 있습니다.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Docs YAML 스키마 유효성 검사 및 자동 완성 기능을 제공합니다.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images)(Docs 이미지): docs.microsoft.com 작성자에게 도움이 되도록 폴더 및 개별 파일에 대해 이미지 압축 및 크기 조정 기능을 제공합니다.

## <a name="prerequisites-and-assumptions"></a>필수 조건 및 가정

Docs Markdown 확장을 사용하여 상대 링크와 이미지, 기타 포함된 콘텐츠를 삽입하려면 VS Code 작업 영역의 범위를 복제된 OPS(Open Publishing System) 리포지토리의 루트로 지정해야 합니다. 예를 들어 docs 리포지토리를 `C:\git\SomeDocsRepo\`에 복제한 경우 VS Code에서 해당 폴더 또는 하위 폴더를 엽니다(**파일** > **폴더 열기** 메뉴를 사용하거나 명령줄에서 `code C:\git\SomeDocsRepo\` 사용).

경고 및 코드 조각과 같이 확장에서 지원하는 일부 구문은 OPS용 사용자 지정 Markdown입니다. 사용자 지정 Markdown은 OPS를 통해 게시하지 않으면 올바르게 렌더링되지 않습니다.

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown 확장을 사용하는 방법

**Docs Markdown** 메뉴에 액세스하려면 <kbd>ALT+M</kbd>을 입력합니다. 위쪽/아래쪽 화살표를 클릭하거나 사용하여 필요한 명령을 선택할 수 있습니다. 또는 필터링을 시작하도록 입력한 후 필요한 함수가 메뉴에 강조 표시되면 <kbd>Enter</kbd> 키를 누릅니다.

최신 명령 목록은 [Docs Markdown 추가 정보](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)를 참조하세요.

## <a name="how-to-generate-a-master-redirect-file"></a>마스터 리디렉션 파일을 생성하는 방법

Docs Markdown 확장에는 개별 파일의 `redirect_url` 메타데이터를 기반으로 리포지토리의 마스터 리디렉션 파일을 생성하거나 업데이트하는 스크립트가 포함되어 있습니다. 이 스크립트는 `redirect_url` 리포지토리의 모든 Markdown 파일을 검사하고, 리포지토리의 마스터 리디렉션 파일( *.openpublishing.redirection.json*)에 리디렉션 메타데이터를 추가하고, 리디렉션된 파일을 리포지토리 외부의 폴더로 이동합니다. 스크립트를 실행하려면 다음을 수행합니다.

1. <kbd>F1</kbd> 키를 선택하여 VS Code 명령 팔레트를 엽니다.
2. “Docs: Generate...”를 입력합니다.
3. `Docs: Generate master redirection file` 명령을 선택합니다.
4. 스크립트 실행이 완료되면 VS Code 출력 창에 리디렉션 결과가 표시되고 기본 경로의 Docs Authoring\redirects 폴더에 제거된 Markdown 파일이 추가됩니다.
5. 결과를 검토합니다. 결과가 예상대로이면 끌어오기 요청을 제출하여 리포지토리를 업데이트합니다.

## <a name="how-to-assign-keyboard-shortcuts"></a>바로 가기 키를 할당하는 방법

1. <kbd>CTRL+K</kbd>, <kbd>Ctrl+S</kbd>를 차례로 입력하여 **바로 가기 키** 목록을 엽니다.
1. 사용자 지정 키 바인딩을 만들 명령(예: `formatBold`)을 검색합니다.
1. 줄 위로 마우스를 가져가면 명령 이름 근처에 표시되는 더하기 기호를 클릭합니다.
1. 새 입력 상자가 표시되면 해당 특정 명령에 바인딩하려는 바로 가기 키를 입력합니다. 예를 들어 굵게 명령의 일반 바로 가기를 사용하려면 <kbd>Ctrl+B</kbd>를 입력합니다.
1. Markdown이 아닌 파일에서는 사용할 수 없도록 키 바인딩에 `when` 절을 삽입하는 것이 좋습니다. 이렇게 하려면 *keybindings.json*을 열고 명령 이름 아래에 다음 줄을 삽입합니다(줄 사이에 쉼표를 추가해야 함).

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    완성된 사용자 지정 키 바인딩은 *keybindings.json*에 다음과 같이 표시됩니다.

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > 이 파일에 키 바인딩을 배치하여 기본값을 덮어씁니다.

1. *keybindings.json*을 저장합니다.

키 바인딩에 대한 자세한 내용은 [VS Code docs](https://code.visualstudio.com/docs/getstarted/keybindings)를 참조하세요.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>레거시 "Gauntlet" 도구 모음을 표시하는 방법

Docs Markdown 확장이 설치되면 "Gauntlet"이라는 확장 코드의 이전 사용자는 더 이상 제작 도구 모음이 VS Code 창 아래쪽에 표시되지 않는다는 사실을 알게 됩니다. 도구 모음은 VS Code 상태 표시줄에서 많은 공간을 차지하고 확장 UX에 대한 모범 사례를 따르지 않았기 때문에 새 확장에서 더 이상 사용되지 않습니다. 그러나 필요에 따라 다음과 같이 VS Code settings.json 파일을 업데이트하여 도구 모음을 표시할 수도 있습니다.

1. VS Code에서 **파일** > **기본 설정** > **설정**으로 이동하거나 <kbd>Ctrl+,</kbd>를 선택합니다.
1. **사용자 설정**을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나 **작업 영역 설정**을 선택하여 현재 작업 영역에 대한 설정만 변경합니다.
1. **확장** > **Docs Markdown 확장 구성**을 선택하고 **Show the legacy toolbar in the bottom status bar**(아래쪽 상태 표시줄에 레거시 도구 모음 표시)를 선택합니다.

   ![VS Code에서 레거시 도구 모음 설정 표시](docs-authoring/media/show-gauntlet-bar.png)

사용자가 항목을 선택하면 VS Code에서 *settings.json* 파일을 업데이트합니다. 그런 다음, 변경 내용을 적용하려면 창을 다시 로드하라는 메시지가 표시됩니다.

확장에 추가된 새 명령은 도구 모음에서 사용할 수 없습니다.

## <a name="how-to-use-docs-templates"></a>Docs 템플릿을 사용하는 방법

Docs 문서 템플릿은 VS Code 작성자가 중앙 저장소의 Markdown 템플릿을 가져와서 파일에 적용할 수 있습니다. 템플릿은 필수 메타데이터가 문서에 포함되어 있는지, 콘텐츠 표준을 따랐는지 등을 확인하는 데 도움이 될 수 있습니다. 템플릿은 공용 GitHub 리포지토리에 Markdown 파일로 관리됩니다.

### <a name="to-apply-a-template-in-vs-code"></a>VS Code의 템플릿을 적용하려면

1. Docs 문서 템플릿 확장이 설치되어 있고 사용하도록 설정되어 있는지 확인합니다.
1. Docs Markdown 확장을 설치하지 않은 경우 <kbd>F1</kbd> 키를 눌러 명령 팔레트를 열고, 필터링할 “템플릿” 입력을 시작한 후 `Docs: Template`을 클릭합니다. Docs Markdown을 설치한 경우 명령 팔레트를 사용하거나 <kbd>Alt+M</kbd>을 클릭하여 Docs Markdown QuickPick 메뉴를 표시한 후 목록에서 `Template`을 선택합니다.
1. 표시되는 목록에서 원하는 템플릿을 선택합니다.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>GitHub ID 및/또는 Microsoft 별칭을 VS Code 설정에 추가하려면

템플릿 확장은 세 가지 동적 메타데이터 필드(author, ms.author, ms.date)를 지원합니다. 즉, 템플릿 작성자가 Markdown 템플릿의 메타데이터 헤더에 이러한 필드를 사용하는 경우 템플릿을 적용하면 다음과 같이 필드가 파일에 자동으로 채워집니다.

| 메타데이터 필드 | 값 |
|--|--|
| `author` | VS Code 설정 파일에 지정한 경우 해당 GitHub 별칭. |
| `ms.author` | VS Code 설정 파일에 지정한 경우 해당 Microsoft 별칭. Microsoft 직원이 아닌 경우 지정되지 않은 상태로 두세요. |
| `ms.date` | Docs 지원 형식, `MM/DD/YYYY`로 된 현재 날짜. 이후에 파일을 업데이트해도 날짜가 자동으로 업데이트되지 않습니다. 수동으로 업데이트해야 합니다. 이 필드는 “문서가 최신 상태임”을 나타내는 데 사용됩니다. |

### <a name="to-set-author-andor-msauthor"></a>author 및/또는 ms.author를 설정하려면

1. VS Code에서 **파일** > **기본 설정** > **설정**으로 이동하거나 <kbd>Ctrl+,</kbd>를 선택합니다.
1. **사용자** 설정을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나 **작업 영역** 설정을 선택하여 현재 작업 영역에 대한 설정만 변경합니다.
1. 왼쪽에 있는 [기본 설정] 창에서 **Docs 문서 템플릿 확장 구성**을 찾은 다음, 원하는 설정 옆에 있는 연필 아이콘을 클릭하고 [설정에서 바꾸기]를 클릭합니다.
1. **사용자** 설정 창이 나란히 열리고 맨 아래에 새 항목이 표시됩니다.
1. GitHub ID 또는 Microsoft 메일 별칭을 적절하게 추가하고 파일을 저장합니다.
1. 변경 사항을 적용하기 위해 VS Code를 닫고 다시 시작해야 할 수도 있습니다.
1. 이제 동적 필드를 사용하는 템플릿을 적용하면 GitHub ID 및/또는 Microsoft 별칭이 메타데이터 헤더에 자동으로 채워집니다.

### <a name="to-make-a-new-template-available-in-vs-code"></a>VS Code에서 새 템플릿을 사용할 수 있도록 하려면

1. 템플릿을 Markdown 파일로 초안을 만듭니다.
1. [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 리포지토리의 템플릿 폴더에 대해 끌어오기 요청을 제출합니다.

docs.microsoft.com 팀은 템플릿을 검토하고 docs.microsoft.com 스타일 지침을 충족하는 경우 PR을 병합합니다. 병합한 후에는 Docs 문서 템플릿 확장의 모든 사용자가 템플릿을 사용할 수 있습니다.

## <a name="demo-several-features"></a>여러 기능에 대한 데모

아래의 짧은 동영상에서는 Docs Authoring Pack의 다음 기능을 간단히 보여 줍니다.

* **YAML 파일**
  * “Docs: 리포지토리의 파일에 연결”에 대한 지원
* **Markdown 파일**
  * “ms.date” 메타데이터 값 업데이트 상황에 맞는 메뉴 옵션
  * 코드 펜스 언어 식별자에 대한 코드 자동 완성 지원
  * 인식할 수 없는 코드 펜스 언어 식별자 경고/자동 수정 지원
  * 선택 영역 오름차순 정렬(A - Z)
  * 선택 영역 내림차순 정렬(Z - A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>기여 예상

Docs Authoring Pack 확장은 오픈 소스로, GitHub 계정이 있는 사용자라면 누구나 기여하는 데 사용할 수 있습니다. 이 프로젝트에 적극적으로 참여하는 Microsoft 내부 전담 팀이 있습니다. 이 팀은 문제 및 끌어오기 요청을 모니터링합니다. SLA(서비스 수준 약정)에 따른 끌어오기 요청 검토의 예상 기간은 현재 1주일입니다. 팀은 소요 시간이 단축되도록 자동화에 노력을 기울이고 있습니다.

## <a name="next-steps"></a>다음 단계

Visual Studio Code 확장인 Docs Authoring Pack에서 제공하는 다양한 기능을 살펴봅니다.

* [개발자 언어 완성](docs-authoring/dev-lang-completion.md)
* [이미지 압축](docs-authoring/image-compression.md)
* [메타데이터 업데이트](docs-authoring/metadata-updates.md)
* [테이블 서식 다시 지정](docs-authoring/reformat-table.md)
* [둥근 따옴표 바꾸기](docs-authoring/smart-quote-replacement.md)
* [리디렉션 정렬](docs-authoring/sort-redirects.md)
* [선택 영역 정렬](docs-authoring/sort-selection.md)
