---
title: ms-date-invalid
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 46cd047253fc7fbfdf92b0c5a6d690e041262b02
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895433"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="939f3-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="939f3-103">ms-date-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="939f3-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="939f3-104">Warning</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY, no more than five days from today.`

## <a name="resolution"></a><span data-ttu-id="939f3-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="939f3-105">Resolution</span></span>

<span data-ttu-id="939f3-106">Verificare che l'articolo sia aggiornato e non includa contenuto danneggiato, quindi aggiungere una data valida nel formato MM/GG/AAAA:</span><span class="sxs-lookup"><span data-stu-id="939f3-106">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
