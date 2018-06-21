---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: dca1ccba2ae4ebd08b6039f5d780e7a7ac92e79f
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238967"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="c21cc-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="c21cc-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="c21cc-104">Gli articoli di docs.microsoft.com sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="c21cc-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="c21cc-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="c21cc-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="c21cc-106">Dato che il contenuto di Docs è archiviato in GitHub, può usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni.</span><span class="sxs-lookup"><span data-stu-id="c21cc-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="c21cc-107">In più, Open Publishing Services (OPS) implementa il parser Markdig per Markdown.</span><span class="sxs-lookup"><span data-stu-id="c21cc-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="c21cc-108">Markdig è altamente compatibile con GitHub Flavored Markdown (GFM) e aggiunge funzionalità per abilitare funzioni specifiche di Docs.</span><span class="sxs-lookup"><span data-stu-id="c21cc-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="c21cc-109">Markdig è un processore Markdown per .NET veloce, potente, estensibile e conforme a CommonMark.</span><span class="sxs-lookup"><span data-stu-id="c21cc-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="c21cc-110">Supporto della community migliorato</span><span class="sxs-lookup"><span data-stu-id="c21cc-110">Better community support</span></span>
* <span data-ttu-id="c21cc-111">Supporto degli standard migliorato</span><span class="sxs-lookup"><span data-stu-id="c21cc-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="c21cc-112">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="c21cc-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="c21cc-113">Titoli</span><span class="sxs-lookup"><span data-stu-id="c21cc-113">Headings</span></span>

<span data-ttu-id="c21cc-114">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="c21cc-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="c21cc-115">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="c21cc-115">Bold and italic text</span></span>

<span data-ttu-id="c21cc-116">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="c21cc-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="c21cc-117">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="c21cc-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="c21cc-118">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="c21cc-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="c21cc-119">Elenchi</span><span class="sxs-lookup"><span data-stu-id="c21cc-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="c21cc-120">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="c21cc-120">Unordered list</span></span>

<span data-ttu-id="c21cc-121">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="c21cc-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="c21cc-122">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="c21cc-123">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-123">will be rendered as:</span></span>

- <span data-ttu-id="c21cc-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="c21cc-124">List item 1</span></span>
- <span data-ttu-id="c21cc-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="c21cc-125">List item 2</span></span>
- <span data-ttu-id="c21cc-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="c21cc-126">List item 3</span></span>

<span data-ttu-id="c21cc-127">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="c21cc-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="c21cc-128">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="c21cc-129">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-129">will be rendered as:</span></span>

- <span data-ttu-id="c21cc-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="c21cc-130">List item 1</span></span>
  - <span data-ttu-id="c21cc-131">List item A</span><span class="sxs-lookup"><span data-stu-id="c21cc-131">List item A</span></span>
  - <span data-ttu-id="c21cc-132">List item B</span><span class="sxs-lookup"><span data-stu-id="c21cc-132">List item B</span></span>
- <span data-ttu-id="c21cc-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="c21cc-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="c21cc-134">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="c21cc-134">Ordered list</span></span>

<span data-ttu-id="c21cc-135">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c21cc-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="c21cc-136">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="c21cc-137">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-137">will be rendered as:</span></span>

1. <span data-ttu-id="c21cc-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-138">First instruction</span></span>
2. <span data-ttu-id="c21cc-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-139">Second instruction</span></span>
3. <span data-ttu-id="c21cc-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-140">Third instruction</span></span>

<span data-ttu-id="c21cc-141">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="c21cc-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="c21cc-142">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="c21cc-143">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-143">will be rendered as:</span></span>

1. <span data-ttu-id="c21cc-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-144">First instruction</span></span>
    1. <span data-ttu-id="c21cc-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-145">Sub-instruction</span></span>
    2. <span data-ttu-id="c21cc-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-146">Sub-instruction</span></span>
2. <span data-ttu-id="c21cc-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="c21cc-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="c21cc-148">Tables</span><span class="sxs-lookup"><span data-stu-id="c21cc-148">Tables</span></span>

<span data-ttu-id="c21cc-149">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="c21cc-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="c21cc-150">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="c21cc-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="c21cc-151">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="c21cc-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="c21cc-152">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="c21cc-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="c21cc-153">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="c21cc-154">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-154">will be rendered as:</span></span>

| <span data-ttu-id="c21cc-155">Fun</span><span class="sxs-lookup"><span data-stu-id="c21cc-155">Fun</span></span>                  | <span data-ttu-id="c21cc-156">With</span><span class="sxs-lookup"><span data-stu-id="c21cc-156">With</span></span>                 | <span data-ttu-id="c21cc-157">Tables</span><span class="sxs-lookup"><span data-stu-id="c21cc-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="c21cc-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="c21cc-158">left-aligned column</span></span>  | <span data-ttu-id="c21cc-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="c21cc-159">right-aligned column</span></span> | <span data-ttu-id="c21cc-160">centered column</span><span class="sxs-lookup"><span data-stu-id="c21cc-160">centered column</span></span> |
| <span data-ttu-id="c21cc-161">$100</span><span class="sxs-lookup"><span data-stu-id="c21cc-161">$100</span></span>                 | <span data-ttu-id="c21cc-162">$100</span><span class="sxs-lookup"><span data-stu-id="c21cc-162">$100</span></span>                 | <span data-ttu-id="c21cc-163">$100</span><span class="sxs-lookup"><span data-stu-id="c21cc-163">$100</span></span>            |
| <span data-ttu-id="c21cc-164">$10</span><span class="sxs-lookup"><span data-stu-id="c21cc-164">$10</span></span>                  | <span data-ttu-id="c21cc-165">$10</span><span class="sxs-lookup"><span data-stu-id="c21cc-165">$10</span></span>                  | <span data-ttu-id="c21cc-166">$10</span><span class="sxs-lookup"><span data-stu-id="c21cc-166">$10</span></span>             |
| <span data-ttu-id="c21cc-167">$1</span><span class="sxs-lookup"><span data-stu-id="c21cc-167">$1</span></span>                   | <span data-ttu-id="c21cc-168">$1</span><span class="sxs-lookup"><span data-stu-id="c21cc-168">$1</span></span>                   | <span data-ttu-id="c21cc-169">$1</span><span class="sxs-lookup"><span data-stu-id="c21cc-169">$1</span></span>              |

<span data-ttu-id="c21cc-170">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="c21cc-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="c21cc-171">La [funzionalità per i ritorni a capo nelle tabelle](#table-wrapping) di Markdig, utile per la formattazione di tabelle estese</span><span class="sxs-lookup"><span data-stu-id="c21cc-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="c21cc-172">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub</span><span class="sxs-lookup"><span data-stu-id="c21cc-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="c21cc-173">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="c21cc-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="c21cc-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard)</span><span class="sxs-lookup"><span data-stu-id="c21cc-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="c21cc-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin)</span><span class="sxs-lookup"><span data-stu-id="c21cc-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- <span data-ttu-id="c21cc-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Conversione di tabelle HTML in Markdown)</span><span class="sxs-lookup"><span data-stu-id="c21cc-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)</span></span>

### <a name="links"></a><span data-ttu-id="c21cc-177">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="c21cc-177">Links</span></span>

<span data-ttu-id="c21cc-178">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="c21cc-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="c21cc-179">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="c21cc-179">For more information on linking, see:</span></span>

- <span data-ttu-id="c21cc-180">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="c21cc-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="c21cc-181">La pagina [Collegamenti](how-to-write-links.md) in questa guida per altri dettagli sulla sintassi aggiuntiva per i collegamenti fornita da Markdig.</span><span class="sxs-lookup"><span data-stu-id="c21cc-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="c21cc-182">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="c21cc-182">Code snippets</span></span>

<span data-ttu-id="c21cc-183">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="c21cc-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="c21cc-184">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="c21cc-184">For details, see:</span></span>

- <span data-ttu-id="c21cc-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="c21cc-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="c21cc-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="c21cc-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="c21cc-187">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="c21cc-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="c21cc-188">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="c21cc-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="c21cc-189">L'alias dopo i tre apici inversi iniziali '\`' definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="c21cc-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="c21cc-190">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="c21cc-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="c21cc-191">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="c21cc-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="c21cc-192">Nome</span><span class="sxs-lookup"><span data-stu-id="c21cc-192">Name</span></span>|<span data-ttu-id="c21cc-193">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="c21cc-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="c21cc-194">Console .NET</span><span class="sxs-lookup"><span data-stu-id="c21cc-194">.NET Console</span></span>|<span data-ttu-id="c21cc-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="c21cc-195">dotnetcli</span></span>|
|<span data-ttu-id="c21cc-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="c21cc-196">ASP.NET (C#)</span></span>|<span data-ttu-id="c21cc-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="c21cc-197">aspx-csharp</span></span>|
|<span data-ttu-id="c21cc-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="c21cc-198">ASP.NET (VB)</span></span>|<span data-ttu-id="c21cc-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="c21cc-199">aspx-vb</span></span>|
|<span data-ttu-id="c21cc-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="c21cc-200">AzCopy</span></span>|<span data-ttu-id="c21cc-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="c21cc-201">azcopy</span></span>|
|<span data-ttu-id="c21cc-202">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="c21cc-202">Azure CLI</span></span>|<span data-ttu-id="c21cc-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="c21cc-203">azurecli</span></span>|
|<span data-ttu-id="c21cc-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c21cc-204">Azure PowerShell</span></span>|<span data-ttu-id="c21cc-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="c21cc-205">azurepowershell</span></span>|
|<span data-ttu-id="c21cc-206">C++</span><span class="sxs-lookup"><span data-stu-id="c21cc-206">C++</span></span>|<span data-ttu-id="c21cc-207">cpp</span><span class="sxs-lookup"><span data-stu-id="c21cc-207">cpp</span></span>|
|<span data-ttu-id="c21cc-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="c21cc-208">C++/CX</span></span>|<span data-ttu-id="c21cc-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="c21cc-209">cppcx</span></span>|
|<span data-ttu-id="c21cc-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="c21cc-210">C++/WinRT</span></span>|<span data-ttu-id="c21cc-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="c21cc-211">cppwinrt</span></span>|
|<span data-ttu-id="c21cc-212">C#</span><span class="sxs-lookup"><span data-stu-id="c21cc-212">C#</span></span>|<span data-ttu-id="c21cc-213">csharp</span><span class="sxs-lookup"><span data-stu-id="c21cc-213">csharp</span></span>|
|<span data-ttu-id="c21cc-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="c21cc-214">CSHTML</span></span>|<span data-ttu-id="c21cc-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="c21cc-215">cshtml</span></span>|
|<span data-ttu-id="c21cc-216">DAX</span><span class="sxs-lookup"><span data-stu-id="c21cc-216">DAX</span></span>|<span data-ttu-id="c21cc-217">dax</span><span class="sxs-lookup"><span data-stu-id="c21cc-217">dax</span></span>|
|<span data-ttu-id="c21cc-218">F#</span><span class="sxs-lookup"><span data-stu-id="c21cc-218">F#</span></span>|<span data-ttu-id="c21cc-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="c21cc-219">fsharp</span></span>|
|<span data-ttu-id="c21cc-220">Go</span><span class="sxs-lookup"><span data-stu-id="c21cc-220">Go</span></span>|<span data-ttu-id="c21cc-221">go</span><span class="sxs-lookup"><span data-stu-id="c21cc-221">go</span></span>|
|<span data-ttu-id="c21cc-222">HTML</span><span class="sxs-lookup"><span data-stu-id="c21cc-222">HTML</span></span>|<span data-ttu-id="c21cc-223">html</span><span class="sxs-lookup"><span data-stu-id="c21cc-223">html</span></span>|
|<span data-ttu-id="c21cc-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="c21cc-224">HTTP</span></span>|<span data-ttu-id="c21cc-225">http</span><span class="sxs-lookup"><span data-stu-id="c21cc-225">http</span></span>|
|<span data-ttu-id="c21cc-226">Java</span><span class="sxs-lookup"><span data-stu-id="c21cc-226">Java</span></span>|<span data-ttu-id="c21cc-227">java</span><span class="sxs-lookup"><span data-stu-id="c21cc-227">java</span></span>|
|<span data-ttu-id="c21cc-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c21cc-228">JavaScript</span></span>|<span data-ttu-id="c21cc-229">javascript</span><span class="sxs-lookup"><span data-stu-id="c21cc-229">javascript</span></span>|
|<span data-ttu-id="c21cc-230">JSON</span><span class="sxs-lookup"><span data-stu-id="c21cc-230">JSON</span></span>|<span data-ttu-id="c21cc-231">json</span><span class="sxs-lookup"><span data-stu-id="c21cc-231">json</span></span>|
|<span data-ttu-id="c21cc-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="c21cc-232">Markdown</span></span>|<span data-ttu-id="c21cc-233">md</span><span class="sxs-lookup"><span data-stu-id="c21cc-233">md</span></span>|
|<span data-ttu-id="c21cc-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="c21cc-234">NodeJS</span></span>|<span data-ttu-id="c21cc-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="c21cc-235">nodejs</span></span>|
|<span data-ttu-id="c21cc-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c21cc-236">Objective-C</span></span>|<span data-ttu-id="c21cc-237">objc</span><span class="sxs-lookup"><span data-stu-id="c21cc-237">objc</span></span>|
|<span data-ttu-id="c21cc-238">OData</span><span class="sxs-lookup"><span data-stu-id="c21cc-238">OData</span></span>|<span data-ttu-id="c21cc-239">odata</span><span class="sxs-lookup"><span data-stu-id="c21cc-239">odata</span></span>|
|<span data-ttu-id="c21cc-240">PHP</span><span class="sxs-lookup"><span data-stu-id="c21cc-240">PHP</span></span>|<span data-ttu-id="c21cc-241">php</span><span class="sxs-lookup"><span data-stu-id="c21cc-241">php</span></span>|
|<span data-ttu-id="c21cc-242">Formula PowerApps</span><span class="sxs-lookup"><span data-stu-id="c21cc-242">Power Apps Formula</span></span>|<span data-ttu-id="c21cc-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="c21cc-243">powerappsfl</span></span>|
|<span data-ttu-id="c21cc-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c21cc-244">PowerShell</span></span>|<span data-ttu-id="c21cc-245">powershell</span><span class="sxs-lookup"><span data-stu-id="c21cc-245">powershell</span></span>|
|<span data-ttu-id="c21cc-246">Python</span><span class="sxs-lookup"><span data-stu-id="c21cc-246">Python</span></span>|<span data-ttu-id="c21cc-247">python</span><span class="sxs-lookup"><span data-stu-id="c21cc-247">python</span></span>|
|<span data-ttu-id="c21cc-248">Q#</span><span class="sxs-lookup"><span data-stu-id="c21cc-248">Q#</span></span>|<span data-ttu-id="c21cc-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="c21cc-249">qsharp</span></span>|
|<span data-ttu-id="c21cc-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="c21cc-250">Ruby</span></span>|<span data-ttu-id="c21cc-251">ruby</span><span class="sxs-lookup"><span data-stu-id="c21cc-251">ruby</span></span>|
|<span data-ttu-id="c21cc-252">SQL</span><span class="sxs-lookup"><span data-stu-id="c21cc-252">SQL</span></span>|<span data-ttu-id="c21cc-253">sql</span><span class="sxs-lookup"><span data-stu-id="c21cc-253">sql</span></span>|
|<span data-ttu-id="c21cc-254">Swift</span><span class="sxs-lookup"><span data-stu-id="c21cc-254">Swift</span></span>|<span data-ttu-id="c21cc-255">swift</span><span class="sxs-lookup"><span data-stu-id="c21cc-255">swift</span></span>|
|<span data-ttu-id="c21cc-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="c21cc-256">TypeScript</span></span>|<span data-ttu-id="c21cc-257">typescript</span><span class="sxs-lookup"><span data-stu-id="c21cc-257">typescript</span></span>|
|<span data-ttu-id="c21cc-258">VB</span><span class="sxs-lookup"><span data-stu-id="c21cc-258">VB</span></span>|<span data-ttu-id="c21cc-259">vb</span><span class="sxs-lookup"><span data-stu-id="c21cc-259">vb</span></span>|
|<span data-ttu-id="c21cc-260">Interfaccia della riga di comando di VSTS</span><span class="sxs-lookup"><span data-stu-id="c21cc-260">VSTS CLI</span></span>|<span data-ttu-id="c21cc-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="c21cc-261">vstscli</span></span>|
|<span data-ttu-id="c21cc-262">XAML</span><span class="sxs-lookup"><span data-stu-id="c21cc-262">XAML</span></span>|<span data-ttu-id="c21cc-263">xaml</span><span class="sxs-lookup"><span data-stu-id="c21cc-263">xaml</span></span>|
|<span data-ttu-id="c21cc-264">XML</span><span class="sxs-lookup"><span data-stu-id="c21cc-264">XML</span></span>|<span data-ttu-id="c21cc-265">xml</span><span class="sxs-lookup"><span data-stu-id="c21cc-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="c21cc-266">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="c21cc-266">Example: C\#</span></span>

<span data-ttu-id="c21cc-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="c21cc-267">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="c21cc-268">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="c21cc-268">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="c21cc-269">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="c21cc-269">Example: SQL</span></span>

<span data-ttu-id="c21cc-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="c21cc-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="c21cc-271">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="c21cc-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="c21cc-272">Estensioni Markdown personalizzate di OPS</span><span class="sxs-lookup"><span data-stu-id="c21cc-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="c21cc-273">OPS (Open Publishing Services) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="c21cc-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="c21cc-274">Markdig aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="c21cc-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="c21cc-275">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="c21cc-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="c21cc-276">(vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="c21cc-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="c21cc-277">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="c21cc-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="c21cc-278">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:</span><span class="sxs-lookup"><span data-stu-id="c21cc-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="c21cc-279">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="c21cc-279">Note blocks</span></span>
- <span data-ttu-id="c21cc-280">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="c21cc-280">Includes</span></span>
- <span data-ttu-id="c21cc-281">Selettori</span><span class="sxs-lookup"><span data-stu-id="c21cc-281">Selectors</span></span>
- <span data-ttu-id="c21cc-282">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="c21cc-282">Embedded videos</span></span>
- <span data-ttu-id="c21cc-283">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="c21cc-283">Code snippets/samples</span></span>

<span data-ttu-id="c21cc-284">Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="c21cc-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="c21cc-285">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="c21cc-285">Note blocks</span></span>

<span data-ttu-id="c21cc-286">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="c21cc-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="c21cc-287">NOTA</span><span class="sxs-lookup"><span data-stu-id="c21cc-287">NOTE</span></span>
- <span data-ttu-id="c21cc-288">AVVISO</span><span class="sxs-lookup"><span data-stu-id="c21cc-288">WARNING</span></span>
- <span data-ttu-id="c21cc-289">SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="c21cc-289">TIP</span></span>
- <span data-ttu-id="c21cc-290">IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="c21cc-290">IMPORTANT</span></span>

<span data-ttu-id="c21cc-291">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="c21cc-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="c21cc-292">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="c21cc-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="c21cc-293">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="c21cc-293">Includes</span></span>

<span data-ttu-id="c21cc-294">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig.</span><span class="sxs-lookup"><span data-stu-id="c21cc-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="c21cc-295">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="c21cc-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="c21cc-296">Esistono tre tipi di inclusioni disponibili per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="c21cc-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="c21cc-297">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="c21cc-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="c21cc-298">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="c21cc-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="c21cc-299">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="c21cc-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="c21cc-300">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (con estensione md),</span><span class="sxs-lookup"><span data-stu-id="c21cc-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="c21cc-301">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="c21cc-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="c21cc-302">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="c21cc-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="c21cc-303">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c21cc-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="c21cc-304">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="c21cc-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="c21cc-305">Usare le inclusioni ogni volta che occorre visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="c21cc-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="c21cc-306">Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="c21cc-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="c21cc-307">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="c21cc-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="c21cc-308">Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig.</span><span class="sxs-lookup"><span data-stu-id="c21cc-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="c21cc-309">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c21cc-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="c21cc-310">Assicurarsi che tutto il testo in un'inclusione sia scritto con frasi complete o frasi che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="c21cc-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="c21cc-311">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="c21cc-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="c21cc-312">Non incorporare inclusioni in altre inclusioni.</span><span class="sxs-lookup"><span data-stu-id="c21cc-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="c21cc-313">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c21cc-313">They are not supported.</span></span>
- <span data-ttu-id="c21cc-314">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="c21cc-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="c21cc-315">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="c21cc-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="c21cc-316">Se nell'inclusione non sono contenute immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="c21cc-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="c21cc-317">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="c21cc-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="c21cc-318">Usare un file separato con un nome univoco per ogni inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="c21cc-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="c21cc-319">Archiviare il file multimediale nella cartella associata all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="c21cc-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="c21cc-320">Non usare un'inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="c21cc-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="c21cc-321">Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="c21cc-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="c21cc-322">Selettori</span><span class="sxs-lookup"><span data-stu-id="c21cc-322">Selectors</span></span>

<span data-ttu-id="c21cc-323">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="c21cc-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="c21cc-324">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="c21cc-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="c21cc-325">In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="c21cc-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="c21cc-326">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un'inclusione.</span><span class="sxs-lookup"><span data-stu-id="c21cc-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="c21cc-327">A questo punto è possibile fare riferimento a quell'inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="c21cc-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="c21cc-328">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="c21cc-328">Code snippets</span></span>

<span data-ttu-id="c21cc-329">Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="c21cc-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="c21cc-330">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="c21cc-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="c21cc-331">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="c21cc-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="c21cc-332">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="c21cc-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="c21cc-333">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="c21cc-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="c21cc-334">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="c21cc-334">Alt text</span></span>

<span data-ttu-id="c21cc-335">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c21cc-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="c21cc-336">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="c21cc-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="c21cc-337">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="c21cc-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="c21cc-338">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="c21cc-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="c21cc-339">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="c21cc-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="c21cc-340">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="c21cc-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="c21cc-341">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="c21cc-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="c21cc-342">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="c21cc-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="c21cc-343">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="c21cc-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="c21cc-344">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="c21cc-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="c21cc-345">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="c21cc-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="c21cc-346">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="c21cc-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="c21cc-347">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="c21cc-347">Angle brackets</span></span>

<span data-ttu-id="c21cc-348">Se nel testo (non nel codice) di un file si usano parentesi uncinate per indicare ad esempio un segnaposto, è necessario codificarle manualmente.</span><span class="sxs-lookup"><span data-stu-id="c21cc-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="c21cc-349">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="c21cc-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="c21cc-350">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="c21cc-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="c21cc-351">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c21cc-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="c21cc-352">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="c21cc-352">Markdown resources</span></span>

- <span data-ttu-id="c21cc-353">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="c21cc-353">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="c21cc-354">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="c21cc-354">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="c21cc-355">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="c21cc-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
