---
title: Modello e foglio informativo per gli articoli .NET
description: Questo articolo contiene un pratico modello da usare per creare nuovi articoli per i repository di documentazione .NET.
ms.date: 11/07/2018
ms.openlocfilehash: 9b57abd96093940c96f90a4a01b9f81eae063ffb
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653621"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="9132a-103">Modello di metadati e Markdown per i documenti .NET</span><span class="sxs-lookup"><span data-stu-id="9132a-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="9132a-104">Questo modello dotnet/docs contiene esempi di sintassi Markdown e indicazioni per l'impostazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="9132a-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="9132a-105">Per creare un file Markdown, copiare in un nuovo file il modello incluso, completare i metadati come specificato di seguito e impostare l'intestazione H1 per il titolo dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="9132a-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="9132a-106">Metadati</span><span class="sxs-lookup"><span data-stu-id="9132a-106">Metadata</span></span>

<span data-ttu-id="9132a-107">Il blocco di metadati necessario si trova nel seguente blocco di metadati di esempio:</span><span class="sxs-lookup"><span data-stu-id="9132a-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="9132a-108">Tra i due punti (:) e il valore di un elemento di metadati **deve** essere presente uno spazio.</span><span class="sxs-lookup"><span data-stu-id="9132a-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="9132a-109">I due punti in un valore (ad esempio in un titolo) interrompono l'esecuzione del parser di metadati.</span><span class="sxs-lookup"><span data-stu-id="9132a-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="9132a-110">In questo caso, racchiudere il titolo tra virgolette doppie (ad esempio `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="9132a-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="9132a-111">**title**: appare nei risultati dei motori di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9132a-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="9132a-112">Il titolo non deve essere identico al titolo incluso nell'intestazione H1 e non può contenere più di 60 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9132a-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="9132a-113">**description**: riepiloga il contenuto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="9132a-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="9132a-114">In genere viene visualizzato nella pagina dei risultati della ricerca ma non viene utilizzato per classificare i risultati.</span><span class="sxs-lookup"><span data-stu-id="9132a-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="9132a-115">La lunghezza deve essere inclusa tra 115 e 145 caratteri, spazi inclusi.</span><span class="sxs-lookup"><span data-stu-id="9132a-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="9132a-116">**author**: deve contenere il **nome utente GitHub** dell'autore.</span><span class="sxs-lookup"><span data-stu-id="9132a-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="9132a-117">**ms.date**: data dell'ultimo aggiornamento significativo.</span><span class="sxs-lookup"><span data-stu-id="9132a-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="9132a-118">Aggiornare questo valore negli articoli esistenti se è stata eseguita una revisione e un aggiornamento dell'intero articolo.</span><span class="sxs-lookup"><span data-stu-id="9132a-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="9132a-119">Per aggiornamenti minori, quali correzioni ortografiche o simili, non è necessario aggiornare il valore.</span><span class="sxs-lookup"><span data-stu-id="9132a-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="9132a-120">A ogni articolo sono associati altri metadati, ma in generale la maggior parte dei metadati viene applicata a livello della cartella e specificata in **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="9132a-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="9132a-121">Nozioni di base su Markdown, GFM e caratteri speciali</span><span class="sxs-lookup"><span data-stu-id="9132a-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="9132a-122">Per le nozioni di base su Markdown, GitHub Flavored Markdown (GFM) e sulle estensioni specifiche di OPS, vedere gli articoli generali [Markdown](how-to-write-use-markdown.md) e [Informazioni di riferimento su Markdown per OPS](markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9132a-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="9132a-123">Markdown usa caratteri speciali per la formattazione, quali \*, \` e \#.</span><span class="sxs-lookup"><span data-stu-id="9132a-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="9132a-124">Se si vuole includere uno di questi caratteri nel contenuto, seguire una di queste due procedure:</span><span class="sxs-lookup"><span data-stu-id="9132a-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="9132a-125">Far precedere una barra rovesciata al carattere speciale come "escape" (ad esempio `\*` per \*)</span><span class="sxs-lookup"><span data-stu-id="9132a-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="9132a-126">Usare il [codice entità HTML](http://www.ascii.cl/htmlcodes.htm) per il carattere (ad esempio `&#42;` per &#42;).</span><span class="sxs-lookup"><span data-stu-id="9132a-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="9132a-127">Nomi di file</span><span class="sxs-lookup"><span data-stu-id="9132a-127">File names</span></span>

<span data-ttu-id="9132a-128">Per i nomi di file sono valide le seguenti regole:</span><span class="sxs-lookup"><span data-stu-id="9132a-128">File names use the following rules:</span></span>

* <span data-ttu-id="9132a-129">Contengono solo lettere minuscole, numeri e trattini.</span><span class="sxs-lookup"><span data-stu-id="9132a-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="9132a-130">Non usare spazi o segni di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="9132a-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="9132a-131">Usare il trattino per separare le parole e i numeri nel nome del file.</span><span class="sxs-lookup"><span data-stu-id="9132a-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="9132a-132">Usare verbi di azione specifici, ad esempio sviluppare, acquistare, compilare, risolvere.</span><span class="sxs-lookup"><span data-stu-id="9132a-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="9132a-133">Non usare parole al gerundio.</span><span class="sxs-lookup"><span data-stu-id="9132a-133">No -ing words.</span></span>
* <span data-ttu-id="9132a-134">Non usare parole estremamente brevi, ad esempio "un", "e", "il", "in", "o" e così via.</span><span class="sxs-lookup"><span data-stu-id="9132a-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="9132a-135">Usare il formato Markdown e l'estensione file md.</span><span class="sxs-lookup"><span data-stu-id="9132a-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="9132a-136">Usare nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="9132a-136">Keep file names reasonably short.</span></span> <span data-ttu-id="9132a-137">I nomi vengono inclusi nell'URL dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="9132a-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="9132a-138">Titoli</span><span class="sxs-lookup"><span data-stu-id="9132a-138">Headings</span></span>

<span data-ttu-id="9132a-139">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="9132a-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="9132a-140">Usare sempre la maiuscola per la prima parola di un titolo.</span><span class="sxs-lookup"><span data-stu-id="9132a-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="9132a-141">Stile del testo</span><span class="sxs-lookup"><span data-stu-id="9132a-141">Text styling</span></span>

<span data-ttu-id="9132a-142">*Corsivo*: usarlo per file, cartelle, percorsi (per elementi lunghi, suddivisi sulla stessa riga), termini nuovi.</span><span class="sxs-lookup"><span data-stu-id="9132a-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="9132a-143">**Grassetto**: usarlo per elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9132a-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="9132a-144">`Code`: usarlo per il codice inline, le parole chiave del linguaggio, i nomi di pacchetti NuGet, i comandi della riga di comando, i nomi di tabella e colonna del database e gli URL sui quali non è possibile fare clic.</span><span class="sxs-lookup"><span data-stu-id="9132a-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="9132a-145">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="9132a-145">Links</span></span>

<span data-ttu-id="9132a-146">Vedere l'articolo generale [Collegamenti](how-to-write-links.md) per informazioni su ancoraggi, collegamenti interni, collegamenti ad altri documenti, inclusioni di codice e collegamenti esterni.</span><span class="sxs-lookup"><span data-stu-id="9132a-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="9132a-147">Il team di documentazione di .NET utilizza le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9132a-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="9132a-148">Nella maggior parte dei casi si usano collegamenti relativi e si sconsiglia l'uso di `~/` nei collegamenti, perché i collegamenti relativi vengono risolti nell'origine in GitHub.</span><span class="sxs-lookup"><span data-stu-id="9132a-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="9132a-149">Tuttavia quando si definisce il collegamento a un file in un repository dipendente, viene usato il carattere `~/` per fornire il percorso.</span><span class="sxs-lookup"><span data-stu-id="9132a-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="9132a-150">Dato che i file nel repository dipendente si trovano in una posizione diversa in GitHub, i collegamenti non vengono risolti correttamente con collegamenti relativi, indipendentemente da come sono stati scritti.</span><span class="sxs-lookup"><span data-stu-id="9132a-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="9132a-151">La specifica del linguaggio C# e la specifica del linguaggio Visual Basic sono incluse nei documenti .NET mediante l'aggiunta dell'origine dai repository del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9132a-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="9132a-152">Le origini di markdown vengono gestite nei repository [csharplang](https://github.com/dotnet/csharplang) e [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="9132a-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="9132a-153">I collegamenti a una specifica devono fare riferimento alle directory di origine che includono le specifiche corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="9132a-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="9132a-154">Per C# la directory è **~/_csharplang/spec** e per VB la directory è **~/_vblang/spec** come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9132a-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="9132a-155">Collegamenti alle API</span><span class="sxs-lookup"><span data-stu-id="9132a-155">Links to APIs</span></span>

<span data-ttu-id="9132a-156">Il sistema di build dispone di estensioni che consentono il collegamento alle API .NET senza dover ricorrere a collegamenti esterni.</span><span class="sxs-lookup"><span data-stu-id="9132a-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="9132a-157">Si usa una delle sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9132a-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="9132a-158">Collegamento automatico: `<xref:UID>` o `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="9132a-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="9132a-159">Il parametro di query `displayProperty` produce un testo del collegamento completo.</span><span class="sxs-lookup"><span data-stu-id="9132a-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="9132a-160">Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo.</span><span class="sxs-lookup"><span data-stu-id="9132a-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="9132a-161">Collegamento Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="9132a-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="9132a-162">Può essere usato quando si vuole personalizzare il testo del collegamento visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9132a-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="9132a-163">Esempi:</span><span class="sxs-lookup"><span data-stu-id="9132a-163">Examples:</span></span>

- <span data-ttu-id="9132a-164">`<xref:System.String>` viene visualizzato come [String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9132a-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="9132a-165">`<xref:System.String?displayProperty=nameWithType>` viene visualizzato come [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9132a-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="9132a-166">`[String class](xref:System.String)` viene visualizzato come [String class](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9132a-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="9132a-167">Per altre informazioni sull'uso di questa notazione, vedere [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Uso del riferimento incrociato).</span><span class="sxs-lookup"><span data-stu-id="9132a-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="9132a-168">Se uno o più UID contengono i caratteri speciali \`, \# o \*, il valore dell'UID deve essere con codifica HTML come `%60`, `%23` e `%2A` rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="9132a-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="9132a-169">A volte sono presenti parentesi con codifica, ma questo non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="9132a-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="9132a-170">Esempi:</span><span class="sxs-lookup"><span data-stu-id="9132a-170">Examples:</span></span>

- <span data-ttu-id="9132a-171">System.Threading.Tasks.Task\`1 diventa `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="9132a-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="9132a-172">System.Exception.\#ctor diventa `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="9132a-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="9132a-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) diventa `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="9132a-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="9132a-174">È possibile trovare gli UID dei tipi, un elenco di overload di membro o un membro in overload specifico in `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="9132a-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="9132a-175">La stringa di query `?text=*\<type-member-name>*` identifica il tipo o il membro di cui si vogliono visualizzare gli UID.</span><span class="sxs-lookup"><span data-stu-id="9132a-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="9132a-176">Ad esempio, `https://xref.docs.microsoft.com/autocomplete?text=string.format` recupera gli overload di [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format).</span><span class="sxs-lookup"><span data-stu-id="9132a-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="9132a-177">Lo strumento cerca il parametro query `text` fornito in qualsiasi parte dell'UID.</span><span class="sxs-lookup"><span data-stu-id="9132a-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="9132a-178">Ad esempio è possibile cercare il nome membro (ToString), il nome membro parziale (ToStri), il tipo e il nome membro (Double.ToString) e così via.</span><span class="sxs-lookup"><span data-stu-id="9132a-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="9132a-179">Se si aggiunge \* (o `%2A`) dopo l'UID, il collegamento rappresenta la pagina di overload e non un'API specifica.</span><span class="sxs-lookup"><span data-stu-id="9132a-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="9132a-180">È ad esempio possibile usare questa opzione per creare un collegamento alla pagina [Metodo List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) in modo generico anziché un overload specifico come [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="9132a-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="9132a-181">È anche possibile usare \* per il collegamento a una pagina membro quando il membro non è in overload; in tal modo è possibile evitare di includere l'elenco parametri nell'UID.</span><span class="sxs-lookup"><span data-stu-id="9132a-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="9132a-182">Per il collegamento all'overload di un metodo specifico, è necessario includere il nome del tipo completo di ciascun parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="9132a-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="9132a-183">Ad esempio, \<xref:System.DateTime.ToString> definisce il collegamento al metodo senza parametri [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), mentre \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> definisce il collegamento al metodo [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="9132a-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="9132a-184">Per il collegamento a un tipo generico, ad esempio [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), usare il carattere \` (`%60`) seguito dal numero dei parametri di tipo generico.</span><span class="sxs-lookup"><span data-stu-id="9132a-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="9132a-185">Ad esempio `<xref:System.Nullable%601>` definisce il collegamento al tipo [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), mentre `<xref:System.Func%602>` definisce il collegamento al delegato [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="9132a-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="9132a-186">Codice</span><span class="sxs-lookup"><span data-stu-id="9132a-186">Code</span></span>

<span data-ttu-id="9132a-187">Il miglior metodo per includere codice è l'inclusione di frammenti di codice da un esempio funzionante.</span><span class="sxs-lookup"><span data-stu-id="9132a-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="9132a-188">Creare l'esempio in base alle istruzioni fornite nell'articolo [Contributing to .NET docs](dotnet-contribute-process.md#contributing-to-samples) (Contributo ai documenti .NET).</span><span class="sxs-lookup"><span data-stu-id="9132a-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="9132a-189">Le regole di base per l'inclusione di codice si trovano nelle indicazioni generali per il [codice](how-to-write-use-markdown.md#code-snippets).</span><span class="sxs-lookup"><span data-stu-id="9132a-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="9132a-190">È possibile includere il codice usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="9132a-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="9132a-191">`-<language>` (*facoltativo* ma *consigliato*)</span><span class="sxs-lookup"><span data-stu-id="9132a-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="9132a-192">Linguaggio del frammento di codice al quale si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="9132a-192">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="9132a-193">`<name>` (*facoltativo*)</span><span class="sxs-lookup"><span data-stu-id="9132a-193">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="9132a-194">Nome del frammento di codice.</span><span class="sxs-lookup"><span data-stu-id="9132a-194">Name for the code snippet.</span></span> <span data-ttu-id="9132a-195">Non deve avere alcun impatto sul file HTML di output ma può essere usato per rendere più leggibile l'origine del Markdown.</span><span class="sxs-lookup"><span data-stu-id="9132a-195">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="9132a-196">`<pathToFile>` (*obbligatorio*)</span><span class="sxs-lookup"><span data-stu-id="9132a-196">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="9132a-197">Percorso relativo nel file system che indica il file del frammento di codice a cui fare riferimento.</span><span class="sxs-lookup"><span data-stu-id="9132a-197">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="9132a-198">Questa notazione può essere complicata dai vari repository che costituiscono il set di documentazione di .NET.</span><span class="sxs-lookup"><span data-stu-id="9132a-198">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="9132a-199">I campioni .NET si trovano nel repository dotnet/samples.</span><span class="sxs-lookup"><span data-stu-id="9132a-199">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="9132a-200">Tutti i percorsi di frammenti iniziano con `~/samples` e la parte rimanente indica il percorso all'origine dalla radice del repository.</span><span class="sxs-lookup"><span data-stu-id="9132a-200">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="9132a-201">`<queryoption>` (*facoltativo*)</span><span class="sxs-lookup"><span data-stu-id="9132a-201">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="9132a-202">Usato per specificare come il codice deve essere recuperato dal file:</span><span class="sxs-lookup"><span data-stu-id="9132a-202">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="9132a-203">`#`: `#{tagname}` (nome del tag) *o* `#L{startlinenumber}-L{endlinenumber}` (intervallo di righe).</span><span class="sxs-lookup"><span data-stu-id="9132a-203">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="9132a-204">L'uso dei numeri di riga è sconsigliato in quanto non sufficientemente affidabile.</span><span class="sxs-lookup"><span data-stu-id="9132a-204">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="9132a-205">Il nome tag è il metodo preferibile per il riferimento ai frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="9132a-205">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="9132a-206">Usare nomi tag significativi.</span><span class="sxs-lookup"><span data-stu-id="9132a-206">Use meaningful tag names.</span></span> <span data-ttu-id="9132a-207">Molti frammenti sono stati sottoposti a migrazione da una piattaforma precedente e i tag hanno nomi come `Snippet1`, `Snippet2` e così via. Questa prassi è più difficile da gestire.</span><span class="sxs-lookup"><span data-stu-id="9132a-207">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="9132a-208">`range`: `?range=1,3-5` Intervallo di righe.</span><span class="sxs-lookup"><span data-stu-id="9132a-208">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="9132a-209">Questo esempio include le righe 1, 3, 4 e 5.</span><span class="sxs-lookup"><span data-stu-id="9132a-209">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="9132a-210">Se possibile, è sempre consigliabile usare l'opzione del nome del tag.</span><span class="sxs-lookup"><span data-stu-id="9132a-210">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="9132a-211">Il nome tag è il nome di un'area o di un commento di codice nel formato di `Snippettagname` presente nel codice di origine.</span><span class="sxs-lookup"><span data-stu-id="9132a-211">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="9132a-212">L'esempio seguente illustra come creare il riferimento al nome tag `BasicThrow`:</span><span class="sxs-lookup"><span data-stu-id="9132a-212">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="9132a-213">Il percorso relativo dell'origine nel repository **dotnet/samples** segue il percorso `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="9132a-213">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="9132a-214">È anche possibile vedere come sono strutturati i tag dei frammenti di codice in [questo file di origine](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span><span class="sxs-lookup"><span data-stu-id="9132a-214">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="9132a-215">Per altri dettagli sulla rappresentazione dei nomi di tag nei file di origine dei frammenti di codice in base al linguaggio, vedere le [linee guida per DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="9132a-215">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="9132a-216">L'esempio seguente mostra il codice incluso in tutti e tre i linguaggi .NET:</span><span class="sxs-lookup"><span data-stu-id="9132a-216">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="9132a-217">L'inclusione di frammenti da programmi completi garantisce che tutto il codice sia conforme al sistema di integrazione continua (CI).</span><span class="sxs-lookup"><span data-stu-id="9132a-217">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="9132a-218">Se tuttavia è necessario visualizzare un elemento che provoca errori di compilazione o di runtime, è possibile usare i blocchi di codice inline.</span><span class="sxs-lookup"><span data-stu-id="9132a-218">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="9132a-219">Immagini</span><span class="sxs-lookup"><span data-stu-id="9132a-219">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="9132a-220">Immagine statica o GIF animata</span><span class="sxs-lookup"><span data-stu-id="9132a-220">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="9132a-221">Immagine collegata</span><span class="sxs-lookup"><span data-stu-id="9132a-221">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="9132a-222">Video</span><span class="sxs-lookup"><span data-stu-id="9132a-222">Videos</span></span>

<span data-ttu-id="9132a-223">Attualmente è possibile incorporare video sia di Channel 9 che di YouTube con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="9132a-223">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="9132a-224">Channel 9</span><span class="sxs-lookup"><span data-stu-id="9132a-224">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="9132a-225">Per ottenere l'URL corretto del video, selezionare la scheda **Incorpora** sotto il fotogramma video e copiare l'URL dall'elemento `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="9132a-225">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="9132a-226">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9132a-226">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="9132a-227">YouTube</span><span class="sxs-lookup"><span data-stu-id="9132a-227">YouTube</span></span>

<span data-ttu-id="9132a-228">Per ottenere l'URL corretto del video, fare clic con il pulsante destro del mouse sul video, selezionare **Copia codice di incorporamento** e copiare l'URL dall'elemento `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="9132a-228">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="9132a-229">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9132a-229">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="9132a-230">Estensioni docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="9132a-230">docs.microsoft extensions</span></span>

<span data-ttu-id="9132a-231">docs.microsoft include alcune estensioni aggiuntive in GitHub Flavored Markdown.</span><span class="sxs-lookup"><span data-stu-id="9132a-231">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="9132a-232">Elenchi con segni di spunta</span><span class="sxs-lookup"><span data-stu-id="9132a-232">Checked lists</span></span>

<span data-ttu-id="9132a-233">Per gli elenchi è disponibile uno stile personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9132a-233">A custom style is available for lists.</span></span> <span data-ttu-id="9132a-234">È possibile contrassegnare gli elenchi con segni di spunta verdi.</span><span class="sxs-lookup"><span data-stu-id="9132a-234">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="9132a-235">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="9132a-235">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="9132a-236">Come creare un'app .NET Core</span><span class="sxs-lookup"><span data-stu-id="9132a-236">How to create a .NET Core app</span></span>
> * <span data-ttu-id="9132a-237">Come aggiungere un riferimento al pacchetto Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="9132a-237">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="9132a-238">Come modificare MyApp.csproj per aggiungere dipendenze</span><span class="sxs-lookup"><span data-stu-id="9132a-238">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="9132a-239">Come aggiungere una classe e un elemento XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="9132a-239">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="9132a-240">Come compilare ed eseguire l'applicazione</span><span class="sxs-lookup"><span data-stu-id="9132a-240">How to build and run the application</span></span>

<span data-ttu-id="9132a-241">Per un esempio di elenchi con segni di spunta, vedere la [documentazione di .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="9132a-241">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="9132a-242">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="9132a-242">Buttons</span></span>

<span data-ttu-id="9132a-243">Collegamenti ai pulsanti:</span><span class="sxs-lookup"><span data-stu-id="9132a-243">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="9132a-244">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="9132a-244">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="9132a-245">button links</span><span class="sxs-lookup"><span data-stu-id="9132a-245">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="9132a-246">Per un esempio di pulsanti attivi, vedere la [documentazione di Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="9132a-246">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="9132a-247">Guide dettagliate</span><span class="sxs-lookup"><span data-stu-id="9132a-247">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="9132a-248">Per un esempio di guide dettagliate attive, vedere la [Guida di C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="9132a-248">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
