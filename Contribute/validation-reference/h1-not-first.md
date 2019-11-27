---
title: h1-not-first
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528921"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>Avviso

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
