---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791534"
---
# <a name="author-missing"></a><span data-ttu-id="f729b-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="f729b-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f729b-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="f729b-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="f729b-105">L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub.</span><span class="sxs-lookup"><span data-stu-id="f729b-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="f729b-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="f729b-106">Resolution</span></span>

<span data-ttu-id="f729b-107">Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:</span><span class="sxs-lookup"><span data-stu-id="f729b-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="f729b-108">Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="f729b-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
