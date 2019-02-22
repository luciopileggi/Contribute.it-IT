---
title: deprecated-attribute
description: Spiegazione e risoluzione del problema di compilazione della documentazione deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322684"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Presto disponibile.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggerimento

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Usare `ms.service` per specificare i servizi cloud. Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`. Non usare `ms.component` perché è deprecato per questo contenuto.

## <a name="resolution"></a>Risoluzione

Verificare che il valore di `ms.service` sia corretto per l'articolo. Scegliere quindi un valore di `ms.subservice` valido.

I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
