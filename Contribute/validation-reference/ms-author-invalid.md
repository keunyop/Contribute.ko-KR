---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481711"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="8c393-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="8c393-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8c393-104">경고</span><span class="sxs-lookup"><span data-stu-id="8c393-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="8c393-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="8c393-105">Resolution</span></span>

<span data-ttu-id="8c393-106">`ms.author` 값이 현재 작성자의 유효한 Microsoft 별칭인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8c393-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="8c393-107">지정된 작성자는 단기 공급 업체가 아닌 상근 직원 또는 팀 배포 목록(DL)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c393-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="8c393-108">별칭이 DL인 경우 `ms.author` 허용 목록에도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c393-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="8c393-109">`ms.author` DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c393-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
