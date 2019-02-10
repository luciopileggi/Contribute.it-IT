---
title: ms-prod-and-service
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 42e6f063c8b3d97386b2655b49a19a3e103d6b3b
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713201"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="21e74-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="21e74-103">ms-prod-and-service</span></span>

<span data-ttu-id="21e74-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="21e74-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="21e74-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="21e74-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="21e74-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="21e74-106">Resolution</span></span>

<span data-ttu-id="21e74-107">`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="21e74-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="21e74-108">Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.</span><span class="sxs-lookup"><span data-stu-id="21e74-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="21e74-109">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="21e74-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
