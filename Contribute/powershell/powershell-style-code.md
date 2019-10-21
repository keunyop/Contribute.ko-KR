---
title: 스크립트 샘플 작성을 위한 특수 지침
description: 이 문서에서는 PowerShell 코드 샘플 서식 지정을 위한 특정 규칙을 제공합니다. 이 내용은 cmdlet 참조뿐 아니라 예제가 포함된 개념 문서에 적용됩니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290268"
---
# <a name="formatting-code-samples"></a>코드 샘플 서식 지정

기존 문서에는 시간이 지나면서 여러 스타일을 사용했고 서식 지정 규칙이 여러 번 변경되었습니다. 문서에서 PowerShell 코드 블록 및 출력의 일관된 스타일을 설정하려고 합니다.

Markdown은 다음 두 가지 코드 스타일을 지원합니다.

- 코드 범위(인라인) - 단일 억음 악센트(`` ` ``) 문자로 표시됩니다. 독립 실행형 블록이 아닌 단락에서 인라인으로 사용됩니다. 가장 일반적으로 cmdlet 이름을 중심으로 사용됩니다. [명령 구문 요소 서식 지정](powershell-style-basic-markdown.md#formatting-command-syntax-elements)을 참조하세요.
- 코드 블록 - 세 억음 악센트(`` ``` ``) 문자열로 둘러싸는 여러 줄 블록입니다.

## <a name="using-code-blocks"></a>코드 블록 사용

Markdown은 코드 블록을 나타내는 들여쓰기를 허용하지만, 이 패턴은 문제가 있을 수 있으므로 사용하지 않아야 합니다. 모든 코드 블록은 코드 펜스에 포함되어야 합니다. 코드 펜스는 세 억음 악센트(`` ``` ``) 문자열로 둘러싸는 코드 블록입니다. 코드 펜스 마커는 코드 샘플 앞 및 뒤의 고유한 줄에 있어야 합니다. 코드 블록 시작 부분의 마커에는 선택적 언어 레이블이 포함될 수 있습니다. Microsoft의 OPS(Open Publishing System)는 언어 레이블을 사용하여 구문 강조 표시 기능을 지원합니다.

또한 OPS는 코드 블록의 콘텐츠를 클립보드에 복사하는 **복사** 단추를 추가합니다. 이를 통해 코드 예제를 테스트하기 위해 코드를 스크립트에 빠르게 붙여넣을 수 있습니다. 그러나 문서의 일부 예제는 이 방식으로 실행되지 않습니다. 일부 코드 블록은 PowerShell 개념이나 구문의 추상적 표현에 대한 간단한 설명일 수 있습니다.

다음 문서에는 두 가지 형식 코드 블록이 사용됩니다.

1. 설명 예제
2. 실행 가능한 예제

## <a name="formatting-illustrative-examples"></a>설명 예제 서식 지정

설명 예제는 PowerShell 개념을 설명하는 데 사용됩니다. 이 예제는 실행을 위해 클립보드에 복사되지는 않습니다. 쉽게 입력할 수 있는 단순 예제에 가장 일반적으로 사용됩니다.
또한 명령 구문을 설명하는 구문 예제에 사용됩니다.

설명 예제는 “naked” 코드 펜스를 사용하여 코드 블록의 시작 및 끝을 표시합니다. 코드 블록에는 설명되는 명령의 예제 출력이 포함될 수 있습니다.

### <a name="syntax-block"></a>구문 블록

이 예제는 `Get-Command` cmdlet의 가능한 모든 매개 변수를 보여 줍니다.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

이 예제는 `for` 문을 일반화된 용어로 설명합니다.

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>간단한 그림 예제

다음은 PowerShell 비교 연산자를 보여 주는 예제입니다.

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

이 예제에는 간소화된 PowerShell 프롬프트가 포함되며 결과 출력이 표시됩니다. 이 경우 독자가 이 예제를 복사하고 실행할 수 없습니다.

## <a name="formatting-executable-examples"></a>실행 가능한 예제 서식 지정

더 복잡한 예제나 복사 및 실행에 유용한 예제에서는 다음 블록 스타일 태그를 사용해야 합니다.

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

PowerShell 명령으로 표시되는 출력은 구문 강조 표시를 방지하기 위해 **출력** 코드 블록으로 묶어야 합니다. 예:

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

**출력** 코드 레이블은 구문 강조 표시 시스템에서 지원하는 공식 “언어”가 아닙니다.
그러나 OPS는 웹 페이지의 코드 상자에 “출력” 레이블을 추가하므로 이 레이블이 유용합니다.
또한 이 “출력” 코드 상자에는 구문 강조 표시가 없습니다.

## <a name="coding-style-rules"></a>코딩 스타일 규칙

### <a name="avoid-line-continuation-in-code-samples"></a>코드 샘플에 줄 연속을 사용하지 않음

PowerShell 코드 예제에서 줄 연속 문자(`` ` ``)를 사용하지 마세요. 줄 연속 문자는 확인하기 어려우며 줄 끝에 추가 공백이 있는 경우 문제를 초래할 수 있습니다.

- PowerShell 스플래팅을 사용하여 많은 매개 변수가 있는 cmdlet의 줄 길이를 줄입니다.
- 파이프(`|`) 문자, 여는 중괄호, 괄호 및 대괄호 같은 PowerShell의 자연스러운 줄 바꿈 기회를 활용합니다.

### <a name="avoid-using-powershell-prompts-in-examples"></a>예제에서 PowerShell 프롬프트를 사용하지 않음

프롬프트 문자열 사용은 권장되지 않으며 명령줄 사용을 설명해야 하는 시나리오로 제한되어야 합니다. 프롬프트는 프롬프트를 변경하는 명령을 보여 주는 예제에 필요하거나 표시된 경로가 설명 중인 시나리오에 중요한 경우 필요합니다.

- PowerShell 프롬프트는 설명 예제에서만 사용해야 합니다. 대부분의 이와 같은 예제에서는 프롬프트 문자열이 “`PS>`”이어야 합니다. 이 프롬프트는 OS 특정 표시기와 관계가 없습니다.
- 실행 가능한 예제에서는 프롬프트를 사용하지 **않아야** 합니다.

다음 예제에서는 레지스트리 공급자를 사용할 때 프롬프트가 어떻게 변경되는지 보여 줍니다.

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a>예제에서 별칭을 사용하지 않음

특별히 별칭을 명시하지 않는 한 항상 모든 cmdlet 및 매개 변수의 전체 이름을 사용해야 합니다. Cmdlet 및 매개 변수 이름에는 코드에 정의된 적절한 파스칼 대/소문자 철자를 사용해야 합니다.

### <a name="using-parameters-in-examples"></a>예제에서 매개 변수 사용

위치 매개 변수를 사용하지 마세요. 일반적으로 위치 매개 변수인 경우에도 예제에는 항상 매개 변수 이름을 포함해야 합니다. 이렇게 하면 예제에서 혼동할 가능성이 줄어듭니다.
