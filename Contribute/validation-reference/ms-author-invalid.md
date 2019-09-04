---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236548"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="3e212-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="3e212-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="3e212-104">경고</span><span class="sxs-lookup"><span data-stu-id="3e212-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="3e212-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="3e212-105">Resolution</span></span>

<span data-ttu-id="3e212-106">`ms.author` 값이 현재 작성자의 유효한 Microsoft 별칭인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e212-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="3e212-107">별칭이 배포 목록이면 허용 목록에도 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e212-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="3e212-108">DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e212-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
