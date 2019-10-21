---
title: cmdlet 참조 작성을 위한 특수 지침
description: 이 문서에서는 PowerShell 코드 샘플 서식 지정을 위한 특정 규칙을 제공합니다. 이 내용은 cmdlet 참조뿐 아니라 예제가 포함된 개념 문서에 적용됩니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290291"
---
# <a name="updating-reference-articles"></a>참조 문서 업데이트

Cmdlet 참조 문서에는 특정 구조가 있습니다. 이 구조는 [PlatyPS][]에 의해 정의됩니다.
PlatyPS는 PowerShell 모듈에 대한 cmdlet 도움말을 생성하는 데 사용하는 도구입니다. PlatyPS는 cmdlet의 기본 Markdown 파일을 만듭니다. Markdown 파일을 편집한 후 PlatyPS는 `Get-Help` cmdlet에서 사용되는 MAML 도움말 파일을 만드는 데 사용됩니다.

PlatyPS에는 코드로 작성되는 cmdlet 참조용 하드 코드된 스키마가 있습니다. [platyPS.schema.md][] 문서는 이 구조를 설명하려고 합니다. 스키마 위반으로 인해 기여를 수락하기 전에 수정해야 하는 빌드 오류가 발생합니다.

## <a name="general-guidelines"></a>일반 지침

- 헤더 구조를 제거하지 마세요. PlatyPS에는 특정 헤더 세트가 필요합니다.
- **입력 형식** 및 **출력 형식** 헤더에는 형식이 있어야 합니다. Cmdlet이 입력을 사용하지 않거나 값을 반환하지 않으면 “None” 값을 사용합니다.
- 펜스 코드 블록은 [예제](#format-for-examples) 섹션에서만 허용됩니다.
- 인라인 코드 범위는 모든 단락에서 사용할 수 있습니다.

## <a name="formatting-about_-files"></a>About_ 파일 서식 지정

이제 `About_*` 파일은 PlatyPS 대신 [Pandoc][]에서 처리됩니다. `About_*` 파일은 모든 버전의 PowerShell 및 게시 도구와 최상의 호환성을 제공하도록 서식이 지정됩니다.
리포지토리 유지 관리자를 사용하여 체크 인하지 않고 `about_*` 파일의 서식을 변경하지 마세요.

기본 서식 지정 지침:

- 줄을 80자로 제한
- Pandoc은 변환하는 동안 공백 4개만큼 들여 쓰므로 코드 블록, 블록 따옴표 및 테이블은 76자로 제한됨
- 테이블은 76자 이내로 맞춰야 함
  - 여러 줄에서 셀 콘텐츠를 수동으로 래핑
  - 각 줄에서 여는 및 닫는 `|` 문자 사용
  - [about_Comparison_Operators][about-example]에서 작업 예제 확인
- Pandoc의 특수 문자 `\`, `$`, `` ` `` 및 `<`을 사용하는 경우
  - 헤더 내 - 이 문자는 선행 `\` 문자를 사용하여 이스케이프되어야 함
  - 단락 내 - 이 문자는 코드 범위에 넣어야 함 예:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>예제 형식

PlatyPS 스키마에서 **EXAMPLES** 헤더는 H2 헤더이며 각 예제는 H3 헤더입니다.

예제 내에서 스키마를 사용하여 코드 블록을 단락으로 구분할 수 없습니다. 유효한 스키마는 다음과 같습니다.

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

각 예제에 번호를 매기고 간단한 제목을 추가합니다.

예:

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org