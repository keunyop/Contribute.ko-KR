---
title: ms-prod-or-service-missing
description: Docs 빌드 문제 ms-prod-or-service-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987563"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="0688f-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="0688f-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="0688f-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="0688f-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0688f-105">제안</span><span class="sxs-lookup"><span data-stu-id="0688f-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="0688f-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0688f-106">Resolution</span></span>

<span data-ttu-id="0688f-107">`ms.prod` 또는 `ms.service`가 필요하고, 둘 다 제공할 수는 없습니다. `ms.prod`는 온-프레미스 제품에 사용되고, `ms.service`는 클라우드 서비스에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0688f-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="0688f-108">문서에 적절한 것을 결정하고, 값이 올바른지 확인하고, 다른 필드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="0688f-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="0688f-109">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0688f-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]