---
title: Microsoft Docs 기여자 가이드 개요
description: 이 가이드에서는 Microsoft 설명서 사이트인 docs.microsoft.com에 참여할 수 있는 방법에 대해 설명합니다.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 04/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1cda40c890e5b30e6e1e10f3bcee0278f8004653
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2018
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 기여자 가이드 개요

[docs.microsoft.com](https://docs.microsoft.com)(Docs) 참여자 가이드를 시작합니다!

GitHub에 호스트된 Microsoft의 여러 설명서 집합은 오픈 소스입니다. 더 많은 팀에서 항상 이 모델을 채택하고 있습니다. 완전히 오픈 소스가 아닌 문서 집합에도 초대되어 끌어오기 요청을 할 수 있는 공용 리포지토리가 있습니다. 이는 제품 엔지니어와 콘텐츠 팀, 고객 간 커뮤니케이션을 간소화하고 개선합니다. 오픈으로 작업하면 다음과 같은 여러 가지 이점이 있습니다.

- 오픈의 오픈 소스 리포지토리 계획은 가장 필요한 문서에 대한 피드백을 받습니다.
- 오픈의 오픈 소스 리포지토리 검토는 첫 번째 릴리스에서 가장 유용한 콘텐츠를 게시할 수 있습니다.
- 오픈의 오픈 소스 리포지토리 업데이트는 콘텐츠를 계속 개선하기 쉽습니다.

[docs.microsoft.com](https://docs.microsoft.com)의 사용자 환경은 [GitHub](https://github.com) 워크플로와 직접 통합되어 훨씬 더 간단합니다. [보고 있는 문서를 편집](#quick-edits-to-existing-documents)하여 시작하세요. 또는 [새 항목을 검토](#review-open-prs)하여 도움을 주거나 [품질 문제를 만드세요](#create-quality-issues).

> [!IMPORTANT]
> docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 채택했습니다. 자세한 내용은 [규정 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요. 또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.<br>
>
> 공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다. 변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다. 온라인 양식 작성을 먼저 완료해야 Microsoft에서 끌어오기 요청을 검토하거나 수락할 수 있습니다.

## <a name="quick-edits-to-existing-documents"></a>기존 문서의 빠른 편집

빠른 편집은 문서의 사소한 오류 및 누락을 보고하고 수정하는 프로세스를 간소화합니다. 모든 노력에도 불구하고, 게시되는 문서에는 사소한 문법 및 맞춤법 오류가 있습니다. 문제를 만들고 실수를 보고할 수 있지만, PR(끌어오기 요청)을 만들면 문제를 더 빠르고 쉽게 해결할 수 있습니다. 거의 모든 문서에는 다음 그림에 표시된 것처럼 편집 단추가 있습니다. **편집** 단추를 클릭하면 GitHub의 원본 파일로 이동됩니다.

![편집 링크의 위치](./media/index/edit-article.png)

그런 후 다음 그림에 표시된 연필 아이콘을 클릭하여 문서를 편집합니다.

> [!NOTE]
> 연필 아이콘이 회색으로 표시되는 경우 GitHub 계정으로 로그인하거나 새 계정을 만들어야 합니다. 웹 편집기에서 편집합니다. **변경 내용 미리 보기** 탭을 클릭하여 변경 내용의 서식을 확인할 수 있습니다.

![연필 아이콘의 위치](./media/index/editicon.png)

변경했으면 페이지 하단으로 스크롤합니다. PR의 제목 및 설명을 입력하고 다음 그림에 표시된 것처럼 **파일 변경 제안**을 클릭합니다.

![변경 제안](./media/index/submit-pull-request.png)

이것으로 끝입니다. 콘텐츠 팀 구성원이 PR을 검토하고 병합합니다. 변경을 많이 수행한 경우 변경을 요청하는 피드백을 받을 수 있습니다.

GitHub 편집 UI는 리포지토리에 대한 사용 권한에 응답합니다. 대상 리포지토리에 대한 쓰기 권한이 없는 contributor의 경우 이전 이미지가 정확합니다. GitHub는 해당 계정의 대상 리포지토리의 포크를 자동으로 만듭니다. 대상 리포지토리에 대한 쓰기 권한이 있는 경우 GitHub는 대상 리포지토리에 새 분기를 만듭니다. 분기 이름의 형식은 GitHub ID와 패치 분기에 대한 숫자 식별자를 사용하는 **\<GitHubId\>-patch-n**입니다.

쓰기 권한이 있는 contributor의 경우에도, Microsoft는 모든 변경 내용에 대해 PR을 사용합니다. 대부분의 리포지토리에는 보호되는 `master` 분기가 있으므로 업데이트는 PR로 제출되어야 합니다.

브라우저 내 편집 환경은 변경 내용이 적거나 자주 변경하지 않는 경우 적합합니다. 크게 참여하거나 고급 Git 기능(분기 관리, 고급 병합 충돌 해결)을 사용하는 경우 [리포지토리를 포크하고 로컬에서 작업](how-to-write-workflows-major.md)해야 합니다.

## <a name="review-open-prs"></a>진행 중인 PR 검토

현재 진행 중인 PR을 확인하여 새 항목이 게시되기 전에 읽을 수 있습니다. 검토는 [GitHub 흐름](https://guides.github.com/introduction/flow/) 프로세스를 따릅니다. 공개 리포지토리에서 제안된 업데이트 또는 새 문서를 볼 수 있습니다. 이를 검토하고 주석을 추가하세요. 원하는 문서 리포지토리를 살펴보고, 관심 있는 영역의 진행 중인 PR(끌어오기 요청)을 확인합니다. 제안된 업데이트에 대한 커뮤니티 피드백은 전체 커뮤니티에 도움이 됩니다.

## <a name="create-quality-issues"></a>품질 문제 만들기

Microsoft의 문서는 계속 진행 중인 작업입니다. 좋은 문제는 커뮤니티의 가장 높은 우선 순위에 집중하는 데 도움이 됩니다. 더 자세한 정보를 제공할수록 문제에 더 도움이 됩니다. 찾은 정보를 알려주세요. 사용한 검색 용어를 알려주세요. 시작할 수 없는 경우 친숙한 기술 탐색을 시작하려는 방법을 알려주세요.

문제를 통해 필요한 사항에 대한 대화가 시작됩니다. 콘텐츠 팀은 추가할 수 있는 아이디어를 가지고 이러한 문제에 응답하며 사용자의 의견을 구합니다. 사용자가 초안을 만들면 Microsoft에서 [PR 검토](#review-open-prs)를 요청할 것입니다.

## <a name="get-more-involved"></a>더 많이 참여하기

기타 항목은 Microsoft Docs에 생산적으로 기여를 시작하는 데 도움이 됩니다. GitHub 리포지토리, Markdown 도구, Microsoft Docs 플랫폼에서 사용되는 확장으로 작업하는 방법을 설명합니다.
