---
title: ms-component-deprecated
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-component-deprecated
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713155"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="6215d-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="6215d-103">ms-component-deprecated</span></span>

<span data-ttu-id="6215d-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="6215d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6215d-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="6215d-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="6215d-106">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="6215d-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="6215d-107">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="6215d-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="6215d-108">Non usare `ms.component` perché è deprecato per questo contenuto.</span><span class="sxs-lookup"><span data-stu-id="6215d-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="6215d-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="6215d-109">Resolution</span></span>

<span data-ttu-id="6215d-110">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="6215d-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="6215d-111">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="6215d-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="6215d-112">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="6215d-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
