---
title: ms-prod-service-mismatch
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636794"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Usare `ms.prod` per specificare i prodotti locali e `ms.service` per i servizi cloud. Per specificare informazioni più dettagliate su `ms.prod`, è facoltativamente possibile specificare `ms.technology`. Per specificare informazioni più dettagliate su `ms.service`, è possibile specificare `ms.subservice`. Non è possibile usare `ms.prod` con `ms.subservice` o `ms.service` con `ms.technology`.

## <a name="resolution"></a>Risoluzione

Verificare prima di tutto di aver selezionato l'attributo padre corretto (`ms.prod` o `ms.service`) per l'articolo. Aggiungere quindi il campo figlio appropriato con un valore abbinato valido. Rimuovere eventuali campi aggiuntivi.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
