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
# <a name="sort-selection"></a>Ordinamento della selezione

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

In un file Markdown ( *\*.md*), dopo aver apportato una selezione, sono ora disponibili due voci di menu di scelta rapida per l'ordinamento. Fare clic con il pulsante destro del mouse sul testo selezionato per aprire il meno di scelta rapida. Vengono visualizzate due voci di menu simili alle seguenti:

:::image type="content" source="media/sort-selection-menu.png" alt-text="Menu di scelta rapida per la selezione dell'ordinamento":::

> [!TIP]
> Le voci di menu di scelta rapida per l'ordinamento rimangono nascoste fino a quando nell'editor di testo Visual Studio Code non viene inserita una selezione valida.

## <a name="sort-selection-ascending-a-to-z"></a>Ordinamento crescente della selezione (dalla A alla Z)

Se si seleziona l'opzione **Ordinamento crescente della selezione (dalla A alla Z)** l'intera selezione viene ordinata in modo alfabetico crescente, dalla A alla Z.

## <a name="sort-selection-descending-z-to-a"></a>Ordinamento decrescente della selezione (dalla Z alla A)

Se si seleziona l'opzione **Ordinamento decrescente della selezione (dalla A alla Z)** l'intera selezione viene ordinata in modo alfabetico decrescente, dalla Z alla A.

## <a name="considerations"></a>Considerazioni

Il meccanismo di ordinamento sottostante usa un *ordinamento* basato sul linguaggio naturale, più efficiente e completo rispetto all'ordinamento standard. Osservare la tabella seguente:

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

Se questo meccanismo non usasse l'ordinamento basato sul linguaggio naturale, l'ordine di `Column1` sarebbe 1, 11, 2 e così via; capisce invece che 11 è maggiore di 2, ottenendo l'ordine crescente seguente:

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

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione dell'ordinamento della selezione](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
