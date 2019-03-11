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
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Avviso

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft. Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata. Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.

I siti seguenti rientrano nell'ambito di questa convalida:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>Risoluzione

Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft. Di seguito è riportato un esempio.

Prima:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Dopo:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]