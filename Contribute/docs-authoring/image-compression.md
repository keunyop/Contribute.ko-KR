---
title: 이미지 압축 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack에서 이미지를 압축하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336661"
---
# <a name="image-compression"></a><span data-ttu-id="bbf74-103">이미지 압축</span><span class="sxs-lookup"><span data-stu-id="bbf74-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="bbf74-104">요약</span><span class="sxs-lookup"><span data-stu-id="bbf74-104">Summary</span></span>

<span data-ttu-id="bbf74-105">모든 설명서는 PDF 버전의 문서를 제외하고는 웹을 통해 제공됩니다. 정적 콘텐츠를 제공하는 경우 네트워크를 통해 전송되는 바이트 수를 최소화하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="bbf74-106">바이트 수를 최소화하는 한 가지 방법은 미사용 이미지를 압축하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="bbf74-107">Docs Authoring Pack 확장에는 이미지 압축 상황에 맞는 메뉴 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="bbf74-108">지원되는 이미지 형식/확장은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="bbf74-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="bbf74-109">*\*.png*</span></span>
* <span data-ttu-id="bbf74-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="bbf74-110">*\*.jpg*</span></span>
* <span data-ttu-id="bbf74-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="bbf74-111">*\*.jpeg*</span></span>
* <span data-ttu-id="bbf74-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="bbf74-112">*\*.gif*</span></span>
* <span data-ttu-id="bbf74-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="bbf74-113">*\*.svg*</span></span>
* <span data-ttu-id="bbf74-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="bbf74-114">*\*.webp*</span></span>

<span data-ttu-id="bbf74-115">적용 가능한 경우 무손실 이미지 압축 알고리즘이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="bbf74-116">이미지 압축</span><span class="sxs-lookup"><span data-stu-id="bbf74-116">Compress image</span></span>

<span data-ttu-id="bbf74-117">**탐색기**의 탐색 창에서 이미지 파일을 마우스 오른쪽 단추로 클릭하고 **이미지 압축** 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="bbf74-118">그러면 이미지가 압축됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="bbf74-119">폴더의 이미지 압축</span><span class="sxs-lookup"><span data-stu-id="bbf74-119">Compress images in folder</span></span>

<span data-ttu-id="bbf74-120">**탐색기**의 탐색 창에서 이미지가 포함된 폴더를 마우스 오른쪽 단추로 클릭하고 **폴더의 이미지 압축** 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="bbf74-121">폴더의 이미지가 모두 압축됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="bbf74-122">고려 사항</span><span class="sxs-lookup"><span data-stu-id="bbf74-122">Considerations</span></span>

<span data-ttu-id="bbf74-123">해상도가 높은 이미지는 암시적으로 크기가 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="bbf74-124">최대 크기는 플랫폼에서 제안하는 최대 너비인 `1,200px`를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="bbf74-125">최댓값은 이미지가 권장 사항보다 큰 경우에만 사용되며 자동으로 크기가 조정될 때 가로 세로 비율이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="bbf74-126">기본 설정</span><span class="sxs-lookup"><span data-stu-id="bbf74-126">Preferences</span></span>

<span data-ttu-id="bbf74-127">최대 크기를 구성할 수 있으나 `1200` 픽셀인 기본 최대 너비가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="bbf74-128">최대 크기를 구성하려면 **파일 -> 기본 설정 -> 설정**을 선택하고 `"Docs Image Extension"`을 기준으로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="이미지 압축 구성":::

> [!NOTE]
> <span data-ttu-id="bbf74-130">**최대 너비** 또는 **최대 높이**의 `0` 값은 해상도 차이를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="bbf74-131">예제</span><span class="sxs-lookup"><span data-stu-id="bbf74-131">In action</span></span>

<span data-ttu-id="bbf74-132">다음은 이 기능에 대한 간단한 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf74-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="bbf74-133">[![이미지 압축 데모](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bbf74-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
