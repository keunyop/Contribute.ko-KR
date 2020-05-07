---
title: 자동 둥근 따옴표 바꾸기 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack을 통해 자동으로 둥근 따옴표를 바꾸는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336707"
---
# <a name="smart-quote-replacement"></a>둥근 따옴표 바꾸기

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

콘텐츠 개발자는 최신 기술 및 인텔리전스의 몇 가지 가장 발전된 기능을 만드는 일을 담당하고 있으나 아직도 현재의 도구는 Markdown에서 “곧은 따옴표”의 사용을 선호합니다. 그 반대는 “둥근 따옴표”입니다. 둥근 따옴표는 이상적인 입력 체계에서 일반적으로 사용되지만 Markdown 및 렌더링된 HTML에서는 선호되지 않습니다.

예를 들어 Microsoft Word 문서에서 작업하는 경우 <kbd>Shift</kbd> 키를 누른 상태로 <kbd>"</kbd>를 입력하면 Microsoft Word가 `"` 문자를 해당하는 둥근 따옴표 문자(`“`)로 빠르게 바꿉니다.

| Description        | 유니코드  | 둥근 따옴표 | 바꾸기 |
|--------------------|----------|-------------|-------------|
| 왼쪽 큰따옴표  | `\u201c` | `“`         | `"`         |
| 오른쪽 큰따옴표 | `\u201d` | `”`         | `"`         |
| 왼쪽 작은따옴표  | `\u2018` | `‘`         | `'`         |
| 오른쪽 작은따옴표 | `\u2019` | `’`         | `'`         |

Markdown( *\*.md*) 파일에서 텍스트를 붙여넣거나 콘텐츠를 업데이트할 때 이 기능을 사용하면 콘텐츠를 적극적으로 평가하고 값을 평가에 따라 자동으로 바꿉니다.

> [!NOTE]
> 둥근 따옴표 바꾸기 기능은 `©, ™, ®, •`, 아래 첨자 및 위 첨자 문자와 같은 다른 문자도 바꿉니다(여기에 나온 문자로 제한되지 않음). 이 기능은 Word 문서에서 텍스트를 붙여넣을 때 유용합니다.

## <a name="preferences"></a>기본 설정

이 기능은 선택 사항이지만, 기본적으로 `true`로 설정되어 있습니다. 이 기능을 설정하거나 해제하도록 토글하려면 다음을 수행합니다.

1. **파일** > **기본 설정** > **설정** 및 Docs Markdown 확장별 필터를 선택합니다. 
1. **Markdown: 둥근 따옴표 바꾸기** 섹션에서 설정을 토글합니다.

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![둥근 따옴표 바꾸기 데모](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
