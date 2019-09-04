---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236274"
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
