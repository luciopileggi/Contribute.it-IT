---
title: ms-prod-service-mismatch
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987616"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="b9661-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="b9661-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="b9661-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="b9661-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b9661-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="b9661-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="b9661-106">Usare `ms.prod` per specificare i prodotti locali e `ms.service` per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="b9661-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="b9661-107">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="b9661-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="b9661-108">Per specificare informazioni più dettagliate su `ms.service`, è possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b9661-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="b9661-109">Non è possibile usare `ms.prod` con `ms.subservice` o `ms.service` con `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="b9661-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b9661-110">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b9661-110">Resolution</span></span>

<span data-ttu-id="b9661-111">Verificare prima di tutto di aver selezionato l'attributo padre corretto (`ms.prod` o `ms.service`) per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="b9661-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="b9661-112">Aggiungere quindi il campo figlio appropriato con un valore abbinato valido.</span><span class="sxs-lookup"><span data-stu-id="b9661-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="b9661-113">Rimuovere eventuali campi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b9661-113">Remove any extra fields.</span></span>

<span data-ttu-id="b9661-114">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b9661-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
