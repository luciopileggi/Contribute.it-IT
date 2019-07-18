---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791542"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Risoluzione

Verificare che il valore `ms.author` sia l'alias Microsoft valido dell'autore corrente. Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti.

I valori validi per le liste di distribuzione sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
