---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481710"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="b2cf4-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="b2cf4-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="b2cf4-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="b2cf4-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="b2cf4-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b2cf4-105">Resolution</span></span>

<span data-ttu-id="b2cf4-106">Verificare che il valore `ms.author` sia l'alias Microsoft valido dell'autore corrente.</span><span class="sxs-lookup"><span data-stu-id="b2cf4-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="b2cf4-107">È consigliabile che l'autore designato sia un dipendente a tempo pieno o una lista di distribuzione di team, anziché un fornitore a breve termine.</span><span class="sxs-lookup"><span data-stu-id="b2cf4-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="b2cf4-108">Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="b2cf4-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="b2cf4-109">I valori validi per le liste di distribuzione `ms.author` sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b2cf4-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
