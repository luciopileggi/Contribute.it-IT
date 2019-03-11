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
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Current file doesn't contain a bookmark named '{bookmark}'.`

Si sta tentando di effettuare il collegamento a un'intestazione nel file corrente non esistente.

## <a name="resolution"></a>Risoluzione

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Verificare l'intestazione a cui si desidera effettuare il collegamento e aggiornare il collegamento.

Per creare un collegamento a una sezione dell'articolo corrente, usare un simbolo hash, seguito dalle parole dell'intestazione. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini. Di seguito è riportato un esempio.

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
