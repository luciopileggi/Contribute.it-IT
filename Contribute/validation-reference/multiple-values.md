---
title: multiple-values
description: Spiegazione e risoluzione del problema di compilazione della documentazione multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465117"
---
# <a name="multiple-values"></a><span data-ttu-id="aa7ca-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="aa7ca-103">multiple-values</span></span>

<span data-ttu-id="aa7ca-104">**Presto disponibile.**</span><span class="sxs-lookup"><span data-stu-id="aa7ca-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="aa7ca-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="aa7ca-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="aa7ca-106">È stato specificato più di un valore per un attributo per cui è consentito un solo valore.</span><span class="sxs-lookup"><span data-stu-id="aa7ca-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="aa7ca-107">Gli attributi per cui è consentito un solo valore devono essere specificati nel formato YML con valore singolo (scalare).</span><span class="sxs-lookup"><span data-stu-id="aa7ca-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="aa7ca-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="aa7ca-108">Resolution</span></span>

<span data-ttu-id="aa7ca-109">Questo suggerimento viene visualizzato ogni volta che si usa una matrice multivalore per un attributo a valore singolo, sia con più valori che con un singolo valore nella matrice.</span><span class="sxs-lookup"><span data-stu-id="aa7ca-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="aa7ca-110">YML supporta i formati di matrice seguenti per gli attributi multivalore, come `ms.custom`:</span><span class="sxs-lookup"><span data-stu-id="aa7ca-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="aa7ca-111">Questi formati non sono validi per gli attributi a valore singolo, come `author`.</span><span class="sxs-lookup"><span data-stu-id="aa7ca-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="aa7ca-112">Se si specificano più valori, controllare quelli specificati e stabilire quale è corretto.</span><span class="sxs-lookup"><span data-stu-id="aa7ca-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="aa7ca-113">Rimuovere gli altri valori e specificare il valore singolo nella stessa riga dell'attributo e senza parentesi quadre, come segue:</span><span class="sxs-lookup"><span data-stu-id="aa7ca-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="aa7ca-114">Nel caso di una matrice a valore singolo, modificarla nel formato scalare di cui sopra.</span><span class="sxs-lookup"><span data-stu-id="aa7ca-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
