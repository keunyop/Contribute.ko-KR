---
title: h1-in-moniker
description: Docs 빌드 문제 h1-in-moniker에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528818"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="e44b2-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="e44b2-103">h1-in-moniker</span></span>

## <a name="warning"></a><span data-ttu-id="e44b2-104">경고</span><span class="sxs-lookup"><span data-stu-id="e44b2-104">Warning</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="e44b2-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="e44b2-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="e44b2-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="e44b2-108">각 파일에는 하나의 H1만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="e44b2-109">모니커에 H1가 있으면 버전 관리를 구성하는 방법에 따라 H1가 쉽게 중복되거나 누락될 수 있으므로 H1는 모니커 섹션에서 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="e44b2-110">모니커 섹션에 `=======` 같은 이중 밑줄을 생성하는 등호 줄이 포함된 경우 이 메시지가 표시될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="e44b2-111">이는 H1의 대체 Markdown 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="e44b2-112">일반적으로 병합 충돌에서도 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="e44b2-113">해결 방법</span><span class="sxs-lookup"><span data-stu-id="e44b2-113">Resolution</span></span>

<span data-ttu-id="e44b2-114">이 문제를 해결하려면 모든 모니커 섹션에서 H1를 제거하고 문서의 맨 위에 있는 H1이 모든 모니커 섹션에 적합한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="e44b2-115">H3에서 H1을 팔로우하는 것과 같이 제목 수준을 건너뛰는 것은 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="e44b2-116">모니커 섹션의 H1이 실제로 이중 밑줄(`=======`)인 경우 이를 제거하거나 `##` 같은 해시태그 제목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="e44b2-117">이중 밑줄이 병합 충돌의 일부인 경우에는 병합 충돌 시작 및 끝 마커와 사용되지 않는 텍스트도 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e44b2-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
