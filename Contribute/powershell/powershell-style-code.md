---
title: Linee guida specifiche per la scrittura di esempi di script
description: Questo articolo include le regole specifiche per la formattazione degli esempi di codice di PowerShell. Tali regole sono valide sia per gli articoli concettuali con esempi, che per le informazioni di riferimento sui cmdlet.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290266"
---
# <a name="formatting-code-samples"></a>Formattazione degli esempi di codice

Nella documentazione esistente sono stati usati più stili nel tempo e le regole di formattazione sono cambiate più volte. L'obiettivo è quello di definire uno stile coerente per i blocchi di codice e l'output di PowerShell nella documentazione.

Markdown supporta due stili di codice diversi:

- Intervalli di codice (inline) contrassegnati da un singolo carattere di apice inverso (`` ` ``). Stile usato inline in un paragrafo anziché come blocco autonomo. Usato più di frequente per racchiudere i nomi dei cmdlet. Vedere [Formattazione degli elementi della sintassi dei comandi ](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Blocchi di codice, ovvero un blocco di più righe racchiuso tra stringhe con triplo apice inverso (`` ``` ``).

## <a name="using-code-blocks"></a>Uso di blocchi di codice

Markdown consente di applicare il rientro per evidenziare un blocco di codice, ma questo modello può essere problematico ed è consigliabile evitarlo. Tutti i blocchi di codice devono essere contenuti in una sequenza di delimitazione del codice. Con codice delimitato si intende un blocco di codice racchiuso tra stringhe con triplo apice inverso (`` ``` ``). Gli indicatori di codice delimitato devono trovarsi sulla stessa riga, prima e dopo l'esempio di codice. L'indicatore all'inizio del blocco di codice può avere un'etichetta di linguaggio facoltativa. Open Publishing System (OPS) di Microsoft usa l'etichetta del linguaggio per supportare la funzionalità di evidenziazione della sintassi.

OPS aggiunge anche un pulsante **Copy** per copiare il contenuto del blocco di codice negli Appunti. In questo modo è possibile incollare rapidamente il codice in uno script per il test dell'esempio di codice. Tuttavia, non tutti gli esempi nella documentazione sono destinati a essere eseguiti in questo modo. Alcuni blocchi di codice possono essere una semplice illustrazione di un concetto di PowerShell o una rappresentazione astratta della sintassi.

Nella documentazione vengono usati due tipi di blocchi di codice:

1. Esempi illustrativi
2. Esempi eseguibili

## <a name="formatting-illustrative-examples"></a>Formattazione degli esempi illustrativi

Gli esempi illustrativi vengono usati per spiegare un concetto di PowerShell. Non sono pensati per essere copiati negli Appunti per l'esecuzione. Questo è il tipo di esempio usato più di frequente per semplici esempi facili da digitare.
Viene anche usato per esempi di sintassi in cui viene illustrata la sintassi di un comando.

Gli esempi illustrativi usano una sequenza di delimitazione del codice "vuota" per contrassegnare l'inizio e la fine del blocco di codice. Il blocco di codice può contenere l'output di esempio del comando illustrato.

### <a name="syntax-block"></a>Blocco di sintassi

Questo esempio illustra tutti i possibili parametri del cmdlet `Get-Command`.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

In questo esempio viene illustrata l'istruzione `for` in termini generalizzati:

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Esempio di illustrazione semplice

Di seguito è riportato un esempio che illustra gli operatori di confronto di PowerShell:

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

Si noti che questo esempio include il prompt di PowerShell semplificato e mostra l'output risultante. In questo caso, non è previsto che il lettore copi ed esegua l'esempio.

## <a name="formatting-executable-examples"></a>Formattazione degli esempi eseguibili

Per gli esempi più complessi o per quelli di utilità progettati per poter essere copiati ed eseguiti, è previsto l'uso del markup dello stile di blocco seguente:

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

L'output visualizzato dai comandi di PowerShell deve essere racchiuso in un blocco di codice **Output** per evitare l'evidenziazione della sintassi. Ad esempio:

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

L'etichetta del codice **Output** non è una "linguaggio" ufficiale supportato dal sistema di evidenziazione della sintassi.
Questa etichetta è tuttavia utile perché OPS aggiunge l'etichetta "Output" alla casella del codice nella pagina Web
e per questa casella del codice "Output" non è prevista alcuna evidenziazione della sintassi.

## <a name="coding-style-rules"></a>Regole di stile di codifica

### <a name="avoid-line-continuation-in-code-samples"></a>Evitare la continuazione di riga negli esempi di codice

Evitare di usare i caratteri di continuazione di riga (`` ` ``) negli esempi di codice di PowerShell. Si tratta di caratteri difficili da visualizzare e possono causare problemi se sono presenti spazi aggiuntivi alla fine della riga.

- Usare la funzionalità di splatting di PowerShell per ridurre la lunghezza della riga per i cmdlet con numerosi parametri.
- Sfruttare le opportunità di interruzione di riga naturali di PowerShell, come dopo i caratteri pipe (`|`), le parentesi graffe di apertura, le parentesi e le parentesi quadre.

### <a name="avoid-using-powershell-prompts-in-examples"></a>Evitare di usare i prompt di PowerShell negli esempi

L'uso della stringa di prompt è sconsigliato e deve essere limitato agli scenari che hanno lo scopo di illustrare l'utilizzo della riga di comando. I prompt sono necessari per esempi che illustrano comandi che modificano il prompt o quando il percorso visualizzato è significativo per lo scenario illustrato.

- I prompt di PowerShell devono essere usati solo negli esempi illustrativi. Per la maggior parte di questi esempi, la stringa di prompt deve essere "`PS>`". Questo prompt è indipendente dagli indicatori specifici del sistema operativo.
- I prompt **NON** devono essere usati negli esempi eseguibili.

L'esempio seguente illustra come cambia il prompt quando si usa il provider del Registro di sistema.

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a>Non usare alias negli esempi

È sempre consigliabile usare il nome completo di tutti i cmdlet e i parametri, a meno che l'esempio non sia pensato per illustrare in modo specifico l'alias. I nomi di cmdlet e parametri devono usare l'ortografia con la combinazione di maiuscole/minuscole Pascal corretta definita nel codice.

### <a name="using-parameters-in-examples"></a>Uso dei parametri negli esempi

Evitare di usare parametri posizionali. In generale, è consigliabile usare sempre il nome del parametro in un esempio, anche se il parametro è posizionale. In questo modo si riduce la possibilità di confusione negli esempi.
