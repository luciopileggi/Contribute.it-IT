---
title: ms-author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246243"
---
# <a name="ms-author-missing"></a><span data-ttu-id="96d22-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="96d22-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="96d22-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="96d22-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="96d22-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="96d22-105">Resolution</span></span>

<span data-ttu-id="96d22-106">Aggiungere l'alias Microsoft dell'autore corrente per `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="96d22-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="96d22-107">Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="96d22-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="96d22-108">È consigliabile che l'autore designato sia un dipendente a tempo pieno o una lista di distribuzione di team, anziché un fornitore a breve termine.</span><span class="sxs-lookup"><span data-stu-id="96d22-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="96d22-109">Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="96d22-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="96d22-110">I valori validi per le liste di distribuzione `ms.author` sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="96d22-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
