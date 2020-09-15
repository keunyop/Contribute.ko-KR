---
title: 레이블, 프로젝트 및 마일스톤 로드맵
description: 이 문서에서는 dotnet/docs 리포지토리에서 레이블, 프로젝트 및 마일스톤을 사용하는 방법을 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b8e9f2a33f9b4a8025aa36a890bff1017cf132c6
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559266"
---
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="8846e-103">레이블, 프로젝트 및 마일스톤 로드맵</span><span class="sxs-lookup"><span data-stu-id="8846e-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="8846e-104">.NET docs 팀에서는 [GitHub 레이블](https://github.com/dotnet/docs/labels)을 광범위하게 사용하여 작업을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="8846e-105">레이블 조합을 필터링하여 [.NET docs 웹 사이트](https://docs.microsoft.com/dotnet)에서 관심 있는 섹션에 빠르게 집중할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="8846e-106">예를 들어 `P1` 문제의 모든 진행 중 우선 순위는 [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22)를 사용해 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="8846e-107">[GitHub 프로젝트](https://github.com/dotnet/docs/projects)를 사용하여 스프린트 및 기타 목표 중심 대규모 사용자 스토리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="8846e-108">또한 [GitHub 마일스톤](https://github.com/dotnet/docs/milestones)을 사용하여 작업을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="8846e-109">계획을 위한 프로젝트(문제) 및 작업의 마일스톤(끌어오기 요청)을 생각해 두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="8846e-110">이 로드맵에서는 이러한 조직 도구를 사용하는 방법을 설명하고 관심 영역을 찾는 데 사용하는 편리한 필터 링크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="8846e-111">레이블</span><span class="sxs-lookup"><span data-stu-id="8846e-111">Labels</span></span>

<span data-ttu-id="8846e-112">[dotnet/docs](https://github.com/dotnet/docs)를 처음 사용하는 경우에는 [일반](https://github.com/dotnet/docs/labels/up-for-grabs) 문제부터 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="8846e-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="8846e-113">이러한 문제는 더 집중적인 범위가 있는 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="8846e-114">첫 번째 기여를 만드는 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="8846e-115">일반 보기에서 영역 및 우선 순위를 기준으로 문제를 추가로 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="8846e-116">작은 규모의 첫 번째 기여를 시도하려는 경우 [처음 사용하기 좋은 문제](https://github.com/dotnet/docs/labels/good-first-issue)로 초보자에게 좋은 문제를 식별했습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="8846e-117">레이블을 사용하여 다양한 방법으로 문제를 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="8846e-118">[.NET 가이드](#find-a-single-net-guide) 및 [가이드 섹션](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="8846e-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="8846e-119">대상 릴리스</span><span class="sxs-lookup"><span data-stu-id="8846e-119">Target release</span></span>](#releases)
- [<span data-ttu-id="8846e-120">우선 순위</span><span class="sxs-lookup"><span data-stu-id="8846e-120">Priority</span></span>](#priority)

<span data-ttu-id="8846e-121">각 집합(가이드, 릴리스, 우선 순위)의 레이블을 결합하여 좁은 범위로 만들고 작업하려는 문제를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="8846e-122">단일 .NET 가이드 찾기</span><span class="sxs-lookup"><span data-stu-id="8846e-122">Find a single .NET guide</span></span>

<span data-ttu-id="8846e-123">각 아키텍처 전자책 및 각 .NET 가이드에 대해 레이블을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="8846e-124">![:book: 연한 녹색 배경의 가이드](./media/labels-projects/guide.png "아키텍처 가이드 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="8846e-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="8846e-125">아키텍처 전자책은 `:book: guide` 접두사로 표시되며 연한 녹색 배경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="8846e-126">다음은 권장 아키텍처를 다루는 긴 형식의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="8846e-127">각 .NET 아키텍처 가이드에 대해 필터링된 현재 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="8846e-128">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="8846e-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="8846e-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="8846e-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="8846e-130">클라우드 네이티브</span><span class="sxs-lookup"><span data-stu-id="8846e-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="8846e-131">Docker 수명 주기</span><span class="sxs-lookup"><span data-stu-id="8846e-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="8846e-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="8846e-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="8846e-133">w/ Windows 컨테이너 현대화</span><span class="sxs-lookup"><span data-stu-id="8846e-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="8846e-134">.NET 마이크로 서비스</span><span class="sxs-lookup"><span data-stu-id="8846e-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="8846e-135">서버리스 앱</span><span class="sxs-lookup"><span data-stu-id="8846e-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="8846e-136">이 레이블 스타일은 [프레임워크 디자인 지침](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)에도 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="8846e-137">이 영역의 레이블 디자인은 동일하지만 커뮤니티 PR은 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="8846e-138">이는 허가를 받아 재인쇄된 자료이므로 편집해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="8846e-139">![진한 파란색 배경의 :books: Area](./media/labels-projects/area.png ".NET 가이드 영역 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="8846e-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="8846e-140">각 .NET 가이드는 `:books: Area` 접두사로 표시되며 진한 파란색 배경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="8846e-141">각 .NET 가이드에 대해 필터링된 현재 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="8846e-142">API 참조</span><span class="sxs-lookup"><span data-stu-id="8846e-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="8846e-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="8846e-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="8846e-144">C# 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="8846e-145">데스크톱 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="8846e-146">F# 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="8846e-147">ML.NET 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="8846e-148">[.NET 아키텍처 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 제거 가능</span><span class="sxs-lookup"><span data-stu-id="8846e-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="8846e-149">.NET Core 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="8846e-150">.NET for Apache Spark 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="8846e-151">.NET Framework 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="8846e-152">.NET 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="8846e-153">[Roslyn API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 제거 가능</span><span class="sxs-lookup"><span data-stu-id="8846e-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="8846e-154">Visual Basic 가이드</span><span class="sxs-lookup"><span data-stu-id="8846e-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="8846e-155">가이드의 한 섹션 검색</span><span class="sxs-lookup"><span data-stu-id="8846e-155">Search one section of a guide</span></span>

<span data-ttu-id="8846e-156">![감색 배경의 :card_file_box: Area](./media/labels-projects/technology.png ".NET 가이드 하위 영역 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="8846e-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="8846e-157">.NET 가이드는 대용량이므로 이 레이블은 가이드 섹션별로 범위를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="8846e-158">각 .NET 가이드 하위 영역은 `:card_file_box: Technology` 접두사로 표시되며 감색 배경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="8846e-159">이러한 레이블의 대부분은 여러 가이드에 적용되고, 일부는 하나의 가이드에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="8846e-160">영역을 필터링한 후 이러한 레이블 중 하나를 추가하여 문제 범위를 추가로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="8846e-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="8846e-161">AppCompat</span></span>
- <span data-ttu-id="8846e-162">비동기 작업</span><span class="sxs-lookup"><span data-stu-id="8846e-162">Async Task</span></span>
- <span data-ttu-id="8846e-163">C# 고급 개념</span><span class="sxs-lookup"><span data-stu-id="8846e-163">C# Advanced concepts</span></span>
- <span data-ttu-id="8846e-164">C# 컴파일러</span><span class="sxs-lookup"><span data-stu-id="8846e-164">C# compiler</span></span>
- <span data-ttu-id="8846e-165">C# 기초</span><span class="sxs-lookup"><span data-stu-id="8846e-165">C# Fundamentals</span></span>
- <span data-ttu-id="8846e-166">C# 시작하기</span><span class="sxs-lookup"><span data-stu-id="8846e-166">C# Get Started</span></span>
- <span data-ttu-id="8846e-167">C# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="8846e-167">C# Language Reference</span></span>
- <span data-ttu-id="8846e-168">C# Null 보안</span><span class="sxs-lookup"><span data-stu-id="8846e-168">C# Null safety</span></span>
- <span data-ttu-id="8846e-169">C# 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="8846e-169">C# What's new</span></span>
- <span data-ttu-id="8846e-170">CLI</span><span class="sxs-lookup"><span data-stu-id="8846e-170">CLI</span></span>
- <span data-ttu-id="8846e-171">데이터 액세스</span><span class="sxs-lookup"><span data-stu-id="8846e-171">Data Access</span></span>
- <span data-ttu-id="8846e-172">Docker</span><span class="sxs-lookup"><span data-stu-id="8846e-172">Docker</span></span>
- <span data-ttu-id="8846e-173">설치 관리자</span><span class="sxs-lookup"><span data-stu-id="8846e-173">Installers</span></span>
- <span data-ttu-id="8846e-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="8846e-174">LINQ</span></span>
- <span data-ttu-id="8846e-175">NCL</span><span class="sxs-lookup"><span data-stu-id="8846e-175">NCL</span></span>
- <span data-ttu-id="8846e-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="8846e-176">.NET Standard</span></span>
- <span data-ttu-id="8846e-177">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="8846e-177">Roslyn APIs</span></span>
- <span data-ttu-id="8846e-178">보안</span><span class="sxs-lookup"><span data-stu-id="8846e-178">Security</span></span>
- <span data-ttu-id="8846e-179">WCF</span><span class="sxs-lookup"><span data-stu-id="8846e-179">WCF</span></span>
- <span data-ttu-id="8846e-180">WF</span><span class="sxs-lookup"><span data-stu-id="8846e-180">WF</span></span>
- <span data-ttu-id="8846e-181">WIF</span><span class="sxs-lookup"><span data-stu-id="8846e-181">WIF</span></span>
- <span data-ttu-id="8846e-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="8846e-182">WinForms</span></span>
- <span data-ttu-id="8846e-183">WPF</span><span class="sxs-lookup"><span data-stu-id="8846e-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="8846e-184">릴리스</span><span class="sxs-lookup"><span data-stu-id="8846e-184">Releases</span></span>

<span data-ttu-id="8846e-185">![진한 노란색의 :checkered_flag: Release:](./media/labels-projects/release.png "릴리스 레이블의 접두사")</span><span class="sxs-lookup"><span data-stu-id="8846e-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="8846e-186">특정 릴리스에 대해 태그가 지정된 문제는 `:checkered_flag: Release:` 접두사로 표시되고 진한 노란색 배경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="8846e-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="8846e-187">.NET Core 2.2</span></span>
- <span data-ttu-id="8846e-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="8846e-188">.NET Core 3.0</span></span>
- <span data-ttu-id="8846e-189">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="8846e-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="8846e-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="8846e-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="8846e-191">우선 순위</span><span class="sxs-lookup"><span data-stu-id="8846e-191">Priority</span></span>

<span data-ttu-id="8846e-192">우선 순위 레이블은 모두 `P` 뒤에 단일 숫자가 옵니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="8846e-193">숫자가 낮을수록 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="8846e-194">P0 - 긴급 우선 순위인 문제 또는 PR(끌어오기 요청)</span><span class="sxs-lookup"><span data-stu-id="8846e-194">P0 - Indicates issues or PRs that are critical priority</span></span>
- <span data-ttu-id="8846e-195">P1 - 높은 우선 순위</span><span class="sxs-lookup"><span data-stu-id="8846e-195">P1 - High priority</span></span>
- <span data-ttu-id="8846e-196">P2 - 중간 우선 순위</span><span class="sxs-lookup"><span data-stu-id="8846e-196">P2 - Medium priority</span></span>
- <span data-ttu-id="8846e-197">P3 - 낮은 우선 순위</span><span class="sxs-lookup"><span data-stu-id="8846e-197">P3 - Low priority</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="8846e-198">다른 레이블의 경우</span><span class="sxs-lookup"><span data-stu-id="8846e-198">What about the other labels</span></span>

<span data-ttu-id="8846e-199">콘텐츠 팀에서 다양한 문제 분류를 관리하기 위해 사용하는 다른 레이블이 많이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-199">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="8846e-200">콘텐츠 팀에 있지 않은 경우에는 이러한 다른 레이블을 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-200">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="8846e-201">프로젝트</span><span class="sxs-lookup"><span data-stu-id="8846e-201">Projects</span></span>

<span data-ttu-id="8846e-202">프로젝트는 계획 목적으로 제공되며, Kanban 보드를 통해 우선 순위가 지정된 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-202">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="8846e-203">프로젝트는 끌어오기 요청이 아닌 GitHub 문제를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-203">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="8846e-204">마일스톤은 끌어오기 요청만 포함하므로 프로젝트는 마일스톤과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-204">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="8846e-205">프로젝트는 다음과 같은 두 가지 방법으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-205">We use projects in two ways:</span></span>

- <span data-ttu-id="8846e-206">`Month YYYY` 프로젝트 형식: 매월의 작업 계획에 대한 Kanban 보드입니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-206">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="8846e-207">예: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) 등</span><span class="sxs-lookup"><span data-stu-id="8846e-207">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="8846e-208">장기 실행 대규모 사용자 스토리: 작업이 몇 개월에 걸쳐 진행되는 경우 목표를 향해 작업을 구성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-208">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="8846e-209">예: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) 등</span><span class="sxs-lookup"><span data-stu-id="8846e-209">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="8846e-210">마일스톤</span><span class="sxs-lookup"><span data-stu-id="8846e-210">Milestones</span></span>

<span data-ttu-id="8846e-211">마일스톤은 일반적으로 `Month YYYY` 프로젝트와 동일한 명명 규칙을 따르지만 프로젝트와는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-211">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="8846e-212">마일스톤은 완료된 작업을 추적할 때 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-212">We use milestones to track completed work.</span></span> <span data-ttu-id="8846e-213">마일스톤은 문제(잠재적 작업)를 포함하는 것이 아니라 단독으로 끌어오기 요청을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-213">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="8846e-214">현재 마일스톤은 새 끌어오기 요청에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8846e-214">The current milestone is automatically applied to new pull requests.</span></span>
