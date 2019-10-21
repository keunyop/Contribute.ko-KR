---
title: PowerShell 문서 리포지토리에 기여
description: 이 문서는 PowerShell 문서를 구성하는 리포지토리입니다.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290176"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="9ac56-103">PowerShell 문서에 기여</span><span class="sxs-lookup"><span data-stu-id="9ac56-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="9ac56-104">PowerShell 문서에 관심을 가져 주셔서 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="9ac56-105">이 문서에서는 PowerShell 문서 사이트에서 호스트되는 문서 및 코드 샘플에 기여하는 프로세스를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="9ac56-106">기여는 오타 수정만큼 간단하거나 새로운 문서처럼 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="9ac56-107">PowerShell 문서 사이트는 하나 이상의 docset를 포함하는 여러 리포지토리에서 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="9ac56-108">[PowerShell 개념 및 cmdlet 참조][psdocs]</span><span class="sxs-lookup"><span data-stu-id="9ac56-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="9ac56-109">PowerShell SDK 코드 샘플 - SDK 문서에 사용된 샘플을 포함하는 프라이빗 리포지토리</span><span class="sxs-lookup"><span data-stu-id="9ac56-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="9ac56-110">[PowerShell .NET SDK 참조](/dotnet/api/?view=pscore-6.2.0) - PowerShell 원본 코드에서 생성된 프라이빗 리포지토리 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="9ac56-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="9ac56-111">이 모든 콘텐츠에 대한 이슈는 [PowerShell-Docs][docsrepo] 리포지토리에서 추적됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="9ac56-112">리포지토리 구조</span><span class="sxs-lookup"><span data-stu-id="9ac56-112">Repository Structure</span></span>

<span data-ttu-id="9ac56-113">PowerShell-Docs 리포지토리는 [Microsoft Docs][psdocs]에 게시된 세 개의 docset로 구성됩니다. docset는 다음 폴더에 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="9ac56-114">[/reference/][ref] - PowerShell에서 제공되는 cmdlet의 PowerShell cmdlet 참조를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="9ac56-115">참조는 버전 폴더(3.0, 4.0, 5.0, 5.1, 6 및 7)에서 수집됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="9ac56-116">이 docset는 Windows 또는 기타 Microsoft 제품에서 제공되는 모듈의 참조를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="9ac56-117">[/reference/docs-conceptual][conceptual] - PowerShell 개념 문서를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="9ac56-118">여기에는 설정 지침, 샘플 스크립트, 방법 항목 등이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="9ac56-119">[/developer/][SDK] - PowerShell SDK 개념 문서를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac56-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
