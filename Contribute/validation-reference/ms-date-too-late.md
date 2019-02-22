---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431485"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Presto disponibile.**

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
