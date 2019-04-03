---
title: ms-prod-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636771"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Usare `ms.prod` per specificare i prodotti locali. Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`, ma se si specifica `ms.technology`, è anche necessario specificare `ms.prod`. I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.technology` specificato sia corretto per l'articolo. Aggiungere quindi il valore appropriato di `ms.prod`, in modo che sia un elemento padre valido per `ms.technology`.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
