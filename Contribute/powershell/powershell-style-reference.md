---
title: cmdlet 참조 작성을 위한 특수 지침
description: 이 문서에서는 PowerShell 코드 샘플 서식 지정을 위한 특정 규칙을 제공합니다. 이 내용은 cmdlet 참조뿐 아니라 예제가 포함된 개념 문서에 적용됩니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290291"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="33329-104">참조 문서 업데이트</span><span class="sxs-lookup"><span data-stu-id="33329-104">Updating reference articles</span></span>

<span data-ttu-id="33329-105">Cmdlet 참조 문서에는 특정 구조가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33329-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="33329-106">이 구조는 [PlatyPS][]에 의해 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="33329-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="33329-107">PlatyPS는 PowerShell 모듈에 대한 cmdlet 도움말을 생성하는 데 사용하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="33329-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="33329-108">PlatyPS는 cmdlet의 기본 Markdown 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33329-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="33329-109">Markdown 파일을 편집한 후 PlatyPS는 `Get-Help` cmdlet에서 사용되는 MAML 도움말 파일을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="33329-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="33329-110">PlatyPS에는 코드로 작성되는 cmdlet 참조용 하드 코드된 스키마가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33329-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="33329-111">[platyPS.schema.md][] 문서는 이 구조를 설명하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="33329-112">스키마 위반으로 인해 기여를 수락하기 전에 수정해야 하는 빌드 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="33329-113">일반 지침</span><span class="sxs-lookup"><span data-stu-id="33329-113">General guidelines</span></span>

- <span data-ttu-id="33329-114">헤더 구조를 제거하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="33329-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="33329-115">PlatyPS에는 특정 헤더 세트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="33329-116">**입력 형식** 및 **출력 형식** 헤더에는 형식이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="33329-117">Cmdlet이 입력을 사용하지 않거나 값을 반환하지 않으면 “None” 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="33329-118">펜스 코드 블록은 [예제](#format-for-examples) 섹션에서만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="33329-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="33329-119">인라인 코드 범위는 모든 단락에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33329-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="33329-120">About_ 파일 서식 지정</span><span class="sxs-lookup"><span data-stu-id="33329-120">Formatting About_ files</span></span>

<span data-ttu-id="33329-121">이제 `About_*` 파일은 PlatyPS 대신 [Pandoc][]에서 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="33329-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="33329-122">`About_*` 파일은 모든 버전의 PowerShell 및 게시 도구와 최상의 호환성을 제공하도록 서식이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="33329-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="33329-123">리포지토리 유지 관리자를 사용하여 체크 인하지 않고 `about_*` 파일의 서식을 변경하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="33329-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="33329-124">기본 서식 지정 지침:</span><span class="sxs-lookup"><span data-stu-id="33329-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="33329-125">줄을 80자로 제한</span><span class="sxs-lookup"><span data-stu-id="33329-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="33329-126">Pandoc은 변환하는 동안 공백 4개만큼 들여 쓰므로 코드 블록, 블록 따옴표 및 테이블은 76자로 제한됨</span><span class="sxs-lookup"><span data-stu-id="33329-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="33329-127">테이블은 76자 이내로 맞춰야 함</span><span class="sxs-lookup"><span data-stu-id="33329-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="33329-128">여러 줄에서 셀 콘텐츠를 수동으로 래핑</span><span class="sxs-lookup"><span data-stu-id="33329-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="33329-129">각 줄에서 여는 및 닫는 `|` 문자 사용</span><span class="sxs-lookup"><span data-stu-id="33329-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="33329-130">[about_Comparison_Operators][about-example]에서 작업 예제 확인</span><span class="sxs-lookup"><span data-stu-id="33329-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="33329-131">Pandoc의 특수 문자 `\`, `$`, `` ` `` 및 `<`을 사용하는 경우</span><span class="sxs-lookup"><span data-stu-id="33329-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="33329-132">헤더 내 - 이 문자는 선행 `\` 문자를 사용하여 이스케이프되어야 함</span><span class="sxs-lookup"><span data-stu-id="33329-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="33329-133">단락 내 - 이 문자는 코드 범위에 넣어야 함</span><span class="sxs-lookup"><span data-stu-id="33329-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="33329-134">예:</span><span class="sxs-lookup"><span data-stu-id="33329-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="33329-135">예제 형식</span><span class="sxs-lookup"><span data-stu-id="33329-135">Format for examples</span></span>

<span data-ttu-id="33329-136">PlatyPS 스키마에서 **EXAMPLES** 헤더는 H2 헤더이며 각 예제는 H3 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="33329-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="33329-137">예제 내에서 스키마를 사용하여 코드 블록을 단락으로 구분할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33329-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="33329-138">유효한 스키마는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="33329-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="33329-139">각 예제에 번호를 매기고 간단한 제목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="33329-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="33329-140">예:</span><span class="sxs-lookup"><span data-stu-id="33329-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org