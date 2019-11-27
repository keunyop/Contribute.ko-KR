---
title: h1-not-first
description: Docs 빌드 문제 h1-not-first에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528927"
---
# <a name="h1-not-first"></a><span data-ttu-id="195b8-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="195b8-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="195b8-104">경고</span><span class="sxs-lookup"><span data-stu-id="195b8-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="195b8-105">markdown 파일에서 YAML 메타데이터 헤더만 H1 앞에 올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="195b8-106">예를 들어, 문서 맨 위에 추가하려는 메모나 이미지는 H1 뒤에 와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="195b8-107">다음은 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="195b8-108">대신 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="195b8-109">본 문제의 다른 일반적인 원인으로는 YAML 헤더 앞에 오는 [BOM(바이트 순서 표시)](http://www.websina.com/bugzero/kb/unicode-bom.html)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="195b8-110">콘텐츠를 리포지토리에 커밋할 때 가끔 이러한 BOM에 인코딩 문제가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="195b8-111">이로 인해 GitHub에서 잘못된 렌더링이 발생하므로 해당 BOM을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="195b8-112">해결 방법</span><span class="sxs-lookup"><span data-stu-id="195b8-112">Resolution</span></span>

<span data-ttu-id="195b8-113">H1 앞에 오는 YAML 메타데이터 헤더를 제외한 모든 콘텐츠를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="195b8-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
