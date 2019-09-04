---
title: ms-date-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236283"
---
# <a name="ms-date-missing"></a>ms-date-missing

## <a name="warning"></a>Avviso

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Alcuni gruppi di contenuto usano `ms.date` per indicare il livello di aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti. Non corrisponde alla data dell'ultima *pubblicazione* dell'articolo, che verrà visualizzata nella pagina se `ms.date` non è specificata esplicitamente.

## <a name="resolution"></a>Risoluzione

Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
