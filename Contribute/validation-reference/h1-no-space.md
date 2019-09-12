---
title: h1-no-space
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856244"
---
# <a name="h1-no-space"></a><span data-ttu-id="140e3-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="140e3-103">h1-no-space</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="140e3-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="140e3-104">Suggestion</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="140e3-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="140e3-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="140e3-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="140e3-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="140e3-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="140e3-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="140e3-108">Senza lo spazio dopo il codice hash, Docs non riconosce un H1.</span><span class="sxs-lookup"><span data-stu-id="140e3-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="140e3-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="140e3-109">Resolution</span></span>

<span data-ttu-id="140e3-110">Per correggere questo errore, aggiungere uno spazio dopo il codice hash ad H1.</span><span class="sxs-lookup"><span data-stu-id="140e3-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
