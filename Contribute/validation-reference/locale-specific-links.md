---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Collegamenti delle impostazioni locali
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841244"
---
# <a name="locale-specific-links"></a><span data-ttu-id="0138a-102">Collegamenti delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="0138a-102">Locale-specific links</span></span>

<span data-ttu-id="0138a-103">I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0138a-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="0138a-104">Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata.</span><span class="sxs-lookup"><span data-stu-id="0138a-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="0138a-105">Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.</span><span class="sxs-lookup"><span data-stu-id="0138a-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="0138a-106">Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0138a-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="0138a-107">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="0138a-107">The following is an example.</span></span>

<span data-ttu-id="0138a-108">Prima:</span><span class="sxs-lookup"><span data-stu-id="0138a-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="0138a-109">Dopo:</span><span class="sxs-lookup"><span data-stu-id="0138a-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="0138a-110">I siti seguenti rientrano nell'ambito di questa convalida:</span><span class="sxs-lookup"><span data-stu-id="0138a-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="0138a-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0138a-111">azure.microsoft.com</span></span>
- <span data-ttu-id="0138a-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0138a-112">docs.microsoft.com</span></span>
- <span data-ttu-id="0138a-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0138a-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="0138a-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0138a-114">technet.microsoft.com</span></span>