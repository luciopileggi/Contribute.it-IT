---
title: ms-service-and-subservice-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236520"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="8c78e-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="8c78e-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8c78e-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="8c78e-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="8c78e-105">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="8c78e-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="8c78e-106">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8c78e-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="8c78e-107">I valori per `ms.service` e `ms.subservice` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="8c78e-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="8c78e-108">Il valore di `ms.service` non è valido oppure il valore di `ms.subservice` non forma una coppia valida con `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="8c78e-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c78e-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="8c78e-109">Resolution</span></span>

<span data-ttu-id="8c78e-110">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="8c78e-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="8c78e-111">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="8c78e-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="8c78e-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8c78e-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="8c78e-113">Per richiedere nuovi valori, seguire [questa procedura](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="8c78e-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
