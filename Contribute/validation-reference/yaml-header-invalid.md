---
title: yaml-header-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs ms-topic-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459028"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="a7701-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="a7701-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="a7701-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="a7701-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="a7701-105">Ciò significa in genere che un valore di metadati non racchiusi tra virgolette in un'intestazione YAML include una virgola o un altro carattere speciale.</span><span class="sxs-lookup"><span data-stu-id="a7701-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="a7701-106">Può anche significare che manca uno spazio dopo i due punti in una coppia chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="a7701-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7701-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="a7701-107">Resolution</span></span>

<span data-ttu-id="a7701-108">Esaminare l'intestazione YAML.</span><span class="sxs-lookup"><span data-stu-id="a7701-108">Review your YAML header.</span></span> <span data-ttu-id="a7701-109">Cercare gli errori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7701-109">Look for the following mistakes.</span></span>

<span data-ttu-id="a7701-110">Due punti in un valore non racchiuso tra virgolette:</span><span class="sxs-lookup"><span data-stu-id="a7701-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="a7701-111">Modificare in:</span><span class="sxs-lookup"><span data-stu-id="a7701-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="a7701-112">Nessuno spazio dopo i due punti nella coppia chiave/valore:</span><span class="sxs-lookup"><span data-stu-id="a7701-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="a7701-113">Modificare in:</span><span class="sxs-lookup"><span data-stu-id="a7701-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
