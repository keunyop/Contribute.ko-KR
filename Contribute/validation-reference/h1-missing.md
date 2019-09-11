---
title: h1-missing
description: Docs 빌드 문제 h1-missing에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848493"
---
# <a name="h1-missing"></a><span data-ttu-id="94cc1-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="94cc1-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="94cc1-104">제안</span><span class="sxs-lookup"><span data-stu-id="94cc1-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="94cc1-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="94cc1-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="94cc1-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="94cc1-108">해결 방법</span><span class="sxs-lookup"><span data-stu-id="94cc1-108">Resolution</span></span>

<span data-ttu-id="94cc1-109">이 문제를 해결하려면 파일의 YML 메타데이터 블록 다음에 H1을 첫 번째 콘텐츠로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="94cc1-110">이 규칙은 포함된 파일에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-110">This rule does not apply to included files.</span></span> <span data-ttu-id="94cc1-111">포함된 파일에 H1 경고를 받게 되면 포함된 파일을 `includes` 폴더로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="94cc1-112">`includes` 폴더는 파일 경로의 모든 수준에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="94cc1-113">경로에 따라 문서 빌드는 파일을 포함된 파일로 인식하고 H1 유효성 검사는 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94cc1-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]