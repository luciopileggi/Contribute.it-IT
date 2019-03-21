---
title: ms-service-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987722"
---
# <a name="ms-service-missing"></a><span data-ttu-id="bc1d2-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="bc1d2-103">ms-service-missing</span></span>

<span data-ttu-id="bc1d2-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="bc1d2-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bc1d2-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="bc1d2-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="bc1d2-106">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="bc1d2-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="bc1d2-107">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`, ma se si specifica `ms.subservice`, è anche necessario specificare `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="bc1d2-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="bc1d2-108">I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="bc1d2-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="bc1d2-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="bc1d2-109">Resolution</span></span>

<span data-ttu-id="bc1d2-110">Verificare che il valore di `ms.subservice` specificato sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="bc1d2-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="bc1d2-111">Aggiungere quindi il valore appropriato di `ms.service`, in modo che sia un elemento padre valido per `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="bc1d2-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="bc1d2-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="bc1d2-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
