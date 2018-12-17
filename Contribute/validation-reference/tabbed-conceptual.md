# <a name="tabbed-conceptual"></a>탭 개념

> [!IMPORTANT]
> 탭 개념 구문이 사용되지 않으므로 새 탭이 추가되지 않야아 합니다. 이 문서에서 설명된 유효성 검사는 대체 기능이 지원될 때까지 탭 개념을 사용하도록 승인된 콘텐츠 세트에 지원됩니다.

## <a name="tab-syntax"></a>탭 구문

탭의 구문은 다음과 같습니다.

단일 수준 탭:

`# [Tab Display Name](#tab/tab-id)`

선택적 종속 탭:

`# [Tab Display Name](#tab/tab-id/tab-condition)`

두 개의 탭 및 탭 그룹 종결자(---)가 있는 단일 수준 탭 섹션의 예제:

```
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

탭에는 선택적으로 보조 탭 또는 종속성 탭이 포함될 수 있습니다. 그러면 탭이 다른 일련의 탭에서 선택 영역에 종속됩니다. 예를 들면 다음과 같습니다.

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

다음 유효성 검사는 탭 구문에 적용됩니다.

- 탭 구문은 정확해야 합니다.
- 종속 탭은 이전 탭 그룹에서 정의되어야 합니다.
- 한 개 수준의 종속성만 허용됩니다.
- 두 개 이상의 탭이 허용됩니다.
- 네 개 이하의 탭이 허용됩니다.
- 탭이 허용 목록으로 지정되어야 합니다.
- 탭/ID 쌍이 유효해야 합니다.
- 하나의 탭 그룹에 여러 번 동일한 탭 ID가 있을 수 없습니다.

## <a name="tab-whitelist"></a>탭 허용 목록

다음 탭 이름/탭 ID 쌍은 허용 목록으로 지정됩니다. 종속 탭 ID는 페어링되지 않지만 탭 ID 열에 대해 유효해야 합니다. 이 값은 대/소문자를 구분합니다.

|탭 이름              |탭 ID            |
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