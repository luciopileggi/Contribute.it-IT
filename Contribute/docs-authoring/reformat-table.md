---
title: Riformattazione delle tabelle Markdown - Docs Authoring Pack
description: Informazioni su come usare le varie funzionalità di formattazione delle tabelle Markdown di Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336774"
---
# <a name="reformat-markdown-tables"></a>Riformattazione delle tabelle Markdown

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

In un file Markdown ( *\*.md*), quando si seleziona una tabella completa, sono ora disponibili due voci di menu di scelta rapida per la formattazione della tabella. Fare clic con il pulsante destro del mouse sulla tabella Markdown per aprire il meno di scelta rapida. Vengono visualizzate due voci di menu simili alle seguenti:

:::image type="content" source="media/reformat-table-menu.png" alt-text="Menu di scelta rapida per la riformattazione della tabella":::

> [!TIP]
> Questa funzionalità **non** può essere usata per più selezioni di tabelle, ma è progettata per una singola tabella Markdown. Per ottenere i risultati desiderati, è necessario selezionare l'intera tabella, incluse le intestazioni.

## <a name="consolidate-selected-table"></a>Consolidare la tabella selezionata

Se si seleziona l'opzione **Consolidate selected table** (Consolida tabella selezionata), le intestazioni e i contenuti delle tabelle vengono compressi lasciando un solo spazio su entrambi i lati di ogni valore.

## <a name="evenly-distribute-selected-table"></a>Distribuire la tabella selezionata in modo uniforme

Se si seleziona l'opzione **Evenly distribute selected table** (Distribuisci in modo uniforme la tabella selezionata) viene calcolato il valore più lungo di ogni colonna e, in base ad esso, tutti gli altri valori vengono distribuiti in modo uniforme, con lo spazio.

## <a name="considerations"></a>Considerazioni

Questa funzionalità non ha alcun effetto sul rendering della tabella, ma ne migliora la leggibilità, rendendola anche più gestibile. La funzionalità di riformattazione della tabella mantiene intatto l'allineamento delle colonne.

Osservare la tabella seguente:

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

Dopo essere stata "distribuita in modo uniforme":

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

Dopo essere stata "consolidata":

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

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione della riformattazione delle tabelle](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
