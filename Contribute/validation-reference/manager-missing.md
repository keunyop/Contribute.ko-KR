---
title: manager-missing
description: Docs 빌드 문제 manager-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427827"
---
# <a name="manager-missing"></a><span data-ttu-id="f5844-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="f5844-103">manager-missing</span></span>

<span data-ttu-id="f5844-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="f5844-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f5844-105">제안</span><span class="sxs-lookup"><span data-stu-id="f5844-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="f5844-106">일부 콘텐츠 그룹에는 작성자의 관리자를 식별할 수 있는 `manager` 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f5844-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5844-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f5844-107">Resolution</span></span>

<span data-ttu-id="f5844-108">`manager`에 대해 유효한 Microsoft 별칭을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f5844-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
