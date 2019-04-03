---
ms.date: 03/29/2019
ms.openlocfilehash: 4e07ecf777f1361e21343b7b80f59ad9c5e86b3e
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653416"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="0d623-101">탭 개념</span><span class="sxs-lookup"><span data-stu-id="0d623-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d623-102">탭 개념 구문이 사용되지 않으므로 새 탭이 추가되지 않야아 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="0d623-103">이 문서에서 설명된 유효성 검사는 대체 기능이 지원될 때까지 탭 개념을 사용하도록 승인된 콘텐츠 세트에 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="0d623-104">탭 구문</span><span class="sxs-lookup"><span data-stu-id="0d623-104">Tab syntax</span></span>

<span data-ttu-id="0d623-105">탭의 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="0d623-106">단일 수준 탭:</span><span class="sxs-lookup"><span data-stu-id="0d623-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="0d623-107">선택적 종속 탭:</span><span class="sxs-lookup"><span data-stu-id="0d623-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="0d623-108">두 개의 탭 및 탭 그룹 종결자(---)가 있는 단일 수준 탭 섹션의 예제:</span><span class="sxs-lookup"><span data-stu-id="0d623-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="0d623-109">탭에는 선택적으로 보조 탭 또는 종속성 탭이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="0d623-110">그러면 탭이 다른 일련의 탭에서 선택 영역에 종속됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="0d623-111">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-111">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="0d623-112">다음 유효성 검사는 탭 구문에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="0d623-113">탭 구문은 정확해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="0d623-114">종속 탭은 이전 탭 그룹에서 정의되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="0d623-115">한 개 수준의 종속성만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="0d623-116">두 개 이상의 탭이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="0d623-117">네 개 이하의 탭이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="0d623-118">탭이 승인되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-118">Tabs must be approved.</span></span>
- <span data-ttu-id="0d623-119">탭/ID 쌍이 유효해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="0d623-120">하나의 탭 그룹에 여러 번 동일한 탭 ID가 있을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="0d623-121">승인된 탭</span><span class="sxs-lookup"><span data-stu-id="0d623-121">Approved tabs</span></span>

<span data-ttu-id="0d623-122">다음 탭 이름/탭 ID 쌍은 승인됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-122">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="0d623-123">종속 탭 ID는 페어링되지 않지만 탭 ID 열에 대해 유효해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="0d623-124">이 값은 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="0d623-124">The values are case-sensitive</span></span>

|<span data-ttu-id="0d623-125">탭 이름</span><span class="sxs-lookup"><span data-stu-id="0d623-125">Tab name</span></span>              |<span data-ttu-id="0d623-126">탭 ID</span><span class="sxs-lookup"><span data-stu-id="0d623-126">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |