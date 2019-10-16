---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288509"
---
# <a name="author-missing"></a><span data-ttu-id="d2c35-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="d2c35-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="d2c35-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="d2c35-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="d2c35-105">L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub.</span><span class="sxs-lookup"><span data-stu-id="d2c35-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="d2c35-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="d2c35-106">Resolution</span></span>

<span data-ttu-id="d2c35-107">Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:</span><span class="sxs-lookup"><span data-stu-id="d2c35-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="d2c35-108">Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2c35-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
