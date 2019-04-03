---
title: ms-prod-or-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8d8d01f95af74009cfa9cb1a57531663df4edf4d
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637369"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Risoluzione

`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud. Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]