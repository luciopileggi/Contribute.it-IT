---
title: Informazioni di riferimento su Markdown per docs.microsoft.com
description: Informazioni sulle funzionalità e sulla sintassi Markdown usate nella piattaforma Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 452cbf97db748532ae2b0e09b4bb558c8f757a61
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188265"
---
# <a name="markdown-reference"></a>Informazioni di riferimento a Markdown

Markdown è un semplice linguaggio di markup che usa una sintassi di formattazione in testo normale. La piattaforma Docs supporta lo standard CommonMark per Markdown e alcune estensioni Markdown personalizzate progettate per offrire contenuti formattati in docs.microsoft.com. In questo articolo vengono elencati in ordine alfabetico gli elementi necessari per usare Markdown per docs.microsoft.com.

Per creare codice Markdown è possibile usare un qualsiasi editor di testo. Per un editore che consenta di inserire sia una sintassi Markdown standard sia estensioni Docs personalizzate, è consigliabile usare [VS Code](https://code.visualstudio.com/) con [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installato.

Docs usa il motore Markdig per Markdown. In [https://babelmark.github.io/](https://babelmark.github.io/) è possibile testare il rendering di Markdown in Markdig e in altri motori.

## <a name="alerts-note-tip-important-caution-warning"></a>Avvisi (nota, suggerimento, informazione importante, attenzione e avviso)

Gli avvisi sono un'estensione di Markdown per Docs che consente di creare citazioni per eseguire il rendering in docs.microsoft.com usando colori e icone che indicano il significato del contenuto. Sono supportati i tipi di avviso seguenti:

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

## <a name="code-snippets"></a>Frammenti di codice

Nei file Markdown è possibile incorporare frammenti di codice:

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Titoli

Docs supporta sei livelli di intestazioni Markdown:

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Deve essere presente uno spazio tra l'ultimo `#` e il testo del titolo.
- Ogni file Markdown deve avere esclusivamente un elemento H1.
- L'elemento H1 deve essere il primo contenuto nel file dopo il blocco di metadati YML.
- Gli elementi H2 vengono visualizzati automaticamente nel menu di spostamento a destra del file pubblicato. Non esistono titoli di livello inferiore. Usare gli H2 in modo strategico per consentire agli utenti di navigare il contenuto.
- I titoli HTML, ad esempio `<h1>`, non sono consigliati e in alcuni casi generano avvisi di compilazione.
- È possibile creare un collegamento a singoli titoli in un file usando i [segnalibri](#bookmark-links).

## <a name="html"></a>HTML

Benché Markdown supporti HTML inline, non è consigliabile usare il linguaggio HTML per la pubblicazione in Docs poiché, fatta eccezione per un piccolo gruppo di valori, genera avvisi o errori di compilazione.

## <a name="images"></a>Immagini

La sintassi per l'inclusione di un'immagine è la seguente:

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Dove `alt text` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine. Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo. È anche utile se in presenza di un bug nel sito non è possibile eseguire il rendering dell'immagine.

Le immagini devono essere archiviate in una cartella `/media` all'interno del docset. Per impostazione predefinita, per le immagini sono supportati i tipi di file seguenti:

- .jpg
- .png

È possibile supportare altri tipi di immagine aggiungendoli come risorse al file docfx.json<!--add link to reference when available--> nel docset.

## <a name="links"></a>Collegamenti

Nella maggior parte dei casi Docs usa collegamenti Markdown standard per collegarsi ad altri file e pagine. I tipi di collegamenti vengono descritti nelle sottosezioni seguenti.

> [!TIP]
> Docs Authoring Pack per VS Code consente di inserire collegamenti relativi e segnalibri in modo corretto senza dover conoscere i percorsi.

> [!IMPORTANT]
> Nei collegamenti ai siti Microsoft non includere codici delle impostazioni locali, ad esempio it-it. I codici delle impostazioni locali hardcoded impediscono il rendering del contenuto localizzato. Si assiste così a una pessima esperienza utente in altre impostazioni locali e a un aumento significativo dei costi i localizzazione. Quando si copia un URL da un browser, il codice delle impostazioni locali viene incluso per impostazione predefinita. È quindi necessario eliminarlo manualmente quando si crea il collegamento. Ad esempio, usare:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Non usare:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Collegamenti relativi a file all'interno dello stesso docset

Un percorso relativo è il percorso al file di destinazione relativo al file corrente. In Docs è possibile usare un percorso relativo per il collegamento a un altro file all'interno dello stesso docset. La sintassi di un percorso relativo è la seguente:

```md
[link text](../../folder/filename.md)
```

Dove `../` indica un livello superiore nella gerarchia.

- Il percorso relativo verrà risolto durante la compilazione e verrà anche rimossa l'estensione md.
- È possibile usare "../" per il collegamento a un file nella cartella padre, ma il file deve appartenere allo stesso docset. Non è possibile usare "../" per il collegamento a un file in un'altra cartella del docset.
- Docs supporta anche un formato speciale di percorso relativo che inizia con "~" (ad esempio, ~/foo/bar.md). Questa sintassi indica un file relativo alla cartella radice di un docset. Anche questo tipo di percorso viene convalidato e risolto durante la compilazione.

> [!IMPORTANT]
> Includere l'estensione del file nel percorso relativo. Durante la compilazione viene convalidata l'esistenza del file di destinazione di tale percorso relativo. Se il percorso relativo non include l'estensione file, la compilazione potrebbe segnalare un avviso di collegamento interrotto. Ad esempio, usare:
>
> `[link text](../../folder/filename.md)`
>
> Non usare:
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Collegamenti relativi di siti ad altri file in Docs

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Non includere l'estensione file md. In questo modo si crea il collegamento al file della panoramica Linux dall'esterno del doset "articles" di Azure.

### <a name="links-to-external-sites"></a>Collegamenti a siti esterni

```md
[Microsoft](https://www.microsoft.com)
```

Collegamento basato su URL a un'altra pagina Web. Deve includere https://.

### <a name="bookmark-links"></a>Collegamento segnalibro

Collegamento segnalibro a un titolo in un altro file all'interno dello stesso repository. Ad esempio:

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

Collegamento segnalibro a un titolo nel file corrente:

```md
[Managed Disks](#managed-disks)
```

Usare un segno hash `#` seguito dalle parole del titolo. Per cambiare il testo del titolo in testo del collegamento:
- Usare solo caratteri minuscoli
- Rimuovere la punteggiatura
- Sostituire gli spazi con trattini

Ad esempio, se il nome del titolo è "2.2 Preoccupazioni sulla sicurezza", il testo del collegamento segnalibro sarà "#22-Preoccupazioni-sulla-sicurezza".

### <a name="explicit-anchor-links"></a>Collegamenti di ancoraggio esplicito

I collegamenti di ancoraggio esplicito che usano il tag HTML `<a>`**non sono né necessari né consigliati** tranne in pagine hub e pagine di destinazione. Usare i segnalibri in file Markdown generali, come descritto in precedenza. In caso di pagine hub e pagine di destinazione, usare gli ancoraggi come descritto di seguito:

`## <a id="AnchorText"> </a>Header text` oppure `## <a name="AnchorText"> </a>Header text`

Per il collegamento ad ancoraggi espliciti, usare la sintassi seguente:

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Collegamenti XREF (riferimento incrociato)

Per il collegamento alle pagine di riferimento API generate automaticamente nel docset corrente o in altri docset, usare i collegamenti XREF con l'ID univoco (UID).

> [!NOTE]
> Per fare riferimento a pagine di riferimento API in altri docset, è necessario aggiungere la configurazione `xrefService` nel file `docfx.json`.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

L'UID corrisponde al nome completo di classe e membro. Se si aggiunge * dopo l'UID, il collegamento rappresenta la pagina di overload e non un'API specifica. Ad esempio, usare `List<T>.BinarySearch*` per il collegamento alla pagina BinarySearch Method anziché all'overload specifico, come `List<T>.BinarySearch(T, IComparer<T>)`.

È possibile usare una delle sintassi seguenti:

- Collegamento automatico: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  Il parametro di query `displayProperty` facoltativo genera un testo del collegamento completo. Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo.

- Collegamento Markdown: `[link text](xref:UID)`
  
  Può essere usato quando si vuole personalizzare il testo del collegamento visualizzato.

Esempi:

- `<xref:System.String>` viene visualizzato come "String".
- `<xref:System.String?displayProperty=nameWithType>` viene visualizzato come "System.String".
- `[String class](xref:System.String)` viene visualizzato come "String class".

Attualmente non è disponibile un sistema semplice per trovare gli UID. <!-- ? -->Il modo migliore per trovare l'UID per un'API consiste nel visualizzare l'origine per la pagina dell'API che si vuole collegare e individuare il valore ms.assetid. I singoli valori di overload non vengono visualizzati nell'origine. È in corso lo sviluppo di un sistema migliore, che sarà disponibile in futuro.

Quando l'UID contiene i caratteri speciali \`, \# o \*, il valore dell'UID deve essere con codifica HTML come `%60`, `%23` e `%2A` rispettivamente. A volte sono presenti parentesi con codifica, ma questo non è un requisito.

Esempi:

- System.Threading.Tasks.Task\`1 diventa `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor diventa `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) diventa `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Elenchi (numerati, puntati, di controllo)

### <a name="numbered-list"></a>Elenco numerato

Per creare un elenco numerato è possibile usare tutti 1, che dopo la pubblicazione vengono visualizzati come elenco sequenziale. Per migliorare la leggibilità dell'origine, è possibile incrementare gli elenchi.

Non usare le lettere negli elenchi, neppure negli elenchi annidati. Non vengono visualizzati correttamente quando vengono pubblicati in Docs. Gli elenchi annidati che usano i numeri vengono visualizzati con lettere minuscole quando vengono pubblicati. Ad esempio:

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Il rendering è il seguente:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>Elenco puntato

Per creare un elenco puntato, usare `-` seguito da uno spazio all'inizio di ogni linea:

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Il rendering è il seguente:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

### <a name="checklist"></a>Elenco di controllo

Gli elenchi di controllo possono essere usati solo in docs.microsoft.com tramite un'estensione Markdown personalizzata:

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Il rendering di esempio in docs.microsoft.com è il seguente:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Usare elenchi di controllo all'inizio o alla fine di un articolo per riepilogare ciò di cui si parlerà o di cui si è parlato nell'articolo. Non aggiungere elenchi di controllo casuali all'interno degli articoli.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Azione Passaggio successivo

È possibile usare un'estensione personalizzata per aggiungere solo alle pagine in docs.microsoft.com un pulsante di azione per il passaggio successivo.

La sintassi è la seguente:

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Ad esempio:

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Il rendering è il seguente:

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

Nell'azione per il passaggio successivo è possibile usare tutti i collegamenti supportati, incluso un collegamento Markdown a un'altra pagina Web. Nella maggior parte dei casi il collegamento all'azione successiva sarà un collegamento relativo a un altro file all'interno dello stesso docset.

## <a name="section-definition"></a>Definizione di sezione

<!-- more info about this would be helpful! -->
Potrebbe essere necessario definire una sezione. Questa sintassi è usata soprattutto nelle tabelle di codice.
Vedere l'esempio seguente:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Il rendering del testo Markdown della citazione precedente sarà il seguente:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Selettori

<!-- could be more clear! -->
È possibile usare un selettore per collegare pagine diverse dello stesso articolo e consentire ai lettori di passare da una pagina all'altra.

> [!NOTE]
> Questa estensione funziona in modo diverso in docs.microsoft.com e in MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Selettore singolo

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

... il rendering sarà il seguente:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Selezione multipla

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

... il rendering sarà il seguente:

> [!div class="op_multi_selector" title1="Piattaforma" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a>Tabelle

Il metodo più semplice per creare una tabella in Markdown consiste nell'uso di barre verticali e linee. Per creare una tabella standard con un titolo, la prima linea deve essere seguita da una linea tratteggiata:

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Il rendering è il seguente:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

È anche possibile creare una tabella senza un titolo. Ad esempio, per creare un elenco con più colonne:

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

Il rendering è il seguente:

|   |   |
| - | - |
| This | table |
| has no | header |

È possibile allineare le colonne usando i due punti:

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Il rendering è il seguente:

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> Docs Authoring Extension per VS Code semplifica l'aggiunta di tabelle Markdown di base.
>
> È anche possibile usare un [generatore di tabelle online](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Funziona solo nel sito docs.microsoft.com.

Se si crea una tabella in Markdown, la tabella potrebbe espandersi fino alla barra di spostamento destra e diventare illeggibile. È possibile risolvere l'inconveniente consentendo l'aggiunta di ritorni a capo alla tabella quando necessario durante il rendering dei documenti. È sufficiente impostare il ritorno a capo nella tabella con la classe personalizzata `[!div class="mx-tdBreakAll"]`.

Ecco un esempio di tabella Markdown con tre righe per le quali il ritorno a capo verrà gestito con `div` con il nome di classe `mx-tdBreakAll`.

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Verrà eseguito il rendering come segue:

> [!div class="mx-tdBreakAll"]
> |Nome|Sintassi|Obbligatorio per l'installazione invisibile all'utente?|Descrizione|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Sì|Esegue il programma di installazione senza visualizzare elementi dell'interfaccia utente o richieste di conferma.|
> |NoRestart|/norestart|No|Impedisce qualsiasi tentativo di riavvio. Per impostazione predefinita l'interfaccia utente richiede una conferma prima del riavvio.|
> |Help|/help|No|Rende disponibili la Guida e il Riferimento rapido. Visualizza l'uso corretto del comando di impostazione con un elenco di tutte le opzioni e i comportamenti.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Funziona solo nel sito docs.microsoft.com.

Occasionalmente potrebbero essere presenti parole molto lunghe nella seconda colonna di una tabella. Per assicurarsi che vengano divise correttamente, è possibile applicare la classe `mx-tdCol2BreakAll` usando la sintassi per il ritorno a capo `div`, come illustrato in precedenza.

### <a name="html-tables"></a>Tabelle HTML

Non è consigliabile usare tabelle HTML per docs.microsoft.com. Non sono leggibili nell'origine, un principio fondamentale di Markdown.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Video

### <a name="embedding-videos-into-a-markdown-page"></a>Incorporamento di video in una pagina Markdown

Attualmente Docs può supportare la pubblicazione di video in tre posizioni:

- YouTube
- Channel 9
- Sistema "OnePlayer" Microsoft

È possibile incorporare un video con la sintassi seguente e Docs ne eseguirà il rendering.

```md
> [!VIDEO <embedded_video_link>]
```

Esempio:

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... il rendering sarà il seguente:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

E verrà visualizzato nel modo seguente nelle pagine pubblicate:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> L'URL del video CH9 deve iniziare con `https` e terminare con `/player`. In caso contrario verrà incorporata l'intera pagina anziché solo il video.

### <a name="uploading-new-videos"></a>Caricamento di nuovi video

Per caricare nuovi video, è consigliabile attenersi al processo seguente:

1. Unirsi al gruppo **docs_video_users** in IDWEB.
1. Accedere a https://aka.ms/VideoUploadRequest e inserire i dettagli del video. Sono necessarie le informazioni seguenti. Si noti che nessuna di queste informazioni sarà visibile al pubblico:
    1. Un titolo per il video.
    1. Un elenco di prodotti/servizi ai quali il video è correlato.
    1. La pagina di destinazione oppure, se la pagine non è ancora disponibile, il docset che ospiterà il video.
    1. Un collegamento al file MP4 per il video. In assenza di un percorso in cui inserire il file, è possibile usare temporaneamente il percorso `\\scratch2\scratch\apex`. La risoluzione dei file MP4 deve essere 720p o superiore.
    1. Una descrizione del video.
1. Inviare (salvare) l'elemento.
1. Entro due giorni lavorativi, il video verrà caricato. Il collegamento necessario per incorporare il video sarà disponibile nell'elemento di lavoro e sarà risolto *dall'utente*.
1. Dopo aver recuperato il collegamento video, chiudere l'elemento di lavoro.
1. Il collegamento video può essere quindi aggiunto al post usando la sintassi seguente:

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
