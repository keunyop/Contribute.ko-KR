---
title: 레이블 및 프로젝트 로드맵
description: 이 문서에서는 dotnet/docs 리포지토리에서 레이블 및 프로젝트를 사용하는 방법을 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760379"
---
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="0222e-103">레이블 및 프로젝트 로드맵</span><span class="sxs-lookup"><span data-stu-id="0222e-103">Labels and projects roadmap</span></span>

<span data-ttu-id="0222e-104">.NET docs 팀에서는 [GitHub 레이블](https://github.com/dotnet/docs/labels)을 광범위하게 사용하여 작업을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="0222e-105">레이블 조합을 필터링하여 [.NET docs 웹 사이트](https://docs.microsoft.com/dotnet)에서 관심 있는 섹션에 빠르게 집중할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="0222e-106">또한 [GitHub 프로젝트](https://github.com/dotnet/docs/projects)를 사용하여 스프린트 및 기타 목표 지향 대규모 사용자 스토리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="0222e-107">이 로드맵에서는 해당 조직 도구를 사용하는 방법을 설명하고 관심 영역을 찾는 데 사용되는 편리한 필터의 링크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="0222e-108">레이블</span><span class="sxs-lookup"><span data-stu-id="0222e-108">Labels</span></span>

<span data-ttu-id="0222e-109">[dotnet/docs](https://github.com/dotnet/docs)에 처음 기여하는 경우 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 이슈로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="0222e-110">이 이슈는 더 집중된 범위가 있는 이슈이며,</span><span class="sxs-lookup"><span data-stu-id="0222e-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="0222e-111">첫 번째 기여를 하는 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="0222e-112">up-for-grabs 보기에서 영역 및 우선 순위를 기준으로 이슈를 추가로 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="0222e-113">작은 첫 번째 기여를 하려는 경우 초보자는 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 이슈를 사용하여 시작하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="0222e-114">다음과 같이 레이블을 사용하여 다양한 방법으로 이슈를 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="0222e-115">[.NET 가이드](#find-a-single-net-guide) 및 [가이드의 섹션](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="0222e-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="0222e-116">대상 릴리스</span><span class="sxs-lookup"><span data-stu-id="0222e-116">Target release</span></span>](#releases)
- [<span data-ttu-id="0222e-117">우선 순위</span><span class="sxs-lookup"><span data-stu-id="0222e-117">Priority</span></span>](#priority)

<span data-ttu-id="0222e-118">각 집합(가이드, 릴리스, 우선 순위)의 레이블을 조합하여 작업하려는 이슈를 찾기 위한 좁은 초점을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="0222e-119">단일 .NET 가이드 찾기</span><span class="sxs-lookup"><span data-stu-id="0222e-119">Find a single .NET guide</span></span>

<span data-ttu-id="0222e-120">각 아키텍처 eBook 및 각 .NET 가이드에 레이블을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="0222e-121">![연한 녹색 배경의 :book: guide](./media/labels-projects/guide.png "아키텍처 가이드 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="0222e-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="0222e-122">아키텍처 eBook은 `:book: guide` 접두사로 표시되고 배경이 연한 녹색입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="0222e-123">이는 권장되는 아키텍처를 다루는 긴 형식 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="0222e-124">각 .NET 아키텍처 가이드에 대해 필터링된 현재 이슈는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="0222e-125">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="0222e-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="0222e-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="0222e-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="0222e-127">클라우드 네이티브</span><span class="sxs-lookup"><span data-stu-id="0222e-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="0222e-128">Docker 수명 주기</span><span class="sxs-lookup"><span data-stu-id="0222e-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="0222e-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="0222e-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="0222e-130">Windows 컨테이너로 현대화</span><span class="sxs-lookup"><span data-stu-id="0222e-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="0222e-131">.NET 마이크로 서비스</span><span class="sxs-lookup"><span data-stu-id="0222e-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="0222e-132">서버리스 앱</span><span class="sxs-lookup"><span data-stu-id="0222e-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="0222e-133">이 레이블 스타일은 [Framework 디자인 지침](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)에도 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="0222e-134">이 영역의 레이블 디자인은 같지만, 커뮤니티 PR은 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="0222e-135">이 자료는 허가를 받고 재인쇄된 것이며 편집하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="0222e-136">![진한 파란색 배경의 :books: Area](./media/labels-projects/area.png ".NET 가이드 영역 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="0222e-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="0222e-137">각 .NET 가이드는 `:books: Area` 접두사로 표시되고 배경이 진한 파란색입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="0222e-138">각 .NET 가이드에 대해 필터링된 현재 이슈는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="0222e-139">API 참조</span><span class="sxs-lookup"><span data-stu-id="0222e-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="0222e-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="0222e-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="0222e-141">C# 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="0222e-142">데스크톱 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="0222e-143">F# 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="0222e-144">ML.NET 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="0222e-145">[.NET 아키텍처 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 제거될 수 있음</span><span class="sxs-lookup"><span data-stu-id="0222e-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="0222e-146">.NET Core 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="0222e-147">.NET for Apache Spark 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="0222e-148">.NET Framework 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="0222e-149">.NET 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="0222e-150">[Roslyn API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 제거될 수 있음</span><span class="sxs-lookup"><span data-stu-id="0222e-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="0222e-151">Visual Basic 가이드</span><span class="sxs-lookup"><span data-stu-id="0222e-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="0222e-152">가이드의 한 섹션 검색</span><span class="sxs-lookup"><span data-stu-id="0222e-152">Search one section of a guide</span></span>

<span data-ttu-id="0222e-153">![감색 배경의 :card_file_box: Area](./media/labels-projects/technology.png ".NET 가이드 하위 영역 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="0222e-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="0222e-154">.NET 가이드가 방대하므로 이 레이블은 범위를 가이드의 섹션으로 더 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="0222e-155">각 .NET 가이드 하위 영역은 `:card_file_box: Technology` 접두사로 표시되고 배경이 감색입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="0222e-156">많은 해당 레이블은 여러 가이드에 적용되는 반면, 나머지는 하나의 가이드에만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="0222e-157">영역을 필터링한 후 해당 레이블 중 하나를 추가하여 이슈 범위를 추가로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="0222e-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="0222e-158">AppCompat</span></span>
- <span data-ttu-id="0222e-159">비동기 작업</span><span class="sxs-lookup"><span data-stu-id="0222e-159">Async Task</span></span>
- <span data-ttu-id="0222e-160">C# 고급 개념</span><span class="sxs-lookup"><span data-stu-id="0222e-160">C# Advanced concepts</span></span>
- <span data-ttu-id="0222e-161">C# 컴파일러</span><span class="sxs-lookup"><span data-stu-id="0222e-161">C# compiler</span></span>
- <span data-ttu-id="0222e-162">C# 기본 사항</span><span class="sxs-lookup"><span data-stu-id="0222e-162">C# Fundamentals</span></span>
- <span data-ttu-id="0222e-163">C# 시작하기</span><span class="sxs-lookup"><span data-stu-id="0222e-163">C# Get Started</span></span>
- <span data-ttu-id="0222e-164">C# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="0222e-164">C# Language Reference</span></span>
- <span data-ttu-id="0222e-165">C# Null 안전</span><span class="sxs-lookup"><span data-stu-id="0222e-165">C# Null safety</span></span>
- <span data-ttu-id="0222e-166">C# 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="0222e-166">C# What's new</span></span>
- <span data-ttu-id="0222e-167">CLI</span><span class="sxs-lookup"><span data-stu-id="0222e-167">CLI</span></span>
- <span data-ttu-id="0222e-168">데이터 액세스</span><span class="sxs-lookup"><span data-stu-id="0222e-168">Data Access</span></span>
- <span data-ttu-id="0222e-169">Docker</span><span class="sxs-lookup"><span data-stu-id="0222e-169">Docker</span></span>
- <span data-ttu-id="0222e-170">설치 관리자</span><span class="sxs-lookup"><span data-stu-id="0222e-170">Installers</span></span>
- <span data-ttu-id="0222e-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="0222e-171">LINQ</span></span>
- <span data-ttu-id="0222e-172">NCL</span><span class="sxs-lookup"><span data-stu-id="0222e-172">NCL</span></span>
- <span data-ttu-id="0222e-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="0222e-173">.NET Standard</span></span>
- <span data-ttu-id="0222e-174">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="0222e-174">Roslyn APIs</span></span>
- <span data-ttu-id="0222e-175">보안</span><span class="sxs-lookup"><span data-stu-id="0222e-175">Security</span></span>
- <span data-ttu-id="0222e-176">WCF</span><span class="sxs-lookup"><span data-stu-id="0222e-176">WCF</span></span>
- <span data-ttu-id="0222e-177">WF</span><span class="sxs-lookup"><span data-stu-id="0222e-177">WF</span></span>
- <span data-ttu-id="0222e-178">WIF</span><span class="sxs-lookup"><span data-stu-id="0222e-178">WIF</span></span>
- <span data-ttu-id="0222e-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="0222e-179">WinForms</span></span>
- <span data-ttu-id="0222e-180">WPF</span><span class="sxs-lookup"><span data-stu-id="0222e-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="0222e-181">릴리스</span><span class="sxs-lookup"><span data-stu-id="0222e-181">Releases</span></span>

<span data-ttu-id="0222e-182">![진한 노란색의 :checkered_flag: Release:](./media/labels-projects/release.png "릴리스 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="0222e-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="0222e-183">특정 릴리스에 대해 태그가 지정된 이슈는 `:checkered_flag: Release:` 접두사로 표시되고 배경이 진한 노란색입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="0222e-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="0222e-184">.NET Core 2.2</span></span>
- <span data-ttu-id="0222e-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="0222e-185">.NET Core 3.0</span></span>
- <span data-ttu-id="0222e-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="0222e-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="0222e-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="0222e-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="0222e-188">우선 순위</span><span class="sxs-lookup"><span data-stu-id="0222e-188">Priority</span></span>

<span data-ttu-id="0222e-189">우선 순위 레이블은 모두 `P` 뒤에 한 자리 숫자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="0222e-190">숫자가 낮을수록 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="0222e-191">P0</span><span class="sxs-lookup"><span data-stu-id="0222e-191">P0</span></span>
- <span data-ttu-id="0222e-192">P1</span><span class="sxs-lookup"><span data-stu-id="0222e-192">P1</span></span>
- <span data-ttu-id="0222e-193">P2</span><span class="sxs-lookup"><span data-stu-id="0222e-193">P2</span></span>
- <span data-ttu-id="0222e-194">P3</span><span class="sxs-lookup"><span data-stu-id="0222e-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="0222e-195">다른 레이블의 경우 어떤가요?</span><span class="sxs-lookup"><span data-stu-id="0222e-195">What about the other labels?</span></span>

<span data-ttu-id="0222e-196">콘텐츠 팀에서 다양한 이슈 분류를 관리하는 데 사용하는 다른 많은 레이블이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="0222e-197">콘텐츠 팀에 속하지 않은 경우 이 다른 레이블을 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="0222e-198">프로젝트</span><span class="sxs-lookup"><span data-stu-id="0222e-198">Projects</span></span>

<span data-ttu-id="0222e-199">프로젝트는 다음과 같은 두 가지 방법으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-199">We use projects in two ways:</span></span>

- <span data-ttu-id="0222e-200">월 YYYY 프로젝트 형식: 매월의 작업 계획에 대한 스크럼 보드입니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="0222e-201">장기 실행 대규모 사용자 스토리: 작업이 몇 개월에 걸쳐 진행되는 경우 목표를 향해 작업을 구성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0222e-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
