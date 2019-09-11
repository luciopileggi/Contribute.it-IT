---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848569"
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
