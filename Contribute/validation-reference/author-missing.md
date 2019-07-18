---
title: author-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791534"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Missing attribute: author. Add the current author's GitHub ID.`

L'attributo `author` identifica l'autore dell'articolo tramite l'ID di GitHub. 

## <a name="resolution"></a>Risoluzione

Aggiungere l'ID GitHub dell'autore corrente all'intestazione YML:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Si noti che è necessario aggiungere il proprietario *corrente* dell'articolo, non l'autore originale se è stata modificata la proprietà.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
