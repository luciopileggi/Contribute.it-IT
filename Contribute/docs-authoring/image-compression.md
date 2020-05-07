---
title: Compressione delle immagini - Docs Authoring Pack
description: Informazioni su come eseguire la compressione delle immagini con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336659"
---
# <a name="image-compression"></a><span data-ttu-id="2fef7-103">Compressione delle immagini</span><span class="sxs-lookup"><span data-stu-id="2fef7-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="2fef7-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="2fef7-104">Summary</span></span>

<span data-ttu-id="2fef7-105">Tutta la documentazione viene fornita tramite il Web, ad eccezione delle versioni PDF dei documenti. Quando si far uso di contenuto statico, è preferibile ridurre al minimo il numero di byte inviati in rete.</span><span class="sxs-lookup"><span data-stu-id="2fef7-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="2fef7-106">A questo scopo, è possibile, ad esempio, comprimere le immagini inattive.</span><span class="sxs-lookup"><span data-stu-id="2fef7-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="2fef7-107">L'estensione Docs Authoring Pack include voci di menu di scelta rapida per la compressione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="2fef7-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="2fef7-108">Sono supportati i tipi di immagini/estensioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fef7-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="2fef7-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="2fef7-109">*\*.png*</span></span>
* <span data-ttu-id="2fef7-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="2fef7-110">*\*.jpg*</span></span>
* <span data-ttu-id="2fef7-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="2fef7-111">*\*.jpeg*</span></span>
* <span data-ttu-id="2fef7-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="2fef7-112">*\*.gif*</span></span>
* <span data-ttu-id="2fef7-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="2fef7-113">*\*.svg*</span></span>
* <span data-ttu-id="2fef7-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="2fef7-114">*\*.webp*</span></span>

<span data-ttu-id="2fef7-115">Se possibile, vengono usati algoritmi di compressione delle immagini senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="2fef7-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="2fef7-116">Comprimere un'immagine</span><span class="sxs-lookup"><span data-stu-id="2fef7-116">Compress image</span></span>

<span data-ttu-id="2fef7-117">Nel riquadro di spostamento **Explorer** fare clic con il pulsante destro del mouse su un file di immagine, quindi selezionare l'opzione **Comprimi immagine**.</span><span class="sxs-lookup"><span data-stu-id="2fef7-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="2fef7-118">L'immagine viene quindi compressa.</span><span class="sxs-lookup"><span data-stu-id="2fef7-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="2fef7-119">Comprimere le immagini in una cartella</span><span class="sxs-lookup"><span data-stu-id="2fef7-119">Compress images in folder</span></span>

<span data-ttu-id="2fef7-120">Nel riquadro di spostamento **Explorer** fare clic con il pulsante destro del mouse su una cartella contenente immagini, quindi selezionare l'opzione **Comprimi immagini in cartella**.</span><span class="sxs-lookup"><span data-stu-id="2fef7-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="2fef7-121">Vengono compresse tutte le immagini della cartella.</span><span class="sxs-lookup"><span data-stu-id="2fef7-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="2fef7-122">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="2fef7-122">Considerations</span></span>

<span data-ttu-id="2fef7-123">Le immagini a risoluzione elevata vengono ridimensionate in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="2fef7-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="2fef7-124">Le dimensioni massime sono basate sulla larghezza massima consigliata dalla piattaforma di `1,200px`.</span><span class="sxs-lookup"><span data-stu-id="2fef7-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="2fef7-125">Il valore massimo viene usato solo quando le immagini sono più grandi rispetto alle dimensioni consigliate e, in caso di ridimensionamento automatico, vengono mantenute le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="2fef7-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="2fef7-126">Preferenze</span><span class="sxs-lookup"><span data-stu-id="2fef7-126">Preferences</span></span>

<span data-ttu-id="2fef7-127">Le dimensioni massime sono configurabili, sebbene esista una larghezza massima predefinita di `1200` pixel.</span><span class="sxs-lookup"><span data-stu-id="2fef7-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="2fef7-128">Per configurare le dimensioni massime, selezionare **File -> Preferenze -> Impostazioni** e filtrare per `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="2fef7-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Configurare la compressione delle immagini":::

> [!NOTE]
> <span data-ttu-id="2fef7-130">Il valore `0` nel campo **Larghezza massima** o **Altezza massima** indica semplicemente di ignorare le varianze di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="2fef7-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="2fef7-131">In azione</span><span class="sxs-lookup"><span data-stu-id="2fef7-131">In action</span></span>

<span data-ttu-id="2fef7-132">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2fef7-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="2fef7-133">[![Dimostrazione della compressione delle immagini](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2fef7-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
