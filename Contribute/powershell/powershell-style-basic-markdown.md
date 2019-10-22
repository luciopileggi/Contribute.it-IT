---
title: Modelli e foglio informativo per gli articoli di PowerShell
description: Questo articolo contiene un pratico modello da usare per creare nuovi articoli per la documentazione di PowerShell
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290358"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>Guida di stile di Markdown per PowerShell-Docs

Questo articolo include alcune linee guida per lo stile specifiche per il contenuto di PowerShell-Docs.

Per altre indicazioni sullo stile di scrittura, vedere la [guida di stile Microsoft](https://docs.microsoft.com/style-guide/welcome/).

## <a name="metadata"></a>Metadati

Questo modello contiene esempi di sintassi Markdown e indicazioni per l'impostazione dei metadati.
Per creare un file Markdown, copiare in un nuovo file il modello incluso, completare i metadati come specificato di seguito e impostare l'intestazione H1 per il titolo dell'articolo.

Il blocco di metadati necessario si trova nel seguente blocco di metadati di esempio:

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Tra i due punti (:) e il valore di un elemento di metadati **deve** essere presente uno spazio.
- I due punti in un valore (ad esempio in un titolo) interrompono l'esecuzione del parser di metadati. In questo caso, racchiudere il titolo tra virgolette doppie (ad esempio `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author**: deve contenere il **nome utente GitHub** dell'autore.
- **description**: riepiloga il contenuto dell'articolo. In genere viene visualizzato nella pagina dei risultati della ricerca ma non viene utilizzato per classificare i risultati. La lunghezza deve essere inclusa tra 115 e 145 caratteri, spazi inclusi.
- **ms.date**: data dell'ultimo aggiornamento significativo. Aggiornare questo valore negli articoli esistenti se è stata eseguita una revisione e un aggiornamento dell'intero articolo. Per correzioni di minore entità, come correzioni ortografiche o simili, non occorre aggiornare il valore.
- **title**: appare nei risultati dei motori di ricerca. Il titolo non deve essere identico al titolo incluso nell'intestazione H1 e non può contenere più di 60 caratteri.

A ogni articolo sono associati altri metadati, ma in generale la maggior parte dei metadati viene applicata a livello della cartella e specificata in **docfx.json**.

## <a name="product-terminology"></a>Terminologia del prodotto

Sono disponibili diverse varianti di PowerShell. Questa tabella definisce alcuni dei diversi termini usati per discutere di PowerShell.

- **PowerShell** - Termine predefinito. PowerShell è il prodotto fornito. Il termine PowerShell può essere usato per descrivere qualsiasi edizione del prodotto.
- **PowerShell Core** - PowerShell basato su .NET Core Common Language Runtime (CoreCLR) per qualsiasi piattaforma supportata.
- **Windows PowerShell** - PowerShell basato su .NET Framework Common Language Runtime (CLR). Windows PowerShell viene fornito solo in Windows e richiede la versione completa di .NET Framework CLR.

In generale, i riferimenti a "Windows PowerShell" nella documentazione possono essere modificati in "PowerShell".
"Windows PowerShell" **non** deve essere modificato nelle presentazioni della tecnologia specifica di Windows.

## <a name="basic-markdown-gfm-and-special-characters"></a>Nozioni di base su Markdown, GFM e caratteri speciali

Per le nozioni di base su Markdown, GitHub Flavored Markdown (GFM) e sulle estensioni specifiche di OPS, vedere gli articoli generali [Markdown](../how-to-write-use-markdown.md) e [Informazioni di riferimento su Markdown per OPS](../markdown-reference.md).

Markdown usa caratteri speciali per la formattazione, quali \*, \` e \#. Se si vuole includere uno di questi caratteri nel contenuto, seguire una di queste due procedure:

- Far precedere una barra rovesciata al carattere speciale come "escape" (ad esempio `\*` per \*)
- Usare il [codice entità HTML](http://www.ascii.cl/htmlcodes.htm) per il carattere (ad esempio `&#42;` per &#42;).
- I file markdown devono usare il testo ASCII normale o la codifica UTF-8. Tuttavia, evitare di usare caratteri UTF-8 a più byte. Usare invece un'entità HTML. Per i simboli di copyright, ad esempio, usare `&copy;`.
  Il rendering viene eseguito come: "&copy;".

## <a name="hyperlinks"></a>Collegamenti ipertestuali

- Evitare l'uso di URL non elaborati (bare). Per i collegamenti è necessario usare la sintassi Markdown `[friendlyname](url-or-path)`
- I collegamenti devono avere un nome descrittivo, in genere il titolo dell'argomento collegato
- Tutti gli elementi nella sezione "Collegamenti correlati" nella parte inferiore devono essere collegati con collegamento ipertestuale.
- Usare i collegamenti relativi per il collegamento ad altro contenuto ospitato in **docs.microsoft.com**.
- Non usare apici inversi, il grassetto o altro markup all'interno delle parentesi quadre di un collegamento ipertestuale.

Per informazioni più dettagliate sui collegamenti, vedere [Uso di collegamenti nella documentazione](../how-to-write-links.md).

## <a name="filenames"></a>Nomi di file

Per i nomi di file usare le regole seguenti:

- Includere solo lettere, numeri e trattini.
- Non usare spazi o segni di punteggiatura. Usare il trattino per separare le parole e i numeri nel nome del file.
- Usare verbi di azione specifici, ad esempio sviluppare, acquistare, compilare, risolvere. Non usare parole al gerundio.
- Non usare parole estremamente brevi, ad esempio "un", "e", "il", "in", "o" e così via.
- Usare il formato Markdown e l'estensione file md.
- Usare nomi di file brevi. I nomi vengono inclusi nell'URL dell'articolo.

## <a name="blank-lines-spaces-and-tabs"></a>Righe vuote, spazi e tabulazioni

Rimuovere le righe vuote duplicate. Più righe vuote vengono sottoposte a rendering come una singola riga vuota in HTML, quindi più righe vuote non hanno alcuno scopo.

Le righe vuote segnalano anche la fine di un blocco in Markdown. Deve esserci una sola riga vuota tra blocchi Markdown di tipi diversi, ad esempio tra un paragrafo e un elenco o un'intestazione.

> [!NOTE]
> La spaziatura è significativa in Markdown. Usa sempre gli spazi anziché tabulazioni fisse. Rimuovere gli spazi superflui alla fine delle righe.

## <a name="titles-and-headings"></a>Titoli e intestazioni

Usare solo [intestazioni ATX][atx] (intestazioni in stile #, anziché `=` o `-`).

- Scrivere in lettere maiuscole solo i nomi propri e la prima lettera di un titolo o di un'intestazione
- Deve esserci un solo spazio tra `#` e la prima lettera dell'intestazione
- Le intestazioni devono essere circondate da una sola riga vuota
- È consentita una sola intestazione H1 per documento
- I livelli di intestazione devono essere incrementati di uno, non saltare livelli
- Non usare apici inversi, il grassetto o altro markup nelle intestazioni

> [!CAUTION]
> Lo schema applicato da [PlatyPS][platyPS] per le informazioni di riferimento sui cmdlet richiede intestazioni H2 e H3 specifiche. L'aggiunta o la rimozione di intestazioni può interrompere la compilazione. Per altre informazioni, vedere la [guida di stile per le informazioni di riferimento sui cmdlet](powershell-style-reference.md).

## <a name="limit-line-length-to-100-characters"></a>Limitare la lunghezza delle righe a 100 caratteri

Questo semplifica l'output da riga di comando per diff e cronologia.

Questa regola non è stata applicata per gran parte del contenuto esistente in PowerShell-Docs, ma l'obiettivo è aggiornare il contenuto corrispondentemente nel tempo. Qualsiasi aiuto è il benvenuto. L'[estensione Reflow Markdown][reflow] in Visual Studio Code (VSCode) semplifica la riformattazione dei paragrafi in base a questo limite.

## <a name="lists"></a>Elenchi

Se l'elenco contiene più frasi o paragrafi, prendere in considerazione l'uso di un'intestazione di livello inferiore anziché di un elenco.

L'elenco deve essere circondato da una singola riga vuota.

### <a name="unordered-lists"></a>Elenchi non ordinati

Non terminare gli elementi degli elenchi con un punto a meno che non contengano più frasi. Usare il segno meno (`-`) per i punti elenco negli elenchi. In questo modo si evita confusione con il markup per il grassetto o il corsivo che usa l'asterisco [`*`]. Per includere un paragrafo o altri elementi come elemento puntato, inserire un'interruzione di riga e allineare il rientro al primo carattere dopo il punto elenco.

Ad esempio:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

Questo è un elenco con sottoelementi di un elemento puntato.

- Primo elemento puntato

  Frase che spiega il primo punto elenco.

  - Sottoelemento puntato

    Frase che spiega il punto elenco secondario.

- Secondo elemento puntato
- Terzo elemento puntato

### <a name="ordered-lists"></a>Elenchi ordinati

Per includere un paragrafo o altri elementi sotto un elemento numerato, allineare il rientro al primo carattere dopo il numero dell'elemento.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

per ottenere questo output:

> 1. Per il primo elemento, inserire un singolo spazio dopo 1. Le frasi lunghe devono essere mandate a capo alla riga successiva e devono essere allineate al primo carattere dopo l'indicatore di elenco numerato.
>
>    Per includere un secondo elemento (come questo), inserire un'interruzione di riga dopo il primo e allineare i rientri. Il rientro del secondo elemento deve essere allineato al primo carattere dopo l'indicatore di elenco numerato. Per gli elementi con cifra singola, come questo, viene applicato un rientro alla colonna 4. Per gli elementi con due cifre, ad esempio l'elemento numero 10, applicare un rientro alla colonna 5.
>
> 1. Il successivo elemento numerato inizia qui.

Tutti gli elementi di un elenco numerato devono usare il numero `1.` anziché incrementare per ogni elemento.
Il rendering di Markdown incrementa automaticamente il valore. In questo modo, il riordino degli elementi risulta più semplice e viene standardizzato il rientro del contenuto subordinato.

## <a name="formatting-command-syntax-elements"></a>Formattazione degli elementi della sintassi dei comandi

- Per i nomi dei cmdlet di PowerShell viene usata la [combinazione di maiuscole/minuscole Pascal][pascal-case]. I verbi sono separati dai sostantivi con un segno meno. Usare sempre il nome con combinazione di maiuscole/minuscole Pascal completo per i cmdlet e i parametri. Evitare l'uso di alias, se non per la presentazione specifica di un alias.

- All'interno di un paragrafo, le parole chiave del linguaggio, i nomi dei cmdlet e i riferimenti alle variabili devono essere racchiusi tra caratteri di apice inverso (`` ` ``). I nomi di proprietà, parametri e classi devono essere in **grassetto**.

  Ad esempio:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- Quando si fa riferimento a un parametro in base al nome, il nome deve essere in **grassetto**. Quando si illustra l'uso di un parametro con il prefisso segno meno, il parametro deve essere racchiuso tra caratteri di apice inverso. Ad esempio:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- Quando si fa riferimento a comandi esterni (EXE, script e così via), il nome del comando deve essere in grassetto, tutto minuscolo (o con iniziale maiuscola se si trova all'inizio di una frase) e includere l'estensione di file appropriata. Ad esempio:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- Quando si mostra un esempio di utilizzo di un comando esterno, l'esempio deve essere racchiuso tra caratteri di apice inverso.
  In presenza di un conflitto di nomi con un alias, è necessario includere l'estensione del file nell'esempio del comando. Ad esempio:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- Quando si scrive un articolo concettuale, anziché contenuto di riferimento, la prima istanza del nome di un cmdlet deve essere impostata come collegamento ipertestuale alla documentazione del cmdlet. Non usare apici inversi, il grassetto o altro markup all'interno delle parentesi quadre di un collegamento ipertestuale.

  Ad esempio:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  Per altre informazioni, vedere la sezione [Collegamenti ipertestuali](#hyperlinks) della guida di stile.

## <a name="images"></a>Immagini

La sintassi per l'inclusione di un'immagine è la seguente:

```Syntax
![[alt text]](<folderPath>)
```

Esempio:

```markdown
![Introduction](./media/overview/Introduction.png)
```

Dove `alt text` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine. Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo. È anche utile in presenza di un bug nel sito a causa del quale non è possibile eseguire il rendering dell'immagine.

Le immagini devono essere archiviate in una cartella `media/<article-name>` all'interno della cartella che contiene l'articolo. Le immagini non devono essere condivise tra gli articoli. Creare una cartella corrispondente al nome del file dell'articolo nella cartella `media`. Copiare le immagini per tale articolo nella nuova cartella. Se un'immagine viene usata da più articoli, ogni cartella di immagini deve avere una copia del file di immagine. Questa procedura impedisce che la modifica di un'immagine in un articolo abbia effetti su un altro articolo.

In alcuni casi, è necessario condividere immagini, ad esempio logo e icone, in più articoli. Queste immagini vengono archiviate nella cartella `/media/shared` nella radice del repository.

Sono supportati i tipi di file di immagine seguenti: *.png", *.gif", *.jpeg", *.jpg", *.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
