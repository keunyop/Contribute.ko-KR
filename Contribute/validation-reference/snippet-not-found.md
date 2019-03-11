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
# <a name="snippet-not-found"></a><span data-ttu-id="30e17-103">snippet-not-found</span><span class="sxs-lookup"><span data-stu-id="30e17-103">snippet-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="30e17-104">경고</span><span class="sxs-lookup"><span data-stu-id="30e17-104">Warning</span></span>

`Code snippet '{snippet path}' not found.`

<span data-ttu-id="30e17-105">코드 조각 참조가 지정된 경로에 없거나 현재 파일에서 경로를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="30e17-105">The code snippet references doesn't exist at the specified path, or the path isn't available from the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="30e17-106">해결 방법</span><span class="sxs-lookup"><span data-stu-id="30e17-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="30e17-107">코드 조각 경로가 올바른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="30e17-107">Ensure that your snippet path is correct.</span></span> <span data-ttu-id="30e17-108">코드 조각이 현재 리포지토리 외부에 저장된 경우 리포지토리가 종속 리포지토리로 구성되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="30e17-108">If the snippet is stored outside the current repo, make sure the repo is configured ase a dependent repo.</span></span> <span data-ttu-id="30e17-109">자세한 내용은 Microsoft 내부 [코드 조각 문서](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30e17-109">For more information, see the Microsoft-internal [code snippet article](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
