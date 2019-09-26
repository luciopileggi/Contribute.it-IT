---
title: h1-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247404"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi. Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.

## <a name="resolution"></a>Risoluzione

Per risolvere questo problema, aggiungere un H1 come primo contenuto dopo il blocco metadati YML nel file:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Questa regola non si applica ai file inclusi. Se vengono visualizzati risultati H1 nei file inclusi, probabilmente è necessario spostare i file inclusi in una cartella `includes`. La cartella `includes` può essere in qualsiasi livello nel percorso del file. In base al percorso, la compilazione di Docs riconoscerà il file come file incluso e le convalide H1 non verranno eseguite.
>
> Una delle cause comuni di H1 mancanti nei file padre è l'utilizzo improprio dei file inclusi: l'H1 si trova nel file incluso, non nel file padre. Questa operazione non è consentita perché l'utilizzo di un H1 in un file incluso indica che ci sono H1 duplicati nei file padre oppure che il file incluso viene usato una sola volta. Gli H1 devono essere univoci all'interno di un set di contenuto e i file inclusi devono essere usati solo per condividere contenuto tra più file. Se vengono visualizzati risultati `h1-missing` perché l'H1 si trova in un file incluso, la soluzione consiste nello spostare l'H1 e tutto il contenuto incluso se il file incluso viene usato solo una volta nel file padre. Per altre informazioni sui file inclusi in Docs, vedere l'articolo interno Microsoft [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master) (Includere contenuto riutilizzabile negli articoli).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
