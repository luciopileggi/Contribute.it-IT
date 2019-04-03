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
# <a name="locale-specific-links"></a>Collegamenti delle impostazioni locali

I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft. Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata. Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.

Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft. Di seguito è riportato un esempio.

Prima:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Dopo:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

I siti seguenti rientrano nell'ambito di questa convalida:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com