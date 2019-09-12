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
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Avviso

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

Si sta tentando di eseguire il collegamento a un'intestazione nel file corrente o in un altro file che non esiste.

## <a name="resolution"></a>Risoluzione

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Verificare l'intestazione a cui si desidera effettuare il collegamento e aggiornare il collegamento.

Per creare un collegamento a una sezione dell'articolo corrente, usare un simbolo hash, seguito dalle parole dell'intestazione. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini. Di seguito è riportato un esempio.

```markdown
[Managed Disks](#managed-disks)
```

Per eseguire il collegamento a un'intestazione in un altro file usare un collegamento relativo a tale file, seguito da un simbolo di hash e dalle parole dell'intestazione. Rimuovere i segni di punteggiatura dall'intestazione e sostituire gli spazi con trattini. Di seguito è riportato un esempio.

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
