---
title: Installare gli strumenti di creazione del contenuto
description: Questo articolo include informazioni utili per scaricare e installare gli strumenti client che saranno necessari per Git e la modifica dei file markdown.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>Installare gli strumenti di creazione del contenuto

In questo articolo vengono descritti i passaggi per installare in modo interattivo gli strumenti client Git e Visual Studio Code.
> [!div class="checklist"]
> * Installare [Git per Windows](https://git-scm.com/download/win)
> * Installare [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> Per apportare solo modifiche minime agli articoli, *non* è necessario completare i passaggi contenuti in questo articolo ed è possibile passare direttamente al [flusso di lavoro per modifiche minime o non frequenti](light-workflow.md).
>
> I collaboratori principali sono invitati a completare questi passaggi, che consentono di usare il [flusso di lavoro per modifiche di rilievo o di lunga durata](full-workflow.md). Anche se sono disponibili le autorizzazioni di scrittura nel repository principale, *è caldamente consigliata la creazione di un fork e di un clone del repository* (e le informazioni nella presente guida la danno per scontata), in modo da disporre di autorizzazioni di lettura/scrittura per archiviare le modifiche proposte nel fork.

## <a name="install-git-client-tools-on-windows"></a>Installare gli strumenti client Git in Windows

 Installare la versione più recente degli [strumenti client Git di Software Freedom Conservancy](https://git-scm.com/download/). L'installazione include il sistema di controllo delle versioni di Git e Git Bash, l'app della riga di comando usata per interagire con il repository Git locale.

Se si preferisce un'interfaccia utente grafica (GUI) rispetto a un'interfaccia della riga di comando, vedere alcune opzioni diffuse in [Software Freedom Conservancy's available GUI Clients](https://git-scm.com/downloads/guis) (Client GUI disponibili di Software Freedom Conservancy), [GitHub's GitHub Desktop](https://desktop.github.com/) (GitHub Desktop di GitHub) o [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).

Seguire le istruzioni relative al client selezionato per l'installazione e configurazione.

Nel prossimo articolo verrà descritto come [configurare un repository Git locale](get-started-setup-local.md).

   Le risorse aggiuntive su Git sono disponibili qui: [Terminologia di Git](https://help.github.com/articles/github-glossary) | [Nozioni di base su Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Risorse di formazione per Git e GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Informazioni sugli editor Markdown

Markdown è un linguaggio di markup leggero di facile lettura e semplice da imparare. Per questo motivo, si è imposto rapidamente come standard del settore. Per scrivere articoli in Markdown, è prima di tutto consigliabile scaricare e installare un editor di Markdown.  [Visual Studio Code](https://code.visualstudio.com/) è lo strumento preferito per la modifica di Markdown in Microsoft. [Atom](https://atom.io) è un altro strumento di ampia diffusione per la modifica di Markdown.

Il testo Markdown viene salvato in file con estensione MD.

Per altri dettagli sulla scrittura con Markdown, inclusi i concetti di base e le funzionalità supportate dalle estensioni Markdown personalizzate per OPS, vedere l'articolo [Come usare Markdown](how-to-write-use-markdown.md).

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), anche denominato VS Code, è un editor leggero che funziona in Windows, Linux e Mac. Include l'integrazione di Git e il supporto per le estensioni.

Scaricare e installare [Visual Studio Code](https://code.visualstudio.com/). La home page di Visual Studio Code dovrebbe rilevare correttamente il sistema operativo.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Per avviare Visual Studio Code e aprire la cartella corrente, eseguire il comando `code .` nella riga di comando o nella shell Bash. Se la cartella corrente fa parte di un repository Git locale, l'integrazione di GitHub viene visualizzata automaticamente in Visual Studio Code.

## <a name="next-steps"></a>Passaggi successivi

A questo punto si è pronti per [configurare un repository Git locale](get-started-setup-local.md).
