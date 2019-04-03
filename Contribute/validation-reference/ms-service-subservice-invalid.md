---
title: ms-service-and-subservice-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637300"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="b36d0-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="b36d0-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b36d0-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="b36d0-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="b36d0-105">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="b36d0-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b36d0-106">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b36d0-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b36d0-107">I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="b36d0-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="b36d0-108">Il valore di `ms.service` non è valido oppure il valore di `ms.subservice` non forma una coppia valida con `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="b36d0-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b36d0-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b36d0-109">Resolution</span></span>

<span data-ttu-id="b36d0-110">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="b36d0-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b36d0-111">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="b36d0-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b36d0-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b36d0-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
