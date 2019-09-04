---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236274"
---
# <a name="author-missing"></a><span data-ttu-id="fb3e7-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="fb3e7-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="fb3e7-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="fb3e7-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="fb3e7-105">L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub.</span><span class="sxs-lookup"><span data-stu-id="fb3e7-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="fb3e7-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="fb3e7-106">Resolution</span></span>

<span data-ttu-id="fb3e7-107">Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:</span><span class="sxs-lookup"><span data-stu-id="fb3e7-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="fb3e7-108">Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb3e7-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
