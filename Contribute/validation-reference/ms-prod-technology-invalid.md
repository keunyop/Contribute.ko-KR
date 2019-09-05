---
title: ms-prod-and-technology-invalid
description: Docs 빌드 문제 ms-prod-and-technology-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236304"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="b12e0-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="b12e0-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="b12e0-104">경고</span><span class="sxs-lookup"><span data-stu-id="b12e0-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="b12e0-105">`ms.prod`를 사용하여 온-프레미스 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="b12e0-106">`ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="b12e0-107">`ms.prod` 및 `ms.technology`의 값은 유효한 쌍이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="b12e0-108">`ms.prod` 값이 잘못되었거나, `ms.technology` 값이 `ms.prod`와 유효한 쌍이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b12e0-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="b12e0-109">Resolution</span></span>

<span data-ttu-id="b12e0-110">`ms.prod` 값이 문서에 적합한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="b12e0-111">그런 다음, 유효한 `ms.technology` 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="b12e0-112">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b12e0-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="b12e0-113">새 값을 요청하려면 [관련 절차](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="b12e0-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
