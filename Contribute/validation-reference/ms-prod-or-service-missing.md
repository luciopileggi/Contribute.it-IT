---
title: ms-prod-or-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: f4d5bc7537ec851ce7ac1de3be2208fd74cbe37f
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713546"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Risoluzione

`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud. Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]