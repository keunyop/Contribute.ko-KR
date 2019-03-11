---
title: block-section-invalid
description: Docs 빌드 문제 block-section-invalid에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 257b963ae37f5a8f0edc2fbca6186ab0f258cfc0
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427891"
---
# <a name="block-section-invalid"></a>block-section-invalid

## <a name="warning"></a>경고

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

몇 가지 Docs Markdown 확장은 `> [!` 문자열로 시작합니다. `>` 및 `[` 사이의 공백이 필요하며 `]` 종료가 있어야 합니다. 구문이 올바르지 않으면 텍스트가 블록 따옴표로 렌더링됩니다.

## <a name="resolution"></a>해결 방법

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

사용 중인 확장에 대한 구문이 올바른지 확인합니다.

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
