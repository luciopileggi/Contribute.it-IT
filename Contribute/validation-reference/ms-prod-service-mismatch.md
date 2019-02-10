---
title: ms-prod-service-mismatch
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713178"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="5acc0-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="5acc0-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="5acc0-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="5acc0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5acc0-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="5acc0-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="5acc0-106">Usare `ms.prod` per specificare i prodotti locali e `ms.service` per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="5acc0-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="5acc0-107">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="5acc0-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="5acc0-108">Per specificare informazioni più dettagliate su `ms.service`, è possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="5acc0-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="5acc0-109">Non è possibile usare `ms.prod` con `ms.subservice` o `ms.service` con `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="5acc0-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="5acc0-110">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="5acc0-110">Resolution</span></span>

<span data-ttu-id="5acc0-111">Verificare prima di tutto di aver selezionato l'attributo padre corretto (`ms.prod` o `ms.service`) per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="5acc0-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="5acc0-112">Aggiungere quindi il campo figlio appropriato con un valore abbinato valido.</span><span class="sxs-lookup"><span data-stu-id="5acc0-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="5acc0-113">Rimuovere eventuali campi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5acc0-113">Remove any extra fields.</span></span>

<span data-ttu-id="5acc0-114">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="5acc0-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
