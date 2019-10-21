---
title: multiple-h1
description: Spiegazione e risoluzione del problema di compilazione di Docs multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246283"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione. È possibile avere solo un H1 in ogni file.

Questo messaggio potrebbe essere visualizzato anche se l'articolo contiene una riga di segni di uguale per ottenere una doppia sottolineatura, come questa: `=======`. Si tratta di una sintassi Markdown alternativa per un H1. Viene anche comunemente visualizzato nei conflitti di merge:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Risoluzione

Per risolvere questo problema, modificare il livello di intestazione di H1 successivi in H2 (`##`), o in caso contrario, riorganizzare il file. Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

Se un'intestazione H1 aggiuntiva è effettivamente una doppia sottolineatura (`=======`), rimuoverla o sostituirla con un'intestazione hashtag, ad esempio `##`, in base alle esigenze. Se la doppia sottolineatura fa parte di un conflitto di merge, assicurarsi di rimuovere anche gli indicatori di inizio e fine del conflitto di merge e il testo obsoleto.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
