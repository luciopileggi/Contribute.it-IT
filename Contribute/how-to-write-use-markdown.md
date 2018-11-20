---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 21194c4bd6020d847b526a4d9544c826aa199e2a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609523"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Come usare Markdown per scrivere articoli di Docs

Gli articoli di [docs.microsoft.com](http://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere. Per questo motivo si sta imponendo rapidamente come standard del settore.

Dato che il contenuto di Docs è archiviato in GitHub, è possibile usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni. In più, Open Publishing Services (OPS) implementa il parser Markdig per Markdown. Markdig è altamente compatibile con GFM e aggiunge funzionalità per abilitare funzioni specifiche di Docs.

* Markdig è un processore Markdown per .NET veloce, potente, estensibile e conforme a CommonMark.
* https://github.com/lunet-io/markdig
* Supporto della community migliorato
* Supporto degli standard migliorato

## <a name="markdown-basics"></a>Nozioni di base su Markdown

### <a name="headings"></a>Titoli

Per creare un titolo, usare il segno di cancelletto (#), come segue:

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Le intestazioni devono essere in stile atx. Devono quindi iniziare con un numero di caratteri cancelletto (#) compreso tra 1 e 6, corrispondente in HTML ai livelli di intestazione da H1 a H6. Quelli riportati qui sopra sono esempi di intestazioni di livello da 1 a 4.

Nell'argomento **deve** essere presente una sola intestazione di primo livello (H1), che verrà visualizzata come titolo sulla pagina.

Se l'intestazione termina con un carattere `#`, perché il rendering sia corretto è necessario aggiungere un altro carattere `#` alla fine, come, ad esempio, in `# Async Programming in F# #`.

Le intestazioni di secondo livello generano il sommario della sezione "In questo articolo", immediatamente dopo il titolo sulla pagina.

### <a name="bold-and-italic-text"></a>Testo in grassetto e corsivo

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
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Citazioni

Per creare citazioni, si usa il carattere `>`:

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Ecco il rendering dell'esempio precedente:

> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.

### <a name="lists"></a>Elenchi

#### <a name="unordered-list"></a>Elenco non ordinato

Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini. Il testo Markdown seguente, ad esempio:

```markdown
- List item 1
- List item 2
- List item 3
```

verrà rappresentato nel modo seguente:

- List item 1
- List item 2
- List item 3

Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio. Il testo Markdown seguente, ad esempio:

```markdown
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

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

verrà rappresentato nel modo seguente:

1. First instruction
2. Second instruction
3. Third instruction

Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio. Il testo Markdown seguente, ad esempio:

```markdown
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

### <a name="tables"></a>Tables

Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM. È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-). I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna. Includere una riga vuota prima della tabella per assicurarne il rendering corretto.

Il testo Markdown seguente, ad esempio:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

verrà rappresentato nel modo seguente:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Per altre informazioni sulla creazione di tabelle, vedere:

- La [funzionalità per il ritorno a capo nelle tabelle](#table-wrapping) di Markdig, utile per la formattazione di tabelle estese.
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

L'alias dopo i tre apici inversi iniziali '`' definisce l'evidenziazione della sintassi da usare. L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:

Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.

|Nome|Etichetta Markdown|
|-----|-------|
|Console .NET|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Interfaccia della riga di comando di Azure|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# nel browser|csharp-interactive|
|Console|console|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Formula PowerApps|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|Interfaccia della riga di comando di VSTS|vstscli|
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

## <a name="ops-custom-markdown-extensions"></a>Estensioni Markdown personalizzate di OPS

> [!NOTE]
> OPS (Open Publishing Services) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM). Markdig aggiunge altre funzionalità tramite le estensioni per Markdown. Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento (vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).

Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via. Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:

- Blocchi per le note
- File di inclusione
- Selettori
- Video incorporati
- Frammenti di codice/esempi

Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.

### <a name="note-blocks"></a>Blocchi per le note

Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:

- NOTA
- AVVISO
- SUGGERIMENTO
- IMPORTANTE

In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi. Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.

Esempi:

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

Il rendering è il seguente:

> [!NOTE]
> Questa è una NOTA

> [!WARNING]
> Questo è un AVVISO

> [!TIP]
> Questo è un SUGGERIMENTO

> [!IMPORTANT]
> Questo testo è IMPORTANTE

### <a name="includes"></a>File di inclusione

In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig. Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato. Esistono tre tipi di inclusioni disponibili per agevolare il riutilizzo del contenuto:

- Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.
- Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.
- Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.

Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (con estensione md), che possono contenere qualsiasi codice Markdown valido. Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository. Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.

Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:

- Usare le inclusioni ogni volta che occorre visualizzare lo stesso testo in più articoli.
- Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa. Non usarle per includere testi più piccoli di una frase.
- Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig. Saranno visualizzate solo dopo la pubblicazione.
- Assicurarsi che tutto il testo in un'inclusione sia scritto con frasi complete o frasi che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione. Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.
- Non incorporare inclusioni in altre inclusioni. Ciò non è supportato.
- Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali. La directory media non deve includere immagini alla radice. Se nell'inclusione non sono contenute immagini, non è necessaria una directory corrispondente per i file multimediali.
- Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione. Usare un file separato con un nome univoco per ogni inclusione e articolo. Archiviare il file multimediale nella cartella associata all'inclusione.
- Non usare un'inclusione come unico contenuto di un articolo.  Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.

Esempio:

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Selettori

Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee. Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili. In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.

Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un'inclusione. A questo punto è possibile fare riferimento a quell'inclusione in tutti gli articoli che usano lo stesso selettore.

Di seguito viene illustrato un esempio di selettore:

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

Per un esempio di selettori attivi, vedere la [documentazione di Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).

### <a name="code-includes"></a>Inclusioni di codice

Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice. Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:

- Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.
- Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.

## <a name="gotchas-and-troubleshooting"></a>Problemi e risoluzione

### <a name="alt-text"></a>Testo alternativo

Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente. Ad esempio, invece di questa formattazione:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:

```markdown
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

## <a name="see-also"></a>Vedere anche:

### <a name="markdown-resources"></a>Risorse per Markdown

- [Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)
- [Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)
- [Nozioni di base su Markdown in GitHub](https://help.github.com/articles/markdown-basics/)
- [Guida Markdown](https://www.markdownguide.org/)
