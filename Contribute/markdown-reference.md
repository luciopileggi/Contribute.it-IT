---
title: Informazioni di riferimento su Markdown per docs.microsoft.com
description: Informazioni sulle funzionalità e sulla sintassi Markdown usate nella piattaforma Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624739"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="b86f0-103">Informazioni di riferimento su Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="b86f0-103">Docs Markdown reference</span></span>

<span data-ttu-id="b86f0-104">In questo articolo sono elencati in ordine alfabetico gli elementi necessari per scrivere codice Markdown per docs.microsoft.com (Docs).</span><span class="sxs-lookup"><span data-stu-id="b86f0-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="b86f0-105">[Markdown](https://daringfireball.net/projects/markdown/) è un linguaggio di tipo Lightweight Markup Language (LML) con sintassi di formattazione in testo normale.</span><span class="sxs-lookup"><span data-stu-id="b86f0-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="b86f0-106">Docs supporta Markdown conforme a [CommonMark](https://commonmark.org/), analizzato tramite il motore di analisi [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="b86f0-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="b86f0-107">Supporta inoltre estensioni di Markdown personalizzate che offrono una formattazione più avanzata dei contenuti sul sito Docs.</span><span class="sxs-lookup"><span data-stu-id="b86f0-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="b86f0-108">Per scrivere codice Markdown è possibile usare qualsiasi editor di testo, ma è consigliabile [Visual Studio Code](https://code.visualstudio.com/) con [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="b86f0-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="b86f0-109">Docs Authoring Pack offre strumenti di modifica e una funzionalità di anteprima che consente di visualizzare l'aspetto che avranno gli articoli quando ne verrà eseguito il rendering in Docs.</span><span class="sxs-lookup"><span data-stu-id="b86f0-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="b86f0-110">Avvisi (nota, suggerimento, informazione importante, attenzione e avviso)</span><span class="sxs-lookup"><span data-stu-id="b86f0-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="b86f0-111">Per gli avvisi è disponibile un'estensione di Markdown che consente di creare in docs.microsoft.com blocchi di testo in evidenza con colori e icone che indicano il significato del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b86f0-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="b86f0-112">Sono supportati i tipi di avviso seguenti:</span><span class="sxs-lookup"><span data-stu-id="b86f0-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="b86f0-113">L'aspetto degli avvisi in docs.microsoft.com è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="b86f0-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="b86f0-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="b86f0-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="b86f0-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b86f0-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="b86f0-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="b86f0-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="b86f0-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="b86f0-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="b86f0-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="b86f0-119">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="b86f0-119">Angle brackets</span></span>

<span data-ttu-id="b86f0-120">Se nel testo di un file si usano parentesi acute, ad esempio per indicare un segnaposto, è necessario codificarle manualmente.</span><span class="sxs-lookup"><span data-stu-id="b86f0-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="b86f0-121">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="b86f0-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="b86f0-122">Ad esempio, codificare `<script name>` come `&lt;script name&gt;` o `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="b86f0-123">Le parentesi acute non devono essere precedute da caratteri di escape nel testo formattato come codice inline o nei blocchi di codice.</span><span class="sxs-lookup"><span data-stu-id="b86f0-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="b86f0-124">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="b86f0-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="b86f0-125">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="b86f0-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="b86f0-126">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="b86f0-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="b86f0-127">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ&euro;&trade;s</span><span class="sxs-lookup"><span data-stu-id="b86f0-127">Otherwise, you end up with things like this when the file is published: Itâ&euro;&trade;s</span></span>

<span data-ttu-id="b86f0-128">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="b86f0-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="b86f0-129">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="b86f0-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="b86f0-130">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="b86f0-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="b86f0-131">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="b86f0-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="b86f0-132">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="b86f0-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="b86f0-133">Citazioni</span><span class="sxs-lookup"><span data-stu-id="b86f0-133">Blockquotes</span></span>

<span data-ttu-id="b86f0-134">Per creare citazioni, si usa il carattere `>`:</span><span class="sxs-lookup"><span data-stu-id="b86f0-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="b86f0-135">Ecco il rendering dell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="b86f0-136">This is a blockquote.</span><span class="sxs-lookup"><span data-stu-id="b86f0-136">This is a blockquote.</span></span> <span data-ttu-id="b86f0-137">It is usually rendered indented and with a different background color.</span><span class="sxs-lookup"><span data-stu-id="b86f0-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="b86f0-138">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="b86f0-138">Bold and italic text</span></span>

<span data-ttu-id="b86f0-139">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="b86f0-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="b86f0-140">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="b86f0-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="b86f0-141">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="b86f0-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="b86f0-142">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="b86f0-142">Code snippets</span></span>

<span data-ttu-id="b86f0-143">Docs Markdown supporta il posizionamento di frammenti di codice sia inline in una frase sia come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="b86f0-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="b86f0-144">Per altre informazioni, vedere [Come includere codice in Docs](code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="b86f0-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="b86f0-145">Colonne</span><span class="sxs-lookup"><span data-stu-id="b86f0-145">Columns</span></span>

<span data-ttu-id="b86f0-146">L'estensione di Markdown per le **colonne** consente agli autori di Docs di aggiungere layout di contenuto basati su colonna più flessibili e potenti rispetto alle tabelle Markdown di base, che sono adatte solo ai dati tabulari veri e propri.</span><span class="sxs-lookup"><span data-stu-id="b86f0-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="b86f0-147">È possibile aggiungere al massimo quattro colonne e usare l'attributo `span` facoltativo per unire due o più colonne.</span><span class="sxs-lookup"><span data-stu-id="b86f0-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="b86f0-148">La sintassi per le colonne è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="b86f0-149">Le colonne devono contenere solo codice Markdown di base, comprese le immagini.</span><span class="sxs-lookup"><span data-stu-id="b86f0-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="b86f0-150">Non è consigliabile includere intestazioni, tabelle, tabulazioni e altre strutture complesse.</span><span class="sxs-lookup"><span data-stu-id="b86f0-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="b86f0-151">Una riga non può includere contenuto all'esterno della colonna.</span><span class="sxs-lookup"><span data-stu-id="b86f0-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="b86f0-152">Il codice Markdown seguente, ad esempio, crea una colonna che si estende su due larghezze e una colonna standard (senza `span`):</span><span class="sxs-lookup"><span data-stu-id="b86f0-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="b86f0-153">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="b86f0-154">**Questa è una colonna che si estende su due larghezze con molto testo.**</span><span class="sxs-lookup"><span data-stu-id="b86f0-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="b86f0-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="b86f0-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="b86f0-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="b86f0-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="b86f0-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="b86f0-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b86f0-159">**Questa è una colonna a larghezza singola contenente un'immagine.**</span><span class="sxs-lookup"><span data-stu-id="b86f0-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="b86f0-161">Titoli</span><span class="sxs-lookup"><span data-stu-id="b86f0-161">Headings</span></span>

<span data-ttu-id="b86f0-162">Docs supporta sei livelli di intestazioni Markdown:</span><span class="sxs-lookup"><span data-stu-id="b86f0-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="b86f0-163">Deve essere presente uno spazio tra l'ultimo `#` e il testo del titolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="b86f0-164">Ogni file Markdown deve avere una sola intestazione H1.</span><span class="sxs-lookup"><span data-stu-id="b86f0-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="b86f0-165">L'intestazione H1 deve essere il primo contenuto nel file dopo il blocco di metadati YML.</span><span class="sxs-lookup"><span data-stu-id="b86f0-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="b86f0-166">Le intestazioni H2 vengono visualizzate automaticamente nel menu di spostamento a destra del file pubblicato.</span><span class="sxs-lookup"><span data-stu-id="b86f0-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="b86f0-167">Non esistono titoli di livello inferiore. Usare quindi le intestazioni H2 in maniera mirata per facilitare la lettura del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b86f0-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="b86f0-168">Le intestazioni HTML, ad esempio `<h1>`, non sono consigliate e in alcuni casi generano avvisi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="b86f0-169">È possibile creare un collegamento a singole intestazioni in un file usando i [collegamenti a segnalibro](how-to-write-links.md#explicit-anchor-links).</span><span class="sxs-lookup"><span data-stu-id="b86f0-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#explicit-anchor-links).</span></span>

## <a name="html"></a><span data-ttu-id="b86f0-170">HTML</span><span class="sxs-lookup"><span data-stu-id="b86f0-170">HTML</span></span>

<span data-ttu-id="b86f0-171">Benché Markdown supporti HTML inline, non è consigliabile usare il linguaggio HTML per la pubblicazione in Docs poiché, fatta eccezione per un piccolo gruppo di valori, genera avvisi o errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="b86f0-172">Immagini</span><span class="sxs-lookup"><span data-stu-id="b86f0-172">Images</span></span>

<span data-ttu-id="b86f0-173">Per impostazione predefinita, per le immagini sono supportati i tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="b86f0-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="b86f0-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="b86f0-174">.jpg</span></span>
- <span data-ttu-id="b86f0-175">.png</span><span class="sxs-lookup"><span data-stu-id="b86f0-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="b86f0-176">Immagini concettuali standard (Markdown predefinito)</span><span class="sxs-lookup"><span data-stu-id="b86f0-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="b86f0-177">La sintassi Markdown di base per incorporare un'immagine è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="b86f0-178">Dove `<alt text>` è una breve descrizione dell'immagine e `<folder path>` è un percorso relativo all'immagine.</span><span class="sxs-lookup"><span data-stu-id="b86f0-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="b86f0-179">Il testo alternativo è necessario perché gli utenti con problemi di vista possano leggere lo schermo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="b86f0-180">È anche utile se, in presenza di un bug nel sito, non è possibile eseguire il rendering dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b86f0-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="b86f0-181">I caratteri di sottolineatura nel testo alternativo vengono sottoposti a rendering correttamente solo se sono preceduti da una barra rovesciata (`\_`).</span><span class="sxs-lookup"><span data-stu-id="b86f0-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="b86f0-182">Evitare tuttavia di copiare i nomi di file per usarli come testo alternativo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="b86f0-183">Ad esempio, invece di scrivere questo:</span><span class="sxs-lookup"><span data-stu-id="b86f0-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="b86f0-184">Scrivere questo:</span><span class="sxs-lookup"><span data-stu-id="b86f0-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="b86f0-185">Immagini concettuali standard (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="b86f0-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="b86f0-186">L'estensione `:::image:::` personalizzata di Docs supporta immagini standard, immagini complesse e icone.</span><span class="sxs-lookup"><span data-stu-id="b86f0-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="b86f0-187">Per le immagini standard, la sintassi Markdown precedente continuerà a funzionare, ma è consigliabile usare la nuova estensione perché supporta funzionalità più potenti, ad esempio la possibilità di specificare un ambito di localizzazione diverso dall'argomento padre.</span><span class="sxs-lookup"><span data-stu-id="b86f0-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="b86f0-188">Altre funzionalità avanzate, ad esempio la possibilità di selezionare un'immagine dalla raccolta di immagini condivise invece di specificarne una locale, saranno disponibili in futuro.</span><span class="sxs-lookup"><span data-stu-id="b86f0-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="b86f0-189">La nuova sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="b86f0-190">Se `type="content"` (impostazione predefinita), è necessario specificare sia `source` che `alt-text`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="b86f0-191">Immagini complesse con lunghe descrizioni</span><span class="sxs-lookup"><span data-stu-id="b86f0-191">Complex images with long descriptions</span></span>

<span data-ttu-id="b86f0-192">È anche possibile usare questa estensione per aggiungere un'immagine con una lunga descrizione che viene letta dalle utilità per la lettura dello schermo, ma non viene visualizzata nella pagina pubblicata.</span><span class="sxs-lookup"><span data-stu-id="b86f0-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="b86f0-193">Le descrizioni lunghe sono un requisito di accessibilità per immagini complesse, ad esempio i grafici.</span><span class="sxs-lookup"><span data-stu-id="b86f0-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="b86f0-194">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="b86f0-195">Se `type="complex"`, è necessario specificare `source`, `alt-text`, una lunga descrizione e il tag `:::image-end:::`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="b86f0-196">Specifica dell'attributo loc-scope</span><span class="sxs-lookup"><span data-stu-id="b86f0-196">Specifying loc-scope</span></span>

<span data-ttu-id="b86f0-197">A volte l'ambito di localizzazione di un'immagine è diverso da quello dell'articolo o del modulo che la contiene.</span><span class="sxs-lookup"><span data-stu-id="b86f0-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="b86f0-198">Questo può avere effetti negativi sull'esperienza globale, ad esempio se uno screenshot di un prodotto viene accidentalmente localizzato in una lingua per cui il prodotto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b86f0-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="b86f0-199">Per evitare questo problema, è possibile specificare l'attributo facoltativo `loc-scope` nelle immagini di tipo `content` e `complex`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="b86f0-200">Icone</span><span class="sxs-lookup"><span data-stu-id="b86f0-200">Icons</span></span>

<span data-ttu-id="b86f0-201">L'estensione per le immagini supporta le icone, che sono immagini decorative e non devono avere testo alternativo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="b86f0-202">La sintassi per le icone è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="b86f0-203">Se `type="icon"`, è necessario specificare solo `source`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="b86f0-204">File Markdown inclusi</span><span class="sxs-lookup"><span data-stu-id="b86f0-204">Included Markdown files</span></span>

<span data-ttu-id="b86f0-205">Se i file Markdown devono essere ripetuti in più articoli, è possibile usare un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="b86f0-206">La funzionalità delle inclusioni indica a Docs di sostituire il riferimento con il contenuto del file di inclusione in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="b86f0-207">È possibile usare le inclusioni nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b86f0-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="b86f0-208">Inline: riutilizzo di un frammento di testo comune inline all'interno di una frase.</span><span class="sxs-lookup"><span data-stu-id="b86f0-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="b86f0-209">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="b86f0-210">I file di inclusione di tipo Inline o Blocco sono file Markdown (con estensione md)</span><span class="sxs-lookup"><span data-stu-id="b86f0-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="b86f0-211">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="b86f0-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="b86f0-212">I file di inclusione si trovano in genere in una sottodirectory *includes* comune, nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="b86f0-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="b86f0-213">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b86f0-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="b86f0-214">Sintassi delle inclusioni</span><span class="sxs-lookup"><span data-stu-id="b86f0-214">Includes syntax</span></span>

<span data-ttu-id="b86f0-215">L'inclusione di tipo Blocco si trova su una riga a sé stante:</span><span class="sxs-lookup"><span data-stu-id="b86f0-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="b86f0-216">L'inclusione di tipo Inline si trova all'interno di una riga:</span><span class="sxs-lookup"><span data-stu-id="b86f0-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="b86f0-217">Dove `<title>` è il nome del file e `<filepath>` è il percorso relativo del file.</span><span class="sxs-lookup"><span data-stu-id="b86f0-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="b86f0-218">`INCLUDE` deve essere riportato in lettere maiuscole e prima di `<title>` deve essere presente uno spazio.</span><span class="sxs-lookup"><span data-stu-id="b86f0-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="b86f0-219">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="b86f0-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="b86f0-220">Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="b86f0-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="b86f0-221">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="b86f0-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="b86f0-222">Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano sulle estensioni di Docs.</span><span class="sxs-lookup"><span data-stu-id="b86f0-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="b86f0-223">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="b86f0-224">Verificare che tutto il testo in un file di inclusione sia scritto con espressioni o frasi complete che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="b86f0-225">Ignorare questa indicazione significa creare una stringa non traducibile nell'articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="b86f0-226">Non incorporare file di inclusione in altri file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="b86f0-227">Posizionare i file multimediali in un'apposita cartella, specifica della sottodirectory delle inclusioni, ad esempio la cartella `<repo>` */includes/media*.</span><span class="sxs-lookup"><span data-stu-id="b86f0-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="b86f0-228">La directory *media* non deve contenere immagini nella radice.</span><span class="sxs-lookup"><span data-stu-id="b86f0-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="b86f0-229">Se l'inclusione non contiene immagini, non è necessario creare una cartella *media* corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b86f0-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="b86f0-230">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="b86f0-231">Usare un file separato con un nome univoco per ogni inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="b86f0-232">Archiviare il file multimediale nella cartella associata all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="b86f0-233">Non usare un'inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="b86f0-234">Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="b86f0-235">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="b86f0-235">Links</span></span>

<span data-ttu-id="b86f0-236">Per informazioni sulla sintassi per i collegamenti, vedere [Usare i collegamenti nella documentazione](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="b86f0-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="b86f0-237">Elenchi (numerati, puntati, di controllo)</span><span class="sxs-lookup"><span data-stu-id="b86f0-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="b86f0-238">Elenco numerato</span><span class="sxs-lookup"><span data-stu-id="b86f0-238">Numbered list</span></span>

<span data-ttu-id="b86f0-239">Per creare un elenco numerato, è possibile usare sempre il numero 1.</span><span class="sxs-lookup"><span data-stu-id="b86f0-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="b86f0-240">Al momento della pubblicazione, il rendering dei numeri viene eseguito in ordine crescente, come elenco sequenziale.</span><span class="sxs-lookup"><span data-stu-id="b86f0-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="b86f0-241">Per migliorare la leggibilità dell'origine, è possibile incrementare gli elenchi manualmente.</span><span class="sxs-lookup"><span data-stu-id="b86f0-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="b86f0-242">Non usare lettere negli elenchi, neppure in quelli annidati,</span><span class="sxs-lookup"><span data-stu-id="b86f0-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="b86f0-243">poiché non vengono visualizzate correttamente al momento della pubblicazione in Docs. Gli elenchi annidati che usano i numeri vengono visualizzati con lettere minuscole quando vengono pubblicati.</span><span class="sxs-lookup"><span data-stu-id="b86f0-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="b86f0-244">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b86f0-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="b86f0-245">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-245">This renders as follows:</span></span>

1. <span data-ttu-id="b86f0-246">This is</span><span class="sxs-lookup"><span data-stu-id="b86f0-246">This is</span></span>
1. <span data-ttu-id="b86f0-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="b86f0-247">a parent numbered list</span></span>
   1. <span data-ttu-id="b86f0-248">and this is</span><span class="sxs-lookup"><span data-stu-id="b86f0-248">and this is</span></span>
   1. <span data-ttu-id="b86f0-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="b86f0-249">a nested numbered list</span></span>
1. <span data-ttu-id="b86f0-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="b86f0-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="b86f0-251">Elenco puntato</span><span class="sxs-lookup"><span data-stu-id="b86f0-251">Bulleted list</span></span>

<span data-ttu-id="b86f0-252">Per creare un elenco puntato, usare `-` o `*` seguito da uno spazio all'inizio di ogni riga:</span><span class="sxs-lookup"><span data-stu-id="b86f0-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="b86f0-253">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-253">This renders as follows:</span></span>

- <span data-ttu-id="b86f0-254">This is</span><span class="sxs-lookup"><span data-stu-id="b86f0-254">This is</span></span>
- <span data-ttu-id="b86f0-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="b86f0-255">a parent bulleted list</span></span>
  - <span data-ttu-id="b86f0-256">and this is</span><span class="sxs-lookup"><span data-stu-id="b86f0-256">and this is</span></span>
  - <span data-ttu-id="b86f0-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="b86f0-257">a nested bulleted list</span></span>
- <span data-ttu-id="b86f0-258">All done!</span><span class="sxs-lookup"><span data-stu-id="b86f0-258">All done!</span></span>

<span data-ttu-id="b86f0-259">Indipendentemente dalla sintassi scelta, `-` o `*`, usarla in modo coerente all'interno di un articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="b86f0-260">Elenco di controllo</span><span class="sxs-lookup"><span data-stu-id="b86f0-260">Checklist</span></span>

<span data-ttu-id="b86f0-261">Gli elenchi di controllo possono essere usati solo in Docs tramite un'estensione di Markdown personalizzata:</span><span class="sxs-lookup"><span data-stu-id="b86f0-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="b86f0-262">Il rendering di questo esempio in Docs è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="b86f0-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="b86f0-263">List item 1</span></span>
> * <span data-ttu-id="b86f0-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="b86f0-264">List item 2</span></span>
> * <span data-ttu-id="b86f0-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="b86f0-265">List item 3</span></span>

<span data-ttu-id="b86f0-266">Usare elenchi di controllo all'inizio o alla fine di un articolo per riepilogare ciò di cui si parlerà o di cui si è parlato nell'articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="b86f0-267">Non aggiungere elenchi di controllo casuali all'interno degli articoli.</span><span class="sxs-lookup"><span data-stu-id="b86f0-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="b86f0-268">Azione Passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="b86f0-268">Next step action</span></span>

<span data-ttu-id="b86f0-269">È possibile usare un'estensione personalizzata per aggiungere un pulsante di azione Passaggio successivo nelle pagine di Docs.</span><span class="sxs-lookup"><span data-stu-id="b86f0-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="b86f0-270">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="b86f0-271">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b86f0-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="b86f0-272">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b86f0-273">Informazioni sull'aggiunta di codice negli articoli</span><span class="sxs-lookup"><span data-stu-id="b86f0-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="b86f0-274">Nell'azione per il passaggio successivo è possibile usare tutti i collegamenti supportati, incluso un collegamento Markdown a un'altra pagina Web.</span><span class="sxs-lookup"><span data-stu-id="b86f0-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="b86f0-275">Nella maggior parte dei casi, il collegamento all'azione successiva è un collegamento relativo a un altro file all'interno dello stesso docset.</span><span class="sxs-lookup"><span data-stu-id="b86f0-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="b86f0-276">Stringhe non localizzate</span><span class="sxs-lookup"><span data-stu-id="b86f0-276">Non-localized strings</span></span>

<span data-ttu-id="b86f0-277">È possibile usare l'estensione di Markdown personalizzata `no-loc` per identificare le stringhe di contenuto che devono essere ignorate dal processo di localizzazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="b86f0-278">Per tutte le stringhe indicate viene fatta distinzione tra maiuscole e minuscole. In altre parole, la stringa deve corrispondere esattamente per essere ignorata per la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="b86f0-279">Per contrassegnare una singola stringa come non localizzabile, usare questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="b86f0-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="b86f0-280">Nel codice seguente, ad esempio, solo la singola istanza di `Document` verrà ignorata durante il processo di localizzazione:</span><span class="sxs-lookup"><span data-stu-id="b86f0-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="b86f0-281">Usare `\` per applicare una sequenza di escape ai caratteri speciali:</span><span class="sxs-lookup"><span data-stu-id="b86f0-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="b86f0-282">È anche possibile usare i metadati nell'intestazione YAML per contrassegnare come non localizzabili tutte le istanze di una stringa all'interno del file Markdown corrente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="b86f0-283">I metadati no-loc non sono supportati come metadati globali nel file *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="b86f0-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="b86f0-284">La pipeline di localizzazione non legge il file *docfx.json* e quindi i metadati no-loc devono essere aggiunti in ogni singolo file di origine.</span><span class="sxs-lookup"><span data-stu-id="b86f0-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="b86f0-285">Nell'esempio seguente, sia nel campo dei metadati `title` sia nell'intestazione Markdown, la parola `Document` verrà ignorata durante il processo di localizzazione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="b86f0-286">Nel campo dei metadati `description` e nel contenuto principale di Markdown, la parola `document` viene invece localizzata, perché non inizia con una lettera `D` maiuscola.</span><span class="sxs-lookup"><span data-stu-id="b86f0-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="b86f0-287">Selettori</span><span class="sxs-lookup"><span data-stu-id="b86f0-287">Selectors</span></span>

<span data-ttu-id="b86f0-288">I selettori sono elementi dell'interfaccia utente che consentono all'utente di passare da una versione all'altra dello stesso articolo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="b86f0-289">Questi elementi vengono usati in alcuni set di documenti per illustrare le differenze di implementazione tra tecnologie o piattaforme.</span><span class="sxs-lookup"><span data-stu-id="b86f0-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="b86f0-290">Un esempio tipico è il contenuto per sviluppatori relativo a più piattaforme per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="b86f0-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="b86f0-291">Poiché lo stesso selettore Markdown viene aggiunto in ogni file di articolo che prevede l'uso del selettore, è consigliabile inserirlo in un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b86f0-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="b86f0-292">Sarà quindi possibile fare riferimento al file di inclusione in tutti i file di articolo che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="b86f0-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="b86f0-293">Esistono due tipi di selettori: un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="b86f0-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="b86f0-294">Selettore singolo</span><span class="sxs-lookup"><span data-stu-id="b86f0-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="b86f0-295">... il rendering sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="b86f0-304">Selezione multipla</span><span class="sxs-lookup"><span data-stu-id="b86f0-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="b86f0-305">... il rendering sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Piattaforma" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows Universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="b86f0-318">Apice e pedice</span><span class="sxs-lookup"><span data-stu-id="b86f0-318">Subscript and superscript</span></span>

<span data-ttu-id="b86f0-319">È consigliabile usare il formato apice e pedice quando è necessario per assicurare l'accuratezza tecnica, ad esempio quando si scrivono le formule matematiche.</span><span class="sxs-lookup"><span data-stu-id="b86f0-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="b86f0-320">Non usarlo per gli stili non standard, come le note a piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="b86f0-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="b86f0-321">Per il formato apice e pedice, usare il codice HTML:</span><span class="sxs-lookup"><span data-stu-id="b86f0-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="b86f0-322">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-322">This renders as follows:</span></span>

<span data-ttu-id="b86f0-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="b86f0-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="b86f0-324">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-324">This renders as follows:</span></span>

<span data-ttu-id="b86f0-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="b86f0-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="b86f0-326">Tabelle</span><span class="sxs-lookup"><span data-stu-id="b86f0-326">Tables</span></span>

<span data-ttu-id="b86f0-327">Il metodo più semplice per creare una tabella in Markdown consiste nell'uso di barre verticali e linee.</span><span class="sxs-lookup"><span data-stu-id="b86f0-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="b86f0-328">Per creare una tabella standard con un titolo, la prima linea deve essere seguita da una linea tratteggiata:</span><span class="sxs-lookup"><span data-stu-id="b86f0-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="b86f0-329">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-329">This renders as follows:</span></span>

|<span data-ttu-id="b86f0-330">This is</span><span class="sxs-lookup"><span data-stu-id="b86f0-330">This is</span></span>   |<span data-ttu-id="b86f0-331">a simple</span><span class="sxs-lookup"><span data-stu-id="b86f0-331">a simple</span></span>   |<span data-ttu-id="b86f0-332">table header</span><span class="sxs-lookup"><span data-stu-id="b86f0-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="b86f0-333">table</span><span class="sxs-lookup"><span data-stu-id="b86f0-333">table</span></span>     |<span data-ttu-id="b86f0-334">data</span><span class="sxs-lookup"><span data-stu-id="b86f0-334">data</span></span>       |<span data-ttu-id="b86f0-335">here</span><span class="sxs-lookup"><span data-stu-id="b86f0-335">here</span></span>        |
|<span data-ttu-id="b86f0-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="b86f0-336">it doesn't</span></span>|<span data-ttu-id="b86f0-337">actually</span><span class="sxs-lookup"><span data-stu-id="b86f0-337">actually</span></span>   |<span data-ttu-id="b86f0-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="b86f0-338">have to line up nicely!</span></span>||

<span data-ttu-id="b86f0-339">È possibile allineare le colonne usando i due punti:</span><span class="sxs-lookup"><span data-stu-id="b86f0-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="b86f0-340">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="b86f0-340">Renders as follows:</span></span>

| <span data-ttu-id="b86f0-341">Fun</span><span class="sxs-lookup"><span data-stu-id="b86f0-341">Fun</span></span>                  | <span data-ttu-id="b86f0-342">With</span><span class="sxs-lookup"><span data-stu-id="b86f0-342">With</span></span>                 | <span data-ttu-id="b86f0-343">Tabelle</span><span class="sxs-lookup"><span data-stu-id="b86f0-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="b86f0-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="b86f0-344">left-aligned column</span></span>  | <span data-ttu-id="b86f0-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="b86f0-345">right-aligned column</span></span> | <span data-ttu-id="b86f0-346">centered column</span><span class="sxs-lookup"><span data-stu-id="b86f0-346">centered column</span></span> |
| <span data-ttu-id="b86f0-347">$100</span><span class="sxs-lookup"><span data-stu-id="b86f0-347">$100</span></span>                 | <span data-ttu-id="b86f0-348">$100</span><span class="sxs-lookup"><span data-stu-id="b86f0-348">$100</span></span>                 | <span data-ttu-id="b86f0-349">$100</span><span class="sxs-lookup"><span data-stu-id="b86f0-349">$100</span></span>            |
| <span data-ttu-id="b86f0-350">$10</span><span class="sxs-lookup"><span data-stu-id="b86f0-350">$10</span></span>                  | <span data-ttu-id="b86f0-351">$10</span><span class="sxs-lookup"><span data-stu-id="b86f0-351">$10</span></span>                  | <span data-ttu-id="b86f0-352">$10</span><span class="sxs-lookup"><span data-stu-id="b86f0-352">$10</span></span>             |
| <span data-ttu-id="b86f0-353">$1</span><span class="sxs-lookup"><span data-stu-id="b86f0-353">$1</span></span>                   | <span data-ttu-id="b86f0-354">$1</span><span class="sxs-lookup"><span data-stu-id="b86f0-354">$1</span></span>                   | <span data-ttu-id="b86f0-355">$1</span><span class="sxs-lookup"><span data-stu-id="b86f0-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="b86f0-356">Docs Authoring Extension per VS Code semplifica l'aggiunta di tabelle Markdown di base.</span><span class="sxs-lookup"><span data-stu-id="b86f0-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="b86f0-357">È anche possibile usare un [generatore di tabelle online](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="b86f0-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="b86f0-358">Interruzioni di riga all'interno di parole in qualsiasi cella di tabella</span><span class="sxs-lookup"><span data-stu-id="b86f0-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="b86f0-359">Se si usano parole lunghe in una tabella Markdown, la tabella potrebbe espandersi fino alla barra di spostamento destra e diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="b86f0-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="b86f0-360">È possibile risolvere questo problema consentendo al rendering di Docs di inserire automaticamente interruzioni di riga all'interno di parole, quando necessario.</span><span class="sxs-lookup"><span data-stu-id="b86f0-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="b86f0-361">È sufficiente impostare il ritorno a capo nella tabella con la classe personalizzata `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="b86f0-362">Ecco un esempio di tabella Markdown con tre righe per le quali il ritorno a capo verrà gestito con `div` con il nome di classe `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="b86f0-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="b86f0-363">Verrà eseguito il rendering come segue:</span><span class="sxs-lookup"><span data-stu-id="b86f0-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="b86f0-364">Nome</span><span class="sxs-lookup"><span data-stu-id="b86f0-364">Name</span></span>|<span data-ttu-id="b86f0-365">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b86f0-365">Syntax</span></span>|<span data-ttu-id="b86f0-366">Obbligatorio per l'installazione invisibile all'utente?</span><span class="sxs-lookup"><span data-stu-id="b86f0-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="b86f0-367">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b86f0-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="b86f0-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="b86f0-368">Quiet</span></span>|<span data-ttu-id="b86f0-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="b86f0-369">/quiet</span></span>|<span data-ttu-id="b86f0-370">Sì</span><span class="sxs-lookup"><span data-stu-id="b86f0-370">Yes</span></span>|<span data-ttu-id="b86f0-371">Esegue il programma di installazione senza visualizzare elementi dell'interfaccia utente o richieste di conferma.</span><span class="sxs-lookup"><span data-stu-id="b86f0-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="b86f0-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="b86f0-372">NoRestart</span></span>|<span data-ttu-id="b86f0-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="b86f0-373">/norestart</span></span>|<span data-ttu-id="b86f0-374">No</span><span class="sxs-lookup"><span data-stu-id="b86f0-374">No</span></span>|<span data-ttu-id="b86f0-375">Impedisce qualsiasi tentativo di riavvio.</span><span class="sxs-lookup"><span data-stu-id="b86f0-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="b86f0-376">Per impostazione predefinita l'interfaccia utente richiede una conferma prima del riavvio.</span><span class="sxs-lookup"><span data-stu-id="b86f0-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="b86f0-377">Help</span><span class="sxs-lookup"><span data-stu-id="b86f0-377">Help</span></span>|<span data-ttu-id="b86f0-378">/help</span><span class="sxs-lookup"><span data-stu-id="b86f0-378">/help</span></span>|<span data-ttu-id="b86f0-379">No</span><span class="sxs-lookup"><span data-stu-id="b86f0-379">No</span></span>|<span data-ttu-id="b86f0-380">Rende disponibili la Guida e il Riferimento rapido.</span><span class="sxs-lookup"><span data-stu-id="b86f0-380">Provides help and quick reference.</span></span> <span data-ttu-id="b86f0-381">Visualizza l'uso corretto del comando di impostazione con un elenco di tutte le opzioni e i comportamenti.</span><span class="sxs-lookup"><span data-stu-id="b86f0-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="b86f0-382">Interruzioni di riga all'interno di parole nelle celle della seconda colonna della tabella</span><span class="sxs-lookup"><span data-stu-id="b86f0-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="b86f0-383">Può essere opportuno impostare l'inserimento automatico di interruzioni di riga all'interno di parole solo nella seconda colonna di una tabella.</span><span class="sxs-lookup"><span data-stu-id="b86f0-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="b86f0-384">Per limitare le interruzioni alla seconda colonna, applicare la classe `mx-tdCol2BreakAll` usando la sintassi del wrapper `div`, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b86f0-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="b86f0-385">Tabelle di matrici di dati</span><span class="sxs-lookup"><span data-stu-id="b86f0-385">Data matrix tables</span></span>

<span data-ttu-id="b86f0-386">Una tabella di matrici di dati include un'intestazione e una prima colonna ponderata, creando una matrice con una cella vuota in alto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="b86f0-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="b86f0-387">Docs ha un Markdown personalizzato per le tabelle di matrici di dati:</span><span class="sxs-lookup"><span data-stu-id="b86f0-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="b86f0-388">Ogni voce nella prima colonna deve essere in grassetto (`**bold**`); in caso contrario, le tabelle non saranno accessibili per le utilità per la lettura dello schermo o valide per Docs.</span><span class="sxs-lookup"><span data-stu-id="b86f0-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="b86f0-389">Tabelle HTML</span><span class="sxs-lookup"><span data-stu-id="b86f0-389">HTML Tables</span></span>

<span data-ttu-id="b86f0-390">Non è consigliabile usare tabelle HTML per docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b86f0-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="b86f0-391">Non sono leggibili nell'origine, mentre questo è un principio fondamentale di Markdown.</span><span class="sxs-lookup"><span data-stu-id="b86f0-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
