---
title: hard-coded-locale
description: Spiegazione e risoluzione del problema di compilazione di Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166818"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="227dd-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="227dd-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="227dd-104">Questa regola è stata inizialmente abilitata come "suggerimento" in modo che i team dei contenuti abbiano il tempo di valutare l'impatto e di sviluppare un piano per pulire i repository.</span><span class="sxs-lookup"><span data-stu-id="227dd-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="227dd-105">**Verrà promossa ad "Avviso" in data 20/12/2019**.</span><span class="sxs-lookup"><span data-stu-id="227dd-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="227dd-106">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="227dd-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="227dd-107">I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="227dd-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="227dd-108">Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata.</span><span class="sxs-lookup"><span data-stu-id="227dd-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="227dd-109">Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.</span><span class="sxs-lookup"><span data-stu-id="227dd-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="227dd-110">I siti seguenti rientrano nell'ambito di questa convalida:</span><span class="sxs-lookup"><span data-stu-id="227dd-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="227dd-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="227dd-111">azure.microsoft.com</span></span>
- <span data-ttu-id="227dd-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="227dd-112">docs.microsoft.com</span></span>
- <span data-ttu-id="227dd-113">msdn.microsoft.com (escluso social.msdn.com, che necessita di impostazioni locali per garantire il collegamento del forum corretto)</span><span class="sxs-lookup"><span data-stu-id="227dd-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="227dd-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="227dd-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="227dd-115">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="227dd-115">Resolution</span></span>

<span data-ttu-id="227dd-116">Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="227dd-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="227dd-117">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="227dd-117">The following is an example.</span></span>

<span data-ttu-id="227dd-118">Prima:</span><span class="sxs-lookup"><span data-stu-id="227dd-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="227dd-119">Dopo:</span><span class="sxs-lookup"><span data-stu-id="227dd-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="227dd-120">L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="227dd-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="227dd-121">Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`.</span><span class="sxs-lookup"><span data-stu-id="227dd-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="227dd-122">Per eseguire lo script:</span><span class="sxs-lookup"><span data-stu-id="227dd-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="227dd-123">Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.</span><span class="sxs-lookup"><span data-stu-id="227dd-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="227dd-124">Premere ALT+M per aprire il menu Markdown.</span><span class="sxs-lookup"><span data-stu-id="227dd-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="227dd-125">Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).</span><span class="sxs-lookup"><span data-stu-id="227dd-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
