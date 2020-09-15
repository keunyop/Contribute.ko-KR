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
# <a name="labels-projects-and-milestones-roadmap"></a>레이블, 프로젝트 및 마일스톤 로드맵

.NET docs 팀에서는 [GitHub 레이블](https://github.com/dotnet/docs/labels)을 광범위하게 사용하여 작업을 구성합니다. 레이블 조합을 필터링하여 [.NET docs 웹 사이트](https://docs.microsoft.com/dotnet)에서 관심 있는 섹션에 빠르게 집중할 수 있습니다. 예를 들어 `P1` 문제의 모든 진행 중 우선 순위는 [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22)를 사용해 필터링할 수 있습니다.

[GitHub 프로젝트](https://github.com/dotnet/docs/projects)를 사용하여 스프린트 및 기타 목표 중심 대규모 사용자 스토리를 구성합니다. 또한 [GitHub 마일스톤](https://github.com/dotnet/docs/milestones)을 사용하여 작업을 추적합니다. 계획을 위한 프로젝트(문제) 및 작업의 마일스톤(끌어오기 요청)을 생각해 두는 것이 좋습니다.

이 로드맵에서는 이러한 조직 도구를 사용하는 방법을 설명하고 관심 영역을 찾는 데 사용하는 편리한 필터 링크를 제공합니다.

## <a name="labels"></a>레이블

[dotnet/docs](https://github.com/dotnet/docs)를 처음 사용하는 경우에는 [일반](https://github.com/dotnet/docs/labels/up-for-grabs) 문제부터 시작하세요. 이러한 문제는 더 집중적인 범위가 있는 문제입니다. 첫 번째 기여를 만드는 좋은 방법입니다. 일반 보기에서 영역 및 우선 순위를 기준으로 문제를 추가로 필터링할 수 있습니다. 작은 규모의 첫 번째 기여를 시도하려는 경우 [처음 사용하기 좋은 문제](https://github.com/dotnet/docs/labels/good-first-issue)로 초보자에게 좋은 문제를 식별했습니다.

레이블을 사용하여 다양한 방법으로 문제를 분류합니다.

- [.NET 가이드](#find-a-single-net-guide) 및 [가이드 섹션](#search-one-section-of-a-guide)
- [대상 릴리스](#releases)
- [우선 순위](#priority)

각 집합(가이드, 릴리스, 우선 순위)의 레이블을 결합하여 좁은 범위로 만들고 작업하려는 문제를 찾을 수 있습니다.

### <a name="find-a-single-net-guide"></a>단일 .NET 가이드 찾기

각 아키텍처 전자책 및 각 .NET 가이드에 대해 레이블을 사용합니다.

![:book: 연한 녹색 배경의 가이드](./media/labels-projects/guide.png "아키텍처 가이드 레이블의 접두사")

아키텍처 전자책은 `:book: guide` 접두사로 표시되며 연한 녹색 배경이 있습니다. 다음은 권장 아키텍처를 다루는 긴 형식의 영역입니다. 각 .NET 아키텍처 가이드에 대해 필터링된 현재 문제는 다음과 같습니다.

- [ASP.NET Core 웹앱](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [클라우드 네이티브](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker 수명 주기](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [w/ Windows 컨테이너 현대화](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET 마이크로 서비스](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [서버리스 앱](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

이 레이블 스타일은 [프레임워크 디자인 지침](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)에도 적용됩니다. 이 영역의 레이블 디자인은 동일하지만 커뮤니티 PR은 권장되지 않습니다. 이는 허가를 받아 재인쇄된 자료이므로 편집해서는 안 됩니다.

![진한 파란색 배경의 :books: Area](./media/labels-projects/area.png ".NET 가이드 영역 레이블의 접두사")

각 .NET 가이드는 `:books: Area` 접두사로 표시되며 진한 파란색 배경이 있습니다. 각 .NET 가이드에 대해 필터링된 현재 문제는 다음과 같습니다.

- [API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [데스크톱 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET 아키텍처 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 제거 가능
- [.NET Core 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 제거 가능
- [Visual Basic 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>가이드의 한 섹션 검색

![감색 배경의 :card_file_box: Area](./media/labels-projects/technology.png ".NET 가이드 하위 영역 레이블의 접두사")

.NET 가이드는 대용량이므로 이 레이블은 가이드 섹션별로 범위를 제한합니다. 각 .NET 가이드 하위 영역은 `:card_file_box: Technology` 접두사로 표시되며 감색 배경이 있습니다. 이러한 레이블의 대부분은 여러 가이드에 적용되고, 일부는 하나의 가이드에만 적용됩니다. 영역을 필터링한 후 이러한 레이블 중 하나를 추가하여 문제 범위를 추가로 제한합니다.

- AppCompat
- 비동기 작업
- C# 고급 개념
- C# 컴파일러
- C# 기초
- C# 시작하기
- C# 언어 참조
- C# Null 보안
- C# 새로운 기능
- CLI
- 데이터 액세스
- Docker
- 설치 관리자
- LINQ
- NCL
- .NET Standard
- Roslyn API
- 보안
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>릴리스

![진한 노란색의 :checkered_flag: Release:](./media/labels-projects/release.png "릴리스 레이블의 접두사")

특정 릴리스에 대해 태그가 지정된 문제는 `:checkered_flag: Release:` 접두사로 표시되고 진한 노란색 배경이 있습니다.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>우선 순위

우선 순위 레이블은 모두 `P` 뒤에 단일 숫자가 옵니다. 숫자가 낮을수록 우선 순위가 높습니다.

- P0 - 긴급 우선 순위인 문제 또는 PR(끌어오기 요청)
- P1 - 높은 우선 순위
- P2 - 중간 우선 순위
- P3 - 낮은 우선 순위

### <a name="what-about-the-other-labels"></a>다른 레이블의 경우

콘텐츠 팀에서 다양한 문제 분류를 관리하기 위해 사용하는 다른 레이블이 많이 있습니다. 콘텐츠 팀에 있지 않은 경우에는 이러한 다른 레이블을 무시할 수 있습니다.

## <a name="projects"></a>프로젝트

프로젝트는 계획 목적으로 제공되며, Kanban 보드를 통해 우선 순위가 지정된 작업을 자동화할 수 있습니다. 프로젝트는 끌어오기 요청이 아닌 GitHub 문제를 포함해야 합니다. 마일스톤은 끌어오기 요청만 포함하므로 프로젝트는 마일스톤과 다릅니다.

프로젝트는 다음과 같은 두 가지 방법으로 사용합니다.

- `Month YYYY` 프로젝트 형식: 매월의 작업 계획에 대한 Kanban 보드입니다.
  - 예: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) 등
- 장기 실행 대규모 사용자 스토리: 작업이 몇 개월에 걸쳐 진행되는 경우 목표를 향해 작업을 구성하는 데 사용됩니다.
  - 예: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) 등

## <a name="milestones"></a>마일스톤

마일스톤은 일반적으로 `Month YYYY` 프로젝트와 동일한 명명 규칙을 따르지만 프로젝트와는 다릅니다. 마일스톤은 완료된 작업을 추적할 때 사용합니다. 마일스톤은 문제(잠재적 작업)를 포함하는 것이 아니라 단독으로 끌어오기 요청을 포함해야 합니다. 현재 마일스톤은 새 끌어오기 요청에 자동으로 적용됩니다.
