---
title: included-file-redirected
description: Docs 빌드 문제 included-file-redirected에 대한 설명 및 해결 방법
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459076"
---
# <a name="included-file-redirected"></a><span data-ttu-id="f206e-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="f206e-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="f206e-104">경고</span><span class="sxs-lookup"><span data-stu-id="f206e-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="f206e-105">해결 방법</span><span class="sxs-lookup"><span data-stu-id="f206e-105">Resolution</span></span>

<span data-ttu-id="f206e-106">리디렉션된 파일을 포함하지 않도록 콘텐츠를 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f206e-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="f206e-107">예를 들어 포함된 참조를 포함하거나 제거할 새 파일을 만들고 콘텐츠에 링크하거나 온라인으로 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="f206e-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
