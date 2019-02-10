---
title: ms-prod-and-technology-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713270"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Presto disponibile.**

## <a name="warning"></a>Avviso

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Usare `ms.prod` per specificare i prodotti locali. Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`. I valori per `ms.prod` e `ms.technology` devono essere una coppia valida. Il valore di `ms.prod` non è valido oppure il valore di `ms.technology` non forma una coppia valida con `ms.prod`.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.prod` sia corretto per l'articolo. Scegliere quindi un valore di `ms.technology` valido.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
