---
title: internal-bookmark-not-found
description: Docs 빌드 문제 internal-bookmark-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856223"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>경고

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

존재하지 않는 현재 파일 또는 다른 파일의 제목에 연결하려고 합니다.

## <a name="resolution"></a>해결 방법

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

연결하려는 제목을 확인하고 링크를 업데이트합니다.

현재 문서의 섹션에 연결하려면 제목의 단어 앞에 해시 기호를 사용합니다. 제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다. 다음은 한 예입니다.

```markdown
[Managed Disks](#managed-disks)
```

다른 파일의 제목에 연결하려면 해시 기호와 제목의 단어 앞에 해당 파일의 상대 링크를 사용합니다. 제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다. 다음은 한 예입니다.

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
