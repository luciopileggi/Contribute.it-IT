---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713040"
---
# <a name="author-missing"></a>author-missing

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: author. Add a valid GitHub ID.`

L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub. 

## <a name="resolution"></a>Risoluzione

Aggiungere l'ID GitHub dell'autore all'intestazione YML:

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]