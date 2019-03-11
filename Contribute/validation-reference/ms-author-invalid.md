---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427850"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a>Risoluzione

Verificare che il valore `ms.author` sia un alias Microsoft valido. Se l'alias è una lista di distribuzione, deve essere ugualmente consentito.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
