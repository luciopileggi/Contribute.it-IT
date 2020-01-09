---
title: Come usare Markdown per scrivere articoli di Docs
description: Questo articolo offre informazioni di base e di riferimento sul linguaggio Markdown usato per la stesura di articoli per il sito docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 1f43cecb450c988e4f546aa5ecc5907061521f34
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188296"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="dee87-103">Come usare Markdown per scrivere articoli di Docs</span><span class="sxs-lookup"><span data-stu-id="dee87-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="dee87-104">Gli articoli di [docs.microsoft.com](https://docs.microsoft.com) sono scritti in un semplice linguaggio di markup denominato [Markdown](https://daringfireball.net/projects/markdown/), facile sia da leggere che da apprendere.</span><span class="sxs-lookup"><span data-stu-id="dee87-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="dee87-105">Per questo motivo si sta imponendo rapidamente come standard del settore.</span><span class="sxs-lookup"><span data-stu-id="dee87-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="dee87-106">Il sito docs usa la [versione Markdig](#markdown-flavor) di Markdown.</span><span class="sxs-lookup"><span data-stu-id="dee87-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="dee87-107">Nozioni di base su Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="dee87-108">Titoli</span><span class="sxs-lookup"><span data-stu-id="dee87-108">Headings</span></span>

<span data-ttu-id="dee87-109">Per creare un titolo, usare il segno di cancelletto (#), come segue:</span><span class="sxs-lookup"><span data-stu-id="dee87-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="dee87-110">Le intestazioni devono essere in stile atx. Devono quindi iniziare con un numero di caratteri cancelletto (#) compreso tra 1 e 6, corrispondente in HTML ai livelli di intestazione da H1 a H6.</span><span class="sxs-lookup"><span data-stu-id="dee87-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="dee87-111">Quelli riportati qui sopra sono esempi di intestazioni di livello da 1 a 4.</span><span class="sxs-lookup"><span data-stu-id="dee87-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="dee87-112">Nell'argomento **deve** essere presente una sola intestazione di primo livello (H1), che verrà visualizzata come titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="dee87-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="dee87-113">Se l'intestazione termina con un carattere `#`, perché il rendering sia corretto è necessario aggiungere un altro carattere `#` alla fine,</span><span class="sxs-lookup"><span data-stu-id="dee87-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="dee87-114">come ad esempio in `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="dee87-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="dee87-115">Le intestazioni di secondo livello generano il sommario della sezione "In questo articolo", immediatamente dopo il titolo sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="dee87-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="dee87-116">Testo in grassetto e corsivo</span><span class="sxs-lookup"><span data-stu-id="dee87-116">Bold and italic text</span></span>

<span data-ttu-id="dee87-117">Per applicare il formato **grassetto** al testo, racchiuderlo tra due coppie asterischi:</span><span class="sxs-lookup"><span data-stu-id="dee87-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="dee87-118">Per applicare il formato *corsivo* al testo, racchiuderlo tra due asterischi:</span><span class="sxs-lookup"><span data-stu-id="dee87-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="dee87-119">Per applicare il formato ***grassetto e corsivo*** al testo, racchiuderlo tra due coppie di tre asterischi:</span><span class="sxs-lookup"><span data-stu-id="dee87-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="dee87-120">Citazioni</span><span class="sxs-lookup"><span data-stu-id="dee87-120">Blockquotes</span></span>

<span data-ttu-id="dee87-121">Per creare citazioni, si usa il carattere `>`:</span><span class="sxs-lookup"><span data-stu-id="dee87-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="dee87-122">Ecco il rendering dell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="dee87-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="dee87-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="dee87-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="dee87-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="dee87-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="dee87-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="dee87-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="dee87-126">Elenchi</span><span class="sxs-lookup"><span data-stu-id="dee87-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="dee87-127">Elenco non ordinato</span><span class="sxs-lookup"><span data-stu-id="dee87-127">Unordered list</span></span>

<span data-ttu-id="dee87-128">Per formattare un elenco puntato non ordinato, si possono usare asterischi o trattini.</span><span class="sxs-lookup"><span data-stu-id="dee87-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="dee87-129">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="dee87-130">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-130">will be rendered as:</span></span>

- <span data-ttu-id="dee87-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="dee87-131">List item 1</span></span>
- <span data-ttu-id="dee87-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="dee87-132">List item 2</span></span>
- <span data-ttu-id="dee87-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="dee87-133">List item 3</span></span>

<span data-ttu-id="dee87-134">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="dee87-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="dee87-135">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="dee87-136">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-136">will be rendered as:</span></span>

- <span data-ttu-id="dee87-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="dee87-137">List item 1</span></span>
  - <span data-ttu-id="dee87-138">List item A</span><span class="sxs-lookup"><span data-stu-id="dee87-138">List item A</span></span>
  - <span data-ttu-id="dee87-139">List item B</span><span class="sxs-lookup"><span data-stu-id="dee87-139">List item B</span></span>
- <span data-ttu-id="dee87-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="dee87-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="dee87-141">Elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="dee87-141">Ordered list</span></span>

<span data-ttu-id="dee87-142">Per formattare un elenco ordinato in più passaggi, usare i numeri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="dee87-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="dee87-143">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="dee87-144">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-144">will be rendered as:</span></span>

1. <span data-ttu-id="dee87-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-145">First instruction</span></span>
2. <span data-ttu-id="dee87-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-146">Second instruction</span></span>
3. <span data-ttu-id="dee87-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-147">Third instruction</span></span>

<span data-ttu-id="dee87-148">Per annidare un elenco all'interno di un altro elenco, far rientrare gli elementi dell'elenco figlio.</span><span class="sxs-lookup"><span data-stu-id="dee87-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="dee87-149">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="dee87-150">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-150">will be rendered as:</span></span>

1. <span data-ttu-id="dee87-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-151">First instruction</span></span>
   1. <span data-ttu-id="dee87-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-152">Sub-instruction</span></span>
   2. <span data-ttu-id="dee87-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-153">Sub-instruction</span></span>
2. <span data-ttu-id="dee87-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="dee87-154">Second instruction</span></span>

<span data-ttu-id="dee87-155">Si noti che si usa '1.'</span><span class="sxs-lookup"><span data-stu-id="dee87-155">Note that we use '1.'</span></span> <span data-ttu-id="dee87-156">per tutte le voci.</span><span class="sxs-lookup"><span data-stu-id="dee87-156">for all entries.</span></span> <span data-ttu-id="dee87-157">Ciò semplifica l'esame delle differenze in occasione di aggiornamenti successivi, quando vengono aggiunti nuovi passaggi o vengono rimossi passaggi esistenti.</span><span class="sxs-lookup"><span data-stu-id="dee87-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="dee87-158">Tabelle</span><span class="sxs-lookup"><span data-stu-id="dee87-158">Tables</span></span>

<span data-ttu-id="dee87-159">Le tabelle non fanno parte della specifica Markdown principale, ma sono supportate da GFM.</span><span class="sxs-lookup"><span data-stu-id="dee87-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="dee87-160">È possibile creare tabelle usando i caratteri barra verticale (|) e segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="dee87-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="dee87-161">I segni meno sono usati per creare l'intestazione delle colonne e le barre verticali per separare ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="dee87-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="dee87-162">Includere una riga vuota prima della tabella per assicurarne il rendering corretto.</span><span class="sxs-lookup"><span data-stu-id="dee87-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="dee87-163">Il testo Markdown seguente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="dee87-164">verrà rappresentato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-164">Will be rendered as:</span></span>

| <span data-ttu-id="dee87-165">Fun</span><span class="sxs-lookup"><span data-stu-id="dee87-165">Fun</span></span>                  | <span data-ttu-id="dee87-166">With</span><span class="sxs-lookup"><span data-stu-id="dee87-166">With</span></span>                 | <span data-ttu-id="dee87-167">Tabelle</span><span class="sxs-lookup"><span data-stu-id="dee87-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="dee87-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="dee87-168">left-aligned column</span></span>  | <span data-ttu-id="dee87-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="dee87-169">right-aligned column</span></span> | <span data-ttu-id="dee87-170">centered column</span><span class="sxs-lookup"><span data-stu-id="dee87-170">centered column</span></span> |
| <span data-ttu-id="dee87-171">$100</span><span class="sxs-lookup"><span data-stu-id="dee87-171">$100</span></span>                 | <span data-ttu-id="dee87-172">$100</span><span class="sxs-lookup"><span data-stu-id="dee87-172">$100</span></span>                 | <span data-ttu-id="dee87-173">$100</span><span class="sxs-lookup"><span data-stu-id="dee87-173">$100</span></span>            |
| <span data-ttu-id="dee87-174">$10</span><span class="sxs-lookup"><span data-stu-id="dee87-174">$10</span></span>                  | <span data-ttu-id="dee87-175">$10</span><span class="sxs-lookup"><span data-stu-id="dee87-175">$10</span></span>                  | <span data-ttu-id="dee87-176">$10</span><span class="sxs-lookup"><span data-stu-id="dee87-176">$10</span></span>             |
| <span data-ttu-id="dee87-177">$1</span><span class="sxs-lookup"><span data-stu-id="dee87-177">$1</span></span>                   | <span data-ttu-id="dee87-178">$1</span><span class="sxs-lookup"><span data-stu-id="dee87-178">$1</span></span>                   | <span data-ttu-id="dee87-179">$1</span><span class="sxs-lookup"><span data-stu-id="dee87-179">$1</span></span>              |

<span data-ttu-id="dee87-180">Per altre informazioni sulla creazione di tabelle, vedere:</span><span class="sxs-lookup"><span data-stu-id="dee87-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="dee87-181">[Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Organizzazione delle informazioni con le tabelle) di GitHub.</span><span class="sxs-lookup"><span data-stu-id="dee87-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="dee87-182">L'app Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="dee87-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="dee87-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Informazioni di riferimento rapide su Markdown di Adam Pritchard).</span><span class="sxs-lookup"><span data-stu-id="dee87-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="dee87-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Markdown Extra di Michel Fortin).</span><span class="sxs-lookup"><span data-stu-id="dee87-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="dee87-185">[Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="dee87-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="dee87-186">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="dee87-186">Links</span></span>

<span data-ttu-id="dee87-187">La sintassi di Markdown per un collegamento inline è costituita dalla parte `[link text]`, ovvero il testo che verrà impostato come collegamento ipertestuale, seguita dalla parte `(file-name.md)`, ovvero l'URL o il nome di file di destinazione del collegamento:</span><span class="sxs-lookup"><span data-stu-id="dee87-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="dee87-188">Per altre informazioni sui collegamenti, vedere:</span><span class="sxs-lookup"><span data-stu-id="dee87-188">For more information on linking, see:</span></span>

- <span data-ttu-id="dee87-189">La [guida alla sintassi di Markdown](https://daringfireball.net/projects/markdown/syntax#link) per informazioni dettagliate sul supporto dei collegamenti di base di Markdown.</span><span class="sxs-lookup"><span data-stu-id="dee87-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="dee87-190">La pagina [Collegamenti](how-to-write-links.md) in questa guida per dettagli sulla sintassi aggiuntiva per i collegamenti disponibile con Markdig.</span><span class="sxs-lookup"><span data-stu-id="dee87-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="dee87-191">Frammenti di codice</span><span class="sxs-lookup"><span data-stu-id="dee87-191">Code snippets</span></span>

<span data-ttu-id="dee87-192">Markdown supporta il posizionamento di frammenti di codice sia inline in una frase che come blocco separato "delimitato" tra due frasi.</span><span class="sxs-lookup"><span data-stu-id="dee87-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="dee87-193">Per informazioni dettagliate, vedere:</span><span class="sxs-lookup"><span data-stu-id="dee87-193">For details, see:</span></span>

- <span data-ttu-id="dee87-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode) (Supporto nativo dei blocchi di codice di Markdown)</span><span class="sxs-lookup"><span data-stu-id="dee87-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="dee87-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/) (Supporto di GFM per la delimitazione del codice e l'evidenziazione della sintassi)</span><span class="sxs-lookup"><span data-stu-id="dee87-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="dee87-196">I blocchi di codice delimitati sono un modo semplice per abilitare l'evidenziazione della sintassi per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="dee87-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="dee87-197">Il formato generare per i blocchi di codice delimitati è:</span><span class="sxs-lookup"><span data-stu-id="dee87-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="dee87-198">L'alias dopo i tre apici inversi iniziali (\`) definisce l'evidenziazione della sintassi da usare.</span><span class="sxs-lookup"><span data-stu-id="dee87-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="dee87-199">L'elenco seguente include i linguaggi di programmazione di uso comune nel contenuto Docs e l'etichetta corrispondente:</span><span class="sxs-lookup"><span data-stu-id="dee87-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="dee87-200">Questi linguaggi supportano nomi descrittivi e la maggior parte ha la funzione di evidenziazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="dee87-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="dee87-201">Nome</span><span class="sxs-lookup"><span data-stu-id="dee87-201">Name</span></span>|<span data-ttu-id="dee87-202">Etichetta Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="dee87-203">Console .NET</span><span class="sxs-lookup"><span data-stu-id="dee87-203">.NET Console</span></span>|<span data-ttu-id="dee87-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="dee87-204">dotnetcli</span></span>|
|<span data-ttu-id="dee87-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="dee87-205">ASP.NET (C#)</span></span>|<span data-ttu-id="dee87-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="dee87-206">aspx-csharp</span></span>|
|<span data-ttu-id="dee87-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="dee87-207">ASP.NET (VB)</span></span>|<span data-ttu-id="dee87-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="dee87-208">aspx-vb</span></span>|
|<span data-ttu-id="dee87-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="dee87-209">AzCopy</span></span>|<span data-ttu-id="dee87-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="dee87-210">azcopy</span></span>|
|<span data-ttu-id="dee87-211">Interfaccia della riga di comando di Azure</span><span class="sxs-lookup"><span data-stu-id="dee87-211">Azure CLI</span></span>|<span data-ttu-id="dee87-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="dee87-212">azurecli</span></span>|
|<span data-ttu-id="dee87-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dee87-213">Azure PowerShell</span></span>|<span data-ttu-id="dee87-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="dee87-214">azurepowershell</span></span>|
|<span data-ttu-id="dee87-215">Bash</span><span class="sxs-lookup"><span data-stu-id="dee87-215">Bash</span></span>|<span data-ttu-id="dee87-216">bash</span><span class="sxs-lookup"><span data-stu-id="dee87-216">bash</span></span>|
|<span data-ttu-id="dee87-217">C++</span><span class="sxs-lookup"><span data-stu-id="dee87-217">C++</span></span>|<span data-ttu-id="dee87-218">cpp</span><span class="sxs-lookup"><span data-stu-id="dee87-218">cpp</span></span>|
|<span data-ttu-id="dee87-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="dee87-219">C++/CX</span></span>|<span data-ttu-id="dee87-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="dee87-220">cppcx</span></span>|
|<span data-ttu-id="dee87-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="dee87-221">C++/WinRT</span></span>|<span data-ttu-id="dee87-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="dee87-222">cppwinrt</span></span>|
|<span data-ttu-id="dee87-223">C#</span><span class="sxs-lookup"><span data-stu-id="dee87-223">C#</span></span>|<span data-ttu-id="dee87-224">csharp</span><span class="sxs-lookup"><span data-stu-id="dee87-224">csharp</span></span>|
|<span data-ttu-id="dee87-225">C# nel browser</span><span class="sxs-lookup"><span data-stu-id="dee87-225">C# in browser</span></span>|<span data-ttu-id="dee87-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="dee87-226">csharp-interactive</span></span>|
|<span data-ttu-id="dee87-227">Console</span><span class="sxs-lookup"><span data-stu-id="dee87-227">Console</span></span>|<span data-ttu-id="dee87-228">console</span><span class="sxs-lookup"><span data-stu-id="dee87-228">console</span></span>|
|<span data-ttu-id="dee87-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="dee87-229">CSHTML</span></span>|<span data-ttu-id="dee87-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="dee87-230">cshtml</span></span>|
|<span data-ttu-id="dee87-231">DAX</span><span class="sxs-lookup"><span data-stu-id="dee87-231">DAX</span></span>|<span data-ttu-id="dee87-232">dax</span><span class="sxs-lookup"><span data-stu-id="dee87-232">dax</span></span>|
|<span data-ttu-id="dee87-233">Docker</span><span class="sxs-lookup"><span data-stu-id="dee87-233">Docker</span></span>|<span data-ttu-id="dee87-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="dee87-234">dockerfile</span></span>|
|<span data-ttu-id="dee87-235">F#</span><span class="sxs-lookup"><span data-stu-id="dee87-235">F#</span></span>|<span data-ttu-id="dee87-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="dee87-236">fsharp</span></span>|
|<span data-ttu-id="dee87-237">Go</span><span class="sxs-lookup"><span data-stu-id="dee87-237">Go</span></span>|<span data-ttu-id="dee87-238">go</span><span class="sxs-lookup"><span data-stu-id="dee87-238">go</span></span>|
|<span data-ttu-id="dee87-239">HTML</span><span class="sxs-lookup"><span data-stu-id="dee87-239">HTML</span></span>|<span data-ttu-id="dee87-240">html</span><span class="sxs-lookup"><span data-stu-id="dee87-240">html</span></span>|
|<span data-ttu-id="dee87-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="dee87-241">HTTP</span></span>|<span data-ttu-id="dee87-242">http</span><span class="sxs-lookup"><span data-stu-id="dee87-242">http</span></span>|
|<span data-ttu-id="dee87-243">Java</span><span class="sxs-lookup"><span data-stu-id="dee87-243">Java</span></span>|<span data-ttu-id="dee87-244">java</span><span class="sxs-lookup"><span data-stu-id="dee87-244">java</span></span>|
|<span data-ttu-id="dee87-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="dee87-245">JavaScript</span></span>|<span data-ttu-id="dee87-246">javascript</span><span class="sxs-lookup"><span data-stu-id="dee87-246">javascript</span></span>|
|<span data-ttu-id="dee87-247">JSON</span><span class="sxs-lookup"><span data-stu-id="dee87-247">JSON</span></span>|<span data-ttu-id="dee87-248">json</span><span class="sxs-lookup"><span data-stu-id="dee87-248">json</span></span>|
|<span data-ttu-id="dee87-249">Linguaggio di query Kusto</span><span class="sxs-lookup"><span data-stu-id="dee87-249">Kusto Query Language</span></span>|<span data-ttu-id="dee87-250">kusto</span><span class="sxs-lookup"><span data-stu-id="dee87-250">kusto</span></span>|
|<span data-ttu-id="dee87-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-251">Markdown</span></span>|<span data-ttu-id="dee87-252">md</span><span class="sxs-lookup"><span data-stu-id="dee87-252">md</span></span>|
|<span data-ttu-id="dee87-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="dee87-253">Objective-C</span></span>|<span data-ttu-id="dee87-254">objc</span><span class="sxs-lookup"><span data-stu-id="dee87-254">objc</span></span>|
|<span data-ttu-id="dee87-255">OData</span><span class="sxs-lookup"><span data-stu-id="dee87-255">OData</span></span>|<span data-ttu-id="dee87-256">odata</span><span class="sxs-lookup"><span data-stu-id="dee87-256">odata</span></span>|
|<span data-ttu-id="dee87-257">PHP</span><span class="sxs-lookup"><span data-stu-id="dee87-257">PHP</span></span>|<span data-ttu-id="dee87-258">php</span><span class="sxs-lookup"><span data-stu-id="dee87-258">php</span></span>|
|<span data-ttu-id="dee87-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="dee87-259">protobuf</span></span>|<span data-ttu-id="dee87-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="dee87-260">protobuf</span></span>|
|<span data-ttu-id="dee87-261">PowerApps (separatore decimale punto)</span><span class="sxs-lookup"><span data-stu-id="dee87-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="dee87-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="dee87-262">powerapps-dot</span></span>|
|<span data-ttu-id="dee87-263">PowerApps (separatore decimale virgola)</span><span class="sxs-lookup"><span data-stu-id="dee87-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="dee87-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="dee87-264">powerapps-comma</span></span>|
|<span data-ttu-id="dee87-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="dee87-265">PowerShell</span></span>|<span data-ttu-id="dee87-266">powershell</span><span class="sxs-lookup"><span data-stu-id="dee87-266">powershell</span></span>|
|<span data-ttu-id="dee87-267">Python</span><span class="sxs-lookup"><span data-stu-id="dee87-267">Python</span></span>|<span data-ttu-id="dee87-268">python</span><span class="sxs-lookup"><span data-stu-id="dee87-268">python</span></span>|
|<span data-ttu-id="dee87-269">Q#</span><span class="sxs-lookup"><span data-stu-id="dee87-269">Q#</span></span>|<span data-ttu-id="dee87-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="dee87-270">qsharp</span></span>|
|<span data-ttu-id="dee87-271">R</span><span class="sxs-lookup"><span data-stu-id="dee87-271">R</span></span>|<span data-ttu-id="dee87-272">r</span><span class="sxs-lookup"><span data-stu-id="dee87-272">r</span></span>|
|<span data-ttu-id="dee87-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="dee87-273">Ruby</span></span>|<span data-ttu-id="dee87-274">ruby</span><span class="sxs-lookup"><span data-stu-id="dee87-274">ruby</span></span>|
|<span data-ttu-id="dee87-275">SQL</span><span class="sxs-lookup"><span data-stu-id="dee87-275">SQL</span></span>|<span data-ttu-id="dee87-276">sql</span><span class="sxs-lookup"><span data-stu-id="dee87-276">sql</span></span>|
|<span data-ttu-id="dee87-277">Swift</span><span class="sxs-lookup"><span data-stu-id="dee87-277">Swift</span></span>|<span data-ttu-id="dee87-278">swift</span><span class="sxs-lookup"><span data-stu-id="dee87-278">swift</span></span>|
|<span data-ttu-id="dee87-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="dee87-279">TypeScript</span></span>|<span data-ttu-id="dee87-280">typescript</span><span class="sxs-lookup"><span data-stu-id="dee87-280">typescript</span></span>|
|<span data-ttu-id="dee87-281">VB</span><span class="sxs-lookup"><span data-stu-id="dee87-281">VB</span></span>|<span data-ttu-id="dee87-282">vb</span><span class="sxs-lookup"><span data-stu-id="dee87-282">vb</span></span>|
|<span data-ttu-id="dee87-283">XAML</span><span class="sxs-lookup"><span data-stu-id="dee87-283">XAML</span></span>|<span data-ttu-id="dee87-284">xaml</span><span class="sxs-lookup"><span data-stu-id="dee87-284">xaml</span></span>|
|<span data-ttu-id="dee87-285">XML</span><span class="sxs-lookup"><span data-stu-id="dee87-285">XML</span></span>|<span data-ttu-id="dee87-286">xml</span><span class="sxs-lookup"><span data-stu-id="dee87-286">xml</span></span>|

<span data-ttu-id="dee87-287">Il nome `csharp-interactive` specifica il linguaggio C# e la capacità di eseguire gli esempi dal browser.</span><span class="sxs-lookup"><span data-stu-id="dee87-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="dee87-288">Questi frammenti di codice vengono compilati ed eseguiti in un contenitore Docker e i risultati dell'esecuzione del programma vengono visualizzati nella finestra del browser dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dee87-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="dee87-289">Esempio: C\#</span><span class="sxs-lookup"><span data-stu-id="dee87-289">Example: C\#</span></span>

<span data-ttu-id="dee87-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="dee87-290">__Markdown__</span></span>

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

<span data-ttu-id="dee87-291">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="dee87-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="dee87-292">Esempio: SQL</span><span class="sxs-lookup"><span data-stu-id="dee87-292">Example: SQL</span></span>

<span data-ttu-id="dee87-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="dee87-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="dee87-294">__Rendering__</span><span class="sxs-lookup"><span data-stu-id="dee87-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="dee87-295">Estensioni Markdown personalizzate di Docs</span><span class="sxs-lookup"><span data-stu-id="dee87-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="dee87-296">Docs.Microsoft.com (Docs) implementa il parser Markdig per Markdown, altamente compatibile con GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="dee87-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="dee87-297">Markdig aggiunge altre funzionalità tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="dee87-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="dee87-298">Di conseguenza, alcuni articoli della guida completa alla creazione in OPS sono inclusi in questa guida per riferimento</span><span class="sxs-lookup"><span data-stu-id="dee87-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="dee87-299">(vedere ad esempio "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario).</span><span class="sxs-lookup"><span data-stu-id="dee87-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="dee87-300">Gli articoli di Docs usano GFM per la maggior parte della formattazione, come paragrafi, collegamenti, elenchi, titoli e così via.</span><span class="sxs-lookup"><span data-stu-id="dee87-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="dee87-301">Per elementi di formattazione più elaborati, negli articoli è possibile usare funzionalità Markdig come:</span><span class="sxs-lookup"><span data-stu-id="dee87-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="dee87-302">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="dee87-302">Note blocks</span></span>
- <span data-ttu-id="dee87-303">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="dee87-303">Include files</span></span>
- <span data-ttu-id="dee87-304">Selettori</span><span class="sxs-lookup"><span data-stu-id="dee87-304">Selectors</span></span>
- <span data-ttu-id="dee87-305">Video incorporati</span><span class="sxs-lookup"><span data-stu-id="dee87-305">Embedded videos</span></span>
- <span data-ttu-id="dee87-306">Frammenti di codice/esempi</span><span class="sxs-lookup"><span data-stu-id="dee87-306">Code snippets/samples</span></span>

<span data-ttu-id="dee87-307">Per l'elenco completo, vedere "Markdig e le estensioni Markdown" e "Frammenti di codice" nel sommario.</span><span class="sxs-lookup"><span data-stu-id="dee87-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="dee87-308">Blocchi per le note</span><span class="sxs-lookup"><span data-stu-id="dee87-308">Note blocks</span></span>

<span data-ttu-id="dee87-309">Per attirare l'attenzione su contenuto specifico, è possibile scegliere tra quattro tipi di blocchi per le note:</span><span class="sxs-lookup"><span data-stu-id="dee87-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="dee87-310">NOTE</span><span class="sxs-lookup"><span data-stu-id="dee87-310">NOTE</span></span>
- <span data-ttu-id="dee87-311">WARNING</span><span class="sxs-lookup"><span data-stu-id="dee87-311">WARNING</span></span>
- <span data-ttu-id="dee87-312">TIP</span><span class="sxs-lookup"><span data-stu-id="dee87-312">TIP</span></span>
- <span data-ttu-id="dee87-313">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="dee87-313">IMPORTANT</span></span>

<span data-ttu-id="dee87-314">In generale è consigliabile usare i blocchi per le note sporadicamente, perché possono creare problemi.</span><span class="sxs-lookup"><span data-stu-id="dee87-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="dee87-315">Sebbene in questi blocchi siano supportati anche blocchi di codice, immagini, elenchi e collegamenti, provare a rendere i blocchi per le note il più possibile semplici e lineari.</span><span class="sxs-lookup"><span data-stu-id="dee87-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="dee87-316">Esempi:</span><span class="sxs-lookup"><span data-stu-id="dee87-316">Examples:</span></span>

```md
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

<span data-ttu-id="dee87-317">L'aspetto degli avvisi in docs.microsoft.com è il seguente:</span><span class="sxs-lookup"><span data-stu-id="dee87-317">These alerts look like this on docs.microsoft.com:</span></span>

![mostra l'aspetto degli avvisi dell'esempio precedente nella pagina di Docs pubblicata con icone e colori diversi](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="dee87-319">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="dee87-319">Include files</span></span>

<span data-ttu-id="dee87-320">In presenza di testo riutilizzabile o file di immagine che devono essere inclusi nei file degli articoli, è possibile usare un riferimento al file di "inclusione" tramite la funzionalità di inclusione file di Markdig.</span><span class="sxs-lookup"><span data-stu-id="dee87-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="dee87-321">Questa funzionalità indica a OPS di includere il file specificato nell'articolo in fase di compilazione, rendendolo così parte dell'articolo pubblicato.</span><span class="sxs-lookup"><span data-stu-id="dee87-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="dee87-322">Sono disponibili tre tipi di riferimenti di inclusione per agevolare il riutilizzo del contenuto:</span><span class="sxs-lookup"><span data-stu-id="dee87-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="dee87-323">Inline: riutilizzo di un frammento di testo comune inline all'interno di un'altra frase.</span><span class="sxs-lookup"><span data-stu-id="dee87-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="dee87-324">Blocco: riutilizzo di un intero file Markdown come blocco, annidato all'interno di una sezione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="dee87-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="dee87-325">Immagine: questa è l'implementazione standard dell'inclusione di immagini in Docs.</span><span class="sxs-lookup"><span data-stu-id="dee87-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="dee87-326">Le inclusioni di tipo Inline e Blocco sono semplici file di Markdown (MD),</span><span class="sxs-lookup"><span data-stu-id="dee87-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="dee87-327">che possono contenere qualsiasi codice Markdown valido.</span><span class="sxs-lookup"><span data-stu-id="dee87-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="dee87-328">Tutti i file di inclusione di Markdown devono essere posizionati in una [sottodirectory`/includes` comune](git-github-fundamentals.md#includes-subdirectory), nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="dee87-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="dee87-329">Al momento della pubblicazione dell'articolo, il file incluso viene integrato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dee87-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="dee87-330">Di seguito sono elencati i requisiti e le considerazioni per i file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="dee87-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="dee87-331">Usare un file di inclusione ogni volta che è necessario visualizzare lo stesso testo in più articoli.</span><span class="sxs-lookup"><span data-stu-id="dee87-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="dee87-332">Usare un riferimento di inclusione di tipo Blocco per quantità significative di contenuto, ad esempio uno o due paragrafi, una procedura o una sezione condivisa.</span><span class="sxs-lookup"><span data-stu-id="dee87-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="dee87-333">Non usarle per includere testi più piccoli di una frase.</span><span class="sxs-lookup"><span data-stu-id="dee87-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="dee87-334">I riferimenti di inclusione non vengono visualizzati nel rendering dell'articolo in GitHub, perché si basano su estensioni Markdig.</span><span class="sxs-lookup"><span data-stu-id="dee87-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="dee87-335">Saranno visualizzate solo dopo la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="dee87-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="dee87-336">Verificare che tutto il testo in un file di inclusione sia scritto con frasi complete o che non dipendono dal testo precedente o successivo nell'articolo che fa riferimento al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="dee87-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="dee87-337">Ignorare questa indicazione significa creare una stringa intraducibile nell'articolo con effetti negativi sull'esperienza localizzata.</span><span class="sxs-lookup"><span data-stu-id="dee87-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="dee87-338">Non incorporare riferimenti di inclusione in altri file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="dee87-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="dee87-339">Ciò non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dee87-339">They are not supported.</span></span>
- <span data-ttu-id="dee87-340">Posizionare i file multimediali in una cartella corrispondete, in una sottodirectory di inclusione, ad esempio la cartella `<repo>`/includi/file multimediali.</span><span class="sxs-lookup"><span data-stu-id="dee87-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="dee87-341">La directory media non deve includere immagini alla radice.</span><span class="sxs-lookup"><span data-stu-id="dee87-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="dee87-342">Se il file di inclusione non contiene immagini, non è necessaria una directory corrispondente per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="dee87-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="dee87-343">Come per gli articoli normali, non condividere elementi multimediali tra file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="dee87-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="dee87-344">Usare un file separato con un nome univoco per ogni file di inclusione e articolo.</span><span class="sxs-lookup"><span data-stu-id="dee87-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="dee87-345">Archiviare il file multimediale nella cartella dei file multimediali associata al file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="dee87-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="dee87-346">Non usare un file di inclusione come unico contenuto di un articolo.</span><span class="sxs-lookup"><span data-stu-id="dee87-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="dee87-347">I file di inclusione sono pensati come supplemento al contenuto nel resto dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="dee87-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="dee87-348">Esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="dee87-349">Selettori</span><span class="sxs-lookup"><span data-stu-id="dee87-349">Selectors</span></span>

<span data-ttu-id="dee87-350">Usare i selettori negli articoli tecnici quando si creano più versioni dello stesso articolo per gestire le differenze a livello di implementazione per tecnologie o piattaforme eterogenee.</span><span class="sxs-lookup"><span data-stu-id="dee87-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="dee87-351">Un esempio tipico è il contenuto per sviluppatori per la piattaforma per dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="dee87-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="dee87-352">In Markdig esistono attualmente due tipi di selettori, un selettore singolo e un selettore multiplo.</span><span class="sxs-lookup"><span data-stu-id="dee87-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="dee87-353">Poiché lo stesso selettore Markdown viene aggiunto in ogni articolo della selezione, è consigliabile inserire il selettore dell'articolo in un file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="dee87-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="dee87-354">A questo punto è possibile fare riferimento a quel file di inclusione in tutti gli articoli che usano lo stesso selettore.</span><span class="sxs-lookup"><span data-stu-id="dee87-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="dee87-355">Di seguito viene illustrato un esempio di selettore:</span><span class="sxs-lookup"><span data-stu-id="dee87-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="dee87-356">Per un esempio di selettori attivi, vedere la [documentazione di Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="dee87-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="dee87-357">Riferimenti di inclusione di codice</span><span class="sxs-lookup"><span data-stu-id="dee87-357">Code include references</span></span>

<span data-ttu-id="dee87-358">Markdig supporta l'inclusione avanzata di codice in un articolo, tramite l'estensione per i frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="dee87-358">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="dee87-359">Sono disponibili opzioni di rendering avanzate basate sulle funzionalità di GFM, come la scelta del linguaggio di programmazione e la colorazione della sintassi, oltre a funzionalità interessanti come:</span><span class="sxs-lookup"><span data-stu-id="dee87-359">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="dee87-360">Inclusione di esempi di codice/frammenti di codice centralizzati da un repository esterno.</span><span class="sxs-lookup"><span data-stu-id="dee87-360">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="dee87-361">Interfaccia utente a schede per visualizzare più versioni degli esempi di codice in linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="dee87-361">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="dee87-362">Problemi e risoluzione</span><span class="sxs-lookup"><span data-stu-id="dee87-362">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="dee87-363">Testo alternativo</span><span class="sxs-lookup"><span data-stu-id="dee87-363">Alt text</span></span>

<span data-ttu-id="dee87-364">Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="dee87-364">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="dee87-365">Ad esempio, invece di questa formattazione:</span><span class="sxs-lookup"><span data-stu-id="dee87-365">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="dee87-366">Usare caratteri di escape per i caratteri di sottolineatura come in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="dee87-366">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="dee87-367">Apostrofi e virgolette</span><span class="sxs-lookup"><span data-stu-id="dee87-367">Apostrophes and quotation marks</span></span>

<span data-ttu-id="dee87-368">Quando si copia da Word in un editor per Markdown, il testo potrebbe contenere apostrofi o virgolette curve,</span><span class="sxs-lookup"><span data-stu-id="dee87-368">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="dee87-369">che devono essere codificati o modificati in semplici apostrofi o virgolette.</span><span class="sxs-lookup"><span data-stu-id="dee87-369">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="dee87-370">In caso contrario, quando il file viene pubblicato, si ottiene questo risultato: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="dee87-370">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="dee87-371">Queste sono le codifiche per le versioni curve di questi segni di punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="dee87-371">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="dee87-372">Virgolette (aperte) a sinistra: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="dee87-372">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="dee87-373">Virgolette (chiuse) a destra: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="dee87-373">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="dee87-374">Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="dee87-374">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="dee87-375">Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="dee87-375">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="dee87-376">Parentesi acute</span><span class="sxs-lookup"><span data-stu-id="dee87-376">Angle brackets</span></span>

<span data-ttu-id="dee87-377">Le parentesi acute vengono comunemente usate per indicare un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="dee87-377">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="dee87-378">Se usate nel testo e non nel codice, le parentesi acute devono essere codificate.</span><span class="sxs-lookup"><span data-stu-id="dee87-378">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="dee87-379">In caso contrario, Markdown le interpreta come tag HTML.</span><span class="sxs-lookup"><span data-stu-id="dee87-379">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="dee87-380">Ad esempio, codificare `<script name>` come `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="dee87-380">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="dee87-381">Versione di Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-381">Markdown flavor</span></span>

<span data-ttu-id="dee87-382">Il back-end del sito docs.microsoft.com supporta il Markdown conforme a [CommonMark](https://commonmark.org/) analizzato tramite il motore di analisi [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="dee87-382">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="dee87-383">Questa versione di Markdown è per lo più compatibile con [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), perché la maggior parte dei documenti viene archiviata in GitHub dove può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="dee87-383">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="dee87-384">Altre funzionalità vengono aggiunte tramite le estensioni per Markdown.</span><span class="sxs-lookup"><span data-stu-id="dee87-384">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="dee87-385">Vedere anche:</span><span class="sxs-lookup"><span data-stu-id="dee87-385">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="dee87-386">Risorse per Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-386">Markdown resources</span></span>

- <span data-ttu-id="dee87-387">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax) (Introduzione a Markdown)</span><span class="sxs-lookup"><span data-stu-id="dee87-387">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="dee87-388">[Docs Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Scheda informativa su Markdown per Docs)</span><span class="sxs-lookup"><span data-stu-id="dee87-388">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="dee87-389">Nozioni di base su Markdown in GitHub</span><span class="sxs-lookup"><span data-stu-id="dee87-389">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="dee87-390">Guida Markdown</span><span class="sxs-lookup"><span data-stu-id="dee87-390">The Markdown Guide</span></span>](https://www.markdownguide.org/)
