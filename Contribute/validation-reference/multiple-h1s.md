---
title: multiple-h1
description: Docs 빌드 문제 multiple-h1에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848593"
---
# <a name="multiple-h1"></a><span data-ttu-id="f73fa-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="f73fa-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f73fa-104">제안</span><span class="sxs-lookup"><span data-stu-id="f73fa-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="f73fa-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="f73fa-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="f73fa-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="f73fa-108">각 파일에는 하나의 H1만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="f73fa-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f73fa-109">Resolution</span></span>

<span data-ttu-id="f73fa-110">이 문제를 해결하려면 후속 H1의 제목 수준을 H2(`##`)로 변경하거나 그렇지 않으면 파일을 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="f73fa-111">H3에서 H1을 팔로우하는 것과 같이 제목 수준을 건너뛰는 것은 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f73fa-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]