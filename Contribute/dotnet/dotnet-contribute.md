---
title: .NET 문서 리포지토리에 참여
description: 이 문서에서는 .NET 설명서에서 구성되는 리포지토리의 문서 및 코드 샘플에 참여하는 프로세스를 설명합니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
ms.openlocfilehash: 810a1335bf3c93b79952c701c44470d3e72fb124
ms.sourcegitcommit: 940c84d6bc23a8fbec780244563af188d2620ed1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "88668646"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a>.NET 문서 리포지토리에 참여하는 방법 알아보기

.NET 문서에 참여해 주셔서 감사합니다.

이 문서에서는 [.NET 문서 사이트](https://docs.microsoft.com/dotnet)에서 호스팅되는 문서 및 코드 샘플에 참여하는 프로세스를 다룹니다. 기여는 오타 수정만큼 간단하거나 새로운 문서처럼 복잡할 수 있습니다.

.NET 문서 사이트는 여러 리포지토리에서 빌드됩니다.

- [.NET 개념 문서 및 코드 조각](https://github.com/dotnet/docs)
- [코드 샘플 및 코드 조각](https://github.com/dotnet/samples)
- [.NET 표준, .NET Core, .NET Framework API 참조](https://github.com/dotnet/dotnet-api-docs)
- [.NET Compiler Platform SDK 참조](https://github.com/dotnet/roslyn-api-docs)
- [ML.NET API 참조](https://github.com/dotnet/ml-api-docs)

이 리포지토리 모두에 대한 문제는 [dotnet/docs](https://github.com/dotnet/docs/issues) 리포지토리에서 추적됩니다.

## <a name="guidelines-for-contributions"></a>기여 지침

문서에 대한 커뮤니티 기여에 감사드립니다. 다음 목록에서는 .NET 설명서에 기여할 때 주의해야 할 몇 가지 지침 규칙을 보여 줍니다.

- 많은 끌어오기 요청으로 놀라게 **하지 마세요**. 대신, 많은 시간을 투자하기 전에 문제를 제기하고 토론을 시작하여 하나의 방향에 동의할 수 있습니다.
- **DO**는 다음 지침과 [음성 및 톤](dotnet-voice-tone.md) 지침을 따릅니다.
- **DO**는 [템플릿](dotnet-style-guide.md) 파일을 작업의 시작점으로 사용합니다.
- **DO**는 문서를 작업하기 전에 포크에 별도의 분기를 만듭니다.
- [GitHub 흐름](https://guides.github.com/introduction/flow/)을 **따릅니다**.
- 원하는 경우 기여에 관해 블로그 및 트윗(또는 기타)을 **합니다**.

이러한 지침을 따르면 모두에게 더 나은 환경을 제공할 것입니다.

## <a name="make-a-contribution-to-net-docs"></a>.NET 문서에 기여하기

**1단계:** 새 콘텐츠를 작성하거나 기존 콘텐츠를 완전히 개정하려는 경우 수행할 작업을 설명하는 [문제](https://github.com/dotnet/docs/issues)를 엽니다. **문서** 폴더 내의 콘텐츠는 TOC(목차)에 반영된 섹션으로 구성됩니다. 토픽에서 TOC에 있는 위치를 정의합니다. 제안에 대한 피드백을 받으세요.

-또는-

기존 문제를 선택하고 해결합니다. 다음과 같은 방법으로, [미해결 문제](https://github.com/dotnet/docs/issues) 목록을 보고 관심 있는 분야의 문제 해결에 자발적으로 참여할 수 있습니다.

- [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 레이블로 필터링하여 적절한 첫 번째 문제를 찾습니다.
- [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 레이블로 필터링하여 커뮤니티 기여에 적합한 문제를 찾습니다. 이 문제는 일반적으로 최소한의 컨텍스트가 필요합니다.
- 숙련된 기여자는 관심 있는 문제를 해결할 수 있습니다.

참여할 문제를 찾았으면 해당 문제가 미해결 상태인지 확인하기 위한 주석을 추가합니다.

참여할 작업을 선택한 후 [시작하기](../get-started-setup-github.md) 가이드에 따라 GitHub 계정을 만들고 환경을 설정합니다.

**2단계:** 필요한 경우 `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` 또는 `dotnet/ml-api-docs` 리포지토리를 선택하여 변경 내용에 대한 분기를 만듭니다.

작은 변경 내용은 기여자 가이드의 [홈 페이지](../index.md#quick-edits-to-existing-documents)에서 GitHub의 편집 지침을 참조하세요.

**3단계:** 이 새 분기를 변경하세요.

새 항목인 경우 이 [템플릿 파일](dotnet-style-guide.md)을 시작점으로 사용할 수 있습니다. 작성 지침이 포함되어 있으며 작성자 정보와 같이 각 문서에 필요한 메타데이터도 설명합니다. docs.microsoft.com 사이트에서 사용되는 Markdown 구문에 대한 자세한 내용은 [Markdown 참조](../markdown-reference.md)를 참조하세요.

1단계에서 문서에 대해 결정된 TOC 위치에 해당하는 폴더로 이동합니다. 이 폴더에는 해당 섹션의 모든 문서에 대한 Markdown 파일이 들어 있습니다. 필요한 경우 콘텐츠용 파일을 배치할 새 폴더를 만듭니다. 해당 섹션의 주요 문서는 *index.md*라고 합니다.

이미지 및 기타 정적 리소스의 경우 문서를 포함하는 폴더 내에 **미디어**라는 하위 폴더를 만듭니다. **미디어** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다(인덱스 파일 제외).

**코드 조각**의 경우 문서를 포함하는 폴더 내에 **조각**이라는 하위 폴더를 만듭니다(아직 없는 경우). **조각** 폴더 내에서 문서 이름으로 하위 폴더를 만듭니다. 대부분의 경우 주요 .NET 언어인 C#, F# 및 Visual Basic 등 세 가지 모두의 코드 조각이 있습니다. 이 경우 세 프로젝트 각각에 대해 **csharp**, **fsharp**, **vb**라는 하위 폴더를 만듭니다. [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp) 또는 [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) 폴더 아래에 각 문서에 대한 코드 조각을 만드는 경우 해당 코드 조각은 한 언어로만 작성되므로 언어 하위 폴더를 생략할 수 있습니다.

코드 조각은 문서에 설명된 개념을 예시하는 요약된 작은 예제입니다. 다운로드 및 탐색을 위한 큰 프로그램은 [dotnet/samples](https://github.com/dotnet/samples) 리포지토리에 있어야 합니다. 전체 샘플은 [샘플에 참여](#contribute-to-samples)의 섹션을 참조하세요.

## <a name="example-folder-structure"></a>폴더 구조의 예

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
```

> [!NOTE]
> 조각 아래의 언어 폴더는 하나의 언어로만 사용되는 언어 가이드 영역에 필요하지 않습니다.

위의 구조에는 이미지 1개(*portability_report.png*) 및 *porting-overview.md* 문서에 포함된 **코드 조각**을 포함하는 코드 프로젝트 3개가 포함됩니다. 허용되는 대체 구조에는 언어별로 해당 폴더의 모든 문서에 대한 모든 코드 조각을 포함하는 프로젝트 1개가 포함됩니다. 이 대체 구조는 언어 구문을 예시하는 아주 작은 조각으로 인해 언어 참조 영역에서 사용되었습니다. 다른 영역에는 권장되지 않습니다.

포함된 조각 대부분이 기록을 위해 *dotnet/docs* 리포지토리의 */samples* 폴더 아래에 저장됩니다. 문서에 중대한 변경 내용을 적용하는 경우 해당 코드 조각을 새 구조로 이동해야 합니다. 소소한 변경인 경우에는 코드 조각을 이동하지 마세요.

**4단계:** 분기에서 마스터 분기로 PR(끌어오기 요청)을 제출합니다.

> [!IMPORTANT]
> 지금은 [주석 자동화](../how-to-write-workflows-major.md#review-and-sign-off) 기능을 .NET 리포지토리에서 사용할 수 없습니다. .NET 문서 팀의 구성원이 PR을 검토하고 병합합니다.

각 PR은 일반적으로 한 번에 하나씩 문제를 해결해야 합니다. PR은 하나 또는 여러 개의 파일을 수정할 수 있습니다. 다른 파일의 여러 수정 사항을 해결하는 경우 PR을 별도로 사용하는 것이 좋습니다. markdown을 업데이트할 뿐만 아니라 샘플을 만드는 경우 샘플에 대해 별도의 PR을 만들어야 합니다.

PR에서 기존 문제를 해결하는 경우 커밋 메시지 또는 PR 설명에 `Fixes #Issue_Number` 키워드를 추가합니다. 이렇게 하면 PR이 병합될 때 이 문제가 자동으로 닫힙니다. 자세한 내용은 [커밋 메시지를 통해 문제 닫기](https://help.github.com/articles/closing-issues-via-commit-messages/)를 참조하세요.

.NET 팀은 PR을 검토하고 승인을 위해 필요한 다른 업데이트/변경 내용이 있는지 알려줍니다.

**5단계:** 팀과 논의한 대로 분기에 필요한 업데이트를 수행합니다.

유지관리자는 피드백이 적용되고 변경 내용이 승인되면 PR을 마스터 분기 내에 병합합니다.

정기적으로 마스터 분기의 모든 커밋을 라이브 분기로 푸시하면 https://docs.microsoft.com/dotnet/ 에서 라이브로 기여한 것을 확인할 수 있습니다. 일반적으로 업무 주간 동안 매일 게시합니다.

## <a name="contribute-to-samples"></a>샘플에 기여

콘텐츠를 지원하는 코드는 다음과 같이 구분합니다.

- 샘플: readers는 샘플을 다운로드하고 실행할 수 있습니다. 모든 샘플은 완전한 애플리케이션 또는 라이브러리여야 합니다. 샘플이 라이브러리를 작성하는 곳에서는 readers가 코드를 실행할 수 있는 단위 테스트 또는 애플리케이션을 포함해야 합니다. 종종 둘 이상의 기술, 기능 또는 도구 키트를 사용합니다. 각 샘플의 readme.md 파일은 문서를 참조하므로 각 샘플에서 다루는 개념에 대해 자세히 읽을 수 있습니다.
- 코드 조각: 더 작은 개념이나 작업을 보여줍니다. 컴파일되지만 완전한 애플리케이션을 위한 것은 아닙니다. 올바르게 실행되어야 하지만 일반적인 시나리오의 예제 애플리케이션은 아닙니다. 대신 단일 개념이나 기능을 설명하기 위해 가능한 한 작게 설계됩니다. 단일 코드 화면을 초과하면 안됩니다.

샘플은 [dotnet/samples](https://github.com/dotnet/samples) 리포지토리에 저장됩니다. 샘플 폴더 구조는 문서 폴더 구조와 일치하는 모델로 작업하고 있습니다. 따르는 표준은 다음과 같습니다.

- 최상위 폴더는 *docs* 리포지토리의 최상위 폴더와 일치합니다. 예를 들어 문서 리포지토리에는 *machine-learning/tutorials* 폴더가 있고, 기계 학습 자습서 샘플은 *samples/machine-learning/tutorials* 폴더에 있습니다.

또한 *핵심* 및 *표준* 폴더 아래의 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼에서 빌드하고 실행해야 합니다. CI 빌드 시스템이 이를 시행할 것입니다. 최상위 수준 *프레임워크* 폴더에는 Windows에서만 빌드되고 유효성을 검사한 샘플이 포함되어 있습니다.

샘플 프로젝트는 지정된 샘플에 대해 가능한 가장 광범위한 플랫폼에서 빌드하고 실행해야 합니다. 실제로, 가능한 경우 .NET Core 기반 콘솔 애플리케이션을 빌드하는 것을 의미합니다. 웹 또는 UI 프레임워크와 관련된 샘플은 필요에 따라 해당 도구를 추가해야 합니다. 예를 들어 웹 애플리케이션, 모바일 앱, WPF 또는 WinForms 앱 등이 있습니다.

모든 코드에 대한 CI 시스템을 갖추기 위해 노력하고 있습니다. 샘플을 업데이트할 때 각 업데이트가 빌드 가능한 프로젝트의 일부인지 확인합니다. 이상적으로 샘플의 정확성에 대한 테스트도 추가합니다.

만드는 모든 샘플에는 *readme.md* 파일이 포함되어야 합니다. 이 파일에는 샘플에 대한 간략한 설명(하나 또는 두 개의 단락)이 포함되어야 합니다. *readme.md*에서는 readers에게 이 샘플을 탐구함으로써 무엇을 배울 것인지를 알려주어야 합니다. *readme.md* 파일에는 [.NET 문서 사이트](https://docs.microsoft.com/dotnet/welcome)에 있는 라이브 문서에 대한 링크도 포함되어야 합니다. 리포지토리의 지정된 파일이 해당 사이트에 매핑되는 위치를 확인하려면 리포지토리 경로의 `/docs`를 `https://docs.microsoft.com/dotnet`으로 바꿉니다.

항목에는 샘플에 대한 링크도 포함됩니다. GitHub의 샘플 폴더에 직접 연결합니다.

### <a name="write-a-new-sample"></a>새 샘플 작성

샘플은 다운로드를 위한 전체 프로그램 및 라이브러리입니다. 샘플의 범위는 작을 수 있지만, 사용자가 직접 살펴보고 실험해 볼 수 있는 방법으로 개념을 예시합니다. 예제에 대한 지침에 따라 독자는 다운로드하고 살펴볼 수 있습니다. 각 지침의 예제로 [PLINQ(병렬 LINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) 샘플을 검토합니다.

1. 샘플은 **빌드 가능한 프로젝트의 일부여야 합니다**. 가능한 경우 프로젝트는 .NET Core에서 지원하는 모든 플랫폼에 빌드되어야 합니다. 이에 대한 예외는 플랫폼별 기능 또는 플랫폼별 도구를 보여주는 샘플입니다.

2. 샘플이 일관성을 유지하려면 [corefx 코딩 스타일](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md)을 준수해야 합니다.

   또한 새 개체를 인스턴스화할 필요가 없는 것을 시연할 때 인스턴스 메서드보다 `static` 메서드를 사용하는 것이 좋습니다.

3. 샘플에는 **적절한 예외 처리**가 포함되어야 합니다. 샘플의 컨텍스트에서 throw될 수 있는 모든 예외를 처리해야 합니다. 예를 들어 사용자 입력을 검색하기 위해 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 메서드를 호출하는 샘플은 메서드에 대한 인수로 문자열을 전달할 때 적절한 예외 처리를 사용해야 합니다. 마찬가지로 샘플에서 메서드 호출이 실패할 것으로 예상되는 경우 결과 예외를 처리해야 합니다. [예외](https://docs.microsoft.com/dotnet/api/system.exception) 또는 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception)과 같은 기본 클래스 예외가 아닌 메서드가 throw한 특정 예외를 항상 처리합니다.

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

    ```dotnetcli
    dotnet build
    ```

2. 다음과 같이 샘플을 실행합니다.

    ```dotnetcli
    dotnet run
    ```

3. 샘플의 루트 디렉터리에 readme.md를 추가합니다.

   여기에는 코드에 대한 간략한 설명이 포함되어야 하며 샘플을 참조하는 문서를 참조해야 합니다. *readme.md*의 맨 위에는 [샘플 브라우저](https://docs.microsoft.com/samples)에 필요한 메타데이터가 있어야 합니다. 헤더 블록에는 다음 필드가 포함되어야 합니다.

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - `languages` 컬렉션에는 샘플에 사용할 수 있는 언어만 포함되어야 합니다.
   - `products` 컬렉션에는 샘플과 관련된 제품만 포함되어야 합니다.

명시된 경우를 제외하고 모든 샘플은 .NET Core에서 지원되는 모든 플랫폼의 명령줄에서 빌드됩니다. Visual Studio와 관련된 샘플이 몇 가지 있으며 Visual Studio 2017 이상이 필요합니다. 또한 일부 샘플은 플랫폼별 기능을 나타내며 특정 플랫폼이 필요합니다. 다른 샘플 및 코드 조각에는 .NET Framework가 필요하고, Windows 플랫폼에서 실행되며, 대상 Framework 버전용 Developer Pack이 필요합니다.

## <a name="the-c-interactive-experience"></a>C# 대화형 환경

문서에 포함된 모든 샘플은 [언어 태그](../code-in-docs.md)를 사용하여 원본 언어를 나타냅니다. C#의 짧은 코드 샘플은 `csharp-interactive` 언어 태그를 사용하여 브라우저에서 실행되는 C# 샘플을 지정할 수 있습니다. (인라인 코드 샘플은 `csharp-interactive` 태그를 사용하고, 소스에서 포함된 코드 조각의 경우 `code-csharp-interactive` 태그를 사용합니다.) 이러한 코드 샘플은 문서에 코드 창과 출력창을 표시합니다. 출력 창은 사용자가 샘플을 실행한 후 대화형 코드를 실행할 때의 모든 출력을 표시합니다.

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

### <a name="contributing-to-international-content"></a>국가별 콘텐츠 기여

MT(기계 번역) 콘텐츠에 대한 기여는 현재 허용되지 않습니다. MT 콘텐츠의 품질을 개선하기 위해 인공신경망 MT 엔진으로 전환되었습니다. 인공신경망 MT 엔진을 학습시키는 데 사용되는 HT(사람이 한 번역) 콘텐츠에 대한 기여는 허용 및 권장됩니다. 따라서 시간을 두고 점차 HT 콘텐츠에 대한 기여가 HT 및 MT 모두의 품질을 개선합니다. MT 토픽에는 토픽의 일부가 MT일 수 있음을 나타내는 고지 사항이 있으며, 편집을 사용할 수 없으므로 **편집** 단추가 표시되지 않습니다.

## <a name="contributor-license-agreement"></a>기여자 라이선스 계약

PR이 병합되기 전에 [.NET Foundation CLA(Contribution License Agreement)](https://cla.dotnetfoundation.org)에 서명해야 합니다. 이는 .NET Foundation의 프로젝트에 대한 일회성 요구 사항입니다. Wikipedia에서 [CLA(Contribution License Agreements)](http://en.wikipedia.org/wiki/Contributor_License_Agreement)에 대한 자세한 내용을 볼 수 있습니다.

계약: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

미리 계약서에 서명할 필요는 없습니다. 평소대로 PR을 복제, 포크 및 제출할 수 있습니다. PR이 생성되면 CLA 봇에 의해 분류됩니다. 변경 내용이 작은 경우(예:오타를 수정한 경우) PR에 `cla-not-required`로 레이블이 지정됩니다. 그렇지 않으면 `cla-required`로 분류됩니다. CLA에 서명하면 현재 및 향후의 모든 끌어오기 요청은 `cla-signed`로 레이블이 지정됩니다.
