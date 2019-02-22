---
title: ms-date-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: e960bc2d8e9013e480f2bb391cdfa0c1da043b8b
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431508"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="61da8-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="61da8-103">ms-date-invalid</span></span>

<span data-ttu-id="61da8-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="61da8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="61da8-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="61da8-105">Suggestion</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="61da8-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="61da8-106">Resolution</span></span>

<span data-ttu-id="61da8-107">Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="61da8-107">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
