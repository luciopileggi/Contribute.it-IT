---
title: Flusso di lavoro per i contributi a GitHub per modifiche minime o non frequenti
description: Questo articolo illustra come usare il flusso di lavoro per i contributi "minimi" per gli articoli di docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>Flusso di lavoro per i contributi a GitHub per modifiche minime o non frequenti

> [!IMPORTANT]
> Tutti i repository che pubblicano contenuto in docs.microsoft.com adottano il [Codice di comportamento Open Source di Microsoft](https://opensource.microsoft.com/codeofconduct/) o il [Codice di comportamento di .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Per altre informazioni, vedere [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) (Domande frequenti sul Codice di comportamento Open Source di Microsoft) oppure contattare [opencode@microsoft.com](mailto:opencode@microsoft.com) o [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) per eventuali domande o commenti.<br>
>
> Le correzioni minori o i chiarimenti inviati per la documentazione e gli esempi di codice nei repository pubblici sono coperti dalle [Condizioni per l'utilizzo di docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Per le novità o le modifiche significative verrà generato un commento nella richiesta pull con la richiesta di inviare un contratto di licenza online per i contributi (Contribution License Agreement, CLA) se non si è dipendenti Microsoft. Prima che la richiesta pull venga accettata, è necessario completare il modulo online.

## <a name="overview"></a>Panoramica

Questo flusso di lavoro è appropriato per apportare modifiche minime o non frequenti usando il Markdown editor basato su Web di GitHub. L'editor di GitHub offre funzionalità limitate poiché l'interfaccia utente non supporta tutte le operazioni e gli scenari di modifica per Git. Per pubblicare contributi più estesi oppure se è necessario il supporto di funzionalità Git avanzate, come la gestione dei rami o la risoluzione avanzata dei conflitti di unione, fare riferimento al [flusso di lavoro per modifiche di rilievo o di lunga durata](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Procedura per l'uso dell'editor di GitHub per proporre le modifiche

1. Passare al repository e al file di Markdown di GitHub corrispondente dell'articolo. È possibile usare uno dei metodi seguenti:

   - Trovare l'articolo esplorando i file di Markdown nel repository di GitHub correlato.
   - Passare all'articolo in [docs.microsoft.com](https://docs.microsoft.com/) e selezionare il collegamento **Modifica** nell'angolo superiore destro della pagina.

     ![Percorso del collegamento Modifica](./media/light-workflow/contributetogit.png)

2. Selezionare l'icona a forma di matita **Edit this file** (Modifica file) per passare alla modalità di modifica:

    ![Posizione dell'icona a forma di matita](./media/light-workflow/editicon.png)

3. Apportare le modifiche con Markdown nella scheda **Edit file** (Modifica file) e visualizzare le modifiche in anteprima nella scheda **Preview changes** (Anteprima modifiche). L'uso dell'editor è immediato, ma se occorre assistenza vedere le guide seguenti:

   - [Come usare Markdown](how-to-write-use-markdown.md)
   - [Creating files on GitHub](https://github.com/blog/1327-creating-files-on-github) (Creazione di file in GitHub)
   - [Upload files to your repositories](https://github.com/blog/2105-upload-files-to-your-repositories) (Caricare file nei repository)

4. Scorrere verso la parte inferiore della pagina dove è visualizzata una delle opzioni seguenti:

   - **Propose file change** (Proponi modifica del file): questa opzione viene visualizzata quando si ha accesso in sola lettura al repository, ad esempio durante la [modifica dei file nel repository di un altro utente](https://help.github.com/articles/editing-files-in-another-user-s-repository/). In questo caso, GitHub crea un ramo "patch" nel fork del repository dell'utente, creando automaticamente un fork se non esiste già. Dopo aver selezionato **Propose file change** (Proponi modifica del file), viene visualizzata una pagina **Comparing changes** (Confronto modifiche) che consente di verificare le modifiche. Fare clic sul pulsante **Create pull request** (Crea richiesta pull) per inviare le modifiche alla coda di richieste pull e procedere alla [sezione successiva](#pull-request-processing).

   - **Commit changes** (Commit modifiche): questa opzione viene visualizzata quando sono disponibili autorizzazioni di scrittura per un repository, ad esempio durante [la modifica di file in un repository personale](https://help.github.com/articles/editing-files-in-your-repository/). In questo caso GitHub offre due opzioni per il salvataggio delle modifiche:

     - **Commit directly to the `<branch-name>` branch** (Eseguire il commit direttamente nel ramo <nome ramo>), dove `<branch-name>` è il nome del ramo attivo quando si è fatto clic sul pulsante **Edit** (Modifica). Questa opzione consente di applicare le modifiche direttamente al ramo, anziché usare una richiesta pull. L'operazione è conclusa.

     - **Create a new branch for this commit and start a pull request** (Creare un nuovo ramo per questo commit e avviare una richiesta pull) che propone un nome predefinito per la creazione di un nuovo ramo. Dopo aver selezionato **Propose file change** (Proponi modifica del file), viene visualizzata una pagina **Comparing changes** (Confronto modifiche) che consente di verificare le modifiche. Fare clic sul pulsante **Create pull request** (Crea richiesta pull) per inviare le modifiche alla coda di richieste pull e procedere alla [sezione successiva](#pull-request-processing).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Passaggi successivi

- Continuare con gli articoli "Informazioni di base per la scrittura" per altre informazioni su Markdown, sulla sintassi delle estensioni Markdown e altro.
