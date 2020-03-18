---
title: Sostituzione automatica delle virgolette curve - Docs Authoring Pack
description: Informazioni su come eseguire la sostituzione automatica delle virgolette curve con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336705"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="cc6cc-103">Sostituzione delle virgolette curve</span><span class="sxs-lookup"><span data-stu-id="cc6cc-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="cc6cc-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cc6cc-104">Summary</span></span>

<span data-ttu-id="cc6cc-105">Sebbene agli sviluppatori di contenuti sia riconosciuta la creazione di alcune delle più avanzate innovazioni della tecnologia e dell'intelligenza moderne, in Markdown viene tuttora preferito l'uso delle virgolette dritte,</span><span class="sxs-lookup"><span data-stu-id="cc6cc-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="cc6cc-106">che si oppongono, ovviamente, alle virgolette curve.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="cc6cc-107">Le virgolette curve sono preferite nelle tipografie ideali, ma non in Markdown o nel codice HTML di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="cc6cc-108">Lavorando su un documento di Microsoft Word, ad esempio, si sarà notato che, se si tiene premuto il tasto <kbd>MAIUSC</kbd> e si digita <kbd>"</kbd>, Microsoft Word sostituisce rapidamente il carattere `"` con virgolette curve, equivalenti al carattere `“`.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="cc6cc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc6cc-109">Description</span></span>        | <span data-ttu-id="cc6cc-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="cc6cc-110">Unicode</span></span>  | <span data-ttu-id="cc6cc-111">Virgolette curve</span><span class="sxs-lookup"><span data-stu-id="cc6cc-111">Smart Quote</span></span> | <span data-ttu-id="cc6cc-112">Sostituzione</span><span class="sxs-lookup"><span data-stu-id="cc6cc-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="cc6cc-113">Virgolette doppie (sinistra)</span><span class="sxs-lookup"><span data-stu-id="cc6cc-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="cc6cc-114">Virgolette doppie (destra)</span><span class="sxs-lookup"><span data-stu-id="cc6cc-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="cc6cc-115">Virgoletta singola (sinistra)</span><span class="sxs-lookup"><span data-stu-id="cc6cc-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="cc6cc-116">Virgoletta singola (destra)</span><span class="sxs-lookup"><span data-stu-id="cc6cc-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="cc6cc-117">In un file Markdown ( *\*.md*), quando si incolla del testo o si aggiorna il contenuto, questa funzionalità valuta attivamente il contenuto e, in automatico, sostituisce i valori di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="cc6cc-118">La funzionalità di sostituzione delle virgolette curve determina anche la sostituzione di altri caratteri, ad esempio (ma non solo): `©, ™, ®, •` e caratteri di apice e pedice.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="cc6cc-119">Questa funzionalità è particolarmente utile quando si incollano blocchi di testo da documenti Word.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="cc6cc-120">Preferenze</span><span class="sxs-lookup"><span data-stu-id="cc6cc-120">Preferences</span></span>

<span data-ttu-id="cc6cc-121">Questa funzionalità è facoltativa ma, per impostazione predefinita, è impostata su `true`.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="cc6cc-122">Per attivare o disattivare questa funzionalità:</span><span class="sxs-lookup"><span data-stu-id="cc6cc-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="cc6cc-123">Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="cc6cc-124">Abilitare o disabilitare l'impostazione nella sezione **Markdown: Replace Smart Quotes** (Markdown: Sostituisci virgolette curve).</span><span class="sxs-lookup"><span data-stu-id="cc6cc-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="cc6cc-125">In azione</span><span class="sxs-lookup"><span data-stu-id="cc6cc-125">In action</span></span>

<span data-ttu-id="cc6cc-126">Di seguito è riportata una breve dimostrazione di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cc6cc-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="cc6cc-127">[![Dimostrazione della sostituzione delle virgolette curve](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cc6cc-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
