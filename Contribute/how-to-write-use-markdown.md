---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 8613d525afc11caf9ec760c4f15ea44010781634
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245896"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="e0b9b-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="e0b9b-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="e0b9b-104">Gli articoli di [docs.microsoft.com](http://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="e0b9b-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="e0b9b-106">Dato che il contenuto di Docs è archiviato in GitHub, è possibile usare un superset di Markdown denominato [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per esigenze di formattazione comuni.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="e0b9b-107">In più, Open Publishing Services (OPS) implementa il parser Markdig per Markdown.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="e0b9b-108">Markdig è altamente compatibile con GFM e aggiunge funzionalità per abilitare funzioni specifiche di Docs.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="e0b9b-109">Markdig è un processore Markdown per .NET veloce, potente, estensibile e conforme a CommonMark.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="e0b9b-110">Supporto della community migliorato</span><span class="sxs-lookup"><span data-stu-id="e0b9b-110">Better community support</span></span>
* <span data-ttu-id="e0b9b-111">Supporto degli standard migliorato</span><span class="sxs-lookup"><span data-stu-id="e0b9b-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="e0b9b-112">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="e0b9b-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="e0b9b-113">Titoli</span><span class="sxs-lookup"><span data-stu-id="e0b9b-113">Headings</span></span>

<span data-ttu-id="e0b9b-114">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="e0b9b-115">Le intestazioni devono essere in stile atx. Devono quindi iniziare con un numero di caratteri cancelletto (#) compreso tra 1 e 6, corrispondente in HTML ai livelli di intestazione da H1 a H6.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="e0b9b-116">Quelli riportati qui sopra sono esempi di intestazioni di livello da 1 a 4.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="e0b9b-117">Nell'argomento **deve** essere presente una sola intestazione di primo livello (H1), che verrà visualizzata come titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="e0b9b-118">Se l'intestazione termina con un carattere `#`, perché il rendering sia corretto è necessario aggiungere un altro carattere `#` alla fine,</span><span class="sxs-lookup"><span data-stu-id="e0b9b-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="e0b9b-119">come, ad esempio, in `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="e0b9b-120">Le intestazioni di secondo livello generano il sommario della sezione "In questo articolo", immediatamente dopo il titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="e0b9b-121">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="e0b9b-121">Bold and italic text</span></span>

<span data-ttu-id="e0b9b-122">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="e0b9b-123">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="e0b9b-124">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="e0b9b-125">Citazioni</span><span class="sxs-lookup"><span data-stu-id="e0b9b-125">Blockquotes</span></span>

<span data-ttu-id="e0b9b-126">Per creare citazioni, si usa il carattere `>`:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="e0b9b-127">Ecco il rendering dell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="e0b9b-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="e0b9b-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="e0b9b-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="e0b9b-131">Elenchi</span><span class="sxs-lookup"><span data-stu-id="e0b9b-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="e0b9b-132">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="e0b9b-132">Unordered list</span></span>

<span data-ttu-id="e0b9b-133">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="e0b9b-134">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="e0b9b-135">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-135">will be rendered as:</span></span>

- <span data-ttu-id="e0b9b-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="e0b9b-136">List item 1</span></span>
- <span data-ttu-id="e0b9b-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="e0b9b-137">List item 2</span></span>
- <span data-ttu-id="e0b9b-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="e0b9b-138">List item 3</span></span>

<span data-ttu-id="e0b9b-139">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="e0b9b-140">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="e0b9b-141">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-141">will be rendered as:</span></span>

- <span data-ttu-id="e0b9b-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="e0b9b-142">List item 1</span></span>
  - <span data-ttu-id="e0b9b-143">List item A</span><span class="sxs-lookup"><span data-stu-id="e0b9b-143">List item A</span></span>
  - <span data-ttu-id="e0b9b-144">List item B</span><span class="sxs-lookup"><span data-stu-id="e0b9b-144">List item B</span></span>
- <span data-ttu-id="e0b9b-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="e0b9b-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="e0b9b-146">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="e0b9b-146">Ordered list</span></span>

<span data-ttu-id="e0b9b-147">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="e0b9b-148">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="e0b9b-149">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-149">will be rendered as:</span></span>

1. <span data-ttu-id="e0b9b-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-150">First instruction</span></span>
2. <span data-ttu-id="e0b9b-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-151">Second instruction</span></span>
3. <span data-ttu-id="e0b9b-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-152">Third instruction</span></span>

<span data-ttu-id="e0b9b-153">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="e0b9b-154">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="e0b9b-155">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-155">will be rendered as:</span></span>

1. <span data-ttu-id="e0b9b-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-156">First instruction</span></span>
   1. <span data-ttu-id="e0b9b-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-157">Sub-instruction</span></span>
   2. <span data-ttu-id="e0b9b-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-158">Sub-instruction</span></span>
2. <span data-ttu-id="e0b9b-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="e0b9b-159">Second instruction</span></span>

<span data-ttu-id="e0b9b-160">Si noti che si usa '1.'</span><span class="sxs-lookup"><span data-stu-id="e0b9b-160">Note that we use '1.'</span></span> <span data-ttu-id="e0b9b-161">per tutte le voci.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-161">for all entries.</span></span> <span data-ttu-id="e0b9b-162">Ciò semplifica l'esame delle differenze in occasione di aggiornamenti successivi, quando vengono aggiunti nuovi passaggi o vengono rimossi passaggi esistenti.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="e0b9b-163">Tables</span><span class="sxs-lookup"><span data-stu-id="e0b9b-163">Tables</span></span>

<span data-ttu-id="e0b9b-164">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="e0b9b-165">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="e0b9b-166">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="e0b9b-167">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="e0b9b-168">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="e0b9b-169">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-169">will be rendered as:</span></span>

| <span data-ttu-id="e0b9b-170">Fun</span><span class="sxs-lookup"><span data-stu-id="e0b9b-170">Fun</span></span>                  | <span data-ttu-id="e0b9b-171">With</span><span class="sxs-lookup"><span data-stu-id="e0b9b-171">With</span></span>                 | <span data-ttu-id="e0b9b-172">Tables</span><span class="sxs-lookup"><span data-stu-id="e0b9b-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="e0b9b-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="e0b9b-173">left-aligned column</span></span>  | <span data-ttu-id="e0b9b-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="e0b9b-174">right-aligned column</span></span> | <span data-ttu-id="e0b9b-175">centered column</span><span class="sxs-lookup"><span data-stu-id="e0b9b-175">centered column</span></span> |
| <span data-ttu-id="e0b9b-176">$100</span><span class="sxs-lookup"><span data-stu-id="e0b9b-176">$100</span></span>                 | <span data-ttu-id="e0b9b-177">$100</span><span class="sxs-lookup"><span data-stu-id="e0b9b-177">$100</span></span>                 | <span data-ttu-id="e0b9b-178">$100</span><span class="sxs-lookup"><span data-stu-id="e0b9b-178">$100</span></span>            |
| <span data-ttu-id="e0b9b-179">$10</span><span class="sxs-lookup"><span data-stu-id="e0b9b-179">$10</span></span>                  | <span data-ttu-id="e0b9b-180">$10</span><span class="sxs-lookup"><span data-stu-id="e0b9b-180">$10</span></span>                  | <span data-ttu-id="e0b9b-181">$10</span><span class="sxs-lookup"><span data-stu-id="e0b9b-181">$10</span></span>             |
| <span data-ttu-id="e0b9b-182">$1</span><span class="sxs-lookup"><span data-stu-id="e0b9b-182">$1</span></span>                   | <span data-ttu-id="e0b9b-183">$1</span><span class="sxs-lookup"><span data-stu-id="e0b9b-183">$1</span></span>                   | <span data-ttu-id="e0b9b-184">$1</span><span class="sxs-lookup"><span data-stu-id="e0b9b-184">$1</span></span>              |

<span data-ttu-id="e0b9b-185">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="e0b9b-186">La [funzionalità per il ritorno a capo nelle tabelle](#table-wrapping) di Markdig, utile per la formattazione di tabelle estese.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="e0b9b-187">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="e0b9b-188">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="e0b9b-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="e0b9b-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="e0b9b-191">[Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="e0b9b-192">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="e0b9b-192">Links</span></span>

<span data-ttu-id="e0b9b-193">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="e0b9b-194">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-194">For more information on linking, see:</span></span>

- <span data-ttu-id="e0b9b-195">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="e0b9b-196">La pagina [Collegamenti](how-to-write-links.md) in questa guida per dettagli sulla sintassi aggiuntiva per i collegamenti disponibile con Markdig.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="e0b9b-197">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="e0b9b-197">Code snippets</span></span>

<span data-ttu-id="e0b9b-198">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="e0b9b-199">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-199">For details, see:</span></span>

- <span data-ttu-id="e0b9b-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="e0b9b-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="e0b9b-202">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="e0b9b-203">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="e0b9b-204">L'alias dopo i tre apici inversi iniziali '\`' definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="e0b9b-205">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="e0b9b-206">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="e0b9b-207">Nome</span><span class="sxs-lookup"><span data-stu-id="e0b9b-207">Name</span></span>|<span data-ttu-id="e0b9b-208">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="e0b9b-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="e0b9b-209">Console .NET</span><span class="sxs-lookup"><span data-stu-id="e0b9b-209">.NET Console</span></span>|<span data-ttu-id="e0b9b-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="e0b9b-210">dotnetcli</span></span>|
|<span data-ttu-id="e0b9b-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-211">ASP.NET (C#)</span></span>|<span data-ttu-id="e0b9b-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="e0b9b-212">aspx-csharp</span></span>|
|<span data-ttu-id="e0b9b-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-213">ASP.NET (VB)</span></span>|<span data-ttu-id="e0b9b-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="e0b9b-214">aspx-vb</span></span>|
|<span data-ttu-id="e0b9b-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="e0b9b-215">AzCopy</span></span>|<span data-ttu-id="e0b9b-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="e0b9b-216">azcopy</span></span>|
|<span data-ttu-id="e0b9b-217">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="e0b9b-217">Azure CLI</span></span>|<span data-ttu-id="e0b9b-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="e0b9b-218">azurecli</span></span>|
|<span data-ttu-id="e0b9b-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0b9b-219">Azure PowerShell</span></span>|<span data-ttu-id="e0b9b-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="e0b9b-220">azurepowershell</span></span>|
|<span data-ttu-id="e0b9b-221">C++</span><span class="sxs-lookup"><span data-stu-id="e0b9b-221">C++</span></span>|<span data-ttu-id="e0b9b-222">cpp</span><span class="sxs-lookup"><span data-stu-id="e0b9b-222">cpp</span></span>|
|<span data-ttu-id="e0b9b-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="e0b9b-223">C++/CX</span></span>|<span data-ttu-id="e0b9b-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="e0b9b-224">cppcx</span></span>|
|<span data-ttu-id="e0b9b-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="e0b9b-225">C++/WinRT</span></span>|<span data-ttu-id="e0b9b-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="e0b9b-226">cppwinrt</span></span>|
|<span data-ttu-id="e0b9b-227">C#</span><span class="sxs-lookup"><span data-stu-id="e0b9b-227">C#</span></span>|<span data-ttu-id="e0b9b-228">csharp</span><span class="sxs-lookup"><span data-stu-id="e0b9b-228">csharp</span></span>|
|<span data-ttu-id="e0b9b-229">C# nel browser</span><span class="sxs-lookup"><span data-stu-id="e0b9b-229">C# in browser</span></span>|<span data-ttu-id="e0b9b-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="e0b9b-230">csharp-interactive</span></span>|
|<span data-ttu-id="e0b9b-231">Console</span><span class="sxs-lookup"><span data-stu-id="e0b9b-231">Console</span></span>|<span data-ttu-id="e0b9b-232">console</span><span class="sxs-lookup"><span data-stu-id="e0b9b-232">console</span></span>|
|<span data-ttu-id="e0b9b-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="e0b9b-233">CSHTML</span></span>|<span data-ttu-id="e0b9b-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="e0b9b-234">cshtml</span></span>|
|<span data-ttu-id="e0b9b-235">DAX</span><span class="sxs-lookup"><span data-stu-id="e0b9b-235">DAX</span></span>|<span data-ttu-id="e0b9b-236">dax</span><span class="sxs-lookup"><span data-stu-id="e0b9b-236">dax</span></span>|
|<span data-ttu-id="e0b9b-237">F#</span><span class="sxs-lookup"><span data-stu-id="e0b9b-237">F#</span></span>|<span data-ttu-id="e0b9b-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="e0b9b-238">fsharp</span></span>|
|<span data-ttu-id="e0b9b-239">Go</span><span class="sxs-lookup"><span data-stu-id="e0b9b-239">Go</span></span>|<span data-ttu-id="e0b9b-240">go</span><span class="sxs-lookup"><span data-stu-id="e0b9b-240">go</span></span>|
|<span data-ttu-id="e0b9b-241">HTML</span><span class="sxs-lookup"><span data-stu-id="e0b9b-241">HTML</span></span>|<span data-ttu-id="e0b9b-242">html</span><span class="sxs-lookup"><span data-stu-id="e0b9b-242">html</span></span>|
|<span data-ttu-id="e0b9b-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="e0b9b-243">HTTP</span></span>|<span data-ttu-id="e0b9b-244">http</span><span class="sxs-lookup"><span data-stu-id="e0b9b-244">http</span></span>|
|<span data-ttu-id="e0b9b-245">Java</span><span class="sxs-lookup"><span data-stu-id="e0b9b-245">Java</span></span>|<span data-ttu-id="e0b9b-246">java</span><span class="sxs-lookup"><span data-stu-id="e0b9b-246">java</span></span>|
|<span data-ttu-id="e0b9b-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0b9b-247">JavaScript</span></span>|<span data-ttu-id="e0b9b-248">javascript</span><span class="sxs-lookup"><span data-stu-id="e0b9b-248">javascript</span></span>|
|<span data-ttu-id="e0b9b-249">JSON</span><span class="sxs-lookup"><span data-stu-id="e0b9b-249">JSON</span></span>|<span data-ttu-id="e0b9b-250">json</span><span class="sxs-lookup"><span data-stu-id="e0b9b-250">json</span></span>|
|<span data-ttu-id="e0b9b-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="e0b9b-251">Markdown</span></span>|<span data-ttu-id="e0b9b-252">md</span><span class="sxs-lookup"><span data-stu-id="e0b9b-252">md</span></span>|
|<span data-ttu-id="e0b9b-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="e0b9b-253">NodeJS</span></span>|<span data-ttu-id="e0b9b-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="e0b9b-254">nodejs</span></span>|
|<span data-ttu-id="e0b9b-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="e0b9b-255">Objective-C</span></span>|<span data-ttu-id="e0b9b-256">objc</span><span class="sxs-lookup"><span data-stu-id="e0b9b-256">objc</span></span>|
|<span data-ttu-id="e0b9b-257">OData</span><span class="sxs-lookup"><span data-stu-id="e0b9b-257">OData</span></span>|<span data-ttu-id="e0b9b-258">odata</span><span class="sxs-lookup"><span data-stu-id="e0b9b-258">odata</span></span>|
|<span data-ttu-id="e0b9b-259">PHP</span><span class="sxs-lookup"><span data-stu-id="e0b9b-259">PHP</span></span>|<span data-ttu-id="e0b9b-260">php</span><span class="sxs-lookup"><span data-stu-id="e0b9b-260">php</span></span>|
|<span data-ttu-id="e0b9b-261">Formula PowerApps</span><span class="sxs-lookup"><span data-stu-id="e0b9b-261">Power Apps Formula</span></span>|<span data-ttu-id="e0b9b-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="e0b9b-262">powerappsfl</span></span>|
|<span data-ttu-id="e0b9b-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0b9b-263">PowerShell</span></span>|<span data-ttu-id="e0b9b-264">powershell</span><span class="sxs-lookup"><span data-stu-id="e0b9b-264">powershell</span></span>|
|<span data-ttu-id="e0b9b-265">Python</span><span class="sxs-lookup"><span data-stu-id="e0b9b-265">Python</span></span>|<span data-ttu-id="e0b9b-266">python</span><span class="sxs-lookup"><span data-stu-id="e0b9b-266">python</span></span>|
|<span data-ttu-id="e0b9b-267">Q#</span><span class="sxs-lookup"><span data-stu-id="e0b9b-267">Q#</span></span>|<span data-ttu-id="e0b9b-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="e0b9b-268">qsharp</span></span>|
|<span data-ttu-id="e0b9b-269">R</span><span class="sxs-lookup"><span data-stu-id="e0b9b-269">R</span></span>|<span data-ttu-id="e0b9b-270">r</span><span class="sxs-lookup"><span data-stu-id="e0b9b-270">r</span></span>|
|<span data-ttu-id="e0b9b-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="e0b9b-271">Ruby</span></span>|<span data-ttu-id="e0b9b-272">ruby</span><span class="sxs-lookup"><span data-stu-id="e0b9b-272">ruby</span></span>|
|<span data-ttu-id="e0b9b-273">SQL</span><span class="sxs-lookup"><span data-stu-id="e0b9b-273">SQL</span></span>|<span data-ttu-id="e0b9b-274">sql</span><span class="sxs-lookup"><span data-stu-id="e0b9b-274">sql</span></span>|
|<span data-ttu-id="e0b9b-275">Swift</span><span class="sxs-lookup"><span data-stu-id="e0b9b-275">Swift</span></span>|<span data-ttu-id="e0b9b-276">swift</span><span class="sxs-lookup"><span data-stu-id="e0b9b-276">swift</span></span>|
|<span data-ttu-id="e0b9b-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="e0b9b-277">TypeScript</span></span>|<span data-ttu-id="e0b9b-278">typescript</span><span class="sxs-lookup"><span data-stu-id="e0b9b-278">typescript</span></span>|
|<span data-ttu-id="e0b9b-279">VB</span><span class="sxs-lookup"><span data-stu-id="e0b9b-279">VB</span></span>|<span data-ttu-id="e0b9b-280">vb</span><span class="sxs-lookup"><span data-stu-id="e0b9b-280">vb</span></span>|
|<span data-ttu-id="e0b9b-281">Interfaccia della riga di comando di VSTS</span><span class="sxs-lookup"><span data-stu-id="e0b9b-281">VSTS CLI</span></span>|<span data-ttu-id="e0b9b-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="e0b9b-282">vstscli</span></span>|
|<span data-ttu-id="e0b9b-283">XAML</span><span class="sxs-lookup"><span data-stu-id="e0b9b-283">XAML</span></span>|<span data-ttu-id="e0b9b-284">xaml</span><span class="sxs-lookup"><span data-stu-id="e0b9b-284">xaml</span></span>|
|<span data-ttu-id="e0b9b-285">XML</span><span class="sxs-lookup"><span data-stu-id="e0b9b-285">XML</span></span>|<span data-ttu-id="e0b9b-286">xml</span><span class="sxs-lookup"><span data-stu-id="e0b9b-286">xml</span></span>|

<span data-ttu-id="e0b9b-287">Il nome `csharp-interactive` specifica il linguaggio C# e la capacità di eseguire gli esempi dal browser.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="e0b9b-288">Questi frammenti di codice vengono compilati ed eseguiti in un contenitore Docker e i risultati dell'esecuzione del programma vengono visualizzati nella finestra del browser dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="e0b9b-289">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="e0b9b-289">Example: C\#</span></span>

<span data-ttu-id="e0b9b-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="e0b9b-290">__Markdown__</span></span>

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

<span data-ttu-id="e0b9b-291">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="e0b9b-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="e0b9b-292">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="e0b9b-292">Example: SQL</span></span>

<span data-ttu-id="e0b9b-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="e0b9b-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="e0b9b-294">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="e0b9b-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="e0b9b-295">Estensioni Markdown personalizzate di OPS</span><span class="sxs-lookup"><span data-stu-id="e0b9b-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="e0b9b-296">OPS (Open Publishing Services) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="e0b9b-297">Markdig aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="e0b9b-298">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="e0b9b-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="e0b9b-299">(vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="e0b9b-300">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="e0b9b-301">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="e0b9b-302">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="e0b9b-302">Note blocks</span></span>
- <span data-ttu-id="e0b9b-303">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="e0b9b-303">Include files</span></span>
- <span data-ttu-id="e0b9b-304">Selettori</span><span class="sxs-lookup"><span data-stu-id="e0b9b-304">Selectors</span></span>
- <span data-ttu-id="e0b9b-305">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="e0b9b-305">Embedded videos</span></span>
- <span data-ttu-id="e0b9b-306">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="e0b9b-306">Code snippets/samples</span></span>

<span data-ttu-id="e0b9b-307">Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="e0b9b-308">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="e0b9b-308">Note blocks</span></span>

<span data-ttu-id="e0b9b-309">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="e0b9b-310">NOTA</span><span class="sxs-lookup"><span data-stu-id="e0b9b-310">NOTE</span></span>
- <span data-ttu-id="e0b9b-311">AVVISO</span><span class="sxs-lookup"><span data-stu-id="e0b9b-311">WARNING</span></span>
- <span data-ttu-id="e0b9b-312">SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="e0b9b-312">TIP</span></span>
- <span data-ttu-id="e0b9b-313">IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="e0b9b-313">IMPORTANT</span></span>

<span data-ttu-id="e0b9b-314">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="e0b9b-315">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="e0b9b-316">Esempi:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-316">Examples:</span></span>

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

<span data-ttu-id="e0b9b-317">Il rendering è il seguente:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="e0b9b-318">Questa è una NOTA</span><span class="sxs-lookup"><span data-stu-id="e0b9b-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="e0b9b-319">Questo è un AVVISO</span><span class="sxs-lookup"><span data-stu-id="e0b9b-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="e0b9b-320">Questo è un SUGGERIMENTO</span><span class="sxs-lookup"><span data-stu-id="e0b9b-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0b9b-321">Questo testo è IMPORTANTE</span><span class="sxs-lookup"><span data-stu-id="e0b9b-321">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="e0b9b-322">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="e0b9b-322">Include files</span></span>

<span data-ttu-id="e0b9b-323">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="e0b9b-324">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="e0b9b-325">Sono disponibili tre tipi di riferimenti di inclusione per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-325">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="e0b9b-326">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="e0b9b-327">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="e0b9b-328">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="e0b9b-329">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (MD),</span><span class="sxs-lookup"><span data-stu-id="e0b9b-329">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="e0b9b-330">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="e0b9b-331">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="e0b9b-332">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="e0b9b-333">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-333">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="e0b9b-334">Usare un file di inclusione ogni volta che è necessario visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-334">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="e0b9b-335">Usare un riferimento di inclusione di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-335">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="e0b9b-336">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="e0b9b-337">I riferimenti di inclusione non vengono visualizzati nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-337">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="e0b9b-338">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="e0b9b-339">Verificare che tutto il testo in un file di inclusione sia scritto con frasi complete o che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-339">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="e0b9b-340">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="e0b9b-341">Non incorporare riferimenti di inclusione in altri file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-341">Don't embed include references within other include files.</span></span> <span data-ttu-id="e0b9b-342">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-342">They are not supported.</span></span>
- <span data-ttu-id="e0b9b-343">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="e0b9b-344">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="e0b9b-345">Se il file di inclusione non contiene immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-345">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="e0b9b-346">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="e0b9b-347">Usare un file separato con un nome univoco per ogni file di inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-347">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="e0b9b-348">Archiviare il file multimediale nella cartella dei file multimediali associata al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-348">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="e0b9b-349">Non usare un file di inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-349">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="e0b9b-350">I file di inclusione sono pensati come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-350">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="e0b9b-351">Esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="e0b9b-352">Selettori</span><span class="sxs-lookup"><span data-stu-id="e0b9b-352">Selectors</span></span>

<span data-ttu-id="e0b9b-353">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="e0b9b-354">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="e0b9b-355">In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="e0b9b-356">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="e0b9b-357">A questo punto è possibile fare riferimento a quel file di inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-357">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="e0b9b-358">Di seguito viene illustrato un esempio di selettore:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="e0b9b-359">Per un esempio di selettori attivi, vedere la [documentazione di Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="e0b9b-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="e0b9b-360">Riferimenti di inclusione di codice</span><span class="sxs-lookup"><span data-stu-id="e0b9b-360">Code include references</span></span>

<span data-ttu-id="e0b9b-361">Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="e0b9b-362">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="e0b9b-363">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="e0b9b-364">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="e0b9b-365">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="e0b9b-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="e0b9b-366">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="e0b9b-366">Alt text</span></span>

<span data-ttu-id="e0b9b-367">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="e0b9b-368">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="e0b9b-369">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="e0b9b-370">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="e0b9b-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="e0b9b-371">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="e0b9b-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="e0b9b-372">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="e0b9b-373">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="e0b9b-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="e0b9b-374">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="e0b9b-375">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="e0b9b-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="e0b9b-376">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="e0b9b-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="e0b9b-377">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="e0b9b-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="e0b9b-378">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="e0b9b-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="e0b9b-379">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="e0b9b-379">Angle brackets</span></span>

<span data-ttu-id="e0b9b-380">Le parentesi acute vengono comunemente usate per indicare un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="e0b9b-381">Se usate nel testo e non nel codice, le parentesi acute devono essere codificate.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="e0b9b-382">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="e0b9b-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="e0b9b-383">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="e0b9b-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="e0b9b-384">Vedere anche:</span><span class="sxs-lookup"><span data-stu-id="e0b9b-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="e0b9b-385">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="e0b9b-385">Markdown resources</span></span>

- <span data-ttu-id="e0b9b-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="e0b9b-387">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="e0b9b-387">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="e0b9b-388">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="e0b9b-388">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="e0b9b-389">Guida Markdown</span><span class="sxs-lookup"><span data-stu-id="e0b9b-389">The Markdown Guide</span></span>](https://www.markdownguide.org/)
