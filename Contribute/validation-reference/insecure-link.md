---
title: insecure-link
description: Spiegazione e risoluzione del problema di compilazione di Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379522"
---
# <a name="insecure-link"></a><span data-ttu-id="68e06-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="68e06-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="68e06-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="68e06-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="68e06-105">Questo messaggio indica che è stato usato un collegamento Markdown esplicito con `http` o è stato usato un URL non elaborato, ad esempio `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="68e06-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="68e06-106">Gli URL non elaborati vengono convertiti in collegamenti non sicuri durante la pubblicazione in Docs e non devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="68e06-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="68e06-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="68e06-107">Resolution</span></span>

<span data-ttu-id="68e06-108">Modificare tutti gli URL di siti Microsoft in modo da usare `https` anziché `http`.</span><span class="sxs-lookup"><span data-stu-id="68e06-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="68e06-109">Se il collegamento è un URL non elaborato, modificarlo in un collegamento Markdown esplicito che inizia con `https`.</span><span class="sxs-lookup"><span data-stu-id="68e06-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="68e06-110">L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68e06-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="68e06-111">Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`.</span><span class="sxs-lookup"><span data-stu-id="68e06-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="68e06-112">Per eseguire lo script:</span><span class="sxs-lookup"><span data-stu-id="68e06-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="68e06-113">Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.</span><span class="sxs-lookup"><span data-stu-id="68e06-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="68e06-114">Premere ALT+M per aprire il menu Markdown.</span><span class="sxs-lookup"><span data-stu-id="68e06-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="68e06-115">Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).</span><span class="sxs-lookup"><span data-stu-id="68e06-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
