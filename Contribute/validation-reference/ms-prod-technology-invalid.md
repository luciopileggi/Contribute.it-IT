---
title: ms-prod-and-technology-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713270"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="d5eef-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="d5eef-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="d5eef-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="d5eef-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="d5eef-105">Avviso</span><span class="sxs-lookup"><span data-stu-id="d5eef-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="d5eef-106">Usare `ms.prod` per specificare i prodotti locali.</span><span class="sxs-lookup"><span data-stu-id="d5eef-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="d5eef-107">Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="d5eef-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="d5eef-108">I valori per `ms.prod` e `ms.technology` devono essere una coppia valida.</span><span class="sxs-lookup"><span data-stu-id="d5eef-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="d5eef-109">Il valore di `ms.prod` non è valido oppure il valore di `ms.technology` non forma una coppia valida con `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="d5eef-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="d5eef-110">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="d5eef-110">Resolution</span></span>

<span data-ttu-id="d5eef-111">Verificare che il valore di `ms.prod` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="d5eef-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="d5eef-112">Scegliere quindi un valore di `ms.technology` valido.</span><span class="sxs-lookup"><span data-stu-id="d5eef-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="d5eef-113">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="d5eef-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
