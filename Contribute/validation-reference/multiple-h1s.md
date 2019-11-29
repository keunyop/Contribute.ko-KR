---
title: multiple-h1s
description: Docs 빌드 문제 multiple-h1s에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528931"
---
# <a name="multiple-h1s"></a><span data-ttu-id="d0b4b-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="d0b4b-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d0b4b-104">제안</span><span class="sxs-lookup"><span data-stu-id="d0b4b-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="d0b4b-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="d0b4b-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="d0b4b-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="d0b4b-108">각 파일에는 하나의 H1만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="d0b4b-109">문서에 `=======` 같은 이중 밑줄을 생성하는 등호 줄이 포함된 경우 이 메시지가 표시될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="d0b4b-110">이는 H1의 대체 Markdown 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="d0b4b-111">일반적으로 병합 충돌에서도 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="d0b4b-112">해결 방법</span><span class="sxs-lookup"><span data-stu-id="d0b4b-112">Resolution</span></span>

<span data-ttu-id="d0b4b-113">이 문제를 해결하려면 후속 H1의 제목 수준을 H2(`##`)로 변경하거나 그렇지 않으면 파일을 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="d0b4b-114">H3에서 H1을 팔로우하는 것과 같이 제목 수준을 건너뛰는 것은 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="d0b4b-115">추가 H1이 실제로 이중 밑줄(`=======`)인 경우 이를 제거하거나 `##` 같은 해시태그 제목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="d0b4b-116">이중 밑줄이 병합 충돌의 일부인 경우에는 병합 충돌 시작 및 끝 마커와 사용되지 않는 텍스트도 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b4b-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
