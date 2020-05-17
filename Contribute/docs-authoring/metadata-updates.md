---
title: 메타데이터 업데이트 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack의 메타데이터를 업데이트하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336638"
---
# <a name="update-metadata"></a><span data-ttu-id="ecc2b-103">메타데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="ecc2b-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="ecc2b-104">요약</span><span class="sxs-lookup"><span data-stu-id="ecc2b-104">Summary</span></span>

<span data-ttu-id="ecc2b-105">Markdown( *\*.md*) 파일에는 메타데이터와 관련된 두 개의 상황에 맞는 메뉴 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="ecc2b-106">텍스트 편집기의 아무 곳이나 마우스 오른쪽 단추로 클릭하면 다음과 유사한 메뉴 항목이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="메타데이터 업데이트 상황에 맞는 메뉴":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="ecc2b-108">`ms.date` 메타데이터 값 업데이트</span><span class="sxs-lookup"><span data-stu-id="ecc2b-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="ecc2b-109">**`ms.date` 메타데이터 값 업데이트** 옵션을 선택하면 현재 Markdown 파일 `ms.date` 값이 오늘 날짜로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="ecc2b-110">문서에 `ms.date` 메타데이터 필드가 없으면 아무 작업도 수행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="ecc2b-111">암시적 메타데이터 값 업데이트</span><span class="sxs-lookup"><span data-stu-id="ecc2b-111">Update implicit metadata values</span></span>

<span data-ttu-id="ecc2b-112">**암시적 메타데이터 값 업데이트** 옵션을 선택하면 암시적으로 지정할 수 있는 모든 가능한 메타데이터 값을 찾아 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="ecc2b-113">메타데이터 값은 *docfx.json* 파일의 `build/fileMetadata` 노드에서 암시적으로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="ecc2b-114">`fileMetadata` 노드에 있는 각각의 키 값 쌍은 메타데이터 기본값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="ecc2b-115">예를 들어 `ms.author` 메타데이터 값을 생략하는 *top-level/sub-folder* 디렉터리의 Markdown 파일은 `fileMetadata` 노드에 사용할 기본값을 암시적으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="ecc2b-116">이 경우 모든 Markdown 파일이 `ms.author: dapine` 메타데이터 값을 암시적으로 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="ecc2b-117">이 기능은 *docfx.json* 파일에 있는 이러한 암시적 설정에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="ecc2b-118">Markdown 파일에 암시적 값이 아닌 값으로 명시적으로 설정된 값을 사용하는 메타데이터가 있는 경우 해당 값은 재정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="ecc2b-119">다음 Markdown 파일 메타데이터를 살펴보세요. 이 Markdown 파일은 **top-level/sub-folder/includes/example.md**에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="ecc2b-120">이 파일에서 **암시적 메타데이터 값 업데이트** 옵션이 실행된 경우 위의 *docfx.json* 콘텐츠를 사용하는 것으로 가정하면 메타데이터 값이 `ms.author: dapine`로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="ecc2b-121">예제</span><span class="sxs-lookup"><span data-stu-id="ecc2b-121">In action</span></span>

<span data-ttu-id="ecc2b-122">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="ecc2b-123">[![메타데이터 업데이트 데모](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ecc2b-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
