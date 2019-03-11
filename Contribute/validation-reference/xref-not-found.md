---
title: xref-not-found
description: Docs 빌드 문제 xref-not-found에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427874"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>경고

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

연결된 UID가 없거나 리포지토리에서 사용할 수 없습니다.

## <a name="resolution"></a>해결 방법

Microsoft 내부 [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) 문서에 설명된 대로 UID가 올바르고 Xref Service가 리포지토리에 적절하게 구성되었는지 확인합니다.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
