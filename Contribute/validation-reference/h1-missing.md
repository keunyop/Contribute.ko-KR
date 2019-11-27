---
title: h1-missing
description: Docs 빌드 문제 h1-missing에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528887"
---
# <a name="h1-missing"></a><span data-ttu-id="96991-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="96991-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="96991-104">제안</span><span class="sxs-lookup"><span data-stu-id="96991-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="96991-105">H1은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="96991-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="96991-106">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96991-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="96991-107">H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="96991-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="96991-108">해결 방법</span><span class="sxs-lookup"><span data-stu-id="96991-108">Resolution</span></span>

<span data-ttu-id="96991-109">이 문제를 해결하려면 파일의 YML 메타데이터 블록 다음에 H1을 첫 번째 콘텐츠로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="96991-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="96991-110">이 규칙은 포함된 파일에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96991-110">This rule does not apply to included files.</span></span> <span data-ttu-id="96991-111">포함된 파일에 H1 결과를 받게 되면 포함된 파일을 `includes` 폴더로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96991-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="96991-112">`includes` 폴더는 파일 경로의 모든 수준에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96991-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="96991-113">경로에 따라 문서 빌드는 파일을 포함된 파일로 인식하고 H1 유효성 검사는 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96991-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="96991-114">부모 파일에서 H1이 누락되는 일반적인 원인으로 포함된 파일의 잘못된 사용이 있습니다. 즉, H1이 포함된 파일에 있지만 부모 파일에는 없는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="96991-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="96991-115">이 경우는 허용되지 않습니다. 포함된 파일에서 H1을 사용하는 것은 부모 파일에 중복된 H1이 있거나, 포함된 파일을 한 번만 사용함을 의미하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="96991-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="96991-116">H1은 콘텐츠 세트 내에서 고유해야 하며, 여러 파일 간에 콘텐츠를 공유하는 데만 포함된 파일을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96991-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="96991-117">H1이 포함된 파일에 있어서 `h1-missing` 결과를 받는 경우에는 H1뿐만 아니라 포함된 모든 콘텐츠(포함된 파일을 한 번만 사용하는 경우)를 부모 파일로 이동하여 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96991-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="96991-118">Docs의 포함된 파일에 대한 자세한 내용은 Microsoft 내부 문서인 [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)(문서에서 재사용 가능 콘텐츠 포함)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96991-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
