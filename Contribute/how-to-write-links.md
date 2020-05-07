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
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624793"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="35e01-103">Usare collegamenti nella documentazione</span><span class="sxs-lookup"><span data-stu-id="35e01-103">Use links in documentation</span></span>

<span data-ttu-id="35e01-104">Questo articolo descrive come usare collegamenti ipertestuali da pagine ospitate in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="35e01-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="35e01-105">È facile aggiungere collegamenti all'interno di markdown, con alcune convenzioni.</span><span class="sxs-lookup"><span data-stu-id="35e01-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="35e01-106">I collegamenti possono indirizzare gli utenti a contenuto all'interno della stessa pagina, in altre pagine vicine o in siti e URL esterni.</span><span class="sxs-lookup"><span data-stu-id="35e01-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="35e01-107">Il back-end del sito docs.microsoft.com usa i servizi OPS (Open Publishing Service) che supportano il Markdown conforme a [CommonMark][] analizzato tramite il motore di analisi [Markdig][].</span><span class="sxs-lookup"><span data-stu-id="35e01-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="35e01-108">Questa versione di Markdown è per lo più compatibile con [GitHub Flavored Markdown (GFM)][GFM], perché la maggior parte dei documenti viene archiviata in GitHub dove può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="35e01-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="35e01-109">Altre funzionalità vengono aggiunte tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="35e01-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35e01-110">Tutti i collegamenti devono essere protetti (`https` invece di `http`) ogni volta che la destinazione lo supporta (come dovrebbe essere nella maggior parte dei casi).</span><span class="sxs-lookup"><span data-stu-id="35e01-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="35e01-111">Testo del collegamento</span><span class="sxs-lookup"><span data-stu-id="35e01-111">Link text</span></span>

<span data-ttu-id="35e01-112">Le parole che vengono incluse nel testo del collegamento devono essere semplici.</span><span class="sxs-lookup"><span data-stu-id="35e01-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="35e01-113">Devono quindi essere parole normali o il titolo della pagina alla quale porta il collegamento.</span><span class="sxs-lookup"><span data-stu-id="35e01-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35e01-114">Non usare "fare clic qui".</span><span class="sxs-lookup"><span data-stu-id="35e01-114">Do not use "click here."</span></span> <span data-ttu-id="35e01-115">È una scelta inefficace per l'ottimizzazione dei motori di ricerca e non descrive adeguatamente la destinazione.</span><span class="sxs-lookup"><span data-stu-id="35e01-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="35e01-116">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="35e01-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="35e01-117">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="35e01-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="35e01-118">Collegamenti da un articolo a un altro</span><span class="sxs-lookup"><span data-stu-id="35e01-118">Links from one article to another</span></span>

<span data-ttu-id="35e01-119">Il sistema di pubblicazione supporta due tipi di collegamenti ipertestuali: **URL** e **collegamenti a file**.</span><span class="sxs-lookup"><span data-stu-id="35e01-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="35e01-120">Un collegamento di tipo URL può essere un percorso URL relativo alla radice di docs.microsoft.com o un URL assoluto che include la sintassi completa dell'URL, ad esempio `https://github.com/MicrosoftDocs/PowerShell-Docs`.</span><span class="sxs-lookup"><span data-stu-id="35e01-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="35e01-121">Usare collegamenti URL quando si crea un collegamento a contenuto al di fuori del _docset_ corrente o tra un riferimento generato automaticamente e articoli concettuali all'interno del docset.</span><span class="sxs-lookup"><span data-stu-id="35e01-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="35e01-122">Il modo più semplice per creare un collegamento relativo consiste nel copiare l'URL dal browser e quindi nel rimuovere `https://docs.microsoft.com/en-us` dal valore incollato nel codice Markdown.</span><span class="sxs-lookup"><span data-stu-id="35e01-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="35e01-123">Non includere le impostazioni locali presenti negli URL per le proprietà Microsoft (ad esempio, rimuovere "/en-us" dall'URL).</span><span class="sxs-lookup"><span data-stu-id="35e01-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="35e01-124">Un collegamento a file viene usato per collegare un articolo a un altro all'interno del docset.</span><span class="sxs-lookup"><span data-stu-id="35e01-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="35e01-125">Tutti i percorsi di file usano caratteri barra (`/`) anziché caratteri barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="35e01-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="35e01-126">Un articolo si collega a un altro articolo nella stessa directory:</span><span class="sxs-lookup"><span data-stu-id="35e01-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="35e01-127">Un articolo si collega a un articolo nella directory padre della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="35e01-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="35e01-128">Un articolo si collega a un articolo in una sottodirectory della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="35e01-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="35e01-129">Un articolo si collega a un articolo in una sottodirectory della directory padre della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="35e01-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="35e01-130">Nessuno degli esempi precedenti usa `~/` come parte del collegamento.</span><span class="sxs-lookup"><span data-stu-id="35e01-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="35e01-131">Per creare un collegamento a un percorso assoluto che inizia dalla radice del repository, iniziare il collegamento con `/`.</span><span class="sxs-lookup"><span data-stu-id="35e01-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="35e01-132">Quando ci si sposta nei repository di origine in GitHub, l'inserimento di `~/` genera collegamenti non validi.</span><span class="sxs-lookup"><span data-stu-id="35e01-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="35e01-133">Iniziare il percorso con `/` risolve correttamente il problema.</span><span class="sxs-lookup"><span data-stu-id="35e01-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="35e01-134">Struttura dei collegamenti in docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="35e01-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="35e01-135">All'interno del contenuto pubblicato in docs.microsoft.com gli URL presentano la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="35e01-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="35e01-136">Esempi:</span><span class="sxs-lookup"><span data-stu-id="35e01-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="35e01-137">`<locale>` - Lingua dell'articolo (esempio: en-us o de-de)</span><span class="sxs-lookup"><span data-stu-id="35e01-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="35e01-138">`<product-service>` - Nome del prodotto o del servizio (esempio: powershell, dotnet o azure)</span><span class="sxs-lookup"><span data-stu-id="35e01-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="35e01-139">`[<feature-service>]` (facoltativo) - Nome della funzionalità o del servizio secondario del prodotto (esempio: csharp o load-balancer)</span><span class="sxs-lookup"><span data-stu-id="35e01-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="35e01-140">`[<subfolder>]` (facoltativo) - Nome di una sottocartella all'interno di una funzionalità</span><span class="sxs-lookup"><span data-stu-id="35e01-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="35e01-141">`<topic>` - Nome del file dell'articolo per l'argomento (esempio: load-balancer-overview o overview)</span><span class="sxs-lookup"><span data-stu-id="35e01-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="35e01-142">`[?view=\<view-name>]` (facoltativo) - Nome visualizzazione usato dal selettore della versione per contenuto con più versioni disponibili (esempio: azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="35e01-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="35e01-143">Nella maggior parte dei casi, gli articoli nello stesso _docset_ hanno lo stesso frammento `<product-service>` nell'URL.</span><span class="sxs-lookup"><span data-stu-id="35e01-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="35e01-144">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="35e01-144">For example:</span></span>
> - <span data-ttu-id="35e01-145">Stesso docset</span><span class="sxs-lookup"><span data-stu-id="35e01-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="35e01-146">Docset diverso</span><span class="sxs-lookup"><span data-stu-id="35e01-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="35e01-147">Collegamento segnalibro</span><span class="sxs-lookup"><span data-stu-id="35e01-147">Bookmark links</span></span>

<span data-ttu-id="35e01-148">Per un collegamento segnalibro a un'intestazione nel file *corrente*, usare un simbolo hash seguito dalle parole dell'intestazione in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="35e01-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="35e01-149">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini:</span><span class="sxs-lookup"><span data-stu-id="35e01-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="35e01-150">Per creare un collegamento a un'intestazione di segnalibro in un altro articolo, usare il collegamento relativo al file o al sito più un simbolo hash, seguito dalle parole dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="35e01-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="35e01-151">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini:</span><span class="sxs-lookup"><span data-stu-id="35e01-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="35e01-152">È anche possibile copiare il collegamento segnalibro dall'URL.</span><span class="sxs-lookup"><span data-stu-id="35e01-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="35e01-153">Per trovare l'URL, passare il puntatore del mouse sulla riga dell'intestazione in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="35e01-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="35e01-154">Verrà visualizzata un'icona di collegamento:</span><span class="sxs-lookup"><span data-stu-id="35e01-154">You should see a link icon appear:</span></span>

![Icona di collegamento nell'intestazione dell'articolo](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="35e01-156">Fare clic sull'icona di collegamento e quindi copiare il testo di ancoraggio del segnalibro dall'URL (ovvero, la parte dopo l'hash).</span><span class="sxs-lookup"><span data-stu-id="35e01-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="35e01-157">L'estensione Docs dispone anche di strumenti che facilitano la creazione di collegamenti.</span><span class="sxs-lookup"><span data-stu-id="35e01-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="35e01-158">Collegamenti di ancoraggio esplicito</span><span class="sxs-lookup"><span data-stu-id="35e01-158">Explicit anchor links</span></span>

<span data-ttu-id="35e01-159">L'aggiunta di collegamenti di ancoraggio esplicito che usano il tag HTML `<a>` non è necessaria né consigliata, tranne che nelle pagine hub e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="35e01-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="35e01-160">Usare invece i segnalibri generati automaticamente come descritto in [Collegamenti segnalibro](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="35e01-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="35e01-161">In caso di pagine hub e di destinazione, dichiarare ancoraggi come descritto di seguito:</span><span class="sxs-lookup"><span data-stu-id="35e01-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="35e01-162">oppure</span><span class="sxs-lookup"><span data-stu-id="35e01-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="35e01-163">E usare i comandi seguenti per collegarsi all'ancoraggio:</span><span class="sxs-lookup"><span data-stu-id="35e01-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="35e01-164">Il testo di ancoraggio deve sempre essere minuscolo e non deve contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="35e01-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="35e01-165">Collegamenti XRef (riferimenti incrociati)</span><span class="sxs-lookup"><span data-stu-id="35e01-165">XRef (cross reference) links</span></span>

<span data-ttu-id="35e01-166">I collegamenti XRef rappresentano il metodo consigliato per i collegamenti alle API, perché vengono convalidati in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="35e01-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="35e01-167">Per creare collegamenti a pagine di riferimento API generate automaticamente nel docset corrente o in altri docset, usare collegamenti XRef con l'ID univoco ([UID](#determine-the-uid)) del tipo di membro.</span><span class="sxs-lookup"><span data-stu-id="35e01-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="35e01-168">È possibile usare l'[estensione Docs Markdown per VS Code][docsextension] (inclusa nel Docs Authoring Pack) per inserire collegamenti XRref .NET da visualizzare nel [browser delle API .NET][].</span><span class="sxs-lookup"><span data-stu-id="35e01-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="35e01-169">Controllare se l'API a cui si vuole creare un collegamento si trova in [docs.microsoft.com][docs] digitando tutto o in parte il nome completo dell'API nella casella di ricerca del [browser delle API .NET][] o della [Windows UWP][].</span><span class="sxs-lookup"><span data-stu-id="35e01-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="35e01-170">Se non vengono visualizzati risultati, il tipo non è ancora disponibile in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="35e01-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="35e01-171">È possibile usare una delle sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="35e01-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="35e01-172">Collegamenti automatici:</span><span class="sxs-lookup"><span data-stu-id="35e01-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="35e01-173">Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo.</span><span class="sxs-lookup"><span data-stu-id="35e01-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="35e01-174">Il parametro di query `displayProperty=nameWithType` facoltativo produce testo di collegamento completo, ovvero **spazio dei nomi.tipo** per i tipi e **tipo.membro** per i membri dei tipi, inclusi i membri del tipo enumerazione.</span><span class="sxs-lookup"><span data-stu-id="35e01-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="35e01-175">Collegamenti in stile Markdown:</span><span class="sxs-lookup"><span data-stu-id="35e01-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="35e01-176">Usare collegamenti in stile Markdown per i collegamenti XRef quando si vuole personalizzare il testo del collegamento visualizzato.</span><span class="sxs-lookup"><span data-stu-id="35e01-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="35e01-177">Esempi:</span><span class="sxs-lookup"><span data-stu-id="35e01-177">Examples:</span></span>

- <span data-ttu-id="35e01-178">**\<xref:System.String>** viene visualizzato come <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="35e01-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="35e01-179">**\<xref:System.String?displayProperty=nameWithType>** viene visualizzato come <xref:System.String?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="35e01-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="35e01-180">**\[classe String](xref:System.String)** viene visualizzato come [classe String](xref:System.String).</span><span class="sxs-lookup"><span data-stu-id="35e01-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="35e01-181">Il parametro di query `displayProperty=fullName` funziona allo stesso modo di `displayProperty=nameWithType` per le classi.</span><span class="sxs-lookup"><span data-stu-id="35e01-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="35e01-182">In altre parole, il testo del collegamento diventa **spaziodeinomi.nomeclasse**.</span><span class="sxs-lookup"><span data-stu-id="35e01-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="35e01-183">Per i membri, tuttavia, il testo del collegamento viene visualizzato come **spaziodeinomi.nomeclasse.nomemembro**, che potrebbe non corrispondere al risultato voluto.</span><span class="sxs-lookup"><span data-stu-id="35e01-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="35e01-184">Gli UID fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="35e01-184">UIDs are case sensitive.</span></span> <span data-ttu-id="35e01-185">Ad esempio, `<xref:System.Object>` viene risolto correttamente, al contrario di `<xref:system.object>`.</span><span class="sxs-lookup"><span data-stu-id="35e01-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="35e01-186">Avvisi di compilazione di XRef e compilazioni incrementali</span><span class="sxs-lookup"><span data-stu-id="35e01-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="35e01-187">Una compilazione incrementale compila solo i file che sono stati modificati o che sono stati interessati da una modifica.</span><span class="sxs-lookup"><span data-stu-id="35e01-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="35e01-188">Se viene visualizzato un avviso di compilazione che segnala un collegamento XREF non valido, ma il collegamento segnalato in realtà è valido, il problema può essere dovuto al fatto che è stata eseguita una compilazione incrementale.</span><span class="sxs-lookup"><span data-stu-id="35e01-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="35e01-189">Il file che ha causato l'avviso non è stato modificato, quindi non è stato compilato. L'avviso visualizzato si riferisce a una compilazione precedente.</span><span class="sxs-lookup"><span data-stu-id="35e01-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="35e01-190">L'avviso scomparirà quando il file verrà modificato o se si attiva una compilazione completa (è possibile avviare una compilazione completa in ops.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="35e01-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="35e01-191">Si tratta di un svantaggio delle compilazioni incrementali, perché DocFX non è in grado di rilevare un aggiornamento dei dati all'interno del servizio XREF.</span><span class="sxs-lookup"><span data-stu-id="35e01-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="35e01-192">Determinare l'UID</span><span class="sxs-lookup"><span data-stu-id="35e01-192">Determine the UID</span></span>

<span data-ttu-id="35e01-193">L'UID è in genere il nome completo della classe o del membro.</span><span class="sxs-lookup"><span data-stu-id="35e01-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="35e01-194">Per determinare l'UID esistono almeno due metodi:</span><span class="sxs-lookup"><span data-stu-id="35e01-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="35e01-195">Fare clic con il pulsante destro del mouse sulla pagina [Docs][docs] relativa a un tipo o a un membro, selezionare **Visualizza origine** e quindi copiare il valore **content** per **ms.assetid**:</span><span class="sxs-lookup"><span data-stu-id="35e01-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid nell'origine per la pagina Web](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="35e01-197">Usare il [sito di completamento automatico][] aggiungendo tutto o in parte il nome del tipo all'URL.</span><span class="sxs-lookup"><span data-stu-id="35e01-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="35e01-198">Se, ad esempio, si immette `https://xref.docs.microsoft.com/autocomplete?text=Writeline` nella barra degli indirizzi del browser vengono visualizzati tutti i tipi e i metodi che contengono **Writeline** nel nome, insieme all'UID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="35e01-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="35e01-199">Verificare l'UID</span><span class="sxs-lookup"><span data-stu-id="35e01-199">Verify the UID</span></span>

<span data-ttu-id="35e01-200">Per verificare se l'UID è corretto, sostituire **System.String** nell'URL seguente con l'UID e quindi incollare l'URL nella barra degli indirizzi di un browser:</span><span class="sxs-lookup"><span data-stu-id="35e01-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="35e01-201">L'UID nell'URL fa distinzione tra maiuscole e minuscole. Se si sta controllando un UID di overload del metodo, non includere spazi tra i tipi di parametro.</span><span class="sxs-lookup"><span data-stu-id="35e01-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="35e01-202">Se viene visualizzato codice simile al seguente, l'UID è corretto:</span><span class="sxs-lookup"><span data-stu-id="35e01-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="35e01-203">Se nella pagina è visualizzato solo `[]`, l'UID non è corretto.</span><span class="sxs-lookup"><span data-stu-id="35e01-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="35e01-204">Codifica con simbolo di percentuale degli URL</span><span class="sxs-lookup"><span data-stu-id="35e01-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="35e01-205">I caratteri speciali nell'UID devono essere codificati in HTML come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="35e01-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="35e01-206">Carattere</span><span class="sxs-lookup"><span data-stu-id="35e01-206">Character</span></span> | <span data-ttu-id="35e01-207">Codifica HTML</span><span class="sxs-lookup"><span data-stu-id="35e01-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="35e01-208">%60</span><span class="sxs-lookup"><span data-stu-id="35e01-208">%60</span></span>           |
| `#`       | <span data-ttu-id="35e01-209">%23</span><span class="sxs-lookup"><span data-stu-id="35e01-209">%23</span></span>           |
| `*`       | <span data-ttu-id="35e01-210">%2A</span><span class="sxs-lookup"><span data-stu-id="35e01-210">%2A</span></span>           |

<span data-ttu-id="35e01-211">Vedere l'elenco completo dei [codici con simbolo di percentuale](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="35e01-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="35e01-212">Esempi di codifica:</span><span class="sxs-lookup"><span data-stu-id="35e01-212">Encoding examples:</span></span>

- <span data-ttu-id="35e01-213">`System.Threading.Tasks.Task``1` viene codificato come `System.Threading.Tasks.Task%601` (vedere la [sezione sui tipi generici](#generic-types))</span><span class="sxs-lookup"><span data-stu-id="35e01-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="35e01-214">`System.Exception.#ctor` viene codificato come `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="35e01-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="35e01-215">`System.Object.Equals*` viene codificato come `System.Object.Equals%2A`</span><span class="sxs-lookup"><span data-stu-id="35e01-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="35e01-216">Tipi generici</span><span class="sxs-lookup"><span data-stu-id="35e01-216">Generic types</span></span>

<span data-ttu-id="35e01-217">I tipi generici sono tipi come `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="35e01-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="35e01-218">Se si passa a questo tipo nel [browser delle API .NET ](https://docs.microsoft.com/dotnet/api/) e se ne osserva l'URL, si nota che `<T>` nell'URL è scritto come `-1`, che in realtà rappresenta **\`1**:</span><span class="sxs-lookup"><span data-stu-id="35e01-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="35e01-219">Per creare un collegamento a un tipo generico, ad esempio **List\<T>** , codificare il carattere di apice inverso **\`** con **%60**, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="35e01-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="35e01-220">Metodi</span><span class="sxs-lookup"><span data-stu-id="35e01-220">Methods</span></span>

<span data-ttu-id="35e01-221">Per eseguire il collegamento a un metodo, è possibile collegarsi alla pagina del metodo generale aggiungendo un asterisco (`*`) dopo il nome del metodo o a un overload specifico.</span><span class="sxs-lookup"><span data-stu-id="35e01-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="35e01-222">Usare, ad esempio, la pagina generale quando si vuole creare un collegamento al metodo `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` senza tipi di parametro specifici.</span><span class="sxs-lookup"><span data-stu-id="35e01-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="35e01-223">Il carattere asterisco viene codificato con `%2A`.</span><span class="sxs-lookup"><span data-stu-id="35e01-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="35e01-224">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="35e01-224">For example:</span></span>

<span data-ttu-id="35e01-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` crea un collegamento a <xref:System.Object.Equals%2A?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="35e01-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="35e01-226">Per creare un collegamento a un overload specifico, aggiungere le parentesi dopo il nome del metodo e includere il nome completo del tipo di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="35e01-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="35e01-227">Non inserire alcuno spazio tra i nomi dei tipi. In caso contrario, il collegamento non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="35e01-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="35e01-228">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="35e01-228">For example:</span></span>

<span data-ttu-id="35e01-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` crea un collegamento a <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="35e01-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="35e01-230">Collegamenti da file di inclusione</span><span class="sxs-lookup"><span data-stu-id="35e01-230">Links from includes</span></span>

<span data-ttu-id="35e01-231">Dato che i file di inclusione sono posizionati in un'altra directory, è necessario usare percorsi relativi più lunghi.</span><span class="sxs-lookup"><span data-stu-id="35e01-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="35e01-232">Per impostare un collegamento a un articolo da un file di inclusione, usare questo formato:</span><span class="sxs-lookup"><span data-stu-id="35e01-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="35e01-233">L'estensione [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) per Visual Studio Code consente di inserire correttamente collegamenti e segnalibri relativi senza la necessità di individuare i percorsi.</span><span class="sxs-lookup"><span data-stu-id="35e01-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="35e01-234">Collegamenti nei selettori</span><span class="sxs-lookup"><span data-stu-id="35e01-234">Links in selectors</span></span>

<span data-ttu-id="35e01-235">Un selettore è un componente di esplorazione visualizzato in un articolo della documentazione sotto forma di elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="35e01-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="35e01-236">Quando il lettore seleziona un valore nell'elenco, il browser apre l'articolo selezionato.</span><span class="sxs-lookup"><span data-stu-id="35e01-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="35e01-237">L'elenco del selettore in genere contiene collegamenti ad articoli strettamente correlati, ad esempio articoli sullo stesso argomento in linguaggi di programmazione diversi.</span><span class="sxs-lookup"><span data-stu-id="35e01-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="35e01-238">In presenza di selettori incorporati in un file di inclusione, per i collegamenti è necessario usare la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="35e01-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="35e01-239">Collegamenti in stile riferimento</span><span class="sxs-lookup"><span data-stu-id="35e01-239">Reference-style links</span></span>

<span data-ttu-id="35e01-240">È possibile usare i collegamenti in stile riferimento per rendere più leggibile il contenuto di origine.</span><span class="sxs-lookup"><span data-stu-id="35e01-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="35e01-241">I collegamenti in stile riferimento sostituiscono la sintassi dei collegamenti inline con una sintassi semplificata che consente di spostare gli URL lunghi alla fine dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="35e01-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="35e01-242">Ecco un esempio tratto da [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="35e01-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="35e01-243">Testo inline:</span><span class="sxs-lookup"><span data-stu-id="35e01-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="35e01-244">Collegamenti di riferimento alla fine dell'articolo:</span><span class="sxs-lookup"><span data-stu-id="35e01-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="35e01-245">Assicurarsi di includere lo spazio dopo i due punti, prima del collegamento.</span><span class="sxs-lookup"><span data-stu-id="35e01-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="35e01-246">Quando si imposta un collegamento ad altri articoli tecnici, se si dimentica di includere lo spazio il collegamento non funzionerà nell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="35e01-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="35e01-247">Collegamenti a pagine non incluse nel set di documentazione tecnica</span><span class="sxs-lookup"><span data-stu-id="35e01-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="35e01-248">Per impostare un collegamento a una pagina in un'altra area di proprietà Microsoft, ad esempio una pagina dei prezzi, la pagina del contratto di servizio o qualsiasi altro contenuto che non sia un articolo della documentazione, usare un URL assoluto omettendo le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="35e01-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="35e01-249">L'obiettivo è che i collegamenti funzionino in GitHub e nel sito di rendering:</span><span class="sxs-lookup"><span data-stu-id="35e01-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="35e01-250">Collegamenti a siti di terze parti</span><span class="sxs-lookup"><span data-stu-id="35e01-250">Links to third-party sites</span></span>

<span data-ttu-id="35e01-251">Per un'esperienza utente ottimale, è consigliabile evitare il più possibile i reindirizzamenti degli utenti a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="35e01-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="35e01-252">Basare quindi i collegamenti a siti di terze parti, a volte necessari, su queste informazioni:</span><span class="sxs-lookup"><span data-stu-id="35e01-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="35e01-253">**Responsabilità**: impostare un collegamento a contenuti di terze parti quando le informazioni da condividere sono di proprietà di terzi.</span><span class="sxs-lookup"><span data-stu-id="35e01-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="35e01-254">Ad esempio, non è compito di Microsoft comunicare agli utenti come usare gli strumenti per sviluppatori Android, è una responsabilità di Google.</span><span class="sxs-lookup"><span data-stu-id="35e01-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="35e01-255">Se necessario, Microsoft può spiegare come usare gli strumenti per sviluppatori di Android *con* Azure, ma è Google ad avere la responsabilità di pubblicare contenuti con istruzioni per l'uso dei suoi strumenti.</span><span class="sxs-lookup"><span data-stu-id="35e01-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="35e01-256">**Approvazione del PM**: richiedere che Microsoft approvi il contenuto di terze parti.</span><span class="sxs-lookup"><span data-stu-id="35e01-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="35e01-257">Con l'inserimento di questo tipo di collegamenti Microsoft fa una dichiarazione implicita in merito all'attendibilità del contenuto collegato e si impegna nei confronti dei clienti che seguono le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="35e01-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="35e01-258">**Verifica dello stato di aggiornamento**: assicurarsi che le informazioni di terze parti siano ancora aggiornate, corrette e pertinenti e che il collegamento non sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="35e01-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="35e01-259">**Uscita dal sito**: comunicare agli utenti che stanno passando a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="35e01-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="35e01-260">Se dal contesto non risulta chiaro, aggiungere una frase esplicativa.</span><span class="sxs-lookup"><span data-stu-id="35e01-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="35e01-261">Ad esempio: "I prerequisiti includono gli strumenti di sviluppo di Android, scaricabili dal sito Android Studio".</span><span class="sxs-lookup"><span data-stu-id="35e01-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="35e01-262">**Passaggi successivi**: in questa sezione è appropriato aggiungere un collegamento, ad esempio, a un blog MVP.</span><span class="sxs-lookup"><span data-stu-id="35e01-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="35e01-263">Anche in questo caso, assicurarsi che gli utenti capiscano che stanno per passare a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="35e01-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="35e01-264">**Informazioni legali**: la copertura legale Microsoft è disponibile in **Collegamenti a siti di Terzi** nel piè di pagina **Condizioni per l'utilizzo** in tutte le pagine del sito microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="35e01-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Browser delle API .NET]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Sito di completamento automatico]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
