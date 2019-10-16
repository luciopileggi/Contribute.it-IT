---
title: Modello e foglio informativo per gli articoli .NET
description: Questo articolo contiene un pratico modello da usare per creare nuovi articoli per i repository di documentazione .NET.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 998ebf90c8a162451dd4ca2e7c8a55833ed9d408
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288374"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>Modello di metadati e Markdown per i documenti .NET

Questo modello dotnet/docs contiene esempi di sintassi Markdown e indicazioni per l'impostazione dei metadati.

Per creare un file Markdown, copiare in un nuovo file il modello incluso, completare i metadati come specificato di seguito e impostare l'intestazione H1 per il titolo dell'articolo.

## <a name="metadata"></a>Metadati

Il blocco di metadati necessario si trova nel seguente blocco di metadati di esempio:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Tra i due punti (:) e il valore di un elemento di metadati **deve** essere presente uno spazio.
- I due punti in un valore (ad esempio in un titolo) interrompono l'esecuzione del parser di metadati. In questo caso, racchiudere il titolo tra virgolette doppie (ad esempio `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title**: appare nei risultati dei motori di ricerca. Il titolo non deve essere identico al titolo incluso nell'intestazione H1 e non può contenere più di 60 caratteri.
- **description**: riepiloga il contenuto dell'articolo. In genere viene visualizzato nella pagina dei risultati della ricerca ma non viene utilizzato per classificare i risultati. La lunghezza deve essere inclusa tra 115 e 145 caratteri, spazi inclusi.
- **author**: deve contenere il **nome utente GitHub** dell'autore.
- **ms.date**: data dell'ultimo aggiornamento significativo. Aggiornare questo valore negli articoli esistenti se è stata eseguita una revisione e un aggiornamento dell'intero articolo. Per aggiornamenti minori, quali correzioni ortografiche o simili, non è necessario aggiornare il valore.

A ogni articolo sono associati altri metadati, ma in generale la maggior parte dei metadati viene applicata a livello della cartella e specificata in **docfx.json**.

## <a name="basic-markdown-gfm-and-special-characters"></a>Nozioni di base su Markdown, GFM e caratteri speciali

Per le nozioni di base su Markdown, GitHub Flavored Markdown (GFM) e sulle estensioni specifiche di OPS, vedere gli articoli generali [Markdown](how-to-write-use-markdown.md) e [Informazioni di riferimento su Markdown per OPS](markdown-reference.md).

Markdown usa caratteri speciali per la formattazione, quali \*, \` e \#. Se si vuole includere uno di questi caratteri nel contenuto, seguire una di queste due procedure:

- Far precedere una barra rovesciata al carattere speciale come "escape" (ad esempio `\*` per \*)
- Usare il [codice entità HTML](http://www.ascii.cl/htmlcodes.htm) per il carattere (ad esempio `&#42;` per &#42;).

## <a name="file-names"></a>Nomi di file

Per i nomi di file sono valide le seguenti regole:

* Contengono solo lettere minuscole, numeri e trattini.
* Non usare spazi o segni di punteggiatura. Usare il trattino per separare le parole e i numeri nel nome del file.
* Usare verbi di azione specifici, ad esempio sviluppare, acquistare, compilare, risolvere. Non usare parole al gerundio.
* Non usare parole estremamente brevi, ad esempio "un", "e", "il", "in", "o" e così via.
* Usare il formato Markdown e l'estensione file md.
* Usare nomi di file brevi. I nomi vengono inclusi nell'URL dell'articolo.

## <a name="headings"></a>Titoli

Usare le maiuscole/minuscole come nelle frasi comuni. Usare sempre la maiuscola per la prima parola di un titolo.

## <a name="text-styling"></a>Stile del testo

*Corsivo*: usarlo per file, cartelle, percorsi (per elementi lunghi, suddivisi sulla stessa riga), termini nuovi.

**Grassetto**: usarlo per elementi dell'interfaccia utente.

`Code`: usarlo per il codice inline, le parole chiave del linguaggio, i nomi di pacchetti NuGet, i comandi della riga di comando, i nomi di tabella e colonna del database e gli URL sui quali non è possibile fare clic.

## <a name="links"></a>Collegamenti

Vedere l'articolo generale [Collegamenti](how-to-write-links.md) per informazioni su ancoraggi, collegamenti interni, collegamenti ad altri documenti, inclusioni di codice e collegamenti esterni.

Il team di documentazione di .NET utilizza le convenzioni seguenti:

- Nella maggior parte dei casi si usano collegamenti relativi e si sconsiglia l'uso di `~/` nei collegamenti, perché i collegamenti relativi vengono risolti nell'origine in GitHub. Tuttavia quando si definisce il collegamento a un file in un repository dipendente, viene usato il carattere `~/` per fornire il percorso. Dato che i file nel repository dipendente si trovano in una posizione diversa in GitHub, i collegamenti non vengono risolti correttamente con collegamenti relativi, indipendentemente da come sono stati scritti.
- La specifica del linguaggio C# e la specifica del linguaggio Visual Basic sono incluse nei documenti .NET mediante l'aggiunta dell'origine dai repository del linguaggio. Le origini di markdown vengono gestite nei repository [csharplang](https://github.com/dotnet/csharplang) e [vblang](https://github.com/dotnet/vblang).

I collegamenti a una specifica devono fare riferimento alle directory di origine che includono le specifiche corrispondenti. Per C# la directory è **~/_csharplang/spec** e per VB la directory è **~/_vblang/spec** come illustrato nell'esempio seguente:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>Collegamenti alle API

Il sistema di build dispone di estensioni che consentono il collegamento alle API .NET senza dover ricorrere a collegamenti esterni. Si usa una delle sintassi seguenti:

1. Collegamento automatico: `<xref:UID>` o `<xref:UID?displayProperty=nameWithType>`

   Il parametro di query `displayProperty` produce un testo del collegamento completo. Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo.

2. Collegamento Markdown: `[link text](xref:UID)`

   Può essere usato quando si vuole personalizzare il testo del collegamento visualizzato.

Esempi:

- `<xref:System.String>` viene visualizzato come [String](https://docs.microsoft.com/dotnet/api/system.string)
- `<xref:System.String?displayProperty=nameWithType>` viene visualizzato come [System.String](https://docs.microsoft.com/dotnet/api/system.string)
- `[String class](xref:System.String)` viene visualizzato come [String class](https://docs.microsoft.com/dotnet/api/system.string)

Per altre informazioni sull'uso di questa notazione, vedere [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Uso del riferimento incrociato).

Se uno o più UID contengono i caratteri speciali \`, \# o \*, il valore dell'UID deve essere con codifica HTML come `%60`, `%23` e `%2A` rispettivamente. A volte sono presenti parentesi con codifica, ma questo non è un requisito.

Esempi:

- System.Threading.Tasks.Task\`1 diventa `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor diventa `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) diventa `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

È possibile trovare gli UID dei tipi, un elenco di overload di membro o un membro in overload specifico in `https://xref.docs.microsoft.com/autocomplete`. La stringa di query `?text=*\<type-member-name>*` identifica il tipo o il membro di cui si vogliono visualizzare gli UID. Ad esempio, `https://xref.docs.microsoft.com/autocomplete?text=string.format` recupera gli overload di [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format). Lo strumento cerca il parametro query `text` fornito in qualsiasi parte dell'UID. Ad esempio è possibile cercare il nome membro (ToString), il nome membro parziale (ToStri), il tipo e il nome membro (Double.ToString) e così via.

Se si aggiunge \* (o `%2A`) dopo l'UID, il collegamento rappresenta la pagina di overload e non un'API specifica. È ad esempio possibile usare questa opzione per creare un collegamento alla pagina [Metodo List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) in modo generico anziché un overload specifico come [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_). È anche possibile usare \* per il collegamento a una pagina membro quando il membro non è in overload; in tal modo è possibile evitare di includere l'elenco parametri nell'UID.

Per il collegamento all'overload di un metodo specifico, è necessario includere il nome del tipo completo di ciascun parametro del metodo. Ad esempio, \<xref:System.DateTime.ToString> definisce il collegamento al metodo senza parametri [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), mentre \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> definisce il collegamento al metodo [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).

Per il collegamento a un tipo generico, ad esempio [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), usare il carattere \` (`%60`) seguito dal numero dei parametri di tipo generico. Ad esempio `<xref:System.Nullable%601>` definisce il collegamento al tipo [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), mentre `<xref:System.Func%602>` definisce il collegamento al delegato [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).

## <a name="code"></a>Codice

Il miglior metodo per includere codice è l'inclusione di frammenti di codice da un esempio funzionante. Creare l'esempio in base alle istruzioni fornite nell'articolo [Contributing to .NET docs](dotnet-contribute-process.md#contributing-to-samples) (Contributo ai documenti .NET). Le regole di base per l'inclusione di codice si trovano nelle indicazioni generali per il [codice](how-to-write-use-markdown.md#code-snippets).

È possibile includere il codice usando la sintassi seguente:

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (*facoltativo* ma *consigliato*)
  * Linguaggio del frammento di codice al quale si fa riferimento.

* `<name>` (*facoltativo*)
  * Nome del frammento di codice. Non deve avere alcun impatto sul file HTML di output ma può essere usato per rendere più leggibile l'origine del Markdown.

* `<pathToFile>` (*obbligatorio*)
  * Percorso relativo nel file system che indica il file del frammento di codice a cui fare riferimento. Questa notazione può essere complicata dai vari repository che costituiscono il set di documentazione di .NET. I campioni .NET si trovano nel repository dotnet/samples. Tutti i percorsi di frammenti iniziano con `~/samples` e la parte rimanente indica il percorso all'origine dalla radice del repository.

* `<queryoption>` (*facoltativo*)
  * Usato per specificare come il codice deve essere recuperato dal file:
    * `#`: `#{tagname}` (nome del tag) *o* `#L{startlinenumber}-L{endlinenumber}` (intervallo di righe).
    L'uso dei numeri di riga è sconsigliato in quanto non sufficientemente affidabile. Il nome tag è il metodo preferibile per il riferimento ai frammenti di codice. Usare nomi tag significativi. Molti frammenti sono stati sottoposti a migrazione da una piattaforma precedente e i tag hanno nomi come `Snippet1`, `Snippet2` e così via. Questa prassi è più difficile da gestire.
    * `range`: `?range=1,3-5` Intervallo di righe. Questo esempio include le righe 1, 3, 4 e 5.

Se possibile, è sempre consigliabile usare l'opzione del nome del tag. Il nome tag è il nome di un'area o di un commento di codice nel formato di `Snippettagname` presente nel codice di origine. L'esempio seguente illustra come creare il riferimento al nome tag `BasicThrow`:

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

Il percorso relativo dell'origine nel repository **dotnet/samples** segue il percorso `~/samples`.

È anche possibile vedere come sono strutturati i tag dei frammenti di codice in [questo file di origine](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs). Per altri dettagli sulla rappresentazione dei nomi di tag nei file di origine dei frammenti di codice in base al linguaggio, vedere le [linee guida per DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

L'esempio seguente mostra il codice incluso in tutti e tre i linguaggi .NET:

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

L'inclusione di frammenti da programmi completi garantisce che tutto il codice sia conforme al sistema di integrazione continua (CI). Se tuttavia è necessario visualizzare un elemento che provoca errori di compilazione o di runtime, è possibile usare i blocchi di codice inline.

## <a name="images"></a>Immagini

### <a name="static-image-or-animated-gif"></a>Immagine statica o GIF animata

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Immagine collegata

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Video

Attualmente è possibile incorporare video sia di Channel 9 che di YouTube con la sintassi seguente:

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

Per ottenere l'URL corretto del video, selezionare la scheda **Incorpora** sotto il fotogramma video e copiare l'URL dall'elemento `<iframe>`. Ad esempio:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Per ottenere l'URL corretto del video, fare clic con il pulsante destro del mouse sul video, selezionare **Copia codice di incorporamento** e copiare l'URL dall'elemento `<iframe>`.

```markdown
> [!VIDEO <youtube_video_link>]
```

Ad esempio:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>Estensioni docs.microsoft

docs.microsoft include alcune estensioni aggiuntive in GitHub Flavored Markdown.

### <a name="checked-lists"></a>Elenchi con segni di spunta

Per gli elenchi è disponibile uno stile personalizzato. È possibile contrassegnare gli elenchi con segni di spunta verdi.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Il rendering è il seguente:

> [!div class="checklist"]
> * Come creare un'app .NET Core
> * Come aggiungere un riferimento al pacchetto Microsoft.XmlSerializer.Generator
> * Come modificare MyApp.csproj per aggiungere dipendenze
> * Come aggiungere una classe e un elemento XmlSerializer
> * Come compilare ed eseguire l'applicazione

Per un esempio di elenchi con segni di spunta, vedere la [documentazione di .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).

### <a name="buttons"></a>Pulsanti

Collegamenti ai pulsanti:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Il rendering è il seguente:

> [!div class="button"]
> [button links](dotnet-contribute.md)

Per un esempio di pulsanti attivi, vedere la [documentazione di Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).

### <a name="step-by-steps"></a>Guide dettagliate

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

Per un esempio di guide dettagliate attive, vedere la [Guida di C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).
