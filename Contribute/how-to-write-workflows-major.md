---
title: Flusso di lavoro per i contributi a GitHub per le modifiche di rilievo o di lunga durata
description: Questo articolo illustra come usare il flusso di lavoro per i contributi "di rilievo" per gli articoli di docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 997f313e94e4858f37501736c1ec0be2fa8fd552
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188232"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Flusso di lavoro per i contributi a GitHub per le modifiche di rilievo o di lunga durata

> [!IMPORTANT]
> Tutti i repository che pubblicano contenuto in docs.microsoft.com adottano il [Codice di comportamento Open Source di Microsoft](https://opensource.microsoft.com/codeofconduct/) o il [Codice di comportamento di .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Per altre informazioni, vedere [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) (Domande frequenti sul Codice di comportamento Open Source di Microsoft) oppure contattare [opencode@microsoft.com](mailto:opencode@microsoft.com) o [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) per eventuali domande o commenti.<br>
>
> Le correzioni minori o i chiarimenti inviati per la documentazione e gli esempi di codice nei repository pubblici sono coperti dalle [Condizioni per l'utilizzo di docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Per le novità o le modifiche significative verrà generato un commento nella richiesta pull con la richiesta di inviare un contratto di licenza online per i contributi (Contribution License Agreement, CLA) se non si è dipendenti Microsoft. Sarà necessario compilare il modulo online, prima che la richiesta pull possa essere unita.

## <a name="overview"></a>Panoramica

Questo flusso di lavoro è appropriato per gli autori di contributi che devono apportare modifiche di rilievo o che forniscono contributi di frequente per un repository. I collaboratori frequenti propongono in genere modifiche continuative (di lunga durata) sottoposte a vari cicli di compilazione, convalida e gestione temporanea oppure con un'elaborazione che richiede più giorni prima dell'approvazione e unione della richiesta pull.

Alcuni esempi di questo tipo di contributi includono:

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologia

Prima di iniziare, è opportuno rivedere alcuni dei termini di Git/GitHub usati in questo flusso di lavoro. Non è importante comprenderli appieno in questa fase. Basta ricordarsi che verranno illustrati in maggiore dettaglio e che è possibile fare riferimento a questa sezione nel caso occorra verificare una definizione.

| Nome | Descrizione |
|-----------|-------------|
|fork|Normalmente usato come sostantivo per fare riferimento a una copia di un repository principale di GitHub. In pratica, un fork è semplicemente un altro repository, ma è speciale perché GitHub mantiene un collegamento con il repository principale/padre. A volte, questo termine descrive un'operazione, ad esempio in "è necessario prima di tutto creare un fork del repository.".|
|remoto|Connessione denominata a un repository remoto, ad esempio il remoto "origin" o "upstream". Git la indica come remota perché è usata per fare riferimento a un repository ospitato in un altro computer. In questo flusso di lavoro, un remoto è sempre un repository di GitHub.|
|origin|Nome assegnato alla connessione tra il repository locale e il repository da cui è stato clonato. In questo flusso di lavoro, origin indica la connessione al fork. Questo termine viene a volte usato per fare riferimento in modo abbreviato al repository origin, come in "Ricordarsi di eseguire il push delle modifiche nell'origine."|
|upstream|Come nel caso del remoto origin, upstream è una connessione denominata a un altro repository. In questo flusso di lavoro, upstream rappresenta la connessione tra il repository locale e il repository principale, da cui è stato creato il fork. Questo termine viene a volte usato per fare riferimento in modo abbreviato al repository upstream, come in "Ricordarsi di effettuare il pull delle modifiche dall'upstream".|

## <a name="workflow"></a>Flusso di lavoro

>[!IMPORTANT]
> Se non è già stato fatto, è necessario completare i passaggi della sezione di [configurazione](get-started-setup-github.md). Questa sezione descrive come configurare l'account GitHub, installare Git Bash e il Markdown editor, creare un fork e configurare il repository locale. Se non si ha familiarità con i concetti principali di Git e GitHub, come repository o ramo, leggere prima di tutto [Concetti fondamentali di Git e GitHub](git-github-fundamentals.md).

In questo flusso di lavoro, le modifiche seguono un ciclo ripetitivo. A partire dal repository locale nel dispositivo dell'utente, il flusso torna verso il fork di GitHub, poi nel repository principale di GitHub, quindi di nuovo in locale quando si incorporano le modifiche di altri collaboratori.

### <a name="use-github-flow"></a>Usare il flusso GitHub

Si ricorderà da [Concetti di base per Git e GitHub](git-github-fundamentals.md#git) che un repository Git contiene un ramo master, oltre a eventuali rami aggiuntivi per il lavoro in corso non integrati in master. Ogni volta che si introduce un set di modifiche correlate dal punto di vista logico, è buona norma creare un *ramo di lavoro* per gestire le modifiche in tutte le fasi del flusso di lavoro. Viene definito ramo di lavoro perché si tratta di uno spazio di lavoro per l'iterazione e la rifinitura delle modifiche, fino a quando non sono pronte per l'integrazione nel ramo master.

La possibilità di isolare modifiche correlate in un ramo specifico consente di controllare e introdurre tali modifiche in modo indipendente, destinandole a una fase di rilascio specifica nel ciclo di pubblicazione. In contesti reali, a seconda del tipo di lavoro svolto, è facile ritrovarsi con vari rami di lavoro nel repository a lavorare su più rami contemporaneamente, ognuno dei quali rappresenta un progetto diverso.

>[!TIP]
>*Non* è buona norma apportare modifiche nel ramo master. Si immagini di usare il ramo master per introdurre un set di modifiche per un rilascio di funzionalità programmato. Dopo aver completato le modifiche si aspetta il momento previsto per il rilascio. Nel frattempo arriva una richiesta urgente di correzione, quindi si apporta la modifica necessaria in un file nel ramo master e la si pubblica. In questo esempio, vengono pubblicate inavvertitamente sia la correzione *che* le modifiche che erano in attesa della data specifica di rilascio.

Di seguito viene descritta la procedura per creare un nuovo ramo di lavoro nel repository locale, per raccogliere le modifiche proposte. Se è stato configurato Git Bash (vedere [Installare gli strumenti di creazione del contenuto](get-started-setup-tools.md)), è possibile creare un nuovo ramo ed eseguire il "checkout" del ramo con un unico comando dall'interno del repository clonato:

````
git checkout -b "branchname"
````

Poiché ogni client Git presenta differenze, consultare la documentazione relativa al client in uso. È possibile visualizzare una panoramica del processo relativo al [flusso GitHub](https://guides.github.com/introduction/flow/) nella Guida di GitHub.

## <a name="making-your-changes"></a>Apportare le modifiche

Ora che è disponibile una copia ("clone") del repository Microsoft e che è stato creato un ramo, è possibile apportare tutte le modifiche che si ritiene possano essere utili per la community usando qualsiasi editor di testo o Markdown, come descritto nella pagina [Installare gli strumenti di creazione del contenuto](get-started-setup-tools.md).  È possibile salvare le modifiche localmente senza che sia necessario inviarle a Microsoft fino a quando non si è pronti.

## <a name="saving-changes-to-your-repository"></a>Salvataggio delle modifiche nel repository

Prima di inviare le modifiche all'autore, è necessario salvarle nel repository GitHub.  Anche se tutti gli strumenti sono diversi, anche in questo caso è possibile eseguire l'operazione con pochi passaggi usando la riga di comando di Git Bash.

Prima di tutto, dall'interno del repository, è necessario _preparare per il commit_ tutte le modifiche apportate.  Questa operazione può essere eseguita con il comando seguente:

````
git add --all
````

Successivamente, è necessario eseguire il commit delle modifiche salvate nel repository locale.  Questa operazione può essere eseguita in Git Bash con il comando seguente:

````
git commit -m "Short Description of Changes Made"
````

Infine, dato che il ramo è stato creato nel computer locale, è necessario fare in modo che il fork nell'account GitHub.com ne sia a conoscenza.  Se si usa Git Bash, è possibile eseguire questa operazione con il comando seguente:

````
git push --set-upstream origin <branchname>
````

Il processo è completo.  Il codice è ora disponibile nel repository GitHub e pronto per la creazione di una richiesta pull.  

>[!TIP]
> Anche se le modifiche diventano visibili nell'account GitHub personale quando si effettua il push, non è obbligatorio inviare immediatamente una richiesta pull.  Se si vuole interrompere il lavoro e tornare in un secondo momento per mettere a punto altri dettagli, è possibile farlo.

Se è necessario apportare una correzione nel materiale inviato,  non è un problema.  È sufficiente apportare le modifiche nello stesso ramo e quindi eseguire di nuovo il commit e il push (non è necessario impostare il server upstream nei push successivi dello stesso ramo).

Se risulta necessario apportare altre modifiche non correlate a queste  è sufficiente tornare al ramo master ed eseguire il checkout di un altro ramo nuovo usando Git Bash, come indicato di seguito:

````
git checkout master
git checkout -b "branchname"
````

A questo punto ci si trova in un nuovo ramo ed è possibile fornire il proprio contributo ancora una volta.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Passaggi successivi

Questo è tutto. È stato completato l'intero flusso di lavoro per fornire il proprio contributo per i contenuti di docs.microsoft.com.

- Per altre informazioni su argomenti come la sintassi per Markdown e le estensioni Markdown, continuare con l'articolo [Informazioni di base per la scrittura](how-to-write-use-markdown.md).
