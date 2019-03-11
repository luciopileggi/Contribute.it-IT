---
title: xref-not-found
description: Spiegazione e risoluzione del problema di compilazione di Docs xref-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427872"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>Avviso

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

L'UID collegato non esiste o non è disponibile nel repository.

## <a name="resolution"></a>Risoluzione

Verificare che l'UID sia corretto e che Xref Service sia configurato correttamente nel repository, come descritto nella documentazione interna Microsoft di [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
