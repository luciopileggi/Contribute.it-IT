---
title: ms-prod-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713224"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Usare `ms.prod` per specificare i prodotti locali. Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`, ma se si specifica `ms.technology`, è anche necessario specificare `ms.prod`. I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.technology` specificato sia corretto per l'articolo. Aggiungere quindi il valore appropriato di `ms.prod`, in modo che sia un elemento padre valido per `ms.technology`.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
