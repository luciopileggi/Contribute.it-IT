---
title: h1-empty
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427689"
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