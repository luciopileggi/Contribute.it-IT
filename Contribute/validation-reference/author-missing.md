---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848569"
---
# <a name="author-missing"></a><span data-ttu-id="da244-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="da244-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="da244-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="da244-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="da244-105">L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub.</span><span class="sxs-lookup"><span data-stu-id="da244-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="da244-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="da244-106">Resolution</span></span>

<span data-ttu-id="da244-107">Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:</span><span class="sxs-lookup"><span data-stu-id="da244-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="da244-108">Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="da244-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
