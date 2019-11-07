---
title: validation-timeout
description: Docs 빌드 문제 validation-timeout에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166788"
---
# <a name="validation-timeout"></a><span data-ttu-id="202a9-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="202a9-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="202a9-104">경고</span><span class="sxs-lookup"><span data-stu-id="202a9-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="202a9-105">서버 상태가 잘못된 것처럼 유효성 검사 서비스에 일시적인 문제가 발생하여 Docs 빌드에서 서비스를 호출하지 못하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="202a9-106">여러 번 시도한 후, 호출 시간이 초과되며 빌드 지연과 빌드 파이프라인이 막히는 것을 방지하기 위해 유효성 검사가 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="202a9-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="202a9-107">Resolution</span></span>

<span data-ttu-id="202a9-108">PR을 닫았다가 다시 열거나 [Docs 포털](https://ops.microsoft.com/#/)을 통해 전체 빌드를 강제로 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="202a9-109">처음 다시 시도 후 서비스 문제가 자체적으로 해결되는 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="202a9-110">Docs 포털을 통해 빌드를 강제로 수행하려면 리포지토리 관리자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="202a9-111">담당 리포지토리 관리자가 누군지 모르거나 강제 빌드 이후에 이 메시지가 계속 표시되면, Microsoft 직원인 경우 [https://SiteHelp](https://SiteHelp)를 통해 이슈를 제출하거나, 외부 기여자인 경우 PR에서 문서의 작성자에게 @멘션하세요.</span><span class="sxs-lookup"><span data-stu-id="202a9-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="202a9-112">리포지토리 관리자인 경우 다음과 같이 전체 빌드를 강제로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="202a9-113">[Docs 포털](https://ops.microsoft.com/#/)로 이동하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="202a9-114">왼쪽 위 모서리에서 검색하여 리포지토리를 찾고 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="202a9-115">:::image type="content" source="media/find-repo.png" alt-text="Docs 포털 검색 상자를 통해 리포지토리 찾기":::</span><span class="sxs-lookup"><span data-stu-id="202a9-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="202a9-116">**빌드 기록** 탭에서 **+ 수동 게시**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="202a9-117">경고가 발생하는 분기(예: 마스터)를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-117">Select the branch that's getting the Warning, such as Master.</span></span>
1. <span data-ttu-id="202a9-118">대상에는 기본값인 **Docs 사이트**를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-118">For target, keep the default, **Docs site**.</span></span>
1. <span data-ttu-id="202a9-119">**Force Publish**(강제 게시) 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="202a9-120">**게시**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-120">Click **Publish**.</span></span>

   <span data-ttu-id="202a9-121">:::image type="content" source="media/force-build.png" alt-text="전체 빌드를 강제로 수행하는 단계":::</span><span class="sxs-lookup"><span data-stu-id="202a9-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="202a9-122">이렇게 하면 분기에서 전체 빌드가 강제로 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="202a9-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
