---
title: ms-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713086"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Usare `ms.service` per specificare i servizi cloud. Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`, ma se si specifica `ms.subservice`, è anche necessario specificare `ms.service`. I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.subservice` specificato sia corretto per l'articolo. Aggiungere quindi il valore appropriato di `ms.service`, in modo che sia un elemento padre valido per `ms.subservice`.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
