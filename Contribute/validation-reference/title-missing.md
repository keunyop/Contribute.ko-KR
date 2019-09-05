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
# <a name="title-missing"></a><span data-ttu-id="b5f05-103">title-missing</span><span class="sxs-lookup"><span data-stu-id="b5f05-103">title-missing</span></span>

## <a name="warning"></a><span data-ttu-id="b5f05-104">경고</span><span class="sxs-lookup"><span data-stu-id="b5f05-104">Warning</span></span>

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a><span data-ttu-id="b5f05-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="b5f05-105">Resolution</span></span>

<span data-ttu-id="b5f05-106">검색 결과에 표시할 제목 문자열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f05-106">Add a title string to show in search results.</span></span> <span data-ttu-id="b5f05-107">일반적으로 제목은 19~59자여야 하고, 문서의 H1과는 구별되어야 하며, 관련 브랜딩 단어를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f05-107">In general, titles should be between 19 and 59 characters, should be distinct from the H1 of the article, and should include relevant branding words.</span></span> <span data-ttu-id="b5f05-108">제목에 “ | Microsoft Docs”를 포함하면 안 됩니다. 이 문자열은 Docs에서 자동으로 추가되며, 명시적으로 추가해도 무시되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f05-108">You shouldn't include " | Microsoft Docs" in your title - this is added automatically by Docs, and is ignored if you add it explicitly.</span></span> <span data-ttu-id="b5f05-109">“ - Azure”와 같은 브랜딩을 콘텐츠 세트의 모든 제목에 추가하려면 `titleSuffix` 메타데이터 값을 전역으로 설정하거나 폴더에 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f05-109">If you want to add additional branding, such as " - Azure", to all titles in a content set, set the `titleSuffix` metadata value globally or for a folder.</span></span>

<span data-ttu-id="b5f05-110">[https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag)에서 해당 제목이 Google에 어떻게 표시되는지 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5f05-110">You can preview how your title will look in Google on [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).</span></span>

<span data-ttu-id="b5f05-111">Microsoft 직원인 경우 좋은 제목 및 SEO(검색 엔진 최적화)에 대한 자세한 내용은 내부 Contributor 가이드에서 [SEO 기본 사항](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b5f05-111">If you're a Microsoft employee, see [SEO Basics](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) in the internal Contributor Guide for more information about good titles and search engine optimization (SEO).</span></span>

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
