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
# <a name="reformat-markdown-tables"></a><span data-ttu-id="22d31-103">Markdown 테이블 서식 다시 지정</span><span class="sxs-lookup"><span data-stu-id="22d31-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="22d31-104">요약</span><span class="sxs-lookup"><span data-stu-id="22d31-104">Summary</span></span>

<span data-ttu-id="22d31-105">Markdown( *\*.md*) 파일에서 전체 테이블을 선택하면 두 개의 테이블 서식 지정 상황에 맞는 메뉴 항목을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="22d31-106">선택한 Markdown 테이블을 마우스 오른쪽 단추로 클릭하여 상황에 맞는 메뉴를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="22d31-107">다음과 유사한 메뉴 항목이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="테이블 서식 다시 지정 상황에 맞는 메뉴":::

> [!TIP]
> <span data-ttu-id="22d31-109">이 기능은 여러 테이블이 선택된 경우 작동하지 **않으며** 단일 Markdown 테이블을 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="22d31-110">원하는 결과에 대한 제목을 포함하여 전체 테이블을 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="22d31-111">선택한 테이블 통합</span><span class="sxs-lookup"><span data-stu-id="22d31-111">Consolidate selected table</span></span>

<span data-ttu-id="22d31-112">**선택한 테이블 통합** 옵션을 선택하면 각 값의 한쪽에 공간이 하나만 있는 상태에서 테이블 제목 및 콘텐츠가 축소됩니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="22d31-113">선택한 테이블 균등 맞춤</span><span class="sxs-lookup"><span data-stu-id="22d31-113">Evenly distribute selected table</span></span>

<span data-ttu-id="22d31-114">**선택한 테이블 균등 맞춤** 옵션을 선택하면 각 열에서 가장 긴 값을 계산하여 다른 모든 값을 공간에 맞게 균등 맞춤합니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="22d31-115">고려 사항</span><span class="sxs-lookup"><span data-stu-id="22d31-115">Considerations</span></span>

<span data-ttu-id="22d31-116">이 기능은 테이블 렌더링에 영향을 주지 않지만 테이블 가독성을 높이는 데 도움을 주므로 유지 관리를 더 쉽게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="22d31-117">테이블 서식 다시 지정 기능은 열 맞춤을 그대로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="22d31-118">다음 테이블을 살펴보세요.</span><span class="sxs-lookup"><span data-stu-id="22d31-118">Consider the following table:</span></span>

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

<span data-ttu-id="22d31-119">“균등 맞춤”된 후 테이블은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-119">After being "evenly distributed":</span></span>

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

<span data-ttu-id="22d31-120">“통합”된 후 테이블은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-120">After being "consolidated":</span></span>

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

## <a name="in-action"></a><span data-ttu-id="22d31-121">예제</span><span class="sxs-lookup"><span data-stu-id="22d31-121">In action</span></span>

<span data-ttu-id="22d31-122">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="22d31-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="22d31-123">[![테이블 서식 다시 지정 데모](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="22d31-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
