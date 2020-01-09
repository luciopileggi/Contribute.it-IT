---
title: Come usare collegamenti nella documentazione
description: Questo articolo rappresenta materiale sussidiario per la creazione di collegamenti a contenuto all'interno di docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 970f80b4e6ce795e0e2f15192d31680d7de6d35b
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188332"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="0d689-103">Usare collegamenti nella documentazione</span><span class="sxs-lookup"><span data-stu-id="0d689-103">Use links in documentation</span></span>

<span data-ttu-id="0d689-104">Questo articolo descrive come usare collegamenti ipertestuali da pagine ospitate in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0d689-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="0d689-105">È facile aggiungere collegamenti all'interno di markdown, con alcune convenzioni.</span><span class="sxs-lookup"><span data-stu-id="0d689-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="0d689-106">I collegamenti possono indirizzare gli utenti a contenuto all'interno della stessa pagina, in altre pagine vicine o in siti e URL esterni.</span><span class="sxs-lookup"><span data-stu-id="0d689-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="0d689-107">Il back-end del sito docs.microsoft.com usa i servizi OPS (Open Publishing Service) che supportano il Markdown conforme a [CommonMark](https://commonmark.org/) analizzato tramite il motore di analisi [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="0d689-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark](https://commonmark.org/)-compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="0d689-108">Questa versione di Markdown è per lo più compatibile con [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), perché la maggior parte dei documenti viene archiviata in GitHub dove può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="0d689-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="0d689-109">Altre funzionalità vengono aggiunte tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="0d689-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d689-110">Tutti i collegamenti devono essere protetti (`https` invece di `http`) ogni volta che la destinazione lo supporta (come dovrebbe essere nella maggior parte dei casi).</span><span class="sxs-lookup"><span data-stu-id="0d689-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="0d689-111">Testo del collegamento</span><span class="sxs-lookup"><span data-stu-id="0d689-111">Link text</span></span>

<span data-ttu-id="0d689-112">Le parole che vengono incluse nel testo del collegamento devono essere semplici.</span><span class="sxs-lookup"><span data-stu-id="0d689-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="0d689-113">Devono quindi essere parole normali o il titolo della pagina alla quale porta il collegamento.</span><span class="sxs-lookup"><span data-stu-id="0d689-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d689-114">Non usare "fare clic qui".</span><span class="sxs-lookup"><span data-stu-id="0d689-114">Do not use "click here."</span></span> <span data-ttu-id="0d689-115">È una scelta inefficace per l'ottimizzazione dei motori di ricerca e non descrive adeguatamente la destinazione.</span><span class="sxs-lookup"><span data-stu-id="0d689-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="0d689-116">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="0d689-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="0d689-117">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="0d689-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="0d689-118">Collegamenti da un articolo a un altro</span><span class="sxs-lookup"><span data-stu-id="0d689-118">Links from one article to another</span></span>

<span data-ttu-id="0d689-119">Per creare un collegamento inline da un articolo tecnico di Docs a un altro articolo tecnico di Docs all'interno dello stesso *docset*, usare la sintassi seguente per i collegamenti:</span><span class="sxs-lookup"><span data-stu-id="0d689-119">To create an inline link from a Docs technical article to another Docs technical article within the same *docset*, use the following link syntax:</span></span>

- <span data-ttu-id="0d689-120">Un articolo si collega a un altro articolo nella stessa directory:</span><span class="sxs-lookup"><span data-stu-id="0d689-120">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="0d689-121">Un articolo si collega a un articolo nella directory padre della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="0d689-121">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="0d689-122">Un articolo si collega a un articolo in una sottodirectory della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="0d689-122">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="0d689-123">Un articolo si collega a un articolo in una sottodirectory della directory padre della directory corrente:</span><span class="sxs-lookup"><span data-stu-id="0d689-123">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="0d689-124">Nessuno degli esempi precedenti usa `~/` come parte del collegamento.</span><span class="sxs-lookup"><span data-stu-id="0d689-124">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="0d689-125">Per creare un collegamento a un percorso assoluto che inizia dalla radice del repository, iniziare il collegamento con `/`.</span><span class="sxs-lookup"><span data-stu-id="0d689-125">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="0d689-126">Quando ci si sposta nei repository di origine in GitHub, l'inserimento di `~/` genera collegamenti non validi.</span><span class="sxs-lookup"><span data-stu-id="0d689-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="0d689-127">Iniziare il percorso con `/` risolve correttamente il problema.</span><span class="sxs-lookup"><span data-stu-id="0d689-127">Starting the path with `/` resolves correctly.</span></span>

<span data-ttu-id="0d689-128">Per creare un collegamento a un articolo in un altro docset, anche se il file si trova nello stesso repository, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="0d689-128">To link to an article in a different docset, even if the file is in the same repository, use the following syntax:</span></span>

`[link text](/docset-root/directory/article-name)`
   
<span data-ttu-id="0d689-129">Ad esempio, se un articolo il cui URL radice è `https://docs.microsoft.com/dotnet` si collega a un articolo il cui URL radice è `https://docs.microsoft.com/visualstudio`, il collegamento sarà `[link text](/visualstudio/directory/article-name)`.</span><span class="sxs-lookup"><span data-stu-id="0d689-129">For example, if an article whose root URL is `https://docs.microsoft.com/dotnet` links to an article whose root URL is `https://docs.microsoft.com/visualstudio`, the link would look like `[link text](/visualstudio/directory/article-name)`.</span></span>

> [!TIP]
> <span data-ttu-id="0d689-130">Gli articoli nello stesso *docset* hanno lo stesso frammento di URL dopo "docs.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="0d689-130">Articles in the same *docset* have the same URL fragment after "docs.microsoft.com".</span></span> <span data-ttu-id="0d689-131">Ad esempio, `https://docs.microsoft.com/dotnet/core/get-started` e `https://docs.microsoft.com/dotnet/framework/install` si trovano nello stesso docset e `https://docs.microsoft.com/dotnet/core/get-started` e `https://docs.microsoft.com/visualstudio/whats-new` si trovano in docset diversi.</span><span class="sxs-lookup"><span data-stu-id="0d689-131">For example, `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/dotnet/framework/install` are in the same docset, and `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/visualstudio/whats-new` are in different docsets.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="0d689-132">Collegamenti agli ancoraggi</span><span class="sxs-lookup"><span data-stu-id="0d689-132">Links to anchors</span></span>

<span data-ttu-id="0d689-133">Non è necessario creare ancoraggi.</span><span class="sxs-lookup"><span data-stu-id="0d689-133">You do not have to create anchors.</span></span> <span data-ttu-id="0d689-134">Vengono generati automaticamente in fase di pubblicazione per tutti i titoli H2.</span><span class="sxs-lookup"><span data-stu-id="0d689-134">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="0d689-135">L'unica operazione necessaria è creare collegamenti alle sezioni H2.</span><span class="sxs-lookup"><span data-stu-id="0d689-135">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="0d689-136">Per impostare un collegamento a un titolo nello stesso articolo:</span><span class="sxs-lookup"><span data-stu-id="0d689-136">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="0d689-137">Per impostare un collegamento a un ancoraggio in un altro articolo:</span><span class="sxs-lookup"><span data-stu-id="0d689-137">To link to an anchor in another article:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="0d689-138">Collegamenti da file di inclusione</span><span class="sxs-lookup"><span data-stu-id="0d689-138">Links from includes</span></span>

<span data-ttu-id="0d689-139">Dato che i file di inclusione sono posizionati in un'altra directory, è necessario usare percorsi relativi più lunghi.</span><span class="sxs-lookup"><span data-stu-id="0d689-139">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="0d689-140">Per impostare un collegamento a un articolo da un file di inclusione, usare questo formato:</span><span class="sxs-lookup"><span data-stu-id="0d689-140">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="0d689-141">Collegamenti nei selettori</span><span class="sxs-lookup"><span data-stu-id="0d689-141">Links in selectors</span></span>

<span data-ttu-id="0d689-142">Un selettore è un componente di esplorazione visualizzato in un articolo della documentazione sotto forma di elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="0d689-142">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="0d689-143">Quando il lettore seleziona un valore nell'elenco, il browser apre l'articolo selezionato.</span><span class="sxs-lookup"><span data-stu-id="0d689-143">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="0d689-144">L'elenco del selettore in genere contiene collegamenti ad articoli strettamente correlati, ad esempio articoli sullo stesso argomento in linguaggi di programmazione diversi.</span><span class="sxs-lookup"><span data-stu-id="0d689-144">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="0d689-145">In presenza di selettori incorporati in un file di inclusione, per i collegamenti è necessario usare la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="0d689-145">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="0d689-146">Collegamenti in stile riferimento</span><span class="sxs-lookup"><span data-stu-id="0d689-146">Reference-style links</span></span>

<span data-ttu-id="0d689-147">È possibile usare i collegamenti in stile riferimento per rendere più leggibile il contenuto di origine.</span><span class="sxs-lookup"><span data-stu-id="0d689-147">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="0d689-148">I collegamenti in stile riferimento sostituiscono la sintassi dei collegamenti inline con una sintassi semplificata che consente di spostare gli URL lunghi alla fine dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="0d689-148">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="0d689-149">Ecco un esempio tratto da [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="0d689-149">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="0d689-150">Testo inline:</span><span class="sxs-lookup"><span data-stu-id="0d689-150">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="0d689-151">Collegamenti di riferimento alla fine dell'articolo:</span><span class="sxs-lookup"><span data-stu-id="0d689-151">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="0d689-152">Assicurarsi di includere lo spazio dopo i due punti, prima del collegamento.</span><span class="sxs-lookup"><span data-stu-id="0d689-152">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="0d689-153">Quando si imposta un collegamento ad altri articoli tecnici, se si dimentica di includere lo spazio il collegamento non funzionerà nell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="0d689-153">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="0d689-154">Collegamenti a pagine non incluse nel set di documentazione tecnica</span><span class="sxs-lookup"><span data-stu-id="0d689-154">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="0d689-155">Per impostare un collegamento a una pagina in un'altra area di proprietà Microsoft, ad esempio una pagina dei prezzi, la pagina del contratto di servizio o qualsiasi altro contenuto che non sia un articolo della documentazione, usare un URL assoluto omettendo le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="0d689-155">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="0d689-156">L'obiettivo è che i collegamenti funzionino in GitHub e nel sito di rendering:</span><span class="sxs-lookup"><span data-stu-id="0d689-156">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="0d689-157">Collegamenti a siti di terze parti</span><span class="sxs-lookup"><span data-stu-id="0d689-157">Links to third-party sites</span></span>

<span data-ttu-id="0d689-158">Per un'esperienza utente ottimale, è consigliabile evitare il più possibile i reindirizzamenti degli utenti a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="0d689-158">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="0d689-159">Basare quindi i collegamenti a siti di terze parti, a volte necessari, su queste informazioni:</span><span class="sxs-lookup"><span data-stu-id="0d689-159">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="0d689-160">**Responsabilità**: impostare un collegamento a contenuti di terze parti quando le informazioni da condividere sono di proprietà di terzi.</span><span class="sxs-lookup"><span data-stu-id="0d689-160">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="0d689-161">Ad esempio, non è compito di Microsoft comunicare agli utenti come usare gli strumenti per sviluppatori Android, è una responsabilità di Google.</span><span class="sxs-lookup"><span data-stu-id="0d689-161">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="0d689-162">Se necessario, Microsoft può spiegare come usare gli strumenti per sviluppatori di Android *con* Azure, ma è Google ad avere la responsabilità di pubblicare contenuti con istruzioni per l'uso dei suoi strumenti.</span><span class="sxs-lookup"><span data-stu-id="0d689-162">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="0d689-163">**Approvazione del PM**: richiedere che Microsoft approvi il contenuto di terze parti.</span><span class="sxs-lookup"><span data-stu-id="0d689-163">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="0d689-164">Con l'inserimento di questo tipo di collegamenti Microsoft fa una dichiarazione implicita in merito all'attendibilità del contenuto collegato e si impegna nei confronti dei clienti che seguono le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="0d689-164">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="0d689-165">**Verifica dello stato di aggiornamento**: assicurarsi che le informazioni di terze parti siano ancora aggiornate, corrette e pertinenti e che il collegamento non sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="0d689-165">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="0d689-166">**Uscita dal sito**: comunicare agli utenti che stanno passando a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="0d689-166">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="0d689-167">Se dal contesto non risulta chiaro, aggiungere una frase esplicativa.</span><span class="sxs-lookup"><span data-stu-id="0d689-167">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="0d689-168">Ad esempio: "I prerequisiti includono gli strumenti per sviluppatori di Android, scaricabili dal sito di Android Studio".</span><span class="sxs-lookup"><span data-stu-id="0d689-168">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="0d689-169">**Passaggi successivi**: è appropriato aggiungere un collegamento, ad esempio a un blog MVP, nella sezione "Passaggi successivi".</span><span class="sxs-lookup"><span data-stu-id="0d689-169">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="0d689-170">Anche in questo caso, assicurarsi che gli utenti capiscano che stanno per passare a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="0d689-170">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="0d689-171">**Informazioni legali**: la copertura legale Microsoft è disponibile in **Collegamenti a siti di Terzi** nel piè di pagina **Condizioni per l'utilizzo** in tutte le pagine di ms.com.</span><span class="sxs-lookup"><span data-stu-id="0d689-171">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="0d689-172">Collegamenti a contenuto di riferimento di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d689-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="0d689-173">Il contenuto di riferimento di Azure PowerShell è stato sottoposto a numerose modifiche da novembre 2016.</span><span class="sxs-lookup"><span data-stu-id="0d689-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="0d689-174">Usare le linee guida seguenti per aggiungere collegamenti a questo contenuto da altri articoli in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0d689-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="0d689-175">Struttura dell'URL:</span><span class="sxs-lookup"><span data-stu-id="0d689-175">Structure of the URL:</span></span>

* <span data-ttu-id="0d689-176">Per i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0d689-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="0d689-177">Per gli argomenti concettuali:</span><span class="sxs-lookup"><span data-stu-id="0d689-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="0d689-178">La parte `<moniker-name>` è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="0d689-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="0d689-179">Se omessa, si verrà indirizzati alla versione più recente del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0d689-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="0d689-180">La parte `<service-name>` è uno degli esempi illustrati negli URL di base seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d689-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="0d689-181">Contenuto di Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="0d689-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="0d689-182">Contenuto di Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="0d689-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="0d689-183">Contenuto di PowerShell per Azure Active Directory (AzureAD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="0d689-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="0d689-184">PowerShell per Azure Service Fabric: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="0d689-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="0d689-185">PowerShell per Azure Information Protection: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="0d689-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="0d689-186">PowerShell per i processi di database elastici di Azure: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="0d689-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="0d689-187">Quando si usano questi URL si verrà indirizzati alla versione più recente del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0d689-187">When you use these URLs, you'll be redirected to the latest version of the content.</span></span> <span data-ttu-id="0d689-188">In questo modo non è necessario specificare un moniker di versione.</span><span class="sxs-lookup"><span data-stu-id="0d689-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="0d689-189">E non si avranno collegamenti a contenuto concettuale che dovranno essere aggiornati in seguito a modifiche di versione.</span><span class="sxs-lookup"><span data-stu-id="0d689-189">And, you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="0d689-190">Per creare il collegamento corretto, trovare la pagina a cui collegarsi nel browser, copiare l'URL e quindi rimuovere il codice delle impostazioni locali, ad esempio **en-US**.</span><span class="sxs-lookup"><span data-stu-id="0d689-190">To create the correct link, find the page that you want to link to in your browser, copy the URL, and then remove the locale code, for example, **en-us**.</span></span>

<span data-ttu-id="0d689-191">Markdown di esempio:</span><span class="sxs-lookup"><span data-stu-id="0d689-191">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](https://docs.microsoft.com/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](https://docs.microsoft.com/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-azurerm-ps)
```
