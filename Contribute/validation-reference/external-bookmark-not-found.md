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
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Avviso

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Si sta tentando di effettuare il collegamento a un'intestazione in un altro file non esistente.

## <a name="resolution"></a>Risoluzione

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Esaminare il file a cui si sta effettuando il collegamento e aggiornare il collegamento al segnalibro in modo che punti a una sezione valida nel file.

Per creare un collegamento a un'intestazione di sezione in un altro articolo, usare il collegamento relativo al file o al sito più un simbolo hash, seguito dalle parole dell'intestazione. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini. Di seguito è riportato un esempio.

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
