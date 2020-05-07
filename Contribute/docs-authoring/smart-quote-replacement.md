---
title: Sostituzione automatica delle virgolette curve - Docs Authoring Pack
description: Informazioni su come eseguire la sostituzione automatica delle virgolette curve con Docs Authoring Pack, estensione di Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336705"
---
# <a name="smart-quote-replacement"></a>Sostituzione delle virgolette curve

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Riepilogo

Sebbene agli sviluppatori di contenuti sia riconosciuta la creazione di alcune delle più avanzate innovazioni della tecnologia e dell'intelligenza moderne, in Markdown viene tuttora preferito l'uso delle virgolette dritte, che si oppongono, ovviamente, alle virgolette curve. Le virgolette curve sono preferite nelle tipografie ideali, ma non in Markdown o nel codice HTML di cui è stato eseguito il rendering.

Lavorando su un documento di Microsoft Word, ad esempio, si sarà notato che, se si tiene premuto il tasto <kbd>MAIUSC</kbd> e si digita <kbd>"</kbd>, Microsoft Word sostituisce rapidamente il carattere `"` con virgolette curve, equivalenti al carattere `“`.

| Descrizione        | Unicode  | Virgolette curve | Sostituzione |
|--------------------|----------|-------------|-------------|
| Virgolette doppie (sinistra)  | `\u201c` | `“`         | `"`         |
| Virgolette doppie (destra) | `\u201d` | `”`         | `"`         |
| Virgoletta singola (sinistra)  | `\u2018` | `‘`         | `'`         |
| Virgoletta singola (destra) | `\u2019` | `’`         | `'`         |

In un file Markdown ( *\*.md*), quando si incolla del testo o si aggiorna il contenuto, questa funzionalità valuta attivamente il contenuto e, in automatico, sostituisce i valori di conseguenza.

> [!NOTE]
> La funzionalità di sostituzione delle virgolette curve determina anche la sostituzione di altri caratteri, ad esempio (ma non solo): `©, ™, ®, •` e caratteri di apice e pedice. Questa funzionalità è particolarmente utile quando si incollano blocchi di testo da documenti Word.

## <a name="preferences"></a>Preferenze

Questa funzionalità è facoltativa ma, per impostazione predefinita, è impostata su `true`. Per attivare o disattivare questa funzionalità:

1. Selezionare **File** > **Preferenze** > **Impostazioni** e filtrare per *Estensione Docs Markdown*.
1. Abilitare o disabilitare l'impostazione nella sezione **Markdown: Replace Smart Quotes** (Markdown: Sostituisci virgolette curve).

## <a name="in-action"></a>In azione

Di seguito è riportata una breve dimostrazione di questa funzionalità.

[![Dimostrazione della sostituzione delle virgolette curve](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
