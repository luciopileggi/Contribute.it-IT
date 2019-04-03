---
title: ms-prod-and-technology-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636840"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Avviso

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Usare `ms.prod` per specificare i prodotti locali. Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`. I valori per `ms.prod` e `ms.technology` devono essere una coppia valida. Il valore di `ms.prod` non è valido oppure il valore di `ms.technology` non forma una coppia valida con `ms.prod`.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.prod` sia corretto per l'articolo. Scegliere quindi un valore di `ms.technology` valido.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
