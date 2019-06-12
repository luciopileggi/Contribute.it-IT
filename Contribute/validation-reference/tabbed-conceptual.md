---
ms.date: 03/29/2019
title: Contenuto concettuale a schede
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841308"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="013c9-102">Contenuto concettuale a schede</span><span class="sxs-lookup"><span data-stu-id="013c9-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="013c9-103">La sintassi per il contenuto concettuale a schede è deprecata e non devono essere aggiunte nuove schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="013c9-104">Le convalide descritte in questo articolo si applicano ai set di contenuto approvati per l'uso del contenuto concettuale a schede finché non è disponibile una funzionalità sostitutiva.</span><span class="sxs-lookup"><span data-stu-id="013c9-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="013c9-105">Sintassi delle schede</span><span class="sxs-lookup"><span data-stu-id="013c9-105">Tab syntax</span></span>

<span data-ttu-id="013c9-106">La sintassi per le schede è la seguente:</span><span class="sxs-lookup"><span data-stu-id="013c9-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="013c9-107">Scheda a livello singolo:</span><span class="sxs-lookup"><span data-stu-id="013c9-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="013c9-108">Scheda dipendente facoltativa:</span><span class="sxs-lookup"><span data-stu-id="013c9-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="013c9-109">Esempio di sezione di scheda a livello singolo con due schede e il carattere di terminazione del gruppo di schede (---):</span><span class="sxs-lookup"><span data-stu-id="013c9-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="013c9-110">Facoltativamente le schede possono contenere schede secondarie o schede di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="013c9-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="013c9-111">In questo modo le schede diventano dipendenti nella selezione in un altro set di schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="013c9-112">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="013c9-112">Here's an example:</span></span>

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

<span data-ttu-id="013c9-113">Le seguenti convalide si applicano alla sintassi delle schede:</span><span class="sxs-lookup"><span data-stu-id="013c9-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="013c9-114">La sintassi delle schede deve essere corretta.</span><span class="sxs-lookup"><span data-stu-id="013c9-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="013c9-115">Le schede dipendenti devono essere definite in un gruppo precedente di schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="013c9-116">È consentito un solo livello di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="013c9-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="013c9-117">Non sono consentite meno di due schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="013c9-118">Non sono consentite più di quattro schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="013c9-119">Le schede devono essere approvate.</span><span class="sxs-lookup"><span data-stu-id="013c9-119">Tabs must be approved.</span></span>
- <span data-ttu-id="013c9-120">Le coppie scheda/ID devono essere valide.</span><span class="sxs-lookup"><span data-stu-id="013c9-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="013c9-121">Non è possibile avere lo stesso ID scheda più volte in un gruppo di schede.</span><span class="sxs-lookup"><span data-stu-id="013c9-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="013c9-122">Schede approvate</span><span class="sxs-lookup"><span data-stu-id="013c9-122">Approved tabs</span></span>

<span data-ttu-id="013c9-123">Le coppie nome scheda/ID scheda seguenti sono approvate.</span><span class="sxs-lookup"><span data-stu-id="013c9-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="013c9-124">Gli ID delle schede dipendenti non sono accoppiati ma devono essere validi in base alla colonna degli ID scheda.</span><span class="sxs-lookup"><span data-stu-id="013c9-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="013c9-125">I valori fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="013c9-125">The values are case-sensitive</span></span>

|<span data-ttu-id="013c9-126">Nome scheda</span><span class="sxs-lookup"><span data-stu-id="013c9-126">Tab name</span></span>              |<span data-ttu-id="013c9-127">ID scheda</span><span class="sxs-lookup"><span data-stu-id="013c9-127">Tab ID</span></span>            |
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