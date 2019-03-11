---
title: internal-bookmark-not-found
description: Docs 빌드 문제 internal-bookmark-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427832"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**서비스 예정!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>제안

`Current file doesn't contain a bookmark named '{bookmark}'.`

존재하지 않는 현재 파일의 제목에 연결하려고 합니다.

## <a name="resolution"></a>해결 방법

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

연결하려는 제목을 확인하고 링크를 업데이트합니다.

현재 문서의 섹션에 연결하려면 제목의 단어 뒤에 해시 기호를 사용합니다. 제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다. 다음은 한 예입니다.

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
