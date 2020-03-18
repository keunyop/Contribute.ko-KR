---
title: 자동 둥근 따옴표 바꾸기 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack을 통해 자동으로 둥근 따옴표를 바꾸는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336707"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="00339-103">둥근 따옴표 바꾸기</span><span class="sxs-lookup"><span data-stu-id="00339-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="00339-104">요약</span><span class="sxs-lookup"><span data-stu-id="00339-104">Summary</span></span>

<span data-ttu-id="00339-105">콘텐츠 개발자는 최신 기술 및 인텔리전스의 몇 가지 가장 발전된 기능을 만드는 일을 담당하고 있으나 아직도 현재의 도구는 Markdown에서 “곧은 따옴표”의 사용을 선호합니다.</span><span class="sxs-lookup"><span data-stu-id="00339-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="00339-106">그 반대는 “둥근 따옴표”입니다.</span><span class="sxs-lookup"><span data-stu-id="00339-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="00339-107">둥근 따옴표는 이상적인 입력 체계에서 일반적으로 사용되지만 Markdown 및 렌더링된 HTML에서는 선호되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00339-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="00339-108">예를 들어 Microsoft Word 문서에서 작업하는 경우 <kbd>Shift</kbd> 키를 누른 상태로 <kbd>"</kbd>를 입력하면 Microsoft Word가 `"` 문자를 해당하는 둥근 따옴표 문자(`“`)로 빠르게 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="00339-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="00339-109">Description</span><span class="sxs-lookup"><span data-stu-id="00339-109">Description</span></span>        | <span data-ttu-id="00339-110">유니코드</span><span class="sxs-lookup"><span data-stu-id="00339-110">Unicode</span></span>  | <span data-ttu-id="00339-111">둥근 따옴표</span><span class="sxs-lookup"><span data-stu-id="00339-111">Smart Quote</span></span> | <span data-ttu-id="00339-112">바꾸기</span><span class="sxs-lookup"><span data-stu-id="00339-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="00339-113">왼쪽 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="00339-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="00339-114">오른쪽 큰따옴표</span><span class="sxs-lookup"><span data-stu-id="00339-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="00339-115">왼쪽 작은따옴표</span><span class="sxs-lookup"><span data-stu-id="00339-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="00339-116">오른쪽 작은따옴표</span><span class="sxs-lookup"><span data-stu-id="00339-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="00339-117">Markdown( *\*.md*) 파일에서 텍스트를 붙여넣거나 콘텐츠를 업데이트할 때 이 기능을 사용하면 콘텐츠를 적극적으로 평가하고 값을 평가에 따라 자동으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="00339-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="00339-118">둥근 따옴표 바꾸기 기능은 `©, ™, ®, •`, 아래 첨자 및 위 첨자 문자와 같은 다른 문자도 바꿉니다(여기에 나온 문자로 제한되지 않음).</span><span class="sxs-lookup"><span data-stu-id="00339-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="00339-119">이 기능은 Word 문서에서 텍스트를 붙여넣을 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="00339-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="00339-120">기본 설정</span><span class="sxs-lookup"><span data-stu-id="00339-120">Preferences</span></span>

<span data-ttu-id="00339-121">이 기능은 선택 사항이지만, 기본적으로 `true`로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00339-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="00339-122">이 기능을 설정하거나 해제하도록 토글하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="00339-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="00339-123">**파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다. </span><span class="sxs-lookup"><span data-stu-id="00339-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="00339-124">**Markdown: 둥근 따옴표 바꾸기** 섹션에서 설정을 토글합니다.</span><span class="sxs-lookup"><span data-stu-id="00339-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="00339-125">예제</span><span class="sxs-lookup"><span data-stu-id="00339-125">In action</span></span>

<span data-ttu-id="00339-126">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="00339-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="00339-127">[![둥근 따옴표 바꾸기 데모](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="00339-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
