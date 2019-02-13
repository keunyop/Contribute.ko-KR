---
title: ms-prod-and-technology-invalid
description: Docs 빌드 문제 ms-prod-and-technology-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713272"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**서비스 예정!**

## <a name="warning"></a>경고

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

`ms.prod`를 사용하여 온-프레미스 제품을 지정합니다. `ms.prod`에 대한 더 자세한 정보를 지정하려면 필요에 따라 `ms.technology`를 지정하면 됩니다. `ms.prod` 및 `ms.technology`의 값은 유효한 쌍이어야 합니다. `ms.prod` 값이 잘못되었거나, `ms.technology` 값이 `ms.prod`와 유효한 쌍이 아닙니다.

## <a name="resolution"></a>해결 방법

`ms.prod` 값이 문서에 적합한지 확인합니다. 그런 다음, 유효한 `ms.technology` 값을 선택합니다.

유효한 값은 [이 Microsoft 내부 사이트](https://docsmetadatatool.azurewebsites.net/whitelists)에서 찾을 수 있습니다.

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
