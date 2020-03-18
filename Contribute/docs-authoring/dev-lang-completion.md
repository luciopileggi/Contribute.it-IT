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
# <a name="dev-lang-completion"></a>Completamento dei linguaggi di sviluppo

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

Agli autori di contributi occorre assistenza per determinare gli identificatori di lingua validi (linguaggi di sviluppo) che possono seguire tripli apici inversi (aperture in un codice delimitato) in un file Markdown. Sfortunatamente, infatti, non esiste la convalida in fase di compilazione dei linguaggi di sviluppo. Ne consegue la coesistenza di varie rappresentazioni di un unico linguaggio all'interno dello stesso docset concettuale.

Si consideri, ad esempio, il linguaggio C#. Gli autori di contributi hanno usato `c#`, `C#`, `cs`, `csharp` e altri simboli come rappresentazioni del linguaggio di sviluppo. Quale delle rappresentazioni precedenti è corretta?

La funzionalità *Completamento dei linguaggi di sviluppo* dissipa la confusione visualizzando un elenco dei linguaggi di sviluppo noti. Quando si seleziona un nome di linguaggio di sviluppo da IntelliSense:

* La delimitazione del codice viene chiusa.
* Il cursore viene posizionato nella delimitazione del codice.

## <a name="preferences"></a>Preferenze

Non è possibile disabilitare questa funzionalità. Sono disponibili le impostazioni seguenti:

* [Display commonly used dev langs](#display-commonly-used-dev-langs) (Visualizza i linguaggi di sviluppo più usati)
* [Display all known dev langs](#display-all-known-dev-langs) (Visualizza tutti i linguaggi di sviluppo noti)

### <a name="display-commonly-used-dev-langs"></a>Visualizzare i linguaggi di sviluppo più usati

In un docset viene usato solo un sottoinsieme dei linguaggi di sviluppo validi. Per migliorare l'esperienza utente:

1. In Visual Studio Code aprire il docst alla directory radice.
1. Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.
1. Fare clic sul collegamento **Edit in settings.json** (Modifica in settings.json) nella sezione **Markdown: Docset Languages** (Markdown: linguaggi docset).
1. Aggiungere la proprietà `markdown.docsetLanguages` seguente al file *settings.json*:

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Posizionare il cursore nella matrice vuota della proprietà e attivare IntelliSense (tramite <kbd>CTRL</kbd> + <kbd>spazio</kbd>). Viene visualizzato un elenco di nomi di linguaggi di sviluppo noti.
1. Aggiungere all'array i nomi di linguaggi di sviluppo desiderati fino a quando non si è soddisfatti dell'elenco. Nell'immagine seguente, ad esempio, i triplici apici digitati dall'utente sono seguiti da un elenco di quattro nomi di linguaggi di sviluppo:

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

1. Salvare le modifiche apportate al file *settings.json*.

> [!WARNING]
> Se la matrice `markdown.docsetLanguages` è vuota, vengono visualizzati tutti i linguaggi di sviluppo noti.

### <a name="display-all-known-dev-langs"></a>Visualizzare tutti i linguaggi di sviluppo noti

Per impostazione predefinita, in IntelliSense vengono visualizzati tutti i nomi di linguaggio di sviluppo noti. Queste impostazioni sostituiscono la proprietà `markdown.docsetLanguages` descritta nella sezione [Visualizzare i linguaggi di sviluppo più usati](#display-commonly-used-dev-langs).

Per modificare questa impostazione:

1. Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.
1. Abilitare o disabilitare l'impostazione nella sezione **Markdown: All Available Languages** (Markdown: Tutti i linguaggi disponibili).

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità:

[![Completamento dei linguaggi di sviluppo](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
