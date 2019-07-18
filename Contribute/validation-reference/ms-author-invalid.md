---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791542"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="8f29c-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="8f29c-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8f29c-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="8f29c-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="8f29c-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="8f29c-105">Resolution</span></span>

<span data-ttu-id="8f29c-106">Verificare che il valore `ms.author` sia l'alias Microsoft valido dell'autore corrente.</span><span class="sxs-lookup"><span data-stu-id="8f29c-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="8f29c-107">Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti.</span><span class="sxs-lookup"><span data-stu-id="8f29c-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="8f29c-108">I valori validi per le liste di distribuzione sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8f29c-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
