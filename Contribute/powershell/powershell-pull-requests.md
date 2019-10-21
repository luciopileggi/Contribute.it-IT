---
title: Invio di una richiesta pull
description: Questo articolo descrive il processo di richiesta pull e le procedure consigliate per garantire che sia possibile completare il merge del contributo.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290082"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="ea769-103">Procedure consigliate per le richieste pull</span><span class="sxs-lookup"><span data-stu-id="ea769-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="ea769-104">Per pubblicare modifiche al contenuto, è necessario inviare una richiesta pull dal fork personale.</span><span class="sxs-lookup"><span data-stu-id="ea769-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="ea769-105">Ogni richiesta pull deve essere verificata prima di poter eseguire il merge.</span><span class="sxs-lookup"><span data-stu-id="ea769-105">Every pull request has to be reviewed before it can merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="ea769-106">Specificare il ramo corretto di destinazione</span><span class="sxs-lookup"><span data-stu-id="ea769-106">Target the correct branch</span></span>

<span data-ttu-id="ea769-107">Tutte le modifiche devono essere apportate nel ramo `staging`.</span><span class="sxs-lookup"><span data-stu-id="ea769-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="ea769-108">Le modifiche non devono mai essere destinate al ramo `live`.</span><span class="sxs-lookup"><span data-stu-id="ea769-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="ea769-109">Per le modifiche apportate nel ramo `staging` viene eseguito il merge in `live`, quindi qualsiasi modifica apportata in `live` viene sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="ea769-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="ea769-110">Se si invia una modifica alla documentazione che si applica solo a una versione non rilasciata di PowerShell, verificare se esiste un ramo di rilascio per tale versione.</span><span class="sxs-lookup"><span data-stu-id="ea769-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="ea769-111">Tutte le modifiche che si applicano a una versione futura specifica devono essere destinate al ramo di rilascio.</span><span class="sxs-lookup"><span data-stu-id="ea769-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="ea769-112">Per i rami di rilascio viene usato questo modello di nome: `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="ea769-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="ea769-113">Migliorare l'efficienza della coda di richieste pull per tutti</span><span class="sxs-lookup"><span data-stu-id="ea769-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="ea769-114">Per la coda di richieste pull esistono due presupposti di base:</span><span class="sxs-lookup"><span data-stu-id="ea769-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="ea769-115">La revisione delle richieste pull di portata minore e che contengono modifiche correlate richiede meno tempo.</span><span class="sxs-lookup"><span data-stu-id="ea769-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="ea769-116">La revisione delle richieste pull più estese o che contengono modifiche non correlate richiede più tempo.</span><span class="sxs-lookup"><span data-stu-id="ea769-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="ea769-117">Evitare i rami che aggiornano numerosi file</span><span class="sxs-lookup"><span data-stu-id="ea769-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="ea769-118">Separare gli aggiornamenti di minore entità ad articoli esistenti dai nuovi articoli o dalle riscritture estese.</span><span class="sxs-lookup"><span data-stu-id="ea769-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="ea769-119">Lavorare a queste modifiche in rami di lavoro separati.</span><span class="sxs-lookup"><span data-stu-id="ea769-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="ea769-120">Le modifiche in blocco generano richieste pull con un numero elevato di file modificati.</span><span class="sxs-lookup"><span data-stu-id="ea769-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="ea769-121">Limitare le richieste pull a un massimo di 50 file modificati.</span><span class="sxs-lookup"><span data-stu-id="ea769-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="ea769-122">La revisione di richieste pull di grandi dimensioni è più difficile e questo tipo di richieste è più soggetto a errori.</span><span class="sxs-lookup"><span data-stu-id="ea769-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="ea769-123">Ridenominazione o eliminazione di file</span><span class="sxs-lookup"><span data-stu-id="ea769-123">Renaming or deleting files</span></span>

<span data-ttu-id="ea769-124">Quando si rinominano o eliminano file, evitare di combinare queste modifiche con aggiunte o aggiornamenti del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea769-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="ea769-125">Gestire queste modifiche in una richiesta pull separata di cui viene eseguito il merge dopo la richiesta pull per gli aggiornamenti correlati.</span><span class="sxs-lookup"><span data-stu-id="ea769-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="ea769-126">Ad esempio, aggiornare il file di reindirizzamento e verificare che il reindirizzamento funzioni correttamente prima di eliminare un articolo.</span><span class="sxs-lookup"><span data-stu-id="ea769-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="ea769-127">È necessario aggiornare tutti i file che si collegano al file rinominato.</span><span class="sxs-lookup"><span data-stu-id="ea769-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="ea769-128">Sono inclusi gli eventuali file di sommario.</span><span class="sxs-lookup"><span data-stu-id="ea769-128">This includes any TOC files.</span></span> <span data-ttu-id="ea769-129">È anche necessario aggiungere voci di reindirizzamento nel file di reindirizzamento master (`.openpublishing.redirection.json`) nella radice del repository.</span><span class="sxs-lookup"><span data-stu-id="ea769-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="ea769-130">Servizio di convalida PR Docs</span><span class="sxs-lookup"><span data-stu-id="ea769-130">Docs PR validation service</span></span>

<span data-ttu-id="ea769-131">Il servizio di convalida PR Docs è un'applicazione GitHub che esegue regole di convalida sui file in un PR.</span><span class="sxs-lookup"><span data-stu-id="ea769-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="ea769-132">Il comportamento sarà il seguente:</span><span class="sxs-lookup"><span data-stu-id="ea769-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="ea769-133">Viene inviato un PR.</span><span class="sxs-lookup"><span data-stu-id="ea769-133">You submit a PR.</span></span>
1. <span data-ttu-id="ea769-134">Nel commento di GitHub che indica lo stato del PR, verrà visualizzato lo stato dei "controlli" abilitati sul repository.</span><span class="sxs-lookup"><span data-stu-id="ea769-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="ea769-135">Si noti che in questo esempio, sono abilitati due controlli, "Commit Validation" e "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="ea769-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![alcuni controlli non sono riusciti](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="ea769-137">Build può essere eseguito anche se la convalida del commit non riesce.</span><span class="sxs-lookup"><span data-stu-id="ea769-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="ea769-138">Per altre informazioni, fare clic su **Dettagli**.</span><span class="sxs-lookup"><span data-stu-id="ea769-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="ea769-139">Nella pagina Dettagli verranno visualizzati tutti i controlli di convalida non riusciti con informazioni su come risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="ea769-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="ea769-140">Quando la convalida ha esito positivo, alla richiesta pull viene aggiunto il commento seguente:</span><span class="sxs-lookup"><span data-stu-id="ea769-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![convalida di compilazione](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="ea769-142">Se si è un collaboratore esterno (non Microsoft), non si ha accesso ai report di compilazione dettagliati o ai collegamenti di anteprima.</span><span class="sxs-lookup"><span data-stu-id="ea769-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="ea769-143">Avvisi di compilazione</span><span class="sxs-lookup"><span data-stu-id="ea769-143">Build warnings</span></span>

<span data-ttu-id="ea769-144">Normalmente è necessario correggere tutti gli errori di compilazione, gli avvisi e i suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="ea769-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="ea769-145">Tuttavia, esistono alcuni avvisi che possono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="ea769-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="ea769-146">È possibile ignorare gli avvisi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea769-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="ea769-147">Impossibile trovare il nome del servizio per `<version>/<modulepath>/About/About.md`</span><span class="sxs-lookup"><span data-stu-id="ea769-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="ea769-148">I metadati con i nomi seguenti non possono essere impostati nell'intestazione Yaml o come metadati a livello di file in docfx.json o come metadati globali in docfx.json: `locale`.</span><span class="sxs-lookup"><span data-stu-id="ea769-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="ea769-149">Vengono generati dalla piattaforma Docs, quindi i valori impostati in queste 3 posizioni verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="ea769-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="ea769-150">Rimuoverli da tutte le 3 posizioni per risolvere l'avviso.</span><span class="sxs-lookup"><span data-stu-id="ea769-150">Please remove them from all 3 places to resolve the warning.</span></span>
