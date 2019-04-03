---
ms.date: 03/29/2019
ms.openlocfilehash: 4e07ecf777f1361e21343b7b80f59ad9c5e86b3e
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653414"
---
# <a name="tabbed-conceptual"></a>Contenuto concettuale a schede

> [!IMPORTANT]
> La sintassi per il contenuto concettuale a schede è deprecata e non devono essere aggiunte nuove schede. Le convalide descritte in questo articolo si applicano ai set di contenuto approvati per l'uso del contenuto concettuale a schede finché non è disponibile una funzionalità sostitutiva.

## <a name="tab-syntax"></a>Sintassi delle schede

La sintassi per le schede è la seguente:

Scheda a livello singolo:

`# [Tab Display Name](#tab/tab-id)`

Scheda dipendente facoltativa:

`# [Tab Display Name](#tab/tab-id/tab-condition)`

Esempio di sezione di scheda a livello singolo con due schede e il carattere di terminazione del gruppo di schede (---):

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

Facoltativamente le schede possono contenere schede secondarie o schede di dipendenza. In questo modo le schede diventano dipendenti nella selezione in un altro set di schede. Ad esempio:

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

Le seguenti convalide si applicano alla sintassi delle schede:

- La sintassi delle schede deve essere corretta.
- Le schede dipendenti devono essere definite in un gruppo precedente di schede.
- È consentito un solo livello di dipendenza.
- Non sono consentite meno di due schede.
- Non sono consentite più di quattro schede.
- Le schede devono essere approvate.
- Le coppie scheda/ID devono essere valide.
- Non è possibile avere lo stesso ID scheda più volte in un gruppo di schede.

## <a name="approved-tabs"></a>Schede approvate

Le coppie nome scheda/ID scheda seguenti sono approvate. Gli ID delle schede dipendenti non sono accoppiati ma devono essere validi in base alla colonna degli ID scheda. I valori fanno distinzione tra maiuscole e minuscole

|Nome scheda              |ID scheda            |
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