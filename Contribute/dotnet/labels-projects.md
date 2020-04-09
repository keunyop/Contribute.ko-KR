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
# <a name="labels-and-projects-roadmap"></a>레이블 및 프로젝트 로드맵

.NET docs 팀에서는 [GitHub 레이블](https://github.com/dotnet/docs/labels)을 광범위하게 사용하여 작업을 구성합니다. 레이블 조합을 필터링하여 [.NET docs 웹 사이트](https://docs.microsoft.com/dotnet)에서 관심 있는 섹션에 빠르게 집중할 수 있습니다.

또한 [GitHub 프로젝트](https://github.com/dotnet/docs/projects)를 사용하여 스프린트 및 기타 목표 지향 대규모 사용자 스토리를 구성합니다.

이 로드맵에서는 해당 조직 도구를 사용하는 방법을 설명하고 관심 영역을 찾는 데 사용되는 편리한 필터의 링크를 제공합니다.

## <a name="labels"></a>레이블

[dotnet/docs](https://github.com/dotnet/docs)에 처음 기여하는 경우 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 이슈로 시작합니다. 이 이슈는 더 집중된 범위가 있는 이슈이며, 첫 번째 기여를 하는 좋은 방법입니다. up-for-grabs 보기에서 영역 및 우선 순위를 기준으로 이슈를 추가로 필터링할 수 있습니다. 작은 첫 번째 기여를 하려는 경우 초보자는 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 이슈를 사용하여 시작하는 것이 좋습니다.

다음과 같이 레이블을 사용하여 다양한 방법으로 이슈를 분류합니다.

- [.NET 가이드](#find-a-single-net-guide) 및 [가이드의 섹션](#search-one-section-of-a-guide)
- [대상 릴리스](#releases)
- [우선 순위](#priority)

각 집합(가이드, 릴리스, 우선 순위)의 레이블을 조합하여 작업하려는 이슈를 찾기 위한 좁은 초점을 만들 수 있습니다.

### <a name="find-a-single-net-guide"></a>단일 .NET 가이드 찾기

각 아키텍처 eBook 및 각 .NET 가이드에 레이블을 사용합니다.

![연한 녹색 배경의 :book: guide](./media/labels-projects/guide.png "아키텍처 가이드 레이블의 접두사")

아키텍처 eBook은 `:book: guide` 접두사로 표시되고 배경이 연한 녹색입니다. 이는 권장되는 아키텍처를 다루는 긴 형식 영역입니다. 각 .NET 아키텍처 가이드에 대해 필터링된 현재 이슈는 다음과 같습니다.

- [ASP.NET Core 웹앱](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [클라우드 네이티브](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker 수명 주기](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Windows 컨테이너로 현대화](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET 마이크로 서비스](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [서버리스 앱](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

이 레이블 스타일은 [Framework 디자인 지침](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)에도 적용됩니다. 이 영역의 레이블 디자인은 같지만, 커뮤니티 PR은 권장되지 않습니다. 이 자료는 허가를 받고 재인쇄된 것이며 편집하면 안 됩니다.

![진한 파란색 배경의 :books: Area](./media/labels-projects/area.png ".NET 가이드 영역 레이블의 접두사")

각 .NET 가이드는 `:books: Area` 접두사로 표시되고 배경이 진한 파란색입니다. 각 .NET 가이드에 대해 필터링된 현재 이슈는 다음과 같습니다.

- [API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [데스크톱 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET 아키텍처 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 제거될 수 있음
- [.NET Core 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API 참조](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 제거될 수 있음
- [Visual Basic 가이드](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>가이드의 한 섹션 검색

![감색 배경의 :card_file_box: Area](./media/labels-projects/technology.png ".NET 가이드 하위 영역 레이블의 접두사")

.NET 가이드가 방대하므로 이 레이블은 범위를 가이드의 섹션으로 더 제한합니다. 각 .NET 가이드 하위 영역은 `:card_file_box: Technology` 접두사로 표시되고 배경이 감색입니다. 많은 해당 레이블은 여러 가이드에 적용되는 반면, 나머지는 하나의 가이드에만 있습니다. 영역을 필터링한 후 해당 레이블 중 하나를 추가하여 이슈 범위를 추가로 제한합니다.

- AppCompat
- 비동기 작업
- C# 고급 개념
- C# 컴파일러
- C# 기본 사항
- C# 시작하기
- C# 언어 참조
- C# Null 안전
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

특정 릴리스에 대해 태그가 지정된 이슈는 `:checkered_flag: Release:` 접두사로 표시되고 배경이 진한 노란색입니다.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>우선 순위

우선 순위 레이블은 모두 `P` 뒤에 한 자리 숫자가 있습니다. 숫자가 낮을수록 우선 순위가 높습니다.

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>다른 레이블의 경우 어떤가요?

콘텐츠 팀에서 다양한 이슈 분류를 관리하는 데 사용하는 다른 많은 레이블이 있습니다. 콘텐츠 팀에 속하지 않은 경우 이 다른 레이블을 무시할 수 있습니다.

## <a name="projects"></a>프로젝트

프로젝트는 다음과 같은 두 가지 방법으로 사용합니다.

- 월 YYYY 프로젝트 형식: 매월의 작업 계획에 대한 스크럼 보드입니다.
- 장기 실행 대규모 사용자 스토리: 작업이 몇 개월에 걸쳐 진행되는 경우 목표를 향해 작업을 구성하는 데 사용됩니다.
