---
title: h1-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848463"
---
# <a name="h1-missing"></a><span data-ttu-id="a05f0-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="a05f0-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a05f0-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="a05f0-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="a05f0-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="a05f0-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a05f0-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="a05f0-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="a05f0-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="a05f0-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="a05f0-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="a05f0-108">Resolution</span></span>

<span data-ttu-id="a05f0-109">Per risolvere questo problema, aggiungere un H1 come primo contenuto dopo il blocco metadati YML nel file:</span><span class="sxs-lookup"><span data-stu-id="a05f0-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="a05f0-110">Questa regola non si applica ai file inclusi.</span><span class="sxs-lookup"><span data-stu-id="a05f0-110">This rule does not apply to included files.</span></span> <span data-ttu-id="a05f0-111">Se vengono visualizzati avvisi H1 nei file inclusi, probabilmente è necessario spostare i file inclusi in una cartella `includes`.</span><span class="sxs-lookup"><span data-stu-id="a05f0-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="a05f0-112">La cartella `includes` può essere in qualsiasi livello nel percorso del file.</span><span class="sxs-lookup"><span data-stu-id="a05f0-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="a05f0-113">In base al percorso, la compilazione di Docs riconoscerà il file come file incluso e le convalide H1 non verranno eseguite.</span><span class="sxs-lookup"><span data-stu-id="a05f0-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]