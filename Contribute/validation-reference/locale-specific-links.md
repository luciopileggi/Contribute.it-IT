---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653552"
---
# <a name="locale-specific-links"></a><span data-ttu-id="7cc52-101">Collegamenti delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="7cc52-101">Locale-specific links</span></span>

<span data-ttu-id="7cc52-102">I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7cc52-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="7cc52-103">Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata.</span><span class="sxs-lookup"><span data-stu-id="7cc52-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="7cc52-104">Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.</span><span class="sxs-lookup"><span data-stu-id="7cc52-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="7cc52-105">Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7cc52-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="7cc52-106">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="7cc52-106">The following is an example.</span></span>

<span data-ttu-id="7cc52-107">Prima:</span><span class="sxs-lookup"><span data-stu-id="7cc52-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="7cc52-108">Dopo:</span><span class="sxs-lookup"><span data-stu-id="7cc52-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="7cc52-109">I siti seguenti rientrano nell'ambito di questa convalida:</span><span class="sxs-lookup"><span data-stu-id="7cc52-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="7cc52-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7cc52-110">azure.microsoft.com</span></span>
- <span data-ttu-id="7cc52-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7cc52-111">docs.microsoft.com</span></span>
- <span data-ttu-id="7cc52-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7cc52-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="7cc52-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7cc52-113">technet.microsoft.com</span></span>