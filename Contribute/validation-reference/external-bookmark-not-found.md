---
title: external-bookmark-not-found
description: Spiegazione e risoluzione del problema di compilazione di Docs external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427770"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="b4e25-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="b4e25-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="b4e25-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="b4e25-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="b4e25-105">Si sta tentando di effettuare il collegamento a un'intestazione in un altro file non esistente.</span><span class="sxs-lookup"><span data-stu-id="b4e25-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4e25-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b4e25-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="b4e25-107">Esaminare il file a cui si sta effettuando il collegamento e aggiornare il collegamento al segnalibro in modo che punti a una sezione valida nel file.</span><span class="sxs-lookup"><span data-stu-id="b4e25-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="b4e25-108">Per creare un collegamento a un'intestazione di sezione in un altro articolo, usare il collegamento relativo al file o al sito più un simbolo hash, seguito dalle parole dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="b4e25-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="b4e25-109">Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini.</span><span class="sxs-lookup"><span data-stu-id="b4e25-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="b4e25-110">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="b4e25-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
