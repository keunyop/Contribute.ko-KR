---
title: .NET 문서 리포지토리에 대한 참여 프로세스
description: 이 문서에서는 .NET 문서 리포지토리에 참여에 대한 간략한 소개를 제공합니다. 사용된 리포지토리, 콘텐츠를 구성하는 프로세스, 코드 샘플 및 기타 자산을 관리하기 위한 정책을 알아봅니다.
ms.date: 11/07/2018
ms.openlocfilehash: a5429864efe56e2004ccfeac4443dc74fbf15dc3
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247314"
---
# <a name="process-for-contributing-to-net-docs"></a>.NET 문서에 참여하는 프로세스

문서에 대한 커뮤니티 기여에 감사드립니다. 다음 목록에서는 .NET 문서에 참여할 때 주의해야 할 몇 가지 지침 규칙을 보여줍니다.

- 많은 끌어오기 요청으로 놀라게 **하지 마세요**. 대신, 많은 시간을 투자하기 전에 문제를 제기하고 토론을 시작하여 하나의 방향에 동의할 수 있습니다.
- **DO**는 다음 지침과 [음성 및 톤](dotnet-voice-tone.md) 지침을 따릅니다.
- **DO**는 [템플릿](dotnet-style-guide.md) 파일을 작업의 시작점으로 사용합니다.
- **DO**는 문서를 작업하기 전에 포크에 별도의 분기를 만듭니다.
- **DO**는 [GitHub Flow 워크플로](https://guides.github.com/introduction/flow/)를 따릅니다.
- **DO**에서 참여에 대해 자주 블로그 및 트윗(또는 기타)을 하세요.

이러한 지침을 따르면 모두에게 더 나은 환경을 제공할 것입니다.

## <a name="make-a-contribution-to-net-docs"></a>.NET 문서에 기여하기

**1단계:** 작은 변경 내용은 이 단계를 건너뜁니다. 새 콘텐츠를 작성하거나 기존 콘텐츠를 완전히 개정하려는 경우 수행할 작업을 설명하는 [문제](https://github.com/dotnet/docs/issues)를 엽니다.

**문서** 폴더 내의 콘텐츠는 TOC(목차)에 반영된 섹션으로 구성됩니다. 토픽에서 TOC에 있는 위치를 정의합니다. 제안에 대한 피드백을 받으세요.

-또는-

커뮤니티 기여가 시작된 기존 문제 중에서 선택할 수도 있습니다. [.NET 커뮤니티 기여자를 위한 프로젝트](https://github.com/dotnet/docs/projects/35)에는 커뮤니티 기여자가 사용할 수 있는 많은 문제가 나열되어 있습니다. 관심사와 책임 수준에 따라 다음 범주의 문제 중에서 선택할 수 있습니다.

- **유지 관리**. 이 범주에는 끊어진 링크 또는 잘못된 링크 수정, 누락된 코드 예제 추가 또는 제한된 콘텐츠 문제 해결과 같은 매우 간단한 기여가 포함됩니다. 경우에 따라 이러한 문제는 많은 수의 파일과 관련될 수 있습니다. 이 경우 시작하기 전에 어떤 작업을 수행하는지 알려주세요. 문제에 대한 주석을 추가하여 작업 진행 중임을 알려주세요.

- **콘텐츠 업데이트**. 문서 집합의 엄청난 양을 감안할 때 콘텐츠는 쉽게 구식이 되어 개정이 필요합니다. 또한 여러 가지 이유로 인해 일부 콘텐츠가 중복되거나 심지어 삼중으로 복제되었습니다. 콘텐츠를 업데이트하려면 개별 항목이 최신인지 확인하거나 기능 영역의 콘텐츠를 수정하여 중복을 제거하고 모든 고유한 콘텐츠를 더 작은 문서 집합에 보존해야 합니다.

- **새 콘텐츠 작성**. 고유의 항목을 작성하는 데 관심이 있는 경우 이러한 문제에는 문서 집합에 추가하려는 항목이 나열됩니다. 하지만 항목에 대한 작업을 시작하기 전에 알려주세요. 여기에 나열되지 않은 항목을 작성하는 데 관심이 있다면 문제를 엽니다.

또한 [문제 열기](https://github.com/dotnet/docs/issues) 목록을 보고 관심 있는 분야에 대한 작업을 자원하여 수행할 수 있습니다. [누구나 구할 수 있는](https://github.com/dotnet/docs/labels/up-for-grabs) 레이블을 사용하여 커뮤니티 기여에 대해 식별된 태그를 지정합니다. 일반적으로 최소한의 컨텍스트만 필요하며 첫 번째 문제에 매우 적합합니다. 커뮤니티의 경험 있는 기여자가 관심 있는 항목을 살펴 볼 것을 권장합니다. 항목을 찾을 때 열려 있는지 묻는 주석을 추가합니다.

수행할 작업을 선택한 후 [시작하기](get-started-setup-github.md) 가이드에 따라 GitHub 계정을 만들고 환경을 설정합니다.

**2단계:** 필요한 경우 `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` 또는 `dotnet/ml-api-docs` 리포지토리를 선택하여 변경 내용에 대한 분기를 만듭니다.

작은 변경 내용은 기여자 가이드의 [홈 페이지](index.md#quick-edits-to-existing-documents)에서 GitHub의 편집 지침을 참조하세요.

**3단계:** 이 새 분기를 변경하세요.

새 항목인 경우 이 [템플릿 파일](dotnet-style-guide.md)을 시작점으로 사용할 수 있습니다. 작성 지침이 포함되어 있으며 작성자 정보와 같이 각 문서에 필요한 메타데이터도 설명합니다.

1단계에서 문서에 대해 결정된 TOC 위치에 해당하는 폴더로 이동합니다. 이 폴더에는 해당 섹션의 모든 문서에 대한 Markdown 파일이 들어 있습니다. 필요한 경우 콘텐츠용 파일을 배치할 새 폴더를 만듭니다. 해당 섹션의 주요 문서는 *index.md*라고 합니다. 이미지 및 기타 정적 리소스의 경우 문서를 포함하는 폴더 내에 **미디어**라는 하위 폴더를 만듭니다. **미디어** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다(인덱스 파일 제외). 샘플 코드는 [샘플](#contributing-to-samples)에 대한 섹션에 설명된 대로 `dotnet/samples` 리포지토리에 있어야 합니다.

올바른 Markdown 구문을 따릅니다. 일반적인 예는 [템플릿 및 markdown 치트 시트](dotnet-style-guide.md)를 참조하세요.

## <a name="example-structure"></a>예제 구조

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**4단계:** 분기에서 마스터 분기로 PR(끌어오기 요청)을 제출합니다.

> [!IMPORTANT]
> 지금은 [주석 자동화](how-to-write-workflows-major.md#review-and-sign-off) 기능을 .NET 리포지토리에서 사용할 수 없습니다. .NET 문서 팀의 구성원이 PR을 검토하고 병합합니다.

각 PR은 일반적으로 한 번에 하나씩 문제를 해결해야 합니다. PR은 하나 또는 여러 개의 파일을 수정할 수 있습니다. 다른 파일의 여러 수정 사항을 해결하는 경우 PR을 별도로 사용하는 것이 좋습니다. markdown 업데이트뿐만 아니라 샘플을 만드는 경우 샘플에 대해 별도의 PR을 만들어야 합니다.

PR에서 기존 문제를 해결하는 경우 커밋 메시지 또는 PR 설명에 `Fixes #Issue_Number` 키워드를 추가합니다. 이렇게 하면 PR이 병합될 때 이 문제가 자동으로 닫힙니다. 자세한 내용은 [커밋 메시지를 통해 문제 닫기](https://help.github.com/articles/closing-issues-via-commit-messages/)를 참조하세요.

.NET 팀은 PR을 검토하고 승인을 위해 필요한 다른 업데이트/변경 내용이 있는지 알려줍니다.

**5단계:** 팀과 논의한 대로 분기에 필요한 업데이트를 수행합니다.

유지관리자는 피드백이 적용되고 변경 내용이 승인되면 PR을 마스터 분기 내에 병합합니다.

정기적으로 마스터 분기의 모든 커밋을 라이브 분기로 푸시하면 https://docs.microsoft.com/dotnet/ 에서 라이브로 기여한 것을 확인할 수 있습니다. 일반적으로 업무 주간 동안 매일 게시합니다. 유지 관리 활동으로 며칠 동안 게시가 지연될 수 있습니다.

## <a name="contributing-to-samples"></a>샘플에 참여

[dotnet/samples](https://github.com/dotnet/samples) 리포지토리에는 .NET 문서 아래 항목의 일부인 모든 샘플 코드가 포함되어 있습니다. 하위 폴더에 구성된 여러 가지 다른 프로젝트가 있습니다. 이러한 하위 폴더는 .NET용 문서 조직과 유사하게 구성됩니다.

리포지토리에 존재하는 코드에 대해 다음과 같이 구분합니다.

- 샘플: readers는 샘플을 다운로드하고 실행할 수 있습니다. 모든 샘플은 완전한 애플리케이션 또는 라이브러리여야 합니다. 샘플이 라이브러리를 작성하는 곳에서는 readers가 코드를 실행할 수 있는 단위 테스트 또는 애플리케이션을 포함해야 합니다. 종종 둘 이상의 기술, 기능 또는 도구 키트를 사용합니다. 각 샘플의 readme.md 파일은 문서를 참조하므로 각 샘플에서 다루는 개념에 대해 자세히 읽을 수 있습니다.
- 코드 조각: 더 작은 개념이나 작업을 보여줍니다. 컴파일되지만 완전한 애플리케이션을 위한 것은 아닙니다. 올바르게 실행되어야 하지만 일반적인 시나리오의 예제 애플리케이션은 아닙니다. 대신 단일 개념이나 기능을 설명하기 위해 가능한 한 작게 설계됩니다. 단일 코드 화면을 초과하면 안됩니다.

모든 코드는 [dotnet/samples](https://github.com/dotnet/samples) 리포지토리에 있습니다. 샘플 폴더 구조는 문서 폴더 구조와 일치하는 모델로 작업하고 있습니다. 따르는 표준은 다음과 같습니다.

- 최상위 수준 *코드 조각* 폴더에는 작고 집중된 샘플을 위한 코드 조각들이 포함되어 있습니다.
- API 참조 샘플은 *snippets/\<language>/api/\<namespace>/\<apiname>* 패턴의 따라 폴더에 배치됩니다.
- 다른 최상위 폴더는 *문서* 리포지토리의 최상위 폴더와 일치합니다. 예를 들어 문서 리포지토리에는 *machine-learning/tutorials* 폴더가 있고, 기계 학습 자습서 샘플은 *samples/machine-learning/tutorials* 폴더에 있습니다.

또한 *핵심* 및 *표준* 폴더 아래의 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼에서 빌드하고 실행해야 합니다. CI 빌드 시스템이 이를 시행할 것입니다. 최상위 수준 *프레임워크* 폴더에는 Windows에서만 빌드되고 유효성을 검사한 샘플이 포함되어 있습니다.

샘플 프로젝트는 지정된 샘플에 대해 가능한 가장 광범위한 플랫폼에서 빌드하고 실행해야 합니다. 실제로, 가능한 경우 .NET Core 기반 콘솔 애플리케이션을 빌드하는 것을 의미합니다. 웹 또는 UI 프레임워크와 관련된 샘플은 필요에 따라 해당 도구를 추가해야 합니다. 예를 들어 웹 애플리케이션, 모바일 앱, WPF 또는 WinForms 앱 등이 있습니다.

모든 코드에 대한 CI 시스템을 갖추기 위해 노력하고 있습니다. 샘플을 업데이트할 때 각 업데이트가 빌드 가능한 프로젝트의 일부인지 확인합니다. 이상적으로 샘플의 정확성에 대한 테스트도 추가합니다.

만드는 모든 샘플에는 *readme.md* 파일이 포함되어야 합니다. 이 파일에는 샘플에 대한 간략한 설명(하나 또는 두 개의 단락)이 포함되어야 합니다. *readme.md*에서는 readers에게 이 샘플을 탐구함으로써 무엇을 배울 것인지를 알려주어야 합니다. *readme.md* 파일에는 [.NET 문서 사이트](https://docs.microsoft.com/dotnet/welcome)에 있는 라이브 문서에 대한 링크도 포함되어야 합니다. 리포지토리의 지정된 파일이 해당 사이트에 매핑되는 위치를 확인하려면 리포지토리 경로의 `/docs`를 `https://docs.microsoft.com/dotnet`으로 바꿉니다.

항목에는 샘플에 대한 링크도 포함됩니다. GitHub의 샘플 폴더에 직접 연결합니다.

### <a name="writing-a-new-snippet-or-sample"></a>새 코드 조각 또는 샘플 작성

1. 샘플은 **빌드 가능한 프로젝트의 일부여야 합니다**. 가능한 경우 프로젝트는 .NET Core에서 지원하는 모든 플랫폼에 빌드되어야 합니다. 이에 대한 예외는 플랫폼별 기능 또는 플랫폼별 도구를 보여주는 샘플입니다.

2. 샘플이 일관성을 유지하려면 [corefx 코딩 스타일](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md)을 준수해야 합니다.

    - 또한 새 개체를 인스턴스화할 필요가 없는 것을 시연할 때 인스턴스 메서드보다 `static` 메서드를 사용하는 것이 좋습니다.

3. 샘플에는 **적절한 예외 처리**가 포함되어야 합니다. 샘플의 컨텍스트에서 throw될 수 있는 모든 예외를 처리해야 합니다. 예를 들어 사용자 입력을 검색하기 위해 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 메서드를 호출하는 샘플은 메서드에 대한 인수로 문자열을 전달할 때 적절한 예외 처리를 사용해야 합니다. 마찬가지로 샘플에서 메서드 호출이 실패할 것으로 예상되는 경우 결과 예외를 처리해야 합니다. [예외](https://docs.microsoft.com/dotnet/api/system.exception) 또는 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception)과 같은 기본 클래스 예외가 아닌 메서드가 throw한 특정 예외를 항상 처리합니다.

4. 샘플이 독립 실행형 패키지를 빌드하는 경우 샘플에서 사용하는 런타임 외에도 CI 빌드 시스템에서 사용하는 런타임을 포함해야 합니다.
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

이러한 프로젝트를 곧 빌드할 수 있는 CI 시스템을 배치하게 될 것입니다.

샘플을 만들려면:

1. [문제](https://github.com/dotnet/docs/issues)를 제출하거나 작업 중인 기존 보고서에 주석을 추가합니다.
2. 샘플에 설명된 개념을 설명하는 항목을 작성합니다(예: `docs/standard/linq/where-clause.md`).
3. 샘플을 작성합니다(예: `WhereClause-Sample1.cs`).
4. 샘플을 호출하는 주 진입점이 있는 Program.cs를 만듭니다. 이미 있는 경우에는 샘플에 호출을 추가합니다.

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

[.NET Core SDK](https://www.microsoft.com/net/download)와 함께 설치할 수 있는 .NET Core CLI를 사용하여 .NET Core 코드 조각 또는 샘플을 빌드합니다. 샘플을 빌드하고 실행하려면:

1. 샘플 폴더로 이동하여 오류를 확인하기 위해 빌드합니다.

    ```console
    dotnet build
    ```
2. 다음과 같이 샘플을 실행합니다.

    ```console
    dotnet run
    ```

3. 샘플의 루트 디렉터리에 readme.md를 추가합니다.

   여기에는 코드에 대한 간략한 설명이 포함되어야 하며 샘플을 참조하는 문서를 참조해야 합니다.

명시된 경우를 제외하고 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼의 명령줄에서 빌드됩니다. Visual Studio와 관련된 샘플이 몇 가지 있으며 Visual Studio 2017 이상이 필요합니다. 또한 일부 샘플은 플랫폼별 기능을 나타내며 특정 플랫폼이 필요합니다. 다른 샘플 및 코드 조각에는 .NET Framework가 필요하고, Windows 플랫폼에서 실행되며, 대상 Framework 버전용 Developer Pack이 필요합니다.

## <a name="the-c-interactive-experience"></a>C# 대화형 환경

문서에 포함된 모든 샘플은 [언어 태그](how-to-write-use-markdown.md#code-snippets)를 사용하여 원본 언어를 나타냅니다. C#의 짧은 코드 샘플은 `csharp-interactive` 언어 태그를 사용하여 브라우저에서 실행되는 C# 샘플을 지정할 수 있습니다. (인라인 코드 샘플은 `csharp-interactive` 태그를 사용하고, 소스에서 포함된 코드 조각의 경우 `code-csharp-interactive` 태그를 사용합니다.) 이러한 코드 샘플은 문서에 코드 창과 출력창을 표시합니다. 출력 창은 사용자가 샘플을 실행한 후 대화형 코드를 실행할 때의 모든 출력을 표시합니다.

C# 대화형 환경은 샘플 작업 방법을 변경합니다. 방문자는 샘플을 실행하여 결과를 볼 수 있습니다. 샘플 또는 해당 텍스트에 출력에 대한 정보가 포함되어야 하는지 여부를 결정하는 데 많은 요인이 도움이 됩니다.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>샘플을 실행하지 않고 예상 출력을 표시하는 시기

- 초보자를 위한 문서는 readers가 작업의 출력을 예상된 답변과 비교할 수 있도록 출력을 제공해야 합니다.
- 출력이 항목에 통합되어 있는 샘플에는 해당 출력이 표시되어야 합니다. 예를 들어 서식이 지정된 텍스트의 문서는 샘플을 실행하지 않고 텍스트 서식을 표시해야 합니다.
- 샘플 및 예상 출력이 모두 짧을 경우 출력을 표시하는 것이 좋습니다. 이는 약간의 시간을 절약합니다.
- 현재 문화권 또는 고정 문화권이 출력에 어떤 영향을 미치는지 설명하는 문서는 예상되는 결과를 설명해야 합니다. 대화형 REPL(Read Evaluate Print Loop)은 Linux 기반 호스트에서 실행됩니다. 기본 문화권 및 고정 문화권은 다른 운영 체제와 머신에서 서로 다른 출력을 생성합니다. 이 문서에서는 Windows, Linux 및 Mac 시스템의 출력을 설명해야 합니다.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>예상 출력을 샘플에서 제외할 시기

- 샘플이 더 큰 출력을 생성하는 문서에서는 주석에 이를 포함해서는 안됩니다. 샘플이 실행되면 코드가 숨겨집니다.
- 샘플에서 항목을 설명하는 문서이지만 출력이 해당 항목을 이해하는 데 필수적인 것은 아닙니다. 예를 들어 쿼리 구문을 설명한 다음, 출력 컬렉션의 모든 항목을 표시하는 LINQ 쿼리를 실행하는 코드입니다.

> [!NOTE]
> 일부 항목은 현재 여기에 지정된 지침을 따르지 않을 수 있습니다. 사이트 전반에 걸쳐 일관성을 유지하기 위해 노력하고 있습니다. 특정 목적에 대해 현재 추적 중인 [미해결 문제](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) 목록을 확인합니다.

## <a name="contributor-license-agreement"></a>기여자 라이선스 계약

PR이 병합되기 전에 [.NET Foundation CLA(Contribution License Agreement)](https://cla.dotnetfoundation.org)에 서명해야 합니다. 이는 .NET Foundation의 프로젝트에 대한 일회성 요구 사항입니다. Wikipedia에서 [CLA(Contribution License Agreements)](http://en.wikipedia.org/wiki/Contributor_License_Agreement)에 대한 자세한 내용을 볼 수 있습니다.

계약: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

미리 계약서에 서명할 필요는 없습니다. 평소대로 PR을 복제, 포크 및 제출할 수 있습니다. PR이 생성되면 CLA 봇에 의해 분류됩니다. 변경 내용이 작은 경우(예:오타를 수정한 경우) PR에 `cla-not-required`로 레이블이 지정됩니다. 그렇지 않으면 `cla-required`로 분류됩니다. CLA에 서명하면 현재 및 향후의 모든 끌어오기 요청은 `cla-signed`로 레이블이 지정됩니다.
