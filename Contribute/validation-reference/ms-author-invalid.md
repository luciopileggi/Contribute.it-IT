---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636725"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Risoluzione

Verificare che il valore `ms.author` sia un alias Microsoft valido. Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti.

I valori validi per le liste di distribuzione sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
