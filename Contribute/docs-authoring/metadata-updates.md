---
title: 메타데이터 업데이트 - Docs Authoring Pack
description: Visual Studio Code 확장인 Docs Authoring Pack의 메타데이터를 업데이트하는 방법을 알아봅니다.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336638"
---
# <a name="update-metadata"></a>메타데이터 업데이트

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>요약

Markdown( *\*.md*) 파일에는 메타데이터와 관련된 두 개의 상황에 맞는 메뉴 항목이 있습니다. 텍스트 편집기의 아무 곳이나 마우스 오른쪽 단추로 클릭하면 다음과 유사한 메뉴 항목이 표시됩니다.

:::image type="content" source="media/update-metadata-menu.png" alt-text="메타데이터 업데이트 상황에 맞는 메뉴":::

## <a name="update-msdate-metadata-value"></a>`ms.date` 메타데이터 값 업데이트

**`ms.date` 메타데이터 값 업데이트** 옵션을 선택하면 현재 Markdown 파일 `ms.date` 값이 오늘 날짜로 설정됩니다. 문서에 `ms.date` 메타데이터 필드가 없으면 아무 작업도 수행되지 않습니다.

## <a name="update-implicit-metadata-values"></a>암시적 메타데이터 값 업데이트

**암시적 메타데이터 값 업데이트** 옵션을 선택하면 암시적으로 지정할 수 있는 모든 가능한 메타데이터 값을 찾아 바꿉니다. 메타데이터 값은 *docfx.json* 파일의 `build/fileMetadata` 노드에서 암시적으로 지정됩니다. `fileMetadata` 노드에 있는 각각의 키 값 쌍은 메타데이터 기본값을 나타냅니다. 예를 들어 *메타데이터 값을 생략하는*top-level/sub-folder`ms.author` 디렉터리의 Markdown 파일은 `fileMetadata` 노드에 사용할 기본값을 암시적으로 지정할 수 있습니다.

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

이 경우 모든 Markdown 파일이 `ms.author: dapine` 메타데이터 값을 암시적으로 허용합니다. 이 기능은 *docfx.json* 파일에 있는 이러한 암시적 설정에 적용됩니다. Markdown 파일에 암시적 값이 아닌 값으로 명시적으로 설정된 값을 사용하는 메타데이터가 있는 경우 해당 값은 재정의됩니다.

다음 Markdown 파일 메타데이터를 살펴보세요. 이 Markdown 파일은 **top-level/sub-folder/includes/example.md**에 있습니다.

```markdown
---
ms.author: someone-else
---

# Content
```

이 파일에서 **암시적 메타데이터 값 업데이트** 옵션이 실행된 경우 위의 *docfx.json* 콘텐츠를 사용하는 것으로 가정하면 메타데이터 값이 `ms.author: dapine`로 업데이트됩니다.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>예제

다음은 이 기능에 대한 간단한 데모입니다.

[![메타데이터 업데이트 데모](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
