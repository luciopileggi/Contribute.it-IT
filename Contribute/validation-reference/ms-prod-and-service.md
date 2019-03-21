---
title: ms-prod-and-service
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987676"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="65b6e-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="65b6e-103">ms-prod-and-service</span></span>

<span data-ttu-id="65b6e-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="65b6e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="65b6e-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="65b6e-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="65b6e-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="65b6e-106">Resolution</span></span>

<span data-ttu-id="65b6e-107">`ms.prod` o `ms.service` è obbligatorio e non possono essere presenti entrambi: `ms.prod` viene usato per i prodotti locali, `ms.service` viene usato per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="65b6e-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="65b6e-108">Determinare il campo appropriato per l'articolo, verificare che il valore sia corretto e rimuovere l'altro campo.</span><span class="sxs-lookup"><span data-stu-id="65b6e-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="65b6e-109">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="65b6e-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
