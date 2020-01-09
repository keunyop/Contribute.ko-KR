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
# <a name="best-practices-for-pull-requests"></a>끌어오기 요청 모범 사례

콘텐츠에 대한 변경 내용을 게시하려면 포크의 끌어오기 요청을 제출해야 합니다. 모든 끌어오기 요청은 병합하기 전에 검토해야 합니다.

## <a name="target-the-correct-branch"></a>올바른 분기를 대상으로 지정

모든 변경 내용은 `staging` 분기에 적용되어야 합니다. 변경 내용은 `live` 분기에서 대상으로 지정되지 않아야 합니다. `staging` 분기의 변경 내용은 `live`에 병합되므로 `live`의 모든 변경 내용을 덮어씁니다.

PowerShell의 릴리스되지 않은 버전에만 적용되는 문서의 변경 내용을 제출하는 경우 해당 버전의 릴리스 분기가 있는지 확인합니다. 특정 미래 버전에 적용되는 모든 변경 내용은 릴리스 분기에서 대상으로 지정되어야 합니다. 릴리스 분기에는 `release-<version>`이라는 이름 패턴이 사용됩니다.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>모든 사용자에게 끌어오기 요청 큐를 사용하기 쉽게 만듬

PR 큐에는 두 가지 기본 상황이 존재합니다.

- 범위가 작고 변경 내용에 관련된 끌어오기 요청은 검토하는 데 더 적은 시간이 걸립니다.
- 범위가 넓고 관련되지 않은 변경 내용이 포함된 끌어오기 요청은 검토하는 데 더 많은 시간이 걸립니다.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>대량 파일을 업데이트하는 분기 사용하지 않기

새로운 문서 또는 주요 다시 쓰기에서 기존 문서에 대한 사소한 업데이트를 분리합니다. 분리된 작업 분기에서 이러한 변경 내용을 사용합니다.

대량 변경 내용은 변경된 파일 수가 많은 PR을 만듭니다. PR을 최대 50개의 변경된 파일로 제한합니다. 큰 PR은 검토하기 어려우며 오류를 포함하기가 더 쉽습니다.

### <a name="renaming-or-deleting-files"></a>파일 이름 바꾸기 또는 삭제

파일 이름을 바꾸거나 파일을 삭제하는 경우 이 변경 내용을 추가 콘텐츠 또는 업데이트와 혼합하지 마세요.
관련 업데이트에 대한 PR 후 병합되는 별도의 PR에서 이 변경 내용을 처리합니다. 예를 들어 리디렉션 파일을 업데이트하고 리디렉션이 작동하는지 확인한 후 문서를 삭제하세요.

이름이 바뀐 파일에 연결되는 모든 파일을 업데이트해야 합니다. 여기에는 모든 목차 파일이 포함됩니다. 또한 리포지토리 루트의 마스터 리디렉션 파일(`.openpublishing.redirection.json`)에서 리디렉션 항목을 추가해야 합니다.

## <a name="docs-pr-validation-service"></a>Docs PR 유효성 검사 서비스

Docs PR 유효성 검사 서비스는 PR에서 파일에 대해 유효성 검사 규칙을 실행하는 GitHub 앱입니다.

다음 동작이 표시됩니다.

1. PR을 제출합니다.
1. PR의 상태를 나타내는 GitHub 주석에는 리포지토리에 대해 설정된 “확인”의 상태가 표시됩니다. 이 예에는 “Commit Validation”과 “OpenPublishing.Build”, 이렇게 두 가지 확인을 사용할 수 있도록 설정되어 있습니다.

   ![일부 확인 실패](media/powershell-pull-requests/validation-failed.png)

   커밋 유효성 검사에 실패하더라도 빌드가 성공할 수 있습니다.

1. 자세한 내용을 알려면 **세부 정보**를 클릭하세요.
1. 세부 정보 페이지에는 문제 수정 방법에 대한 정보와 함께 실패한 모든 유효성 검사가 표시됩니다.
1. 유효성 검사에 성공하면 다음 설명이 PR에 추가됩니다.

   ![빌드 유효성 검사](media/powershell-pull-requests/build-validation.png)

외부(타사) 기여자인 경우 자세한 빌드 보고서 또는 미리 보기 링크에 액세스할 수 없습니다.

### <a name="build-warnings"></a>빌드 경고

일반적으로 모든 빌드 오류, 경고 및 제안 사항을 수정해야 합니다. 그러나 무시할 수 있는 몇 가지 경고가 있습니다.

다음 경고를 무시할 수 있습니다.

- > `<version>/<modulepath>/About/About.md`의 서비스 이름을 찾을 수 없음

- > 이름이 `locale`인 메타데이터는 Yaml 헤더에서 설정하거나 docfx.json의 파일 수준 메타데이터 또는 docfx.json의 전역 메타데이터로 설정할 수 없습니다. 이 위치는 Docs 플랫폼에서 생성되므로 이 3개 위치에 설정된 값은 무시됩니다. 경고를 해결하려면 3개 위치를 모두 제거하세요.
