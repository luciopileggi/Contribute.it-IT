---
title: insecure-link
description: Spiegazione e risoluzione del problema di compilazione di Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528856"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Questa regola è stata inizialmente abilitata come "suggerimento" in modo che i team dei contenuti abbiano il tempo di valutare l'impatto e di sviluppare un piano per pulire i repository. **Verrà promossa ad "Avviso" in data 20/12/2019**.

## <a name="suggestion"></a>Suggerimento

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Questo messaggio indica che è stato usato un collegamento Markdown esplicito con `http` o è stato usato un URL non elaborato, ad esempio `www.microsoft.com`. Gli URL non elaborati vengono convertiti in collegamenti non sicuri durante la pubblicazione in Docs e non devono essere usati.

## <a name="resolution"></a>Risoluzione

Modificare tutti gli URL di siti Microsoft in modo da usare `https` anziché `http`.

Se il collegamento è un URL non elaborato, modificarlo in un collegamento Markdown esplicito che inizia con `https`, ad esempio:

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> L'estensione Docs Markdown per VS Code include uno script di pulizia per i collegamenti Microsoft. Lo script controlla tutti i collegamenti ai siti Microsoft in un repository per assicurarsi che inizino con `https` anziché `http` e non contengano il codice delle impostazioni locali, ad esempio `en-us`. Per eseguire lo script:
>
> 1. Installare l'estensione [Docs Markdown ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) per VS Code.
> 1. Premere ALT+M per aprire il menu Markdown.
> 1. Selezionare **Cleanup** (Pulizia) e quindi **Microsoft links** (Collegamenti Microsoft).

In alcuni casi, potrebbe essere necessario documentare gli indirizzi Web, ad esempio i nomi di dominio completi, che non sono destinati a essere collegamenti selezionabili tramite clic. È necessario applicare lo stile di codice inline, ad esempio:

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
