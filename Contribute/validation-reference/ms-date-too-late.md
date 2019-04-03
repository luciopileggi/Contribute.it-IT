---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637392"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Avviso

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

L'attributo `ms.date` viene usato per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti. L'attributo non può quindi essere una data futura. È consentito un massimo di cinque giorni prima della data di rilascio, ad esempio quando il contenuto viene bloccato per il controllo di qualità in preparazione di un evento importante.

## <a name="resolution"></a>Risoluzione

Specificare una `ms.date` fino a cinque giorni successiva a quella corrente, in formato MM/GG/AAAA:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
