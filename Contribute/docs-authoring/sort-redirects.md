---
title: 리디렉션 정렬 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack을 통해 리디렉션을 정렬하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336684"
---
# <a name="sort-redirects"></a>리디렉션 정렬

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

docs.microsoft.com 문서 집합이 개선되어 일부 Markdown 파일이 삭제될 예정입니다. Markdown 파일이 삭제되면 삭제된 문서에 대한 모든 참조가 리디렉션을 통해 제대로 확인되도록 리디렉션을 제공해야 합니다. 리디렉션은 *.openpublishing.redirection.json* 파일에 지정됩니다.

1. 명령 팔레트를 열고 <kbd>F1</kbd>(또는 macOS에서 <kbd>⇧⌘P</kbd>)을 누릅니다.
1. 다음을 입력합니다. **Docs: Sort master redirection file**
1. 명령을 선택하여 실행합니다.
1. *.openpublishing.redirection.json* 파일의 변경 내용을 살펴봅니다.

## <a name="considerations"></a>고려 사항

“데이지 체이닝”의 개념은 *.openpublishing.redirection.json* 파일이 원래 설계된 방식에 드러납니다. 시간이 지날수록 리디렉션으로 추가된 파일은 오래된 상태가 됩니다. 파일 A가 삭제되고 파일 B로의 리디렉션이 필요하게 되며 나중에는 파일 B가 삭제되고 파일 C로 리디렉션될 때 이러한 상태가 됩니다. 두 항목 다 C를 가리키도록 하여 A는 C로 리디렉션되고 B는 동일하게 유지하는 것이 이상적입니다. 이렇게 하면 성능이 약간 향상되므로 이 기능에 대한 작업이 활발하게 이루어지고 있습니다.

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![리디렉션 정렬 데모](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
