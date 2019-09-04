---
title: ms-prod-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236270"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="6b854-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="6b854-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="6b854-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="6b854-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="6b854-105">Usare `ms.prod` per specificare i prodotti locali.</span><span class="sxs-lookup"><span data-stu-id="6b854-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="6b854-106">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`, ma se si specifica `ms.technology`, è anche necessario specificare `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="6b854-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="6b854-107">I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="6b854-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b854-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="6b854-108">Resolution</span></span>

<span data-ttu-id="6b854-109">Verificare che il valore di `ms.technology` specificato sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="6b854-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="6b854-110">Aggiungere quindi il valore appropriato di `ms.prod`, in modo che sia un elemento padre valido per `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="6b854-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="6b854-111">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="6b854-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="6b854-112">Per richiedere nuovi valori, seguire [questa procedura](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="6b854-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
