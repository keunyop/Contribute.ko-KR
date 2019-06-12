---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: 로캘별 링크
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841254"
---
# <a name="locale-specific-links"></a><span data-ttu-id="10605-102">로캘별 링크</span><span class="sxs-lookup"><span data-stu-id="10605-102">Locale-specific links</span></span>

<span data-ttu-id="10605-103">`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="10605-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="10605-104">영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10605-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="10605-105">예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="10605-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="10605-106">Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="10605-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="10605-107">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="10605-107">The following is an example.</span></span>

<span data-ttu-id="10605-108">이전:</span><span class="sxs-lookup"><span data-stu-id="10605-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="10605-109">이후:</span><span class="sxs-lookup"><span data-stu-id="10605-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="10605-110">다음 사이트는 이 유효성 검사의 범위에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="10605-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="10605-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="10605-111">azure.microsoft.com</span></span>
- <span data-ttu-id="10605-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="10605-112">docs.microsoft.com</span></span>
- <span data-ttu-id="10605-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="10605-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="10605-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="10605-114">technet.microsoft.com</span></span>