---
title: internal-bookmark-not-found
description: Docs 빌드 문제 internal-bookmark-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427832"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="aff32-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="aff32-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="aff32-104">**서비스 예정!**</span><span class="sxs-lookup"><span data-stu-id="aff32-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="aff32-105">제안</span><span class="sxs-lookup"><span data-stu-id="aff32-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="aff32-106">존재하지 않는 현재 파일의 제목에 연결하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff32-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="aff32-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="aff32-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="aff32-108">연결하려는 제목을 확인하고 링크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aff32-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="aff32-109">현재 문서의 섹션에 연결하려면 제목의 단어 뒤에 해시 기호를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="aff32-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="aff32-110">제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="aff32-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="aff32-111">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="aff32-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
