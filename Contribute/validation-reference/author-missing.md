---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431533"
---
# <a name="author-missing"></a><span data-ttu-id="66cc8-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="66cc8-103">author-missing</span></span>

<span data-ttu-id="66cc8-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="66cc8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="66cc8-105">제안</span><span class="sxs-lookup"><span data-stu-id="66cc8-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="66cc8-106">`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="66cc8-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="66cc8-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="66cc8-107">Resolution</span></span>

<span data-ttu-id="66cc8-108">다음과 같이 작성자의 GitHub ID를 YML 헤더에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="66cc8-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]