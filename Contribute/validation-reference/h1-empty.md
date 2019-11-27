---
title: h1-empty
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528802"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Avviso

`H1 is required. Add content to your top-level heading.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.

## <a name="resolution"></a>Risoluzione

Per risolvere questo problema, assicurarsi che H1 includa il contenuto, non solo un codice hash.

Valore non valido:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Valore valido:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
