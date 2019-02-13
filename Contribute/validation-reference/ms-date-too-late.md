---
title: ms-date-too-late
description: Docs 빌드 문제 ms-date-too-late에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713111"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**서비스 예정!**

## <a name="warning"></a>경고

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` 특성은 “유효 시간”(문서의 관련성, 정확성, 올바른 스크린샷 및 작업 링크가 마지막으로 검토된 시간)을 나타내는 데 사용됩니다. 따라서 미래의 날짜를 지정할 수는 없습니다. 주요 이벤트를 준비하면서 QA 콘텐츠가 동결되는 경우와 같이 5일의 릴리스 시간을 고려할 수 있습니다.

## <a name="resolution"></a>해결 방법

YYYY/MM/DD 형식으로 오늘부터 5일 이내의 `ms.date`를 지정합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
