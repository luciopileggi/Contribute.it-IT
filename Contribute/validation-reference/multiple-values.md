---
title: multiple-values
description: Spiegazione e risoluzione del problema di compilazione della documentazione multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899660"
---
# <a name="multiple-values"></a><span data-ttu-id="4bda3-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="4bda3-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4bda3-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="4bda3-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="4bda3-105">È stato specificato più di un valore per un attributo per cui è consentito un solo valore.</span><span class="sxs-lookup"><span data-stu-id="4bda3-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="4bda3-106">Gli attributi per cui è consentito un solo valore devono essere specificati nel formato YML con valore singolo (scalare).</span><span class="sxs-lookup"><span data-stu-id="4bda3-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="4bda3-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="4bda3-107">Resolution</span></span>

<span data-ttu-id="4bda3-108">Questo suggerimento viene visualizzato ogni volta che si usa una matrice multivalore per un attributo a valore singolo, sia con più valori che con un singolo valore nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4bda3-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="4bda3-109">YML supporta i formati di matrice seguenti per gli attributi multivalore, come `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="4bda3-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="4bda3-110">Questi formati non sono validi per gli attributi a valore singolo, come `author`.</span><span class="sxs-lookup"><span data-stu-id="4bda3-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="4bda3-111">Se si specificano più valori, controllare quelli specificati e stabilire quale è corretto.</span><span class="sxs-lookup"><span data-stu-id="4bda3-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="4bda3-112">Rimuovere gli altri valori e specificare il valore singolo nella stessa riga dell'attributo e senza parentesi quadre, come segue:</span><span class="sxs-lookup"><span data-stu-id="4bda3-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="4bda3-113">Nel caso di una matrice a valore singolo, modificarla nel formato scalare di cui sopra.</span><span class="sxs-lookup"><span data-stu-id="4bda3-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="4bda3-114">Attributi nell'ambito</span><span class="sxs-lookup"><span data-stu-id="4bda3-114">Attributes in scope</span></span>

<span data-ttu-id="4bda3-115">Gli attributi seguenti devono essere a valore singolo:</span><span class="sxs-lookup"><span data-stu-id="4bda3-115">The following attributes are required to be single-valued:</span></span>

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
