---
title: ms-prod-or-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: f4d5bc7537ec851ce7ac1de3be2208fd74cbe37f
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713546"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="e08e0-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="e08e0-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="e08e0-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="e08e0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e08e0-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="e08e0-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="e08e0-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="e08e0-106">Resolution</span></span>

<span data-ttu-id="e08e0-107">`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="e08e0-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="e08e0-108">Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.</span><span class="sxs-lookup"><span data-stu-id="e08e0-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="e08e0-109">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="e08e0-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]