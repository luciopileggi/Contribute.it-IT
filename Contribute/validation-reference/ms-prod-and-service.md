---
title: ms-prod-and-service
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 77c0dd71cf526ee837799bcd01e21290ce7d6058
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636748"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="c2bb5-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="c2bb5-103">ms-prod-and-service</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c2bb5-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="c2bb5-104">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="c2bb5-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="c2bb5-105">Resolution</span></span>

<span data-ttu-id="c2bb5-106">`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="c2bb5-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="c2bb5-107">Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.</span><span class="sxs-lookup"><span data-stu-id="c2bb5-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="c2bb5-108">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="c2bb5-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
