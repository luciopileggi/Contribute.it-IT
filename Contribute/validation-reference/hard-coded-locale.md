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
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Avviso

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

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

> [!TIP]
> L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft. Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`. Per eseguire lo script:
>
> 1. Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.
> 1. Premere ALT+M per aprire il menu Markdown.
> 1. Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]