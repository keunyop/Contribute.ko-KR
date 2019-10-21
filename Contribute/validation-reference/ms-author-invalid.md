---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246298"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="8e563-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="8e563-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8e563-104">경고</span><span class="sxs-lookup"><span data-stu-id="8e563-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="8e563-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="8e563-105">Resolution</span></span>

<span data-ttu-id="8e563-106">현재 작성자의 유효한 Microsoft 별칭으로 `ms.author` 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8e563-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="8e563-107">지정된 작성자는 단기 공급 업체가 아닌 상근 직원 또는 팀 DL(배포 목록)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e563-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="8e563-108">별칭이 DL인 경우 `ms.author` 허용 목록에도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e563-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="8e563-109">`ms.author` DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e563-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
