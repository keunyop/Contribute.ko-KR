---
title: 개발자 언어 완성 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack에서 제공하는 개발자 언어 완성 기능이 기여자에게 어떻게 도움이 되는지 알아봅니다.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336799"
---
# <a name="dev-lang-completion"></a>개발자 언어 완성

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

기여자가 Markdown 파일에서 세 개의 억음 악센트 기호(코드 펜스 시작 부분) 다음에 올 수 있는 유효한 언어 식별자(개발자 언어)를 결정하는 데는 도움이 필요합니다. 아쉽게도 개발자 언어에 대한 빌드 시간 유효성 검사는 존재하지 않습니다. 그 결과 동일한 개념 문서 집합에 단일 언어에 대한 서로 다른 표시가 나타날 수 있습니다.

C#을 예로 들어 보겠습니다. 기여자는 해당 언어에 대한 개발자 언어 표시로 `c#`, `C#`, `cs`, `csharp` 등을 사용합니다. 이러한 표시 중 올바른 것은 무엇인가요?

‘개발자 언어 완성’ 기능은 알려진 개발자 언어 목록을 표시하여 혼동이 발생하지 않도록 합니다. IntelliSense에서 개발자 언어 이름을 선택하면 다음 작업이 수행됩니다.

* 코드 펜스가 닫힙니다.
* 캐럿이 코드 펜스에 배치됩니다.

## <a name="preferences"></a>기본 설정

이 기능은 사용하지 않도록 설정할 수 없습니다. 사용할 수 있는 설정은 다음과 같습니다.

* [일반적으로 사용되는 개발자 언어 표시](#display-commonly-used-dev-langs)
* [모든 알려진 개발자 언어 표시](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>일반적으로 사용되는 개발자 언어 표시

단일 문서 집합에는 유효한 개발자 언어의 일부만 사용됩니다. 사용자 환경을 개선하려면 다음을 수행합니다.

1. Visual Studio Code에서 루트 디렉터리의 문서 집합을 엽니다.
1. **파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다.
1. **Markdown: 문서 집합 언어** 섹션에서 **settings.json에서 편집** 링크를 클릭합니다.
1. 다음 `markdown.docsetLanguages` 속성을 *settings.json* 파일에 추가합니다.

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. 속성의 빈 배열에 캐럿을 배치하고 IntelliSense를 활성화합니다(<kbd>Ctrl</kbd> + <kbd>Space</kbd> 사용). 알려진 개발자 언어 이름 목록이 표시됩니다.
1. 필요한 만큼 배열에 개발자 언어 이름을 추가합니다. 예를 들어 다음 목록에서는 세 개의 억음 악센트 기호를 입력하면 네 개의 개발자 언어 이름이 사용자에게 표시됩니다.

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. 변경 내용을 *settings.json* 파일에 저장합니다.

> [!WARNING]
> `markdown.docsetLanguages` 배열을 비워 두면 모든 알려진 개발자 언어가 표시됩니다.

### <a name="display-all-known-dev-langs"></a>모든 알려진 개발자 언어 표시

기본적으로 모든 알려진 개발자 언어 이름이 IntelliSense에 표시됩니다. 이 설정은 [일반적으로 사용되는 개발자 언어 표시](#display-commonly-used-dev-langs)에 설명된 `markdown.docsetLanguages` 속성을 재정의합니다.

이 설정을 변경하려면 다음을 수행합니다.

1. **파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다.
1. **Markdown: 모든 사용 가능한 언어** 섹션에서 설정을 토글합니다.

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![개발자 언어 완성](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
