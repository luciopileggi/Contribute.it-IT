---
title: hard-coded-locale
description: Spiegazione e risoluzione del problema di compilazione di Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310342"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="115d8-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="115d8-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="115d8-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="115d8-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="115d8-105">I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="115d8-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="115d8-106">Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata.</span><span class="sxs-lookup"><span data-stu-id="115d8-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="115d8-107">Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.</span><span class="sxs-lookup"><span data-stu-id="115d8-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="115d8-108">I siti seguenti rientrano nell'ambito di questa convalida:</span><span class="sxs-lookup"><span data-stu-id="115d8-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="115d8-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="115d8-109">azure.microsoft.com</span></span>
- <span data-ttu-id="115d8-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="115d8-110">docs.microsoft.com</span></span>
- <span data-ttu-id="115d8-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="115d8-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="115d8-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="115d8-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="115d8-113">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="115d8-113">Resolution</span></span>

<span data-ttu-id="115d8-114">Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="115d8-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="115d8-115">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="115d8-115">The following is an example.</span></span>

<span data-ttu-id="115d8-116">Prima:</span><span class="sxs-lookup"><span data-stu-id="115d8-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="115d8-117">Dopo:</span><span class="sxs-lookup"><span data-stu-id="115d8-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="115d8-118">L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="115d8-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="115d8-119">Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`.</span><span class="sxs-lookup"><span data-stu-id="115d8-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="115d8-120">Per eseguire lo script:</span><span class="sxs-lookup"><span data-stu-id="115d8-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="115d8-121">Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.</span><span class="sxs-lookup"><span data-stu-id="115d8-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="115d8-122">Premere ALT+M per aprire il menu Markdown.</span><span class="sxs-lookup"><span data-stu-id="115d8-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="115d8-123">Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).</span><span class="sxs-lookup"><span data-stu-id="115d8-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]