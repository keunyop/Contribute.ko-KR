---
title: 리디렉션 정렬 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack을 통해 리디렉션을 정렬하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336684"
---
# <a name="sort-redirects"></a><span data-ttu-id="68057-103">리디렉션 정렬</span><span class="sxs-lookup"><span data-stu-id="68057-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="68057-104">요약</span><span class="sxs-lookup"><span data-stu-id="68057-104">Summary</span></span>

<span data-ttu-id="68057-105">docs.microsoft.com 문서 집합이 개선되어 일부 Markdown 파일이 삭제될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="68057-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="68057-106">Markdown 파일이 삭제되면 삭제된 문서에 대한 모든 참조가 리디렉션을 통해 제대로 확인되도록 리디렉션을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68057-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="68057-107">리디렉션은 *.openpublishing.redirection.json* 파일에 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="68057-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="68057-108">명령 팔레트를 열고 <kbd>F1</kbd>(또는 macOS에서 <kbd>⇧⌘P</kbd>)을 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="68057-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="68057-109">다음을 입력합니다. **Docs: Sort master redirection file**</span><span class="sxs-lookup"><span data-stu-id="68057-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="68057-110">명령을 선택하여 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="68057-110">Select the command to execute it</span></span>
1. <span data-ttu-id="68057-111">*.openpublishing.redirection.json* 파일의 변경 내용을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="68057-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="68057-112">고려 사항</span><span class="sxs-lookup"><span data-stu-id="68057-112">Considerations</span></span>

<span data-ttu-id="68057-113">“데이지 체이닝”의 개념은 *.openpublishing.redirection.json* 파일이 원래 설계된 방식에 드러납니다.</span><span class="sxs-lookup"><span data-stu-id="68057-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="68057-114">시간이 지날수록 리디렉션으로 추가된 파일은 오래된 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68057-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="68057-115">파일 A가 삭제되고 파일 B로의 리디렉션이 필요하게 되며 나중에는 파일 B가 삭제되고 파일 C로 리디렉션될 때 이러한 상태가 됩니다. 두 항목 다 C를 가리키도록 하여 A는 C로 리디렉션되고 B는 동일하게 유지하는 것이 이상적입니다.</span><span class="sxs-lookup"><span data-stu-id="68057-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="68057-116">이렇게 하면 성능이 약간 향상되므로 이 기능에 대한 작업이 활발하게 이루어지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68057-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="68057-117">예제</span><span class="sxs-lookup"><span data-stu-id="68057-117">In action</span></span>

<span data-ttu-id="68057-118">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="68057-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="68057-119">[![리디렉션 정렬 데모](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="68057-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
