---
title: Markdown 제목
description: Markdown 제목에 필요한 요구 사항을 설명합니다.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084558"
---
# <a name="markdown-headings"></a><span data-ttu-id="4f1f9-103">Markdown 제목</span><span class="sxs-lookup"><span data-stu-id="4f1f9-103">Markdown headings</span></span>

<span data-ttu-id="4f1f9-104">다음 유효성 검사 요구 사항이 OPS Markdown 파일의 제목에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="4f1f9-105">H1</span><span class="sxs-lookup"><span data-stu-id="4f1f9-105">H1</span></span>

<span data-ttu-id="4f1f9-106">`H1`은 Markdown 파일의 첫 번째 제목을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="4f1f9-107">docs.microsoft.com에 게시하면 H1이 페이지 맨 위에 큰 글꼴로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="4f1f9-108">H1은 단일 해시(`#`), 공백 및 제목 텍스트를 차례로 사용하는 행을 시작하여 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="4f1f9-109">예를 들어 이 문서의 H1은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="4f1f9-110">H1 제목에는 다음 규칙이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="4f1f9-111">파일에 H1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="4f1f9-112">하나의 H1만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-112">There can only be one H1.</span></span>
- <span data-ttu-id="4f1f9-113">H1에 콘텐츠가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="4f1f9-114">`#`과 H1 콘텐츠 사이에 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="4f1f9-115">공백이 없는 H1은 게시된 페이지에서 제목으로 렌더링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="4f1f9-116">H1은 파일에서 YML 메타데이터 헤더 다음의 첫 번째 콘텐츠여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="4f1f9-117">텍스트나 이미지와 같은 콘텐츠는 YML 헤더의 끝과 H1 사이에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="4f1f9-118">첫 번째 수준 제목에 대한 HTML 요소 `<h1>`은 사용하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="4f1f9-119">Markdown 구문(`# `)을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="4f1f9-120">H1은 100자 이하여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="4f1f9-121">스타일 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="4f1f9-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="4f1f9-122">H2 - H6</span></span>

<span data-ttu-id="4f1f9-123">H2(`## `)-H6(`###### `)는 OPS에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="4f1f9-124">제목을 만들려면 HTML(`<h2>` - `<h6>`)을 사용하지 말고 Markdown 헤더를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
