---
title: Completamento dei linguaggi di sviluppo - Docs Authoring Pack
description: Informazioni su come il completamento dei linguaggi di sviluppo semplifichi il lavoro degli autori di contributi in Docs Authoring Pack, estensione di Visual Studio Code.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336797"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="eba15-103">Completamento dei linguaggi di sviluppo</span><span class="sxs-lookup"><span data-stu-id="eba15-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="eba15-104">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="eba15-104">Summary</span></span>

<span data-ttu-id="eba15-105">Agli autori di contributi occorre assistenza per determinare gli identificatori di lingua validi (linguaggi di sviluppo) che possono seguire tripli apici inversi (aperture in un codice delimitato) in un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="eba15-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="eba15-106">Sfortunatamente, infatti, non esiste la convalida in fase di compilazione dei linguaggi di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="eba15-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="eba15-107">Ne consegue la coesistenza di varie rappresentazioni di un unico linguaggio all'interno dello stesso docset concettuale.</span><span class="sxs-lookup"><span data-stu-id="eba15-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="eba15-108">Si consideri, ad esempio, il linguaggio C#.</span><span class="sxs-lookup"><span data-stu-id="eba15-108">Consider C# as an example.</span></span> <span data-ttu-id="eba15-109">Gli autori di contributi hanno usato `c#`, `C#`, `cs`, `csharp` e altri simboli come rappresentazioni del linguaggio di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="eba15-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="eba15-110">Quale delle rappresentazioni precedenti è corretta?</span><span class="sxs-lookup"><span data-stu-id="eba15-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="eba15-111">La funzionalità *Completamento dei linguaggi di sviluppo* dissipa la confusione visualizzando un elenco dei linguaggi di sviluppo noti.</span><span class="sxs-lookup"><span data-stu-id="eba15-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="eba15-112">Quando si seleziona un nome di linguaggio di sviluppo da IntelliSense:</span><span class="sxs-lookup"><span data-stu-id="eba15-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="eba15-113">La delimitazione del codice viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="eba15-113">The code fence is closed.</span></span>
* <span data-ttu-id="eba15-114">Il cursore viene posizionato nella delimitazione del codice.</span><span class="sxs-lookup"><span data-stu-id="eba15-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="eba15-115">Preferenze</span><span class="sxs-lookup"><span data-stu-id="eba15-115">Preferences</span></span>

<span data-ttu-id="eba15-116">Non è possibile disabilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="eba15-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="eba15-117">Sono disponibili le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="eba15-117">The following settings are available:</span></span>

* <span data-ttu-id="eba15-118">[Display commonly used dev langs](#display-commonly-used-dev-langs) (Visualizza i linguaggi di sviluppo più usati)</span><span class="sxs-lookup"><span data-stu-id="eba15-118">[Display commonly used dev langs](#display-commonly-used-dev-langs)</span></span>
* <span data-ttu-id="eba15-119">[Display all known dev langs](#display-all-known-dev-langs) (Visualizza tutti i linguaggi di sviluppo noti)</span><span class="sxs-lookup"><span data-stu-id="eba15-119">[Display all known dev langs](#display-all-known-dev-langs)</span></span>

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="eba15-120">Visualizzare i linguaggi di sviluppo più usati</span><span class="sxs-lookup"><span data-stu-id="eba15-120">Display commonly used dev langs</span></span>

<span data-ttu-id="eba15-121">In un docset viene usato solo un sottoinsieme dei linguaggi di sviluppo validi.</span><span class="sxs-lookup"><span data-stu-id="eba15-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="eba15-122">Per migliorare l'esperienza utente:</span><span class="sxs-lookup"><span data-stu-id="eba15-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="eba15-123">In Visual Studio Code aprire il docst alla directory radice.</span><span class="sxs-lookup"><span data-stu-id="eba15-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="eba15-124">Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="eba15-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="eba15-125">Fare clic sul collegamento **Edit in settings.json** (Modifica in settings.json) nella sezione **Markdown: Docset Languages** (Markdown: linguaggi docset).</span><span class="sxs-lookup"><span data-stu-id="eba15-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="eba15-126">Aggiungere la proprietà `markdown.docsetLanguages` seguente al file *settings.json*:</span><span class="sxs-lookup"><span data-stu-id="eba15-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="eba15-127">Posizionare il cursore nella matrice vuota della proprietà e attivare IntelliSense (tramite <kbd>CTRL</kbd> + <kbd>spazio</kbd>).</span><span class="sxs-lookup"><span data-stu-id="eba15-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="eba15-128">Viene visualizzato un elenco di nomi di linguaggi di sviluppo noti.</span><span class="sxs-lookup"><span data-stu-id="eba15-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="eba15-129">Aggiungere all'array i nomi di linguaggi di sviluppo desiderati fino a quando non si è soddisfatti dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="eba15-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="eba15-130">Nell'immagine seguente, ad esempio, i triplici apici digitati dall'utente sono seguiti da un elenco di quattro nomi di linguaggi di sviluppo:</span><span class="sxs-lookup"><span data-stu-id="eba15-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="eba15-131">Salvare le modifiche apportate al file *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="eba15-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="eba15-132">Se la matrice `markdown.docsetLanguages` è vuota, vengono visualizzati tutti i linguaggi di sviluppo noti.</span><span class="sxs-lookup"><span data-stu-id="eba15-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="eba15-133">Visualizzare tutti i linguaggi di sviluppo noti</span><span class="sxs-lookup"><span data-stu-id="eba15-133">Display all known dev langs</span></span>

<span data-ttu-id="eba15-134">Per impostazione predefinita, in IntelliSense vengono visualizzati tutti i nomi di linguaggio di sviluppo noti.</span><span class="sxs-lookup"><span data-stu-id="eba15-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="eba15-135">Queste impostazioni sostituiscono la proprietà `markdown.docsetLanguages` descritta nella sezione [Visualizzare i linguaggi di sviluppo più usati](#display-commonly-used-dev-langs).</span><span class="sxs-lookup"><span data-stu-id="eba15-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="eba15-136">Per modificare questa impostazione:</span><span class="sxs-lookup"><span data-stu-id="eba15-136">To change this setting:</span></span>

1. <span data-ttu-id="eba15-137">Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="eba15-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="eba15-138">Abilitare o disabilitare l'impostazione nella sezione **Markdown: All Available Languages** (Markdown: Tutti i linguaggi disponibili).</span><span class="sxs-lookup"><span data-stu-id="eba15-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="eba15-139">In azione</span><span class="sxs-lookup"><span data-stu-id="eba15-139">In action</span></span>

<span data-ttu-id="eba15-140">Di seguito è riportata una breve dimostrazione di questa funzionalità:</span><span class="sxs-lookup"><span data-stu-id="eba15-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="eba15-141">[![Completamento dei linguaggi di sviluppo](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="eba15-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
