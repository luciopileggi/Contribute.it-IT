---
title: ms-date-too-late
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431485"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="6c5c9-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="6c5c9-103">ms-date-too-late</span></span>

<span data-ttu-id="6c5c9-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="6c5c9-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="6c5c9-105">Avviso</span><span class="sxs-lookup"><span data-stu-id="6c5c9-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="6c5c9-106">L'attributo `ms.date` viene usato per indicare un aggiornamento, ovvero l'ultima revisione dell'articolo per verificarne rilevanza, accuratezza, correttezza degli screenshot e funzionamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="6c5c9-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="6c5c9-107">L'attributo non può quindi essere una data futura.</span><span class="sxs-lookup"><span data-stu-id="6c5c9-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="6c5c9-108">È consentito un massimo di cinque giorni prima della data di rilascio, ad esempio quando il contenuto viene bloccato per il controllo di qualità in preparazione di un evento importante.</span><span class="sxs-lookup"><span data-stu-id="6c5c9-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="6c5c9-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="6c5c9-109">Resolution</span></span>

<span data-ttu-id="6c5c9-110">Specificare una `ms.date` fino a cinque giorni successiva a quella corrente, in formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="6c5c9-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
