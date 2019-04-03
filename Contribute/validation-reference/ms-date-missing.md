---
title: ms-date-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637277"
---
# <a name="ms-date-missing"></a><span data-ttu-id="786f2-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="786f2-103">ms-date-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="786f2-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="786f2-104">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="786f2-105">Alcuni gruppi di contenuto usano `ms.date` per indicare il livello di aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="786f2-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="786f2-106">Non corrisponde alla data dell'ultima *pubblicazione* dell'articolo, che verrà visualizzata nella pagina se `ms.date` non è specificata esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="786f2-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="786f2-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="786f2-107">Resolution</span></span>

<span data-ttu-id="786f2-108">Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="786f2-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
