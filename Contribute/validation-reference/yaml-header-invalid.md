---
title: yaml-header-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-topic-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459028"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Avviso

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Ciò significa in genere che un valore di metadati non racchiusi tra virgolette in un'intestazione YAML include una virgola o un altro carattere speciale. Può anche significare che manca uno spazio dopo i due punti in una coppia chiave/valore.

## <a name="resolution"></a>Risoluzione

Esaminare l'intestazione YAML. Cercare gli errori seguenti:

Due punti in un valore non racchiuso tra virgolette:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Modificare in:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Nessuno spazio dopo i due punti nella coppia chiave/valore:

```yml
---
title:I omitted a space.
---
```

Modificare in:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
