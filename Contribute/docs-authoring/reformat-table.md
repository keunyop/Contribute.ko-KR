---
title: Markdown 테이블 서식 다시 지정 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack의 다양한 Markdown 테이블 서식 지정 기능을 사용하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336776"
---
# <a name="reformat-markdown-tables"></a>Markdown 테이블 서식 다시 지정

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

Markdown( *\*.md*) 파일에서 전체 테이블을 선택하면 두 개의 테이블 서식 지정 상황에 맞는 메뉴 항목을 사용할 수 있습니다. 선택한 Markdown 테이블을 마우스 오른쪽 단추로 클릭하여 상황에 맞는 메뉴를 엽니다. 다음과 유사한 메뉴 항목이 표시됩니다.

:::image type="content" source="media/reformat-table-menu.png" alt-text="테이블 서식 다시 지정 상황에 맞는 메뉴":::

> [!TIP]
> 이 기능은 여러 테이블이 선택된 경우 작동하지 **않으며** 단일 Markdown 테이블을 대상으로 합니다. 원하는 결과에 대한 제목을 포함하여 전체 테이블을 선택해야 합니다.

## <a name="consolidate-selected-table"></a>선택한 테이블 통합

**선택한 테이블 통합** 옵션을 선택하면 각 값의 한쪽에 공간이 하나만 있는 상태에서 테이블 제목 및 콘텐츠가 축소됩니다.

## <a name="evenly-distribute-selected-table"></a>선택한 테이블 균등 맞춤

**선택한 테이블 균등 맞춤** 옵션을 선택하면 각 열에서 가장 긴 값을 계산하여 다른 모든 값을 공간에 맞게 균등 맞춤합니다.

## <a name="considerations"></a>고려 사항

이 기능은 테이블 렌더링에 영향을 주지 않지만 테이블 가독성을 높이는 데 도움을 주므로 유지 관리를 더 쉽게 할 수 있습니다. 테이블 서식 다시 지정 기능은 열 맞춤을 그대로 유지합니다.

다음 테이블을 살펴보세요.

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

“균등 맞춤”된 후 테이블은 다음과 같습니다.

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

“통합”된 후 테이블은 다음과 같습니다.

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![테이블 서식 다시 지정 데모](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
