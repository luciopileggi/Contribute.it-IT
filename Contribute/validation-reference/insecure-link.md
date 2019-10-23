---
title: insecure-link
description: Spiegazione e risoluzione del problema di compilazione di Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587687"
---
# <a name="insecure-link"></a><span data-ttu-id="1bcb0-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="1bcb0-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bcb0-104">Questa regola è stata inizialmente abilitata come "suggerimento" in modo che i team dei contenuti abbiano il tempo di valutare l'impatto e di sviluppare un piano per pulire i repository.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="1bcb0-105">**Verrà promossa ad "Avviso" in data 20/12/2019**.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="1bcb0-106">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="1bcb0-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="1bcb0-107">Questo messaggio indica che è stato usato un collegamento Markdown esplicito con `http` o è stato usato un URL non elaborato, ad esempio `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="1bcb0-108">Gli URL non elaborati vengono convertiti in collegamenti non sicuri durante la pubblicazione in Docs e non devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="1bcb0-109">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="1bcb0-109">Resolution</span></span>

<span data-ttu-id="1bcb0-110">Modificare tutti gli URL di siti Microsoft in modo da usare `https` anziché `http`.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="1bcb0-111">Se il collegamento è un URL non elaborato, modificarlo in un collegamento Markdown esplicito che inizia con `https`.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="1bcb0-112">L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="1bcb0-113">Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="1bcb0-114">Per eseguire lo script:</span><span class="sxs-lookup"><span data-stu-id="1bcb0-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="1bcb0-115">Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="1bcb0-116">Premere ALT+M per aprire il menu Markdown.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="1bcb0-117">Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).</span><span class="sxs-lookup"><span data-stu-id="1bcb0-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
