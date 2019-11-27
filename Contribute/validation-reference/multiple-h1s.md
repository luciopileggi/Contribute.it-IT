---
title: multiple-h1s
description: Spiegazione e risoluzione del problema di compilazione di Docs multiple-h1s.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528933"
---
# <a name="multiple-h1s"></a><span data-ttu-id="ed936-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="ed936-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ed936-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="ed936-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="ed936-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="ed936-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="ed936-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="ed936-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="ed936-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ed936-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="ed936-108">È possibile avere solo un H1 in ogni file.</span><span class="sxs-lookup"><span data-stu-id="ed936-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="ed936-109">Questo messaggio potrebbe essere visualizzato anche se l'articolo contiene una riga di segni di uguale per ottenere una doppia sottolineatura, come questa: `=======`.</span><span class="sxs-lookup"><span data-stu-id="ed936-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="ed936-110">Si tratta di una sintassi Markdown alternativa per un H1.</span><span class="sxs-lookup"><span data-stu-id="ed936-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="ed936-111">Viene anche comunemente visualizzato nei conflitti di merge:</span><span class="sxs-lookup"><span data-stu-id="ed936-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="ed936-112">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="ed936-112">Resolution</span></span>

<span data-ttu-id="ed936-113">Per risolvere questo problema, modificare il livello di intestazione di H1 successivi in H2 (`##`), o in caso contrario, riorganizzare il file.</span><span class="sxs-lookup"><span data-stu-id="ed936-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="ed936-114">Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.</span><span class="sxs-lookup"><span data-stu-id="ed936-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="ed936-115">Se un'intestazione H1 aggiuntiva è effettivamente una doppia sottolineatura (`=======`), rimuoverla o sostituirla con un'intestazione hashtag, ad esempio `##`, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ed936-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="ed936-116">Se la doppia sottolineatura fa parte di un conflitto di merge, assicurarsi di rimuovere anche gli indicatori di inizio e fine del conflitto di merge e il testo obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ed936-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
