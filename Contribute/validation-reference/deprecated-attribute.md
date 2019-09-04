---
title: deprecated-attribute
description: Spiegazione e risoluzione del problema di compilazione della documentazione deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236223"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

## <a name="warning"></a>Avviso

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Usare `ms.service` per specificare i servizi cloud. Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`. Non usare `ms.component` perché è deprecato per questo contenuto.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.service` sia corretto per l'articolo. Scegliere quindi un valore di `ms.subservice` valido.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
