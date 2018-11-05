---
title: Informazioni di riferimento su Markdown per OPS e docs.microsoft.com
description: Guida della piattaforma OPS per le estensioni Markdown e DocFX Flavored Markdown (DFM).
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: e248eafb0247b200313ba198f2545eca947f5627
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805910"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="eca8b-103">Informazioni di riferimento su Markdown per OPS</span><span class="sxs-lookup"><span data-stu-id="eca8b-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="eca8b-104">Markdown è un semplice linguaggio di markup che usa una sintassi di formattazione in testo normale.</span><span class="sxs-lookup"><span data-stu-id="eca8b-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="eca8b-105">OPS supporta lo standard CommonMark per Markdown e alcune estensioni Markdown personalizzate progettate per offrire contenuti formattati in docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca8b-105">OPS supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="eca8b-106">In questo articolo vengono elencanti in ordine alfabetico gli elementi necessari per usare Markdown in OPS per docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca8b-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="eca8b-107">Per creare codice Markdown è possibile usare un qualsiasi editor di testo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="eca8b-108">Per un editore che consenta di inserire sia una sintassi Markdown standard sia estensioni OPS personalizzate, è consigliabile usare [VS Code](https://code.visualstudio.com/) con [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installato.</span><span class="sxs-lookup"><span data-stu-id="eca8b-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="eca8b-109">OPS ha adottato come standard Markdig per tutti i nuovi repository mentre dei repository precedenti viene eseguita la migrazione in Markdig.</span><span class="sxs-lookup"><span data-stu-id="eca8b-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="eca8b-110">In [https://babelmark.github.io/](https://babelmark.github.io/) è possibile testare il rendering di Markdown in Markdig e in altri motori.</span><span class="sxs-lookup"><span data-stu-id="eca8b-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="eca8b-111">Avvisi (nota, suggerimento, informazione importante, attenzione e avvertimento)</span><span class="sxs-lookup"><span data-stu-id="eca8b-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="eca8b-112">Avvisa un estensione Markdown specifica per OPS affinché si creino citazioni per eseguire il rendering in docs.microsoft.com usando colori e icone che indicano il significato del contenuto.</span><span class="sxs-lookup"><span data-stu-id="eca8b-112">Alerts an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="eca8b-113">Sono supportati i tipi di avviso seguenti:</span><span class="sxs-lookup"><span data-stu-id="eca8b-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="eca8b-114">L'aspetto degli avvisi in docs.microsoft.com è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="eca8b-115">Informazioni che l'utente dovrebbe leggere velocemente.</span><span class="sxs-lookup"><span data-stu-id="eca8b-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="eca8b-116">Informazioni facoltative che facilitano le attività dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eca8b-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca8b-117">Informazioni essenziali per le attività dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eca8b-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="eca8b-118">Conseguenze potenzialmente negative di un'azione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="eca8b-119">Conseguenze assolutamente pericolose di un'azione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="eca8b-120">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="eca8b-120">Code snippets</span></span>

<span data-ttu-id="eca8b-121">Nei file Markdown è possibile incorporare frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="eca8b-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="eca8b-122">Titoli</span><span class="sxs-lookup"><span data-stu-id="eca8b-122">Headings</span></span>

<span data-ttu-id="eca8b-123">OPS supporta sei livelli di titoli Markdown:</span><span class="sxs-lookup"><span data-stu-id="eca8b-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="eca8b-124">Deve essere presente uno spazio tra l'ultimo `#` e il testo del titolo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="eca8b-125">Ogni file Markdown deve avere esclusivamente un elemento H1.</span><span class="sxs-lookup"><span data-stu-id="eca8b-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="eca8b-126">L'elemento H1 deve essere il primo contenuto nel file dopo il blocco di metadati YML.</span><span class="sxs-lookup"><span data-stu-id="eca8b-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="eca8b-127">Gli elementi H2 vengono visualizzati automaticamente nel menu di spostamento a destra del file pubblicato.</span><span class="sxs-lookup"><span data-stu-id="eca8b-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="eca8b-128">Non esistono titoli di livello inferiore. Usare gli H2 in modo strategico per consentire agli utenti di navigare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="eca8b-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="eca8b-129">I titoli HMTL, ad esempio `<h1>`, non sono consigliati e in alcuni casi generano avvisi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="eca8b-130">È possibile creare un collegamento a singoli titoli in un file usando i [segnalibri](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="eca8b-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="eca8b-131">HTML</span><span class="sxs-lookup"><span data-stu-id="eca8b-131">HTML</span></span>

<span data-ttu-id="eca8b-132">Markdown supporta HTML inline. Il linguaggio HTML non è comunque consigliabile per eseguire la pubblicazione tramite OPS ed eccezione fatta per un breve elenco di valori, genera errori o avvisi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="eca8b-133">Immagini</span><span class="sxs-lookup"><span data-stu-id="eca8b-133">Images</span></span>

<span data-ttu-id="eca8b-134">La sintassi per l'inclusione di un'immagine è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="eca8b-135">Dove `alt text` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine.</span><span class="sxs-lookup"><span data-stu-id="eca8b-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="eca8b-136">Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="eca8b-137">È anche utile se in presenza di un bug nel sito non è possibile eseguire il rendering dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="eca8b-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="eca8b-138">Le immagini devono essere archiviate in una cartella `/media` all'interno del docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="eca8b-139">Per impostazione predefinita, per le immagini sono supportati i tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="eca8b-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="eca8b-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="eca8b-140">.jpg</span></span>
- <span data-ttu-id="eca8b-141">.png</span><span class="sxs-lookup"><span data-stu-id="eca8b-141">.png</span></span>

<span data-ttu-id="eca8b-142">È possibile supportare altri tipi i immagine aggiungendoli come risorse al file docfx.json<!--add link to reference when available--> nel docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="eca8b-143">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="eca8b-143">Links</span></span>

<span data-ttu-id="eca8b-144">Nella maggior parte dei casi OPS usa collegamenti Markdown standard per collegarsi ad altri file e pagine.</span><span class="sxs-lookup"><span data-stu-id="eca8b-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="eca8b-145">I tipi di collegamenti vengono descritti nelle sottosezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="eca8b-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="eca8b-146">Docs Authoring Pack per VS Code consente di inserire collegamenti relativi e segnalibri in modo corretto senza dover conoscere i percorsi.</span><span class="sxs-lookup"><span data-stu-id="eca8b-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca8b-147">Nei collegamenti ai siti Microsoft non includere codici delle impostazioni locali, ad esempio it-it.</span><span class="sxs-lookup"><span data-stu-id="eca8b-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="eca8b-148">I codici delle impostazioni locali hardcoded impediscono il rendering del contenuto localizzato. Si assiste così a una pessima esperienza utente in altre impostazioni locali e a un aumento significativo dei costi i localizzazione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="eca8b-149">Quando si copia un URL da un browser, il codice delle impostazioni locali viene incluso per impostazione predefinita. È quindi necessario eliminarlo manualmente quando si crea il collegamento.</span><span class="sxs-lookup"><span data-stu-id="eca8b-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete in when you create your link.</span></span> <span data-ttu-id="eca8b-150">Ad esempio, usare:</span><span class="sxs-lookup"><span data-stu-id="eca8b-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="eca8b-151">Non usare:</span><span class="sxs-lookup"><span data-stu-id="eca8b-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="eca8b-152">Collegamenti relativi a file all'interno dello stesso docset</span><span class="sxs-lookup"><span data-stu-id="eca8b-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="eca8b-153">Un percorso relativo è il percorso al file di destinazione relativo al file corrente.</span><span class="sxs-lookup"><span data-stu-id="eca8b-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="eca8b-154">In OPS è possibile usare un percorso relativo per il collegamento a un altro file all'interno dello stesso docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="eca8b-155">La sintassi di un percorso relativo è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="eca8b-156">Dove `../` indica un livello superiore nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="eca8b-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="eca8b-157">Il percorso relativo verrà risolto durante la compilazione e verrà anche rimossa l'estensione md.</span><span class="sxs-lookup"><span data-stu-id="eca8b-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="eca8b-158">È possibile usare "../" per il collegamento a un file nella cartella padre, ma il file deve appartenere allo stesso docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="eca8b-159">Non è possibile usare "../" per il collegamento a un file in un'altra cartella del docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="eca8b-160">OPS supporta anche un formato speciale di percorso relativo che inizia con "~" (ad esempio, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="eca8b-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="eca8b-161">Questa sintassi indica un file relativo alla cartella radice di un docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="eca8b-162">Anche questo tipo di percorso viene convalidato e risolto durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca8b-163">Includere l'estensione del file nel percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="eca8b-164">Durante la compilazione viene convalidata l'esistenza del file di destinazione di tale percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="eca8b-165">Se il percorso relativo non include l'estensione file, la compilazione potrebbe segnalare un avviso di collegamento interrotto.</span><span class="sxs-lookup"><span data-stu-id="eca8b-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="eca8b-166">Ad esempio, usare:</span><span class="sxs-lookup"><span data-stu-id="eca8b-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="eca8b-167">Non usare:</span><span class="sxs-lookup"><span data-stu-id="eca8b-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="eca8b-168">Collegamenti assoluti ad altri file in OPS</span><span class="sxs-lookup"><span data-stu-id="eca8b-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="eca8b-169">Non includere l'estensione file md.</span><span class="sxs-lookup"><span data-stu-id="eca8b-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="eca8b-170">In questo modo si crea il collegamento al file della panoramica Linux dall'esterno del doset "articles" di Azure.</span><span class="sxs-lookup"><span data-stu-id="eca8b-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="eca8b-171">Collegamenti a siti esterni</span><span class="sxs-lookup"><span data-stu-id="eca8b-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="eca8b-172">Collegamento basato su URL a un'altra pagina Web. Deve includere https://.</span><span class="sxs-lookup"><span data-stu-id="eca8b-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="eca8b-173">Collegamento segnalibro</span><span class="sxs-lookup"><span data-stu-id="eca8b-173">Bookmark links</span></span>

<span data-ttu-id="eca8b-174">Collegamento segnalibro a un titolo in un altro file all'interno dello stesso repository:</span><span class="sxs-lookup"><span data-stu-id="eca8b-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="eca8b-175">Collegamento segnalibro a un titolo nel file corrente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="eca8b-176">Usare un hashtag seguito dalle parole del titolo senza la punteggiatura e sostituire gli spazi con i trattini.</span><span class="sxs-lookup"><span data-stu-id="eca8b-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="eca8b-177">Collegamenti di ancoraggio esplicito</span><span class="sxs-lookup"><span data-stu-id="eca8b-177">Explicit anchor links</span></span>

<span data-ttu-id="eca8b-178">I collegamenti di ancoraggio esplicito che usano il tag HTML `<a>` **non sono né necessari né consigliati** tranne in pagine hub e pagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="eca8b-179">Usare i segnalibri in file Markdown generali, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="eca8b-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="eca8b-180">In caso di pagine hub e pagine di destinazione, usare gli ancoraggi come descritto di seguito:</span><span class="sxs-lookup"><span data-stu-id="eca8b-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="eca8b-181">`## <a id="AnchorText"> </a>Header text` oppure `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="eca8b-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="eca8b-182">Per il collegamento ad ancoraggi espliciti, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="eca8b-183">Collegamenti XREF (riferimento incrociato)</span><span class="sxs-lookup"><span data-stu-id="eca8b-183">XREF (cross reference) links</span></span>

<span data-ttu-id="eca8b-184">Per il collegamento alle pagine di riferimento API generate automaticamente nel docset corrente o in altri docset, usare i collegamenti XREF con l'ID univoco (UID).</span><span class="sxs-lookup"><span data-stu-id="eca8b-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="eca8b-185">Per fare riferimento a pagine di riferimento API in altri docset, è necessario aggiungere la configurazione `xrefService` nel file `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-185">To reference API reference pages in other docsets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="eca8b-186">L'UID corrisponde al nome completo di classe e membro.</span><span class="sxs-lookup"><span data-stu-id="eca8b-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="eca8b-187">Se si aggiunge \* dopo l'UID, il collegamento rappresenta la pagina di overload e non un'API specifica.</span><span class="sxs-lookup"><span data-stu-id="eca8b-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="eca8b-188">Ad esempio, usare `List<T>.BinarySearch*` per il collegamento alla pagina BinarySearch Method anziché all'overload specifico, come `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="eca8b-189">È possibile usare una delle sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="eca8b-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="eca8b-190">Collegamento automatico: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="eca8b-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="eca8b-191">Il parametro di query `displayProperty` facoltativo genera un testo del collegamento completo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="eca8b-192">Per impostazione predefinita, il testo del collegamento mostra solo il nome del membro o del tipo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="eca8b-193">Collegamento Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="eca8b-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="eca8b-194">Può essere usato quando si vuole personalizzare il testo del collegamento visualizzato.</span><span class="sxs-lookup"><span data-stu-id="eca8b-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="eca8b-195">Esempi:</span><span class="sxs-lookup"><span data-stu-id="eca8b-195">Examples:</span></span>

- <span data-ttu-id="eca8b-196">`<xref:System.String>` viene visualizzato come "String".</span><span class="sxs-lookup"><span data-stu-id="eca8b-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="eca8b-197">`<xref:System.String?displayProperty=nameWithType>` viene visualizzato come "System.String".</span><span class="sxs-lookup"><span data-stu-id="eca8b-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="eca8b-198">`[String class](xref:System.String)` viene visualizzato come "String class".</span><span class="sxs-lookup"><span data-stu-id="eca8b-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="eca8b-199">Attualmente non è disponibile un sistema semplice per trovare gli UID.</span><span class="sxs-lookup"><span data-stu-id="eca8b-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="eca8b-200"><!-- ? -->Il modo migliore per trovare l'UID per un'API consiste nel visualizzare l'origine della pagina dell'API che si vuole collegare e individuare il valore ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="eca8b-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="eca8b-201">I singoli valori di overload non vengono visualizzati nell'origine.</span><span class="sxs-lookup"><span data-stu-id="eca8b-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="eca8b-202">È in corso lo sviluppo di un sistema migliore, che sarà disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="eca8b-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="eca8b-203">Quando l'UID contiene i caratteri speciali \`, \# o \*, il valore dell'UID deve essere con codifica HTML come `%60`, `%23` e `%2A` rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="eca8b-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="eca8b-204">A volte sono presenti parentesi con codifica, ma questo non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="eca8b-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="eca8b-205">Esempi:</span><span class="sxs-lookup"><span data-stu-id="eca8b-205">Examples:</span></span>

- <span data-ttu-id="eca8b-206">System.Threading.Tasks.Task\`1 diventa `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="eca8b-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="eca8b-207">System.Exception.\#ctor diventa `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="eca8b-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="eca8b-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) diventa `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="eca8b-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="eca8b-209">Elenchi (numerati, puntati, di controllo)</span><span class="sxs-lookup"><span data-stu-id="eca8b-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="eca8b-210">Elenco numerato</span><span class="sxs-lookup"><span data-stu-id="eca8b-210">Numbered list</span></span>

<span data-ttu-id="eca8b-211">Per creare un elenco numerato è possibile usare tutti 1, che dopo la pubblicazione vengono visualizzati come elenco sequenziale.</span><span class="sxs-lookup"><span data-stu-id="eca8b-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="eca8b-212">Per migliorare la leggibilità dell'origine, è possibile incrementare gli elenchi.</span><span class="sxs-lookup"><span data-stu-id="eca8b-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="eca8b-213">Non usare le lettere negli elenchi, neppure negli elenchi annidati.</span><span class="sxs-lookup"><span data-stu-id="eca8b-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="eca8b-214">Non vengono visualizzati correttamente quando vengono pubblicati tramite OPS.</span><span class="sxs-lookup"><span data-stu-id="eca8b-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="eca8b-215">Gli elenchi annidati che usano i numeri vengono visualizzati con lettere minuscole quando vengono pubblicati.</span><span class="sxs-lookup"><span data-stu-id="eca8b-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="eca8b-216">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="eca8b-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="eca8b-217">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-217">This renders as follows:</span></span>

1. <span data-ttu-id="eca8b-218">This is</span><span class="sxs-lookup"><span data-stu-id="eca8b-218">This is</span></span>
1. <span data-ttu-id="eca8b-219">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="eca8b-219">a parent numbered list</span></span>
   1. <span data-ttu-id="eca8b-220">and this is</span><span class="sxs-lookup"><span data-stu-id="eca8b-220">and this is</span></span>
   1. <span data-ttu-id="eca8b-221">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="eca8b-221">a nested numbered list</span></span>
1. <span data-ttu-id="eca8b-222">(fin)</span><span class="sxs-lookup"><span data-stu-id="eca8b-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="eca8b-223">Elenco puntato</span><span class="sxs-lookup"><span data-stu-id="eca8b-223">Bulleted list</span></span>

<span data-ttu-id="eca8b-224">Per creare un elenco puntato, usare `-` seguito da uno spazio all'inizio di ogni linea:</span><span class="sxs-lookup"><span data-stu-id="eca8b-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="eca8b-225">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-225">This renders as follows:</span></span>

- <span data-ttu-id="eca8b-226">This is</span><span class="sxs-lookup"><span data-stu-id="eca8b-226">This is</span></span>
- <span data-ttu-id="eca8b-227">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="eca8b-227">a parent bulleted list</span></span>
  - <span data-ttu-id="eca8b-228">and this is</span><span class="sxs-lookup"><span data-stu-id="eca8b-228">and this is</span></span>
  - <span data-ttu-id="eca8b-229">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="eca8b-229">a nested bulleted list</span></span>
- <span data-ttu-id="eca8b-230">All done!</span><span class="sxs-lookup"><span data-stu-id="eca8b-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="eca8b-231">Elenco di controllo</span><span class="sxs-lookup"><span data-stu-id="eca8b-231">Checklist</span></span>

<span data-ttu-id="eca8b-232">Gli elenchi di controllo possono essere usati solo in docs.microsoft.com tramite un'estensione Markdown personalizzata:</span><span class="sxs-lookup"><span data-stu-id="eca8b-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="eca8b-233">Il rendering di esempio in docs.microsoft.com è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="eca8b-234">List item 1</span><span class="sxs-lookup"><span data-stu-id="eca8b-234">List item 1</span></span>
> * <span data-ttu-id="eca8b-235">List item 2</span><span class="sxs-lookup"><span data-stu-id="eca8b-235">List item 2</span></span>
> * <span data-ttu-id="eca8b-236">List item 3</span><span class="sxs-lookup"><span data-stu-id="eca8b-236">List item 3</span></span>

<span data-ttu-id="eca8b-237">Usare gli elenchi di controllo all'inizio o alla fine di un articolo per riepilogare il contenuto di cui si parlerà o di cui si è parlato nell'articolo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-237">Use checklits at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="eca8b-238">Non aggiungere elenchi di controllo casuali all'interno degli articoli.</span><span class="sxs-lookup"><span data-stu-id="eca8b-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="eca8b-239">Azione Passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="eca8b-239">Next step action</span></span>

<span data-ttu-id="eca8b-240">È possibile usare un'estensione personalizzata per aggiungere solo alle pagine in docs.microsoft.com un pulsante di azione per il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="eca8b-241">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="eca8b-242">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="eca8b-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="eca8b-243">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="eca8b-244">Informazioni su stile di base</span><span class="sxs-lookup"><span data-stu-id="eca8b-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="eca8b-245">Nell'azione per il passaggio successivo è possibile usare tutti i collegamenti supportati, incluso un collegamento Markdown a un'altra pagina Web.</span><span class="sxs-lookup"><span data-stu-id="eca8b-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="eca8b-246">Nella maggior parte dei casi il collegamento all'azione successiva sarà un collegamento relativo a un altro file all'interno dello stesso docset.</span><span class="sxs-lookup"><span data-stu-id="eca8b-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="eca8b-247">Definizione di sezione</span><span class="sxs-lookup"><span data-stu-id="eca8b-247">Section definition</span></span>

<span data-ttu-id="eca8b-248"><!-- more info about this would be helpful! --> Potrebbe essere necessario definire una sezione.</span><span class="sxs-lookup"><span data-stu-id="eca8b-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="eca8b-249">Questa sintassi è usata soprattutto nelle tabelle di codice.</span><span class="sxs-lookup"><span data-stu-id="eca8b-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="eca8b-250">Vedere l'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="eca8b-251">Il rendering del testo Markdown della citazione precedente sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="eca8b-252">Selettori</span><span class="sxs-lookup"><span data-stu-id="eca8b-252">Selectors</span></span>

<span data-ttu-id="eca8b-253"><!-- could be more clear! --> È possibile usare un selettore per collegare pagine diverse dello stesso articolo e</span><span class="sxs-lookup"><span data-stu-id="eca8b-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="eca8b-254">consentire ai lettori di passare da una pagina all'altra.</span><span class="sxs-lookup"><span data-stu-id="eca8b-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="eca8b-255">Questa estensione funziona in modo diverso in docs.microsoft.com e in MSDN.</span><span class="sxs-lookup"><span data-stu-id="eca8b-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="eca8b-256">Selettore singolo</span><span class="sxs-lookup"><span data-stu-id="eca8b-256">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="eca8b-257">... il rendering sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="eca8b-266">Selezione multipla</span><span class="sxs-lookup"><span data-stu-id="eca8b-266">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="eca8b-267">... il rendering sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-267">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="eca8b-278">Tabelle</span><span class="sxs-lookup"><span data-stu-id="eca8b-278">Tables</span></span>

<span data-ttu-id="eca8b-279">Il metodo più semplice per creare una tabella in Markdown consiste nell'uso di barre verticali e linee.</span><span class="sxs-lookup"><span data-stu-id="eca8b-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="eca8b-280">Per creare una tabella standard con un titolo, la prima linea deve essere seguita da una linea tratteggiata:</span><span class="sxs-lookup"><span data-stu-id="eca8b-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="eca8b-281">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-281">This renders as follows:</span></span>

|<span data-ttu-id="eca8b-282">This is</span><span class="sxs-lookup"><span data-stu-id="eca8b-282">This is</span></span>   |<span data-ttu-id="eca8b-283">a simple</span><span class="sxs-lookup"><span data-stu-id="eca8b-283">a simple</span></span>   |<span data-ttu-id="eca8b-284">table header</span><span class="sxs-lookup"><span data-stu-id="eca8b-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="eca8b-285">table</span><span class="sxs-lookup"><span data-stu-id="eca8b-285">table</span></span>     |<span data-ttu-id="eca8b-286">data</span><span class="sxs-lookup"><span data-stu-id="eca8b-286">data</span></span>       |<span data-ttu-id="eca8b-287">here</span><span class="sxs-lookup"><span data-stu-id="eca8b-287">here</span></span>        |
|<span data-ttu-id="eca8b-288">it doesn't</span><span class="sxs-lookup"><span data-stu-id="eca8b-288">it doesn't</span></span>|<span data-ttu-id="eca8b-289">actually</span><span class="sxs-lookup"><span data-stu-id="eca8b-289">actually</span></span>   |<span data-ttu-id="eca8b-290">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="eca8b-290">have to line up nicely!</span></span>||

<span data-ttu-id="eca8b-291">È anche possibile creare una tabella senza un titolo.</span><span class="sxs-lookup"><span data-stu-id="eca8b-291">You can also create a table without a header.</span></span> <span data-ttu-id="eca8b-292">Ad esempio, per creare un elenco con più colonne:</span><span class="sxs-lookup"><span data-stu-id="eca8b-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="eca8b-293">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="eca8b-294">This</span><span class="sxs-lookup"><span data-stu-id="eca8b-294">This</span></span> | <span data-ttu-id="eca8b-295">table</span><span class="sxs-lookup"><span data-stu-id="eca8b-295">table</span></span> |
| <span data-ttu-id="eca8b-296">has no</span><span class="sxs-lookup"><span data-stu-id="eca8b-296">has no</span></span> | <span data-ttu-id="eca8b-297">header</span><span class="sxs-lookup"><span data-stu-id="eca8b-297">header</span></span> |

<span data-ttu-id="eca8b-298">È possibile allineare le colonne usando i due punti:</span><span class="sxs-lookup"><span data-stu-id="eca8b-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="eca8b-299">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="eca8b-300">right aligned:</span><span class="sxs-lookup"><span data-stu-id="eca8b-300">right aligned:</span></span>|
|<span data-ttu-id="eca8b-301">:left aligned</span><span class="sxs-lookup"><span data-stu-id="eca8b-301">:left aligned</span></span>     |
|<span data-ttu-id="eca8b-302">:centered        :</span><span class="sxs-lookup"><span data-stu-id="eca8b-302">:centered        :</span></span>|

> [!TIP]
> Docs Authoring Extension per VS Code semplifica l'aggiunta di tabelle Markdown di base.
>
> È anche possibile usare un [generatore di tabelle online](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="eca8b-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="eca8b-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Funziona solo nel sito docs.microsoft.com.

<span data-ttu-id="eca8b-307">Se si crea una tabella in Markdown, la tabella potrebbe espandersi fino alla barra di spostamento destra e diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="eca8b-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="eca8b-308">È possibile risolvere l'inconveniente consentendo l'aggiunta di ritorni a capo alla tabella quando necessario durante il rendering dei documenti.</span><span class="sxs-lookup"><span data-stu-id="eca8b-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="eca8b-309">È sufficiente impostare il ritorno a capo nella tabella con la classe personalizzata `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="eca8b-310">Ecco un esempio di tabella Markdown con tre righe per le quali il ritorno a capo verrà gestito con `div` con il nome di classe `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="eca8b-311">Verrà eseguito il rendering come segue:</span><span class="sxs-lookup"><span data-stu-id="eca8b-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="eca8b-312">Nome</span><span class="sxs-lookup"><span data-stu-id="eca8b-312">Name</span></span>|<span data-ttu-id="eca8b-313">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eca8b-313">Syntax</span></span>|<span data-ttu-id="eca8b-314">Obbligatorio per l'installazione invisibile all'utente?</span><span class="sxs-lookup"><span data-stu-id="eca8b-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="eca8b-315">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eca8b-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="eca8b-316">Quiet</span><span class="sxs-lookup"><span data-stu-id="eca8b-316">Quiet</span></span>|<span data-ttu-id="eca8b-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="eca8b-317">/quiet</span></span>|<span data-ttu-id="eca8b-318">Sì</span><span class="sxs-lookup"><span data-stu-id="eca8b-318">Yes</span></span>|<span data-ttu-id="eca8b-319">Esegue il programma di installazione senza visualizzare elementi dell'interfaccia utente o richieste di conferma.</span><span class="sxs-lookup"><span data-stu-id="eca8b-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="eca8b-320">NoRestart</span><span class="sxs-lookup"><span data-stu-id="eca8b-320">NoRestart</span></span>|<span data-ttu-id="eca8b-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="eca8b-321">/norestart</span></span>|<span data-ttu-id="eca8b-322">No</span><span class="sxs-lookup"><span data-stu-id="eca8b-322">No</span></span>|<span data-ttu-id="eca8b-323">Impedisce qualsiasi tentativo di riavvio.</span><span class="sxs-lookup"><span data-stu-id="eca8b-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="eca8b-324">Per impostazione predefinita l'interfaccia utente richiede una conferma prima del riavvio.</span><span class="sxs-lookup"><span data-stu-id="eca8b-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="eca8b-325">Help</span><span class="sxs-lookup"><span data-stu-id="eca8b-325">Help</span></span>|<span data-ttu-id="eca8b-326">/help</span><span class="sxs-lookup"><span data-stu-id="eca8b-326">/help</span></span>|<span data-ttu-id="eca8b-327">No</span><span class="sxs-lookup"><span data-stu-id="eca8b-327">No</span></span>|<span data-ttu-id="eca8b-328">Rende disponibili la Guida e il Riferimento rapido.</span><span class="sxs-lookup"><span data-stu-id="eca8b-328">Provides help and quick reference.</span></span> <span data-ttu-id="eca8b-329">Visualizza l'uso corretto del comando di impostazione con un elenco di tutte le opzioni e i comportamenti.</span><span class="sxs-lookup"><span data-stu-id="eca8b-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="eca8b-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="eca8b-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eca8b-331">Funziona solo nel sito docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca8b-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="eca8b-332">Occasionalmente potrebbero essere presenti parole molto lunghe nella seconda colonna di una tabella.</span><span class="sxs-lookup"><span data-stu-id="eca8b-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="eca8b-333">Per assicurarsi che vengano divise correttamente, è possibile applicare la classe `mx-tdCol2BreakAll` usando la sintassi per il ritorno a capo `div`, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="eca8b-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="eca8b-334">Tabelle HTML</span><span class="sxs-lookup"><span data-stu-id="eca8b-334">HTML Tables</span></span>

<span data-ttu-id="eca8b-335">Non è consigliabile usare tabelle HTML per docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="eca8b-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="eca8b-336">Non sono leggibili nell'origine, un principio fondamentale di Markdown.</span><span class="sxs-lookup"><span data-stu-id="eca8b-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="eca8b-337">Video</span><span class="sxs-lookup"><span data-stu-id="eca8b-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="eca8b-338">Incorporamento di video in una pagina Markdown</span><span class="sxs-lookup"><span data-stu-id="eca8b-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="eca8b-339">Attualmente OPS può supportare la pubblicazione di video in tre posizioni:</span><span class="sxs-lookup"><span data-stu-id="eca8b-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="eca8b-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="eca8b-340">YouTube</span></span>
- <span data-ttu-id="eca8b-341">Channel 9</span><span class="sxs-lookup"><span data-stu-id="eca8b-341">Channel 9</span></span>
- <span data-ttu-id="eca8b-342">Sistema "OnePlayer" Microsoft</span><span class="sxs-lookup"><span data-stu-id="eca8b-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="eca8b-343">È possibile incorporare un video con la sintassi seguente e OPS ne eseguirà il rendering.</span><span class="sxs-lookup"><span data-stu-id="eca8b-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="eca8b-344">Esempio:</span><span class="sxs-lookup"><span data-stu-id="eca8b-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="eca8b-345">... il rendering sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="eca8b-346">E verrà visualizzato nel modo seguente nelle pagine pubblicate:</span><span class="sxs-lookup"><span data-stu-id="eca8b-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="eca8b-347">L'URL del video CH9 deve iniziare con `https` e terminare con `/player`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="eca8b-348">In caso contrario verrà incorporata l'intera pagina anziché solo il video.</span><span class="sxs-lookup"><span data-stu-id="eca8b-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="eca8b-349">Caricamento di nuovi video</span><span class="sxs-lookup"><span data-stu-id="eca8b-349">Uploading new videos</span></span>

<span data-ttu-id="eca8b-350">Per caricare nuovi video, è consigliabile attenersi al processo seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="eca8b-351">Unirsi al gruppo **docs_video_users** in IDWEB.</span><span class="sxs-lookup"><span data-stu-id="eca8b-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="eca8b-352">Accedere a https://aka.ms/VideoUploadRequest e inserire i dettagli del video.</span><span class="sxs-lookup"><span data-stu-id="eca8b-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="eca8b-353">Sono necessarie le informazioni seguenti. Si noti che nessuna di queste informazioni sarà visibile al pubblico:</span><span class="sxs-lookup"><span data-stu-id="eca8b-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="eca8b-354">Un titolo per il video.</span><span class="sxs-lookup"><span data-stu-id="eca8b-354">A title for your video.</span></span>
    1. <span data-ttu-id="eca8b-355">Un elenco di prodotti/servizi ai quali il video è correlato.</span><span class="sxs-lookup"><span data-stu-id="eca8b-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="eca8b-356">La pagina di destinazione oppure, se la pagine non è ancora disponibile, il docset che ospiterà il video.</span><span class="sxs-lookup"><span data-stu-id="eca8b-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="eca8b-357">Un collegamento al file MP4 per il video. In assenza di un percorso in cui inserire il file, è possibile usare temporaneamente il percorso `\\scratch2\scratch\apex`.</span><span class="sxs-lookup"><span data-stu-id="eca8b-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="eca8b-358">La risoluzione dei file MP4 deve essere 720p o superiore.</span><span class="sxs-lookup"><span data-stu-id="eca8b-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="eca8b-359">Una descrizione del video.</span><span class="sxs-lookup"><span data-stu-id="eca8b-359">A description of the video.</span></span>
1. <span data-ttu-id="eca8b-360">Inviare (salvare) l'elemento.</span><span class="sxs-lookup"><span data-stu-id="eca8b-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="eca8b-361">Entro due giorni lavorativi, il video verrà caricato.</span><span class="sxs-lookup"><span data-stu-id="eca8b-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="eca8b-362">Il collegamento necessario per incorporare il video sarà disponibile nell'elemento di lavoro e sarà risolto *dall'utente*.</span><span class="sxs-lookup"><span data-stu-id="eca8b-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="eca8b-363">Dopo aver recuperato il collegamento video, chiudere l'elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eca8b-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="eca8b-364">Il collegamento video può essere quindi aggiunto al post usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="eca8b-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```