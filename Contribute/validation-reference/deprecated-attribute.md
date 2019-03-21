---
title: deprecated-attribute
description: Docs 빌드 문제 deprecated-attribute에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987793"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Deprecated attribute: ms.component. Use ms.subservice instead.`

`ms.service`를 사용하여 클라우드 서비스를 지정합니다. `ms.service`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.subservice`를 지정하면 됩니다. `ms.component`를 사용하지 마세요. 이 콘텐츠에 더 이상 사용되지 않습니다.

## <a name="resolution"></a>해결 방법

`ms.service` 값이 문서에 적합한지 확인합니다. 그런 다음, 유효한 `ms.subservice` 값을 선택합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/allowlists)에서 찾을 수 있습니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
