---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637392"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="67d75-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="67d75-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="67d75-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="67d75-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="67d75-105">L'attributo `ms.date` viene usato per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="67d75-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="67d75-106">L'attributo non può quindi essere una data futura.</span><span class="sxs-lookup"><span data-stu-id="67d75-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="67d75-107">È consentito un massimo di cinque giorni prima della data di rilascio, ad esempio quando il contenuto viene bloccato per il controllo di qualità in preparazione di un evento importante.</span><span class="sxs-lookup"><span data-stu-id="67d75-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="67d75-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="67d75-108">Resolution</span></span>

<span data-ttu-id="67d75-109">Specificare una `ms.date` fino a cinque giorni successiva a quella corrente, in formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="67d75-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
