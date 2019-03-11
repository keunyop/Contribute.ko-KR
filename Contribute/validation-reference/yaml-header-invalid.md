---
title: yaml-header-invalid
description: Docs 빌드 문제 yaml-header-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459030"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="3c3f3-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="3c3f3-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="3c3f3-104">경고</span><span class="sxs-lookup"><span data-stu-id="3c3f3-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="3c3f3-105">일반적으로 YAML 헤더의 따옴표가 없는 메타데이터 값에는 콜론이나 다른 특수 문자가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c3f3-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="3c3f3-106">키/값 쌍의 콜론 뒤에 공백이 누락되었다는 것을 의미할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c3f3-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c3f3-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="3c3f3-107">Resolution</span></span>

<span data-ttu-id="3c3f3-108">YAML 헤더를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="3c3f3-108">Review your YAML header.</span></span> <span data-ttu-id="3c3f3-109">다음 오류를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3c3f3-109">Look for the following mistakes.</span></span>

<span data-ttu-id="3c3f3-110">따옴표가 없는 값의 콜론:</span><span class="sxs-lookup"><span data-stu-id="3c3f3-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="3c3f3-111">변경 대상:</span><span class="sxs-lookup"><span data-stu-id="3c3f3-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="3c3f3-112">키/값 쌍의 콜론 뒤에 공백 없음:</span><span class="sxs-lookup"><span data-stu-id="3c3f3-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="3c3f3-113">변경 대상:</span><span class="sxs-lookup"><span data-stu-id="3c3f3-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
