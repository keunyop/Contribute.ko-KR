---
title: ms-service-missing
description: Docs 빌드 문제 ms-service-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636704"
---
# <a name="ms-service-missing"></a><span data-ttu-id="f88d9-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="f88d9-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f88d9-104">제안</span><span class="sxs-lookup"><span data-stu-id="f88d9-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="f88d9-105">`ms.service`를 사용하여 클라우드 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="f88d9-106">`ms.service`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.subservice`를 지정하면 되지만, `ms.subservice`를 지정하는 경우에는 `ms.service`도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="f88d9-107">`ms.service` 및 `ms.subservice`의 값은 유효한 쌍이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f88d9-108">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f88d9-108">Resolution</span></span>

<span data-ttu-id="f88d9-109">지정한 `ms.subservice` 값이 문서에 적합한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="f88d9-110">그런 다음, `ms.subservice`에 유효한 부모인 적절한 `ms.service` 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="f88d9-111">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f88d9-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
