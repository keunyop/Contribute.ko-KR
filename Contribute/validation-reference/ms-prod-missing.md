---
title: ms-prod-missing
description: Docs 빌드 문제 ms-prod-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987701"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="0fa19-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="0fa19-103">ms-prod-missing</span></span>

<span data-ttu-id="0fa19-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="0fa19-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0fa19-105">제안</span><span class="sxs-lookup"><span data-stu-id="0fa19-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="0fa19-106">`ms.prod`를 사용하여 온-프레미스 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="0fa19-107">`ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 되지만, `ms.technology`를 지정하는 경우에는 `ms.prod`도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="0fa19-108">`ms.prod` 및 `ms.technology`의 값은 유효한 쌍이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="0fa19-109">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0fa19-109">Resolution</span></span>

<span data-ttu-id="0fa19-110">지정한 `ms.technology` 값이 문서에 적합한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="0fa19-111">그런 다음, `ms.technology`에 유효한 부모인 적절한 `ms.prod` 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="0fa19-112">유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fa19-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
