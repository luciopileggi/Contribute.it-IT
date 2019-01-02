---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615836"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="044dd-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="044dd-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="044dd-104">Gli articoli di [docs.microsoft.com](http://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="044dd-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="044dd-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="044dd-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="044dd-106">Dato che il contenuto di Docs è archiviato in GitHub, è possibile usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni.</span><span class="sxs-lookup"><span data-stu-id="044dd-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="044dd-107">In più, Open Publishing Services (OPS) implementa il parser Markdig per Markdown.</span><span class="sxs-lookup"><span data-stu-id="044dd-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="044dd-108">Markdig è altamente compatibile con GFM e aggiunge funzionalità per abilitare funzioni specifiche di Docs.</span><span class="sxs-lookup"><span data-stu-id="044dd-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="044dd-109">Markdig è un processore Markdown per .NET veloce, potente, estensibile e conforme a CommonMark.</span><span class="sxs-lookup"><span data-stu-id="044dd-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="044dd-110">Supporto della community migliorato</span><span class="sxs-lookup"><span data-stu-id="044dd-110">Better community support</span></span>
* <span data-ttu-id="044dd-111">Supporto degli standard migliorato</span><span class="sxs-lookup"><span data-stu-id="044dd-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="044dd-112">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="044dd-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="044dd-113">Titoli</span><span class="sxs-lookup"><span data-stu-id="044dd-113">Headings</span></span>

<span data-ttu-id="044dd-114">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="044dd-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="044dd-115">Le intestazioni devono essere in stile atx. Devono quindi iniziare con un numero di caratteri cancelletto (#) compreso tra 1 e 6, corrispondente in HTML ai livelli di intestazione da H1 a H6.</span><span class="sxs-lookup"><span data-stu-id="044dd-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="044dd-116">Quelli riportati qui sopra sono esempi di intestazioni di livello da 1 a 4.</span><span class="sxs-lookup"><span data-stu-id="044dd-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="044dd-117">Nell'argomento **deve** essere presente una sola intestazione di primo livello (H1), che verrà visualizzata come titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="044dd-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="044dd-118">Se l'intestazione termina con un carattere `#`, perché il rendering sia corretto è necessario aggiungere un altro carattere `#` alla fine,</span><span class="sxs-lookup"><span data-stu-id="044dd-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="044dd-119">come, ad esempio, in `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="044dd-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="044dd-120">Le intestazioni di secondo livello generano il sommario della sezione "In questo articolo", immediatamente dopo il titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="044dd-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="044dd-121">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="044dd-121">Bold and italic text</span></span>

<span data-ttu-id="044dd-122">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="044dd-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="044dd-123">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="044dd-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="044dd-124">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="044dd-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="044dd-125">Citazioni</span><span class="sxs-lookup"><span data-stu-id="044dd-125">Blockquotes</span></span>

<span data-ttu-id="044dd-126">Per creare citazioni, si usa il carattere `>`:</span><span class="sxs-lookup"><span data-stu-id="044dd-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="044dd-127">Ecco il rendering dell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="044dd-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="044dd-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="044dd-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="044dd-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="044dd-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="044dd-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="044dd-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="044dd-131">Elenchi</span><span class="sxs-lookup"><span data-stu-id="044dd-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="044dd-132">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="044dd-132">Unordered list</span></span>

<span data-ttu-id="044dd-133">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="044dd-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="044dd-134">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="044dd-135">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-135">will be rendered as:</span></span>

- <span data-ttu-id="044dd-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="044dd-136">List item 1</span></span>
- <span data-ttu-id="044dd-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="044dd-137">List item 2</span></span>
- <span data-ttu-id="044dd-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="044dd-138">List item 3</span></span>

<span data-ttu-id="044dd-139">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="044dd-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="044dd-140">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="044dd-141">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-141">will be rendered as:</span></span>

- <span data-ttu-id="044dd-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="044dd-142">List item 1</span></span>
  - <span data-ttu-id="044dd-143">List item A</span><span class="sxs-lookup"><span data-stu-id="044dd-143">List item A</span></span>
  - <span data-ttu-id="044dd-144">List item B</span><span class="sxs-lookup"><span data-stu-id="044dd-144">List item B</span></span>
- <span data-ttu-id="044dd-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="044dd-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="044dd-146">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="044dd-146">Ordered list</span></span>

<span data-ttu-id="044dd-147">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="044dd-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="044dd-148">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="044dd-149">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-149">will be rendered as:</span></span>

1. <span data-ttu-id="044dd-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-150">First instruction</span></span>
2. <span data-ttu-id="044dd-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-151">Second instruction</span></span>
3. <span data-ttu-id="044dd-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-152">Third instruction</span></span>

<span data-ttu-id="044dd-153">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="044dd-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="044dd-154">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="044dd-155">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-155">will be rendered as:</span></span>

1. <span data-ttu-id="044dd-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-156">First instruction</span></span>
   1. <span data-ttu-id="044dd-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-157">Sub-instruction</span></span>
   2. <span data-ttu-id="044dd-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-158">Sub-instruction</span></span>
2. <span data-ttu-id="044dd-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="044dd-159">Second instruction</span></span>

<span data-ttu-id="044dd-160">Si noti che si usa '1.'</span><span class="sxs-lookup"><span data-stu-id="044dd-160">Note that we use '1.'</span></span> <span data-ttu-id="044dd-161">per tutte le voci.</span><span class="sxs-lookup"><span data-stu-id="044dd-161">for all entries.</span></span> <span data-ttu-id="044dd-162">Ciò semplifica l'esame delle differenze in occasione di aggiornamenti successivi, quando vengono aggiunti nuovi passaggi o vengono rimossi passaggi esistenti.</span><span class="sxs-lookup"><span data-stu-id="044dd-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="044dd-163">Tables</span><span class="sxs-lookup"><span data-stu-id="044dd-163">Tables</span></span>

<span data-ttu-id="044dd-164">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="044dd-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="044dd-165">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="044dd-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="044dd-166">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="044dd-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="044dd-167">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="044dd-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="044dd-168">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="044dd-169">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-169">will be rendered as:</span></span>

| <span data-ttu-id="044dd-170">Fun</span><span class="sxs-lookup"><span data-stu-id="044dd-170">Fun</span></span>                  | <span data-ttu-id="044dd-171">With</span><span class="sxs-lookup"><span data-stu-id="044dd-171">With</span></span>                 | <span data-ttu-id="044dd-172">Tables</span><span class="sxs-lookup"><span data-stu-id="044dd-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="044dd-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="044dd-173">left-aligned column</span></span>  | <span data-ttu-id="044dd-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="044dd-174">right-aligned column</span></span> | <span data-ttu-id="044dd-175">centered column</span><span class="sxs-lookup"><span data-stu-id="044dd-175">centered column</span></span> |
| <span data-ttu-id="044dd-176">$100</span><span class="sxs-lookup"><span data-stu-id="044dd-176">$100</span></span>                 | <span data-ttu-id="044dd-177">$100</span><span class="sxs-lookup"><span data-stu-id="044dd-177">$100</span></span>                 | <span data-ttu-id="044dd-178">$100</span><span class="sxs-lookup"><span data-stu-id="044dd-178">$100</span></span>            |
| <span data-ttu-id="044dd-179">$10</span><span class="sxs-lookup"><span data-stu-id="044dd-179">$10</span></span>                  | <span data-ttu-id="044dd-180">$10</span><span class="sxs-lookup"><span data-stu-id="044dd-180">$10</span></span>                  | <span data-ttu-id="044dd-181">$10</span><span class="sxs-lookup"><span data-stu-id="044dd-181">$10</span></span>             |
| <span data-ttu-id="044dd-182">$1</span><span class="sxs-lookup"><span data-stu-id="044dd-182">$1</span></span>                   | <span data-ttu-id="044dd-183">$1</span><span class="sxs-lookup"><span data-stu-id="044dd-183">$1</span></span>                   | <span data-ttu-id="044dd-184">$1</span><span class="sxs-lookup"><span data-stu-id="044dd-184">$1</span></span>              |

<span data-ttu-id="044dd-185">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="044dd-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="044dd-186">La [funzionalità per il ritorno a capo nelle tabelle](#table-wrapping) di Markdig, utile per la formattazione di tabelle estese.</span><span class="sxs-lookup"><span data-stu-id="044dd-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="044dd-187">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub.</span><span class="sxs-lookup"><span data-stu-id="044dd-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="044dd-188">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="044dd-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="044dd-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard).</span><span class="sxs-lookup"><span data-stu-id="044dd-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="044dd-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin).</span><span class="sxs-lookup"><span data-stu-id="044dd-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="044dd-191">[Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="044dd-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="044dd-192">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="044dd-192">Links</span></span>

<span data-ttu-id="044dd-193">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="044dd-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="044dd-194">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="044dd-194">For more information on linking, see:</span></span>

- <span data-ttu-id="044dd-195">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="044dd-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="044dd-196">La pagina [Collegamenti](how-to-write-links.md) in questa guida per dettagli sulla sintassi aggiuntiva per i collegamenti disponibile con Markdig.</span><span class="sxs-lookup"><span data-stu-id="044dd-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="044dd-197">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="044dd-197">Code snippets</span></span>

<span data-ttu-id="044dd-198">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="044dd-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="044dd-199">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="044dd-199">For details, see:</span></span>

- <span data-ttu-id="044dd-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="044dd-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="044dd-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="044dd-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="044dd-202">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="044dd-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="044dd-203">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="044dd-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="044dd-204">L'alias dopo i tre apici inversi iniziali '\`' definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="044dd-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="044dd-205">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="044dd-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="044dd-206">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="044dd-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="044dd-207">Nome</span><span class="sxs-lookup"><span data-stu-id="044dd-207">Name</span></span>|<span data-ttu-id="044dd-208">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="044dd-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="044dd-209">Console .NET</span><span class="sxs-lookup"><span data-stu-id="044dd-209">.NET Console</span></span>|<span data-ttu-id="044dd-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="044dd-210">dotnetcli</span></span>|
|<span data-ttu-id="044dd-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="044dd-211">ASP.NET (C#)</span></span>|<span data-ttu-id="044dd-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="044dd-212">aspx-csharp</span></span>|
|<span data-ttu-id="044dd-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="044dd-213">ASP.NET (VB)</span></span>|<span data-ttu-id="044dd-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="044dd-214">aspx-vb</span></span>|
|<span data-ttu-id="044dd-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="044dd-215">AzCopy</span></span>|<span data-ttu-id="044dd-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="044dd-216">azcopy</span></span>|
|<span data-ttu-id="044dd-217">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="044dd-217">Azure CLI</span></span>|<span data-ttu-id="044dd-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="044dd-218">azurecli</span></span>|
|<span data-ttu-id="044dd-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="044dd-219">Azure PowerShell</span></span>|<span data-ttu-id="044dd-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="044dd-220">azurepowershell</span></span>|
|<span data-ttu-id="044dd-221">C++</span><span class="sxs-lookup"><span data-stu-id="044dd-221">C++</span></span>|<span data-ttu-id="044dd-222">cpp</span><span class="sxs-lookup"><span data-stu-id="044dd-222">cpp</span></span>|
|<span data-ttu-id="044dd-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="044dd-223">C++/CX</span></span>|<span data-ttu-id="044dd-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="044dd-224">cppcx</span></span>|
|<span data-ttu-id="044dd-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="044dd-225">C++/WinRT</span></span>|<span data-ttu-id="044dd-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="044dd-226">cppwinrt</span></span>|
|<span data-ttu-id="044dd-227">C#</span><span class="sxs-lookup"><span data-stu-id="044dd-227">C#</span></span>|<span data-ttu-id="044dd-228">csharp</span><span class="sxs-lookup"><span data-stu-id="044dd-228">csharp</span></span>|
|<span data-ttu-id="044dd-229">C# nel browser</span><span class="sxs-lookup"><span data-stu-id="044dd-229">C# in browser</span></span>|<span data-ttu-id="044dd-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="044dd-230">csharp-interactive</span></span>|
|<span data-ttu-id="044dd-231">Console</span><span class="sxs-lookup"><span data-stu-id="044dd-231">Console</span></span>|<span data-ttu-id="044dd-232">console</span><span class="sxs-lookup"><span data-stu-id="044dd-232">console</span></span>|
|<span data-ttu-id="044dd-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="044dd-233">CSHTML</span></span>|<span data-ttu-id="044dd-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="044dd-234">cshtml</span></span>|
|<span data-ttu-id="044dd-235">DAX</span><span class="sxs-lookup"><span data-stu-id="044dd-235">DAX</span></span>|<span data-ttu-id="044dd-236">dax</span><span class="sxs-lookup"><span data-stu-id="044dd-236">dax</span></span>|
|<span data-ttu-id="044dd-237">F#</span><span class="sxs-lookup"><span data-stu-id="044dd-237">F#</span></span>|<span data-ttu-id="044dd-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="044dd-238">fsharp</span></span>|
|<span data-ttu-id="044dd-239">Go</span><span class="sxs-lookup"><span data-stu-id="044dd-239">Go</span></span>|<span data-ttu-id="044dd-240">go</span><span class="sxs-lookup"><span data-stu-id="044dd-240">go</span></span>|
|<span data-ttu-id="044dd-241">HTML</span><span class="sxs-lookup"><span data-stu-id="044dd-241">HTML</span></span>|<span data-ttu-id="044dd-242">html</span><span class="sxs-lookup"><span data-stu-id="044dd-242">html</span></span>|
|<span data-ttu-id="044dd-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="044dd-243">HTTP</span></span>|<span data-ttu-id="044dd-244">http</span><span class="sxs-lookup"><span data-stu-id="044dd-244">http</span></span>|
|<span data-ttu-id="044dd-245">Java</span><span class="sxs-lookup"><span data-stu-id="044dd-245">Java</span></span>|<span data-ttu-id="044dd-246">java</span><span class="sxs-lookup"><span data-stu-id="044dd-246">java</span></span>|
|<span data-ttu-id="044dd-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="044dd-247">JavaScript</span></span>|<span data-ttu-id="044dd-248">javascript</span><span class="sxs-lookup"><span data-stu-id="044dd-248">javascript</span></span>|
|<span data-ttu-id="044dd-249">JSON</span><span class="sxs-lookup"><span data-stu-id="044dd-249">JSON</span></span>|<span data-ttu-id="044dd-250">json</span><span class="sxs-lookup"><span data-stu-id="044dd-250">json</span></span>|
|<span data-ttu-id="044dd-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="044dd-251">Markdown</span></span>|<span data-ttu-id="044dd-252">md</span><span class="sxs-lookup"><span data-stu-id="044dd-252">md</span></span>|
|<span data-ttu-id="044dd-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="044dd-253">NodeJS</span></span>|<span data-ttu-id="044dd-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="044dd-254">nodejs</span></span>|
|<span data-ttu-id="044dd-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="044dd-255">Objective-C</span></span>|<span data-ttu-id="044dd-256">objc</span><span class="sxs-lookup"><span data-stu-id="044dd-256">objc</span></span>|
|<span data-ttu-id="044dd-257">OData</span><span class="sxs-lookup"><span data-stu-id="044dd-257">OData</span></span>|<span data-ttu-id="044dd-258">odata</span><span class="sxs-lookup"><span data-stu-id="044dd-258">odata</span></span>|
|<span data-ttu-id="044dd-259">PHP</span><span class="sxs-lookup"><span data-stu-id="044dd-259">PHP</span></span>|<span data-ttu-id="044dd-260">php</span><span class="sxs-lookup"><span data-stu-id="044dd-260">php</span></span>|
|<span data-ttu-id="044dd-261">PowerApps (separatore decimale punto)</span><span class="sxs-lookup"><span data-stu-id="044dd-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="044dd-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="044dd-262">powerapps-dot</span></span>|
|<span data-ttu-id="044dd-263">PowerApps (separatore decimale virgola)</span><span class="sxs-lookup"><span data-stu-id="044dd-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="044dd-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="044dd-264">powerapps-comma</span></span>|
|<span data-ttu-id="044dd-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="044dd-265">PowerShell</span></span>|<span data-ttu-id="044dd-266">powershell</span><span class="sxs-lookup"><span data-stu-id="044dd-266">powershell</span></span>|
|<span data-ttu-id="044dd-267">Python</span><span class="sxs-lookup"><span data-stu-id="044dd-267">Python</span></span>|<span data-ttu-id="044dd-268">python</span><span class="sxs-lookup"><span data-stu-id="044dd-268">python</span></span>|
|<span data-ttu-id="044dd-269">Q#</span><span class="sxs-lookup"><span data-stu-id="044dd-269">Q#</span></span>|<span data-ttu-id="044dd-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="044dd-270">qsharp</span></span>|
|<span data-ttu-id="044dd-271">R</span><span class="sxs-lookup"><span data-stu-id="044dd-271">R</span></span>|<span data-ttu-id="044dd-272">r</span><span class="sxs-lookup"><span data-stu-id="044dd-272">r</span></span>|
|<span data-ttu-id="044dd-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="044dd-273">Ruby</span></span>|<span data-ttu-id="044dd-274">ruby</span><span class="sxs-lookup"><span data-stu-id="044dd-274">ruby</span></span>|
|<span data-ttu-id="044dd-275">SQL</span><span class="sxs-lookup"><span data-stu-id="044dd-275">SQL</span></span>|<span data-ttu-id="044dd-276">sql</span><span class="sxs-lookup"><span data-stu-id="044dd-276">sql</span></span>|
|<span data-ttu-id="044dd-277">Swift</span><span class="sxs-lookup"><span data-stu-id="044dd-277">Swift</span></span>|<span data-ttu-id="044dd-278">swift</span><span class="sxs-lookup"><span data-stu-id="044dd-278">swift</span></span>|
|<span data-ttu-id="044dd-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="044dd-279">TypeScript</span></span>|<span data-ttu-id="044dd-280">typescript</span><span class="sxs-lookup"><span data-stu-id="044dd-280">typescript</span></span>|
|<span data-ttu-id="044dd-281">VB</span><span class="sxs-lookup"><span data-stu-id="044dd-281">VB</span></span>|<span data-ttu-id="044dd-282">vb</span><span class="sxs-lookup"><span data-stu-id="044dd-282">vb</span></span>|
|<span data-ttu-id="044dd-283">Interfaccia della riga di comando di VSTS</span><span class="sxs-lookup"><span data-stu-id="044dd-283">VSTS CLI</span></span>|<span data-ttu-id="044dd-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="044dd-284">vstscli</span></span>|
|<span data-ttu-id="044dd-285">XAML</span><span class="sxs-lookup"><span data-stu-id="044dd-285">XAML</span></span>|<span data-ttu-id="044dd-286">xaml</span><span class="sxs-lookup"><span data-stu-id="044dd-286">xaml</span></span>|
|<span data-ttu-id="044dd-287">XML</span><span class="sxs-lookup"><span data-stu-id="044dd-287">XML</span></span>|<span data-ttu-id="044dd-288">xml</span><span class="sxs-lookup"><span data-stu-id="044dd-288">xml</span></span>|

<span data-ttu-id="044dd-289">Il nome `csharp-interactive` specifica il linguaggio C# e la capacità di eseguire gli esempi dal browser.</span><span class="sxs-lookup"><span data-stu-id="044dd-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="044dd-290">Questi frammenti di codice vengono compilati ed eseguiti in un contenitore Docker e i risultati dell'esecuzione del programma vengono visualizzati nella finestra del browser dell'utente.</span><span class="sxs-lookup"><span data-stu-id="044dd-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="044dd-291">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="044dd-291">Example: C\#</span></span>

<span data-ttu-id="044dd-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="044dd-292">__Markdown__</span></span>

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

<span data-ttu-id="044dd-293">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="044dd-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="044dd-294">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="044dd-294">Example: SQL</span></span>

<span data-ttu-id="044dd-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="044dd-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="044dd-296">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="044dd-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="044dd-297">Estensioni Markdown personalizzate di OPS</span><span class="sxs-lookup"><span data-stu-id="044dd-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="044dd-298">OPS (Open Publishing Services) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="044dd-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="044dd-299">Markdig aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="044dd-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="044dd-300">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="044dd-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="044dd-301">(vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="044dd-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="044dd-302">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="044dd-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="044dd-303">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:</span><span class="sxs-lookup"><span data-stu-id="044dd-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="044dd-304">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="044dd-304">Note blocks</span></span>
- <span data-ttu-id="044dd-305">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="044dd-305">Include files</span></span>
- <span data-ttu-id="044dd-306">Selettori</span><span class="sxs-lookup"><span data-stu-id="044dd-306">Selectors</span></span>
- <span data-ttu-id="044dd-307">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="044dd-307">Embedded videos</span></span>
- <span data-ttu-id="044dd-308">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="044dd-308">Code snippets/samples</span></span>

<span data-ttu-id="044dd-309">Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="044dd-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="044dd-310">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="044dd-310">Note blocks</span></span>

<span data-ttu-id="044dd-311">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="044dd-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="044dd-312">NOTA</span><span class="sxs-lookup"><span data-stu-id="044dd-312">NOTE</span></span>
- <span data-ttu-id="044dd-313">AVVISO</span><span class="sxs-lookup"><span data-stu-id="044dd-313">WARNING</span></span>
- <span data-ttu-id="044dd-314">SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="044dd-314">TIP</span></span>
- <span data-ttu-id="044dd-315">IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="044dd-315">IMPORTANT</span></span>

<span data-ttu-id="044dd-316">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="044dd-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="044dd-317">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="044dd-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="044dd-318">Esempi:</span><span class="sxs-lookup"><span data-stu-id="044dd-318">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="044dd-319">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="044dd-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="044dd-320">Questa è una NOTA</span><span class="sxs-lookup"><span data-stu-id="044dd-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="044dd-321">Questo è un AVVISO</span><span class="sxs-lookup"><span data-stu-id="044dd-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="044dd-322">Questo è un SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="044dd-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="044dd-323">Questo testo è IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="044dd-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="044dd-324">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="044dd-324">Include files</span></span>

<span data-ttu-id="044dd-325">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig.</span><span class="sxs-lookup"><span data-stu-id="044dd-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="044dd-326">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="044dd-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="044dd-327">Sono disponibili tre tipi di riferimenti di inclusione per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="044dd-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="044dd-328">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="044dd-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="044dd-329">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="044dd-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="044dd-330">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="044dd-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="044dd-331">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (MD),</span><span class="sxs-lookup"><span data-stu-id="044dd-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="044dd-332">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="044dd-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="044dd-333">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="044dd-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="044dd-334">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="044dd-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="044dd-335">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="044dd-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="044dd-336">Usare un file di inclusione ogni volta che è necessario visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="044dd-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="044dd-337">Usare un riferimento di inclusione di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="044dd-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="044dd-338">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="044dd-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="044dd-339">I riferimenti di inclusione non vengono visualizzati nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig.</span><span class="sxs-lookup"><span data-stu-id="044dd-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="044dd-340">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="044dd-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="044dd-341">Verificare che tutto il testo in un file di inclusione sia scritto con frasi complete o che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="044dd-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="044dd-342">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="044dd-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="044dd-343">Non incorporare riferimenti di inclusione in altri file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="044dd-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="044dd-344">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="044dd-344">They are not supported.</span></span>
- <span data-ttu-id="044dd-345">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="044dd-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="044dd-346">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="044dd-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="044dd-347">Se il file di inclusione non contiene immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="044dd-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="044dd-348">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="044dd-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="044dd-349">Usare un file separato con un nome univoco per ogni file di inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="044dd-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="044dd-350">Archiviare il file multimediale nella cartella dei file multimediali associata al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="044dd-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="044dd-351">Non usare un file di inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="044dd-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="044dd-352">I file di inclusione sono pensati come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="044dd-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="044dd-353">Esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="044dd-354">Selettori</span><span class="sxs-lookup"><span data-stu-id="044dd-354">Selectors</span></span>

<span data-ttu-id="044dd-355">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="044dd-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="044dd-356">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="044dd-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="044dd-357">In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="044dd-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="044dd-358">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="044dd-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="044dd-359">A questo punto è possibile fare riferimento a quel file di inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="044dd-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="044dd-360">Di seguito viene illustrato un esempio di selettore:</span><span class="sxs-lookup"><span data-stu-id="044dd-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="044dd-361">Per un esempio di selettori attivi, vedere la [documentazione di Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="044dd-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="044dd-362">Riferimenti di inclusione di codice</span><span class="sxs-lookup"><span data-stu-id="044dd-362">Code include references</span></span>

<span data-ttu-id="044dd-363">Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="044dd-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="044dd-364">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="044dd-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="044dd-365">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="044dd-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="044dd-366">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="044dd-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="044dd-367">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="044dd-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="044dd-368">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="044dd-368">Alt text</span></span>

<span data-ttu-id="044dd-369">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="044dd-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="044dd-370">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="044dd-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="044dd-371">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="044dd-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="044dd-372">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="044dd-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="044dd-373">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="044dd-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="044dd-374">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="044dd-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="044dd-375">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="044dd-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="044dd-376">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="044dd-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="044dd-377">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="044dd-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="044dd-378">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="044dd-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="044dd-379">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="044dd-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="044dd-380">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="044dd-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="044dd-381">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="044dd-381">Angle brackets</span></span>

<span data-ttu-id="044dd-382">Le parentesi acute vengono comunemente usate per indicare un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="044dd-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="044dd-383">Se usate nel testo e non nel codice, le parentesi acute devono essere codificate.</span><span class="sxs-lookup"><span data-stu-id="044dd-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="044dd-384">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="044dd-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="044dd-385">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="044dd-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="044dd-386">Vedere anche:</span><span class="sxs-lookup"><span data-stu-id="044dd-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="044dd-387">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="044dd-387">Markdown resources</span></span>

- <span data-ttu-id="044dd-388">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="044dd-388">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="044dd-389">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="044dd-389">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="044dd-390">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="044dd-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="044dd-391">Guida Markdown</span><span class="sxs-lookup"><span data-stu-id="044dd-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
