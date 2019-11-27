---
title: h1-no-space
description: Docs 빌드 문제 h1-no-space에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528971"
---
# <a name="h1-no-space"></a><span data-ttu-id="9a736-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="9a736-103">h1-no-space</span></span>

## <a name="warning"></a><span data-ttu-id="9a736-104">경고</span><span class="sxs-lookup"><span data-stu-id="9a736-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="9a736-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9a736-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="9a736-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a736-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="9a736-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a736-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="9a736-108">해시 뒤에 공백이 없으면 문서는 H1을 인식하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="9a736-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="9a736-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="9a736-109">Resolution</span></span>

<span data-ttu-id="9a736-110">이 오류를 해결하려면 H1의 해시 뒤에 공백을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9a736-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
