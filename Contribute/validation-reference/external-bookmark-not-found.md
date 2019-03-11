---
title: external-bookmark-not-found
description: Docs 빌드 문제 external-bookmark-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427772"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>경고

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

존재하지 않는 다른 파일의 제목에 연결하려고 합니다.

## <a name="resolution"></a>해결 방법

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

연결할 파일을 검토하고 파일의 유효한 섹션을 가리키도록 책갈피 링크를 업데이트합니다.

다른 문서의 섹션 제목에 연결하려면 파일 관련 또는 사이트 관련 링크와 해시 기호를 더하여 뒤에 오는 제목의 단어를 사용합니다. 제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다. 다음은 한 예입니다.

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
