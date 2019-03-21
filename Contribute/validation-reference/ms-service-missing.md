---
title: ms-service-missing
description: Docs 빌드 문제 ms-service-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987724"
---
# <a name="ms-service-missing"></a>ms-service-missing

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

`ms.service`를 사용하여 클라우드 서비스를 지정합니다. `ms.service`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.subservice`를 지정하면 되지만, `ms.subservice`를 지정하는 경우에는 `ms.service`도 지정해야 합니다. `ms.service` 및 `ms.subservice`의 값은 유효한 쌍이어야 합니다.

## <a name="resolution"></a>해결 방법

지정한 `ms.subservice` 값이 문서에 적합한지 확인합니다. 그런 다음, `ms.subservice`에 유효한 부모인 적절한 `ms.service` 값을 추가합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
