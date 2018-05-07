---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="88212-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="88212-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="88212-104">Gli articoli di docs.microsoft.com sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="88212-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="88212-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="88212-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="88212-106">Dato che il contenuto di Docs è archiviato in GitHub, può usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni.</span><span class="sxs-lookup"><span data-stu-id="88212-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="88212-107">In più, Open Publishing Services (OPS) implementa DocFX Flavored Markdown (DFM),</span><span class="sxs-lookup"><span data-stu-id="88212-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="88212-108">un linguaggio altamente compatibile con GitHub Flavored Markdown (GFM), che aggiunge funzionalità per abilitare funzioni specifiche di Docs.</span><span class="sxs-lookup"><span data-stu-id="88212-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="88212-109">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="88212-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="88212-110">Titoli</span><span class="sxs-lookup"><span data-stu-id="88212-110">Headings</span></span>

<span data-ttu-id="88212-111">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="88212-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="88212-112">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="88212-112">Bold and italic text</span></span>

<span data-ttu-id="88212-113">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="88212-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="88212-114">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="88212-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="88212-115">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="88212-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="88212-116">Elenchi</span><span class="sxs-lookup"><span data-stu-id="88212-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="88212-117">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="88212-117">Unordered list</span></span>

<span data-ttu-id="88212-118">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="88212-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="88212-119">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="88212-120">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88212-120">will be rendered as:</span></span>

- <span data-ttu-id="88212-121">List item 1</span><span class="sxs-lookup"><span data-stu-id="88212-121">List item 1</span></span>
- <span data-ttu-id="88212-122">List item 2</span><span class="sxs-lookup"><span data-stu-id="88212-122">List item 2</span></span>
- <span data-ttu-id="88212-123">List item 3</span><span class="sxs-lookup"><span data-stu-id="88212-123">List item 3</span></span>

<span data-ttu-id="88212-124">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="88212-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="88212-125">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="88212-126">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88212-126">will be rendered as:</span></span>

- <span data-ttu-id="88212-127">List item 1</span><span class="sxs-lookup"><span data-stu-id="88212-127">List item 1</span></span>
  - <span data-ttu-id="88212-128">List item A</span><span class="sxs-lookup"><span data-stu-id="88212-128">List item A</span></span>
  - <span data-ttu-id="88212-129">List item B</span><span class="sxs-lookup"><span data-stu-id="88212-129">List item B</span></span>
- <span data-ttu-id="88212-130">List item 2</span><span class="sxs-lookup"><span data-stu-id="88212-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="88212-131">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="88212-131">Ordered list</span></span>

<span data-ttu-id="88212-132">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="88212-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="88212-133">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="88212-134">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88212-134">will be rendered as:</span></span>

1. <span data-ttu-id="88212-135">First instruction</span><span class="sxs-lookup"><span data-stu-id="88212-135">First instruction</span></span>
2. <span data-ttu-id="88212-136">Second instruction</span><span class="sxs-lookup"><span data-stu-id="88212-136">Second instruction</span></span>
3. <span data-ttu-id="88212-137">Third instruction</span><span class="sxs-lookup"><span data-stu-id="88212-137">Third instruction</span></span>

<span data-ttu-id="88212-138">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="88212-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="88212-139">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="88212-140">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88212-140">will be rendered as:</span></span>

1. <span data-ttu-id="88212-141">First instruction</span><span class="sxs-lookup"><span data-stu-id="88212-141">First instruction</span></span>
    1. <span data-ttu-id="88212-142">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="88212-142">Sub-instruction</span></span>
    2. <span data-ttu-id="88212-143">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="88212-143">Sub-instruction</span></span>
2. <span data-ttu-id="88212-144">Second instruction</span><span class="sxs-lookup"><span data-stu-id="88212-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="88212-145">Tables</span><span class="sxs-lookup"><span data-stu-id="88212-145">Tables</span></span>

<span data-ttu-id="88212-146">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="88212-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="88212-147">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="88212-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="88212-148">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="88212-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="88212-149">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="88212-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="88212-150">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="88212-151">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88212-151">will be rendered as:</span></span>

| <span data-ttu-id="88212-152">Fun</span><span class="sxs-lookup"><span data-stu-id="88212-152">Fun</span></span>                  | <span data-ttu-id="88212-153">With</span><span class="sxs-lookup"><span data-stu-id="88212-153">With</span></span>                 | <span data-ttu-id="88212-154">Tables</span><span class="sxs-lookup"><span data-stu-id="88212-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="88212-155">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="88212-155">left-aligned column</span></span>  | <span data-ttu-id="88212-156">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="88212-156">right-aligned column</span></span> | <span data-ttu-id="88212-157">centered column</span><span class="sxs-lookup"><span data-stu-id="88212-157">centered column</span></span> |
| <span data-ttu-id="88212-158">$100</span><span class="sxs-lookup"><span data-stu-id="88212-158">$100</span></span>                 | <span data-ttu-id="88212-159">$100</span><span class="sxs-lookup"><span data-stu-id="88212-159">$100</span></span>                 | <span data-ttu-id="88212-160">$100</span><span class="sxs-lookup"><span data-stu-id="88212-160">$100</span></span>            |
| <span data-ttu-id="88212-161">$10</span><span class="sxs-lookup"><span data-stu-id="88212-161">$10</span></span>                  | <span data-ttu-id="88212-162">$10</span><span class="sxs-lookup"><span data-stu-id="88212-162">$10</span></span>                  | <span data-ttu-id="88212-163">$10</span><span class="sxs-lookup"><span data-stu-id="88212-163">$10</span></span>             |
| <span data-ttu-id="88212-164">$1</span><span class="sxs-lookup"><span data-stu-id="88212-164">$1</span></span>                   | <span data-ttu-id="88212-165">$1</span><span class="sxs-lookup"><span data-stu-id="88212-165">$1</span></span>                   | <span data-ttu-id="88212-166">$1</span><span class="sxs-lookup"><span data-stu-id="88212-166">$1</span></span>              |

<span data-ttu-id="88212-167">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="88212-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="88212-168">La [funzionalità per i ritorni a capo nelle tabelle](#table-wrapping) di DFM, utile per la formattazione di tabelle estese</span><span class="sxs-lookup"><span data-stu-id="88212-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="88212-169">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub</span><span class="sxs-lookup"><span data-stu-id="88212-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="88212-170">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="88212-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="88212-171">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard)</span><span class="sxs-lookup"><span data-stu-id="88212-171">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="88212-172">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin)</span><span class="sxs-lookup"><span data-stu-id="88212-172">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- <span data-ttu-id="88212-173">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Conversione di tabelle HTML in Markdown)</span><span class="sxs-lookup"><span data-stu-id="88212-173">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)</span></span>

### <a name="links"></a><span data-ttu-id="88212-174">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="88212-174">Links</span></span>

<span data-ttu-id="88212-175">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="88212-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="88212-176">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="88212-176">For more information on linking, see:</span></span>

- <span data-ttu-id="88212-177">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="88212-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="88212-178">La pagina [Collegamenti](how-to-write-links.md) in questa guida per altri dettagli sulla sintassi aggiuntiva per i collegamenti prevista da DFM.</span><span class="sxs-lookup"><span data-stu-id="88212-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="88212-179">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="88212-179">Code snippets</span></span>

<span data-ttu-id="88212-180">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="88212-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="88212-181">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="88212-181">For details, see:</span></span>

- <span data-ttu-id="88212-182">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="88212-182">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="88212-183">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="88212-183">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="88212-184">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="88212-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="88212-185">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="88212-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="88212-186">L'alias dopo i tre apici inversi iniziali '\`' definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="88212-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="88212-187">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="88212-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="88212-188">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="88212-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="88212-189">Nome</span><span class="sxs-lookup"><span data-stu-id="88212-189">Name</span></span>|<span data-ttu-id="88212-190">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="88212-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="88212-191">Console .NET</span><span class="sxs-lookup"><span data-stu-id="88212-191">.NET Console</span></span>|<span data-ttu-id="88212-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="88212-192">dotnetcli</span></span>|
|<span data-ttu-id="88212-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="88212-193">ASP.NET (C#)</span></span>|<span data-ttu-id="88212-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="88212-194">aspx-csharp</span></span>|
|<span data-ttu-id="88212-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="88212-195">ASP.NET (VB)</span></span>|<span data-ttu-id="88212-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="88212-196">aspx-vb</span></span>|
|<span data-ttu-id="88212-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="88212-197">AzCopy</span></span>|<span data-ttu-id="88212-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="88212-198">azcopy</span></span>|
|<span data-ttu-id="88212-199">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="88212-199">Azure CLI</span></span>|<span data-ttu-id="88212-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="88212-200">azurecli</span></span>|
|<span data-ttu-id="88212-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="88212-201">Azure PowerShell</span></span>|<span data-ttu-id="88212-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="88212-202">azurepowershell</span></span>|
|<span data-ttu-id="88212-203">C++</span><span class="sxs-lookup"><span data-stu-id="88212-203">C++</span></span>|<span data-ttu-id="88212-204">cpp</span><span class="sxs-lookup"><span data-stu-id="88212-204">cpp</span></span>|
|<span data-ttu-id="88212-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="88212-205">C++/CX</span></span>|<span data-ttu-id="88212-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="88212-206">cppcx</span></span>|
|<span data-ttu-id="88212-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="88212-207">C++/WinRT</span></span>|<span data-ttu-id="88212-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="88212-208">cppwinrt</span></span>|
|<span data-ttu-id="88212-209">C#</span><span class="sxs-lookup"><span data-stu-id="88212-209">C#</span></span>|<span data-ttu-id="88212-210">csharp</span><span class="sxs-lookup"><span data-stu-id="88212-210">csharp</span></span>|
|<span data-ttu-id="88212-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="88212-211">CSHTML</span></span>|<span data-ttu-id="88212-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="88212-212">cshtml</span></span>|
|<span data-ttu-id="88212-213">DAX</span><span class="sxs-lookup"><span data-stu-id="88212-213">DAX</span></span>|<span data-ttu-id="88212-214">dax</span><span class="sxs-lookup"><span data-stu-id="88212-214">dax</span></span>|
|<span data-ttu-id="88212-215">F#</span><span class="sxs-lookup"><span data-stu-id="88212-215">F#</span></span>|<span data-ttu-id="88212-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="88212-216">fsharp</span></span>|
|<span data-ttu-id="88212-217">Go</span><span class="sxs-lookup"><span data-stu-id="88212-217">Go</span></span>|<span data-ttu-id="88212-218">go</span><span class="sxs-lookup"><span data-stu-id="88212-218">go</span></span>|
|<span data-ttu-id="88212-219">HTML</span><span class="sxs-lookup"><span data-stu-id="88212-219">HTML</span></span>|<span data-ttu-id="88212-220">html</span><span class="sxs-lookup"><span data-stu-id="88212-220">html</span></span>|
|<span data-ttu-id="88212-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="88212-221">HTTP</span></span>|<span data-ttu-id="88212-222">http</span><span class="sxs-lookup"><span data-stu-id="88212-222">http</span></span>|
|<span data-ttu-id="88212-223">Java</span><span class="sxs-lookup"><span data-stu-id="88212-223">Java</span></span>|<span data-ttu-id="88212-224">java</span><span class="sxs-lookup"><span data-stu-id="88212-224">java</span></span>|
|<span data-ttu-id="88212-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="88212-225">JavaScript</span></span>|<span data-ttu-id="88212-226">javascript</span><span class="sxs-lookup"><span data-stu-id="88212-226">javascript</span></span>|
|<span data-ttu-id="88212-227">JSON</span><span class="sxs-lookup"><span data-stu-id="88212-227">JSON</span></span>|<span data-ttu-id="88212-228">json</span><span class="sxs-lookup"><span data-stu-id="88212-228">json</span></span>|
|<span data-ttu-id="88212-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="88212-229">Markdown</span></span>|<span data-ttu-id="88212-230">md</span><span class="sxs-lookup"><span data-stu-id="88212-230">md</span></span>|
|<span data-ttu-id="88212-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="88212-231">NodeJS</span></span>|<span data-ttu-id="88212-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="88212-232">nodejs</span></span>|
|<span data-ttu-id="88212-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="88212-233">Objective-C</span></span>|<span data-ttu-id="88212-234">objc</span><span class="sxs-lookup"><span data-stu-id="88212-234">objc</span></span>|
|<span data-ttu-id="88212-235">OData</span><span class="sxs-lookup"><span data-stu-id="88212-235">OData</span></span>|<span data-ttu-id="88212-236">odata</span><span class="sxs-lookup"><span data-stu-id="88212-236">odata</span></span>|
|<span data-ttu-id="88212-237">PHP</span><span class="sxs-lookup"><span data-stu-id="88212-237">PHP</span></span>|<span data-ttu-id="88212-238">php</span><span class="sxs-lookup"><span data-stu-id="88212-238">php</span></span>|
|<span data-ttu-id="88212-239">Formula PowerApps</span><span class="sxs-lookup"><span data-stu-id="88212-239">Power Apps Formula</span></span>|<span data-ttu-id="88212-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="88212-240">powerappsfl</span></span>|
|<span data-ttu-id="88212-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="88212-241">PowerShell</span></span>|<span data-ttu-id="88212-242">powershell</span><span class="sxs-lookup"><span data-stu-id="88212-242">powershell</span></span>|
|<span data-ttu-id="88212-243">Python</span><span class="sxs-lookup"><span data-stu-id="88212-243">Python</span></span>|<span data-ttu-id="88212-244">python</span><span class="sxs-lookup"><span data-stu-id="88212-244">python</span></span>|
|<span data-ttu-id="88212-245">Q#</span><span class="sxs-lookup"><span data-stu-id="88212-245">Q#</span></span>|<span data-ttu-id="88212-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="88212-246">qsharp</span></span>|
|<span data-ttu-id="88212-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="88212-247">Ruby</span></span>|<span data-ttu-id="88212-248">ruby</span><span class="sxs-lookup"><span data-stu-id="88212-248">ruby</span></span>|
|<span data-ttu-id="88212-249">SQL</span><span class="sxs-lookup"><span data-stu-id="88212-249">SQL</span></span>|<span data-ttu-id="88212-250">sql</span><span class="sxs-lookup"><span data-stu-id="88212-250">sql</span></span>|
|<span data-ttu-id="88212-251">Swift</span><span class="sxs-lookup"><span data-stu-id="88212-251">Swift</span></span>|<span data-ttu-id="88212-252">swift</span><span class="sxs-lookup"><span data-stu-id="88212-252">swift</span></span>|
|<span data-ttu-id="88212-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="88212-253">TypeScript</span></span>|<span data-ttu-id="88212-254">typescript</span><span class="sxs-lookup"><span data-stu-id="88212-254">typescript</span></span>|
|<span data-ttu-id="88212-255">VB</span><span class="sxs-lookup"><span data-stu-id="88212-255">VB</span></span>|<span data-ttu-id="88212-256">vb</span><span class="sxs-lookup"><span data-stu-id="88212-256">vb</span></span>|
|<span data-ttu-id="88212-257">Interfaccia della riga di comando di VSTS</span><span class="sxs-lookup"><span data-stu-id="88212-257">VSTS CLI</span></span>|<span data-ttu-id="88212-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="88212-258">vstscli</span></span>|
|<span data-ttu-id="88212-259">XAML</span><span class="sxs-lookup"><span data-stu-id="88212-259">XAML</span></span>|<span data-ttu-id="88212-260">xaml</span><span class="sxs-lookup"><span data-stu-id="88212-260">xaml</span></span>|
|<span data-ttu-id="88212-261">XML</span><span class="sxs-lookup"><span data-stu-id="88212-261">XML</span></span>|<span data-ttu-id="88212-262">xml</span><span class="sxs-lookup"><span data-stu-id="88212-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="88212-263">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="88212-263">Example: C\#</span></span>

<span data-ttu-id="88212-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="88212-264">__Markdown__</span></span>

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

<span data-ttu-id="88212-265">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="88212-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="88212-266">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="88212-266">Example: SQL</span></span>

<span data-ttu-id="88212-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="88212-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="88212-268">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="88212-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="88212-269">Estensioni Markdown personalizzate di OPS</span><span class="sxs-lookup"><span data-stu-id="88212-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="88212-270">OPS (Open Publishing Services) implementa DocFX Flavored Markdown (DFM), altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="88212-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="88212-271">DFM aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="88212-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="88212-272">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="88212-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="88212-273">(vedere ad esempio "Estensioni DFM e Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="88212-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="88212-274">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="88212-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="88212-275">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità DFM come:</span><span class="sxs-lookup"><span data-stu-id="88212-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="88212-276">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="88212-276">Note blocks</span></span>
- <span data-ttu-id="88212-277">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="88212-277">Includes</span></span>
- <span data-ttu-id="88212-278">Selettori</span><span class="sxs-lookup"><span data-stu-id="88212-278">Selectors</span></span>
- <span data-ttu-id="88212-279">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="88212-279">Embedded videos</span></span>
- <span data-ttu-id="88212-280">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="88212-280">Code snippets/samples</span></span>

<span data-ttu-id="88212-281">Per l'elenco completo, vedere "Estensioni DFM e Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="88212-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="88212-282">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="88212-282">Note blocks</span></span>

<span data-ttu-id="88212-283">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="88212-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="88212-284">NOTA</span><span class="sxs-lookup"><span data-stu-id="88212-284">NOTE</span></span>
- <span data-ttu-id="88212-285">AVVISO</span><span class="sxs-lookup"><span data-stu-id="88212-285">WARNING</span></span>
- <span data-ttu-id="88212-286">SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="88212-286">TIP</span></span>
- <span data-ttu-id="88212-287">IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="88212-287">IMPORTANT</span></span>

<span data-ttu-id="88212-288">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="88212-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="88212-289">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="88212-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="88212-290">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="88212-290">Includes</span></span>

<span data-ttu-id="88212-291">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di DFM.</span><span class="sxs-lookup"><span data-stu-id="88212-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="88212-292">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="88212-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="88212-293">Esistono tre tipi di inclusioni disponibili per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="88212-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="88212-294">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="88212-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="88212-295">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="88212-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="88212-296">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="88212-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="88212-297">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (con estensione md),</span><span class="sxs-lookup"><span data-stu-id="88212-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="88212-298">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="88212-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="88212-299">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="88212-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="88212-300">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="88212-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="88212-301">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="88212-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="88212-302">Usare le inclusioni ogni volta che occorre visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="88212-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="88212-303">Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="88212-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="88212-304">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="88212-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="88212-305">Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano su estensioni DFM.</span><span class="sxs-lookup"><span data-stu-id="88212-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="88212-306">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="88212-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="88212-307">Assicurarsi che tutto il testo in un'inclusione sia scritto con frasi complete o frasi che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="88212-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="88212-308">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="88212-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="88212-309">Non incorporare inclusioni in altre inclusioni.</span><span class="sxs-lookup"><span data-stu-id="88212-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="88212-310">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="88212-310">They are not supported.</span></span>
- <span data-ttu-id="88212-311">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="88212-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="88212-312">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="88212-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="88212-313">Se nell'inclusione non sono contenute immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="88212-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="88212-314">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="88212-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="88212-315">Usare un file separato con un nome univoco per ogni inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="88212-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="88212-316">Archiviare il file multimediale nella cartella associata all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="88212-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="88212-317">Non usare un'inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="88212-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="88212-318">Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="88212-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="88212-319">Selettori</span><span class="sxs-lookup"><span data-stu-id="88212-319">Selectors</span></span>

<span data-ttu-id="88212-320">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="88212-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="88212-321">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="88212-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="88212-322">Esistono attualmente due diversi tipi di selettori in DFM, ovvero un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="88212-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="88212-323">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un'inclusione.</span><span class="sxs-lookup"><span data-stu-id="88212-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="88212-324">A questo punto è possibile fare riferimento a quell'inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="88212-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="88212-325">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="88212-325">Code snippets</span></span>

<span data-ttu-id="88212-326">DFM supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="88212-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="88212-327">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="88212-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="88212-328">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="88212-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="88212-329">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="88212-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="88212-330">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="88212-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="88212-331">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="88212-331">Alt text</span></span>

<span data-ttu-id="88212-332">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="88212-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="88212-333">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="88212-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="88212-334">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="88212-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="88212-335">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="88212-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="88212-336">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="88212-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="88212-337">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="88212-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="88212-338">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="88212-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="88212-339">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="88212-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="88212-340">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="88212-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="88212-341">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="88212-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="88212-342">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="88212-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="88212-343">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="88212-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="88212-344">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="88212-344">Angle brackets</span></span>

<span data-ttu-id="88212-345">Se nel testo (non nel codice) di un file si usano parentesi uncinate per indicare ad esempio un segnaposto, è necessario codificarle manualmente.</span><span class="sxs-lookup"><span data-stu-id="88212-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="88212-346">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="88212-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="88212-347">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="88212-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="88212-348">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="88212-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="88212-349">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="88212-349">Markdown resources</span></span>

- <span data-ttu-id="88212-350">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="88212-350">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="88212-351">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="88212-351">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="88212-352">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="88212-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
