---
title: h1-missing
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459120"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Avviso

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
> Questa regola non si applica ai file inclusi. Se vengono visualizzati avvisi H1 nei file inclusi, probabilmente è necessario spostare i file inclusi in una cartella `includes`. La cartella `includes` può essere in qualsiasi livello nel percorso del file. In base al percorso, la compilazione di Docs riconoscerà il file come file incluso e le convalide H1 non verranno eseguite.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]