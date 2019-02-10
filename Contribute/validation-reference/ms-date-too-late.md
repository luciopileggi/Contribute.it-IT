---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713109"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="19932-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="19932-103">ms-date-too-late</span></span>

<span data-ttu-id="19932-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="19932-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="19932-105">Avviso</span><span class="sxs-lookup"><span data-stu-id="19932-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="19932-106">L'attributo `ms.date` viene usato per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="19932-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="19932-107">L'attributo non può quindi essere una data futura.</span><span class="sxs-lookup"><span data-stu-id="19932-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="19932-108">È consentito un massimo di cinque giorni prima della data di rilascio, ad esempio quando il contenuto viene bloccato per il controllo di qualità in preparazione di un evento importante.</span><span class="sxs-lookup"><span data-stu-id="19932-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="19932-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="19932-109">Resolution</span></span>

<span data-ttu-id="19932-110">Specificare una `ms.date` fino a cinque giorni successiva a quella corrente, in formato MM/GG/AAAA.</span><span class="sxs-lookup"><span data-stu-id="19932-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
