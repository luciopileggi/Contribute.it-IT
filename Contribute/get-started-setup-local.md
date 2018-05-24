---
title: Configurare un repository Git locale
description: Questo articolo contiene indicazioni su come creare il repository Git locale e contribuire alla documentazione, incluso il processo di creazione di fork e cloni.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: f702d0d29ee7dc9c69cb26b79bf6283d91b6b6bc
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2018
---
# <a name="set-up-git-repository-locally-for-documentation"></a>Configurare un repository Git locale per la documentazione

In questo articolo vengono descritti i passaggi per impostare un repository Git nel computer locale, allo scopo di contribuire alla documentazione Microsoft. I collaboratori possono usare un repository clonato in locale per aggiungere nuovi articoli, apportare modifiche di rilievo ad articoli esistenti o modificare la grafica.

Eseguire le attività di installazione seguenti, da effettuare una sola volta, per iniziare a contribuire:
> [!div class="checklist"]
> * Determinare il repository appropriato
> * Eseguire il fork del repository nell'account GitHub
> * Scegliere una cartella locale per i file clonati
> * Clonare il repository nel computer locale
> * Configurare il valore del repository remoto upstream

> [!IMPORTANT]
> Se si stanno apportando solo piccole modifiche a un articolo, *non* è necessario completare i passaggi descritti in questo articolo. È possibile proseguire direttamente con il [flusso di lavoro delle modifiche rapide](index.md#quick-edits-to-existing-documents).
>

## <a name="overview"></a>Panoramica

Per contribuire al sito della documentazione Microsoft, è possibile creare e modificare file Markdown in locale clonando il repository della documentazione corrispondente. Microsoft richiede di eseguire il fork del repository appropriato nel proprio account Github, in modo da disporre di autorizzazioni di lettura/scrittura per archiviare le modifiche proposte. Sarà quindi possibile usare richieste pull per unire le modifiche nel repository condiviso centrale in sola lettura.

![Triangolo GitHub](./media/git-and-github-initial-setup.png)

Se non si ha familiarità con GitHub, guardare il video seguente per una panoramica concettuale del processo di creazione di fork e cloni:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>Determinare il repository

La documentazione ospitata in [docs.microsoft.com](https://docs.microsoft.com) si trova in diversi repository su [github.com](https://www.github.com).

1. Se non si è certi del repository da usare, visitare l'articolo su docs.microsoft.com con il Web browser. Selezionare il collegamento **Modifica** (icona a forma di matita) nell'angolo superiore destro dell'articolo.

   ![Fare clic su Modifica per determinare il repository e il percorso del file.](media/index/edit-article.png)

2. Tale collegamento consente di visualizzare la posizione in github.com del file Markdown corrispondente nel repository appropriato. Esaminare l'URL per visualizzare il nome del repository.

   ![Esaminare l'URL per determinare il percorso del repository.](media/public-repo.png)

   Ad esempio, i repository seguenti sono disponibili per i contributi pubblici:
   - Documentazione di Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - Documentazione di SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Documentazione di Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - Documentazione di .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Documentazione di Azure .NET SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)

## <a name="fork-the-repository"></a>Creare una copia tramite fork del repository
Selezionando il repository appropriato, creare un fork del repository nel proprio account GitHub usando il sito Web GitHub.

Un fork personale è richiesto poiché tutti i repository principali della documentazione sono accessibili in sola lettura e questo significa che non è possibile modificare direttamente il contenuto nei repository. Per apportare modifiche, è necessario inviare una [richiesta pull](git-github-fundamentals.md#pull-requests) dal fork al repository principale. Per facilitare questo processo, è prima necessario avere una copia del repository, accessibile in scrittura. Un *fork* di GitHub serve a tale scopo.

1. Passare alla pagina di GitHub del repository principale e fare clic sul pulsante **Fork** in alto a destra.

   ![Esempio di profilo GitHub](./media/contribute-get-started-setup-local/fork.png)

2. Se richiesto, selezionare il riquadro del proprio account GitHub come destinazione per la creazione del fork. Con questo prompt viene creata una copia del repository nell'account GitHub personale, nota come fork.

## <a name="choose-a-local-folder"></a>Scegliere una cartella locale
Fare in modo che una cartella locale contenga una copia del repository localmente. Alcuni repository possono essere di grandi dimensioni, ad esempio fino a 5 GB per azure-docs. Scegliere una posizione in cui sia disponibile spazio su disco.

1. Scegliere un nome di cartella facile da ricordare e digitare. Considerare ad esempio una cartella radice `C:\docs\` o creare una cartella nella directory del profilo utente `~/Documents/docs/`

   > [!IMPORTANT]
   > Evitare di scegliere un percorso cartella locale nidificato all'interno di un altro percorso cartella di repository Git. Benché sia accettabile archiviare le cartelle Git clonate l'una accanto all'altra, annidare le cartelle Git l'una nell'altra causa errori per il rilevamento file.

2. Avviare Git Bash

   ![Avviare Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   Il percorso predefinito in cui viene avviato Git Bash normalmente è la home directory (~) o `/c/users/<Windows-user-account>/` nel sistema operativo Windows.

   Per determinare la directory corrente, digitare `pwd` al prompt $. 

3. Cambiare directory (cd) selezionando la cartella creata per ospitare il repository localmente. Si noti che in Git Bash per i percorsi cartella viene usata la convenzione di Linux, ovvero le barre anziché le barre rovesciate.

   Ad esempio, `cd /c/docs/ ` o `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>Creare un clone locale

Usando Git Bash, preparare l'esecuzione del comando **clone** per eseguire il pull di una copia di un repository (il fork) nel dispositivo presente nella directory corrente. 

### <a name="authenticate-by-using-git-credential-manager"></a>Eseguire l'autenticazione con Git Credential Manager
Se è stata installata la versione più recente di Git per Windows accettando l'installazione predefinita, Git Credential Manager viene abilitato per impostazione predefinita. Git Credential Manager semplifica notevolmente l'autenticazione, perché non occorre richiamare il token di accesso personale per ristabilire connessioni autenticate o remote con GitHub.

1. Eseguire il comando **clone** specificando il nome del repository. Con la clonazione, il repository di cui è stato creato un fork viene scaricato (clonato) nel computer locale. 

    > [!Tip]
    > È possibile ottenere l'URL di GitHub per il fork per il comando di clonazione dal pulsante **Clone or download** (Clona o scarica) nell'interfaccia utente di GitHub:
    >
    > ![Clone or download (Clona o scarica)](./media/contribute-get-started-setup-local/clone-or-download.png)

    Assicurarsi di specificare il percorso del *proprio fork* durante il processo di clonazione e non quello del repository principale da cui è stato creato il fork. In caso contrario non è possibile collaborare alle modifiche. Viene fatto riferimento al fork attraverso l'account utente di GitHub, ad esempio `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Il comando clone deve essere simile all'esempio seguente:

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. Quando richiesto, immettere le credenziali di GitHub.

    ![Accesso a GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. Quando richiesto, immettere il codice di autenticazione a due fattori.

    ![Autenticazione a due fattori di GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Le credenziali verranno salvate e usate per l'autenticazione di richieste future per GitHub. Questa autenticazione è necessaria una sola volta per ogni computer. 

4. Il comando clone viene eseguito e scarica una copia dei file del repository dal fork in una nuova cartella nel disco locale. Viene creata una nuova cartella all'interno della cartella corrente. Possono essere necessari alcuni minuti, in base alla dimensione del repository. È possibile esplorare la cartella per vedere la struttura dopo che è stata completata.

## <a name="configure-remote-upstream"></a>Configurare l'upstream remoto
Dopo aver clonato il repository, impostare una connessione remota di sola lettura al repository principale denominata **upstream**. L'URL di upstream verrà usata per mantenere il repository locale sincronizzato con le modifiche più recenti apportate da altri. Il comando **git remote** si usa per impostare il valore di configurazione. Il comando **fetch** viene usato per aggiornare le informazioni sul ramo dal repository upstream.

1. Se si usa **Git Credential Manager**, usare i comandi riportati di seguito. Sostituire i segnaposto \<repo\> e \<organization\>.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Visualizzare i valori configurati e verificare che gli URL siano corretti. Verificare che gli URL di **origin** puntino al fork personale. Verificare che gli URL di **upstream** puntino al repository principale, ad esempio MicrosoftDocs o Azure. 
   ```bash
   git remote -v 
   ```

   Nell'esempio è illustrato un output remoto. Un account Git fittizio denominato MyGitAccount viene configurato con un token di accesso personale per accedere al repository azure-docs:
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Se si commette un errore, è possibile rimuovere il valore remoto. Per rimuovere il valore upstream, eseguire il comando `git remote remove upstream`.

## <a name="next-steps"></a>Passaggi successivi
- Per altre informazioni sull'aggiunta e l'aggiornamento del contenuto, passare alla pagina [Flusso di lavoro per i contributi a GitHub](how-to-write-workflows-major.md).