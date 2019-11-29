---
title: insecure-link
description: Docs 빌드 문제 insecure-link에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528836"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> 콘텐츠 팀이 시간을 두고 영향을 가늠하고 리포지토리를 정리할 계획을 세우도록 처음에 이 규칙을 “제안”으로 활성화했습니다. **그러나 2019년 12월 20일에는 “제안”이 “경고”로 상향 조정됩니다**.

## <a name="suggestion"></a>제안

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

이 메시지는 `http`와 함께 명시적인 Markdown 링크를 사용했거나 `www.microsoft.com`과 같은 원시 URL을 사용했음을 의미합니다. 원시 URL은 Docs에 게시될 때 안전하지 않은 링크로 변환되며 사용되지 않아야 합니다.

## <a name="resolution"></a>해결 방법

`http` 대신 `https`를 사용하도록 모든 URL을 Microsoft 사이트로 변경합니다.

링크가 원시 URL인 경우 다음과 같이 `https`로 시작하는 명시적 Markdown 링크로 변경합니다.

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> VS Code에 대한 Docs Markdown에는 Microsoft 링크의 정리 스크립트가 포함됩니다. 이 스크립트는 리포지퇴에서 Microsoft 사이트의 모든 링크를 확인하여 링크가 `http` 대신 `https`로 시작하며 `en-us`와 같은 로캘 코드를 포함하지 않는지 확인합니다. 스크립트를 실행하려면 다음을 수행합니다.
>
> 1. VS Code용 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 확장을 설치합니다.
> 1. Alt+M을 클릭하여 Markdown 메뉴를 엽니다.
> 1. **정리**를 선택한 후 **Microsoft 링크**를 선택합니다.

경우에 따라 정규화된 도메인 이름과 같이 클릭 가능한 링크를 제공하지 않는 웹 주소를 문서화해야 할 수도 있습니다. 이 경우 다음과 같이 인라인 코드로 웹 주소의 스타일을 지정해야 합니다.

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
