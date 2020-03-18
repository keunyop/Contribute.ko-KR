---
title: 개발자 언어 완성 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack에서 제공하는 개발자 언어 완성 기능이 기여자에게 어떻게 도움이 되는지 알아봅니다.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336799"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="04a7a-103">개발자 언어 완성</span><span class="sxs-lookup"><span data-stu-id="04a7a-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="04a7a-104">요약</span><span class="sxs-lookup"><span data-stu-id="04a7a-104">Summary</span></span>

<span data-ttu-id="04a7a-105">기여자가 Markdown 파일에서 세 개의 억음 악센트 기호(코드 펜스 시작 부분) 다음에 올 수 있는 유효한 언어 식별자(개발자 언어)를 결정하는 데는 도움이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="04a7a-106">아쉽게도 개발자 언어에 대한 빌드 시간 유효성 검사는 존재하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="04a7a-107">그 결과 동일한 개념 문서 집합에 단일 언어에 대한 서로 다른 표시가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="04a7a-108">C#을 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-108">Consider C# as an example.</span></span> <span data-ttu-id="04a7a-109">기여자는 해당 언어에 대한 개발자 언어 표시로 `c#`, `C#`, `cs`, `csharp` 등을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="04a7a-110">이러한 표시 중 올바른 것은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="04a7a-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="04a7a-111">‘개발자 언어 완성’ 기능은 알려진 개발자 언어 목록을 표시하여 혼동이 발생하지 않도록 합니다. </span><span class="sxs-lookup"><span data-stu-id="04a7a-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="04a7a-112">IntelliSense에서 개발자 언어 이름을 선택하면 다음 작업이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="04a7a-113">코드 펜스가 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-113">The code fence is closed.</span></span>
* <span data-ttu-id="04a7a-114">캐럿이 코드 펜스에 배치됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="04a7a-115">기본 설정</span><span class="sxs-lookup"><span data-stu-id="04a7a-115">Preferences</span></span>

<span data-ttu-id="04a7a-116">이 기능은 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="04a7a-117">사용할 수 있는 설정은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-117">The following settings are available:</span></span>

* [<span data-ttu-id="04a7a-118">일반적으로 사용되는 개발자 언어 표시</span><span class="sxs-lookup"><span data-stu-id="04a7a-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="04a7a-119">모든 알려진 개발자 언어 표시</span><span class="sxs-lookup"><span data-stu-id="04a7a-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="04a7a-120">일반적으로 사용되는 개발자 언어 표시</span><span class="sxs-lookup"><span data-stu-id="04a7a-120">Display commonly used dev langs</span></span>

<span data-ttu-id="04a7a-121">단일 문서 집합에는 유효한 개발자 언어의 일부만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="04a7a-122">사용자 환경을 개선하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="04a7a-123">Visual Studio Code에서 루트 디렉터리의 문서 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="04a7a-124">**파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다. </span><span class="sxs-lookup"><span data-stu-id="04a7a-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="04a7a-125">**Markdown: 문서 집합 언어** 섹션에서 **settings.json에서 편집** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="04a7a-126">다음 `markdown.docsetLanguages` 속성을 *settings.json* 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="04a7a-127">속성의 빈 배열에 캐럿을 배치하고 IntelliSense를 활성화합니다(<kbd>Ctrl</kbd> + <kbd>Space</kbd> 사용).</span><span class="sxs-lookup"><span data-stu-id="04a7a-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="04a7a-128">알려진 개발자 언어 이름 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="04a7a-129">필요한 만큼 배열에 개발자 언어 이름을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="04a7a-130">예를 들어 다음 목록에서는 세 개의 억음 악센트 기호를 입력하면 네 개의 개발자 언어 이름이 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="04a7a-131">변경 내용을 *settings.json* 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="04a7a-132">`markdown.docsetLanguages` 배열을 비워 두면 모든 알려진 개발자 언어가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="04a7a-133">모든 알려진 개발자 언어 표시</span><span class="sxs-lookup"><span data-stu-id="04a7a-133">Display all known dev langs</span></span>

<span data-ttu-id="04a7a-134">기본적으로 모든 알려진 개발자 언어 이름이 IntelliSense에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="04a7a-135">이 설정은 [일반적으로 사용되는 개발자 언어 표시](#display-commonly-used-dev-langs)에 설명된 `markdown.docsetLanguages` 속성을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="04a7a-136">이 설정을 변경하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-136">To change this setting:</span></span>

1. <span data-ttu-id="04a7a-137">**파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다. </span><span class="sxs-lookup"><span data-stu-id="04a7a-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="04a7a-138">**Markdown: 모든 사용 가능한 언어** 섹션에서 설정을 토글합니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="04a7a-139">예제</span><span class="sxs-lookup"><span data-stu-id="04a7a-139">In action</span></span>

<span data-ttu-id="04a7a-140">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="04a7a-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="04a7a-141">[![개발자 언어 완성](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="04a7a-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
