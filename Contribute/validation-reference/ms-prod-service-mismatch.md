---
title: ms-prod-service-mismatch
description: Docs 빌드 문제 ms-prod-service-mismatch에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987618"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

`ms.prod`를 사용하여 온-프레미스 제품을 지정하고 클라우드 서비스에는 `ms.service`를 사용합니다. `ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 됩니다. `ms.service`에 대한 더 자세한 정보를 지정하려면 `ms.subservice`를 지정하면 됩니다. `ms.prod`와 `ms.subservice`를 함께 사용하거나 `ms.service`와 `ms.technology`를 함께 사용할 수는 없습니다.

## <a name="resolution"></a>해결 방법

먼저, 문서의 올바른 부모 특성(`ms.prod` 또는 `ms.service`)을 선택했는지 확인합니다. 그런 다음, 유효한 쌍 값으로 적절한 자식 필드를 추가합니다. 추가 필드를 제거합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
