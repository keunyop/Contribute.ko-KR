---
title: 중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로
description: 이 문서에서는 "중요한" 기여자 워크플로를 사용하여 docs.microsoft.com 문서에 참여하는 방법을 보여 줍니다.
ms.date: 08/30/2017
ms.openlocfilehash: 93e659df4f72c6a272d15fd7487eb3a997bdf3c8
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609408"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>중요하거나 장기 실행되는 변경 내용에 대한 GitHub 참여 워크플로

> [!IMPORTANT]
> docs.microsoft.com에 게시하는 모든 리포지토리는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)(Microsoft 오픈 소스 규정) 또는 [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)(.NET Foundation 규정)를 채택했습니다. 자세한 내용은 [준수 사항 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)를 참조하세요. 또는 [opencode@microsoft.com](mailto:opencode@microsoft.com)이나 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)에 궁금한 사항을 문의하거나 의견을 제시하세요.<br>
>
> 공용 리포지토리의 설명서 및 코드 예제에 대한 사소한 수정 또는 확인 내용은 [docs.microsoft.com 사용 약관](https://docs.microsoft.com/legal/termsofuse)에서 다룹니다. 변경 내용이 새롭거나 중요한 내용일 경우 Microsoft 직원이 아닌 경우에 한해 끌어오기 요청에서 온라인 CLA(참가 라이선스 계약)를 제출하도록 요청하는 주석이 생성됩니다. 끌어오기 요청을 병합하기 전에 온라인 양식을 입력해야 합니다.

## <a name="overview"></a>개요

이 워크플로는 주요 변경 내용을 적용해야 하거나 리포지토리에 자주 참여할 참여자에게 적합합니다. 자주 참여하는 사용자에게는 일반적으로 진행 중인(장기 실행) 변경 내용이 있습니다. 이 작업은 끌어오기 요청이 승인 및 병합되기 전에 여러 빌드/유효성 검사/스테이징 주기를 거치거나 여러 날에 걸쳐 이루어집니다.

이러한 참여의 예제는 다음을 포함합니다.

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>용어

시작하기 전에 이 워크플로에서 사용되는 Git/GitHub 용어 및 monikers의 일부를 검토하겠습니다. 이 내용을 이제 이해할 수 있습니다. 이 내용에 대해 배우게 됩니다. 정의를 확인해야 하는 경우 이 섹션을 다시 참조하세요.

| 이름 | 설명 |
|-----------|-------------|
|포크|기본 GitHub 리포지토리의 복사본을 참조하는 경우 일반적으로 명사로 사용됩니다. 실제로 포크는 다른 리포지토리일 뿐입니다. 하지만 GitHub이 기본/부모 리포지토리에 다시 연결된다는 점에서 구별됩니다. "먼저 리포지토리를 포크해야 합니다."에서와 같이 동사로 사용되는 경우가 있습니다.|
|원격|"원본" 또는 "업스트림" 원격과 같이 원격 리포지토리에 대한 명명된 연결입니다. 이 연결은 다른 컴퓨터에서 호스팅되는 리포지토리를 참조하는 데 사용되므로 Git에서는 이를 원격이라고 합니다. 이 워크플로에서 원격은 항상 GitHub 리포지토리입니다.|
|원본|로컬 리포지토리와 복제 원본 리포지토리 간 연결에 할당된 이름입니다. 이 워크플로에서 원본은 포크에 대한 연결을 나타냅니다. "변경 내용을 원본으로 푸시합니다."에서와 같이 원본 리포지토리 자체의 모니커로 사용되는 경우가 있습니다.|
|업스트림|원본 원격과 같이 업스트림은 다른 리포지토리에 대한 명명된 연결입니다. 이 워크플로에서 업스트림은 로컬 리포지토리와 포크를 만든 기본 리포지토리 간에 연결을 나타냅니다. "변경 내용을 업스트림으로 끌어옵니다."에서와 같이 업스트림 리포지토리 자체에 모니커로 사용되는 경우가 있습니다.|

## <a name="workflow"></a>워크플로

>[!IMPORTANT]
> 아직 [설정](get-started-setup-github.md) 단계를 완료하지 않은 경우 해당 단계를 완료해야 합니다. 이 섹션은 GitHub 계정을 설정하고 Git Bash 및 Markdown 편집기를 설치하며 포크를 만들고 로컬 리포지토리를 설정하는 과정을 설명합니다. 리포지토리 또는 분기와 같은 Git 및 GitHub 개념에 익숙하지 않은 경우 먼저 [Git 및 GitHub 기본 사항](git-github-fundamentals.md)을 검토하세요.

이 워크플로에서 반복적인 주기에서 흐름을 변경합니다. 장치의 로컬 리포지토리에서 시작하여 GitHub 포크로 이동하여 기본 GitHub 리포지토리로 이동한 다음 다른 참여자의 변경 내용을 포함하도록 다시 로컬로 돌아옵니다.

### <a name="use-github-flow"></a>GitHub Flow 사용

[Git 및 GitHub 기본 사항](git-github-fundamentals.md#git)에서 Git 리포지토리에는 마스터 분기와 마스터로 통합되지 않은 상태에서 진행 중인 추가 분기가 포함된다는 점을 상기하세요. 논리적으로 연결된 변경 내용 집합을 새로 지정할 때마다 워크플로를 통해 변경 내용을 관리하는 *작업 분기*를 만드는 것이 가장 좋습니다. 여기서 작업 분기라고 하는 이유는 변경 내용을 다시 마스터 분기로 통합하기 전까지 변경 내용을 반복/구체화하는 작업 영역이기 때문입니다.

특정 분기에 연결된 변경 내용을 격리하면 해당 변경 내용을 독립적으로 제어하고 소개하고 게시 주기에 있는 특정 릴리스 시점에 대상으로 지정할 수 있습니다. 실제로, 작업 유형에 따라 리포지토리에 몇 개의 작업 분기를 쉽게 구축할 수 있습니다. 각각 다른 프로젝트를 나타내는 여러 분기에서 동시에 작업하는 것은 일반적입니다.

>[!TIP]
>마스터 분기에서 변경 내용을 지정하는 것은 적절하지 *않습니다*. 특정 시기에 기능을 릴리스하기 위해 마스터 분기를 사용하여 변경 내용을 적용하는 경우를 가정하겠습니다. 변경 내용을 지정하고 릴리스되기를 기다리고 있습니다. 그 사이에 어떤 문제를 해결해 달라는 긴급 요청을 받고 마스터 분기에 있는 파일을 변경한 다음 해당 변경 내용을 게시합니다. 이 예제에서는 특정 날짜에 릴리스하기 위해 유보하고 있던 수정 *및* 변경 내용을 의도치 않게 게시했습니다.

이제 로컬 리포지토리에서 새로운 작업 분기를 만들어 제안된 변경 내용을 캡처하겠습니다. Git 클라이언트는 각기 다르므로 원하는 클라이언트에 대한 도움말을 참조하세요. [GitHub Flow](https://guides.github.com/introduction/flow/)의 GitHub Guide에서 프로세스의 개요를 볼 수 있습니다.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>다음 단계

이것으로 끝입니다. 여러분은 docs.microsoft.com 콘텐츠에 참여하셨습니다.

- Markdwon, Markdown 확장 구문과 같은 항목에 대해 자세히 알아보려면 계속해서 "필수 항목 작성" 섹션을 진행하세요.
