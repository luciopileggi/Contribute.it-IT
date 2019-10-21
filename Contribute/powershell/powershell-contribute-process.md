---
title: Processo per contribuire ai repository della documentazione di PowerShell
description: Questo articolo offre una breve introduzione al processo per inviare contributi per i repository della documentazione di PowerShell. Vengono presentati i repository usati, il processo per l'organizzazione del contenuto e i criteri per la gestione degli esempi di codice e di altri asset.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290197"
---
# <a name="process-for-contributing-to-powershell-docs"></a>Processo per contribuire alla documentazione di PowerShell

I contributi della community alla documentazione sono molto apprezzati. L'elenco seguente include alcune regole di massima da tenere presenti per l'invio di contributi per la documentazione di PowerShell:

- **NON** inviare a sorpresa richieste pull di grandi dimensioni. Registrare invece un problema e avviare una discussione, in modo da poter concordare una direzione prima di investire molto tempo.
- **SEGUIRE** queste istruzioni e le guide di stile per il [codice](powershell-style-code.md) e le [informazioni di riferimento](powershell-style-reference.md).
- **USARE** il file [modello](powershell-style-basic-markdown.md) come punto di partenza per il lavoro.
- **CREARE** un ramo separato nel fork personale prima di iniziare a lavorare agli articoli.
- **SEGUIRE** il [flusso di lavoro GitHub Flow](../how-to-write-workflows-major.md).
- **PUBBLICARE AGGIORNAMENTI** di frequente tramite blog e tweet (o altri strumenti) sui contributi.

Seguendo queste linee guida si garantisce un'esperienza migliore per tutti.

## <a name="make-a-contribution-to-powershell-docs"></a>Creare un contributo per la documentazione di PowerShell

È possibile scegliere tra i [problemi](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose) esistenti.
A seconda dei propri interessi e del livello di impegno, i contributi rientrano nelle categorie seguenti:

- **Modifiche di minore entità**. Per le modifiche di minore entità, vedere le istruzioni per la modifica in GitHub nella [home page](../index.md#quick-edits-to-existing-documents) della guida per i collaboratori. Le modifiche di minore entità includono:

  - Correzione di errori di digitazione e ortografia
  - Miglioramento della grammatica o della formattazione
  - Modifiche tecniche o fattuali minime

- **Maintenance (Manutenzione)** . Questa categoria include contributi piuttosto semplici, come la correzione di collegamenti interrotti o non corretti, l'aggiunta di esempi di codice mancanti o la correzione di problemi limitati del contenuto. Questi problemi possono a volte interessare numerosi file. In tal caso, è opportuno fare sapere a Microsoft su cosa si vorrebbe lavorare prima di iniziare. Aggiungere un commento al problema per segnalare che si sta lavorando al problema.

- **Content updates (Aggiornamenti del contenuto)** . Considerata la vastità del set di documenti, i contenuti diventano facilmente obsoleti e richiedono una revisione. Inoltre, per svariati motivi, certi contenuti sono duplicati o persino triplicati. L'aggiornamento del contenuto comporta assicurarsi che i singoli argomenti siano aggiornati oppure rivedere il contenuto in un'area funzionale per eliminare duplicati e assicurarsi che tutto il contenuto univoco sia mantenuto nel set di documentazione più ridotto.

- **New content authoring (Creazione di nuovo contenuto)** . Se si è interessati a creare un nuovo argomento, questi problemi elencano gli argomenti che Microsoft vorrebbe aggiungere al set di documenti. Prima di iniziare a lavorare a un argomento, però, farlo sapere a Microsoft. Se si è interessati a scrivere un argomento non presente in questo elenco, aprire un problema.

Dopo aver selezionato un'attività su cui lavorare, seguire la [guida introduttiva](../get-started-setup-github.md) per creare un account GitHub e configurare l'ambiente.

### <a name="making-large-changes"></a>Apportare modifiche estese

**Passaggio 1:** se si è interessati alla scrittura di nuovo contenuto o a una revisione consistente di contenuto esistente, aprire un problema per descrivere le proprie intenzioni.

**Passaggio 2:** creare una copia tramite fork del repository `MicrosoftDocs/PowerShell-Docs` e creare un ramo di lavoro per le modifiche.

**Passaggio 3:** apportare le modifiche nel nuovo ramo.

Se si tratta di un nuovo argomento, usare il modello nella [guida di stile](powershell-style-basic-markdown.md) come punto di partenza. La guida di stile contiene le linee guida per la scrittura e illustra i metadati necessari per ogni articolo.

Passare alla cartella corrispondente alla posizione del sommario stabilita per l'articolo nel passaggio 1.
Tale cartella contiene i file Markdown per tutti gli articoli in quella sezione. Se necessario, creare una nuova cartella in cui posizionare i file per il contenuto. L'articolo principale per tale sezione è denominato *index.md*.
Per le immagini e altre risorse statiche, creare una sottocartella denominata **media** all'interno della cartella che contiene l'articolo, se non esiste già. All'interno della cartella **media** creare una sottocartella con il nome dell'articolo (ad eccezione del file index).

Assicurarsi di usare la sintassi Markdown corretta. Per istruzioni dettagliate ed esempi, leggere la [guida di stile](powershell-style-basic-markdown.md).

**Struttura di esempio**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**Passaggio 4:** Inviare una richiesta pull (PR) dal ramo di lavoro al ramo di *staging*.

In genere, una richiesta pull deve riguardare un problema alla volta. e può includere modifiche per uno o più file. Per la risoluzione di più problemi in file diversi, sono preferibili richieste pull separate.

Se la richiesta pull risolve un problema esistente, aggiungere la parola chiave `Fixes #Issue_Number` nel messaggio di commit o nella descrizione della richiesta pull. In questo modo, il problema viene chiuso automaticamente al momento del merge della richiesta pull. Per altre informazioni, vedere [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (Chiusura dei problemi tramite messaggi di commit).

Il team di PowerShell effettua la revisione della richiesta pull e avvisa nel caso siano necessarie altre modifiche per l'approvazione.

**Passaggio 5:** apportare eventuali modifiche necessarie al ramo in base a quanto concordato con il team.

Dopo l'approvazione, i responsabili della manutenzione effettuano il merge della richiesta pull nel ramo di *staging*. Microsoft esegue periodicamente il push di tutti i commit dal ramo di *staging* al ramo *live*. Dopo la pubblicazione, il contributo sarà visibile nel [sito della documentazione di PowerShell](https://docs.microsoft.com/PowerShell/). Vengono in genere pubblicati nuovi contenuti due o tre volte durante la settimana lavorativa.

## <a name="contributor-license-agreement"></a>Contratto di licenza per i collaboratori

Prima del merge della richiesta pull, è necessario sottoscrivere il [Contratto di licenza per contributi (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs). Questa operazione viene richiesta una sola volta per i contributi alla documentazione.

Non è necessario sottoscrivere il contratto anticipatamente. È possibile clonare il ramo, creare una copia tramite fork e inviare la richiesta pull come di consueto.
Al momento della creazione, la richiesta pull viene classificata da un bot CLA. Se la modifica è minima (ad esempio, la correzione di un errore ortografico) alla richiesta pull viene assegnata l'etichetta `cla-not-required`. In caso contrario, viene classificata come `cla-required`. Dopo la sottoscrizione del contratto di licenza per contributi, tutte le richieste pull correnti e future vengono classificate come `cla-signed`.
