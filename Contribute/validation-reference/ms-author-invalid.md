---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987768"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="b1c5e-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="b1c5e-103">ms-author-invalid</span></span>

<span data-ttu-id="b1c5e-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="b1c5e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b1c5e-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="b1c5e-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="b1c5e-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b1c5e-106">Resolution</span></span>

<span data-ttu-id="b1c5e-107">Verificare che il valore `ms.author` sia un alias Microsoft valido.</span><span class="sxs-lookup"><span data-stu-id="b1c5e-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="b1c5e-108">Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti.</span><span class="sxs-lookup"><span data-stu-id="b1c5e-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="b1c5e-109">I valori validi per le liste di distribuzione sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b1c5e-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
