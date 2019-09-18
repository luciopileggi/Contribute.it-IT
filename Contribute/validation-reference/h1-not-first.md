---
title: h1-not-first
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895463"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Markdown content is not allowed before H1.`

Solo l'intestazione dei metadati YAML può venire prima di H1 in un file Markdown. Ad esempio, se si vuole aggiungere una nota o un'immagine all'inizio dell'articolo, deve essere successiva a H1. Questa disposizione non è consentita:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Usare invece:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Un'altra causa comune di questo problema è la presenza di [byte order mark (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) prima dell'intestazione YAML, introdotti a volta da problemi di codifica durante il commit del contenuto nei repository. Questi BOM causano problemi di rendering in GitHub e devono essere rimossi.

## <a name="resolution"></a>Risoluzione

Rimuovere eventuale contenuto diverso dall'intestazione dei metadati YAML prima di H1.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
