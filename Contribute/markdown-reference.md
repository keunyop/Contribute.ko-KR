---
title: docs.microsoft.com에 대한 Markdown 참조
description: Microsoft Docs 플랫폼에서 사용되는 Markdown 기능 및 구문을 알아봅니다.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592556"
---
# <a name="markdown-reference"></a><span data-ttu-id="0d494-103">Markdown 참조</span><span class="sxs-lookup"><span data-stu-id="0d494-103">Markdown Reference</span></span>

<span data-ttu-id="0d494-104">Markdown은 일반 텍스트 서식 구문을 사용하는 경량 생성 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="0d494-105">Docs 플랫폼은 Markdown에 대한 CommonMark 표준과 docs.microsoft.com에서 더 풍부한 콘텐츠를 제공하도록 설계된 사용자 지정 Markdown 확장을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="0d494-106">이 문서에서는 docs.microsoft.com에 대해 Markdown을 사용하기 위한 사전순 참조를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="0d494-107">텍스트 편집기를 사용하여 Markdown을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="0d494-108">표준 Markdown 구문과 사용자 지정 Docs 확장을 쉽게 삽입할 수 있는 편집기의 경우 [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack)이 설치된 [VS Code](https://code.visualstudio.com/)를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="0d494-109">Docs에서는 Markdig Markdown 엔진을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="0d494-110">[https://babelmark.github.io/](https://babelmark.github.io/)에서 Markdig 및 기타 엔진에 대한 Markdown의 렌더링을 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="0d494-111">경고(Note, Tip, Important, Caution, Warning)</span><span class="sxs-lookup"><span data-stu-id="0d494-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="0d494-112">Docs Markdown 확장을 경고하여 docs.microsoft.com에서 콘텐츠의 중요도를 색과 아이콘으로 표시하여 렌더링하는 블록 따옴표를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="0d494-113">다음과 같은 경고 유형이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-113">The following alert types are supported:</span></span>

```md
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="0d494-114">이러한 경고는 docs.microsoft.com에서 다음과 같이 보입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-114">These alerts look like this on docs.microsoft.com:</span></span>

![게시된 Docs 페이지에서 이전 예제의 경고가 다른 아이콘 및 색으로 어떻게 표시되는지를 보여 주는 이미지](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="0d494-116">코드 조각</span><span class="sxs-lookup"><span data-stu-id="0d494-116">Code snippets</span></span>

<span data-ttu-id="0d494-117">Markdown 파일에 코드 조각을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="0d494-118">제목</span><span class="sxs-lookup"><span data-stu-id="0d494-118">Headings</span></span>

<span data-ttu-id="0d494-119">Docs는 6가지 수준의 Markdown 제목을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="0d494-120">마지막 `#`과 제목 텍스트 사이에는 공백이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="0d494-121">각 Markdown 파일에는 H1이 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="0d494-122">H1은 파일에서 YML 메타데이터 블록 다음의 첫 번째 콘텐츠여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="0d494-123">H2는 게시된 파일의 오른쪽 탐색 메뉴에 자동으로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="0d494-124">하위 수준의 제목은 그렇지 않으므로 H2를 전략적으로 사용하여 독자가 콘텐츠를 탐색하는 것을 돕습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="0d494-125">`<h1>`과 같은 HTML 제목은 권장되지 않으며 경우에 따라 빌드 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-125">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="0d494-126">[책갈피](#bookmark-links)를 통해 파일의 개별 제목에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="0d494-127">HTML</span><span class="sxs-lookup"><span data-stu-id="0d494-127">HTML</span></span>

<span data-ttu-id="0d494-128">Markdown은 인라인 HTML을 지원하지만 HTML은 Docs에 게시하도록 권장되지 않으며 제한된 값 목록을 제외하고는 빌드 오류 또는 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="0d494-129">이미지</span><span class="sxs-lookup"><span data-stu-id="0d494-129">Images</span></span>

<span data-ttu-id="0d494-130">이미지를 포함하는 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="0d494-131">여기서 `alt text`는 이미지에 대한 간략한 설명이고 `<folder path>`는 이미지에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="0d494-132">시각 장애인용 화면 읽기 프로그램에는 대체 텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="0d494-133">또한 이미지를 렌더링할 수 없는 사이트 버그가 있는 경우에도 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="0d494-134">이미지는 문서 집합 내의 `/media` 폴더에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="0d494-135">기본적으로 이미지에 대해 다음 파일 형식이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="0d494-136">.jpg</span><span class="sxs-lookup"><span data-stu-id="0d494-136">.jpg</span></span>
- <span data-ttu-id="0d494-137">.png</span><span class="sxs-lookup"><span data-stu-id="0d494-137">.png</span></span>

<span data-ttu-id="0d494-138">문서 세트의 docfx.json 파일에 리소스로 추가하여 다른 이미지 형식에 대한 지원을</span><span class="sxs-lookup"><span data-stu-id="0d494-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="0d494-139">추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="0d494-140">링크</span><span class="sxs-lookup"><span data-stu-id="0d494-140">Links</span></span>

<span data-ttu-id="0d494-141">대부분의 경우 Docs는 다른 파일 및 페이지에 대한 표준 Markdown 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="0d494-142">링크 유형은 아래의 하위 섹션에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="0d494-143">VS Code용 Docs Authoring Pack은 경로를 찾는 번거로움 없이 상대 링크와 책갈피를 올바르게 삽입하는 데 도움을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d494-144">Microsoft 사이트에 대한 링크에 ko-kr와 같은 로캘 코드를 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="0d494-145">하드 코딩된 로캘 코드는 지역화된 콘텐츠가 렌더링되지 못하게 합니다. 이는 다른 로캘의 사용자에게 좋지 않은 고객 환경이며 상당한 지역화 비용이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="0d494-146">브라우저에서 URL을 복사하면 로캘 코드가 기본적으로 포함되므로 링크를 만들 때 수동으로 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="0d494-147">예를 들어 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="0d494-148">다음을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="0d494-149">동일한 문서 집합에서 파일에 대한 상대 링크</span><span class="sxs-lookup"><span data-stu-id="0d494-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="0d494-150">상대 경로는 현재 파일을 기준으로 대상 파일에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="0d494-151">Docs에서는 상대 경로를 사용하여 동일한 문서 세트 내의 다른 파일에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="0d494-152">상대 경로에 대한 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="0d494-153">여기서 `../`는 계층 구조에서 한 수준 위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="0d494-154">상대 경로는 빌드 중에 .md 확장명 제거를 포함하여 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="0d494-155">“../”를 사용하여 부모 폴더의 파일에 연결할 수 있지만, 해당 파일이 같은 문서 집합에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="0d494-156">“../”를 사용하여 다른 문서 집합 폴더의 파일에 연결할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="0d494-157">Docs는 또한 "~"로 시작하는 특별한 양식의 상대 경로(예: ~/foo/bar.md)도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="0d494-158">이 구문은 문서 집합의 루트 폴더를 기준으로 한 파일임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="0d494-159">이러한 종류의 경로도 빌드 중에 유효성이 검사되고 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d494-160">상대 경로에 파일 확장명을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="0d494-161">빌드는 상대 경로의 대상 파일이 있는지를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="0d494-162">상대 경로에 파일 확장명이 포함되어 있지 않으면 빌드가 끊어진 링크 경고를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="0d494-163">예를 들어 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="0d494-164">다음을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="0d494-165">Docs의 다른 파일에 대한 사이트 상대 경로</span><span class="sxs-lookup"><span data-stu-id="0d494-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="0d494-166">파일 확장명(.md)을 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="0d494-167">이것은 Azure “articles” 문서 집합 외부의 Linux 개요 파일에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="0d494-168">외부 사이트로 연결</span><span class="sxs-lookup"><span data-stu-id="0d494-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="0d494-169">다른 웹 페이지로 URL 기반 연결(https://를 포함해야 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="0d494-170">책갈피 링크</span><span class="sxs-lookup"><span data-stu-id="0d494-170">Bookmark links</span></span>

<span data-ttu-id="0d494-171">같은 리포지토리의 다른 파일 제목에 대한 책갈피 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="0d494-172">예:</span><span class="sxs-lookup"><span data-stu-id="0d494-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="0d494-173">현재 파일의 제목에 대한 책갈피 링크</span><span class="sxs-lookup"><span data-stu-id="0d494-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="0d494-174">`#` 해시 표시 뒤에 제목의 단어를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="0d494-175">제목 텍스트를 링크 텍스트로 변경하려면 다음을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="0d494-176">모두 소문자 사용</span><span class="sxs-lookup"><span data-stu-id="0d494-176">Use all lowercase characters</span></span>
- <span data-ttu-id="0d494-177">문장 부호 제거</span><span class="sxs-lookup"><span data-stu-id="0d494-177">Remove punctuation</span></span>
- <span data-ttu-id="0d494-178">공백을 대시로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="0d494-178">Replace spaces with dashes</span></span>

<span data-ttu-id="0d494-179">예를 들어, 제목 이름이 "2.2 Security concerns"인 경우 책갈피 링크 텍스트는 "#22-security-concerns"입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="0d494-180">명시적 앵커 링크</span><span class="sxs-lookup"><span data-stu-id="0d494-180">Explicit anchor links</span></span>

<span data-ttu-id="0d494-181">허브 및 방문 페이지를 제외하고는 `<a>` HTML 태그를 사용하는 명시적 앵커 링크가 **필요하거나 권장되지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="0d494-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="0d494-182">일반 Markdown 파일에 위에서 설명한 대로 책갈피를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="0d494-183">허브 및 방문 페이지의 경우 다음과 같이 앵커를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="0d494-184">`## <a id="AnchorText"> </a>Header text` 또는 `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="0d494-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="0d494-185">명시적 앵커에 연결하려면 다음 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="0d494-186">XREF(상호 참조) 링크</span><span class="sxs-lookup"><span data-stu-id="0d494-186">XREF (cross reference) links</span></span>

<span data-ttu-id="0d494-187">현재 문서 집합 또는 다른 문서 집합에서 자동 생성된 API 참조 페이지에 연결하려면 UID(고유한 ID)와 함께 XREF 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="0d494-188">다른 문서 집합에서 API 참조 페이지를 참조하려면 `docfx.json` 파일에서 `xrefService` 구성을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="0d494-189">UID는 정규화된 클래스 및 멤버 이름과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="0d494-190">UID 뒤에 \*를 추가하면 링크는 특정 API가 아닌 오버로드 페이지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="0d494-191">예를 들어 `List<T>.BinarySearch*`를 사용하여 `List<T>.BinarySearch(T, IComparer<T>)`와 같은 특정 과부하로 연결하는 대신 BinarySearch 메서드 페이지에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="0d494-192">다음 구문 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="0d494-193">자동 연결: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="0d494-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="0d494-194">선택적 `displayProperty` 쿼리 매개 변수는 정규화된 링크 텍스트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="0d494-195">기본적으로 링크 텍스트는 멤버 또는 형식 이름만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="0d494-196">Markdown 링크: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="0d494-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="0d494-197">표시되는 링크 텍스트를 사용자 지정하려면 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="0d494-198">예제:</span><span class="sxs-lookup"><span data-stu-id="0d494-198">Examples:</span></span>

- <span data-ttu-id="0d494-199">`<xref:System.String>`은 “String”으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="0d494-200">`<xref:System.String?displayProperty=nameWithType>`은 “System.String”으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="0d494-201">`[String class](xref:System.String)`는 “String class”로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="0d494-202">지금은 UID를 쉽게 찾는 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="0d494-203">API의 UID를 찾는 가장 좋은 방법은 연결하려는 API 페이지의 소스를 보고 ms.assetid 값을 찾는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="0d494-204">개별 오버로드 값은 소스에 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="0d494-205">Microsoft는 시스템 개선을 위해 노력하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="0d494-206">UID에 특수 문자 \`, \# 또는 \*이 포함되는 경우 UID 값을 `%60`, `%23` 및 `%2A`로 각각 HTML 인코딩해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="0d494-207">때때로 괄호 인코딩을 보게 되겠지만 이는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="0d494-208">예제:</span><span class="sxs-lookup"><span data-stu-id="0d494-208">Examples:</span></span>

- <span data-ttu-id="0d494-209">System.Threading.Tasks.Task\`1은 `System.Threading.Tasks.Task%601`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="0d494-210">System.Exception.\#ctor은 `System.Exception.%23ctor`이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="0d494-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode)은 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="0d494-212">목록(번호 매김, 글머리 기호, 검사 목록)</span><span class="sxs-lookup"><span data-stu-id="0d494-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="0d494-213">번호 매기기 목록</span><span class="sxs-lookup"><span data-stu-id="0d494-213">Numbered list</span></span>

<span data-ttu-id="0d494-214">번호 매기기 목록을 만들려면, 모두 1을 사용할 수 있으며 이것은 게시할 때 순차 목록으로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="0d494-215">소스 가독성을 높이기 위해 목록을 증가시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="0d494-216">중첩 목록을 포함하여 목록에 문자를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="0d494-217">Docs에 게시할 때 올바르게 렌더링되지 않습니다. 숫자를 사용하여 중첩된 목록은 게시될 때 소문자로 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="0d494-218">예:</span><span class="sxs-lookup"><span data-stu-id="0d494-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="0d494-219">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-219">This renders as follows:</span></span>

1. <span data-ttu-id="0d494-220">This is</span><span class="sxs-lookup"><span data-stu-id="0d494-220">This is</span></span>
1. <span data-ttu-id="0d494-221">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="0d494-221">a parent numbered list</span></span>
   1. <span data-ttu-id="0d494-222">and this is</span><span class="sxs-lookup"><span data-stu-id="0d494-222">and this is</span></span>
   1. <span data-ttu-id="0d494-223">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="0d494-223">a nested numbered list</span></span>
1. <span data-ttu-id="0d494-224">(fin)</span><span class="sxs-lookup"><span data-stu-id="0d494-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="0d494-225">글머리 기호 목록</span><span class="sxs-lookup"><span data-stu-id="0d494-225">Bulleted list</span></span>

<span data-ttu-id="0d494-226">글머리 기호 목록을 만들려면 각 줄의 시작 위치에 `-`와 공백을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="0d494-227">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-227">This renders as follows:</span></span>

- <span data-ttu-id="0d494-228">This is</span><span class="sxs-lookup"><span data-stu-id="0d494-228">This is</span></span>
- <span data-ttu-id="0d494-229">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="0d494-229">a parent bulleted list</span></span>
  - <span data-ttu-id="0d494-230">and this is</span><span class="sxs-lookup"><span data-stu-id="0d494-230">and this is</span></span>
  - <span data-ttu-id="0d494-231">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="0d494-231">a nested bulleted list</span></span>
- <span data-ttu-id="0d494-232">All done!</span><span class="sxs-lookup"><span data-stu-id="0d494-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="0d494-233">검사 목록</span><span class="sxs-lookup"><span data-stu-id="0d494-233">Checklist</span></span>

<span data-ttu-id="0d494-234">검사 목록은 사용자 지정 Markdown 확장을 통해 docs.microsoft.com에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="0d494-235">이 예제는 다음과 같이 docs.microsoft.com에서 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="0d494-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="0d494-236">List item 1</span></span>
> * <span data-ttu-id="0d494-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="0d494-237">List item 2</span></span>
> * <span data-ttu-id="0d494-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="0d494-238">List item 3</span></span>

<span data-ttu-id="0d494-239">문서의 처음이나 끝에 있는 검사 목록을 사용하여 “학습할 내용” 또는 “학습한 내용” 콘텐츠를 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="0d494-240">문서 전체에 임의의 검사 목록을 추가하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="0d494-241">다음 단계 작업</span><span class="sxs-lookup"><span data-stu-id="0d494-241">Next step action</span></span>

<span data-ttu-id="0d494-242">사용자 지정 확장 프로그램을 사용하여 docs.microsoft.com의 페이지에만 다음 단계 작업 단추를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="0d494-243">구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="0d494-244">예:</span><span class="sxs-lookup"><span data-stu-id="0d494-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="0d494-245">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="0d494-246">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="0d494-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="0d494-247">다른 웹 페이지에 대한 Markdown 링크를 포함하여 다음 단계 작업에서 지원되는 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="0d494-248">대부분의 경우 다음 작업 링크는 동일한 문서 집합에 있는 다른 파일에 대한 상대 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="0d494-249">섹션 정의</span><span class="sxs-lookup"><span data-stu-id="0d494-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="0d494-250">섹션을 정의해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-250">You might need to define a section.</span></span> <span data-ttu-id="0d494-251">이 구문은 대개 코드 테이블에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="0d494-252">다음 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d494-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="0d494-253">앞의 blockquote Markdown 텍스트는 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="0d494-254">선택기</span><span class="sxs-lookup"><span data-stu-id="0d494-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="0d494-255">같은 문서의 다른 페이지에 연결할 때 선택기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="0d494-256">그러면 독자는 해당 페이지 간에 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="0d494-257">이 확장은 docs.microsoft.com과 MSDN에서 서로 다르게 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="0d494-258">단일 선택기</span><span class="sxs-lookup"><span data-stu-id="0d494-258">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="0d494-259">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="0d494-268">다중 선택기</span><span class="sxs-lookup"><span data-stu-id="0d494-268">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="0d494-269">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-269">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="플랫폼" title2="백 엔드"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a><span data-ttu-id="0d494-282">테이블</span><span class="sxs-lookup"><span data-stu-id="0d494-282">Tables</span></span>

<span data-ttu-id="0d494-283">Markdown에서 테이블을 만드는 가장 간단한 방법은 파이프 및 줄을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="0d494-284">헤더가 있는 표준 테이블을 만들려면 첫 번째 선을 파선으로 그립니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="0d494-285">이것은 다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-285">This renders as follows:</span></span>

|<span data-ttu-id="0d494-286">This is</span><span class="sxs-lookup"><span data-stu-id="0d494-286">This is</span></span>   |<span data-ttu-id="0d494-287">a simple</span><span class="sxs-lookup"><span data-stu-id="0d494-287">a simple</span></span>   |<span data-ttu-id="0d494-288">table header</span><span class="sxs-lookup"><span data-stu-id="0d494-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="0d494-289">table</span><span class="sxs-lookup"><span data-stu-id="0d494-289">table</span></span>     |<span data-ttu-id="0d494-290">data</span><span class="sxs-lookup"><span data-stu-id="0d494-290">data</span></span>       |<span data-ttu-id="0d494-291">here</span><span class="sxs-lookup"><span data-stu-id="0d494-291">here</span></span>        |
|<span data-ttu-id="0d494-292">it doesn't</span><span class="sxs-lookup"><span data-stu-id="0d494-292">it doesn't</span></span>|<span data-ttu-id="0d494-293">actually</span><span class="sxs-lookup"><span data-stu-id="0d494-293">actually</span></span>   |<span data-ttu-id="0d494-294">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="0d494-294">have to line up nicely!</span></span>||

<span data-ttu-id="0d494-295">헤더가 없는 테이블을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-295">You can also create a table without a header.</span></span> <span data-ttu-id="0d494-296">예를 들어 다중 열 목록을 만들려면:</span><span class="sxs-lookup"><span data-stu-id="0d494-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="0d494-297">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="0d494-298">This</span><span class="sxs-lookup"><span data-stu-id="0d494-298">This</span></span> | <span data-ttu-id="0d494-299">table</span><span class="sxs-lookup"><span data-stu-id="0d494-299">table</span></span> |
| <span data-ttu-id="0d494-300">has no</span><span class="sxs-lookup"><span data-stu-id="0d494-300">has no</span></span> | <span data-ttu-id="0d494-301">header</span><span class="sxs-lookup"><span data-stu-id="0d494-301">header</span></span> |

<span data-ttu-id="0d494-302">콜론을 사용하여 열을 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="0d494-303">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="0d494-304">right aligned:</span><span class="sxs-lookup"><span data-stu-id="0d494-304">right aligned:</span></span>|
|<span data-ttu-id="0d494-305">:left aligned</span><span class="sxs-lookup"><span data-stu-id="0d494-305">:left aligned</span></span>     |
|<span data-ttu-id="0d494-306">:centered        :</span><span class="sxs-lookup"><span data-stu-id="0d494-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="0d494-307">VS Code용 Docs Authoring Extension을 사용하면 기본 Markdown 테이블을 쉽게 추가할 수 있습니다!</span><span class="sxs-lookup"><span data-stu-id="0d494-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="0d494-308">[온라인 테이블 생성기](http://www.tablesgenerator.com/markdown_tables)를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="0d494-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="0d494-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d494-310">이것은 docs.microsoft.com 사이트에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="0d494-311">Markdown에서 테이블을 만드는 경우 테이블이 오른쪽 탐색으로 확장되어 읽을 수 없게 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="0d494-312">필요한 경우 문서 렌더링에서 테이블을 나눌 수 있도록 허용하여 이 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="0d494-313">`[!div class="mx-tdBreakAll"]` 사용자 지정 클래스로 테이블을 래핑하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="0d494-314">다음은 클래스 이름이 `mx-tdBreakAll`인 `div`로 래핑될 행이 세 개인 테이블의 Markdown 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="0d494-315">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="0d494-316">Name</span><span class="sxs-lookup"><span data-stu-id="0d494-316">Name</span></span>|<span data-ttu-id="0d494-317">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d494-317">Syntax</span></span>|<span data-ttu-id="0d494-318">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="0d494-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="0d494-319">Description</span><span class="sxs-lookup"><span data-stu-id="0d494-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="0d494-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="0d494-320">Quiet</span></span>|<span data-ttu-id="0d494-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="0d494-321">/quiet</span></span>|<span data-ttu-id="0d494-322">Yes</span><span class="sxs-lookup"><span data-stu-id="0d494-322">Yes</span></span>|<span data-ttu-id="0d494-323">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="0d494-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="0d494-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="0d494-324">NoRestart</span></span>|<span data-ttu-id="0d494-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="0d494-325">/norestart</span></span>|<span data-ttu-id="0d494-326">No</span><span class="sxs-lookup"><span data-stu-id="0d494-326">No</span></span>|<span data-ttu-id="0d494-327">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="0d494-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="0d494-328">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="0d494-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="0d494-329">Help</span><span class="sxs-lookup"><span data-stu-id="0d494-329">Help</span></span>|<span data-ttu-id="0d494-330">/help</span><span class="sxs-lookup"><span data-stu-id="0d494-330">/help</span></span>|<span data-ttu-id="0d494-331">No</span><span class="sxs-lookup"><span data-stu-id="0d494-331">No</span></span>|<span data-ttu-id="0d494-332">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="0d494-332">Provides help and quick reference.</span></span> <span data-ttu-id="0d494-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="0d494-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="0d494-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="0d494-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d494-335">이것은 docs.microsoft.com 사이트에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="0d494-336">때때로 테이블의 두 번째 열에 매우 긴 단어가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="0d494-337">이것을 깔끔하게 분리하려면 앞서 보았듯이 `div` 래퍼 구문을 사용하여 `mx-tdCol2BreakAll` 클래스를 적용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="0d494-338">HTML 테이블</span><span class="sxs-lookup"><span data-stu-id="0d494-338">HTML Tables</span></span>

<span data-ttu-id="0d494-339">HTML 테이블은 docs.microsoft.com에 사용하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="0d494-340">소스에서 사람이 읽을 수 없으며 이것이 Markdown의 핵심 원칙입니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="0d494-341">비디오</span><span class="sxs-lookup"><span data-stu-id="0d494-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="0d494-342">Markdown 페이지에 비디오 포함</span><span class="sxs-lookup"><span data-stu-id="0d494-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="0d494-343">현재 Docs는 다음 3개 위치 중 하나에 게시된 비디오를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="0d494-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="0d494-344">YouTube</span></span>
- <span data-ttu-id="0d494-345">Channel9</span><span class="sxs-lookup"><span data-stu-id="0d494-345">Channel 9</span></span>
- <span data-ttu-id="0d494-346">Microsoft 고유 'One Player' 시스템</span><span class="sxs-lookup"><span data-stu-id="0d494-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="0d494-347">다음 구문으로 비디오를 포함할 수 있으며, 그러면 Docs에서 렌더링합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="0d494-348">예제:</span><span class="sxs-lookup"><span data-stu-id="0d494-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="0d494-349">다음과 같이 렌더링됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="0d494-350">그리고 게시된 페이지에 다음과 같이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="0d494-351">CH9 비디오 URL은 `https`로 시작하고 `/player`로 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="0d494-352">그렇지 않으면 비디오만이 아니라 전체 페이지를 포함하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="0d494-353">새 비디오 업로딩</span><span class="sxs-lookup"><span data-stu-id="0d494-353">Uploading new videos</span></span>

<span data-ttu-id="0d494-354">모든 새 비디오는 다음 프로세스에 따라 업로드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="0d494-355">IDWEB에서 **docs_video_users** 그룹에 조인합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="0d494-356">[https://aka.ms/VideoUploadRequest](https://aka.ms/VideoUploadRequest )로 이동하고 비디오에 대한 세부 사항을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="0d494-357">다음이 필요합니다(이러한 항목은 공개되지 않음).</span><span class="sxs-lookup"><span data-stu-id="0d494-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="0d494-358">비디오의 제목</span><span class="sxs-lookup"><span data-stu-id="0d494-358">A title for your video.</span></span>
    1. <span data-ttu-id="0d494-359">비디오가 관련된 제품/서비스 목록</span><span class="sxs-lookup"><span data-stu-id="0d494-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="0d494-360">비디오가 호스트되는 대상 페이지 또는 (아직 페이지가 없는 경우) 문서 집합</span><span class="sxs-lookup"><span data-stu-id="0d494-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="0d494-361">비디오에 대한 MP4 파일 링크(파일을 배치할 위치가 없으면 임시로 여기에 배치할 수 있음: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="0d494-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="0d494-362">MP4 파일은 720p 이상이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="0d494-363">비디오 설명</span><span class="sxs-lookup"><span data-stu-id="0d494-363">A description of the video.</span></span>
1. <span data-ttu-id="0d494-364">항목을 제출(저장)합니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="0d494-365">2 영업일 이내에 비디오가 업로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="0d494-366">포함에 필요한 링크가 작업 항목에 배치되고 확인되어 *전달됩니다*.</span><span class="sxs-lookup"><span data-stu-id="0d494-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="0d494-367">비디오 링크를 얻었으면 작업 항목을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="0d494-368">다음 구문을 사용하여 비디오 링크를 게시물에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d494-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
