---
title: manager-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637254"
---
# <a name="manager-missing"></a>manager-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Alcuni gruppi di contenuto richiedono l'attributo `manager` per identificare il manager dell'autore.

## <a name="resolution"></a>Risoluzione

Aggiungere un alias Microsoft valido per `manager`:

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
