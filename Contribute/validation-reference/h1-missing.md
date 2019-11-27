---
title: h1-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528883"
---
# <a name="h1-missing"></a><span data-ttu-id="5c92e-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="5c92e-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5c92e-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="5c92e-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="5c92e-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="5c92e-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5c92e-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="5c92e-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5c92e-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="5c92e-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="5c92e-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="5c92e-108">Resolution</span></span>

<span data-ttu-id="5c92e-109">Per risolvere questo problema, aggiungere un H1 come primo contenuto dopo il blocco metadati YML nel file:</span><span class="sxs-lookup"><span data-stu-id="5c92e-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="5c92e-110">Questa regola non si applica ai file inclusi.</span><span class="sxs-lookup"><span data-stu-id="5c92e-110">This rule does not apply to included files.</span></span> <span data-ttu-id="5c92e-111">Se vengono visualizzati risultati H1 nei file inclusi, probabilmente è necessario spostare i file inclusi in una cartella `includes`.</span><span class="sxs-lookup"><span data-stu-id="5c92e-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="5c92e-112">La cartella `includes` può essere in qualsiasi livello nel percorso del file.</span><span class="sxs-lookup"><span data-stu-id="5c92e-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="5c92e-113">In base al percorso, la compilazione di Docs riconoscerà il file come file incluso e le convalide H1 non verranno eseguite.</span><span class="sxs-lookup"><span data-stu-id="5c92e-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="5c92e-114">Una delle cause comuni di H1 mancanti nei file padre è l'utilizzo improprio dei file inclusi: l'H1 si trova nel file incluso, non nel file padre.</span><span class="sxs-lookup"><span data-stu-id="5c92e-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="5c92e-115">Questa operazione non è consentita perché l'utilizzo di un H1 in un file incluso indica che ci sono H1 duplicati nei file padre oppure che il file incluso viene usato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="5c92e-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="5c92e-116">Gli H1 devono essere univoci all'interno di un set di contenuto e i file inclusi devono essere usati solo per condividere contenuto tra più file.</span><span class="sxs-lookup"><span data-stu-id="5c92e-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="5c92e-117">Se vengono visualizzati risultati `h1-missing` perché l'H1 si trova in un file incluso, la soluzione consiste nello spostare l'H1 e tutto il contenuto incluso se il file incluso viene usato solo una volta nel file padre.</span><span class="sxs-lookup"><span data-stu-id="5c92e-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="5c92e-118">Per altre informazioni sui file inclusi in Docs, vedere l'articolo interno Microsoft [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master) (Includere contenuto riutilizzabile negli articoli).</span><span class="sxs-lookup"><span data-stu-id="5c92e-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
