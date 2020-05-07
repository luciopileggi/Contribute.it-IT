---
title: Aggiornamenti dei metadati - Docs Authoring Pack
description: Informazioni su come eseguire l'aggiornamento dei metadati con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336636"
---
# <a name="update-metadata"></a><span data-ttu-id="fe841-103">Aggiornare i metadati</span><span class="sxs-lookup"><span data-stu-id="fe841-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="fe841-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="fe841-104">Summary</span></span>

<span data-ttu-id="fe841-105">In un file Markdown (*\*.md*) sono disponibili due voci di menu contestuali dedicate ai metadati.</span><span class="sxs-lookup"><span data-stu-id="fe841-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="fe841-106">Quando si fa clic con il pulsante destro del mouse in un punto qualsiasi dell'editor di testo, vengono visualizzate due voci di menu simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe841-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Aggiornare il menu di scelta rapida dei metadati":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="fe841-108">Aggiornare il valore di metadati `ms.date`</span><span class="sxs-lookup"><span data-stu-id="fe841-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="fe841-109">Se si seleziona l'opzione **Update `ms.date` Metadata Value** (Aggiorna il valore di metadati `ms.date`), il valore `ms.date` dei file Markdown correnti viene impostato sulla data odierna.</span><span class="sxs-lookup"><span data-stu-id="fe841-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="fe841-110">Se nel documento non è presente un campo di metadati `ms.date`, non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="fe841-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="fe841-111">Aggiornare i valori dei metadati impliciti</span><span class="sxs-lookup"><span data-stu-id="fe841-111">Update implicit metadata values</span></span>

<span data-ttu-id="fe841-112">Se si seleziona l'opzione **Update implicit metadata values** (Aggiorna i valori dei metadati impliciti), vengono trovati e sostituiti tutti i valori di metadati che potrebbero essere stati specificati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="fe841-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="fe841-113">I valori dei metadati vengono specificati in modo implicito nel file *docfx.json*, contenuto nel nodo `build/fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="fe841-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="fe841-114">Ogni coppia chiave-valore del nodo `fileMetadata` rappresenta le impostazioni predefinite dei metadati.</span><span class="sxs-lookup"><span data-stu-id="fe841-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="fe841-115">Un file Markdown nella directory di *primo livello/sottocartella* che omette il valore di metadati `ms.author` potrebbe specificare in modo implicito un valore predefinito da usare nel nodo `fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="fe841-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="fe841-116">In questo caso, tutti i file Markdown accetterebbero in modo implicito il valore di metadati `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="fe841-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="fe841-117">Questa funzionalità interessa quindi le impostazioni implicite rilevate nel file *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="fe841-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="fe841-118">Se un file Markdown contiene metadati con valori impostati in modo esplicito su valori diversi da quelli impliciti, questi valori vengono sostituiti.</span><span class="sxs-lookup"><span data-stu-id="fe841-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="fe841-119">Si considerino, ad esempio, i seguenti metadati del file Markdown, che si trova in **top-level/sub-folder/includes/example.md**:</span><span class="sxs-lookup"><span data-stu-id="fe841-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="fe841-120">Se in questo file venisse eseguita l'opzione **Update implicit metadata values** (Aggiorna i valori dei metadati impliciti), supponendo che contenga il file *docfx.json* sopra specificato, il valore di metadati verrebbe aggiornato su `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="fe841-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="fe841-121">In azione</span><span class="sxs-lookup"><span data-stu-id="fe841-121">In action</span></span>

<span data-ttu-id="fe841-122">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fe841-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="fe841-123">[![Dimostrazione dell'aggiornamento dei metadati](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="fe841-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
