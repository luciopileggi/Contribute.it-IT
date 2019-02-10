---
title: ms-component-deprecated
description: Spiegazione e risoluzione del problema di compilazione della documentazione ms-component-deprecated
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713155"
---
# <a name="ms-component-deprecated"></a>ms-component-deprecated

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
