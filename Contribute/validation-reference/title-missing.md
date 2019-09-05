---
title: title-missing
description: Docs 빌드 문제 title-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236559"
---
# <a name="title-missing"></a>title-missing

## <a name="warning"></a>경고

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a>해결 방법

검색 결과에 표시할 제목 문자열을 추가합니다. 일반적으로 제목은 19~59자여야 하고, 문서의 H1과는 구별되어야 하며, 관련 브랜딩 단어를 포함해야 합니다. 제목에 “ | Microsoft Docs”를 포함하면 안 됩니다. 이 문자열은 Docs에서 자동으로 추가되며, 명시적으로 추가해도 무시되기 때문입니다. “ - Azure”와 같은 브랜딩을 콘텐츠 세트의 모든 제목에 추가하려면 `titleSuffix` 메타데이터 값을 전역으로 설정하거나 폴더에 설정합니다.

[https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag)에서 해당 제목이 Google에 어떻게 표시되는지 미리 볼 수 있습니다.

Microsoft 직원인 경우 좋은 제목 및 SEO(검색 엔진 최적화)에 대한 자세한 내용은 내부 Contributor 가이드에서 [SEO 기본 사항](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master)을 참조하세요.

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
