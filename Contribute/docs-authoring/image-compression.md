---
title: 이미지 압축 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack에서 이미지를 압축하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336661"
---
# <a name="image-compression"></a>이미지 압축

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>요약

모든 설명서는 PDF 버전의 문서를 제외하고는 웹을 통해 제공됩니다. 정적 콘텐츠를 제공하는 경우 네트워크를 통해 전송되는 바이트 수를 최소화하는 것이 가장 좋습니다. 바이트 수를 최소화하는 한 가지 방법은 미사용 이미지를 압축하는 것입니다.

Docs Authoring Pack 확장에는 이미지 압축 상황에 맞는 메뉴 항목이 포함되어 있습니다. 지원되는 이미지 형식/확장은 다음과 같습니다.

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

적용 가능한 경우 무손실 이미지 압축 알고리즘이 사용됩니다.

## <a name="compress-image"></a>이미지 압축

**탐색기**의 탐색 창에서 이미지 파일을 마우스 오른쪽 단추로 클릭하고 **이미지 압축** 옵션을 선택합니다. 그러면 이미지가 압축됩니다.

## <a name="compress-images-in-folder"></a>폴더의 이미지 압축

**탐색기**의 탐색 창에서 이미지가 포함된 폴더를 마우스 오른쪽 단추로 클릭하고 **폴더의 이미지 압축** 옵션을 선택합니다. 폴더의 이미지가 모두 압축됩니다.

## <a name="considerations"></a>고려 사항

해상도가 높은 이미지는 암시적으로 크기가 조정됩니다. 최대 크기는 플랫폼에서 제안하는 최대 너비인 `1,200px`를 기준으로 합니다. 최댓값은 이미지가 권장 사항보다 큰 경우에만 사용되며 자동으로 크기가 조정될 때 가로 세로 비율이 유지됩니다.

## <a name="preferences"></a>기본 설정

최대 크기를 구성할 수 있으나 `1200` 픽셀인 기본 최대 너비가 있습니다. 최대 크기를 구성하려면 **파일 -> 기본 설정 -> 설정**을 선택하고 `"Docs Image Extension"`을 기준으로 필터링합니다.

:::image type="content" source="media/configure-image-compression.png" alt-text="이미지 압축 구성":::

> [!NOTE]
> **최대 너비** 또는 **최대 높이**의 `0` 값은 해상도 차이를 무시합니다.

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![이미지 압축 데모](media/compress-image.gif)](media/compress-image.gif#lightbox)
