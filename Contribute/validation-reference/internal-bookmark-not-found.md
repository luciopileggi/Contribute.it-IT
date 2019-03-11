---
title: internal-bookmark-not-found
description: Spiegazione e risoluzione del problema di compilazione di Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427830"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="4ee9b-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="4ee9b-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="4ee9b-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="4ee9b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4ee9b-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="4ee9b-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="4ee9b-106">Si sta tentando di effettuare il collegamento a un'intestazione nel file corrente non esistente.</span><span class="sxs-lookup"><span data-stu-id="4ee9b-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="4ee9b-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="4ee9b-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="4ee9b-108">Verificare l'intestazione a cui si desidera effettuare il collegamento e aggiornare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="4ee9b-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="4ee9b-109">Per creare un collegamento a una sezione dell'articolo corrente, usare un simbolo hash, seguito dalle parole dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee9b-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="4ee9b-110">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini.</span><span class="sxs-lookup"><span data-stu-id="4ee9b-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="4ee9b-111">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="4ee9b-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
