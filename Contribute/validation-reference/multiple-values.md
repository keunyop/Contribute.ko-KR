---
title: multiple-values
description: Docs 빌드 문제 multiple-values에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637331"
---
# <a name="multiple-values"></a><span data-ttu-id="0e9bb-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="0e9bb-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0e9bb-104">제안</span><span class="sxs-lookup"><span data-stu-id="0e9bb-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="0e9bb-105">값이 하나만 허용되는 특성에 둘 이상의 값을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="0e9bb-106">둘 이상의 값이 허용되지 않는 특성은 단일 값(스칼라) YML 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e9bb-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0e9bb-107">Resolution</span></span>

<span data-ttu-id="0e9bb-108">다중 값 배열이 단일 값 특성(여러 값이 포함되었거나 배열의 단일 값)에 사용될 때마다 이 제안을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="0e9bb-109">YML은 다중 값 특성(예: `ms.custom`)에 다음과 같은 배열 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="0e9bb-110">해당 형식은 단일 값 특성(예: `author`)에는 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="0e9bb-111">다중 값을 지정한 경우 지정된 값을 검토하고 어떤 값이 올바른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="0e9bb-112">다른 값을 제거하고 다음과 같이 대괄호 없이 특성과 같은 줄에 단일 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="0e9bb-113">단일 값 배열이 있는 경우 위의 스칼라 형식으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="0e9bb-113">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
