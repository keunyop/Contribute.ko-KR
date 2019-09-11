---
title: author-not-found
description: Docs 빌드 문제 author-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1a41dbc8efc5ba6cadbec3ee9f17cbc6c64ab116
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848619"
---
# <a name="author-not-found"></a><span data-ttu-id="f814a-103">author-not-found</span><span class="sxs-lookup"><span data-stu-id="f814a-103">author-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="f814a-104">경고</span><span class="sxs-lookup"><span data-stu-id="f814a-104">Warning</span></span>

`Invalid value for author: '{value}' is not a valid GitHub ID.`

## <a name="resolution"></a><span data-ttu-id="f814a-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f814a-105">Resolution</span></span>

<span data-ttu-id="f814a-106">현재 작성자의 GitHub ID를 `author` 값으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f814a-106">Add the current author's GitHub ID as the `author` value.</span></span>

<span data-ttu-id="f814a-107">소유권이 변경된 경우 이는 원본 작성자가 아니라 문서의 *현재* 소유자이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f814a-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
