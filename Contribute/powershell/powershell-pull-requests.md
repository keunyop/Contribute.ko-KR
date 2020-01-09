---
title: 끌어오기 요청 제출
description: 이 문서에서는 기여를 병합할 수 있도록 하는 PR 프로세스 및 모범 사례를 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188210"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="d2fc4-103">끌어오기 요청 모범 사례</span><span class="sxs-lookup"><span data-stu-id="d2fc4-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="d2fc4-104">콘텐츠에 대한 변경 내용을 게시하려면 포크의 끌어오기 요청을 제출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="d2fc4-105">모든 끌어오기 요청은 병합하기 전에 검토해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-105">Every pull request has to be reviewed before it can be merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="d2fc4-106">올바른 분기를 대상으로 지정</span><span class="sxs-lookup"><span data-stu-id="d2fc4-106">Target the correct branch</span></span>

<span data-ttu-id="d2fc4-107">모든 변경 내용은 `staging` 분기에 적용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="d2fc4-108">변경 내용은 `live` 분기에서 대상으로 지정되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="d2fc4-109">`staging` 분기의 변경 내용은 `live`에 병합되므로 `live`의 모든 변경 내용을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="d2fc4-110">PowerShell의 릴리스되지 않은 버전에만 적용되는 문서의 변경 내용을 제출하는 경우 해당 버전의 릴리스 분기가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="d2fc4-111">특정 미래 버전에 적용되는 모든 변경 내용은 릴리스 분기에서 대상으로 지정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="d2fc4-112">릴리스 분기에는 `release-<version>`이라는 이름 패턴이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="d2fc4-113">모든 사용자에게 끌어오기 요청 큐를 사용하기 쉽게 만듬</span><span class="sxs-lookup"><span data-stu-id="d2fc4-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="d2fc4-114">PR 큐에는 두 가지 기본 상황이 존재합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="d2fc4-115">범위가 작고 변경 내용에 관련된 끌어오기 요청은 검토하는 데 더 적은 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="d2fc4-116">범위가 넓고 관련되지 않은 변경 내용이 포함된 끌어오기 요청은 검토하는 데 더 많은 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="d2fc4-117">대량 파일을 업데이트하는 분기 사용하지 않기</span><span class="sxs-lookup"><span data-stu-id="d2fc4-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="d2fc4-118">새로운 문서 또는 주요 다시 쓰기에서 기존 문서에 대한 사소한 업데이트를 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="d2fc4-119">분리된 작업 분기에서 이러한 변경 내용을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="d2fc4-120">대량 변경 내용은 변경된 파일 수가 많은 PR을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="d2fc4-121">PR을 최대 50개의 변경된 파일로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="d2fc4-122">큰 PR은 검토하기 어려우며 오류를 포함하기가 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="d2fc4-123">파일 이름 바꾸기 또는 삭제</span><span class="sxs-lookup"><span data-stu-id="d2fc4-123">Renaming or deleting files</span></span>

<span data-ttu-id="d2fc4-124">파일 이름을 바꾸거나 파일을 삭제하는 경우 이 변경 내용을 추가 콘텐츠 또는 업데이트와 혼합하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="d2fc4-125">관련 업데이트에 대한 PR 후 병합되는 별도의 PR에서 이 변경 내용을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="d2fc4-126">예를 들어 리디렉션 파일을 업데이트하고 리디렉션이 작동하는지 확인한 후 문서를 삭제하세요.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="d2fc4-127">이름이 바뀐 파일에 연결되는 모든 파일을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="d2fc4-128">여기에는 모든 목차 파일이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-128">This includes any TOC files.</span></span> <span data-ttu-id="d2fc4-129">또한 리포지토리 루트의 마스터 리디렉션 파일(`.openpublishing.redirection.json`)에서 리디렉션 항목을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="d2fc4-130">Docs PR 유효성 검사 서비스</span><span class="sxs-lookup"><span data-stu-id="d2fc4-130">Docs PR validation service</span></span>

<span data-ttu-id="d2fc4-131">Docs PR 유효성 검사 서비스는 PR에서 파일에 대해 유효성 검사 규칙을 실행하는 GitHub 앱입니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="d2fc4-132">다음 동작이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="d2fc4-133">PR을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-133">You submit a PR.</span></span>
1. <span data-ttu-id="d2fc4-134">PR의 상태를 나타내는 GitHub 주석에는 리포지토리에 대해 설정된 “확인”의 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="d2fc4-135">이 예에는 “Commit Validation”과 “OpenPublishing.Build”, 이렇게 두 가지 확인을 사용할 수 있도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![일부 확인 실패](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="d2fc4-137">커밋 유효성 검사에 실패하더라도 빌드가 성공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="d2fc4-138">자세한 내용을 알려면 **세부 정보**를 클릭하세요.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="d2fc4-139">세부 정보 페이지에는 문제 수정 방법에 대한 정보와 함께 실패한 모든 유효성 검사가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="d2fc4-140">유효성 검사에 성공하면 다음 설명이 PR에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![빌드 유효성 검사](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="d2fc4-142">외부(타사) 기여자인 경우 자세한 빌드 보고서 또는 미리 보기 링크에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="d2fc4-143">빌드 경고</span><span class="sxs-lookup"><span data-stu-id="d2fc4-143">Build warnings</span></span>

<span data-ttu-id="d2fc4-144">일반적으로 모든 빌드 오류, 경고 및 제안 사항을 수정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="d2fc4-145">그러나 무시할 수 있는 몇 가지 경고가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="d2fc4-146">다음 경고를 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="d2fc4-147">`<version>/<modulepath>/About/About.md`의 서비스 이름을 찾을 수 없음</span><span class="sxs-lookup"><span data-stu-id="d2fc4-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="d2fc4-148">이름이 `locale`인 메타데이터는 Yaml 헤더에서 설정하거나 docfx.json의 파일 수준 메타데이터 또는 docfx.json의 전역 메타데이터로 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="d2fc4-149">이 위치는 Docs 플랫폼에서 생성되므로 이 3개 위치에 설정된 값은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="d2fc4-150">경고를 해결하려면 3개 위치를 모두 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="d2fc4-150">Please remove them from all 3 places to resolve the warning.</span></span>
