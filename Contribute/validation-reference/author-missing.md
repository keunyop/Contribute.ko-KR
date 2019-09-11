---
title: author-missing
description: Docs 빌드 문제 author-missing에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848572"
---
# <a name="author-missing"></a><span data-ttu-id="85e13-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="85e13-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="85e13-104">경고</span><span class="sxs-lookup"><span data-stu-id="85e13-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="85e13-105">`author` 특성은 GitHub ID를 기준으로 문서의 작성자를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="85e13-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="85e13-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="85e13-106">Resolution</span></span>

<span data-ttu-id="85e13-107">다음과 같이 현재 작성자의 GitHub ID를 YML 헤더에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="85e13-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="85e13-108">소유권이 변경된 경우 이는 원본 작성자가 아니라 문서의 *현재* 소유자이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e13-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
