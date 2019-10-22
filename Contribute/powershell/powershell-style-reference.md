---
title: Linee guida specifiche per la scrittura di informazioni di riferimento sui cmdlet
description: Questo articolo include le regole specifiche per la formattazione degli esempi di codice di PowerShell. Tali regole sono valide sia per gli articoli concettuali con esempi, che per le informazioni di riferimento sui cmdlet.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290289"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="94828-104">Aggiornamento degli articoli di riferimento</span><span class="sxs-lookup"><span data-stu-id="94828-104">Updating reference articles</span></span>

<span data-ttu-id="94828-105">Gli articoli di riferimento sui cmdlet hanno una struttura specifica.</span><span class="sxs-lookup"><span data-stu-id="94828-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="94828-106">Questa struttura è definita da [PlatyPS][].</span><span class="sxs-lookup"><span data-stu-id="94828-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="94828-107">PlatyPS è lo strumento usato da Microsoft per generare la Guida dei cmdlet per i moduli di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94828-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="94828-108">PlatyPS crea il file markdown di base per un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94828-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="94828-109">Dopo aver modificato i file markdown, si usa PlatyPS per creare i file della Guida MAML usati dal cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="94828-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="94828-110">PlatyPS dispone di uno schema hardcoded per le informazioni di riferimento sui cmdlet scritte nel codice.</span><span class="sxs-lookup"><span data-stu-id="94828-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="94828-111">Il documento [platyPS.schema.md][] tenta di descrivere la struttura.</span><span class="sxs-lookup"><span data-stu-id="94828-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="94828-112">Le violazioni dello schema causano errori di compilazione che devono essere corretti prima di poter accettare il contributo.</span><span class="sxs-lookup"><span data-stu-id="94828-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="94828-113">Linee guida generali</span><span class="sxs-lookup"><span data-stu-id="94828-113">General guidelines</span></span>

- <span data-ttu-id="94828-114">Non rimuovere alcuna struttura nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="94828-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="94828-115">PlatyPS prevede un set specifico di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="94828-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="94828-116">Le intestazioni **Input type** e **Output type** devono avere un tipo.</span><span class="sxs-lookup"><span data-stu-id="94828-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="94828-117">Se il cmdlet non accetta input o restituisce un valore, usare il valore "None".</span><span class="sxs-lookup"><span data-stu-id="94828-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="94828-118">I blocchi di codice delimitati sono consentiti solo nella sezione [Esempi](#format-for-examples).</span><span class="sxs-lookup"><span data-stu-id="94828-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="94828-119">Gli intervalli di codice inline possono essere usati in qualsiasi paragrafo.</span><span class="sxs-lookup"><span data-stu-id="94828-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="94828-120">Formattazione dei file About_</span><span class="sxs-lookup"><span data-stu-id="94828-120">Formatting About_ files</span></span>

<span data-ttu-id="94828-121">I file `About_*` vengono ora elaborati da [Pandoc][], anziché da PlatyPS.</span><span class="sxs-lookup"><span data-stu-id="94828-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="94828-122">I file `About_*` sono formattati in modo da ottenere la massima compatibilità con tutte le versioni di PowerShell e con gli strumenti di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="94828-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="94828-123">Non modificare la formattazione dei file `about_*` senza verificare prima con un responsabile della manutenzione del repository.</span><span class="sxs-lookup"><span data-stu-id="94828-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="94828-124">Linee guida di base per la formattazione:</span><span class="sxs-lookup"><span data-stu-id="94828-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="94828-125">Limitare le righe a 80 caratteri</span><span class="sxs-lookup"><span data-stu-id="94828-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="94828-126">I blocchi di codice, le citazioni e le tabelle sono limitati a 76 caratteri perché Pandoc applica un rientro di quattro spazi a questi elementi durante la conversione</span><span class="sxs-lookup"><span data-stu-id="94828-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="94828-127">Le tabelle devono rientrare nei 76 caratteri</span><span class="sxs-lookup"><span data-stu-id="94828-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="94828-128">Mandare a capo manualmente il contenuto delle celle su più righe</span><span class="sxs-lookup"><span data-stu-id="94828-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="94828-129">Usare i caratteri `|` di apertura e chiusura per ogni riga</span><span class="sxs-lookup"><span data-stu-id="94828-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="94828-130">Vedere un esempio funzionante in [about_Comparison_Operators][about-example]</span><span class="sxs-lookup"><span data-stu-id="94828-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="94828-131">Quando si usano i caratteri speciali di Pandoc `\`, `$`, `` ` `` e `<`</span><span class="sxs-lookup"><span data-stu-id="94828-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="94828-132">All'interno di un'intestazione questi caratteri devono essere preceduti dal carattere di escape `\`</span><span class="sxs-lookup"><span data-stu-id="94828-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="94828-133">All'interno di un paragrafo questi caratteri devono essere inseriti in intervalli di codice.</span><span class="sxs-lookup"><span data-stu-id="94828-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="94828-134">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="94828-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="94828-135">Formato per gli esempi</span><span class="sxs-lookup"><span data-stu-id="94828-135">Format for examples</span></span>

<span data-ttu-id="94828-136">Nello schema PlatyPS l'intestazione **EXAMPLES** è un'intestazione H2 e ogni esempio è un'intestazione H3.</span><span class="sxs-lookup"><span data-stu-id="94828-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="94828-137">All'interno di un esempio, lo schema non consente la separazione dei blocchi di codice tramite paragrafi.</span><span class="sxs-lookup"><span data-stu-id="94828-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="94828-138">Lo schema valido è:</span><span class="sxs-lookup"><span data-stu-id="94828-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="94828-139">Numerare ogni esempio e aggiungere un breve titolo.</span><span class="sxs-lookup"><span data-stu-id="94828-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="94828-140">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="94828-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org