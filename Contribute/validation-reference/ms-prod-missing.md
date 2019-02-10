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
# <a name="ms-prod-missing"></a><span data-ttu-id="533cb-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="533cb-103">ms-prod-missing</span></span>

<span data-ttu-id="533cb-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="533cb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="533cb-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="533cb-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="533cb-106">Usare `ms.prod` per specificare i prodotti locali.</span><span class="sxs-lookup"><span data-stu-id="533cb-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="533cb-107">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`, ma se si specifica `ms.technology`, è anche necessario specificare `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="533cb-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="533cb-108">I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="533cb-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="533cb-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="533cb-109">Resolution</span></span>

<span data-ttu-id="533cb-110">Verificare che il valore di `ms.technology` specificato sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="533cb-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="533cb-111">Aggiungere quindi il valore appropriato di `ms.prod`, in modo che sia un elemento padre valido per `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="533cb-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="533cb-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="533cb-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
