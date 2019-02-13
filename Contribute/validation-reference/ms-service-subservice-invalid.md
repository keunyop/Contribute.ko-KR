---
title: ms-service-and-subservice-invalid
description: Docs 빌드 문제 ms-service-and-subservice-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713134"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="35ace-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="35ace-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="35ace-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="35ace-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="35ace-105">경고</span><span class="sxs-lookup"><span data-stu-id="35ace-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="35ace-106">`ms.service`를 사용하여 클라우드 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="35ace-107">`ms.service`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.subservice`를 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="35ace-108">`ms.service` 및 `ms.subservice`의 값은 유효한 쌍이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="35ace-109">`ms.service` 값이 잘못되었거나, `ms.subservice` 값이 `ms.service`와 유효한 쌍이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="35ace-110">해결 방법</span><span class="sxs-lookup"><span data-stu-id="35ace-110">Resolution</span></span>

<span data-ttu-id="35ace-111">`ms.service` 값이 문서에 적합한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="35ace-112">그런 다음, 유효한 `ms.subservice` 값을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="35ace-113">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/whitelists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ace-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
