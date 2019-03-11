---
title: no-space-in-h1
description: Docs 빌드 문제 no-space-in-h1에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427847"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="18bb8-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="18bb8-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="18bb8-104">경고</span><span class="sxs-lookup"><span data-stu-id="18bb8-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="18bb8-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="18bb8-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="18bb8-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18bb8-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="18bb8-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="18bb8-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="18bb8-108">해시 뒤에 공백이 없으면 문서는 H1을 인식하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="18bb8-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="18bb8-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="18bb8-109">Resolution</span></span>

<span data-ttu-id="18bb8-110">이 오류를 해결하려면 H1의 해시 뒤에 공백을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="18bb8-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]