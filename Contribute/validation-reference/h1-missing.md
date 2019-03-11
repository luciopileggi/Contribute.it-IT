---
title: h1-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459120"
---
# <a name="h1-missing"></a><span data-ttu-id="d0481-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="d0481-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="d0481-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="d0481-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="d0481-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="d0481-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="d0481-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="d0481-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="d0481-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="d0481-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="d0481-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="d0481-108">Resolution</span></span>

<span data-ttu-id="d0481-109">Per risolvere questo problema, aggiungere un H1 come primo contenuto dopo il blocco metadati YML nel file:</span><span class="sxs-lookup"><span data-stu-id="d0481-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="d0481-110">Questa regola non si applica ai file inclusi.</span><span class="sxs-lookup"><span data-stu-id="d0481-110">This rule does not apply to included files.</span></span> <span data-ttu-id="d0481-111">Se vengono visualizzati avvisi H1 nei file inclusi, probabilmente è necessario spostare i file inclusi in una cartella `includes`.</span><span class="sxs-lookup"><span data-stu-id="d0481-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="d0481-112">La cartella `includes` può essere in qualsiasi livello nel percorso del file.</span><span class="sxs-lookup"><span data-stu-id="d0481-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="d0481-113">In base al percorso, la compilazione di Docs riconoscerà il file come file incluso e le convalide H1 non verranno eseguite.</span><span class="sxs-lookup"><span data-stu-id="d0481-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]