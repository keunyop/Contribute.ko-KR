---
title: validation-timeout
description: Docs 빌드 문제 validation-timeout에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024213"
---
# <a name="validation-timeout"></a><span data-ttu-id="eb656-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="eb656-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="eb656-104">경고</span><span class="sxs-lookup"><span data-stu-id="eb656-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="eb656-105">서버 상태가 잘못된 것처럼 유효성 검사 서비스에 일시적인 문제가 발생하여 Docs 빌드에서 서비스를 호출하지 못하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb656-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="eb656-106">세 번 시도 후, 호출 시간이 초과되며 빌드 지연과 빌드 파이프라인이 막히는 것을 방지하기 위해 유효성 검사가 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb656-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="eb656-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="eb656-107">Resolution</span></span>

<span data-ttu-id="eb656-108">PR을 닫았다가 다시 열거나, 수동 빌드를 다시 실행합니다(리포지토리 관리자만).</span><span class="sxs-lookup"><span data-stu-id="eb656-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="eb656-109">처음 다시 시도 후 서비스 문제가 자체적으로 해결되는 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb656-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="eb656-110">메시지가 계속 표시되면 Microsoft 직원인 경우 [https://SiteHelp](https://SiteHelp)를 통해 이슈를 제출하거나, 외부 기여자인 경우 PR에서 문서의 작성자에게 @멘션하세요.</span><span class="sxs-lookup"><span data-stu-id="eb656-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
