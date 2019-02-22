---
title: ms-date-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431462"
---
# <a name="ms-date-missing"></a><span data-ttu-id="9aa6d-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="9aa6d-103">ms-date-missing</span></span>

<span data-ttu-id="9aa6d-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="9aa6d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9aa6d-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="9aa6d-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="9aa6d-106">Questa data viene usata per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="9aa6d-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="9aa6d-107">Non corrisponde alla data dell'ultima *pubblicazione* dell'articolo, che verrà visualizzata nella pagina se `ms.date` non è specificata esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="9aa6d-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="9aa6d-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="9aa6d-108">Resolution</span></span>

<span data-ttu-id="9aa6d-109">Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="9aa6d-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
