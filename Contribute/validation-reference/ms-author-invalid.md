---
title: ms-author-invalid
description: Docs 빌드 문제 ms-author-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987770"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="c19c4-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="c19c4-103">ms-author-invalid</span></span>

<span data-ttu-id="c19c4-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="c19c4-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c19c4-105">제안</span><span class="sxs-lookup"><span data-stu-id="c19c4-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="c19c4-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="c19c4-106">Resolution</span></span>

<span data-ttu-id="c19c4-107">`ms.author` 값이 유효한 Microsoft 별칭인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c19c4-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="c19c4-108">별칭이 배포 목록이면 허용 목록에도 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c19c4-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="c19c4-109">DL에서 유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c19c4-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
