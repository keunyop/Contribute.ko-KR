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
# <a name="docs-authoring-pack-for-vs-code"></a><span data-ttu-id="01947-103">VS Code용 Docs Authoring Pack</span><span class="sxs-lookup"><span data-stu-id="01947-103">Docs Authoring Pack for VS Code</span></span>

<span data-ttu-id="01947-104">Docs Authoring Pack은 docs.microsoft.com용 Markdown 작성을 지원하는 VS Code 확장 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="01947-104">The Docs Authoring Pack is a collection of VS Code extensions to aid with Markdown authoring for docs.microsoft.com.</span></span> <span data-ttu-id="01947-105">이 팩은 [VS Code Marketplace에서 사용](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)할 수 있으며 포함된 확장은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-105">The pack is [available in the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and contains the following extensions:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="01947-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): 경고, 코드 조각, 지역화 불가능한 텍스트 등 Docs(docs.microsoft.com)의 기본 Markdown 지원 및 사용자 지정 Markdown 구문 지원을 포함하여 Docs 콘텐츠에 대한 Markdown 작성 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Provides Markdown authoring assistance for docs.microsoft.com (Docs) content, including basic Markdown support and support for custom Markdown syntax in Docs, such as alerts, code snippets, and non-localizable text.</span></span> <span data-ttu-id="01947-107">이제 TOC 항목 삽입과 같은 몇 가지 기본 YAML 작성 지원도 포함되었습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-107">Now also includes some basic YAML authoring assistance, such as inserting TOC entries.</span></span>
> * <span data-ttu-id="01947-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): David Anson이 개발한 인기 있는 Markdown Linter이며, Markdown이 유효하도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): A popular Markdown linter by David Anson to help make sure your Markdown is valid.</span></span>
> * <span data-ttu-id="01947-109">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)(Code 맞춤법 검사기): Street Side Software에서 제공하는 완전한 오프라인 맞춤법 검사기입니다.</span><span class="sxs-lookup"><span data-stu-id="01947-109">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): A fully offline spell checker by Street Side Software.</span></span>
> * <span data-ttu-id="01947-110">[Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): 사용자 지정 Markdown을 포함하여 보다 정확한 Markdown 미리 보기를 위해 docs.microsoft.com CSS를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-110">[Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Uses the docs.microsoft.com CSS for more accurate Markdown preview, including custom Markdown.</span></span>
> * <span data-ttu-id="01947-111">[Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)(Docs 문서 템플릿): 사용자가 학습 모듈을 스캐폴드하고 Markdown 스켈레톤 콘텐츠를 새 파일에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-111">[Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Allows users to scaffold Learn modules and apply Markdown skeleton content to new files.</span></span>
> * <span data-ttu-id="01947-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Docs YAML 스키마 유효성 검사 및 자동 완성 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Provides Docs YAML schema validation and auto-complete.</span></span>
> * <span data-ttu-id="01947-113">[Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images)(Docs 이미지): docs.microsoft.com 작성자에게 도움이 되도록 폴더 및 개별 파일에 대해 이미지 압축 및 크기 조정 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-113">[Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): Provides image compression and resizing for folders and individual files to help authors of docs.microsoft.com.</span></span>

## <a name="prerequisites-and-assumptions"></a><span data-ttu-id="01947-114">필수 조건 및 가정</span><span class="sxs-lookup"><span data-stu-id="01947-114">Prerequisites and assumptions</span></span>

<span data-ttu-id="01947-115">Docs Markdown 확장을 사용하여 상대 링크와 이미지, 기타 포함된 콘텐츠를 삽입하려면 VS Code 작업 영역의 범위를 복제된 OPS(Open Publishing System) 리포지토리의 루트로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-115">To insert relative links, images, and other embedded content with the Docs Markdown extension, you must have your VS Code workspace scoped to the root of your cloned Open Publishing System (OPS) repo.</span></span> <span data-ttu-id="01947-116">예를 들어 docs 리포지토리를 `C:\git\SomeDocsRepo\`에 복제한 경우 VS Code에서 해당 폴더 또는 하위 폴더를 엽니다(**파일** > **폴더 열기** 메뉴를 사용하거나 명령줄에서 `code C:\git\SomeDocsRepo\` 사용).</span><span class="sxs-lookup"><span data-stu-id="01947-116">For example, if you have cloned the docs repository to `C:\git\SomeDocsRepo\`, then open that folder or a subfolder in VS Code: **File** > **Open Folder** menu,  or `code C:\git\SomeDocsRepo\` from the command line.</span></span>

<span data-ttu-id="01947-117">경고 및 코드 조각과 같이 확장에서 지원하는 일부 구문은 OPS용 사용자 지정 Markdown입니다.</span><span class="sxs-lookup"><span data-stu-id="01947-117">Some syntax supported by the extension, such as alerts and snippets, are custom Markdown for OPS.</span></span> <span data-ttu-id="01947-118">사용자 지정 Markdown은 OPS를 통해 게시하지 않으면 올바르게 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-118">Custom Markdown will not render correctly unless published via OPS.</span></span>

## <a name="how-to-use-the-docs-markdown-extension"></a><span data-ttu-id="01947-119">Docs Markdown 확장을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="01947-119">How to use the Docs Markdown extension</span></span>

<span data-ttu-id="01947-120">**Docs Markdown** 메뉴에 액세스하려면 <kbd>ALT+M</kbd>을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-120">To access the **Docs Markdown** menu, type <kbd>ALT+M</kbd>.</span></span> <span data-ttu-id="01947-121">위쪽/아래쪽 화살표를 클릭하거나 사용하여 필요한 명령을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-121">You can click or use the up and down arrows to select the command you want.</span></span> <span data-ttu-id="01947-122">또는 필터링을 시작하도록 입력한 후 필요한 함수가 메뉴에 강조 표시되면 <kbd>Enter</kbd> 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="01947-122">Or you can type to start filtering, then hit <kbd>ENTER</kbd> when the function you want is highlighted in the menu.</span></span>

<span data-ttu-id="01947-123">최신 명령 목록은 [Docs Markdown 추가 정보](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01947-123">See the [Docs Markdown readme](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) for an up-to-date list of commands.</span></span>

## <a name="how-to-generate-a-master-redirect-file"></a><span data-ttu-id="01947-124">마스터 리디렉션 파일을 생성하는 방법</span><span class="sxs-lookup"><span data-stu-id="01947-124">How to generate a master redirect file</span></span>

<span data-ttu-id="01947-125">Docs Markdown 확장에는 개별 파일의 `redirect_url` 메타데이터를 기반으로 리포지토리의 마스터 리디렉션 파일을 생성하거나 업데이트하는 스크립트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-125">The Docs Markdown extension includes a script to generate or update a master redirection file for a repo, based on the `redirect_url` metadata in individual files.</span></span> <span data-ttu-id="01947-126">이 스크립트는 `redirect_url` 리포지토리의 모든 Markdown 파일을 검사하고, 리포지토리의 마스터 리디렉션 파일( *.openpublishing.redirection.json*)에 리디렉션 메타데이터를 추가하고, 리디렉션된 파일을 리포지토리 외부의 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-126">This script checks every Markdown file in the repo for `redirect_url`, adds the redirection metadata to the master redirection file (*.openpublishing.redirection.json*) for the repo, and moves the redirected files to a folder outside the repo.</span></span> <span data-ttu-id="01947-127">스크립트를 실행하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-127">To run the script:</span></span>

1. <span data-ttu-id="01947-128"><kbd>F1</kbd> 키를 선택하여 VS Code 명령 팔레트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="01947-128">Select <kbd>F1</kbd> to open the VS Code command palette.</span></span>
2. <span data-ttu-id="01947-129">“Docs: Generate...”를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-129">Start typing "Docs: Generate..."</span></span>
3. <span data-ttu-id="01947-130">`Docs: Generate master redirection file` 명령을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-130">Select the command `Docs: Generate master redirection file`.</span></span>
4. <span data-ttu-id="01947-131">스크립트 실행이 완료되면 VS Code 출력 창에 리디렉션 결과가 표시되고 기본 경로의 Docs Authoring\redirects 폴더에 제거된 Markdown 파일이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-131">When the script finishes running, the redirection results will show in the VS Code output pane, and the removed Markdown files will be added to the Docs Authoring\redirects folder under your default path.</span></span>
5. <span data-ttu-id="01947-132">결과를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-132">Review the results.</span></span> <span data-ttu-id="01947-133">결과가 예상대로이면 끌어오기 요청을 제출하여 리포지토리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-133">If they are as expected, submit a pull request to update the repo.</span></span>

## <a name="how-to-assign-keyboard-shortcuts"></a><span data-ttu-id="01947-134">바로 가기 키를 할당하는 방법</span><span class="sxs-lookup"><span data-stu-id="01947-134">How to assign keyboard shortcuts</span></span>

1. <span data-ttu-id="01947-135"><kbd>CTRL+K</kbd>, <kbd>Ctrl+S</kbd>를 차례로 입력하여 **바로 가기 키** 목록을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="01947-135">Type <kbd>CTRL+K</kbd> then <kbd>Ctrl+S</kbd> to open the **Keyboard Shortcuts** list.</span></span>
1. <span data-ttu-id="01947-136">사용자 지정 키 바인딩을 만들 명령(예: `formatBold`)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-136">Search for the command, such as `formatBold`, for which you want to create a custom key binding.</span></span>
1. <span data-ttu-id="01947-137">줄 위로 마우스를 가져가면 명령 이름 근처에 표시되는 더하기 기호를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-137">Click the plus that appears near the command name when you mouse over the line.</span></span>
1. <span data-ttu-id="01947-138">새 입력 상자가 표시되면 해당 특정 명령에 바인딩하려는 바로 가기 키를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-138">After a new input box is visible, type the keyboard shortcut you want to bind to that particular command.</span></span> <span data-ttu-id="01947-139">예를 들어 굵게 명령의 일반 바로 가기를 사용하려면 <kbd>Ctrl+B</kbd>를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-139">For example, to use the common shortcut for bold, type <kbd>Ctrl+B</kbd>.</span></span>
1. <span data-ttu-id="01947-140">Markdown이 아닌 파일에서는 사용할 수 없도록 키 바인딩에 `when` 절을 삽입하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-140">It's a good idea to insert a `when` clause into your key binding, so it won't be available in files other than Markdown.</span></span> <span data-ttu-id="01947-141">이렇게 하려면 *keybindings.json*을 열고 명령 이름 아래에 다음 줄을 삽입합니다(줄 사이에 쉼표를 추가해야 함).</span><span class="sxs-lookup"><span data-stu-id="01947-141">To do this, open *keybindings.json* and insert the following line below the command name (be sure to add a comma between lines):</span></span>

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    <span data-ttu-id="01947-142">완성된 사용자 지정 키 바인딩은 *keybindings.json*에 다음과 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-142">Your completed custom key binding should look like this in *keybindings.json*:</span></span>

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
    > <span data-ttu-id="01947-143">이 파일에 키 바인딩을 배치하여 기본값을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="01947-143">Place your key bindings in this file to overwrite the defaults</span></span>

1. <span data-ttu-id="01947-144">*keybindings.json*을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-144">Save *keybindings.json*.</span></span>

<span data-ttu-id="01947-145">키 바인딩에 대한 자세한 내용은 [VS Code docs](https://code.visualstudio.com/docs/getstarted/keybindings)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01947-145">For more information on key bindings, see the [VS Code docs](https://code.visualstudio.com/docs/getstarted/keybindings).</span></span>

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a><span data-ttu-id="01947-146">레거시 "Gauntlet" 도구 모음을 표시하는 방법</span><span class="sxs-lookup"><span data-stu-id="01947-146">How to show the legacy "Gauntlet" toolbar</span></span>

<span data-ttu-id="01947-147">Docs Markdown 확장이 설치되면 "Gauntlet"이라는 확장 코드의 이전 사용자는 더 이상 제작 도구 모음이 VS Code 창 아래쪽에 표시되지 않는다는 사실을 알게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-147">Former users of the extension code-named "Gauntlet" will notice that the authoring toolbar no longer appears at the bottom of the VS Code window when the Docs Markdown Extension is installed.</span></span> <span data-ttu-id="01947-148">도구 모음은 VS Code 상태 표시줄에서 많은 공간을 차지하고 확장 UX에 대한 모범 사례를 따르지 않았기 때문에 새 확장에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-148">This is because the toolbar took up a large space on the VS Code status bar and did not follow best practices for extension UX, so it is deprecated in the new extension.</span></span> <span data-ttu-id="01947-149">그러나 필요에 따라 다음과 같이 VS Code settings.json 파일을 업데이트하여 도구 모음을 표시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-149">However, you can optionally show the toolbar by updating your VS Code settings.json file as follows:</span></span>

1. <span data-ttu-id="01947-150">VS Code에서 **파일** > **기본 설정** > **설정**으로 이동하거나 <kbd>Ctrl+,</kbd>를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-150">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="01947-151">**사용자 설정**을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나 **작업 영역 설정**을 선택하여 현재 작업 영역에 대한 설정만 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-151">Select **User Settings** to change the settings for all VS Code workspaces or **Workspace Settings** to change them for just the current workspace.</span></span>
1. <span data-ttu-id="01947-152">**확장** > **Docs Markdown 확장 구성**을 선택하고 **Show the legacy toolbar in the bottom status bar**(아래쪽 상태 표시줄에 레거시 도구 모음 표시)를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-152">Select **Extensions** > **Docs Markdown Extension Configuration**, and then select **Show the legacy toolbar in the bottom status bar**.</span></span>

   ![VS Code에서 레거시 도구 모음 설정 표시](docs-authoring/media/show-gauntlet-bar.png)

<span data-ttu-id="01947-154">사용자가 항목을 선택하면 VS Code에서 *settings.json* 파일을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-154">Once you've made your selection, VS Code updates the *settings.json* file.</span></span> <span data-ttu-id="01947-155">그런 다음, 변경 내용을 적용하려면 창을 다시 로드하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-155">You will then be prompted to reload the window for the changes to take effect.</span></span>

<span data-ttu-id="01947-156">확장에 추가된 새 명령은 도구 모음에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-156">Newer commands added to the extension will not be available from the toolbar.</span></span>

## <a name="how-to-use-docs-templates"></a><span data-ttu-id="01947-157">Docs 템플릿을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="01947-157">How to use Docs templates</span></span>

<span data-ttu-id="01947-158">Docs 문서 템플릿은 VS Code 작성자가 중앙 저장소의 Markdown 템플릿을 가져와서 파일에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-158">The Docs Article Templates extension lets writers in VS Code pull a Markdown template from a centralized store and apply it to a file.</span></span> <span data-ttu-id="01947-159">템플릿은 필수 메타데이터가 문서에 포함되어 있는지, 콘텐츠 표준을 따랐는지 등을 확인하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-159">Templates can help ensure that required metadata is included in articles, that content standards are followed, and so on.</span></span> <span data-ttu-id="01947-160">템플릿은 공용 GitHub 리포지토리에 Markdown 파일로 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-160">Templates are managed as Markdown files in a public GitHub repository.</span></span>

### <a name="to-apply-a-template-in-vs-code"></a><span data-ttu-id="01947-161">VS Code의 템플릿을 적용하려면</span><span class="sxs-lookup"><span data-stu-id="01947-161">To apply a template in VS Code</span></span>

1. <span data-ttu-id="01947-162">Docs 문서 템플릿 확장이 설치되어 있고 사용하도록 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-162">Ensure the Docs Article Templates extension is installed and enabled.</span></span>
1. <span data-ttu-id="01947-163">Docs Markdown 확장을 설치하지 않은 경우 <kbd>F1</kbd> 키를 눌러 명령 팔레트를 열고, 필터링할 “템플릿” 입력을 시작한 후 `Docs: Template`을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-163">If you don't have the Docs Markdown extension installed, click <kbd>F1</kbd> to open the command palette, start typing "template" to filter, then click `Docs: Template`.</span></span> <span data-ttu-id="01947-164">Docs Markdown을 설치한 경우 명령 팔레트를 사용하거나 <kbd>Alt+M</kbd>을 클릭하여 Docs Markdown QuickPick 메뉴를 표시한 후 목록에서 `Template`을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-164">If you do have Docs Markdown installed, you can use either the command palette or click <kbd>Alt+M</kbd> to bring up the Docs Markdown QuickPick menu, then select `Template` from the list.</span></span>
1. <span data-ttu-id="01947-165">표시되는 목록에서 원하는 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-165">Select the desired template from the list that appears.</span></span>

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a><span data-ttu-id="01947-166">GitHub ID 및/또는 Microsoft 별칭을 VS Code 설정에 추가하려면</span><span class="sxs-lookup"><span data-stu-id="01947-166">To add your GitHub ID and/or Microsoft alias to your VS Code settings</span></span>

<span data-ttu-id="01947-167">템플릿 확장은 세 가지 동적 메타데이터 필드(author, ms.author, ms.date)를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-167">The Templates extension supports three dynamic metadata fields: author, ms.author, and ms.date.</span></span> <span data-ttu-id="01947-168">즉, 템플릿 작성자가 Markdown 템플릿의 메타데이터 헤더에 이러한 필드를 사용하는 경우 템플릿을 적용하면 다음과 같이 필드가 파일에 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="01947-168">That means that if a template creator uses these fields in the metadata header of a Markdown template, they will be auto-populated in your file when you apply the template, as follows:</span></span>

| <span data-ttu-id="01947-169">메타데이터 필드</span><span class="sxs-lookup"><span data-stu-id="01947-169">Metadata field</span></span> | <span data-ttu-id="01947-170">값</span><span class="sxs-lookup"><span data-stu-id="01947-170">Value</span></span> |
|--|--|
| `author` | <span data-ttu-id="01947-171">VS Code 설정 파일에 지정한 경우 해당 GitHub 별칭.</span><span class="sxs-lookup"><span data-stu-id="01947-171">Your GitHub alias, if specified in your VS Code settings file.</span></span> |
| `ms.author` | <span data-ttu-id="01947-172">VS Code 설정 파일에 지정한 경우 해당 Microsoft 별칭.</span><span class="sxs-lookup"><span data-stu-id="01947-172">Your Microsoft alias, if specified in your VS Code settings file.</span></span> <span data-ttu-id="01947-173">Microsoft 직원이 아닌 경우 지정되지 않은 상태로 두세요.</span><span class="sxs-lookup"><span data-stu-id="01947-173">If you are not a Microsoft employee, leave unspecified.</span></span> |
| `ms.date` | <span data-ttu-id="01947-174">Docs 지원 형식, `MM/DD/YYYY`로 된 현재 날짜.</span><span class="sxs-lookup"><span data-stu-id="01947-174">The current date in the Docs-supported format, `MM/DD/YYYY`.</span></span> <span data-ttu-id="01947-175">이후에 파일을 업데이트해도 날짜가 자동으로 업데이트되지 않습니다. 수동으로 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-175">The date is not automatically updated if you subsequently update the file - you must update it manually.</span></span> <span data-ttu-id="01947-176">이 필드는 “문서가 최신 상태임”을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-176">This field is used to indicate the "article freshness".</span></span> |

### <a name="to-set-author-andor-msauthor"></a><span data-ttu-id="01947-177">author 및/또는 ms.author를 설정하려면</span><span class="sxs-lookup"><span data-stu-id="01947-177">To set author and/or ms.author</span></span>

1. <span data-ttu-id="01947-178">VS Code에서 **파일** > **기본 설정** > **설정**으로 이동하거나 <kbd>Ctrl+,</kbd>를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-178">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="01947-179">**사용자** 설정을 선택하여 모든 VS Code 작업 영역에 대한 설정을 변경하거나 **작업 영역** 설정을 선택하여 현재 작업 영역에 대한 설정만 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-179">Select **User** settings to change the settings for all VS Code workspaces, or **Workspace** settings to change them for just the current workspace.</span></span>
1. <span data-ttu-id="01947-180">왼쪽에 있는 [기본 설정] 창에서 **Docs 문서 템플릿 확장 구성**을 찾은 다음, 원하는 설정 옆에 있는 연필 아이콘을 클릭하고 [설정에서 바꾸기]를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-180">In the Default Settings pane on the left, find **Docs Article Templates Extension Configuration**, click the pencil icon next to the desired setting, then click Replace in Settings.</span></span>
1. <span data-ttu-id="01947-181">**사용자** 설정 창이 나란히 열리고 맨 아래에 새 항목이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01947-181">The **User** settings pane will open side by side, with a new entry at the bottom.</span></span>
1. <span data-ttu-id="01947-182">GitHub ID 또는 Microsoft 메일 별칭을 적절하게 추가하고 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-182">Add your GitHub ID or Microsoft email alias, as appropriate, and save the file.</span></span>
1. <span data-ttu-id="01947-183">변경 사항을 적용하기 위해 VS Code를 닫고 다시 시작해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-183">You might need to close and restart VS Code for the changes to take effect.</span></span>
1. <span data-ttu-id="01947-184">이제 동적 필드를 사용하는 템플릿을 적용하면 GitHub ID 및/또는 Microsoft 별칭이 메타데이터 헤더에 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="01947-184">Now, when you apply a template that uses dynamic fields, your GitHub ID and/or Microsoft alias will be auto-populated in the metadata header.</span></span>

### <a name="to-make-a-new-template-available-in-vs-code"></a><span data-ttu-id="01947-185">VS Code에서 새 템플릿을 사용할 수 있도록 하려면</span><span class="sxs-lookup"><span data-stu-id="01947-185">To make a new template available in VS Code</span></span>

1. <span data-ttu-id="01947-186">템플릿을 Markdown 파일로 초안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01947-186">Draft your template as a Markdown file.</span></span>
1. <span data-ttu-id="01947-187">[MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 리포지토리의 템플릿 폴더에 대해 끌어오기 요청을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-187">Submit a pull request to the templates folder of the [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) repo.</span></span>

<span data-ttu-id="01947-188">docs.microsoft.com 팀은 템플릿을 검토하고 docs.microsoft.com 스타일 지침을 충족하는 경우 PR을 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-188">The docs.microsoft.com team will review your template and merge the PR if it meets docs.microsoft.com style guidelines.</span></span> <span data-ttu-id="01947-189">병합한 후에는 Docs 문서 템플릿 확장의 모든 사용자가 템플릿을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-189">Once merged, the template will be available to all users of the Docs Article Templates extension.</span></span>

## <a name="demo-several-features"></a><span data-ttu-id="01947-190">여러 기능에 대한 데모</span><span class="sxs-lookup"><span data-stu-id="01947-190">Demo several features</span></span>

<span data-ttu-id="01947-191">아래의 짧은 동영상에서는 Docs Authoring Pack의 다음 기능을 간단히 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01947-191">Here's a short video that demonstrates the following features of the Docs Authoring Pack:</span></span>

* <span data-ttu-id="01947-192">**YAML 파일**</span><span class="sxs-lookup"><span data-stu-id="01947-192">**YAML files**</span></span>
  * <span data-ttu-id="01947-193">“Docs: 리포지토리의 파일에 연결”에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="01947-193">Support for "Docs: Link to file in repo"</span></span>
* <span data-ttu-id="01947-194">**Markdown 파일**</span><span class="sxs-lookup"><span data-stu-id="01947-194">**Markdown files**</span></span>
  * <span data-ttu-id="01947-195">“ms.date” 메타데이터 값 업데이트 상황에 맞는 메뉴 옵션</span><span class="sxs-lookup"><span data-stu-id="01947-195">Update "ms.date" Metadata Value context menu option</span></span>
  * <span data-ttu-id="01947-196">코드 펜스 언어 식별자에 대한 코드 자동 완성 지원</span><span class="sxs-lookup"><span data-stu-id="01947-196">Code auto-completion support for code-fence language identifiers</span></span>
  * <span data-ttu-id="01947-197">인식할 수 없는 코드 펜스 언어 식별자 경고/자동 수정 지원</span><span class="sxs-lookup"><span data-stu-id="01947-197">Unrecognized code-fence language identifier warnings / auto correction support</span></span>
  * <span data-ttu-id="01947-198">선택 영역 오름차순 정렬(A - Z)</span><span class="sxs-lookup"><span data-stu-id="01947-198">Sort selection ascending (A to Z)</span></span>
  * <span data-ttu-id="01947-199">선택 영역 내림차순 정렬(Z - A)</span><span class="sxs-lookup"><span data-stu-id="01947-199">Sort selection descending (Z to A)</span></span>

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a><span data-ttu-id="01947-200">기여 예상</span><span class="sxs-lookup"><span data-stu-id="01947-200">Contribution expectations</span></span>

<span data-ttu-id="01947-201">Docs Authoring Pack 확장은 오픈 소스로, GitHub 계정이 있는 사용자라면 누구나 기여하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-201">The Docs Authoring Pack extension is open source and available for contributions to anyone with a GitHub account.</span></span> <span data-ttu-id="01947-202">이 프로젝트에 적극적으로 참여하는 Microsoft 내부 전담 팀이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-202">There is a dedicated internal Microsoft team that actively works on this project.</span></span> <span data-ttu-id="01947-203">이 팀은 문제 및 끌어오기 요청을 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="01947-203">This team monitors issues and pull requests.</span></span> <span data-ttu-id="01947-204">SLA(서비스 수준 약정)에 따른 끌어오기 요청 검토의 예상 기간은 현재 1주일입니다.</span><span class="sxs-lookup"><span data-stu-id="01947-204">The service level agreement (SLA) and expectation of getting a pull request reviewed is currently one week.</span></span> <span data-ttu-id="01947-205">팀은 소요 시간이 단축되도록 자동화에 노력을 기울이고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01947-205">The team is undergoing automation efforts to improve this turn around time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="01947-206">다음 단계</span><span class="sxs-lookup"><span data-stu-id="01947-206">Next steps</span></span>

<span data-ttu-id="01947-207">Visual Studio Code 확장인 Docs Authoring Pack에서 제공하는 다양한 기능을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="01947-207">Explore the various features available in the Docs Authoring Pack, Visual Studio Code extension.</span></span>

* [<span data-ttu-id="01947-208">개발자 언어 완성</span><span class="sxs-lookup"><span data-stu-id="01947-208">Dev lang completion</span></span>](docs-authoring/dev-lang-completion.md)
* [<span data-ttu-id="01947-209">이미지 압축</span><span class="sxs-lookup"><span data-stu-id="01947-209">Image compression</span></span>](docs-authoring/image-compression.md)
* [<span data-ttu-id="01947-210">메타데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="01947-210">Metadata updates</span></span>](docs-authoring/metadata-updates.md)
* [<span data-ttu-id="01947-211">테이블 서식 다시 지정</span><span class="sxs-lookup"><span data-stu-id="01947-211">Reformat table</span></span>](docs-authoring/reformat-table.md)
* [<span data-ttu-id="01947-212">둥근 따옴표 바꾸기</span><span class="sxs-lookup"><span data-stu-id="01947-212">Smart quote replacement</span></span>](docs-authoring/smart-quote-replacement.md)
* [<span data-ttu-id="01947-213">리디렉션 정렬</span><span class="sxs-lookup"><span data-stu-id="01947-213">Sort redirects</span></span>](docs-authoring/sort-redirects.md)
* [<span data-ttu-id="01947-214">선택 영역 정렬</span><span class="sxs-lookup"><span data-stu-id="01947-214">Sort selection</span></span>](docs-authoring/sort-selection.md)
