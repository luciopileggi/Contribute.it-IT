---
title: Configurare un repository Git locale
description: Questo articolo contiene indicazioni su come creare il repository Git locale e contribuire alla documentazione, incluso il processo di creazione di fork e cloni.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.openlocfilehash: 2ad0de552d481e2460ca0f56570181e33d0a6608
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238990"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="78ddf-103">Configurare un repository Git locale per la documentazione</span><span class="sxs-lookup"><span data-stu-id="78ddf-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="78ddf-104">In questo articolo vengono descritti i passaggi per impostare un repository Git nel computer locale, allo scopo di contribuire alla documentazione Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78ddf-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="78ddf-105">I collaboratori possono usare un repository clonato in locale per aggiungere nuovi articoli, apportare modifiche di rilievo ad articoli esistenti o modificare la grafica.</span><span class="sxs-lookup"><span data-stu-id="78ddf-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="78ddf-106">Eseguire le attività di installazione seguenti, da effettuare una sola volta, per iniziare a contribuire:</span><span class="sxs-lookup"><span data-stu-id="78ddf-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="78ddf-107">Determinare il repository appropriato</span><span class="sxs-lookup"><span data-stu-id="78ddf-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="78ddf-108">Eseguire il fork del repository nell'account GitHub</span><span class="sxs-lookup"><span data-stu-id="78ddf-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="78ddf-109">Scegliere una cartella locale per i file clonati</span><span class="sxs-lookup"><span data-stu-id="78ddf-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="78ddf-110">Clonare il repository nel computer locale</span><span class="sxs-lookup"><span data-stu-id="78ddf-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="78ddf-111">Configurare il valore del repository remoto upstream</span><span class="sxs-lookup"><span data-stu-id="78ddf-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78ddf-112">Se si stanno apportando solo piccole modifiche a un articolo, *non* è necessario completare i passaggi descritti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="78ddf-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="78ddf-113">È possibile proseguire direttamente con il [flusso di lavoro delle modifiche rapide](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="78ddf-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="78ddf-114">Panoramica</span><span class="sxs-lookup"><span data-stu-id="78ddf-114">Overview</span></span>

<span data-ttu-id="78ddf-115">Per contribuire al sito della documentazione Microsoft, è possibile creare e modificare file Markdown in locale clonando il repository della documentazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="78ddf-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="78ddf-116">Microsoft richiede di eseguire il fork del repository appropriato nel proprio account Github, in modo da disporre di autorizzazioni di lettura/scrittura per archiviare le modifiche proposte.</span><span class="sxs-lookup"><span data-stu-id="78ddf-116">Microsoft requires you to fork the appropriate repository into your own github account, so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="78ddf-117">Sarà quindi possibile usare richieste pull per unire le modifiche nel repository condiviso centrale in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="78ddf-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![Triangolo GitHub](./media/git-and-github-initial-setup.png)

<span data-ttu-id="78ddf-119">Se non si ha familiarità con GitHub, guardare il video seguente per una panoramica concettuale del processo di creazione di fork e cloni:</span><span class="sxs-lookup"><span data-stu-id="78ddf-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="78ddf-120">Determinare il repository</span><span class="sxs-lookup"><span data-stu-id="78ddf-120">Determine the repository</span></span>

<span data-ttu-id="78ddf-121">La documentazione ospitata in [docs.microsoft.com](https://docs.microsoft.com) si trova in diversi repository su [github.com](https://www.github.com).</span><span class="sxs-lookup"><span data-stu-id="78ddf-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="78ddf-122">Se non si è certi del repository da usare, visitare l'articolo su docs.microsoft.com con il Web browser.</span><span class="sxs-lookup"><span data-stu-id="78ddf-122">If you are unsure of which repository to use, then visit the article on docs.microsoft.com using your web browser.</span></span> <span data-ttu-id="78ddf-123">Selezionare il collegamento **Modifica** (icona a forma di matita) nell'angolo superiore destro dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="78ddf-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Fare clic su Modifica per determinare il repository e il percorso del file.](media/index/edit-article.png)

2. <span data-ttu-id="78ddf-125">Tale collegamento consente di visualizzare la posizione in github.com del file Markdown corrispondente nel repository appropriato.</span><span class="sxs-lookup"><span data-stu-id="78ddf-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="78ddf-126">Esaminare l'URL per visualizzare il nome del repository.</span><span class="sxs-lookup"><span data-stu-id="78ddf-126">Note the URL to view the repository name.</span></span>

   ![Esaminare l'URL per determinare il percorso del repository.](media/public-repo.png)

   <span data-ttu-id="78ddf-128">Ad esempio, i repository seguenti sono disponibili per i contributi pubblici:</span><span class="sxs-lookup"><span data-stu-id="78ddf-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="78ddf-129">Documentazione di Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="78ddf-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="78ddf-130">Documentazione di SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="78ddf-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="78ddf-131">Documentazione di Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="78ddf-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="78ddf-132">Documentazione di .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="78ddf-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="78ddf-133">Documentazione di Azure .NET SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="78ddf-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="78ddf-134">Creare una copia tramite fork del repository</span><span class="sxs-lookup"><span data-stu-id="78ddf-134">Fork the repository</span></span>
<span data-ttu-id="78ddf-135">Selezionando il repository appropriato, creare un fork del repository nel proprio account GitHub usando il sito Web GitHub.</span><span class="sxs-lookup"><span data-stu-id="78ddf-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="78ddf-136">Un fork personale è richiesto poiché tutti i repository principali della documentazione sono accessibili in sola lettura e questo significa che non è possibile modificare direttamente il contenuto nei repository.</span><span class="sxs-lookup"><span data-stu-id="78ddf-136">A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories.</span></span> <span data-ttu-id="78ddf-137">Per apportare modifiche, è necessario inviare una [richiesta pull](git-github-fundamentals.md#pull-requests) dal fork al repository principale.</span><span class="sxs-lookup"><span data-stu-id="78ddf-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="78ddf-138">Per facilitare questo processo, è prima necessario avere una copia del repository, accessibile in scrittura.</span><span class="sxs-lookup"><span data-stu-id="78ddf-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="78ddf-139">Un *fork* di GitHub serve a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="78ddf-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="78ddf-140">Passare alla pagina di GitHub del repository principale e fare clic sul pulsante **Fork** in alto a destra.</span><span class="sxs-lookup"><span data-stu-id="78ddf-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Esempio di profilo GitHub](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="78ddf-142">Se richiesto, selezionare il riquadro del proprio account GitHub come destinazione per la creazione del fork.</span><span class="sxs-lookup"><span data-stu-id="78ddf-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="78ddf-143">Con questo prompt viene creata una copia del repository nell'account GitHub personale, nota come fork.</span><span class="sxs-lookup"><span data-stu-id="78ddf-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="78ddf-144">Scegliere una cartella locale</span><span class="sxs-lookup"><span data-stu-id="78ddf-144">Choose a local folder</span></span>
<span data-ttu-id="78ddf-145">Fare in modo che una cartella locale contenga una copia del repository localmente.</span><span class="sxs-lookup"><span data-stu-id="78ddf-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="78ddf-146">Alcuni repository possono essere di grandi dimensioni, ad esempio fino a 5 GB per azure-docs.</span><span class="sxs-lookup"><span data-stu-id="78ddf-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="78ddf-147">Scegliere una posizione in cui sia disponibile spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="78ddf-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="78ddf-148">Scegliere un nome di cartella facile da ricordare e digitare.</span><span class="sxs-lookup"><span data-stu-id="78ddf-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="78ddf-149">Considerare ad esempio una cartella radice `C:\docs\` o creare una cartella nella directory del profilo utente `~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="78ddf-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="78ddf-150">Evitare di scegliere un percorso cartella locale nidificato all'interno di un altro percorso cartella di repository Git.</span><span class="sxs-lookup"><span data-stu-id="78ddf-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="78ddf-151">Benché sia accettabile archiviare le cartelle Git clonate l'una accanto all'altra, annidare le cartelle Git l'una nell'altra causa errori per il rilevamento file.</span><span class="sxs-lookup"><span data-stu-id="78ddf-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="78ddf-152">Avviare Git Bash</span><span class="sxs-lookup"><span data-stu-id="78ddf-152">Launch Git Bash</span></span>

   ![Avviare Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="78ddf-154">Il percorso predefinito in cui viene avviato Git Bash normalmente è la home directory (~) o `/c/users/<Windows-user-account>/` nel sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="78ddf-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="78ddf-155">Per determinare la directory corrente, digitare `pwd` al prompt $.</span><span class="sxs-lookup"><span data-stu-id="78ddf-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="78ddf-156">Cambiare directory (cd) selezionando la cartella creata per ospitare il repository localmente.</span><span class="sxs-lookup"><span data-stu-id="78ddf-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="78ddf-157">Si noti che in Git Bash per i percorsi cartella viene usata la convenzione di Linux, ovvero le barre anziché le barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="78ddf-157">Note that Git Bash uses Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="78ddf-158">Ad esempio, `cd /c/docs/ ` o `cd ~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="78ddf-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="78ddf-159">Creare un clone locale</span><span class="sxs-lookup"><span data-stu-id="78ddf-159">Create a local clone</span></span>

<span data-ttu-id="78ddf-160">Usando Git Bash, preparare l'esecuzione del comando **clone** per eseguire il pull di una copia di un repository (il fork) nel dispositivo presente nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="78ddf-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="78ddf-161">Eseguire l'autenticazione con Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="78ddf-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="78ddf-162">Se è stata installata la versione più recente di Git per Windows accettando l'installazione predefinita, Git Credential Manager viene abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="78ddf-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="78ddf-163">Git Credential Manager semplifica notevolmente l'autenticazione, perché non occorre richiamare il token di accesso personale per ristabilire connessioni autenticate o remote con GitHub.</span><span class="sxs-lookup"><span data-stu-id="78ddf-163">Git Credential Manager makes authentication much easier, because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="78ddf-164">Eseguire il comando **clone** specificando il nome del repository.</span><span class="sxs-lookup"><span data-stu-id="78ddf-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="78ddf-165">Con la clonazione, il repository di cui è stato creato un fork viene scaricato (clonato) nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="78ddf-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="78ddf-166">È possibile ottenere l'URL di GitHub per il fork per il comando di clonazione dal pulsante **Clone or download** (Clona o scarica) nell'interfaccia utente di GitHub:</span><span class="sxs-lookup"><span data-stu-id="78ddf-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Clone or download (Clona o scarica)](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="78ddf-168">Assicurarsi di specificare il percorso del *proprio fork* durante il processo di clonazione e non quello del repository principale da cui è stato creato il fork.</span><span class="sxs-lookup"><span data-stu-id="78ddf-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="78ddf-169">In caso contrario non è possibile collaborare alle modifiche.</span><span class="sxs-lookup"><span data-stu-id="78ddf-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="78ddf-170">Viene fatto riferimento al fork attraverso l'account utente di GitHub, ad esempio `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="78ddf-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="78ddf-171">Il comando clone deve essere simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="78ddf-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="78ddf-172">Quando richiesto, immettere le credenziali di GitHub.</span><span class="sxs-lookup"><span data-stu-id="78ddf-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![Accesso a GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="78ddf-174">Quando richiesto, immettere il codice di autenticazione a due fattori.</span><span class="sxs-lookup"><span data-stu-id="78ddf-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![Autenticazione a due fattori di GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="78ddf-176">Le credenziali verranno salvate e usate per l'autenticazione di richieste future per GitHub.</span><span class="sxs-lookup"><span data-stu-id="78ddf-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="78ddf-177">Questa autenticazione è necessaria una sola volta per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="78ddf-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="78ddf-178">Il comando clone viene eseguito e scarica una copia dei file del repository dal fork in una nuova cartella nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="78ddf-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="78ddf-179">Viene creata una nuova cartella all'interno della cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="78ddf-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="78ddf-180">Possono essere necessari alcuni minuti, in base alla dimensione del repository.</span><span class="sxs-lookup"><span data-stu-id="78ddf-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="78ddf-181">È possibile esplorare la cartella per vedere la struttura dopo che è stata completata.</span><span class="sxs-lookup"><span data-stu-id="78ddf-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="78ddf-182">Configurare l'upstream remoto</span><span class="sxs-lookup"><span data-stu-id="78ddf-182">Configure remote upstream</span></span>
<span data-ttu-id="78ddf-183">Dopo aver clonato il repository, impostare una connessione remota di sola lettura al repository principale denominata **upstream**.</span><span class="sxs-lookup"><span data-stu-id="78ddf-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="78ddf-184">L'URL di upstream verrà usata per mantenere il repository locale sincronizzato con le modifiche più recenti apportate da altri.</span><span class="sxs-lookup"><span data-stu-id="78ddf-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="78ddf-185">Il comando **git remote** si usa per impostare il valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="78ddf-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="78ddf-186">Il comando **fetch** viene usato per aggiornare le informazioni sul ramo dal repository upstream.</span><span class="sxs-lookup"><span data-stu-id="78ddf-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="78ddf-187">Se si usa **Git Credential Manager**, usare i comandi riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="78ddf-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="78ddf-188">Sostituire i segnaposto \<repo\> e \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="78ddf-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="78ddf-189">Visualizzare i valori configurati e verificare che gli URL siano corretti.</span><span class="sxs-lookup"><span data-stu-id="78ddf-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="78ddf-190">Verificare che gli URL di **origin** puntino al fork personale.</span><span class="sxs-lookup"><span data-stu-id="78ddf-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="78ddf-191">Verificare che gli URL di **upstream** puntino al repository principale, ad esempio MicrosoftDocs o Azure.</span><span class="sxs-lookup"><span data-stu-id="78ddf-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="78ddf-192">Nell'esempio è illustrato un output remoto.</span><span class="sxs-lookup"><span data-stu-id="78ddf-192">Example remote output is shown.</span></span> <span data-ttu-id="78ddf-193">Un account Git fittizio denominato MyGitAccount viene configurato con un token di accesso personale per accedere al repository azure-docs:</span><span class="sxs-lookup"><span data-stu-id="78ddf-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="78ddf-194">Se si commette un errore, è possibile rimuovere il valore remoto.</span><span class="sxs-lookup"><span data-stu-id="78ddf-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="78ddf-195">Per rimuovere il valore upstream, eseguire il comando `git remote remove upstream`.</span><span class="sxs-lookup"><span data-stu-id="78ddf-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="78ddf-196">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="78ddf-196">Next steps</span></span>
- <span data-ttu-id="78ddf-197">Per altre informazioni sull'aggiunta e l'aggiornamento del contenuto, passare alla pagina [Flusso di lavoro per i contributi a GitHub](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="78ddf-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>