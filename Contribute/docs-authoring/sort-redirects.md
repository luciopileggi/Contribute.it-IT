---
title: Ordinamento dei reindirizzamenti - Docs Authoring Pack
description: Informazioni su come eseguire l'ordinamento dei reindirizzamenti con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336682"
---
# <a name="sort-redirects"></a>Ordinamento dei reindirizzamenti

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

Con l'evoluzione di un docset docs.microsoft.com, alcuni file Markdown verranno eliminati. Quando viene eliminato un file Markdown, è necessario specificare un reindirizzamento in modo che qualsiasi riferimento all'articolo eliminato venga risolto correttamente tramite il reindirizzamento. I reindirizzamenti vengono specificati nel file *.openpublishing.redirection.json*.

1. Aprire il riquadro comandi, premere <kbd>F1</kbd> (o <kbd>⇧⌘P</kbd> in macOS)
1. Digitare: **Docs: Sort master redirection file**
1. Selezionare il comando da eseguire
1. Osservare le modifiche apportate al file *.openpublishing.redirection.json*

## <a name="considerations"></a>Considerazioni

Il concetto di "daisy chaining" fa riferimento al modo in cui è stato originariamente progettato il file *.openpublishing.redirection.json*. Con il passare del tempo, i file aggiunti come reindirizzamento verranno resi obsoleti. Questa situazione si verifica quando il file A viene eliminato e viene quindi specificato un reindirizzamento al file B e, in seguito, anche il file B viene eliminato e viene eseguito un reindirizzamento al file C. In teoria, quindi, entrambi i file puntano a C, in modo che A venga reindirizzato direttamente a C e B rimanga invariato. Ne risulta un lieve miglioramento delle prestazioni e questa funzionalità è ancora oggetto di studio.

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione dell'ordinamento dei reindirizzamenti](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
