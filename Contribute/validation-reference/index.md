---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084620"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="646e8-101">Docs PR 유효성 검사 서비스</span><span class="sxs-lookup"><span data-stu-id="646e8-101">Docs PR validation service</span></span>

<span data-ttu-id="646e8-102">Docs PR 유효성 검사 서비스는 PR에서 파일에 대해 유효성 검사 규칙을 실행하는 GitHub 앱입니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="646e8-103">리포지토리에서 유효성 검사 서비스를 수행할 수 있도록 설정하면 다음 동작이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="646e8-104">PR을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-104">You submit a PR.</span></span>
1. <span data-ttu-id="646e8-105">PR의 상태를 나타내는 GitHub 주석에는 리포지토리에 대해 설정된 “확인”의 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="646e8-106">이 예에는 “Commit Validation”과 “OpenPublishing.Build”, 이렇게 두 가지 확인을 사용할 수 있도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![일부 확인 실패](media/validation-failed.png)

   <span data-ttu-id="646e8-108">커밋 유효성 검사에 실패하더라도 빌드가 성공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="646e8-109">자세한 내용을 알려면 **세부 정보**를 클릭하세요.</span><span class="sxs-lookup"><span data-stu-id="646e8-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="646e8-110">세부 정보 페이지에는 문제 수정 방법에 대한 정보와 함께 실패한 모든 유효성 검사가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="646e8-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![유효성 검사 메시지](media/validation-details.png)

<span data-ttu-id="646e8-112">현재 서비스 중인 유효성 검사 목록이 필요하면 이 문서의 왼쪽 목차를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="646e8-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>