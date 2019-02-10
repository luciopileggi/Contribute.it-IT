---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713109"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Presto disponibile.**

## <a name="warning"></a>Avviso

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

L'attributo `ms.date` viene usato per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti. L'attributo non può quindi essere una data futura. È consentito un massimo di cinque giorni prima della data di rilascio, ad esempio quando il contenuto viene bloccato per il controllo di qualità in preparazione di un evento importante.

## <a name="resolution"></a>Risoluzione

Specificare una `ms.date` fino a cinque giorni successiva a quella corrente, in formato MM/GG/AAAA.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
