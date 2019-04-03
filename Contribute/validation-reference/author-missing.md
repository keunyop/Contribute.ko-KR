---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6c7306cf674a345b25d3e05c4e00662623c44469
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637440"
---
# <a name="author-missing"></a><span data-ttu-id="99072-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="99072-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="99072-104">제안</span><span class="sxs-lookup"><span data-stu-id="99072-104">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="99072-105">`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="99072-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="99072-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="99072-106">Resolution</span></span>

<span data-ttu-id="99072-107">다음과 같이 작성자의 GitHub ID를 YML 헤더에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="99072-107">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]