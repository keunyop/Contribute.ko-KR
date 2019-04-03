---
title: ms-service-and-subservice-invalid
description: Docs 빌드 문제 ms-service-and-subservice-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637302"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

`ms.service`를 사용하여 클라우드 서비스를 지정합니다. `ms.service`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.subservice`를 지정하면 됩니다. `ms.service` 및 `ms.subservice`의 값은 유효한 쌍이어야 합니다. `ms.service` 값이 잘못되었거나, `ms.subservice` 값이 `ms.service`와 유효한 쌍이 아닙니다.

## <a name="resolution"></a>해결 방법

`ms.service` 값이 문서에 적합한지 확인합니다. 그런 다음, 유효한 `ms.subservice` 값을 선택합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
