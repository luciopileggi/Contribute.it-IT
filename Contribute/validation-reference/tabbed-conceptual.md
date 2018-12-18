# <a name="tabbed-conceptual"></a><span data-ttu-id="899b8-101">Contenuto concettuale a schede</span><span class="sxs-lookup"><span data-stu-id="899b8-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="899b8-102">La sintassi per il contenuto concettuale a schede è deprecata e non devono essere aggiunte nuove schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="899b8-103">Le convalide descritte in questo articolo si applicano ai set di contenuto approvati per l'uso del contenuto concettuale a schede finché non è disponibile una funzionalità sostitutiva.</span><span class="sxs-lookup"><span data-stu-id="899b8-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="899b8-104">Sintassi delle schede</span><span class="sxs-lookup"><span data-stu-id="899b8-104">Tab syntax</span></span>

<span data-ttu-id="899b8-105">La sintassi per le schede è la seguente:</span><span class="sxs-lookup"><span data-stu-id="899b8-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="899b8-106">Scheda a livello singolo:</span><span class="sxs-lookup"><span data-stu-id="899b8-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="899b8-107">Scheda dipendente facoltativa:</span><span class="sxs-lookup"><span data-stu-id="899b8-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="899b8-108">Esempio di sezione di scheda a livello singolo con due schede e il carattere di terminazione del gruppo di schede (---):</span><span class="sxs-lookup"><span data-stu-id="899b8-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="899b8-109">Facoltativamente le schede possono contenere schede secondarie o schede di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="899b8-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="899b8-110">In questo modo le schede diventano dipendenti nella selezione in un altro set di schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="899b8-111">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="899b8-111">Here's an example:</span></span>

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

<span data-ttu-id="899b8-112">Le seguenti convalide si applicano alla sintassi delle schede:</span><span class="sxs-lookup"><span data-stu-id="899b8-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="899b8-113">La sintassi delle schede deve essere corretta.</span><span class="sxs-lookup"><span data-stu-id="899b8-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="899b8-114">Le schede dipendenti devono essere definite in un gruppo precedente di schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="899b8-115">È consentito un solo livello di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="899b8-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="899b8-116">Non sono consentite meno di due schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="899b8-117">Non sono consentite più di quattro schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="899b8-118">Le schede devono essere incluse nell'elenco degli elementi consentiti.</span><span class="sxs-lookup"><span data-stu-id="899b8-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="899b8-119">Le coppie scheda/ID devono essere valide.</span><span class="sxs-lookup"><span data-stu-id="899b8-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="899b8-120">Non è possibile avere lo stesso ID scheda più volte in un gruppo di schede.</span><span class="sxs-lookup"><span data-stu-id="899b8-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="899b8-121">Schede incluse nell'elenco degli elementi consentiti</span><span class="sxs-lookup"><span data-stu-id="899b8-121">Tab whitelist</span></span>

<span data-ttu-id="899b8-122">Le seguenti coppie nome scheda/ID scheda sono incluse nell'elenco degli elementi consentiti.</span><span class="sxs-lookup"><span data-stu-id="899b8-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="899b8-123">Gli ID delle schede dipendenti non sono accoppiati ma devono essere validi in base alla colonna degli ID scheda.</span><span class="sxs-lookup"><span data-stu-id="899b8-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="899b8-124">I valori fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="899b8-124">The values are case-sensitive</span></span>

|<span data-ttu-id="899b8-125">Nome scheda</span><span class="sxs-lookup"><span data-stu-id="899b8-125">Tab name</span></span>              |<span data-ttu-id="899b8-126">ID scheda</span><span class="sxs-lookup"><span data-stu-id="899b8-126">Tab ID</span></span>            |
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