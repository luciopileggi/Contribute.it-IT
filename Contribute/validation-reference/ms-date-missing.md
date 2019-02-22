---
title: ms-date-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431462"
---
# <a name="ms-date-missing"></a>ms-date-missing

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Questa data viene usata per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti. Non corrisponde alla data dell'ultima *pubblicazione* dell'articolo, che verrà visualizzata nella pagina se `ms.date` non è specificata esplicitamente.

## <a name="resolution"></a>Risoluzione

Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
