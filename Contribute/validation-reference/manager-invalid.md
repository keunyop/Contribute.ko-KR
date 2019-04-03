---
title: manager-invalid
description: Docs 빌드 문제 manager-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637233"
---
# <a name="manager-invalid"></a>manager-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

일부 콘텐츠 그룹에는 작성자의 관리자를 식별할 수 있는 `manager` 속성이 필요합니다.

## <a name="resolution"></a>해결 방법

`manager`의 값은 Microsoft 직원 각각의 유효한 별칭이어야 합니다. 작성자 관리자의 별칭을 확인하고 값을 업데이트합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
