---
title: multiple-h1
description: Spiegazione e risoluzione del problema di compilazione di Docs multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427894"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>Avviso

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione. È possibile avere solo un H1 in ogni file.

## <a name="resolution"></a>Risoluzione

Per risolvere questo problema, modificare il livello di intestazione di H1 successivi in H2 (`##`), o in caso contrario, riorganizzare il file. Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]