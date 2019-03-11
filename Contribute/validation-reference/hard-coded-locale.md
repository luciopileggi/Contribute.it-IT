---
title: hard-coded-locale
description: Spiegazione e risoluzione del problema di compilazione di Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427670"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="0f164-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="0f164-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="0f164-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="0f164-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="0f164-105">I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0f164-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="0f164-106">Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata.</span><span class="sxs-lookup"><span data-stu-id="0f164-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="0f164-107">Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.</span><span class="sxs-lookup"><span data-stu-id="0f164-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="0f164-108">I siti seguenti rientrano nell'ambito di questa convalida:</span><span class="sxs-lookup"><span data-stu-id="0f164-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="0f164-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0f164-109">azure.microsoft.com</span></span>
- <span data-ttu-id="0f164-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0f164-110">docs.microsoft.com</span></span>
- <span data-ttu-id="0f164-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0f164-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="0f164-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0f164-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="0f164-113">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="0f164-113">Resolution</span></span>

<span data-ttu-id="0f164-114">Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0f164-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="0f164-115">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="0f164-115">The following is an example.</span></span>

<span data-ttu-id="0f164-116">Prima:</span><span class="sxs-lookup"><span data-stu-id="0f164-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="0f164-117">Dopo:</span><span class="sxs-lookup"><span data-stu-id="0f164-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]