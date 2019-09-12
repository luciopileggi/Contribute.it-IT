---
title: internal-bookmark-not-found
description: Spiegazione e risoluzione del problema di compilazione di Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856221"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="e63e4-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="e63e4-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="e63e4-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="e63e4-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="e63e4-105">Si sta tentando di eseguire il collegamento a un'intestazione nel file corrente o in un altro file che non esiste.</span><span class="sxs-lookup"><span data-stu-id="e63e4-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="e63e4-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="e63e4-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="e63e4-107">Verificare l'intestazione a cui si desidera effettuare il collegamento e aggiornare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="e63e4-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="e63e4-108">Per creare un collegamento a una sezione dell'articolo corrente, usare un simbolo hash, seguito dalle parole dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="e63e4-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="e63e4-109">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini.</span><span class="sxs-lookup"><span data-stu-id="e63e4-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="e63e4-110">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="e63e4-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="e63e4-111">Per eseguire il collegamento a un'intestazione in un altro file usare un collegamento relativo a tale file, seguito da un simbolo di hash e dalle parole dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="e63e4-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="e63e4-112">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini.</span><span class="sxs-lookup"><span data-stu-id="e63e4-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="e63e4-113">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="e63e4-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
