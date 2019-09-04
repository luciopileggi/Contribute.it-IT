---
title: ms-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236489"
---
# <a name="ms-service-missing"></a><span data-ttu-id="5c5b4-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="5c5b4-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="5c5b4-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="5c5b4-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="5c5b4-105">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="5c5b4-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="5c5b4-106">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`, ma se si specifica `ms.subservice`, è anche necessario specificare `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="5c5b4-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="5c5b4-107">I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="5c5b4-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="5c5b4-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="5c5b4-108">Resolution</span></span>

<span data-ttu-id="5c5b4-109">Verificare che il valore di `ms.subservice` specificato sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="5c5b4-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="5c5b4-110">Aggiungere quindi il valore appropriato di `ms.service`, in modo che sia un elemento padre valido per `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="5c5b4-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="5c5b4-111">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="5c5b4-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="5c5b4-112">Per richiedere nuovi valori, seguire [questa procedura](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="5c5b4-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
