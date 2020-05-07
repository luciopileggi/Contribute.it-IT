---
title: Ordinamento dei reindirizzamenti - Docs Authoring Pack
description: Informazioni su come eseguire l'ordinamento dei reindirizzamenti con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336682"
---
# <a name="sort-redirects"></a><span data-ttu-id="b0069-103">Ordinamento dei reindirizzamenti</span><span class="sxs-lookup"><span data-stu-id="b0069-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="b0069-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="b0069-104">Summary</span></span>

<span data-ttu-id="b0069-105">Con l'evoluzione di un docset docs.microsoft.com, alcuni file Markdown verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="b0069-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="b0069-106">Quando viene eliminato un file Markdown, è necessario specificare un reindirizzamento in modo che qualsiasi riferimento all'articolo eliminato venga risolto correttamente tramite il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="b0069-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="b0069-107">I reindirizzamenti vengono specificati nel file *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="b0069-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="b0069-108">Aprire il riquadro comandi, premere <kbd>F1</kbd> (o <kbd>⇧⌘P</kbd> in macOS)</span><span class="sxs-lookup"><span data-stu-id="b0069-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="b0069-109">Digitare: **Docs: Sort master redirection file**</span><span class="sxs-lookup"><span data-stu-id="b0069-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="b0069-110">Selezionare il comando da eseguire</span><span class="sxs-lookup"><span data-stu-id="b0069-110">Select the command to execute it</span></span>
1. <span data-ttu-id="b0069-111">Osservare le modifiche apportate al file *.openpublishing.redirection.json*</span><span class="sxs-lookup"><span data-stu-id="b0069-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="b0069-112">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="b0069-112">Considerations</span></span>

<span data-ttu-id="b0069-113">Il concetto di "daisy chaining" fa riferimento al modo in cui è stato originariamente progettato il file *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="b0069-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="b0069-114">Con il passare del tempo, i file aggiunti come reindirizzamento verranno resi obsoleti.</span><span class="sxs-lookup"><span data-stu-id="b0069-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="b0069-115">Questa situazione si verifica quando il file A viene eliminato e viene quindi specificato un reindirizzamento al file B e, in seguito, anche il file B viene eliminato e viene eseguito un reindirizzamento al file C. In teoria, quindi, entrambi i file puntano a C, in modo che A venga reindirizzato direttamente a C e B rimanga invariato.</span><span class="sxs-lookup"><span data-stu-id="b0069-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="b0069-116">Ne risulta un lieve miglioramento delle prestazioni e questa funzionalità è ancora oggetto di studio.</span><span class="sxs-lookup"><span data-stu-id="b0069-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="b0069-117">In azione</span><span class="sxs-lookup"><span data-stu-id="b0069-117">In action</span></span>

<span data-ttu-id="b0069-118">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b0069-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="b0069-119">[![Dimostrazione dell'ordinamento dei reindirizzamenti](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b0069-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
