---
title: ms-prod-and-service
description: Docs 빌드 문제 ms-prod-and-service에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236363"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="0a314-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="0a314-103">ms-prod-and-service</span></span>

## <a name="warning"></a><span data-ttu-id="0a314-104">경고</span><span class="sxs-lookup"><span data-stu-id="0a314-104">Warning</span></span>
<span data-ttu-id="0a314-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span><span class="sxs-lookup"><span data-stu-id="0a314-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span></span>

## <a name="resolution"></a><span data-ttu-id="0a314-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0a314-106">Resolution</span></span>

<span data-ttu-id="0a314-107">`ms.prod` 또는 `ms.service`가 필요하고, 둘 다 제공할 수는 없습니다. `ms.prod`는 온-프레미스 제품에 사용되고, `ms.service`는 클라우드 서비스에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a314-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="0a314-108">문서에 적절한 것을 결정하고, 값이 올바른지 확인하고, 다른 필드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="0a314-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="0a314-109">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a314-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="0a314-110">새 값을 요청하려면 [관련 절차](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master)를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="0a314-110">To request new values, follow [this process](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
