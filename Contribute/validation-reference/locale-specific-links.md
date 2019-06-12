---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: 로캘별 링크
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841254"
---
# <a name="locale-specific-links"></a>로캘별 링크

`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다. 영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다. 예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.

Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요. 다음은 한 예입니다.

이전:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

이후:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

다음 사이트는 이 유효성 검사의 범위에 포함됩니다.

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com