---
title: ms-service-and-subservice-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713132"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Presto disponibile.**

## <a name="warning"></a>Avviso

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Usare `ms.service` per specificare i servizi cloud. Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`. I valori per `ms.service` e `ms.subservice` devono essere una coppia valida. Il valore di `ms.service` non è valido oppure il valore di `ms.subservice` non forma una coppia valida con `ms.service`.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.service` sia corretto per l'articolo. Scegliere quindi un valore di `ms.subservice` valido.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
