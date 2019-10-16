---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288509"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Avviso

`Missing attribute: author. Add the current author's GitHub ID.`

L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub. 

## <a name="resolution"></a>Risoluzione

Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
