---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713042"
---
# <a name="author-missing"></a><span data-ttu-id="c31d1-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="c31d1-103">author-missing</span></span>

<span data-ttu-id="c31d1-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="c31d1-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c31d1-105">제안</span><span class="sxs-lookup"><span data-stu-id="c31d1-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="c31d1-106">`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="c31d1-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="c31d1-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="c31d1-107">Resolution</span></span>

<span data-ttu-id="c31d1-108">다음과 같이 작성자의 GitHub ID를 YML 헤더에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c31d1-108">Add the author's GitHub ID to the YML header:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]