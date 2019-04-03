---
title: ms-prod-service-mismatch
description: Docs 빌드 문제 ms-prod-service-mismatch에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636796"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="5f0d1-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="5f0d1-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5f0d1-104">제안</span><span class="sxs-lookup"><span data-stu-id="5f0d1-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="5f0d1-105">`ms.prod`를 사용하여 온-프레미스 제품을 지정하고 클라우드 서비스에는 `ms.service`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="5f0d1-106">`ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="5f0d1-107">`ms.service`에 대한 더 자세한 정보를 지정하려면 `ms.subservice`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="5f0d1-108">`ms.prod`와 `ms.subservice`를 함께 사용하거나 `ms.service`와 `ms.technology`를 함께 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f0d1-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="5f0d1-109">Resolution</span></span>

<span data-ttu-id="5f0d1-110">먼저, 문서의 올바른 부모 특성(`ms.prod` 또는 `ms.service`)을 선택했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="5f0d1-111">그런 다음, 유효한 쌍 값으로 적절한 자식 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="5f0d1-112">추가 필드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-112">Remove any extra fields.</span></span>

<span data-ttu-id="5f0d1-113">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f0d1-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
