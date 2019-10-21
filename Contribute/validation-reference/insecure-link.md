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
# <a name="insecure-link"></a>insecure-link

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Questo messaggio indica che è stato usato un collegamento Markdown esplicito con `http` o è stato usato un URL non elaborato, ad esempio `www.microsoft.com`. Gli URL non elaborati vengono convertiti in collegamenti non sicuri durante la pubblicazione in Docs e non devono essere usati.

## <a name="resolution"></a>Risoluzione

Modificare tutti gli URL di siti Microsoft in modo da usare `https` anziché `http`.

Se il collegamento è un URL non elaborato, modificarlo in un collegamento Markdown esplicito che inizia con `https`.

> [!TIP]
> L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft. Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`. Per eseguire lo script:
>
> 1. Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.
> 1. Premere ALT+M per aprire il menu Markdown.
> 1. Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
