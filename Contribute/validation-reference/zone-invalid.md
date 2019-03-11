---
title: zone-invalid
description: Docs 빌드 문제 zone-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/4/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0f654d553dcb48cadfc305b91e4f809e3fa69fc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57461721"
---
# <a name="zone-invalid"></a><span data-ttu-id="a262c-103">zone-invalid</span><span class="sxs-lookup"><span data-stu-id="a262c-103">zone-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="a262c-104">경고</span><span class="sxs-lookup"><span data-stu-id="a262c-104">Warning</span></span>

`Invalid zone: No "::: zone-end" found. Blocks should be explicitly closed.`

## <a name="resolution"></a><span data-ttu-id="a262c-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="a262c-105">Resolution</span></span>

<span data-ttu-id="a262c-106">영역 끝에 `::: zone-end`를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a262c-106">Add `::: zone-end` at the end of your zone.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
