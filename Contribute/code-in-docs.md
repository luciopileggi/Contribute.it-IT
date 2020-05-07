---
title: Come includere codice in docs
description: Informazioni su come includere elementi e frammenti di codice negli articoli per la pubblicazione in docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336484"
---
# <a name="how-to-include-code-in-docs"></a>Come includere codice in docs

Esistono diversi modi per includere il codice in un articolo pubblicato in docs.microsoft.com:

* Singoli elementi (parole) all'interno di una riga.

  Ecco un esempio dello stile `code`.

  Usare il formato codice quando si fa riferimento a variabili e parametri denominati in un blocco di codice vicino all'interno del testo. Il formato codice può essere usato anche per proprietà, metodi, classi e parole chiave del linguaggio. Per altre informazioni, vedere la sezione [Elementi di codice](#code-elements) più avanti in questo articolo.

* Blocchi di codice nel file Markdown dell'articolo.

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Usare i blocchi di codice inline quando non è possibile visualizzare il codice facendo riferimento a un file di codice. Per altre informazioni, vedere la sezione [Blocchi di codice](#inline-code-blocks) più avanti in questo articolo.

* Blocchi di codice facendo riferimento a un file di codice nel repository locale.

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Per altre informazioni, vedere la sezione [Riferimenti a frammenti di codice nel repository](#in-repo-snippet-references) più avanti in questo articolo.

* Blocchi di codice facendo riferimento a un file di codice in un altro repository.

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Per altre informazioni, vedere la sezione [Riferimenti a frammenti di codice al di fuori del repository](#out-of-repo-snippet-references) più avanti in questo articolo.
  
* Blocchi di codice che consentono all'utente di eseguire codice nel browser.

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Per altre informazioni, vedere la sezione [Frammenti di codice interattivi](#interactive-code-snippets) più avanti in questo articolo.

Oltre a illustrare il Markdown per ognuno di questi metodi di inserimento di codice, l'articolo offre anche alcune [indicazioni generali per tutti i blocchi di codice](#code-blocks).

## <a name="code-elements"></a>Elementi del codice

Un "elemento del codice" è una parola chiave, un nome di classe, un nome di proprietà e altri oggetti di un linguaggio di programmazione. Non è sempre ovvio quali elementi vengono qualificati come codice. Ad esempio, i nomi di pacchetto NuGet devono essere considerati codice. In caso di dubbi, vedere [Linee guida per la formattazione del testo](text-formatting-guidelines.md).

### <a name="inline-code-style"></a>Stile codice inline

Per includere un elemento di codice nel testo dell'articolo, racchiuderlo tra apici inversi (\`) per indicare lo stile codice.
Nello stile codice inline non deve essere usato il formato del triplo apice inverso.

|Markdown |Rendering |
|---------|---------|
|Per impostazione predefinita, Entity Framework interpreta una proprietà denominata \`Id\` o \`ClassnameID\` come la chiave primaria.|Per impostazione predefinita, Entity Framework interpreta una proprietà denominata `Id` o `ClassnameID` come la chiave primaria.|

Quando un articolo è localizzato (tradotto in altre lingue), il testo con stile codice viene lasciato non tradotto. Se si vuole impedire la localizzazione senza usare lo stile codice, vedere [Stringhe non localizzate](markdown-reference.md#non-localized-strings).

### <a name="bold-style"></a>Stile grassetto

Alcune guide di stile meno recenti raccomandano l'uso del grassetto per il codice inline. Il grassetto è un'opzione da prendere in considerazione quando lo stile codice è talmente invadente da compromettere la leggibilità. Ad esempio una tabella Markdown composta principalmente da elementi di codice può apparire confusa se formattata interamente con lo stile codice. Se si sceglie di applicare lo stile grassetto, usare la [sintassi basata su stringhe non localizzate](markdown-reference.md#non-localized-strings) per assicurarsi che il codice non sia localizzato.

### <a name="links"></a>Collegamenti

In alcuni contesti, un collegamento alla documentazione di riferimento può essere più utile del formato di codice. Se si usa un collegamento, quindi, non applicare il formato di codice al testo del collegamento. Se si formatta un collegamento con lo stile codice, può risultare difficile capire che il testo è un collegamento.

Se si usa un collegamento e, in seguito, si fa riferimento allo stesso elemento nello stesso contesto, specificare le istanze successive in formato di codice anziché come collegamenti.

### <a name="placeholders"></a>Segnaposto

Se si vuole che l'utente sostituisca una sezione del codice visualizzato con valori personali, usare un testo segnaposto contrassegnato da parentesi acute o parentesi graffe. Ad esempio: `az group delete -n <ResourceGroupName>`. Spiegare che, quando si sostituisce il testo segnaposto con i valori reali, è necessario rimuovere le parentesi acute o graffe.

## <a name="code-blocks"></a>Blocchi di codice

La sintassi per l'inserimento di codice in un documento dipende dalla posizione del codice:

* [Nel file markdown dell'articolo](#inline-code-blocks)
* [In un file di codice nello stesso repository](#in-repo-snippet-references)
* [In un file di codice in un repository diverso](#out-of-repo-snippet-references)

Le linee guida seguenti sono applicabili a tutti e tre i tipi di blocchi di codice:

* [Automatizzare la convalida del codice.](#code-validation)
* [Evidenziare righe chiave del codice.](#highlighting)
* [Evitare le barre di scorrimento orizzontali.](#horizontal-scroll-bars)

### <a name="screenshots"></a>Screenshot

Tutti i metodi elencati nella sezione precedente danno origine a blocchi di codice utilizzabili:

* È possibile usarli per eseguire operazioni di copia e incolla.
* Sono indicizzati dai motori di ricerca.
* Sono accessibili dalle utilità per la lettura dello schermo.

Questi sono solo alcuni dei motivi per cui gli screenshot IDE non sono consigliati come metodi di inserimento di codice in un articolo. È opportuno usare screenshot IDE per il codice solo se si mostrano contenuti relativi all'IDE stesso, come nel caso di IntelliSense. È preferibile non usarli invece per mostrare l'applicazione di colori o sottolineature.

### <a name="code-validation"></a>Convalida del codice

Per alcuni repository sono disponibili processi implementati che compilano automaticamente tutto il codice di esempio per individuare eventuali errori. Il repository .NET è uno di questi. Per altre informazioni, vedere [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) (Contributi) nel repository .NET.

Se si includono blocchi di codice da un altro repository, concordare con i rispettivi proprietari una strategia di gestione del codice che, in caso di distribuzione di nuove versioni delle librerie usate dal codice, impedisca che il codice risulti obsoleto o danneggiato.

### <a name="highlighting"></a>Evidenziazione

I frammenti di codice includono in genere più codice rispetto al necessario per fornire contesto. Ciò consente di migliorare la leggibilità evidenziando le righe chiave nel frammento di codice su cui concentrarsi, come nell'esempio seguente:

![Esempio che mostra il codice evidenziato](media/code-in-docs/highlighted-code.png)

Non è possibile evidenziare il codice quando lo si include nel file markdown dell'articolo. L'evidenziazione funziona solo per i frammenti di codice inclusi facendo riferimento a un file di codice.

### <a name="horizontal-scroll-bars"></a>Barre di scorrimento orizzontali

Suddividere le righe lunghe per evitare le barre di scorrimento orizzontali. Le barre di scorrimento nei blocchi di codice peggiorano la leggibilità del codice. Sono particolarmente problematiche nei blocchi di codice più lunghi, in cui potrebbe risultare impossibile visualizzare contemporaneamente la barra di scorrimento e la riga da leggere.

Una buona norma per ridurre al minimo le barre di scorrimento orizzontali nei blocchi di codice consiste nel suddividere le righe di codice più lunghe di 85 caratteri. Tenere presente, tuttavia, che la presenza o l'assenza di una barra di scorrimento non è l'unico criterio di leggibilità. Se l'interruzione di una riga prima dell'85° carattere può comprometterne la leggibilità o ostacolarne il copia e incolla, è preferibile andare oltre gli 85 caratteri.

## <a name="inline-code-blocks"></a>Blocchi di codice inline

Usare i blocchi di codice inline solo quando non è possibile visualizzare il codice facendo riferimento a un file di codice. Il codice inline è generalmente più difficile da testare e mantenere aggiornato rispetto a un file di codice che fa parte di un progetto completo.  È possibile, inoltre, che il codice inline ometta parti di contesto che potrebbero aiutare gli sviluppatori a comprendere e usare meglio il codice. Queste considerazioni si applicano essenzialmente ai linguaggi di programmazione. I blocchi di codice inline possono essere usati anche per output e input (ad esempio, JSON), linguaggi di query (ad esempio, SQL) e linguaggi di scripting (ad esempio, PowerShell).
  
Esistono due modi per indicare che una sezione di testo in un file di articolo è un blocco di codice: *racchiuderla* tra apici inversi tripli (\`\`\`) o applicare un rientro. La prima soluzione è preferibile perché consente di specificare il linguaggio. Evitare di impostare rientri perché possono creare confusione e potrebbe essere difficile per un altro autore identificarli nel momento in cui deve modificare l'articolo.

Gli indicatori del linguaggio vengono posizionati subito dopo i tre apici inversi di apertura, come nell'esempio seguente:

Markdown:

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

Rendering:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Per informazioni sui valori che è possibile usare come indicatori di linguaggio, vedere [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases) (Nomi e alias dei linguaggi).

Se dopo i triplici apici inversi (\`\`\`) si usa un termine di linguaggio o ambiente non supportato, il termine viene visualizzato nella barra del titolo della sezione di codice relativa alla pagina di cui è stato eseguito il rendering. Se possibile, usare un indicatore di linguaggio o di ambiente nei blocchi di codice inline.

> [!NOTE]
> Se si copia e incolla codice da un documento di Word, assicurarsi che non siano presenti "virgolette curve", in quanto non valide nei blocchi di codice, ad esempio `“` e `’`. Se invece sono presenti, convertirle in virgolette normali (`'` e `"`). In alternativa, consultare l'articolo di Docs Authoring Pack relativo alla [funzionalità di sostituzione delle virgolette curve](docs-authoring/smart-quote-replacement.md).

## <a name="in-repo-snippet-references"></a>Riferimenti a frammenti di codice nel repository

Il modo migliore per includere in un documento frammenti di codice per linguaggi di programmazione è quello di fare riferimento a un file di codice. Questo metodo, infatti, offre la possibilità di evidenziare righe di codice e di rendere disponibile agli sviluppatori in GitHub un contesto più ampio del frammento di codice. È possibile includere frammenti di codice anche applicando il formato dei triplici due punti (:\:\:) manualmente o in Visual Studio Code con il supporto di [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. In Visual Studio Code fare clic su <kbd>ALT+M</kbd> o <kbd>Opzione+M</kbd> e selezionare Snippet (Frammento).
2. Dopo aver selezionato Snippet (Frammento) verrà richiesto di selezionare Full Search (Ricerca completa), Scoped Search (Ricerca con ambito) o Cross-Repository Reference (Riferimento tra repository). Per eseguire la ricerca in locale, selezionare Full Search (Ricerca completa).
3. Immettere un termine di ricerca per trovare il file. Dopo aver trovato il file, selezionarlo.
4. Selezionare quindi un'opzione per determinare le righe di codice da includere nel frammento. Le opzioni disponibili sono: **ID**, **Range** (Intervallo) e **None** (Nessuna).
5. In base alla selezione effettuata nel passaggio 4, fornire un valore se necessario.

Visualizzare l'intero file di codice:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Visualizzare una parte di un file di codice specificando i numeri di riga:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Visualizzare una parte di un file di codice specificando un nome di frammento:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Le sezioni seguenti spiegano questi esempi:

* [Usare un percorso relativo al file di codice](#path-to-code-file)
* [Includere solo i numeri di riga selezionati](#selected-line-numbers)
* [Fare riferimento a un frammento di codice denominato](#named-snippet)
* [Evidenziare righe selezionate](#highlighting-selected-lines)

Per altre informazioni, vedere la sezione [Informazioni di riferimento per la sintassi per i frammenti di codice](#snippet-syntax-reference) più avanti in questo articolo.

### <a name="path-to-code-file"></a>Percorso del file di codice

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

L'esempio è tratto dal repository docs ASP.NET, file dell'articolo [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Si fa riferimento al file di codice tramite un percorso relativo a [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) nello stesso repository.

### <a name="selected-line-numbers"></a>Numeri di riga selezionati

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Questo esempio mostra solo le righe 2-24 e 26 del file di codice *StudentController.cs*.

Preferire frammenti di codice denominati piuttosto che numeri di riga hardcoded, come spiegato nella sezione successiva.

### <a name="named-snippet"></a>Frammento di codice denominato

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Usare solo lettere e caratteri di sottolineatura per il nome.

L'esempio mostra la sezione `snippet_Create` del file di codice. Il file di codice per questo esempio contiene tag snippet nei commenti in codice C#:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Quando possibile, fare riferimento a una sezione denominata piuttosto che specificare numeri di riga. I riferimenti ai numeri di riga sono precari perché i file di codice inevitabilmente cambiano in modi che comportano anche la modifica dei numeri di riga.
Non si riceve necessariamente notifica di queste modifiche e nell'articolo iniziano a essere visualizzate le righe sbagliate senza alcuna indicazione di cosa è cambiato.

### <a name="highlighting-selected-lines"></a>Evidenziazione delle righe selezionate

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

Nell'esempio vengono evidenziate le righe 2 e 5, a partire dall'inizio del frammento visualizzato. I numeri di riga da evidenziare non vengono conteggiati dall'inizio del file di codice. In altre parole, vengono evidenziate le righe 3 e 6 del file di codice.

## <a name="out-of-repo-snippet-references"></a>Riferimenti a frammenti di codice al di fuori del repository

Se il file di codice a cui si vuole fare riferimento si trova in un altro repository, impostare il repository del codice come *repository dipendente*. In questo caso è necessario specificare un nome per il repository. Tale nome funge quindi da nome di cartella ai fini dei riferimenti al codice.

Ad esempio, il repository docs è *Azure/azure-docs* e il repository del codice è *Azure/azure-functions-durable-extension*.

Nella cartella radice di *azure-docs* aggiungere la sezione seguente in *.openpublishing.publish.config.json*:

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

In questo modo, quando si fa riferimento a *samples-durable-functions* come se fosse una cartella in *azure-docs*, in realtà si fa riferimento alla cartella radice nel repository *azure-functions-durable-extension*.

È possibile includere frammenti di codice anche applicando il formato dei triplici due punti (:\:\:) manualmente o in Visual Studio Code con il supporto di [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. In Visual Studio Code fare clic su <kbd>ALT+M</kbd> o <kbd>Opzione+M</kbd> e selezionare Snippet (Frammento).
2. Dopo aver selezionato Snippet (Frammento) verrà richiesto di selezionare Full Search (Ricerca completa), Scoped Search (Ricerca con ambito) o Cross-Repository Reference (Riferimento tra repository). Per eseguire la ricerca tra repository, selezionare Cross-Repository Reference (Riferimento tra repository).
3. Verrà fornita una selezione di repository disponibili in *.openpublishing.publish.config.json*. Selezionare un repository.
4. Immettere un termine di ricerca per trovare il file. Dopo aver trovato il file, selezionarlo.
5. Selezionare quindi un'opzione per determinare le righe di codice da includere nel frammento. Le opzioni disponibili sono: **ID**, **Range** (Intervallo) e **None** (Nessuna).
6. In base alla selezione effettuata nel passaggio 5, specificare un valore.

Il riferimento al frammento di codice sarà simile al seguente:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

Nel repository *azure-functions-durable-extension*, tale file di codice è disponibile nella cartella *samples/csx/shared*. Come specificato [in precedenza](#highlighting-selected-lines), i numeri di riga per l'evidenziazione fanno riferimento all'inizio del frammento e non all'inizio del file.

> [!NOTE]
> Il nome assegnato al repository dipendente fa riferimento alla radice del repository principale, mentre la tilde (~) si riferisce alla radice del docset. La radice del docset è definita da `build_source_folder` in *.openpublishing.publish.config.json*. Il percorso del frammento riportato nell'esempio precedente funziona nel repository azure-docs perché `build_source_folder` fa riferimento alla radice del repository (`.`). Se `build_source_folder` fosse `articles`, il percorso inizierebbe con `~/../samples-durable-functions` anziché con `~/samples-durable-functions`.

## <a name="interactive-code-snippets"></a>Frammenti di codice interattivi

### <a name="inline-interactive-code-blocks"></a>Blocchi di codice interattivi inline

Per i linguaggi seguenti, è possibile impostare i frammenti di codice come eseguibili nella finestra del browser:

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Quando è abilitata la modalità interattiva, i riquadri del codice dopo il rendering includono un pulsante **Prova** o **Esegui**. Ad esempio:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

Il rendering è il seguente:

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Per attivare questa funzionalità per un blocco di codice specifico, usare un identificatore di linguaggio speciale. Le opzioni disponibili sono:

* `azurepowershell-interactive` - Abilita Azure PowerShell Cloud Shell, come nell'esempio precedente
* `azurecli-interactive` - Abilita Azure Cloud Shell
* `csharp-interactive` - Abilita REPL C#

Per Azure Cloud Shell e PowerShell Cloud Shell, gli utenti possono eseguire i comandi solo con l'account personale di Azure.

### <a name="code-snippets-included-by-reference"></a>Frammenti di codice inclusi per riferimento

È possibile abilitare la modalità interattiva per i frammenti di codice inclusi per riferimento. Ecco alcuni esempi:

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Per attivare questa funzionalità per un blocco di codice specifico, usare l'attributo `interactive`. I valori disponibili per l'attributo sono:

* `cloudshell-powershell` - Abilita Azure PowerShell Cloud Shell, come nell'esempio precedente
* `cloudshell-bash` - Abilita Azure Cloud Shell
* `try-dotnet` -Abilita Try .NET
* `try-dotnet-class` -Abilita Try .NET con scaffolding delle classi
* `try-dotnet-method` -Abilita Try .NET con scaffolding dei metodi

Per Azure Cloud Shell e PowerShell Cloud Shell, gli utenti possono eseguire i comandi solo con l'account personale di Azure.

## <a name="snippet-syntax-reference"></a>Informazioni di riferimento per la sintassi per i frammenti di codice

Sintassi:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Questa sintassi è un'estensione Markdown di blocco e deve essere usata su una riga a sé stante.

* `<language>` (*facoltativo*)
  * Linguaggio del frammento di codice. Per altre informazioni, vedere la sezione [Linguaggi supportati](#supported-languages) più avanti in questo articolo.

* `<path>` (*obbligatorio*)
  * Percorso relativo nel file system che indica il file del frammento di codice a cui fare riferimento.

* `<attribute>` e `<attribute-value>` (*facoltativo*)
  * Usati insieme per specificare come il codice deve essere recuperato dal file e come deve essere visualizzato:
    * `range`: `1,3-5` Intervallo di righe. Questo esempio include le righe 1, 3, 4 e 5.
    * `id`: `snippet_Create` ID del frammento che deve essere inserito dal file di codice. Questo valore non può coesistere con un intervallo.
    * `highlight`: `2-4,6` Intervallo e/o numero di righe che devono essere evidenziate nel frammento di codice generato. La numerazione è relativa alle righe visualizzate (in base a quanto specificato dall'intervallo o dall'ID) e non al file.
    * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class``try-dotnet-method` Valore stringa che determina quali tipi di interattività sono abilitati.
    * Per altri dettagli sulla rappresentazione dei nomi di tag nei file di origine dei frammenti di codice in base al linguaggio, vedere le [linee guida per DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

## <a name="supported-languages"></a>Linguaggi supportati

[Docs Authoring Pack](how-to-write-docs-auth-pack.md) include una funzionalità che esegue il completamento delle istruzioni e la convalida degli identificatori di lingua disponibili per i blocchi di delimitazione del codice.

### <a name="fenced-code-blocks"></a>Blocchi di codice delimitati

| Nome                           | Alias validi                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| Interfaccia della riga di comando di .NET Core                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Log di accesso                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| Assembler ARM                  | `armasm`, `arm`                                                                |
| Assembler AVR                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Interfaccia della riga di comando di Azure                      | `azurecli`                                                                     |
| Interfaccia della riga di comando di Azure (interattiva)        | `azurecli-interactive`                                                         |
| Azure PowerShell               | `azurepowershell`                                                              |
| Azure PowerShell (interattivo) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (interattivo)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Script oggetto cache            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| File di zona DNS                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (Device Tree)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| MOF (Managed Object Format)          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (interattivo)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective-C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| PlainText (senza evidenziazione)         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL e PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (interattivo)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Proprietà                     | `properties`                                                                   |
| Protocol Buffers               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python Profiler (risultati)        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM (file specifiche)                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Shell                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Testo strutturato                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> La [funzionalità di completamento dei linguaggi di sviluppo](docs-authoring/dev-lang-completion.md) di Docs Authoring Pack usa il primo alias valido nel caso in cui siano disponibili più alias.

## <a name="next-steps"></a>Passaggi successivi

Per informazioni sulla formattazione del testo in caso di tipi di contenuto diversi dal codice, vedere [Linee guida per la formattazione del testo](text-formatting-guidelines.md).
