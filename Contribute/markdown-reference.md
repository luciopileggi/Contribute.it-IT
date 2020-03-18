---
title: Informazioni di riferimento su Markdown per docs.microsoft.com
description: Informazioni sulle funzionalità e sulla sintassi Markdown usate nella piattaforma Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 14cc9f0912149eb342c97d0dd7d2776bd54c84e7
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331965"
---
# <a name="docs-markdown-reference"></a>Informazioni di riferimento su Docs Markdown

In questo articolo sono elencati in ordine alfabetico gli elementi necessari per scrivere codice Markdown per docs.microsoft.com (Docs).

[Markdown](https://daringfireball.net/projects/markdown/) è un linguaggio di tipo Lightweight Markup Language (LML) con sintassi di formattazione in testo normale. Docs supporta Markdown conforme a [CommonMark](https://commonmark.org/), analizzato tramite il motore di analisi [Markdig](https://github.com/lunet-io/markdig). Supporta inoltre estensioni di Markdown personalizzate che offrono una formattazione più avanzata dei contenuti sul sito Docs.

Per scrivere codice Markdown è possibile usare qualsiasi editor di testo, ma è consigliabile [Visual Studio Code](https://code.visualstudio.com/) con [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack). Docs Authoring Pack offre strumenti di modifica e una funzionalità di anteprima che consente di visualizzare l'aspetto che avranno gli articoli quando ne verrà eseguito il rendering in Docs.

## <a name="alerts-note-tip-important-caution-warning"></a>Avvisi (nota, suggerimento, informazione importante, attenzione e avviso)

Per gli avvisi è disponibile un'estensione di Markdown che consente di creare in docs.microsoft.com blocchi di testo in evidenza con colori e icone che indicano il significato del contenuto. Sono supportati i tipi di avviso seguenti:

```markdown
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

### <a name="angle-brackets"></a>Parentesi acute

Se nel testo di un file si usano parentesi acute, ad esempio per indicare un segnaposto, è necessario codificarle manualmente. In caso contrario, Markdown le interpreta come tag HTML.

Ad esempio, codificare `<script name>` come `&lt;script name&gt;` o `\<script name>`.

Le parentesi acute non devono essere precedute da caratteri di escape nel testo formattato come codice inline o nei blocchi di codice.

## <a name="apostrophes-and-quotation-marks"></a>Apostrofi e virgolette

Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve, che devono essere codificati o modificati in semplici apostrofi o virgolette. In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s

Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:

- Virgolette (aperte) a sinistra: `&#8220;`
- Virgolette (chiuse) a destra: `&#8221;`
- Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`
- Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`

## <a name="blockquotes"></a>Citazioni

Per creare citazioni, si usa il carattere `>`:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

Ecco il rendering dell'esempio precedente:

> This is a blockquote. It is usually rendered indented and with a different background color.

## <a name="bold-and-italic-text"></a>Testo in grassetto e corsivo

Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:

```markdown
This text is **bold**.
```

Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:

```markdown
This text is *italic*.
```

Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Frammenti di codice

Docs Markdown supporta il posizionamento di frammenti di codice sia inline in una frase sia come blocco separato "delimitato" tra due frasi. Per altre informazioni, vedere [Come includere codice in Docs](code-in-docs.md).

## <a name="columns"></a>Colonne

L'estensione di Markdown per le **colonne** consente agli autori di Docs di aggiungere layout di contenuto basati su colonna più flessibili e potenti rispetto alle tabelle Markdown di base, che sono adatte solo ai dati tabulari veri e propri. È possibile aggiungere al massimo quattro colonne e usare l'attributo `span` facoltativo per unire due o più colonne.

La sintassi per le colonne è la seguente:

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

Le colonne devono contenere solo codice Markdown di base, comprese le immagini. Non è consigliabile includere intestazioni, tabelle, tabulazioni e altre strutture complesse. Una riga non può includere contenuto all'esterno della colonna.

Il codice Markdown seguente, ad esempio, crea una colonna che si estende su due larghezze e una colonna standard (senza `span`):

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

Il rendering è il seguente:

:::row:::
   :::column span="2":::
      **Questa è una colonna che si estende su due larghezze con molto testo.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **Questa è una colonna a larghezza singola contenente un'immagine.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>Titoli

Docs supporta sei livelli di intestazioni Markdown:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Deve essere presente uno spazio tra l'ultimo `#` e il testo del titolo.
- Ogni file Markdown deve avere una sola intestazione H1.
- L'intestazione H1 deve essere il primo contenuto nel file dopo il blocco di metadati YML.
- Le intestazioni H2 vengono visualizzate automaticamente nel menu di spostamento a destra del file pubblicato. Non esistono titoli di livello inferiore. Usare quindi le intestazioni H2 in maniera mirata per facilitare la lettura del contenuto.
- Le intestazioni HTML, ad esempio `<h1>`, non sono consigliate e in alcuni casi generano avvisi di compilazione.
- È possibile creare un collegamento a singole intestazioni in un file usando i [collegamenti a segnalibro](how-to-write-links.md#links-to-anchors).

## <a name="html"></a>HTML

Benché Markdown supporti HTML inline, non è consigliabile usare il linguaggio HTML per la pubblicazione in Docs poiché, fatta eccezione per un piccolo gruppo di valori, genera avvisi o errori di compilazione. 

## <a name="images"></a>Immagini

Per impostazione predefinita, per le immagini sono supportati i tipi di file seguenti:

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>Immagini concettuali standard (Markdown predefinito)

La sintassi Markdown di base per incorporare un'immagine è la seguente:

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Dove `<alt text>` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine. Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo. È anche utile se, in presenza di un bug nel sito, non è possibile eseguire il rendering dell'immagine.

I caratteri di sottolineatura nel testo alternativo vengono sottoposti a rendering correttamente solo se sono preceduti da una barra rovesciata (`\_`). Evitare tuttavia di copiare i nomi di file per usarli come testo alternativo. Ad esempio, invece di scrivere questo:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Scrivere questo:

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Immagini concettuali standard (Docs Markdown)

L'estensione `:::image:::` personalizzata di Docs supporta immagini standard, immagini complesse e icone.

Per le immagini standard, la sintassi Markdown precedente continuerà a funzionare, ma è consigliabile usare la nuova estensione perché supporta funzionalità più potenti, ad esempio la possibilità di specificare un ambito di localizzazione diverso dall'argomento padre. Altre funzionalità avanzate, ad esempio la possibilità di selezionare un'immagine dalla raccolta di immagini condivise invece di specificarne una locale, saranno disponibili in futuro. La nuova sintassi è la seguente:

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

Se `type="content"` (impostazione predefinita), è necessario specificare sia `source` che `alt-text`.

### <a name="complex-images-with-long-descriptions"></a>Immagini complesse con lunghe descrizioni

È anche possibile usare questa estensione per aggiungere un'immagine con una lunga descrizione che viene letta dalle utilità per la lettura dello schermo, ma non viene visualizzata nella pagina pubblicata. Le descrizioni lunghe sono un requisito di accessibilità per immagini complesse, ad esempio i grafici. La sintassi è la seguente:

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

Se `type="complex"`, è necessario specificare `source`, `alt-text`, una lunga descrizione e il tag `:::image-end:::`.

### <a name="specifying-loc-scope"></a>Specifica dell'attributo loc-scope

A volte l'ambito di localizzazione di un'immagine è diverso da quello dell'articolo o del modulo che la contiene. Questo può avere effetti negativi sull'esperienza globale, ad esempio se uno screenshot di un prodotto viene accidentalmente localizzato in una lingua per cui il prodotto non è disponibile. Per evitare questo problema, è possibile specificare l'attributo facoltativo `loc-scope` nelle immagini di tipo `content` e `complex`.

### <a name="icons"></a>Icone

L'estensione per le immagini supporta le icone, che sono immagini decorative e non devono avere testo alternativo. La sintassi per le icone è la seguente:

```Markdown
:::image type="icon" source="<folderPath>":::
```

Se `type="icon"`, è necessario specificare solo `source`.

## <a name="included-markdown-files"></a>File Markdown inclusi

Se i file Markdown devono essere ripetuti in più articoli, è possibile usare un file di inclusione. La funzionalità delle inclusioni indica a Docs di sostituire il riferimento con il contenuto del file di inclusione in fase di compilazione. È possibile usare le inclusioni nei modi seguenti:

- Inline: riutilizzo di un frammento di testo comune inline all'interno di una frase.
- Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.

I file di inclusione di tipo Inline o Blocco sono file Markdown (con estensione md) che possono contenere qualsiasi codice Markdown valido. I file di inclusione si trovano in genere in una sottodirectory *includes* comune, nella radice del repository. Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.

### <a name="includes-syntax"></a>Sintassi delle inclusioni

L'inclusione di tipo Blocco si trova su una riga a sé stante:

```markdown
[!INCLUDE [<title>](<filepath>)]
```

L'inclusione di tipo Inline si trova all'interno di una riga:

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

Dove `<title>` è il nome del file e `<filepath>` è il percorso relativo del file. `INCLUDE` deve essere riportato in lettere maiuscole e prima di `<title>` deve essere presente uno spazio.

Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:

- Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa. Non usarle per includere testi più piccoli di una frase.
- Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano sulle estensioni di Docs. Saranno visualizzate solo dopo la pubblicazione.
- Verificare che tutto il testo in un file di inclusione sia scritto con espressioni o frasi complete che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione. Ignorare questa indicazione significa creare una stringa non traducibile nell'articolo.
- Non incorporare file di inclusione in altri file di inclusione.
- Posizionare i file multimediali in un'apposita cartella, specifica della sottodirectory delle inclusioni, ad esempio la cartella `<repo>` */includes/media*. La directory *media* non deve contenere immagini nella radice. Se l'inclusione non contiene immagini, non è necessario creare una cartella *media* corrispondente.
- Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione. Usare un file separato con un nome univoco per ogni inclusione e articolo. Archiviare il file multimediale nella cartella associata all'inclusione.
- Non usare un'inclusione come unico contenuto di un articolo.  Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.

## <a name="links"></a>Collegamenti

Per informazioni sulla sintassi per i collegamenti, vedere [Usare i collegamenti nella documentazione](how-to-write-links.md).

## <a name="lists-numbered-bulleted-checklist"></a>Elenchi (numerati, puntati, di controllo)

### <a name="numbered-list"></a>Elenco numerato

Per creare un elenco numerato, è possibile usare sempre il numero 1. Al momento della pubblicazione, il rendering dei numeri viene eseguito in ordine crescente, come elenco sequenziale. Per migliorare la leggibilità dell'origine, è possibile incrementare gli elenchi manualmente.

Non usare lettere negli elenchi, neppure in quelli annidati, poiché non vengono visualizzate correttamente al momento della pubblicazione in Docs. Gli elenchi annidati che usano i numeri vengono visualizzati con lettere minuscole quando vengono pubblicati. Ad esempio:

```markdown
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

Per creare un elenco puntato, usare `-` o `*` seguito da uno spazio all'inizio di ogni riga:

```markdown
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

Indipendentemente dalla sintassi scelta, `-` o `*`, usarla in modo coerente all'interno di un articolo.

### <a name="checklist"></a>Elenco di controllo

Gli elenchi di controllo possono essere usati solo in Docs tramite un'estensione di Markdown personalizzata:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Il rendering di questo esempio in Docs è il seguente:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Usare elenchi di controllo all'inizio o alla fine di un articolo per riepilogare ciò di cui si parlerà o di cui si è parlato nell'articolo. Non aggiungere elenchi di controllo casuali all'interno degli articoli.

## <a name="next-step-action"></a>Azione Passaggio successivo

È possibile usare un'estensione personalizzata per aggiungere un pulsante di azione Passaggio successivo nelle pagine di Docs.

La sintassi è la seguente:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Ad esempio:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Il rendering è il seguente:

> [!div class="nextstepaction"]
> [Informazioni sull'aggiunta di codice negli articoli](code-in-docs.md)

Nell'azione per il passaggio successivo è possibile usare tutti i collegamenti supportati, incluso un collegamento Markdown a un'altra pagina Web. Nella maggior parte dei casi, il collegamento all'azione successiva è un collegamento relativo a un altro file all'interno dello stesso docset.

## <a name="non-localized-strings"></a>Stringhe non localizzate

È possibile usare l'estensione di Markdown personalizzata `no-loc` per identificare le stringhe di contenuto che devono essere ignorate dal processo di localizzazione.

Per tutte le stringhe indicate viene fatta distinzione tra maiuscole e minuscole. In altre parole, la stringa deve corrispondere esattamente per essere ignorata per la localizzazione.

Per contrassegnare una singola stringa come non localizzabile, usare questa sintassi:

```markdown
:::no-loc text="String":::
```

Nel codice seguente, ad esempio, solo la singola istanza di `Document` verrà ignorata durante il processo di localizzazione:

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> Usare `\` per applicare una sequenza di escape ai caratteri speciali:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

È anche possibile usare i metadati nell'intestazione YAML per contrassegnare come non localizzabili tutte le istanze di una stringa all'interno del file Markdown corrente:

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> I metadati no-loc non sono supportati come metadati globali nel file *docfx.json*. La pipeline di localizzazione non legge il file *docfx.json* e quindi i metadati no-loc devono essere aggiunti in ogni singolo file di origine.

Nell'esempio seguente, sia nel campo dei metadati `title` sia nell'intestazione Markdown, la parola `Document` verrà ignorata durante il processo di localizzazione.

Nel campo dei metadati `description` e nel contenuto principale di Markdown, la parola `document` viene invece localizzata, perché non inizia con una lettera `D` maiuscola.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>Selettori

I selettori sono elementi dell'interfaccia utente che consentono all'utente di passare da una versione all'altra dello stesso articolo. Questi elementi vengono usati in alcuni set di documenti per illustrare le differenze di implementazione tra tecnologie o piattaforme. Un esempio tipico è il contenuto per sviluppatori relativo a più piattaforme per dispositivi mobili.

Poiché lo stesso selettore Markdown viene aggiunto in ogni file di articolo che prevede l'uso del selettore, è consigliabile inserirlo in un file di inclusione. Sarà quindi possibile fare riferimento al file di inclusione in tutti i file di articolo che usano lo stesso selettore.

Esistono due tipi di selettori: un selettore singolo e un selettore multiplo.

### <a name="single-selector"></a>Selettore singolo

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

... il rendering sarà il seguente:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Selezione multipla

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

... il rendering sarà il seguente:

> [!div class="op_multi_selector" title1="Piattaforma" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows Universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>Apice e pedice

È consigliabile usare il formato apice e pedice quando è necessario per assicurare l'accuratezza tecnica, ad esempio quando si scrivono le formule matematiche. Non usarlo per gli stili non standard, come le note a piè di pagina.

Per il formato apice e pedice, usare il codice HTML:

```html
Hello <sub>This is subscript!</sub>
```

Il rendering è il seguente:

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Il rendering è il seguente:

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Tabelle

Il metodo più semplice per creare una tabella in Markdown consiste nell'uso di barre verticali e linee. Per creare una tabella standard con un titolo, la prima linea deve essere seguita da una linea tratteggiata:

```markdown
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

È possibile allineare le colonne usando i due punti:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Il rendering è il seguente:

| Fun                  | With                 | Tabelle          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> Docs Authoring Extension per VS Code semplifica l'aggiunta di tabelle Markdown di base.
>
> È anche possibile usare un [generatore di tabelle online](http://www.tablesgenerator.com/markdown_tables).

### <a name="line-breaks-within-words-in-any-table-cell"></a>Interruzioni di riga all'interno di parole in qualsiasi cella di tabella

Se si usano parole lunghe in una tabella Markdown, la tabella potrebbe espandersi fino alla barra di spostamento destra e diventare illeggibile. È possibile risolvere questo problema consentendo al rendering di Docs di inserire automaticamente interruzioni di riga all'interno di parole, quando necessario. È sufficiente impostare il ritorno a capo nella tabella con la classe personalizzata `[!div class="mx-tdBreakAll"]`.

Ecco un esempio di tabella Markdown con tre righe per le quali il ritorno a capo verrà gestito con `div` con il nome di classe `mx-tdBreakAll`.

```markdown
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

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Interruzioni di riga all'interno di parole nelle celle della seconda colonna della tabella

Può essere opportuno impostare l'inserimento automatico di interruzioni di riga all'interno di parole solo nella seconda colonna di una tabella. Per limitare le interruzioni alla seconda colonna, applicare la classe `mx-tdCol2BreakAll` usando la sintassi del wrapper `div`, come illustrato in precedenza.

### <a name="html-tables"></a>Tabelle HTML

Non è consigliabile usare tabelle HTML per docs.microsoft.com. Non sono leggibili nell'origine, mentre questo è un principio fondamentale di Markdown.
