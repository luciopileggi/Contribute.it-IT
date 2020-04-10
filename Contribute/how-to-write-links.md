---
title: Come usare collegamenti nella documentazione
description: Questo articolo rappresenta materiale sussidiario per la creazione di collegamenti a contenuto all'interno di docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624793"
---
# <a name="use-links-in-documentation"></a>Usare collegamenti nella documentazione

Questo articolo descrive come usare collegamenti ipertestuali da pagine ospitate in docs.microsoft.com. È facile aggiungere collegamenti all'interno di markdown, con alcune convenzioni. I collegamenti possono indirizzare gli utenti a contenuto all'interno della stessa pagina, in altre pagine vicine o in siti e URL esterni.

Il back-end del sito docs.microsoft.com usa i servizi OPS (Open Publishing Service) che supportano il Markdown conforme a [CommonMark][] analizzato tramite il motore di analisi [Markdig][]. Questa versione di Markdown è per lo più compatibile con [GitHub Flavored Markdown (GFM)][GFM], perché la maggior parte dei documenti viene archiviata in GitHub dove può essere modificata. Altre funzionalità vengono aggiunte tramite le estensioni per Markdown.

> [!IMPORTANT]
> Tutti i collegamenti devono essere protetti (`https` invece di `http`) ogni volta che la destinazione lo supporta (come dovrebbe essere nella maggior parte dei casi).

## <a name="link-text"></a>Testo del collegamento

Le parole che vengono incluse nel testo del collegamento devono essere semplici. Devono quindi essere parole normali o il titolo della pagina alla quale porta il collegamento.

> [!IMPORTANT]
> Non usare "fare clic qui". È una scelta inefficace per l'ottimizzazione dei motori di ricerca e non descrive adeguatamente la destinazione.

**Corretto:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**Non corretto:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Collegamenti da un articolo a un altro

Il sistema di pubblicazione supporta due tipi di collegamenti ipertestuali: **URL** e **collegamenti a file**.

Un collegamento di tipo URL può essere un percorso URL relativo alla radice di docs.microsoft.com o un URL assoluto che include la sintassi completa dell'URL, ad esempio `https://github.com/MicrosoftDocs/PowerShell-Docs`.

- Usare collegamenti URL quando si crea un collegamento a contenuto al di fuori del _docset_ corrente o tra un riferimento generato automaticamente e articoli concettuali all'interno del docset.
- Il modo più semplice per creare un collegamento relativo consiste nel copiare l'URL dal browser e quindi nel rimuovere `https://docs.microsoft.com/en-us` dal valore incollato nel codice Markdown.
   - Non includere le impostazioni locali presenti negli URL per le proprietà Microsoft (ad esempio, rimuovere "/en-us" dall'URL).

Un collegamento a file viene usato per collegare un articolo a un altro all'interno del docset.

- Tutti i percorsi di file usano caratteri barra (`/`) anziché caratteri barra rovesciata.
- Un articolo si collega a un altro articolo nella stessa directory:

  `[link text](article-name.md)`

- Un articolo si collega a un articolo nella directory padre della directory corrente:

  `[link text](../article-name.md)`

- Un articolo si collega a un articolo in una sottodirectory della directory corrente:

  `[link text](directory/article-name.md)`

- Un articolo si collega a un articolo in una sottodirectory della directory padre della directory corrente:

  `[link text](../directory/article-name.md)`

> [!NOTE]
> Nessuno degli esempi precedenti usa `~/` come parte del collegamento. Per creare un collegamento a un percorso assoluto che inizia dalla radice del repository, iniziare il collegamento con `/`. Quando ci si sposta nei repository di origine in GitHub, l'inserimento di `~/` genera collegamenti non validi. Iniziare il percorso con `/` risolve correttamente il problema.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>Struttura dei collegamenti in docs.microsoft.com

All'interno del contenuto pubblicato in docs.microsoft.com gli URL presentano la struttura seguente:

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

Esempi:

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` - Lingua dell'articolo (esempio: en-us o de-de)
- `<product-service>` - Nome del prodotto o del servizio (esempio: powershell, dotnet o azure)
- `[<feature-service>]` (facoltativo) - Nome della funzionalità o del servizio secondario del prodotto (esempio: csharp o load-balancer)
- `[<subfolder>]` (facoltativo) - Nome di una sottocartella all'interno di una funzionalità
- `<topic>` - Nome del file dell'articolo per l'argomento (esempio: load-balancer-overview o overview)
- `[?view=\<view-name>]` (facoltativo) - Nome visualizzazione usato dal selettore della versione per contenuto con più versioni disponibili (esempio: azps-3.5.0)

> [!TIP]
> Nella maggior parte dei casi, gli articoli nello stesso _docset_ hanno lo stesso frammento `<product-service>` nell'URL. Ad esempio:
> - Stesso docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - Docset diverso
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>Collegamento segnalibro

Per un collegamento segnalibro a un'intestazione nel file *corrente*, usare un simbolo hash seguito dalle parole dell'intestazione in lettere minuscole. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini:

```markdown
[Managed Disks](#managed-disks)
```

Per creare un collegamento a un'intestazione di segnalibro in un altro articolo, usare il collegamento relativo al file o al sito più un simbolo hash, seguito dalle parole dell'intestazione. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

È anche possibile copiare il collegamento segnalibro dall'URL. Per trovare l'URL, passare il puntatore del mouse sulla riga dell'intestazione in docs.microsoft.com. Verrà visualizzata un'icona di collegamento:

![Icona di collegamento nell'intestazione dell'articolo](media/how-to-write-links/bookmark-link.png)

Fare clic sull'icona di collegamento e quindi copiare il testo di ancoraggio del segnalibro dall'URL (ovvero, la parte dopo l'hash).

> [!NOTE]
> L'estensione Docs dispone anche di strumenti che facilitano la creazione di collegamenti.

### <a name="explicit-anchor-links"></a>Collegamenti di ancoraggio esplicito

L'aggiunta di collegamenti di ancoraggio esplicito che usano il tag HTML `<a>` non è necessaria né consigliata, tranne che nelle pagine hub e di destinazione. Usare invece i segnalibri generati automaticamente come descritto in [Collegamenti segnalibro](#bookmark-links). In caso di pagine hub e di destinazione, dichiarare ancoraggi come descritto di seguito:

```markdown
## <a id="anchortext" />Header text
```

oppure

```markdown
## <a name="anchortext" />Header text
```

E usare i comandi seguenti per collegarsi all'ancoraggio:

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> Il testo di ancoraggio deve sempre essere minuscolo e non deve contenere spazi.

## <a name="xref-cross-reference-links"></a>Collegamenti XRef (riferimenti incrociati)

I collegamenti XRef rappresentano il metodo consigliato per i collegamenti alle API, perché vengono convalidati in fase di compilazione. Per creare collegamenti a pagine di riferimento API generate automaticamente nel docset corrente o in altri docset, usare collegamenti XRef con l'ID univoco ([UID](#determine-the-uid)) del tipo di membro.

> [!TIP]
> È possibile usare l'[estensione Docs Markdown per VS Code][docsextension] (inclusa nel Docs Authoring Pack) per inserire collegamenti XRref .NET da visualizzare nel [browser delle API .NET][].

Controllare se l'API a cui si vuole creare un collegamento si trova in [docs.microsoft.com][docs] digitando tutto o in parte il nome completo dell'API nella casella di ricerca del [browser delle API .NET][] o della [Windows UWP][]. Se non vengono visualizzati risultati, il tipo non è ancora disponibile in docs.microsoft.com.

È possibile usare una delle sintassi seguenti:

- Collegamenti automatici:

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo. Il parametro di query `displayProperty=nameWithType` facoltativo produce testo di collegamento completo, ovvero **spazio dei nomi.tipo** per i tipi e **tipo.membro** per i membri dei tipi, inclusi i membri del tipo enumerazione.

- Collegamenti in stile Markdown:

   ```markdown
   [link text](xref:UID)
   ```

   Usare collegamenti in stile Markdown per i collegamenti XRef quando si vuole personalizzare il testo del collegamento visualizzato.

Esempi:

- **\<xref:System.String>** viene visualizzato come <xref:System.String>

- **\<xref:System.String?displayProperty=nameWithType>** viene visualizzato come <xref:System.String?displayProperty=nameWithType>

- **\[classe String](xref:System.String)** viene visualizzato come [classe String](xref:System.String).

Il parametro di query `displayProperty=fullName` funziona allo stesso modo di `displayProperty=nameWithType` per le classi. In altre parole, il testo del collegamento diventa **spaziodeinomi.nomeclasse**. Per i membri, tuttavia, il testo del collegamento viene visualizzato come **spaziodeinomi.nomeclasse.nomemembro**, che potrebbe non corrispondere al risultato voluto.

> [!NOTE]
> Gli UID fanno distinzione tra maiuscole e minuscole. Ad esempio, `<xref:System.Object>` viene risolto correttamente, al contrario di `<xref:system.object>`.

### <a name="xref-build-warnings-and-incremental-builds"></a>Avvisi di compilazione di XRef e compilazioni incrementali

Una compilazione incrementale compila solo i file che sono stati modificati o che sono stati interessati da una modifica. Se viene visualizzato un avviso di compilazione che segnala un collegamento XREF non valido, ma il collegamento segnalato in realtà è valido, il problema può essere dovuto al fatto che è stata eseguita una compilazione incrementale. Il file che ha causato l'avviso non è stato modificato, quindi non è stato compilato. L'avviso visualizzato si riferisce a una compilazione precedente. L'avviso scomparirà quando il file verrà modificato o se si attiva una compilazione completa (è possibile avviare una compilazione completa in ops.microsoft.com). Si tratta di un svantaggio delle compilazioni incrementali, perché DocFX non è in grado di rilevare un aggiornamento dei dati all'interno del servizio XREF.

### <a name="determine-the-uid"></a>Determinare l'UID

L'UID è in genere il nome completo della classe o del membro. Per determinare l'UID esistono almeno due metodi:

- Fare clic con il pulsante destro del mouse sulla pagina [Docs][docs] relativa a un tipo o a un membro, selezionare **Visualizza origine** e quindi copiare il valore **content** per **ms.assetid**:

  ![ms.assetid nell'origine per la pagina Web](media/how-to-write-links/ms-assetid.png)

- Usare il [sito di completamento automatico][] aggiungendo tutto o in parte il nome del tipo all'URL. Se, ad esempio, si immette `https://xref.docs.microsoft.com/autocomplete?text=Writeline` nella barra degli indirizzi del browser vengono visualizzati tutti i tipi e i metodi che contengono **Writeline** nel nome, insieme all'UID corrispondente.

#### <a name="verify-the-uid"></a>Verificare l'UID

Per verificare se l'UID è corretto, sostituire **System.String** nell'URL seguente con l'UID e quindi incollare l'URL nella barra degli indirizzi di un browser:

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> L'UID nell'URL fa distinzione tra maiuscole e minuscole. Se si sta controllando un UID di overload del metodo, non includere spazi tra i tipi di parametro.

Se viene visualizzato codice simile al seguente, l'UID è corretto:

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

Se nella pagina è visualizzato solo `[]`, l'UID non è corretto.

### <a name="percent-encoding-of-urls"></a>Codifica con simbolo di percentuale degli URL

I caratteri speciali nell'UID devono essere codificati in HTML come indicato di seguito:

| Carattere | Codifica HTML |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

Vedere l'elenco completo dei [codici con simbolo di percentuale](https://en.wikipedia.org/wiki/Percent-encoding).

Esempi di codifica:

- `System.Threading.Tasks.Task``1` viene codificato come `System.Threading.Tasks.Task%601` (vedere la [sezione sui tipi generici](#generic-types))

- `System.Exception.#ctor` viene codificato come `System.Exception.%23ctor`

- `System.Object.Equals*` viene codificato come `System.Object.Equals%2A`

### <a name="generic-types"></a>Tipi generici

I tipi generici sono tipi come `System.Collections.Generic.List<T>`. Se si passa a questo tipo nel [browser delle API .NET ](https://docs.microsoft.com/dotnet/api/) e se ne osserva l'URL, si nota che `<T>` nell'URL è scritto come `-1`, che in realtà rappresenta **`1**:

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

Per creare un collegamento a un tipo generico, ad esempio **List\<T>** , codificare il carattere di apice inverso **\`** con **%60**, come illustrato nell'esempio seguente:

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>Metodi

Per eseguire il collegamento a un metodo, è possibile collegarsi alla pagina del metodo generale aggiungendo un asterisco (`*`) dopo il nome del metodo o a un overload specifico. Usare, ad esempio, la pagina generale quando si vuole creare un collegamento al metodo `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` senza tipi di parametro specifici. Il carattere asterisco viene codificato con `%2A`. Ad esempio:

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` crea un collegamento a <xref:System.Object.Equals%2A?displayProperty=nameWithType>

Per creare un collegamento a un overload specifico, aggiungere le parentesi dopo il nome del metodo e includere il nome completo del tipo di ogni parametro. Non inserire alcuno spazio tra i nomi dei tipi. In caso contrario, il collegamento non funzionerà. Ad esempio:

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` crea un collegamento a <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>

## <a name="links-from-includes"></a>Collegamenti da file di inclusione

Dato che i file di inclusione sono posizionati in un'altra directory, è necessario usare percorsi relativi più lunghi. Per impostare un collegamento a un articolo da un file di inclusione, usare questo formato:

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> L'estensione [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) per Visual Studio Code consente di inserire correttamente collegamenti e segnalibri relativi senza la necessità di individuare i percorsi.

## <a name="links-in-selectors"></a>Collegamenti nei selettori

Un selettore è un componente di esplorazione visualizzato in un articolo della documentazione sotto forma di elenco a discesa. Quando il lettore seleziona un valore nell'elenco, il browser apre l'articolo selezionato. L'elenco del selettore in genere contiene collegamenti ad articoli strettamente correlati, ad esempio articoli sullo stesso argomento in linguaggi di programmazione diversi.

In presenza di selettori incorporati in un file di inclusione, per i collegamenti è necessario usare la struttura seguente:

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>Collegamenti in stile riferimento

È possibile usare i collegamenti in stile riferimento per rendere più leggibile il contenuto di origine. I collegamenti in stile riferimento sostituiscono la sintassi dei collegamenti inline con una sintassi semplificata che consente di spostare gli URL lunghi alla fine dell'articolo. Ecco un esempio tratto da [Daring Fireball](https://daringfireball.net/projects/markdown/):

Testo inline:

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Collegamenti di riferimento alla fine dell'articolo:

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

Assicurarsi di includere lo spazio dopo i due punti, prima del collegamento. Quando si imposta un collegamento ad altri articoli tecnici, se si dimentica di includere lo spazio il collegamento non funzionerà nell'articolo pubblicato.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Collegamenti a pagine non incluse nel set di documentazione tecnica

Per impostare un collegamento a una pagina in un'altra area di proprietà Microsoft, ad esempio una pagina dei prezzi, la pagina del contratto di servizio o qualsiasi altro contenuto che non sia un articolo della documentazione, usare un URL assoluto omettendo le impostazioni locali. L'obiettivo è che i collegamenti funzionino in GitHub e nel sito di rendering:

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>Collegamenti a siti di terze parti

Per un'esperienza utente ottimale, è consigliabile evitare il più possibile i reindirizzamenti degli utenti a un altro sito. Basare quindi i collegamenti a siti di terze parti, a volte necessari, su queste informazioni:

- **Responsabilità**: impostare un collegamento a contenuti di terze parti quando le informazioni da condividere sono di proprietà di terzi. Ad esempio, non è compito di Microsoft comunicare agli utenti come usare gli strumenti per sviluppatori Android, è una responsabilità di Google. Se necessario, Microsoft può spiegare come usare gli strumenti per sviluppatori di Android *con* Azure, ma è Google ad avere la responsabilità di pubblicare contenuti con istruzioni per l'uso dei suoi strumenti.
- **Approvazione del PM**: richiedere che Microsoft approvi il contenuto di terze parti. Con l'inserimento di questo tipo di collegamenti Microsoft fa una dichiarazione implicita in merito all'attendibilità del contenuto collegato e si impegna nei confronti dei clienti che seguono le istruzioni.
- **Verifica dello stato di aggiornamento**: assicurarsi che le informazioni di terze parti siano ancora aggiornate, corrette e pertinenti e che il collegamento non sia stato modificato.
- **Uscita dal sito**: comunicare agli utenti che stanno passando a un altro sito. Se dal contesto non risulta chiaro, aggiungere una frase esplicativa. Ad esempio: "I prerequisiti includono gli strumenti di sviluppo di Android, scaricabili dal sito Android Studio".
- **Passaggi successivi**: in questa sezione è appropriato aggiungere un collegamento, ad esempio, a un blog MVP. Anche in questo caso, assicurarsi che gli utenti capiscano che stanno per passare a un altro sito.
- **Informazioni legali**: la copertura legale Microsoft è disponibile in **Collegamenti a siti di Terzi** nel piè di pagina **Condizioni per l'utilizzo** in tutte le pagine del sito microsoft.com.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Browser delle API .NET]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Sito di completamento automatico]: https://xref.docs.microsoft.com/autocomplete?text=
