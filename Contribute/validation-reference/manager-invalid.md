---
title: manager-invalid
description: Docs 빌드 문제 manager-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7eac188b16b402767bbec551a6dec8b5877680af
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427652"
---
# <a name="manager-invalid"></a><span data-ttu-id="4c933-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="4c933-103">manager-invalid</span></span>

<span data-ttu-id="4c933-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="4c933-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4c933-105">제안</span><span class="sxs-lookup"><span data-stu-id="4c933-105">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="4c933-106">일부 콘텐츠 그룹에는 작성자의 관리자를 식별할 수 있는 `manager` 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4c933-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="4c933-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="4c933-107">Resolution</span></span>

<span data-ttu-id="4c933-108">`manager`의 값은 Microsoft 직원 각각의 유효한 별칭이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c933-108">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="4c933-109">작성자 관리자의 별칭을 확인하고 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4c933-109">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
