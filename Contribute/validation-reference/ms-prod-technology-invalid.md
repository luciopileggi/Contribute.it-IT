---
title: ms-prod-and-technology-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987584"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="fa255-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="fa255-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="fa255-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="fa255-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="fa255-105">Avviso</span><span class="sxs-lookup"><span data-stu-id="fa255-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="fa255-106">Usare `ms.prod` per specificare i prodotti locali.</span><span class="sxs-lookup"><span data-stu-id="fa255-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="fa255-107">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="fa255-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="fa255-108">I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="fa255-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="fa255-109">Il valore di `ms.prod` non è valido oppure il valore di `ms.technology` non forma una coppia valida con `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="fa255-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="fa255-110">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="fa255-110">Resolution</span></span>

<span data-ttu-id="fa255-111">Verificare che il valore di `ms.prod` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="fa255-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="fa255-112">Scegliere quindi un valore di `ms.technology` valido.</span><span class="sxs-lookup"><span data-stu-id="fa255-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="fa255-113">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="fa255-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
