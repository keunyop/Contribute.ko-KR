---
title: ms-prod-service-mismatch
description: Docs 빌드 문제 ms-prod-service-mismatch에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713180"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="5167a-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="5167a-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="5167a-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="5167a-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5167a-105">제안</span><span class="sxs-lookup"><span data-stu-id="5167a-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="5167a-106">`ms.prod`를 사용하여 온-프레미스 제품을 지정하고 클라우드 서비스에는 `ms.service`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="5167a-107">`ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="5167a-108">`ms.service`에 대한 더 자세한 정보를 지정하려면 `ms.subservice`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="5167a-109">`ms.prod`와 `ms.subservice`를 함께 사용하거나 `ms.service`와 `ms.technology`를 함께 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="5167a-110">해결 방법</span><span class="sxs-lookup"><span data-stu-id="5167a-110">Resolution</span></span>

<span data-ttu-id="5167a-111">먼저, 문서의 올바른 부모 특성(`ms.prod` 또는 `ms.service`)을 선택했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="5167a-112">그런 다음, 유효한 쌍 값으로 적절한 자식 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="5167a-113">추가 필드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-113">Remove any extra fields.</span></span>

<span data-ttu-id="5167a-114">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/whitelists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5167a-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
