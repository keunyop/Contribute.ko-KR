---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791543"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="66c81-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="66c81-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="66c81-104">제안</span><span class="sxs-lookup"><span data-stu-id="66c81-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="66c81-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="66c81-105">Resolution</span></span>

<span data-ttu-id="66c81-106">`ms.author` 값이 현재 작성자의 유효한 Microsoft 별칭인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="66c81-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="66c81-107">별칭이 배포 목록이면 허용 목록에도 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c81-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="66c81-108">DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66c81-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
