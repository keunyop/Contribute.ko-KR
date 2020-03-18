---
title: 설명서용 Git 및 GitHub 기본 사항
description: 이 문서에서는 Git, GitHub 리포지토리 및 콘텐츠 구성 방법에 대한 개요와 docs.microsoft.com에 사용되는 명명 규칙에 대해 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/30/2017
ms.openlocfilehash: c099a458718ade11840c314542c530dd6669402d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331886"
---
# <a name="git-and-github-essentials-for-docs"></a>Docs용 Git 및 GitHub 기본 사항

## <a name="overview"></a>개요

Docs 콘텐츠 참여자는 여러 도구와 프로세스를 사용합니다. 동일한 프로젝트에서 다른 참여자와 동시에 작업하게 되며, 정확히 동일한 콘텐츠를 동시에 작업하게 될 수도 있습니다. 이러한 작업은 Git 및 GitHub 소프트웨어를 통해 가능합니다.

Git은 오픈 소스 버전 제어 시스템입니다. Git을 사용하면 *리포지토리*에 위치하는 파일의 *배포된 버전 제어*를 통해 이러한 유형의 프로젝트 협업을 손쉽게 수행할 수 있습니다. 본질적으로 Git를 통해 지정된 리포지토리에서 시간에 따라 여러 참여자가 수행한 작업의 스트림을 통합할 수 있습니다.

GitHub는 [docs.microsoft.com](https://docs.microsoft.com) 콘텐츠를 저장하는 데 사용되는 Git 리포지토리와 같은 Git 리포지토리용 웹 기반 호스팅 서비스입니다. 모든 프로젝트에서 GitHub는 기본 리포지토리를 호스트합니다. 여기에서 참여자는 각자 작업의 복사본을 만들 수 있습니다.

## <a name="git"></a>Git

중앙 집중식 버전 제어 시스템(예: Team Foundation Server, SharePoint 또는 Visual SourceSafe)에 익숙한 경우 Git에는 해당 배포 모델을 지원하는 고유한 참여 워크플로 및 용어가 있다는 점을 알 수 있습니다. 예를 들어 일반적으로 체크 아웃/체크 인 작업과 연결된 파일 잠금이 없습니다. 실제로 Git은 더욱 자세한 수준에서 변경 내용을 확인하고 파일을 바이트 단위로 비교합니다.

또한 Git은 계층화된 구조를 사용하여 프로젝트에 대한 콘텐츠를 저장하고 관리합니다.

- 리포지토리:  리포지토리는 가장 높은 스토리지 단위입니다.  리포지토리는 하나 이상의 분기를 포함합니다.
- 분기:  프로젝트의 콘텐츠 세트를 구성하는 파일과 폴더가 포함된 스토리지 단위입니다. 분기는 작업 스트림(일반적으로 버전이라고 함)을 구분합니다. 기여는 항상 특정 분기에 대해 이루어지고 범위 지정됩니다. 모든 리포지토리에는 하나의 기본 분기(일반적으로 “마스터”라고 함)와 마스터 분기에 다시 병합되도록 지정된 하나 이상의 분기가 포함되어 있습니다. 마스터 분기는 프로젝트의 현재 버전이자 “진실한 단일 원본”으로 사용됩니다. 리포지토리의 나머지 분기들은 부모인 마스터 분기에서 생성됩니다.

참여자는 Git와 상호 작용하여 로컬 및 GitHub 수준에서 리포지토리를 업데이트하고 조작합니다.

- 로컬로 Git Bash 콘솔과 같은 도구를 통해 로컬 리포지토리를 관리하고 GitHub 리포지토리와 통신하는 Git 명령을 지원합니다.
- Git과 통합된 [www.github.com](https://www.github.com)을 통해 기본 리포지토리로 다시 이동하는 참가 조정을 관리합니다.

## <a name="github"></a>GitHub

> [!NOTE]
> Docs 지침이 GitHub 사용을 기반으로 하지만 일부 팀에서는 Visual Studio Team Services를 사용하여 Git 리포지토리를 호스트합니다. Visual Studio 팀 탐색기 클라이언트는 명령줄을 통한 Git 명령 사용의 대안으로 Team Services 리포지토리를 조작하기 위한 GUI를 제공합니다.
> </br>
> 또한 아래 지침 중 다수는 GitHub에서 Azure 서비스 콘텐츠를 호스트하는 몇 년 동안의 경험을 통해 모범 사례로 발전되었습니다. 일부 Docs 리포지토리에서 이러한 지침이 필요할 수 있습니다.

모든 워크플로는 모든 Docs 프로젝트의 기본 리포지토리가 저장되는 GitHub 수준에서 시작하고 끝납니다. 기여자가 자신의 용도에 맞게 만든 복사본이 여러 컴퓨터에 배포됩니다. 이러한 복사본은 결과적으로 프로젝트의 기본 GitHub 리포지토리로 조정됩니다.

### <a name="directory-organization"></a>디렉토리 조직

앞서 언급한 대로 프로젝트의 기본/마스터 분기는 프로젝트에 대한 현재 버전의 콘텐츠로 사용됩니다. 마스터 분기의 콘텐츠(및 여기에서 만든 분기)는 해당 Docs 페이지에 대한 문서의 구성에 맞추어 느슨하게 조정됩니다. 하위 디렉터리는 유사 콘텐츠(예: 서비스), 미디어 콘텐츠(예: 이미지 파일) 및 “포함” 파일(콘텐츠를 다시 사용할 수 있는 파일)을 분리하는 데 사용됩니다.

일반적으로 기본 `articles` 디렉터리는 리포지토리 루트 아래에서 찾을 수 있습니다. 문서 디렉터리에는 일련의 하위 디렉터리 집합이 포함되어 있습니다. 하위 디렉터리의 문서는 *.md* 확장명을 사용하는 Markdown 파일로 서식이 지정됩니다. 여러 서비스를 지원하는 일부 리포지토리는 [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) 리포지토리와 같은 일반 `/articles` 하위 디렉터리를 사용합니다. 다른 리포지토리는 `/IntuneDocs`를 사용하는 [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) 리포지토리와 같은 서비스 특정 이름을 사용할 수 있습니다.

이 디렉토리의 루트 내에서 전반적인 서비스 또는 제품과 관련된 일반적인 문서를 발견할 수 있습니다. 또한 일반적으로 기능/서비스 또는 일반적인 시나리오와 일치하는 다른 하위 디렉토리 시리즈를 찾을 수 있습니다. 예를 들어 Azure "가상 머신" 문서는 `/virtual-machines` 하위 디렉터리에 있으며, Intune "이해 및 탐색" 문서는 `/understand-explore` 하위 디렉터리에 있습니다.

### <a name="media-subdirectory"></a>미디어 하위 디렉토리

각 문서 디렉터리에는 해당 미디어 파일의 `/media` 하위 디렉터리가 포함되어 있습니다. 미디어 파일에는 이미지 참조가 있는 문서에서 사용하는 이미지가 포함되어 있습니다.

### <a name="includes-subdirectory"></a>포함되는 내용 하위 디렉토리

두 개 이상의 문서에서 공유되는 재사용 가능 콘텐츠는 언제나 기본 `articles` 디렉터리 아래 `/includes` 하위 디렉터리에 배치됩니다. 포함 파일을 사용하는 Markdown 파일에서는 포함 파일을 참조해야 하는 위치에 해당하는 “포함” Markdown 확장이 배치됩니다.

추가 지침은 [Markdown 참조: 포함되는 내용](markdown-reference.md#included-markdown-files)을 참조하세요.

### <a name="markdown-file-template"></a>Markdown 파일 템플릿

각 리포지토리의 루트 디렉터리에는 편의를 위해 일반적으로 `template.md`라는 Markdown 템플릿 파일이 포함되어 있습니다. 리포지토리에 제출할 새 문서를 만들어야 하는 경우 이 템플릿 파일을 "스타터 파일"로 사용할 수 있습니다. 파일에는 다음 항목이 포함되어 있습니다.

- 파일 맨 위에서 2개의 3-하이픈 선으로 구분된 **메타데이터 헤더**. 문서와 관련된 정보를 추적하는 데 사용되는 다양한 태그가 포함되어 있습니다. 문서 메타데이터를 사용하면 작성자 특성, 기여자 특성, 이동 경로, 문서 설명 등의 특정 기능을 사용할 수 있습니다. 또한 Microsoft가 콘텐츠의 성능을 평가하는 데 사용하는 SEO 최적화 및 보고 프로세스가 포함되어 있습니다. 따라서 메타데이터는 중요합니다.
- 다양한 메타데이터 태그 및 값에 대해 설명하는 **메타데이터 섹션**. 메타데이터 섹션에 사용할 값을 잘 모를 경우에는 해당 섹션을 비워두거나 선행 해시태그(#)를 사용하여 주석으로 처리할 수 있습니다. 그런 다음 리포지토리의 끌어오기 요청 검토자가 검토 및 완료합니다.
- 다양한 **Markdown 사용 예**는 문서 요소의 형식을 지정합니다.
- 다양한 알림 형식에 사용할 수 있는 **Markdown 확장 사용에 대한 일반적인 지침**
- iframe을 사용하여 **동영상을 포함**하는 예제
- 단추 및 선택기와 같은 특수한 컨트롤에 사용할 수 있는 **docs.microsoft.com 확장 사용에 대한 일반적인 지침**

## <a name="pull-requests"></a>끌어오기 요청

*끌어오기 요청*을 사용하면 참여자가 기본 분기에 적용할 일련의 변경 내용을 편리하게 제안할 수 있습니다. 변경 내용(*커밋*이라고도 함)은 참여자의 분기에 저장되므로 GitHub는 가장 먼저 이러한 변경 내용을 기본 분기에 *병합*할 경우의 영향을 모델링할 수 있습니다. 끌어오기 요청은 참여자에게 빌드/유효성 검사 프로세스의 피드백을 제공하고, 변경 내용이 기본 분기에 병합되기 전에 끌어오기 요청 검토자가 잠재적인 문제 및 질문을 해결하는 매커니즘으로도 사용됩니다.

제안하려는 변경 내용의 크기에 따라 끌어오기 요청으로 참여하는 방법은 두 가지가 있습니다. 이 내용은 나중에 이 가이드의 [GitHub 워크플로](how-to-write-workflows-major.md) 섹션에서 자세히 다룹니다.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
