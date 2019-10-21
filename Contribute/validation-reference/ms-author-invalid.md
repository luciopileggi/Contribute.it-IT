---
title: ms-author-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246303"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Avviso

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Risoluzione

Aggiornare il valore `ms.author` con l'alias Microsoft valido dell'autore corrente. È consigliabile che l'autore designato sia un dipendente a tempo pieno o una lista di distribuzione di team, anziché un fornitore a breve termine. Se l'alias è una lista di distribuzione, deve essere anche nell'elenco degli indirizzi consentiti `ms.author`.

I valori validi per le liste di distribuzione `ms.author` sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
