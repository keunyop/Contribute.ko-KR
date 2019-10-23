---
title: hard-coded-locale
description: Docs 빌드 문제 hard-coded-locale에 대한 설명 및 해결 방법.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0fbc7634e00202fdfdf607b9504744a6d9846792
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590857"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> 콘텐츠 팀이 시간을 두고 영향을 가늠하고 리포지토리를 정리할 계획을 세우도록 처음에 이 규칙을 “제안”으로 활성화했습니다. **그러나 2019년 12월 20일에는 “제안”이 “경고”로 상향 조정됩니다**.

## <a name="suggestion"></a>제안

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다. 영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다. 예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.

다음 사이트는 이 유효성 검사의 범위에 포함됩니다.

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>해결 방법

Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요. 다음은 한 예입니다.

이전:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

이후:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> VS Code에 대한 Docs Markdown에는 Microsoft 링크의 정리 스크립트가 포함됩니다. 이 스크립트는 리포지퇴에서 Microsoft 사이트의 모든 링크를 확인하여 링크가 `http` 대신 `https`로 시작하며 `en-us`와 같은 로캘 코드를 포함하지 않는지 확인합니다. 스크립트를 실행하려면 다음을 수행합니다.
>
> 1. VS Code용 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 확장을 설치합니다.
> 1. Alt+M을 클릭하여 Markdown 메뉴를 엽니다.
> 1. **정리**를 선택한 후 **Microsoft 링크**를 선택합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
