---
title: no-space-in-h1
description: Spiegazione e risoluzione del problema di compilazione di Docs no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427849"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Avviso

`A space is required after the hash (#) in H1.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione. Senza lo spazio dopo il codice hash, Docs non riconosce un H1.

## <a name="resolution"></a>Risoluzione

Per correggere questo errore, aggiungere uno spazio dopo il codice hash ad H1.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]