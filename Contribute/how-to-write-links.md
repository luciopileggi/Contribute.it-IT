---
title: Come usare collegamenti nella documentazione
description: Questo articolo rappresenta materiale sussidiario per la creazione di collegamenti a contenuto all'interno di docs.microsoft.com.
ms.date: 06/29/2017
ms.openlocfilehash: 92c23f2b91c67d7a1695c5f1e5dcdc80a8517f6e
ms.sourcegitcommit: 37cd16636d7dcfc5222ef5a5d60e4ff30f74485c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2018
ms.locfileid: "48030934"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="b5aa0-103">Uso di collegamenti nella documentazione</span><span class="sxs-lookup"><span data-stu-id="b5aa0-103">Using links in documentation</span></span>
<span data-ttu-id="b5aa0-104">Questo articolo descrive come usare collegamenti ipertestuali da pagine ospitate in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="b5aa0-105">È facile aggiungere collegamenti all'interno di markdown, con alcune convenzioni.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="b5aa0-106">I collegamenti possono indirizzare gli utenti a contenuto all'interno della stessa pagina, ad altre pagine vicine o a siti e URL esterni.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="b5aa0-107">Il back-end del sito docs.microsoft.com usa Open Publishing Services (OPS), che implementa DocFX Flavored Markdown (DFM).</span><span class="sxs-lookup"><span data-stu-id="b5aa0-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="b5aa0-108">DFM ha un'elevata compatibilità con GitHub Flavored Markdown (GFM) e aggiunge altre funzionalità tramite estensioni Markdown.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5aa0-109">Tutti i collegamenti devono essere protetti (`https` invece di `http`) ogni volta che la destinazione lo supporta (come dovrebbe essere nella maggior parte dei casi).</span><span class="sxs-lookup"><span data-stu-id="b5aa0-109">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="b5aa0-110">Testo del collegamento</span><span class="sxs-lookup"><span data-stu-id="b5aa0-110">Link text</span></span>

<span data-ttu-id="b5aa0-111">Le parole che vengono incluse nel testo del collegamento devono essere semplici.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-111">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="b5aa0-112">Devono quindi essere parole normali o il titolo della pagina alla quale porta il collegamento.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-112">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5aa0-113">Non usare "fare clic qui".</span><span class="sxs-lookup"><span data-stu-id="b5aa0-113">Do not use "click here."</span></span> <span data-ttu-id="b5aa0-114">È una scelta inefficace per l'ottimizzazione dei motori di ricerca e non descrive adeguatamente la destinazione.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-114">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="b5aa0-115">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b5aa0-115">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="b5aa0-116">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b5aa0-116">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="b5aa0-117">Collegamenti da un articolo a un altro</span><span class="sxs-lookup"><span data-stu-id="b5aa0-117">Links from one article to another</span></span>

<span data-ttu-id="b5aa0-118">Per creare un collegamento inline da un articolo tecnico di Docs a un altro articolo tecnico di Docs all'interno dello stesso docset, usare la sintassi seguente per i collegamenti:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-118">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="b5aa0-119">Un articolo in una directory si collega a un altro articolo nella stessa directory:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-119">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="b5aa0-120">Un articolo si collega da una sottodirectory a un articolo nella directory radice:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-120">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="b5aa0-121">Un articolo nella directory radice si collega a un articolo in una sottodirectory:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-121">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="b5aa0-122">Un articolo in una sottodirectory si collega a un articolo in un'altra sottodirectory:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-122">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="b5aa0-123">Un articolo che si collega a più docset (anche se nello stesso repository): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="b5aa0-123">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5aa0-124">Nessuno degli esempi precedenti utilizza `~/` come parte del collegamento.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-124">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="b5aa0-125">Se ci si collega a un percorso alla radice del repository, iniziare con `/`.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-125">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="b5aa0-126">Quando ci si sposta nei repository di origine in GitHub, l'inserimento di `~/` genera collegamenti non validi.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="b5aa0-127">Iniziare il percorso con `/` risolve correttamente il problema.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-127">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="b5aa0-128">Collegamenti agli ancoraggi</span><span class="sxs-lookup"><span data-stu-id="b5aa0-128">Links to anchors</span></span>

<span data-ttu-id="b5aa0-129">Non è necessario creare ancoraggi.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-129">You do not have to create anchors.</span></span> <span data-ttu-id="b5aa0-130">Vengono generati automaticamente in fase di pubblicazione per tutti i titoli H2.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-130">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="b5aa0-131">L'unica operazione necessaria è creare collegamenti alle sezioni H2.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-131">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="b5aa0-132">Per impostare un collegamento a un titolo nello stesso articolo:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-132">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="b5aa0-133">Per impostare un collegamento a un ancoraggio in un altro articolo nella stessa sottodirectory:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-133">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="b5aa0-134">Per impostare un collegamento a un ancoraggio nella sottodirectory di un altro servizio:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-134">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="b5aa0-135">Collegamenti da file di inclusione</span><span class="sxs-lookup"><span data-stu-id="b5aa0-135">Links from includes</span></span>

<span data-ttu-id="b5aa0-136">Dato che i file di inclusione sono posizionati in un'altra directory, è necessario usare percorsi relativi più lunghi.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-136">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="b5aa0-137">Per impostare un collegamento a un articolo da un file di inclusione, usare questo formato:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-137">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="b5aa0-138">Collegamenti nei selettori</span><span class="sxs-lookup"><span data-stu-id="b5aa0-138">Links in selectors</span></span>

<span data-ttu-id="b5aa0-139">In presenza di selettori incorporati in un file di inclusione, come quelli usati dal team della documentazione di Azure, è necessario usare la struttura seguente per i collegamenti:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-139">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="b5aa0-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="b5aa0-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="b5aa0-141">(Testo1 | Esempio1)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-141">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="b5aa0-142">(Testo1 | Esempio2)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-142">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="b5aa0-143">(Testo2 | Esempio3)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-143">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="b5aa0-144">[(Testo2 | Esempio4)](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="b5aa0-144">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="b5aa0-145">Collegamenti in stile riferimento</span><span class="sxs-lookup"><span data-stu-id="b5aa0-145">Reference-style links</span></span>

<span data-ttu-id="b5aa0-146">È possibile usare i collegamenti in stile riferimento per rendere più leggibile il contenuto di origine.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-146">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="b5aa0-147">I collegamenti in stile riferimento sostituiscono la sintassi dei collegamenti inline con una sintassi semplificata che consente di spostare gli URL lunghi alla fine dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-147">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="b5aa0-148">Ecco un esempio tratto da [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="b5aa0-148">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="b5aa0-149">Testo inline:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-149">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="b5aa0-150">Collegamenti di riferimento alla fine dell'articolo:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-150">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="b5aa0-151">Assicurarsi di includere lo spazio dopo i due punti, prima del collegamento.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-151">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="b5aa0-152">Quando si imposta un collegamento ad altri articoli tecnici, se si dimentica di includere lo spazio il collegamento non funzionerà nell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-152">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="b5aa0-153">Collegamenti a pagine non incluse nel set di documentazione tecnica</span><span class="sxs-lookup"><span data-stu-id="b5aa0-153">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="b5aa0-154">Per impostare un collegamento a una pagina in un'altra area di proprietà Microsoft, ad esempio una pagina dei prezzi, la pagina del contratto di servizio o qualsiasi altro contenuto che non sia un articolo della documentazione, usare un URL assoluto omettendo le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-154">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="b5aa0-155">L'obiettivo è che i collegamenti funzionino in GitHub e nel sito di rendering:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-155">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="b5aa0-156">Collegamenti a siti di terze parti</span><span class="sxs-lookup"><span data-stu-id="b5aa0-156">Links to third-party sites</span></span>

<span data-ttu-id="b5aa0-157">Per un'esperienza utente ottimale, è consigliabile evitare il più possibile i reindirizzamenti degli utenti a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-157">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="b5aa0-158">Basare quindi i collegamenti a siti di terze parti, a volte necessari, su queste informazioni:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-158">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="b5aa0-159">**Responsabilità:**: impostare un collegamento a contenuti di terze parti quando le informazioni da condividere sono di proprietà di terzi.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-159">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="b5aa0-160">Ad esempio, non è compito di Microsoft comunicare agli utenti come usare gli strumenti per sviluppatori Android, è una responsabilità di Google.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-160">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="b5aa0-161">Se necessario, Microsoft può spiegare come usare gli strumenti per sviluppatori di Android *con* Azure, ma è Google ad avere la responsabilità di pubblicare contenuti con istruzioni per l'uso dei suoi strumenti.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-161">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="b5aa0-162">**Approvazione del PM**: richiedere che Microsoft approvi il contenuto di terze parti.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-162">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="b5aa0-163">Con l'inserimento di questo tipo di collegamenti Microsoft fa una dichiarazione implicita in merito all'attendibilità del contenuto collegato e si impegna nei confronti dei clienti che seguono le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-163">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="b5aa0-164">**Verifica dello stato di aggiornamento**: assicurarsi che le informazioni di terze parti siano ancora aggiornate, corrette e pertinenti e che il collegamento non sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-164">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="b5aa0-165">**Uscita dal sito**: comunicare agli utenti che stanno passando a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-165">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="b5aa0-166">Se dal contesto non risulta chiaro, aggiungere una frase esplicativa.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-166">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="b5aa0-167">Ad esempio, "I prerequisiti includono Android Developer Tools, scaricabile dal sito di Android Studio".</span><span class="sxs-lookup"><span data-stu-id="b5aa0-167">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="b5aa0-168">**Passaggi successivi**: è appropriato aggiungere un collegamento, ad esempio a un blog MVP, nella sezione "Passaggi successivi".</span><span class="sxs-lookup"><span data-stu-id="b5aa0-168">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="b5aa0-169">Anche in questo caso, assicurarsi che gli utenti capiscano che stanno per passare a un altro sito.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-169">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="b5aa0-170">**Informazioni legali**: la copertura legale Microsoft è disponibile in **Collegamenti a siti di Terzi** nel piè di pagina **Condizioni per l'utilizzo** in tutte le pagine di ms.com.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-170">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="b5aa0-171">Collegamenti a MSDN o TechNet</span><span class="sxs-lookup"><span data-stu-id="b5aa0-171">Links to MSDN or TechNet</span></span>

<span data-ttu-id="b5aa0-172">Quando è necessario inserire un collegamento a MSDN o TechNet, usare il collegamento completo all'argomento rimuovendo l'indicatore della lingua delle impostazioni locali "it-it" dal collegamento.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-172">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="b5aa0-173">Collegamenti a contenuto di riferimento di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b5aa0-173">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="b5aa0-174">Il contenuto di riferimento di Azure PowerShell è stato sottoposto a numerose modifiche da novembre 2016.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-174">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="b5aa0-175">Usare le linee guida seguenti per aggiungere collegamenti a questo contenuto da altri articoli in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-175">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="b5aa0-176">Struttura dell'URL:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-176">Structure of the URL:</span></span>

* <span data-ttu-id="b5aa0-177">Per i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-177">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="b5aa0-178">Per gli argomenti concettuali:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-178">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="b5aa0-179">La parte &lt;moniker-name&gt; è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-179">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="b5aa0-180">Se omessa, si verrà indirizzati alla versione più recente del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-180">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="b5aa0-181">La parte &lt;service-name&gt; è uno degli esempi indicati negli URL di base seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-181">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="b5aa0-182">Contenuto di Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-182">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="b5aa0-183">Contenuto di Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-183">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="b5aa0-184">Contenuto di PowerShell per Azure Active Directory (AzureAD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-184">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="b5aa0-185">PowerShell per Azure Service Fabric: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-185">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="b5aa0-186">PowerShell per Azure Information Protection: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-186">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="b5aa0-187">PowerShell per i processi di database elastici di Azure: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="b5aa0-187">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="b5aa0-188">Quando si usano questi URL si verrà indirizzati alla versione più recente del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-188">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="b5aa0-189">In questo modo non è necessario specificare un moniker di versione.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-189">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="b5aa0-190">E non si avranno collegamenti a contenuto concettuale che dovranno essere aggiornati in seguito a modifiche di versione.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-190">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="b5aa0-191">Per creare il collegamento corretto, trovare la pagina a cui collegarsi nel browser e copiare l'URL.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-191">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="b5aa0-192">Rimuovere quindi ´ "https://docs.microsoft.com" ´ e le informazioni delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-192">Then, remove ´ "https://docs.microsoft.com" ´ and the locale info.</span></span>

<span data-ttu-id="b5aa0-193">Per i collegamenti da un sommario, è necessario usare l'URL completo senza le informazioni delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="b5aa0-193">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="b5aa0-194">Markdown di esempio:</span><span class="sxs-lookup"><span data-stu-id="b5aa0-194">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
