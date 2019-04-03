---
title: ms-prod-missing
description: Docs 빌드 문제 ms-prod-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636773"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

`ms.prod`를 사용하여 온-프레미스 제품을 지정합니다. `ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 되지만, `ms.technology`를 지정하는 경우에는 `ms.prod`도 지정해야 합니다. `ms.prod` 및 `ms.technology`의 값은 유효한 쌍이어야 합니다.

## <a name="resolution"></a>해결 방법

지정한 `ms.technology` 값이 문서에 적합한지 확인합니다. 그런 다음, `ms.technology`에 유효한 부모인 적절한 `ms.prod` 값을 추가합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
