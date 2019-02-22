---
title: deprecated-attribute
description: Spiegazione e risoluzione del problema di compilazione della documentazione deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322684"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="2374c-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="2374c-103">deprecated-attribute</span></span>

<span data-ttu-id="2374c-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="2374c-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2374c-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="2374c-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="2374c-106">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="2374c-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="2374c-107">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="2374c-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="2374c-108">Non usare `ms.component` perché è deprecato per questo contenuto.</span><span class="sxs-lookup"><span data-stu-id="2374c-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="2374c-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="2374c-109">Resolution</span></span>

<span data-ttu-id="2374c-110">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="2374c-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="2374c-111">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="2374c-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="2374c-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="2374c-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
