---
title: manager-missing
description: Docs 빌드 문제 manager-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637256"
---
# <a name="manager-missing"></a><span data-ttu-id="30bba-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="30bba-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="30bba-104">제안</span><span class="sxs-lookup"><span data-stu-id="30bba-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="30bba-105">일부 콘텐츠 그룹에는 작성자의 관리자를 식별할 수 있는 `manager` 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="30bba-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="30bba-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="30bba-106">Resolution</span></span>

<span data-ttu-id="30bba-107">`manager`에 대해 유효한 Microsoft 별칭을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="30bba-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
