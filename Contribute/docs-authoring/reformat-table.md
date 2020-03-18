---
title: Riformattazione delle tabelle Markdown - Docs Authoring Pack
description: Informazioni su come usare le varie funzionalità di formattazione delle tabelle Markdown di Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336774"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="cad7c-103">Riformattazione delle tabelle Markdown</span><span class="sxs-lookup"><span data-stu-id="cad7c-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="cad7c-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cad7c-104">Summary</span></span>

<span data-ttu-id="cad7c-105">In un file Markdown ( *\*.md*), quando si seleziona una tabella completa, sono ora disponibili due voci di menu di scelta rapida per la formattazione della tabella.</span><span class="sxs-lookup"><span data-stu-id="cad7c-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="cad7c-106">Fare clic con il pulsante destro del mouse sulla tabella Markdown per aprire il meno di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="cad7c-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="cad7c-107">Vengono visualizzate due voci di menu simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="cad7c-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Menu di scelta rapida per la riformattazione della tabella":::

> [!TIP]
> <span data-ttu-id="cad7c-109">Questa funzionalità **non** può essere usata per più selezioni di tabelle, ma è progettata per una singola tabella Markdown.</span><span class="sxs-lookup"><span data-stu-id="cad7c-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="cad7c-110">Per ottenere i risultati desiderati, è necessario selezionare l'intera tabella, incluse le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="cad7c-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="cad7c-111">Consolidare la tabella selezionata</span><span class="sxs-lookup"><span data-stu-id="cad7c-111">Consolidate selected table</span></span>

<span data-ttu-id="cad7c-112">Se si seleziona l'opzione **Consolidate selected table** (Consolida tabella selezionata), le intestazioni e i contenuti delle tabelle vengono compressi lasciando un solo spazio su entrambi i lati di ogni valore.</span><span class="sxs-lookup"><span data-stu-id="cad7c-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="cad7c-113">Distribuire la tabella selezionata in modo uniforme</span><span class="sxs-lookup"><span data-stu-id="cad7c-113">Evenly distribute selected table</span></span>

<span data-ttu-id="cad7c-114">Se si seleziona l'opzione **Evenly distribute selected table** (Distribuisci in modo uniforme la tabella selezionata) viene calcolato il valore più lungo di ogni colonna e, in base ad esso, tutti gli altri valori vengono distribuiti in modo uniforme, con lo spazio.</span><span class="sxs-lookup"><span data-stu-id="cad7c-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="cad7c-115">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="cad7c-115">Considerations</span></span>

<span data-ttu-id="cad7c-116">Questa funzionalità non ha alcun effetto sul rendering della tabella, ma ne migliora la leggibilità, rendendola anche più gestibile.</span><span class="sxs-lookup"><span data-stu-id="cad7c-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="cad7c-117">La funzionalità di riformattazione della tabella mantiene intatto l'allineamento delle colonne.</span><span class="sxs-lookup"><span data-stu-id="cad7c-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="cad7c-118">Osservare la tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="cad7c-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="cad7c-119">Dopo essere stata "distribuita in modo uniforme":</span><span class="sxs-lookup"><span data-stu-id="cad7c-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="cad7c-120">Dopo essere stata "consolidata":</span><span class="sxs-lookup"><span data-stu-id="cad7c-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="cad7c-121">In azione</span><span class="sxs-lookup"><span data-stu-id="cad7c-121">In action</span></span>

<span data-ttu-id="cad7c-122">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cad7c-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="cad7c-123">[![Dimostrazione della riformattazione delle tabelle](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cad7c-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
