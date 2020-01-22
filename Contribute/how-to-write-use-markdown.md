---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111057"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Come usare Markdown per scrivere articoli di Docs

Gli articoli di [docs.microsoft.com](https://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere. Per questo motivo si sta imponendo rapidamente come standard del settore. Il sito docs usa la [versione Markdig](#markdown-flavor) di Markdown.


## <a name="markdown-basics"></a>Nozioni di base su Markdown

### <a name="headings"></a>Titoli

Per creare un titolo, usare il segno di cancelletto (#), come segue:

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Le intestazioni devono essere in stile atx. Devono quindi iniziare con un numero di caratteri cancelletto (#) compreso tra 1 e 6, corrispondente in HTML ai livelli di intestazione da H1 a H6. Quelli riportati qui sopra sono esempi di intestazioni di livello da 1 a 4.

Nell'argomento **deve** essere presente una sola intestazione di primo livello (H1), che verrà visualizzata come titolo sulla pagina.

Se l'intestazione termina con un carattere `#`, perché il rendering sia corretto è necessario aggiungere un altro carattere `#` alla fine, come ad esempio in `# Async Programming in F# #`.

Le intestazioni di secondo livello generano il sommario della sezione "In questo articolo", immediatamente dopo il titolo sulla pagina.

### <a name="bold-and-italic-text"></a>Testo in grassetto e corsivo

Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:

```md
This text is **bold**.
```

Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:

```md
This text is *italic*.
```

Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Citazioni

Per creare citazioni, si usa il carattere `>`:

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Ecco il rendering dell'esempio precedente:

> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.

### <a name="lists"></a>Elenchi

#### <a name="unordered-list"></a>Elenco non ordinato

Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini. Il testo Markdown seguente, ad esempio:

```md
- List item 1
- List item 2
- List item 3
```

verrà rappresentato nel modo seguente:

- List item 1
- List item 2
- List item 3

Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio. Il testo Markdown seguente, ad esempio:

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

verrà rappresentato nel modo seguente:

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>Elenco ordinato

Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti. Il testo Markdown seguente, ad esempio:

```md
1. First instruction
1. Second instruction
1. Third instruction
```

verrà rappresentato nel modo seguente:

1. First instruction
2. Second instruction
3. Third instruction

Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio. Il testo Markdown seguente, ad esempio:

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

verrà rappresentato nel modo seguente:

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

Si noti che si usa '1.' per tutte le voci. Ciò semplifica l'esame delle differenze in occasione di aggiornamenti successivi, quando vengono aggiunti nuovi passaggi o vengono rimossi passaggi esistenti.

### <a name="tables"></a>Tabelle

Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM. È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-). I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna. Includere una riga vuota prima della tabella per assicurarne il rendering corretto.

Il testo Markdown seguente, ad esempio:

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

verrà rappresentato nel modo seguente:

| Fun                  | With                 | Tabelle          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Per altre informazioni sulla creazione di tabelle, vedere:

- [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub.
- L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).
- [Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard).
- [Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin).
- [Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/).

### <a name="links"></a>Collegamenti

La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:

 `[link text](file-name.md)`

Per altre informazioni sui collegamenti, vedere:

- La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.
- La pagina [Collegamenti](how-to-write-links.md) in questa guida per dettagli sulla sintassi aggiuntiva per i collegamenti disponibile con Markdig.

### <a name="code-snippets"></a>Frammenti di codice

Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi. Per informazioni dettagliate, vedere:

- [Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)
- [GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)

I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice. Il formato generare per i blocchi di codice delimitati è:

    ```alias
    ...
    your code goes in here
    ...
    ```

L'alias dopo i tre apici inversi iniziali (\`) definisce l'evidenziazione della sintassi da usare. L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:

Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.

|Nome|Etichetta Markdown|
|-----|-------|
|Console .NET|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Interfaccia della riga di comando di Azure|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# nel browser|csharp-interactive|
|Console|console|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Linguaggio di query Kusto|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps (separatore decimale punto)|powerapps-dot|
|PowerApps (separatore decimale virgola)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

Il nome `csharp-interactive` specifica il linguaggio C# e la capacità di eseguire gli esempi dal browser. Questi frammenti di codice vengono compilati ed eseguiti in un contenitore Docker e i risultati dell'esecuzione del programma vengono visualizzati nella finestra del browser dell'utente.

#### <a name="example-c"></a>Esempio: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Rendering__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Esempio: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Rendering__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a>Estensioni Markdown personalizzate di Docs

> [!NOTE]
> Docs.Microsoft.com (Docs) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM). Markdig aggiunge altre funzionalità tramite le estensioni per Markdown. Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento (vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).

Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via. Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:

- Blocchi per le note
- File di inclusione
- Selettori
- Video incorporati
- Frammenti di codice/esempi

Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.

### <a name="note-blocks"></a>Blocchi per le note

Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:

- NOTE
- WARNING
- TIP
- IMPORTANT

In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi. Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.

Esempi:

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

L'aspetto degli avvisi in docs.microsoft.com è il seguente:

![mostra l'aspetto degli avvisi dell'esempio precedente nella pagina di Docs pubblicata con icone e colori diversi](media/alerts-rendering.png)

### <a name="include-files"></a>File di inclusione

In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig. Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato. Sono disponibili tre tipi di riferimenti di inclusione per agevolare il riutilizzo del contenuto:

- Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.
- Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.
- Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.

Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (MD), che possono contenere qualsiasi codice Markdown valido. Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository. Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.

Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:

- Usare un file di inclusione ogni volta che è necessario visualizzare lo stesso testo in più articoli.
- Usare un riferimento di inclusione di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa. Non usarle per includere testi più piccoli di una frase.
- I riferimenti di inclusione non vengono visualizzati nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig. Saranno visualizzate solo dopo la pubblicazione.
- Verificare che tutto il testo in un file di inclusione sia scritto con frasi complete o che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento al file di inclusione. Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.
- Non incorporare riferimenti di inclusione in altri file di inclusione. Ciò non è supportato.
- Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali. La directory media non deve includere immagini alla radice. Se il file di inclusione non contiene immagini, non è necessaria una directory corrispondente per i file multimediali.
- Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione. Usare un file separato con un nome univoco per ogni file di inclusione e articolo. Archiviare il file multimediale nella cartella dei file multimediali associata al file di inclusione.
- Non usare un file di inclusione come unico contenuto di un articolo.  I file di inclusione sono pensati come supplemento al contenuto nel resto dell'articolo.

Esempio:

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Selettori

Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee. Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili. In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.

Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un file di inclusione. A questo punto è possibile fare riferimento a quel file di inclusione in tutti gli articoli che usano lo stesso selettore.

Di seguito viene illustrato un esempio di selettore:

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

Per un esempio di selettori attivi, vedere la [documentazione di Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).

### <a name="code-include-references"></a>Riferimenti di inclusione di codice

L'estensione Markdown per i frammenti di codice Docs consente di incorporare esempi di codice negli articoli e di eseguirne il rendering con colorazione della sintassi specifica del linguaggio. È possibile includere codice dal repository corrente o da un altro repository. Nelle istruzioni riportate di seguito viene fornita una panoramica di come usare la funzionalità con [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack). In Visual Studio Code è possibile visualizzare l'anteprima dei frammenti di codice aprendo **Anteprima**. L'evidenziazione e l'interattività non sono disponibili nell'anteprima.

> [!NOTE]
> L'estensione non supporta l'inclusione del contenuto del codice inline. Questa operazione deve essere eseguita tramite la convenzione Markdown standard con triplo apice.

#### <a name="code-from-current-repository"></a>Codice dal repository corrente

1. In Visual Studio Code fare clic su **ALT+M** o **Opzione+M** e selezionare Snippet (Frammento).
2. Dopo aver selezionato Snippet (Frammento) verrà richiesto di selezionare Full Search (Ricerca completa), Scoped Search (Ricerca con ambito) o Cross-Repository Reference (Riferimento tra repository). Per eseguire la ricerca in locale, selezionare Full Local Search (Ricerca locale completa).
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

Visualizzare una parte di un file di codice in base a un nome di frammento:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>Codice da un altro repository

1. In Visual Studio Code fare clic su **ALT+M** o **Opzione+M** e selezionare Snippet (Frammento).
2. Dopo aver selezionato Snippet (Frammento) verrà richiesto di selezionare Full Search (Ricerca completa), Scoped Search (Ricerca con ambito) o Cross-Repository Reference (Riferimento tra repository). Per eseguire la ricerca tra repository, selezionare Cross-Repository Reference (Riferimento tra repository).
3. Verrà fornita una selezione di repository disponibili in *.openpublishing.publish.config.json*. Selezionare un repository.
3. Immettere un termine di ricerca per trovare il file. Dopo aver trovato il file, selezionarlo.
4. Selezionare quindi un'opzione per determinare le righe di codice da includere nel frammento. Le opzioni disponibili sono: **ID**, **Range** (Intervallo) e **None** (Nessuna).
5. In base alla selezione effettuata nel passaggio 5, fornire un valore se necessario.

Il riferimento al frammento di codice sarà simile al seguente:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>Percorso del file di codice

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

L'esempio è tratto dal repository docs ASP.NET, file dell'articolo [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Si fa riferimento al file di codice tramite un percorso relativo a [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) nello stesso repository.

#### <a name="selected-line-numbers"></a>Numeri di riga selezionati

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Questo esempio mostra solo le righe 2-24 e 26 del file di codice *StudentController.cs*.

Preferire i riferimenti a frammenti di codice piuttosto che a numeri di riga hardcoded, come spiegato nella sezione successiva.

#### <a name="named-snippet"></a>Frammento di codice denominato

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Usare solo lettere e caratteri di sottolineatura per il nome.

L'esempio mostra la sezione `snippet_Create` del file di codice. Il file di codice per questo esempio include un'area C# denominata `snippet_Create`:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Quando possibile, fare riferimento a una sezione denominata piuttosto che specificare numeri di riga. I riferimenti ai numeri di riga sono precari perché i file di codice inevitabilmente cambiano in modi che comportano anche la modifica dei numeri di riga.
Non si riceve necessariamente notifica di queste modifiche e nell'articolo iniziano a essere visualizzate le righe sbagliate senza alcuna indicazione di cosa è cambiato.

#### <a name="highlighting-selected-lines"></a>Evidenziazione delle righe selezionate

Esempio:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

Nell'esempio vengono evidenziate le righe 2 e 5, a partire dall'inizio del frammento visualizzato. (I numeri di riga da evidenziare non vengono conteggiati dall'inizio del file di codice.) In altre parole, vengono evidenziate le righe 3 e 6 del file di codice.

#### <a name="interactive-code-snippets"></a>Frammenti di codice interattivi

È possibile abilitare la modalità interattiva per i frammenti di codice inclusi per riferimento. Ecco alcuni esempi:

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

Per attivare questa funzionalità per un blocco di codice specifico, usare l'attributo `interactive`. I valori disponibili per l'attributo sono:

- `cloudshell-powershell` - Abilita Azure PowerShell Cloud Shell, come nell'esempio precedente
- `cloudshell-bash` - Abilita Azure Cloud Shell
- `try-dotnet` -Abilita Try .NET
- `try-dotnet-class` -Abilita Try .NET con scaffolding delle classi
- `try-dotnet-method` -Abilita Try .NET con scaffolding dei metodi

Sono disponibili coppie di `language` e `interactive` compatibili. Ad esempio, se `interactive` è `try-dotnet`, il linguaggio deve essere `csharp`. Analogamente, `cloudshell-powershell` funzionerebbe solo con `powershell` e `cloudshell-bash` funzionerebbe solo con `bash` come linguaggio.

Per Azure Cloud Shell e PowerShell Cloud Shell, gli utenti possono eseguire i comandi solo con l'account personale di Azure.

[Try .NET](https://github.com/dotnet/try) consente l'esecuzione interattiva di codice .NET (C#) nel browser. Per Try .NET sono disponibili tre opzioni per l'interattività: `try-dotnet`, `try-dotnet-class` e `try-dotnet-method`. L'uso di queste opzioni non richiede alcuna configurazione aggiuntiva all'interno del frammento di codice. Gli spazi dei nomi attualmente disponibili per impostazione predefinita sono:

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

Il valore dell'attributo `try-dotnet` consente agli utenti di eseguire codice C# nel browser senza che sia necessario eseguirne il wrapping in codice personalizzato.

Esempio:

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

Il valore `try-dotnet-class` applica lo scaffolding a livello di classi al codice passato al componente interattivo.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

Esempio:

Frammento di codice senza scaffolding delle classi applicato

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

Frammento di codice con scaffolding delle classi applicato

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

Il valore `try-dotnet-method` applica lo scaffolding a livello di metodi al codice passato al componente interattivo.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

Esempio:

Frammento di codice senza scaffolding dei metodi applicato

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

Frammento di codice con scaffolding dei metodi applicato

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>Informazioni di riferimento per la sintassi per i frammenti di codice

Per fare riferimento ai frammenti di codice archiviati nel repository, usare il linguaggio del codice specificato. Il contenuto del percorso di codice specificato verrà espanso e incluso nel file.

Non esistono restrizioni per la struttura delle cartelle dei frammenti di codice. È possibile gestire i frammenti di codice come se fossero codice sorgente normale.

Sintassi:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Questa sintassi è un'estensione Markdown di blocco e deve essere usata su una riga a sé stante.

- `<language>` (*facoltativo*)
  - Linguaggio del frammento di codice. Per altre informazioni, vedere la sezione [Linguaggi supportati](#supported-languages) più avanti in questo articolo.

- `<path>` (*obbligatorio*)
  - Percorso relativo nel file system che indica il file del frammento di codice a cui fare riferimento.

- `<attribute>` e `<attribute-value>` (*facoltativo*)
  - Usati insieme per specificare come il codice deve essere recuperato dal file:
    - `range`: `1,3-5` Intervallo di righe. Questo esempio include le righe 1, 3, 4 e 5.
    - `id`: `snippet_Create` ID del frammento che deve essere inserito dal file di codice. Questo valore non può coesistere con un intervallo.
    - `highlight`: `2-4,6` Intervallo e/o numero di righe che devono essere evidenziate nel frammento di codice generato. La numerazione è relativa al frammento di codice, non all'intervallo importato.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class``try-dotnet-method` Valore stringa che determina quali tipi di interattività sono abilitati.

#### <a name="supported-languages"></a>Linguaggi supportati

|Nome|Etichetta Markdown|
|-----|-------|
|Interfaccia della riga di comando di .NET Core|`dotnetcli`|
|ASP.NET con C#|`aspx-csharp`|
|ASP.NET con VB|`aspx-vb`|
|Interfaccia della riga di comando di Azure|`azurecli`|
|Interfaccia della riga di comando di Azure nel browser|`azurecli-interactive`|
|Azure PowerShell nel browser|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|C# nel browser|`csharp-interactive`|
|Console|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Linguaggio di query Kusto|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|Power Query M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>Estensioni del codice

|Nome|Etichetta Markdown|Estensione del file|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xaml|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>Problemi e risoluzione

### <a name="alt-text"></a>Testo alternativo

Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente. Ad esempio, invece di questa formattazione:

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrofi e virgolette

Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve, che devono essere codificati o modificati in semplici apostrofi o virgolette. In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s

Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:

- Virgolette (aperte) a sinistra: `&#8220;`
- Virgolette (chiuse) a destra: `&#8221;`
- Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`
- Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`

### <a name="angle-brackets"></a>Parentesi acute

Le parentesi acute vengono comunemente usate per indicare un segnaposto. Se usate nel testo e non nel codice, le parentesi acute devono essere codificate. In caso contrario, Markdown le interpreta come tag HTML.

Ad esempio, codificare `<script name>` come `&lt;script name&gt;`

## <a name="markdown-flavor"></a>Versione di Markdown

Il back-end del sito docs.microsoft.com supporta il Markdown conforme a [CommonMark](https://commonmark.org/) analizzato tramite il motore di analisi [Markdig](https://github.com/lunet-io/markdig). Questa versione di Markdown è per lo più compatibile con [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), perché la maggior parte dei documenti viene archiviata in GitHub dove può essere modificata. Altre funzionalità vengono aggiunte tramite le estensioni per Markdown.

## <a name="see-also"></a>Vedere anche:

### <a name="markdown-resources"></a>Risorse per Markdown

- [Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)
- [Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)
- [Nozioni di base su Markdown in GitHub](https://help.github.com/articles/markdown-basics/)
- [Guida Markdown](https://www.markdownguide.org/)
