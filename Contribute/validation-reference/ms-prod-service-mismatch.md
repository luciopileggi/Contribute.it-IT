---
title: ms-prod-service-mismatch
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636794"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="e8313-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="e8313-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e8313-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="e8313-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="e8313-105">Usare `ms.prod` per specificare i prodotti locali e `ms.service` per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="e8313-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="e8313-106">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="e8313-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="e8313-107">Per specificare informazioni più dettagliate su `ms.service`, è possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="e8313-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="e8313-108">Non è possibile usare `ms.prod` con `ms.subservice` o `ms.service` con `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="e8313-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="e8313-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="e8313-109">Resolution</span></span>

<span data-ttu-id="e8313-110">Verificare prima di tutto di aver selezionato l'attributo padre corretto (`ms.prod` o `ms.service`) per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="e8313-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="e8313-111">Aggiungere quindi il campo figlio appropriato con un valore abbinato valido.</span><span class="sxs-lookup"><span data-stu-id="e8313-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="e8313-112">Rimuovere eventuali campi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e8313-112">Remove any extra fields.</span></span>

<span data-ttu-id="e8313-113">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e8313-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
