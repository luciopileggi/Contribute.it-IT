---
title: ms-service-and-subservice-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713132"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="ecef7-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="ecef7-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="ecef7-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="ecef7-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="ecef7-105">Avviso</span><span class="sxs-lookup"><span data-stu-id="ecef7-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="ecef7-106">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="ecef7-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="ecef7-107">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="ecef7-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="ecef7-108">I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="ecef7-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="ecef7-109">Il valore di `ms.service` non è valido oppure il valore di `ms.subservice` non forma una coppia valida con `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="ecef7-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="ecef7-110">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="ecef7-110">Resolution</span></span>

<span data-ttu-id="ecef7-111">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="ecef7-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="ecef7-112">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="ecef7-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="ecef7-113">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="ecef7-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
