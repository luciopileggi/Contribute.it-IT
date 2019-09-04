---
title: multiple-values
description: Spiegazione e risoluzione del problema di compilazione della documentazione multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 515a8cd76cbd3d9bd117b1d0d59492f4a77bea4c
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236479"
---
# <a name="multiple-values"></a>multiple-values

## <a name="warning"></a>Avviso

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

È stato specificato più di un valore per un attributo per cui è consentito un solo valore.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Gli attributi per cui è consentito un solo valore devono essere specificati nel formato YML con valore singolo (scalare).

## <a name="resolution"></a>Risoluzione

Questo suggerimento viene visualizzato ogni volta che si usa una matrice multivalore per un attributo a valore singolo, sia con più valori che con un singolo valore nella matrice.

YML supporta i formati di matrice seguenti per gli attributi multivalore, come `ms.custom`:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Questi formati non sono validi per gli attributi a valore singolo, come `author`.

Se si specificano più valori, controllare quelli specificati e stabilire quale è corretto. Rimuovere gli altri valori e specificare il valore singolo nella stessa riga dell'attributo e senza parentesi quadre, come segue:

```yml
---
author: meganbradley
---
```

Nel caso di una matrice a valore singolo, modificarla nel formato scalare di cui sopra.

## <a name="attributes-in-scope"></a>Attributi nell'ambito

Gli attributi seguenti devono essere a valore singolo:

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
