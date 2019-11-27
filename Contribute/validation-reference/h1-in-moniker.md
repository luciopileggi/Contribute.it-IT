---
title: h1-in-moniker
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-in-moniker
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528817"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

## <a name="warning"></a>Avviso

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione. È possibile avere solo un H1 in ogni file. Le intestazioni H1 non sono consentite nelle sezioni del moniker, perché possono facilmente causare intestazioni H1 duplicate o mancanti a seconda della configurazione del controllo delle versioni.

Questo messaggio potrebbe essere visualizzato anche se una sezione del moniker contiene una riga di segni di uguale per ottenere una doppia sottolineatura, come questa: `=======`. Si tratta di una sintassi Markdown alternativa per un H1. Viene anche comunemente visualizzato nei conflitti di merge:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Risoluzione

Per risolvere il problema, rimuovere le intestazioni H1 da tutte le sezioni del moniker e assicurarsi che l'intestazione H1 all'inizio dell'articolo sia appropriata per tutte le sezioni del moniker. Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.

Se un'intestazione H1 in una sezione del moniker è effettivamente una doppia sottolineatura (`=======`), rimuoverla o sostituirla con un'intestazione hashtag, ad esempio `##`, in base alle esigenze. Se la doppia sottolineatura fa parte di un conflitto di merge, assicurarsi di rimuovere anche gli indicatori di inizio e fine del conflitto di merge e il testo obsoleto.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
