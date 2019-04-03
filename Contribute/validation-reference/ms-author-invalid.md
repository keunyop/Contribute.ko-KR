---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636727"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="c95ab-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="c95ab-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c95ab-104">제안</span><span class="sxs-lookup"><span data-stu-id="c95ab-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="c95ab-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="c95ab-105">Resolution</span></span>

<span data-ttu-id="c95ab-106">`ms.author` 값이 유효한 Microsoft 별칭인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c95ab-106">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="c95ab-107">별칭이 배포 목록이면 허용 목록에도 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c95ab-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="c95ab-108">DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c95ab-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
