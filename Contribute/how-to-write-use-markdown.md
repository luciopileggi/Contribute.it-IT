---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805727"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="8fbdd-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="8fbdd-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="8fbdd-104">Gli articoli di [docs.microsoft.com](http://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="8fbdd-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="8fbdd-106">Dato che il contenuto di Docs è archiviato in GitHub, è possibile usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="8fbdd-107">In più, Open Publishing Services (OPS) implementa il parser Markdig per Markdown.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="8fbdd-108">Markdig è altamente compatibile con GFM e aggiunge funzionalità per abilitare funzioni specifiche di Docs.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="8fbdd-109">Markdig è un processore Markdown per .NET veloce, potente, estensibile e conforme a CommonMark.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="8fbdd-110">Supporto della community migliorato</span><span class="sxs-lookup"><span data-stu-id="8fbdd-110">Better community support</span></span>
* <span data-ttu-id="8fbdd-111">Supporto degli standard migliorato</span><span class="sxs-lookup"><span data-stu-id="8fbdd-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="8fbdd-112">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="8fbdd-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="8fbdd-113">Titoli</span><span class="sxs-lookup"><span data-stu-id="8fbdd-113">Headings</span></span>

<span data-ttu-id="8fbdd-114">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="8fbdd-115">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="8fbdd-115">Bold and italic text</span></span>

<span data-ttu-id="8fbdd-116">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="8fbdd-117">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="8fbdd-118">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="8fbdd-119">Elenchi</span><span class="sxs-lookup"><span data-stu-id="8fbdd-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="8fbdd-120">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="8fbdd-120">Unordered list</span></span>

<span data-ttu-id="8fbdd-121">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="8fbdd-122">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="8fbdd-123">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-123">will be rendered as:</span></span>

- <span data-ttu-id="8fbdd-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="8fbdd-124">List item 1</span></span>
- <span data-ttu-id="8fbdd-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="8fbdd-125">List item 2</span></span>
- <span data-ttu-id="8fbdd-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="8fbdd-126">List item 3</span></span>

<span data-ttu-id="8fbdd-127">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="8fbdd-128">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="8fbdd-129">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-129">will be rendered as:</span></span>

- <span data-ttu-id="8fbdd-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="8fbdd-130">List item 1</span></span>
  - <span data-ttu-id="8fbdd-131">List item A</span><span class="sxs-lookup"><span data-stu-id="8fbdd-131">List item A</span></span>
  - <span data-ttu-id="8fbdd-132">List item B</span><span class="sxs-lookup"><span data-stu-id="8fbdd-132">List item B</span></span>
- <span data-ttu-id="8fbdd-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="8fbdd-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="8fbdd-134">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="8fbdd-134">Ordered list</span></span>

<span data-ttu-id="8fbdd-135">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="8fbdd-136">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="8fbdd-137">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-137">will be rendered as:</span></span>

1. <span data-ttu-id="8fbdd-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-138">First instruction</span></span>
2. <span data-ttu-id="8fbdd-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-139">Second instruction</span></span>
3. <span data-ttu-id="8fbdd-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-140">Third instruction</span></span>

<span data-ttu-id="8fbdd-141">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="8fbdd-142">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="8fbdd-143">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-143">will be rendered as:</span></span>

1. <span data-ttu-id="8fbdd-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-144">First instruction</span></span>
   1. <span data-ttu-id="8fbdd-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-145">Sub-instruction</span></span>
   2. <span data-ttu-id="8fbdd-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-146">Sub-instruction</span></span>
2. <span data-ttu-id="8fbdd-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="8fbdd-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="8fbdd-148">Tables</span><span class="sxs-lookup"><span data-stu-id="8fbdd-148">Tables</span></span>

<span data-ttu-id="8fbdd-149">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="8fbdd-150">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="8fbdd-151">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="8fbdd-152">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="8fbdd-153">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="8fbdd-154">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-154">will be rendered as:</span></span>

| <span data-ttu-id="8fbdd-155">Fun</span><span class="sxs-lookup"><span data-stu-id="8fbdd-155">Fun</span></span>                  | <span data-ttu-id="8fbdd-156">With</span><span class="sxs-lookup"><span data-stu-id="8fbdd-156">With</span></span>                 | <span data-ttu-id="8fbdd-157">Tables</span><span class="sxs-lookup"><span data-stu-id="8fbdd-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="8fbdd-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="8fbdd-158">left-aligned column</span></span>  | <span data-ttu-id="8fbdd-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="8fbdd-159">right-aligned column</span></span> | <span data-ttu-id="8fbdd-160">centered column</span><span class="sxs-lookup"><span data-stu-id="8fbdd-160">centered column</span></span> |
| <span data-ttu-id="8fbdd-161">$100</span><span class="sxs-lookup"><span data-stu-id="8fbdd-161">$100</span></span>                 | <span data-ttu-id="8fbdd-162">$100</span><span class="sxs-lookup"><span data-stu-id="8fbdd-162">$100</span></span>                 | <span data-ttu-id="8fbdd-163">$100</span><span class="sxs-lookup"><span data-stu-id="8fbdd-163">$100</span></span>            |
| <span data-ttu-id="8fbdd-164">$10</span><span class="sxs-lookup"><span data-stu-id="8fbdd-164">$10</span></span>                  | <span data-ttu-id="8fbdd-165">$10</span><span class="sxs-lookup"><span data-stu-id="8fbdd-165">$10</span></span>                  | <span data-ttu-id="8fbdd-166">$10</span><span class="sxs-lookup"><span data-stu-id="8fbdd-166">$10</span></span>             |
| <span data-ttu-id="8fbdd-167">$1</span><span class="sxs-lookup"><span data-stu-id="8fbdd-167">$1</span></span>                   | <span data-ttu-id="8fbdd-168">$1</span><span class="sxs-lookup"><span data-stu-id="8fbdd-168">$1</span></span>                   | <span data-ttu-id="8fbdd-169">$1</span><span class="sxs-lookup"><span data-stu-id="8fbdd-169">$1</span></span>              |

<span data-ttu-id="8fbdd-170">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="8fbdd-171">La [funzionalità per il ritorno a capo nelle tabelle](#table-wrapping) di Markdig, utile per la formattazione di tabelle estese.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="8fbdd-172">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="8fbdd-173">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="8fbdd-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="8fbdd-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="8fbdd-176">[Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="8fbdd-177">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="8fbdd-177">Links</span></span>

<span data-ttu-id="8fbdd-178">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="8fbdd-179">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-179">For more information on linking, see:</span></span>

- <span data-ttu-id="8fbdd-180">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="8fbdd-181">La pagina [Collegamenti](how-to-write-links.md) in questa guida per dettagli sulla sintassi aggiuntiva per i collegamenti disponibile con Markdig.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-181">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="8fbdd-182">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="8fbdd-182">Code snippets</span></span>

<span data-ttu-id="8fbdd-183">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="8fbdd-184">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-184">For details, see:</span></span>

- <span data-ttu-id="8fbdd-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="8fbdd-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="8fbdd-187">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="8fbdd-188">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="8fbdd-189">L'alias dopo i tre apici inversi iniziali '\`' definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="8fbdd-190">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="8fbdd-191">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="8fbdd-192">Nome</span><span class="sxs-lookup"><span data-stu-id="8fbdd-192">Name</span></span>|<span data-ttu-id="8fbdd-193">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="8fbdd-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="8fbdd-194">Console .NET</span><span class="sxs-lookup"><span data-stu-id="8fbdd-194">.NET Console</span></span>|<span data-ttu-id="8fbdd-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="8fbdd-195">dotnetcli</span></span>|
|<span data-ttu-id="8fbdd-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-196">ASP.NET (C#)</span></span>|<span data-ttu-id="8fbdd-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="8fbdd-197">aspx-csharp</span></span>|
|<span data-ttu-id="8fbdd-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-198">ASP.NET (VB)</span></span>|<span data-ttu-id="8fbdd-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="8fbdd-199">aspx-vb</span></span>|
|<span data-ttu-id="8fbdd-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="8fbdd-200">AzCopy</span></span>|<span data-ttu-id="8fbdd-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="8fbdd-201">azcopy</span></span>|
|<span data-ttu-id="8fbdd-202">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="8fbdd-202">Azure CLI</span></span>|<span data-ttu-id="8fbdd-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="8fbdd-203">azurecli</span></span>|
|<span data-ttu-id="8fbdd-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8fbdd-204">Azure PowerShell</span></span>|<span data-ttu-id="8fbdd-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="8fbdd-205">azurepowershell</span></span>|
|<span data-ttu-id="8fbdd-206">C++</span><span class="sxs-lookup"><span data-stu-id="8fbdd-206">C++</span></span>|<span data-ttu-id="8fbdd-207">cpp</span><span class="sxs-lookup"><span data-stu-id="8fbdd-207">cpp</span></span>|
|<span data-ttu-id="8fbdd-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="8fbdd-208">C++/CX</span></span>|<span data-ttu-id="8fbdd-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="8fbdd-209">cppcx</span></span>|
|<span data-ttu-id="8fbdd-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="8fbdd-210">C++/WinRT</span></span>|<span data-ttu-id="8fbdd-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="8fbdd-211">cppwinrt</span></span>|
|<span data-ttu-id="8fbdd-212">C#</span><span class="sxs-lookup"><span data-stu-id="8fbdd-212">C#</span></span>|<span data-ttu-id="8fbdd-213">csharp</span><span class="sxs-lookup"><span data-stu-id="8fbdd-213">csharp</span></span>|
|<span data-ttu-id="8fbdd-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="8fbdd-214">CSHTML</span></span>|<span data-ttu-id="8fbdd-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="8fbdd-215">cshtml</span></span>|
|<span data-ttu-id="8fbdd-216">DAX</span><span class="sxs-lookup"><span data-stu-id="8fbdd-216">DAX</span></span>|<span data-ttu-id="8fbdd-217">dax</span><span class="sxs-lookup"><span data-stu-id="8fbdd-217">dax</span></span>|
|<span data-ttu-id="8fbdd-218">F#</span><span class="sxs-lookup"><span data-stu-id="8fbdd-218">F#</span></span>|<span data-ttu-id="8fbdd-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="8fbdd-219">fsharp</span></span>|
|<span data-ttu-id="8fbdd-220">Go</span><span class="sxs-lookup"><span data-stu-id="8fbdd-220">Go</span></span>|<span data-ttu-id="8fbdd-221">go</span><span class="sxs-lookup"><span data-stu-id="8fbdd-221">go</span></span>|
|<span data-ttu-id="8fbdd-222">HTML</span><span class="sxs-lookup"><span data-stu-id="8fbdd-222">HTML</span></span>|<span data-ttu-id="8fbdd-223">html</span><span class="sxs-lookup"><span data-stu-id="8fbdd-223">html</span></span>|
|<span data-ttu-id="8fbdd-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="8fbdd-224">HTTP</span></span>|<span data-ttu-id="8fbdd-225">http</span><span class="sxs-lookup"><span data-stu-id="8fbdd-225">http</span></span>|
|<span data-ttu-id="8fbdd-226">Java</span><span class="sxs-lookup"><span data-stu-id="8fbdd-226">Java</span></span>|<span data-ttu-id="8fbdd-227">java</span><span class="sxs-lookup"><span data-stu-id="8fbdd-227">java</span></span>|
|<span data-ttu-id="8fbdd-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="8fbdd-228">JavaScript</span></span>|<span data-ttu-id="8fbdd-229">javascript</span><span class="sxs-lookup"><span data-stu-id="8fbdd-229">javascript</span></span>|
|<span data-ttu-id="8fbdd-230">JSON</span><span class="sxs-lookup"><span data-stu-id="8fbdd-230">JSON</span></span>|<span data-ttu-id="8fbdd-231">json</span><span class="sxs-lookup"><span data-stu-id="8fbdd-231">json</span></span>|
|<span data-ttu-id="8fbdd-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="8fbdd-232">Markdown</span></span>|<span data-ttu-id="8fbdd-233">md</span><span class="sxs-lookup"><span data-stu-id="8fbdd-233">md</span></span>|
|<span data-ttu-id="8fbdd-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="8fbdd-234">NodeJS</span></span>|<span data-ttu-id="8fbdd-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="8fbdd-235">nodejs</span></span>|
|<span data-ttu-id="8fbdd-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="8fbdd-236">Objective-C</span></span>|<span data-ttu-id="8fbdd-237">objc</span><span class="sxs-lookup"><span data-stu-id="8fbdd-237">objc</span></span>|
|<span data-ttu-id="8fbdd-238">OData</span><span class="sxs-lookup"><span data-stu-id="8fbdd-238">OData</span></span>|<span data-ttu-id="8fbdd-239">odata</span><span class="sxs-lookup"><span data-stu-id="8fbdd-239">odata</span></span>|
|<span data-ttu-id="8fbdd-240">PHP</span><span class="sxs-lookup"><span data-stu-id="8fbdd-240">PHP</span></span>|<span data-ttu-id="8fbdd-241">php</span><span class="sxs-lookup"><span data-stu-id="8fbdd-241">php</span></span>|
|<span data-ttu-id="8fbdd-242">Formula PowerApps</span><span class="sxs-lookup"><span data-stu-id="8fbdd-242">Power Apps Formula</span></span>|<span data-ttu-id="8fbdd-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="8fbdd-243">powerappsfl</span></span>|
|<span data-ttu-id="8fbdd-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8fbdd-244">PowerShell</span></span>|<span data-ttu-id="8fbdd-245">powershell</span><span class="sxs-lookup"><span data-stu-id="8fbdd-245">powershell</span></span>|
|<span data-ttu-id="8fbdd-246">Python</span><span class="sxs-lookup"><span data-stu-id="8fbdd-246">Python</span></span>|<span data-ttu-id="8fbdd-247">python</span><span class="sxs-lookup"><span data-stu-id="8fbdd-247">python</span></span>|
|<span data-ttu-id="8fbdd-248">Q#</span><span class="sxs-lookup"><span data-stu-id="8fbdd-248">Q#</span></span>|<span data-ttu-id="8fbdd-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="8fbdd-249">qsharp</span></span>|
|<span data-ttu-id="8fbdd-250">R</span><span class="sxs-lookup"><span data-stu-id="8fbdd-250">R</span></span>|<span data-ttu-id="8fbdd-251">r</span><span class="sxs-lookup"><span data-stu-id="8fbdd-251">r</span></span>|
|<span data-ttu-id="8fbdd-252">Ruby</span><span class="sxs-lookup"><span data-stu-id="8fbdd-252">Ruby</span></span>|<span data-ttu-id="8fbdd-253">ruby</span><span class="sxs-lookup"><span data-stu-id="8fbdd-253">ruby</span></span>|
|<span data-ttu-id="8fbdd-254">SQL</span><span class="sxs-lookup"><span data-stu-id="8fbdd-254">SQL</span></span>|<span data-ttu-id="8fbdd-255">sql</span><span class="sxs-lookup"><span data-stu-id="8fbdd-255">sql</span></span>|
|<span data-ttu-id="8fbdd-256">Swift</span><span class="sxs-lookup"><span data-stu-id="8fbdd-256">Swift</span></span>|<span data-ttu-id="8fbdd-257">swift</span><span class="sxs-lookup"><span data-stu-id="8fbdd-257">swift</span></span>|
|<span data-ttu-id="8fbdd-258">TypeScript</span><span class="sxs-lookup"><span data-stu-id="8fbdd-258">TypeScript</span></span>|<span data-ttu-id="8fbdd-259">typescript</span><span class="sxs-lookup"><span data-stu-id="8fbdd-259">typescript</span></span>|
|<span data-ttu-id="8fbdd-260">VB</span><span class="sxs-lookup"><span data-stu-id="8fbdd-260">VB</span></span>|<span data-ttu-id="8fbdd-261">vb</span><span class="sxs-lookup"><span data-stu-id="8fbdd-261">vb</span></span>|
|<span data-ttu-id="8fbdd-262">Interfaccia della riga di comando di VSTS</span><span class="sxs-lookup"><span data-stu-id="8fbdd-262">VSTS CLI</span></span>|<span data-ttu-id="8fbdd-263">vstscli</span><span class="sxs-lookup"><span data-stu-id="8fbdd-263">vstscli</span></span>|
|<span data-ttu-id="8fbdd-264">XAML</span><span class="sxs-lookup"><span data-stu-id="8fbdd-264">XAML</span></span>|<span data-ttu-id="8fbdd-265">xaml</span><span class="sxs-lookup"><span data-stu-id="8fbdd-265">xaml</span></span>|
|<span data-ttu-id="8fbdd-266">XML</span><span class="sxs-lookup"><span data-stu-id="8fbdd-266">XML</span></span>|<span data-ttu-id="8fbdd-267">xml</span><span class="sxs-lookup"><span data-stu-id="8fbdd-267">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="8fbdd-268">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="8fbdd-268">Example: C\#</span></span>

<span data-ttu-id="8fbdd-269">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="8fbdd-269">__Markdown__</span></span>

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

<span data-ttu-id="8fbdd-270">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="8fbdd-270">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="8fbdd-271">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="8fbdd-271">Example: SQL</span></span>

<span data-ttu-id="8fbdd-272">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="8fbdd-272">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="8fbdd-273">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="8fbdd-273">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="8fbdd-274">Estensioni Markdown personalizzate di OPS</span><span class="sxs-lookup"><span data-stu-id="8fbdd-274">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="8fbdd-275">OPS (Open Publishing Services) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-275">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="8fbdd-276">Markdig aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-276">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="8fbdd-277">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="8fbdd-277">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="8fbdd-278">(vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-278">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="8fbdd-279">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-279">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="8fbdd-280">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-280">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="8fbdd-281">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="8fbdd-281">Note blocks</span></span>
- <span data-ttu-id="8fbdd-282">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="8fbdd-282">Includes</span></span>
- <span data-ttu-id="8fbdd-283">Selettori</span><span class="sxs-lookup"><span data-stu-id="8fbdd-283">Selectors</span></span>
- <span data-ttu-id="8fbdd-284">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="8fbdd-284">Embedded videos</span></span>
- <span data-ttu-id="8fbdd-285">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="8fbdd-285">Code snippets/samples</span></span>

<span data-ttu-id="8fbdd-286">Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-286">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="8fbdd-287">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="8fbdd-287">Note blocks</span></span>

<span data-ttu-id="8fbdd-288">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-288">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="8fbdd-289">NOTA</span><span class="sxs-lookup"><span data-stu-id="8fbdd-289">NOTE</span></span>
- <span data-ttu-id="8fbdd-290">AVVISO</span><span class="sxs-lookup"><span data-stu-id="8fbdd-290">WARNING</span></span>
- <span data-ttu-id="8fbdd-291">SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="8fbdd-291">TIP</span></span>
- <span data-ttu-id="8fbdd-292">IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="8fbdd-292">IMPORTANT</span></span>

<span data-ttu-id="8fbdd-293">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-293">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="8fbdd-294">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-294">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="8fbdd-295">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="8fbdd-295">Includes</span></span>

<span data-ttu-id="8fbdd-296">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-296">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="8fbdd-297">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-297">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="8fbdd-298">Esistono tre tipi di inclusioni disponibili per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-298">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="8fbdd-299">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-299">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="8fbdd-300">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-300">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="8fbdd-301">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-301">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="8fbdd-302">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (con estensione md),</span><span class="sxs-lookup"><span data-stu-id="8fbdd-302">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="8fbdd-303">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-303">It can contain any valid Markdown.</span></span> <span data-ttu-id="8fbdd-304">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-304">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="8fbdd-305">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-305">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="8fbdd-306">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-306">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="8fbdd-307">Usare le inclusioni ogni volta che occorre visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-307">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="8fbdd-308">Usare le inclusioni di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-308">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="8fbdd-309">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-309">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="8fbdd-310">Le inclusioni non vengono visualizzate nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-310">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="8fbdd-311">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-311">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="8fbdd-312">Assicurarsi che tutto il testo in un'inclusione sia scritto con frasi complete o frasi che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-312">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="8fbdd-313">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-313">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="8fbdd-314">Non incorporare inclusioni in altre inclusioni.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-314">Don't embed includes within other includes.</span></span> <span data-ttu-id="8fbdd-315">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-315">They are not supported.</span></span>
- <span data-ttu-id="8fbdd-316">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-316">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="8fbdd-317">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-317">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="8fbdd-318">Se nell'inclusione non sono contenute immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-318">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="8fbdd-319">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-319">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="8fbdd-320">Usare un file separato con un nome univoco per ogni inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-320">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="8fbdd-321">Archiviare il file multimediale nella cartella associata all'inclusione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-321">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="8fbdd-322">Non usare un'inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-322">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="8fbdd-323">Le inclusioni sono pensate come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-323">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="8fbdd-324">Selettori</span><span class="sxs-lookup"><span data-stu-id="8fbdd-324">Selectors</span></span>

<span data-ttu-id="8fbdd-325">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-325">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="8fbdd-326">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-326">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="8fbdd-327">In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-327">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="8fbdd-328">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un'inclusione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-328">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="8fbdd-329">A questo punto è possibile fare riferimento a quell'inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-329">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="8fbdd-330">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="8fbdd-330">Code snippets</span></span>

<span data-ttu-id="8fbdd-331">Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-331">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="8fbdd-332">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-332">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="8fbdd-333">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-333">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="8fbdd-334">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-334">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="8fbdd-335">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="8fbdd-335">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="8fbdd-336">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="8fbdd-336">Alt text</span></span>

<span data-ttu-id="8fbdd-337">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-337">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="8fbdd-338">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-338">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="8fbdd-339">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-339">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="8fbdd-340">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="8fbdd-340">Apostrophes and quotation marks</span></span>

<span data-ttu-id="8fbdd-341">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="8fbdd-341">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="8fbdd-342">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-342">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span>
<span data-ttu-id="8fbdd-343">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="8fbdd-343">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="8fbdd-344">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-344">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="8fbdd-345">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="8fbdd-345">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="8fbdd-346">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="8fbdd-346">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="8fbdd-347">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="8fbdd-347">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="8fbdd-348">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="8fbdd-348">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="8fbdd-349">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="8fbdd-349">Angle brackets</span></span>

<span data-ttu-id="8fbdd-350">Le parentesi acute vengono comunemente usate per indicare un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-350">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="8fbdd-351">Se usate nel testo e non nel codice, le parentesi acute devono essere codificate.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-351">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="8fbdd-352">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-352">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="8fbdd-353">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="8fbdd-353">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="8fbdd-354">Vedere anche:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-354">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="8fbdd-355">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="8fbdd-355">Markdown resources</span></span>

- <span data-ttu-id="8fbdd-356">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-356">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="8fbdd-357">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-357">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="8fbdd-358">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="8fbdd-358">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="8fbdd-359">Guida Markdown</span><span class="sxs-lookup"><span data-stu-id="8fbdd-359">The Markdown Guide</span></span>](https://www.markdownguide.org/)
