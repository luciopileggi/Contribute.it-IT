---
title: Modelli e foglio informativo per gli articoli di PowerShell
description: Questo articolo contiene un pratico modello da usare per creare nuovi articoli per la documentazione di PowerShell
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331930"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="34f7f-103">Guida di stile di Markdown per PowerShell-Docs</span><span class="sxs-lookup"><span data-stu-id="34f7f-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="34f7f-104">Questo articolo include alcune linee guida per lo stile specifiche per il contenuto di PowerShell-Docs.</span><span class="sxs-lookup"><span data-stu-id="34f7f-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="34f7f-105">Per altre indicazioni sullo stile di scrittura, vedere la [guida di stile Microsoft](https://docs.microsoft.com/style-guide/welcome/).</span><span class="sxs-lookup"><span data-stu-id="34f7f-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="34f7f-106">Metadati</span><span class="sxs-lookup"><span data-stu-id="34f7f-106">Metadata</span></span>

<span data-ttu-id="34f7f-107">Questo modello contiene esempi di sintassi Markdown e indicazioni per l'impostazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="34f7f-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="34f7f-108">Per creare un file Markdown, copiare in un nuovo file il modello incluso, completare i metadati come specificato di seguito e impostare l'intestazione H1 per il titolo dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="34f7f-109">Il blocco di metadati necessario si trova nel seguente blocco di metadati di esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="34f7f-110">Tra i due punti (:) e il valore di un elemento di metadati **deve** essere presente uno spazio.</span><span class="sxs-lookup"><span data-stu-id="34f7f-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="34f7f-111">I due punti in un valore (ad esempio in un titolo) interrompono l'esecuzione del parser di metadati.</span><span class="sxs-lookup"><span data-stu-id="34f7f-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="34f7f-112">In questo caso, racchiudere il titolo tra virgolette doppie (ad esempio `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="34f7f-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="34f7f-113">**author**: deve contenere il **nome utente GitHub** dell'autore.</span><span class="sxs-lookup"><span data-stu-id="34f7f-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="34f7f-114">**description**: riepiloga il contenuto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="34f7f-115">In genere viene visualizzato nella pagina dei risultati della ricerca ma non viene utilizzato per classificare i risultati.</span><span class="sxs-lookup"><span data-stu-id="34f7f-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="34f7f-116">La lunghezza deve essere inclusa tra 115 e 145 caratteri, spazi inclusi.</span><span class="sxs-lookup"><span data-stu-id="34f7f-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="34f7f-117">**ms.date**: data dell'ultimo aggiornamento significativo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="34f7f-118">Aggiornare questo valore negli articoli esistenti se è stata eseguita una revisione e un aggiornamento dell'intero articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="34f7f-119">Per correzioni di minore entità, come correzioni ortografiche o simili, non occorre aggiornare il valore.</span><span class="sxs-lookup"><span data-stu-id="34f7f-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="34f7f-120">**title**: appare nei risultati dei motori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="34f7f-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="34f7f-121">Il titolo non deve essere identico al titolo incluso nell'intestazione H1 e non può contenere più di 60 caratteri.</span><span class="sxs-lookup"><span data-stu-id="34f7f-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="34f7f-122">A ogni articolo sono associati altri metadati, ma in generale la maggior parte dei metadati viene applicata a livello della cartella e specificata in **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="34f7f-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="34f7f-123">Terminologia del prodotto</span><span class="sxs-lookup"><span data-stu-id="34f7f-123">Product Terminology</span></span>

<span data-ttu-id="34f7f-124">Sono disponibili diverse varianti di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="34f7f-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="34f7f-125">Questa tabella definisce alcuni dei diversi termini usati per discutere di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="34f7f-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="34f7f-126">**PowerShell** - Termine predefinito.</span><span class="sxs-lookup"><span data-stu-id="34f7f-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="34f7f-127">PowerShell è il prodotto fornito.</span><span class="sxs-lookup"><span data-stu-id="34f7f-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="34f7f-128">Il termine PowerShell può essere usato per descrivere qualsiasi edizione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="34f7f-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="34f7f-129">**PowerShell Core** - PowerShell basato su .NET Core Common Language Runtime (CoreCLR) per qualsiasi piattaforma supportata.</span><span class="sxs-lookup"><span data-stu-id="34f7f-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="34f7f-130">**Windows PowerShell** - PowerShell basato su .NET Framework Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="34f7f-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="34f7f-131">Windows PowerShell viene fornito solo in Windows e richiede la versione completa di .NET Framework CLR.</span><span class="sxs-lookup"><span data-stu-id="34f7f-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="34f7f-132">In generale, i riferimenti a "Windows PowerShell" nella documentazione possono essere modificati in "PowerShell".</span><span class="sxs-lookup"><span data-stu-id="34f7f-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="34f7f-133">"Windows PowerShell" **non** deve essere modificato nelle presentazioni della tecnologia specifica di Windows.</span><span class="sxs-lookup"><span data-stu-id="34f7f-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="34f7f-134">Nozioni di base su Markdown, GFM e caratteri speciali</span><span class="sxs-lookup"><span data-stu-id="34f7f-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="34f7f-135">Per le nozioni di base su Markdown, GitHub Flavored Markdown (GFM) e sulle estensioni specifiche per OPS, vedere l'articolo [Informazioni di riferimento su Markdown](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="34f7f-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="34f7f-136">Markdown usa caratteri speciali per la formattazione, quali \*, \` e \#.</span><span class="sxs-lookup"><span data-stu-id="34f7f-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="34f7f-137">Se si vuole includere uno di questi caratteri nel contenuto, seguire una di queste due procedure:</span><span class="sxs-lookup"><span data-stu-id="34f7f-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="34f7f-138">Far precedere una barra rovesciata al carattere speciale come "escape" (ad esempio `\*` per \*)</span><span class="sxs-lookup"><span data-stu-id="34f7f-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="34f7f-139">Usare il [codice entità HTML](http://www.ascii.cl/htmlcodes.htm) per il carattere (ad esempio `&#42;` per &#42;).</span><span class="sxs-lookup"><span data-stu-id="34f7f-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="34f7f-140">I file markdown devono usare il testo ASCII normale o la codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="34f7f-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="34f7f-141">Tuttavia, evitare di usare caratteri UTF-8 a più byte.</span><span class="sxs-lookup"><span data-stu-id="34f7f-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="34f7f-142">Usare invece un'entità HTML.</span><span class="sxs-lookup"><span data-stu-id="34f7f-142">Instead use an HTML entity.</span></span> <span data-ttu-id="34f7f-143">Per i simboli di copyright, ad esempio, usare `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="34f7f-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="34f7f-144">Il rendering viene eseguito come: "&copy;".</span><span class="sxs-lookup"><span data-stu-id="34f7f-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="34f7f-145">Collegamenti ipertestuali</span><span class="sxs-lookup"><span data-stu-id="34f7f-145">Hyperlinks</span></span>

- <span data-ttu-id="34f7f-146">Evitare l'uso di URL non elaborati (bare).</span><span class="sxs-lookup"><span data-stu-id="34f7f-146">Avoid using bare URLs.</span></span> <span data-ttu-id="34f7f-147">Per i collegamenti è necessario usare la sintassi Markdown `[friendlyname](url-or-path)`</span><span class="sxs-lookup"><span data-stu-id="34f7f-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="34f7f-148">I collegamenti devono avere un nome descrittivo, in genere il titolo dell'argomento collegato</span><span class="sxs-lookup"><span data-stu-id="34f7f-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="34f7f-149">Tutti gli elementi nella sezione "Collegamenti correlati" nella parte inferiore devono essere collegati con collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="34f7f-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="34f7f-150">Usare i collegamenti relativi per il collegamento ad altro contenuto ospitato in **docs.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="34f7f-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="34f7f-151">Non usare apici inversi, il grassetto o altro markup all'interno delle parentesi quadre di un collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="34f7f-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="34f7f-152">Per informazioni più dettagliate sui collegamenti, vedere [Uso di collegamenti nella documentazione](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="34f7f-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="34f7f-153">Nomi di file</span><span class="sxs-lookup"><span data-stu-id="34f7f-153">Filenames</span></span>

<span data-ttu-id="34f7f-154">Per i nomi di file usare le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="34f7f-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="34f7f-155">Includere solo lettere, numeri e trattini.</span><span class="sxs-lookup"><span data-stu-id="34f7f-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="34f7f-156">Non usare spazi o segni di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="34f7f-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="34f7f-157">Usare il trattino per separare le parole e i numeri nel nome del file.</span><span class="sxs-lookup"><span data-stu-id="34f7f-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="34f7f-158">Usare verbi di azione specifici, ad esempio sviluppare, acquistare, compilare, risolvere.</span><span class="sxs-lookup"><span data-stu-id="34f7f-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="34f7f-159">Non usare parole al gerundio.</span><span class="sxs-lookup"><span data-stu-id="34f7f-159">No -ing words.</span></span>
- <span data-ttu-id="34f7f-160">Non usare parole estremamente brevi, ad esempio "un", "e", "il", "in", "o" e così via.</span><span class="sxs-lookup"><span data-stu-id="34f7f-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="34f7f-161">Usare il formato Markdown e l'estensione file md.</span><span class="sxs-lookup"><span data-stu-id="34f7f-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="34f7f-162">Usare nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="34f7f-162">Keep file names reasonably short.</span></span> <span data-ttu-id="34f7f-163">I nomi vengono inclusi nell'URL dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="34f7f-164">Righe vuote, spazi e tabulazioni</span><span class="sxs-lookup"><span data-stu-id="34f7f-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="34f7f-165">Rimuovere le righe vuote duplicate.</span><span class="sxs-lookup"><span data-stu-id="34f7f-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="34f7f-166">Più righe vuote vengono sottoposte a rendering come una singola riga vuota in HTML, quindi più righe vuote non hanno alcuno scopo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="34f7f-167">Le righe vuote segnalano anche la fine di un blocco in Markdown.</span><span class="sxs-lookup"><span data-stu-id="34f7f-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="34f7f-168">Deve esserci una sola riga vuota tra blocchi Markdown di tipi diversi, ad esempio tra un paragrafo e un elenco o un'intestazione.</span><span class="sxs-lookup"><span data-stu-id="34f7f-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="34f7f-169">La spaziatura è significativa in Markdown.</span><span class="sxs-lookup"><span data-stu-id="34f7f-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="34f7f-170">Usa sempre gli spazi anziché tabulazioni fisse.</span><span class="sxs-lookup"><span data-stu-id="34f7f-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="34f7f-171">Rimuovere gli spazi superflui alla fine delle righe.</span><span class="sxs-lookup"><span data-stu-id="34f7f-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="34f7f-172">Titoli e intestazioni</span><span class="sxs-lookup"><span data-stu-id="34f7f-172">Titles and headings</span></span>

<span data-ttu-id="34f7f-173">Usare solo [intestazioni ATX][atx] (intestazioni in stile #, anziché `=` o `-`).</span><span class="sxs-lookup"><span data-stu-id="34f7f-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="34f7f-174">Scrivere in lettere maiuscole solo i nomi propri e la prima lettera di un titolo o di un'intestazione</span><span class="sxs-lookup"><span data-stu-id="34f7f-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="34f7f-175">Deve esserci un solo spazio tra `#` e la prima lettera dell'intestazione</span><span class="sxs-lookup"><span data-stu-id="34f7f-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="34f7f-176">Le intestazioni devono essere circondate da una sola riga vuota</span><span class="sxs-lookup"><span data-stu-id="34f7f-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="34f7f-177">È consentita una sola intestazione H1 per documento</span><span class="sxs-lookup"><span data-stu-id="34f7f-177">Only one H1 per document</span></span>
- <span data-ttu-id="34f7f-178">I livelli di intestazione devono essere incrementati di uno, non saltare livelli</span><span class="sxs-lookup"><span data-stu-id="34f7f-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="34f7f-179">Non usare apici inversi, il grassetto o altro markup nelle intestazioni</span><span class="sxs-lookup"><span data-stu-id="34f7f-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="34f7f-180">Lo schema applicato da [PlatyPS][platyPS] per le informazioni di riferimento sui cmdlet richiede intestazioni H2 e H3 specifiche.</span><span class="sxs-lookup"><span data-stu-id="34f7f-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="34f7f-181">L'aggiunta o la rimozione di intestazioni può interrompere la compilazione.</span><span class="sxs-lookup"><span data-stu-id="34f7f-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="34f7f-182">Per altre informazioni, vedere la [guida di stile per le informazioni di riferimento sui cmdlet](powershell-style-reference.md).</span><span class="sxs-lookup"><span data-stu-id="34f7f-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="34f7f-183">Limitare la lunghezza delle righe a 100 caratteri</span><span class="sxs-lookup"><span data-stu-id="34f7f-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="34f7f-184">Questo semplifica l'output da riga di comando per diff e cronologia.</span><span class="sxs-lookup"><span data-stu-id="34f7f-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="34f7f-185">Questa regola non è stata applicata per gran parte del contenuto esistente in PowerShell-Docs, ma l'obiettivo è aggiornare il contenuto corrispondentemente nel tempo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="34f7f-186">Qualsiasi aiuto è il benvenuto. L'[estensione Reflow Markdown][reflow] in Visual Studio Code (VSCode) semplifica la riformattazione dei paragrafi in base a questo limite.</span><span class="sxs-lookup"><span data-stu-id="34f7f-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="34f7f-187">Elenchi</span><span class="sxs-lookup"><span data-stu-id="34f7f-187">Lists</span></span>

<span data-ttu-id="34f7f-188">Se l'elenco contiene più frasi o paragrafi, prendere in considerazione l'uso di un'intestazione di livello inferiore anziché di un elenco.</span><span class="sxs-lookup"><span data-stu-id="34f7f-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="34f7f-189">L'elenco deve essere circondato da una singola riga vuota.</span><span class="sxs-lookup"><span data-stu-id="34f7f-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="34f7f-190">Elenchi non ordinati</span><span class="sxs-lookup"><span data-stu-id="34f7f-190">Unordered lists</span></span>

<span data-ttu-id="34f7f-191">Non terminare gli elementi degli elenchi con un punto a meno che non contengano più frasi.</span><span class="sxs-lookup"><span data-stu-id="34f7f-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="34f7f-192">Usare il segno meno (`-`) per i punti elenco negli elenchi.</span><span class="sxs-lookup"><span data-stu-id="34f7f-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="34f7f-193">In questo modo si evita confusione con il markup per il grassetto o il corsivo che usa l'asterisco [`*`].</span><span class="sxs-lookup"><span data-stu-id="34f7f-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="34f7f-194">Per includere un paragrafo o altri elementi come elemento puntato, inserire un'interruzione di riga e allineare il rientro al primo carattere dopo il punto elenco.</span><span class="sxs-lookup"><span data-stu-id="34f7f-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="34f7f-195">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="34f7f-196">Questo è un elenco con sottoelementi di un elemento puntato.</span><span class="sxs-lookup"><span data-stu-id="34f7f-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="34f7f-197">Primo elemento puntato</span><span class="sxs-lookup"><span data-stu-id="34f7f-197">First bullet item</span></span>

  <span data-ttu-id="34f7f-198">Frase che spiega il primo punto elenco.</span><span class="sxs-lookup"><span data-stu-id="34f7f-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="34f7f-199">Sottoelemento puntato</span><span class="sxs-lookup"><span data-stu-id="34f7f-199">Sub-bullet item</span></span>

    <span data-ttu-id="34f7f-200">Frase che spiega il punto elenco secondario.</span><span class="sxs-lookup"><span data-stu-id="34f7f-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="34f7f-201">Secondo elemento puntato</span><span class="sxs-lookup"><span data-stu-id="34f7f-201">Second bullet item</span></span>
- <span data-ttu-id="34f7f-202">Terzo elemento puntato</span><span class="sxs-lookup"><span data-stu-id="34f7f-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="34f7f-203">Elenchi ordinati</span><span class="sxs-lookup"><span data-stu-id="34f7f-203">Ordered lists</span></span>

<span data-ttu-id="34f7f-204">Per includere un paragrafo o altri elementi sotto un elemento numerato, allineare il rientro al primo carattere dopo il numero dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="34f7f-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

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

<span data-ttu-id="34f7f-205">per ottenere questo output:</span><span class="sxs-lookup"><span data-stu-id="34f7f-205">to get this output:</span></span>

> 1. <span data-ttu-id="34f7f-206">Per il primo elemento, inserire un singolo spazio dopo 1.</span><span class="sxs-lookup"><span data-stu-id="34f7f-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="34f7f-207">Le frasi lunghe devono essere mandate a capo alla riga successiva e devono essere allineate al primo carattere dopo l'indicatore di elenco numerato.</span><span class="sxs-lookup"><span data-stu-id="34f7f-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="34f7f-208">Per includere un secondo elemento (come questo), inserire un'interruzione di riga dopo il primo e allineare i rientri.</span><span class="sxs-lookup"><span data-stu-id="34f7f-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="34f7f-209">Il rientro del secondo elemento deve essere allineato al primo carattere dopo l'indicatore di elenco numerato.</span><span class="sxs-lookup"><span data-stu-id="34f7f-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="34f7f-210">Per gli elementi con cifra singola, come questo, viene applicato un rientro alla colonna 4.</span><span class="sxs-lookup"><span data-stu-id="34f7f-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="34f7f-211">Per gli elementi con due cifre, ad esempio l'elemento numero 10, applicare un rientro alla colonna 5.</span><span class="sxs-lookup"><span data-stu-id="34f7f-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="34f7f-212">Il successivo elemento numerato inizia qui.</span><span class="sxs-lookup"><span data-stu-id="34f7f-212">The next numbered item starts here.</span></span>

<span data-ttu-id="34f7f-213">Tutti gli elementi di un elenco numerato devono usare il numero `1.` anziché incrementare per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="34f7f-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="34f7f-214">Il rendering di Markdown incrementa automaticamente il valore.</span><span class="sxs-lookup"><span data-stu-id="34f7f-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="34f7f-215">In questo modo, il riordino degli elementi risulta più semplice e viene standardizzato il rientro del contenuto subordinato.</span><span class="sxs-lookup"><span data-stu-id="34f7f-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="34f7f-216">Formattazione degli elementi della sintassi dei comandi</span><span class="sxs-lookup"><span data-stu-id="34f7f-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="34f7f-217">Per i nomi dei cmdlet di PowerShell viene usata la [combinazione di maiuscole/minuscole Pascal][pascal-case].</span><span class="sxs-lookup"><span data-stu-id="34f7f-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="34f7f-218">I verbi sono separati dai sostantivi con un segno meno.</span><span class="sxs-lookup"><span data-stu-id="34f7f-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="34f7f-219">Usare sempre il nome con combinazione di maiuscole/minuscole Pascal completo per i cmdlet e i parametri.</span><span class="sxs-lookup"><span data-stu-id="34f7f-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="34f7f-220">Evitare l'uso di alias, se non per la presentazione specifica di un alias.</span><span class="sxs-lookup"><span data-stu-id="34f7f-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="34f7f-221">All'interno di un paragrafo, le parole chiave del linguaggio, i nomi dei cmdlet e i riferimenti alle variabili devono essere racchiusi tra caratteri di apice inverso (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="34f7f-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="34f7f-222">I nomi di proprietà, parametri e classi devono essere in **grassetto**.</span><span class="sxs-lookup"><span data-stu-id="34f7f-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="34f7f-223">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="34f7f-224">Quando si fa riferimento a un parametro in base al nome, il nome deve essere in **grassetto**.</span><span class="sxs-lookup"><span data-stu-id="34f7f-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="34f7f-225">Quando si illustra l'uso di un parametro con il prefisso segno meno, il parametro deve essere racchiuso tra caratteri di apice inverso.</span><span class="sxs-lookup"><span data-stu-id="34f7f-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="34f7f-226">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="34f7f-227">Quando si fa riferimento a comandi esterni (EXE, script e così via), il nome del comando deve essere in grassetto, tutto minuscolo (o con iniziale maiuscola se si trova all'inizio di una frase) e includere l'estensione di file appropriata.</span><span class="sxs-lookup"><span data-stu-id="34f7f-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="34f7f-228">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="34f7f-229">Quando si mostra un esempio di utilizzo di un comando esterno, l'esempio deve essere racchiuso tra caratteri di apice inverso.</span><span class="sxs-lookup"><span data-stu-id="34f7f-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="34f7f-230">In presenza di un conflitto di nomi con un alias, è necessario includere l'estensione del file nell'esempio del comando.</span><span class="sxs-lookup"><span data-stu-id="34f7f-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="34f7f-231">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="34f7f-232">Quando si scrive un articolo concettuale, anziché contenuto di riferimento, la prima istanza del nome di un cmdlet deve essere impostata come collegamento ipertestuale alla documentazione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f7f-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="34f7f-233">Non usare apici inversi, il grassetto o altro markup all'interno delle parentesi quadre di un collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="34f7f-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="34f7f-234">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="34f7f-235">Per altre informazioni, vedere la sezione [Collegamenti ipertestuali](#hyperlinks) della guida di stile.</span><span class="sxs-lookup"><span data-stu-id="34f7f-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="34f7f-236">Immagini</span><span class="sxs-lookup"><span data-stu-id="34f7f-236">Images</span></span>

<span data-ttu-id="34f7f-237">La sintassi per l'inclusione di un'immagine è la seguente:</span><span class="sxs-lookup"><span data-stu-id="34f7f-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="34f7f-238">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34f7f-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="34f7f-239">Dove `alt text` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine.</span><span class="sxs-lookup"><span data-stu-id="34f7f-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="34f7f-240">Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="34f7f-241">È anche utile in presenza di un bug nel sito a causa del quale non è possibile eseguire il rendering dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="34f7f-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="34f7f-242">Le immagini devono essere archiviate in una cartella `media/<article-name>` all'interno della cartella che contiene l'articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="34f7f-243">Le immagini non devono essere condivise tra gli articoli.</span><span class="sxs-lookup"><span data-stu-id="34f7f-243">Images should not be shared between articles.</span></span> <span data-ttu-id="34f7f-244">Creare una cartella corrispondente al nome del file dell'articolo nella cartella `media`.</span><span class="sxs-lookup"><span data-stu-id="34f7f-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="34f7f-245">Copiare le immagini per tale articolo nella nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="34f7f-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="34f7f-246">Se un'immagine viene usata da più articoli, ogni cartella di immagini deve avere una copia del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="34f7f-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="34f7f-247">Questa procedura impedisce che la modifica di un'immagine in un articolo abbia effetti su un altro articolo.</span><span class="sxs-lookup"><span data-stu-id="34f7f-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="34f7f-248">In alcuni casi, è necessario condividere immagini, ad esempio logo e icone, in più articoli.</span><span class="sxs-lookup"><span data-stu-id="34f7f-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="34f7f-249">Queste immagini vengono archiviate nella cartella `/media/shared` nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="34f7f-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="34f7f-250">Sono supportati i tipi di file di immagine seguenti: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span><span class="sxs-lookup"><span data-stu-id="34f7f-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
