---
title: h1-in-moniker
description: Docs 빌드 문제 h1-in-moniker에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528818"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

## <a name="warning"></a>경고

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1은 Markdown 파일의 첫 번째 제목을 참조합니다. docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다. H1은 단일 해시(#), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다. 각 파일에는 하나의 H1만 있을 수 있습니다. 모니커에 H1가 있으면 버전 관리를 구성하는 방법에 따라 H1가 쉽게 중복되거나 누락될 수 있으므로 H1는 모니커 섹션에서 허용되지 않습니다.

모니커 섹션에 `=======` 같은 이중 밑줄을 생성하는 등호 줄이 포함된 경우 이 메시지가 표시될 수도 있습니다. 이는 H1의 대체 Markdown 구문입니다. 일반적으로 병합 충돌에서도 확인됩니다.

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>해결 방법

이 문제를 해결하려면 모든 모니커 섹션에서 H1를 제거하고 문서의 맨 위에 있는 H1이 모든 모니커 섹션에 적합한지 확인합니다. H3에서 H1을 팔로우하는 것과 같이 제목 수준을 건너뛰는 것은 허용되지 않습니다.

모니커 섹션의 H1이 실제로 이중 밑줄(`=======`)인 경우 이를 제거하거나 `##` 같은 해시태그 제목으로 바꿉니다. 이중 밑줄이 병합 충돌의 일부인 경우에는 병합 충돌 시작 및 끝 마커와 사용되지 않는 텍스트도 제거해야 합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
