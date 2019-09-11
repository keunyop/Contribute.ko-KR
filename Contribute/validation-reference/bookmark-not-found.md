---
title: internal-bookmark-not-found
description: Docs 빌드 문제 internal-bookmark-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856223"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="4c669-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="4c669-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="4c669-104">경고</span><span class="sxs-lookup"><span data-stu-id="4c669-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="4c669-105">존재하지 않는 현재 파일 또는 다른 파일의 제목에 연결하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="4c669-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="4c669-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="4c669-107">연결하려는 제목을 확인하고 링크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="4c669-108">현재 문서의 섹션에 연결하려면 제목의 단어 앞에 해시 기호를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="4c669-109">제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="4c669-110">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="4c669-111">다른 파일의 제목에 연결하려면 해시 기호와 제목의 단어 앞에 해당 파일의 상대 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="4c669-112">제목에서 문장 부호를 제거하고 공간을 대시로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="4c669-113">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4c669-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
