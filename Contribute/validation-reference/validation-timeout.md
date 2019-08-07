---
title: validation-timeout
description: Docs 빌드 문제 validation-timeout에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817399"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>경고

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

서버 상태가 잘못된 것처럼 유효성 검사 서비스에 일시적인 문제가 발생하여 Docs 빌드에서 서비스를 호출하지 못하는 경우가 있습니다. 여러 번 시도한 후, 호출 시간이 초과되며 빌드 지연과 빌드 파이프라인이 막히는 것을 방지하기 위해 유효성 검사가 취소됩니다.

## <a name="resolution"></a>해결 방법

PR을 닫았다가 다시 열거나, Docs 포털을 통해 수동 빌드를 다시 실행합니다(리포지토리 관리자만). 처음 다시 시도 후 서비스 문제가 자체적으로 해결되는 경우가 종종 있습니다. 관리자의 도움이 필요하거나 이 메시지가 계속 표시되면 Microsoft 직원인 경우 [https://SiteHelp](https://SiteHelp)를 통해 이슈를 제출하거나, 외부 기여자인 경우 PR에서 문서의 작성자에게 @멘션하세요.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
