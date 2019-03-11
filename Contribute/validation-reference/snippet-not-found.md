---
title: snippet-not-found
description: Docs 빌드 문제 snippet-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459099"
---
# <a name="snippet-not-found"></a>snippet-not-found

## <a name="warning"></a>경고

`Code snippet '{snippet path}' not found.`

코드 조각 참조가 지정된 경로에 없거나 현재 파일에서 경로를 사용할 수 없습니다.

## <a name="resolution"></a>해결 방법

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

코드 조각 경로가 올바른지 확인합니다. 코드 조각이 현재 리포지토리 외부에 저장된 경우 리포지토리가 종속 리포지토리로 구성되어 있는지 확인합니다. 자세한 내용은 Microsoft 내부 [코드 조각 문서](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)를 참조하세요.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
