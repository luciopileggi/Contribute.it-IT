---
title: multiple-h1
description: Spiegazione e risoluzione del problema di compilazione di Docs multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848598"
---
# <a name="multiple-h1"></a><span data-ttu-id="1eacc-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="1eacc-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="1eacc-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="1eacc-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="1eacc-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="1eacc-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="1eacc-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="1eacc-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="1eacc-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="1eacc-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="1eacc-108">È possibile avere solo un H1 in ogni file.</span><span class="sxs-lookup"><span data-stu-id="1eacc-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="1eacc-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="1eacc-109">Resolution</span></span>

<span data-ttu-id="1eacc-110">Per risolvere questo problema, modificare il livello di intestazione di H1 successivi in H2 (`##`), o in caso contrario, riorganizzare il file.</span><span class="sxs-lookup"><span data-stu-id="1eacc-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="1eacc-111">Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.</span><span class="sxs-lookup"><span data-stu-id="1eacc-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]