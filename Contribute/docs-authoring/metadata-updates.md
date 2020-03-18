---
title: Aggiornamenti dei metadati - Docs Authoring Pack
description: Informazioni su come eseguire l'aggiornamento dei metadati con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336636"
---
# <a name="update-metadata"></a>Aggiornare i metadati

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

In un file Markdown ( *\*.md*) sono disponibili due voci di menu contestuali dedicate ai metadati. Quando si fa clic con il pulsante destro del mouse in un punto qualsiasi dell'editor di testo, vengono visualizzate due voci di menu simili alle seguenti:

:::image type="content" source="media/update-metadata-menu.png" alt-text="Aggiornare il menu di scelta rapida dei metadati":::

## <a name="update-msdate-metadata-value"></a>Aggiornare il valore di metadati `ms.date`

Se si seleziona l'opzione **Update `ms.date` Metadata Value** (Aggiorna il valore di metadati `ms.date`), il valore `ms.date` dei file Markdown correnti viene impostato sulla data odierna. Se nel documento non è presente un campo di metadati `ms.date`, non viene eseguita alcuna azione.

## <a name="update-implicit-metadata-values"></a>Aggiornare i valori dei metadati impliciti

Se si seleziona l'opzione **Update implicit metadata values** (Aggiorna i valori dei metadati impliciti), vengono trovati e sostituiti tutti i valori di metadati che potrebbero essere stati specificati in modo implicito. I valori dei metadati vengono specificati in modo implicito nel file *docfx.json*, contenuto nel nodo `build/fileMetadata`. Ogni coppia chiave-valore del nodo `fileMetadata` rappresenta le impostazioni predefinite dei metadati. Un file Markdown nella directory di *primo livello/sottocartella* che omette il valore di metadati `ms.author` potrebbe specificare in modo implicito un valore predefinito da usare nel nodo `fileMetadata`.

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

In questo caso, tutti i file Markdown accetterebbero in modo implicito il valore di metadati `ms.author: dapine`. Questa funzionalità interessa quindi le impostazioni implicite rilevate nel file *docfx.json*. Se un file Markdown contiene metadati con valori impostati in modo esplicito su valori diversi da quelli impliciti, questi valori vengono sostituiti.

Si considerino, ad esempio, i seguenti metadati del file Markdown, che si trova in **top-level/sub-folder/includes/example.md**:

```markdown
---
ms.author: someone-else
---

# Content
```

Se in questo file venisse eseguita l'opzione **Update implicit metadata values** (Aggiorna i valori dei metadati impliciti), supponendo che contenga il file *docfx.json* sopra specificato, il valore di metadati verrebbe aggiornato su `ms.author: dapine`.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione dell'aggiornamento dei metadati](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
