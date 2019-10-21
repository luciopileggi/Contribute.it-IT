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
# <a name="best-practices-for-pull-requests"></a>Procedure consigliate per le richieste pull

Per pubblicare modifiche al contenuto, è necessario inviare una richiesta pull dal fork personale. Ogni richiesta pull deve essere verificata prima di poter eseguire il merge.

## <a name="target-the-correct-branch"></a>Specificare il ramo corretto di destinazione

Tutte le modifiche devono essere apportate nel ramo `staging`. Le modifiche non devono mai essere destinate al ramo `live`. Per le modifiche apportate nel ramo `staging` viene eseguito il merge in `live`, quindi qualsiasi modifica apportata in `live` viene sovrascritta.

Se si invia una modifica alla documentazione che si applica solo a una versione non rilasciata di PowerShell, verificare se esiste un ramo di rilascio per tale versione. Tutte le modifiche che si applicano a una versione futura specifica devono essere destinate al ramo di rilascio. Per i rami di rilascio viene usato questo modello di nome: `release-<version>`.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>Migliorare l'efficienza della coda di richieste pull per tutti

Per la coda di richieste pull esistono due presupposti di base:

- La revisione delle richieste pull di portata minore e che contengono modifiche correlate richiede meno tempo.
- La revisione delle richieste pull più estese o che contengono modifiche non correlate richiede più tempo.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>Evitare i rami che aggiornano numerosi file

Separare gli aggiornamenti di minore entità ad articoli esistenti dai nuovi articoli o dalle riscritture estese. Lavorare a queste modifiche in rami di lavoro separati.

Le modifiche in blocco generano richieste pull con un numero elevato di file modificati. Limitare le richieste pull a un massimo di 50 file modificati. La revisione di richieste pull di grandi dimensioni è più difficile e questo tipo di richieste è più soggetto a errori.

### <a name="renaming-or-deleting-files"></a>Ridenominazione o eliminazione di file

Quando si rinominano o eliminano file, evitare di combinare queste modifiche con aggiunte o aggiornamenti del contenuto.
Gestire queste modifiche in una richiesta pull separata di cui viene eseguito il merge dopo la richiesta pull per gli aggiornamenti correlati. Ad esempio, aggiornare il file di reindirizzamento e verificare che il reindirizzamento funzioni correttamente prima di eliminare un articolo.

È necessario aggiornare tutti i file che si collegano al file rinominato. Sono inclusi gli eventuali file di sommario. È anche necessario aggiungere voci di reindirizzamento nel file di reindirizzamento master (`.openpublishing.redirection.json`) nella radice del repository.

## <a name="docs-pr-validation-service"></a>Servizio di convalida PR Docs

Il servizio di convalida PR Docs è un'applicazione GitHub che esegue regole di convalida sui file in un PR.

Il comportamento sarà il seguente:

1. Viene inviato un PR.
1. Nel commento di GitHub che indica lo stato del PR, verrà visualizzato lo stato dei "controlli" abilitati sul repository. Si noti che in questo esempio, sono abilitati due controlli, "Commit Validation" e "OpenPublishing.Build":

   ![alcuni controlli non sono riusciti](media/powershell-pull-requests/validation-failed.png)

   Build può essere eseguito anche se la convalida del commit non riesce.

1. Per altre informazioni, fare clic su **Dettagli**.
1. Nella pagina Dettagli verranno visualizzati tutti i controlli di convalida non riusciti con informazioni su come risolvere i problemi.
1. Quando la convalida ha esito positivo, alla richiesta pull viene aggiunto il commento seguente:

   ![convalida di compilazione](media/powershell-pull-requests/build-validation.png)

Se si è un collaboratore esterno (non Microsoft), non si ha accesso ai report di compilazione dettagliati o ai collegamenti di anteprima.

### <a name="build-warnings"></a>Avvisi di compilazione

Normalmente è necessario correggere tutti gli errori di compilazione, gli avvisi e i suggerimenti. Tuttavia, esistono alcuni avvisi che possono essere ignorati.

È possibile ignorare gli avvisi seguenti:

- > Impossibile trovare il nome del servizio per `<version>/<modulepath>/About/About.md`

- > I metadati con i nomi seguenti non possono essere impostati nell'intestazione Yaml o come metadati a livello di file in docfx.json o come metadati globali in docfx.json: `locale`. Vengono generati dalla piattaforma Docs, quindi i valori impostati in queste 3 posizioni verranno ignorati. Rimuoverli da tutte le 3 posizioni per risolvere l'avviso.
