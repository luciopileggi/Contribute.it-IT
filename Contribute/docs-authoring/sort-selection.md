---
title: Ordinamento della selezione - Docs Authoring Pack
description: Informazioni su come usare la funzionalità Ordinamento della selezione di Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336751"
---
# <a name="sort-selection"></a><span data-ttu-id="8f397-103">Ordinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="8f397-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="8f397-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="8f397-104">Summary</span></span>

<span data-ttu-id="8f397-105">In un file Markdown ( *\*.md*), dopo aver apportato una selezione, sono ora disponibili due voci di menu di scelta rapida per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8f397-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="8f397-106">Fare clic con il pulsante destro del mouse sul testo selezionato per aprire il meno di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8f397-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="8f397-107">Vengono visualizzate due voci di menu simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f397-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Menu di scelta rapida per la selezione dell'ordinamento":::

> [!TIP]
> <span data-ttu-id="8f397-109">Le voci di menu di scelta rapida per l'ordinamento rimangono nascoste fino a quando nell'editor di testo Visual Studio Code non viene inserita una selezione valida.</span><span class="sxs-lookup"><span data-stu-id="8f397-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="8f397-110">Ordinamento crescente della selezione (dalla A alla Z)</span><span class="sxs-lookup"><span data-stu-id="8f397-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="8f397-111">Se si seleziona l'opzione **Ordinamento crescente della selezione (dalla A alla Z)** l'intera selezione viene ordinata in modo alfabetico crescente, dalla A alla Z.</span><span class="sxs-lookup"><span data-stu-id="8f397-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="8f397-112">Ordinamento decrescente della selezione (dalla Z alla A)</span><span class="sxs-lookup"><span data-stu-id="8f397-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="8f397-113">Se si seleziona l'opzione **Ordinamento decrescente della selezione (dalla A alla Z)** l'intera selezione viene ordinata in modo alfabetico decrescente, dalla Z alla A.</span><span class="sxs-lookup"><span data-stu-id="8f397-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="8f397-114">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="8f397-114">Considerations</span></span>

<span data-ttu-id="8f397-115">Il meccanismo di ordinamento sottostante usa un *ordinamento* basato sul linguaggio naturale,</span><span class="sxs-lookup"><span data-stu-id="8f397-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="8f397-116">più efficiente e completo rispetto all'ordinamento standard.</span><span class="sxs-lookup"><span data-stu-id="8f397-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="8f397-117">Osservare la tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="8f397-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="8f397-118">Se questo meccanismo non usasse l'ordinamento basato sul linguaggio naturale, l'ordine di `Column1` sarebbe 1, 11, 2 e così via; capisce invece che 11 è maggiore di 2, ottenendo l'ordine crescente seguente:</span><span class="sxs-lookup"><span data-stu-id="8f397-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="8f397-119">In azione</span><span class="sxs-lookup"><span data-stu-id="8f397-119">In action</span></span>

<span data-ttu-id="8f397-120">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8f397-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="8f397-121">[![Dimostrazione dell'ordinamento della selezione](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8f397-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
