---
title: Microsoft Docs 참여자 가이드 개요
description: 이 가이드에서는 Microsoft 설명서 사이트인 docs.microsoft.com에 참여할 수 있는 방법에 대해 설명합니다.
author: billwagner
ms.author: wiwagn
ms.date: 06/23/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 084da0320514b3a4551ce130d8d17e3040a35f29
ms.sourcegitcommit: 6a7c9b5e9538ed588bd2da772ae319c09e545a74
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85279350"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 참여자 가이드 개요

[docs.microsoft.com](https://docs.microsoft.com)(Docs) 참여자 가이드에 관심을 가져주셔서 감사합니다.

몇몇 Microsoft 설명서 집합은 오픈 소스로, GitHub에서 호스트 됩니다. 일부 문서 세트는 완전히 오픈 소스는 아니지만, 많은 문서 세트에는 끌어오기 요청을 통해 제안된 변경을 수행할 수 있는 공용 리포지토리가 있습니다. 이러한 오픈 소스 방식은 제품 엔지니어와 콘텐츠 팀, 고객 간 커뮤니케이션을 간소화하고 개선하며 다음과 같은 이점을 제공합니다.

- 오픈 소스 리포지토리의_공개 계획_을 통해 가장 필요한 문서에 대한 피드백을 받습니다.
- 오픈 소스 리포지토리의_공개 검토_를 통해 첫 번째 릴리스에서 가장 유용한 콘텐츠를 게시할 수 있습니다.
- 오픈 소스 리포지토리의_공개 업데이트_를 통해 콘텐츠를 지속적으로 개선할 수 있습니다.

[docs.microsoft.com](https://docs.microsoft.com)의 사용자 환경은 [GitHub](https://github.com) 워크플로와 직접 통합되어 훨씬 더 간단합니다. [보고 있는 문서를 편집](#quick-edits-to-existing-documents)하여 시작하세요. 또는 [새 항목을 검토](#review-open-prs)하여 도움을 주거나 [품질 이슈를 작성](#create-quality-issues)하세요.

> [!IMPORTANT]
> docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 준수합니다. 자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요. 또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.<br>
>
> 공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다. 변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다. 온라인 양식을 먼저 작성한 후 Microsoft에서 끌어오기 요청을 검토하거나 수락할 수 있습니다.

## <a name="quick-edits-to-existing-documents"></a>기존 문서의 빠른 편집

빠른 편집은 문서의 사소한 오류 및 누락을 보고하고 수정하는 프로세스를 간소화합니다. 오류를 최소화하려는 모든 노력에도 불구하고 게시되는 문서에서 사소한 문법 및 맞춤법 _오류가 발견될 수 있습니다_. 이슈를 작성해 오류를 보고할 수도 있지만, PR(끌어오기 요청)을 만들면 문제를 더 빠르고 쉽게 해결할 수 있습니다(옵션을 사용할 수 있는 경우).

1. 일부 문서 페이지의 경우 브라우저에서 직접 콘텐츠를 편집할 수 있습니다. 해당하는 경우 아래 표시된 것처럼 **편집** 단추가 표시됩니다. **편집**(또는 지역화된) 단추를 클릭하면 GitHub의 원본 파일로 이동합니다. **편집** 단추가 없는 경우 설명서 페이지를 변경할 수 없다는 의미입니다.

   ![편집 링크의 위치](./media/index/edit-article.png)

2. 다음으로 연필 아이콘을 클릭하여 표시된 것처럼 문서를 편집합니다. 연필 아이콘이 회색으로 표시되는 경우 GitHub 계정으로 로그인하거나 새 계정을 만들어야 합니다. 

   ![연필 아이콘의 위치](./media/index/edit-icon.png)


3. 웹 편집기에서 편집합니다. **변경 내용 미리 보기** 탭을 클릭하여 변경 내용의 서식을 확인합니다.

4. 변경했으면 페이지 하단으로 스크롤 합니다. 변경 내용의 제목 및 설명을 입력하고 다음 그림에 표시된 것처럼 **파일 변경 제안**을 클릭합니다.

   ![파일 변경 제안](./media/index/submit-pull-request.png)

5. 변경을 제안했으므로 리포지토리 소유자에게 변경 사항을 리포지토리로 “끌어오도록” 요청해야 합니다. 이 작업은 “끌어오기 요청”을 사용하여 수행합니다. 위 그림에서 **파일 변경 제안**을 클릭한 경우 다음 그림과 같은 새 페이지로 이동됩니다.

   ![끌어오기 요청 만들기](media/index/create-pull-request.png)

   **끌어오기 요청 만들기**를 클릭하고, 끌어오기 요청 제목(및 필요한 경우 설명)을 입력한 다음, **끌어오기 요청 만들기**를 다시 클릭합니다. (GitHub을 처음 사용하는 경우 자세한 내용은 [끌어오기 요청 정보](https://help.github.com/en/articles/about-pull-requests)를 참조하세요.)

6. 이것으로 끝입니다. 콘텐츠 팀 구성원이 PR을 검토하고 병합합니다. 변경을 많이 수행한 경우 변경을 요청하는 피드백을 받을 수 있습니다.

GitHub 편집 UI는 리포지토리에 대한 사용 권한에 따라 달라집니다. 대상 리포지토리에 대한 쓰기 권한이 없는 contributor의 경우 이전 이미지가 정확합니다. GitHub는 해당 계정의 대상 리포지토리의 포크를 자동으로 만듭니다. 대상 리포지토리에 대한 쓰기 권한이 있는 경우 GitHub는 대상 리포지토리에 새 분기를 만듭니다. 분기 이름의 형식은 GitHub ID와 패치 분기에 대한 숫자 식별자를 사용하는 **\<GitHubId\>-patch-n**입니다.

쓰기 권한이 있는 기여자의 경우에도, Microsoft는 모든 변경 내용에 대해 끌어오기 요청을 사용합니다. 대부분의 리포지토리에는 보호되는 `master` 분기가 있으므로 업데이트는 끌어오기 요청으로 제출해야 합니다.

브라우저 내 편집 환경은 변경 내용이 적거나 자주 변경하지 않는 경우 적합합니다. 편집 적용 범위가 넓거나 고급 Git 기능(예: 분기 관리, 고급 병합 충돌 해결)을 사용하는 경우 [리포지토리를 포크하고 로컬에서 작업](how-to-write-workflows-major.md)해야 합니다.

> [!NOTE]
> 활성화된 경우 문서를 **임의 언어**로 편집하고, 편집 유형에 따라 다음 작업이 수행됩니다.
> 1. 승인된 언어 변경은 기계 번역 엔진을 개선하는 데에도 도움이 됩니다.
> 2. 문서 내용을 많이 수정하는 편집은 내부적으로 처리되어 동일한 문서에 대한 변경 사항을 영어로 제출하므로, 승인된 경우 모든 언어로 지역화됩니다.
> 제안한 개선 사항은 해당 언어로 된 문서뿐만 아니라 사용 가능한 모든 언어로 된 문서에 긍정적으로 영향을 줍니다.

## <a name="review-open-prs"></a>진행 중인 PR 검토

현재 진행 중인 PR을 확인하여 새 항목이 게시되기 전에 읽을 수 있습니다. 검토는 [GitHub 흐름](https://guides.github.com/introduction/flow/) 프로세스를 따릅니다. 공개 리포지토리에서 제안된 업데이트 또는 새 문서를 볼 수 있습니다. 이를 검토하고 댓글을 추가하세요. 원하는 문서 리포지토리를 살펴보고, 관심 있는 영역의 진행 중인 PR(끌어오기 요청)을 확인합니다. 제안된 업데이트에 대한 커뮤니티 피드백은 전체 커뮤니티에 도움이 됩니다.

## <a name="create-quality-issues"></a>품질 이슈 작성하기

Microsoft의 문서는 계속 진행 중인 작업입니다. 유용한 이슈들 덕분에 커뮤니티에 가장 중요한 콘텐츠에 집중할 수 있습니다. 더 자세한 정보를 제공할수록 문제에 더 도움이 됩니다. 찾은 정보를 알려주세요. 사용한 검색 용어를 알려주세요. 시작하기가 어렵다면 새로운 기술을 어떻게 활용하면 좋을지 공유해 주세요.

많은 Microsoft의 설명서 페이지에는 페이지 아래쪽에 클릭하여 해당 문서와 관련된 문제를 추적하기 위해 **제품 피드백** 또는 **콘텐츠 피드백**을 남길 수 있는 **피드백** 섹션이 있습니다.

문제를 통해 필요한 사항에 대한 대화가 시작됩니다. 콘텐츠 팀은 추가할 수 있는 아이디어를 가지고 이러한 문제에 응답하며 사용자의 의견을 구합니다. 사용자가 초안을 만들면 Microsoft에서 [PR 검토](#review-open-prs)를 요청할 것입니다.

## <a name="get-more-involved"></a>더 많이 참여하기

기타 항목은 Microsoft Docs에 생산적으로 기여를 시작하는 데 도움이 됩니다. GitHub 리포지토리, Markdown 도구, Microsoft Docs 플랫폼에서 사용되는 확장으로 작업하는 방법을 설명합니다.
