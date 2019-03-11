---
title: circular-reference
description: Spiegazione e risoluzione del problema di compilazione di Docs circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459212"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Errore

`Files '{file name 1}' and '{file name 2}' reference each other.`

Ad esempio, potrebbe trattarsi di un file incluso che si collega al file corrente o un collegamento a un file che è stato reindirizzato al file corrente.

## <a name="resolution"></a>Risoluzione

Esaminare i collegamenti nei file e apportare le modifiche necessarie in modo che nessun file si colleghi a se stesso o si includa.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
