---
title: ms-prod-or-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987561"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="db0cb-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="db0cb-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="db0cb-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="db0cb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="db0cb-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="db0cb-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="db0cb-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="db0cb-106">Resolution</span></span>

<span data-ttu-id="db0cb-107">`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="db0cb-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="db0cb-108">Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.</span><span class="sxs-lookup"><span data-stu-id="db0cb-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="db0cb-109">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="db0cb-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]