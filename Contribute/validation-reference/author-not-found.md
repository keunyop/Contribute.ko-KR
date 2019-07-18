---
title: author-not-found
description: Docs 빌드 문제 author-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: af4145b4f6be07f07a22842e6ded279e8390b054
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791581"
---
# <a name="author-not-found"></a><span data-ttu-id="3b75a-103">author-not-found</span><span class="sxs-lookup"><span data-stu-id="3b75a-103">author-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="3b75a-104">경고</span><span class="sxs-lookup"><span data-stu-id="3b75a-104">Warning</span></span>

`Invalid value for author: '{value}' is not a valid GitHub ID.`

## <a name="resolution"></a><span data-ttu-id="3b75a-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="3b75a-105">Resolution</span></span>

<span data-ttu-id="3b75a-106">현재 작성자의 GitHub ID를 `author` 값으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3b75a-106">Add the current author's GitHub ID as the `author` value.</span></span>

<span data-ttu-id="3b75a-107">소유권이 변경된 경우 이는 원본 작성자가 아니라 문서의 *현재* 소유자이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b75a-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
