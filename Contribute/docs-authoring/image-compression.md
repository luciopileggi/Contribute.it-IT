---
title: Compressione delle immagini - Docs Authoring Pack
description: Informazioni su come eseguire la compressione delle immagini con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336659"
---
# <a name="image-compression"></a>Compressione delle immagini

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>Riepilogo

Tutta la documentazione viene fornita tramite il Web, ad eccezione delle versioni PDF dei documenti. Quando si far uso di contenuto statico, è preferibile ridurre al minimo il numero di byte inviati in rete. A questo scopo, è possibile, ad esempio, comprimere le immagini inattive.

L'estensione Docs Authoring Pack include voci di menu di scelta rapida per la compressione delle immagini. Sono supportati i tipi di immagini/estensioni seguenti:

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

Se possibile, vengono usati algoritmi di compressione delle immagini senza perdita di dati.

## <a name="compress-image"></a>Comprimere un'immagine

Nel riquadro di spostamento **Explorer** fare clic con il pulsante destro del mouse su un file di immagine, quindi selezionare l'opzione **Comprimi immagine**. L'immagine viene quindi compressa.

## <a name="compress-images-in-folder"></a>Comprimere le immagini in una cartella

Nel riquadro di spostamento **Explorer** fare clic con il pulsante destro del mouse su una cartella contenente immagini, quindi selezionare l'opzione **Comprimi immagini in cartella**. Vengono compresse tutte le immagini della cartella.

## <a name="considerations"></a>Considerazioni

Le immagini a risoluzione elevata vengono ridimensionate in modo implicito. Le dimensioni massime sono basate sulla larghezza massima consigliata dalla piattaforma di `1,200px`. Il valore massimo viene usato solo quando le immagini sono più grandi rispetto alle dimensioni consigliate e, in caso di ridimensionamento automatico, vengono mantenute le proporzioni.

## <a name="preferences"></a>Preferenze

Le dimensioni massime sono configurabili, sebbene esista una larghezza massima predefinita di `1200` pixel. Per configurare le dimensioni massime, selezionare **File -> Preferenze -> Impostazioni** e filtrare per `"Docs Image Extension"`.

:::image type="content" source="media/configure-image-compression.png" alt-text="Configurare la compressione delle immagini":::

> [!NOTE]
> Il valore `0` nel campo **Larghezza massima** o **Altezza massima** indica semplicemente di ignorare le varianze di risoluzione.

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione della compressione delle immagini](media/compress-image.gif)](media/compress-image.gif#lightbox)
