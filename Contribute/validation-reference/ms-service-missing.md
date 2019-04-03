---
title: ms-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636702"
---
# <a name="ms-service-missing"></a>ms-service-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Usare `ms.service` per specificare i servizi cloud. Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`, ma se si specifica `ms.subservice`, è anche necessario specificare `ms.service`. I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.subservice` specificato sia corretto per l'articolo. Aggiungere quindi il valore appropriato di `ms.service`, in modo che sia un elemento padre valido per `ms.subservice`.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
