---
title: circular-reference
description: Docs 빌드 문제 circular-reference에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459214"
---
# <a name="circular-reference"></a><span data-ttu-id="400f5-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="400f5-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="400f5-104">오류</span><span class="sxs-lookup"><span data-stu-id="400f5-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="400f5-105">예를 들어 현재 파일에 링크된 포함 파일이거나 현재 파일로 리디렉션된 파일에 대한 링크일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="400f5-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="400f5-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="400f5-106">Resolution</span></span>

<span data-ttu-id="400f5-107">파일의 링크를 검토하고 파일을 링크하거나 자체 포함되지 않도록 필요한 편집을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="400f5-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
