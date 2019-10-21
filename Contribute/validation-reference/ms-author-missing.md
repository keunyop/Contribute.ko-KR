---
title: ms-author-missing
description: Docs 빌드 문제 ms-author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246248"
---
# <a name="ms-author-missing"></a><span data-ttu-id="06e1d-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="06e1d-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="06e1d-104">경고</span><span class="sxs-lookup"><span data-stu-id="06e1d-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="06e1d-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="06e1d-105">Resolution</span></span>

<span data-ttu-id="06e1d-106">`ms.author`에 대한 현재 작성자의 Microsoft 별칭을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1d-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="06e1d-107">소유권이 변경된 경우 이는 원본 작성자가 아니라 문서의 *현재* 소유자이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1d-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="06e1d-108">지정된 작성자는 단기 공급 업체가 아닌 상근 직원 또는 팀 DL(배포 목록)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1d-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="06e1d-109">별칭이 DL인 경우 `ms.author` 허용 목록에도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1d-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="06e1d-110">`ms.author` DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06e1d-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
