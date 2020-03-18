---
title: 선택 영역 정렬 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack의 선택 영역 정렬 기능을 사용하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336753"
---
# <a name="sort-selection"></a>선택 영역 정렬

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

Markdown( *\*.md*) 파일에서 선택을 수행하면 두 개의 정렬 상황에 맞는 메뉴 항목을 사용할 수 있습니다. 선택한 텍스트를 마우스 오른쪽 단추로 클릭하여 상황에 맞는 메뉴를 엽니다. 다음과 유사한 메뉴 항목이 표시됩니다.

:::image type="content" source="media/sort-selection-menu.png" alt-text="선택 영역 정렬 상황에 맞는 메뉴":::

> [!TIP]
> Visual Studio Code 텍스트 편집기에서 유효한 선택이 수행될 때까지 정렬 상황에 맞는 메뉴 항목은 숨겨져 있습니다.

## <a name="sort-selection-ascending-a-to-z"></a>선택 영역 오름차순 정렬(A - Z)

**선택 영역 오름차순 정렬(A - Z)** 옵션을 선택하면 전체 선택 영역을 사전순으로 A부터 Z까지 오름차순으로 정렬합니다.

## <a name="sort-selection-descending-z-to-a"></a>선택 영역 내림차순 정렬(Z - A)

**선택 영역 내림차순 정렬(Z - A)** 옵션을 선택하면 전체 선택 영역을 사전순으로 Z부터 A까지 내림차순으로 정렬합니다.

## <a name="considerations"></a>고려 사항

기본 정렬 메커니즘은 ‘자연어’ 정렬을 사용합니다.  기본 정렬은 표준 정렬보다 더 강력하고 포괄적입니다. 다음 테이블을 살펴보세요.

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

자연어 정렬을 사용하지 않으면 `Column1`의 순서가 1, 11, 2 등이 되지만 대신 11이 2보다 큼을 이해하며 다음과 같이 오름차순으로 정렬됩니다.

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![선택 영역 정렬 데모](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
