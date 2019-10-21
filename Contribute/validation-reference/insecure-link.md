---
title: insecure-link
description: Docs 빌드 문제 insecure-link에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379519"
---
# <a name="insecure-link"></a><span data-ttu-id="9f300-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="9f300-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9f300-104">제안</span><span class="sxs-lookup"><span data-stu-id="9f300-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="9f300-105">이 메시지는 `http`와 함께 명시적인 Markdown 링크를 사용했거나 `www.microsoft.com`과 같은 원시 URL을 사용했음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="9f300-106">원시 URL은 Docs에 게시될 때 안전하지 않은 링크로 변환되며 사용되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="9f300-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="9f300-107">Resolution</span></span>

<span data-ttu-id="9f300-108">`http` 대신 `https`를 사용하도록 모든 URL을 Microsoft 사이트로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="9f300-109">링크가 원시 URL인 경우 `https`로 시작하는 명시적 Markdown 링크로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="9f300-110">VS Code에 대한 Docs Markdown에는 Microsoft 링크의 정리 스크립트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="9f300-111">이 스크립트는 리포지퇴에서 Microsoft 사이트의 모든 링크를 확인하여 링크가 `http` 대신 `https`로 시작하며 `en-us`와 같은 로캘 코드를 포함하지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="9f300-112">스크립트를 실행하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="9f300-113">VS Code용 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="9f300-114">Alt+M을 클릭하여 Markdown 메뉴를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="9f300-115">**정리**를 선택한 후 **Microsoft 링크**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9f300-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
