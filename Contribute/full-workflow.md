---
title: Flusso di lavoro per i contributi a GitHub per modifiche di rilievo o di lunga durata
description: Questo articolo illustra come usare il flusso di lavoro per i contributi "di rilievo" per gli articoli di docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: a43e9a8274c430b1eeed796fc74085c2248f1c14
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Flusso di lavoro per i contributi a GitHub per modifiche di rilievo o di lunga durata

> [!IMPORTANT]
> Tutti i repository che pubblicano contenuto in docs.microsoft.com adottano il [Codice di comportamento Open Source di Microsoft](https://opensource.microsoft.com/codeofconduct/) o il [Codice di comportamento di .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Per altre informazioni, vedere [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) (Domande frequenti sul Codice di comportamento Open Source di Microsoft) oppure contattare [opencode@microsoft.com](mailto:opencode@microsoft.com) o [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) per eventuali domande o commenti.<br>
>
> Le correzioni minori o i chiarimenti inviati per la documentazione e gli esempi di codice nei repository pubblici sono coperti dalle [Condizioni per l'utilizzo di docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Per le novità o le modifiche significative verrà generato un commento nella richiesta pull con la richiesta di inviare un contratto di licenza online per i contributi (Contribution License Agreement, CLA) se non si è dipendenti Microsoft. Sarà necessario compilare il modulo online, prima che la richiesta pull possa essere unita.

## <a name="overview"></a>Panoramica

Questo flusso di lavoro è appropriato per gli autori di contributi che devono apportare modifiche di rilievo o che forniscono contributi di frequente per un repository. I collaboratori frequenti propongono in genere modifiche continuative (di lunga durata) sottoposte a vari cicli di compilazione, convalida e gestione temporanea oppure con un'elaborazione che richiede più giorni prima dell'approvazione e unione della richiesta pull.

Per i dipendenti Microsoft che lavorano a progetti che usano sia repository pubblici che privati, è anche importante che questi tipi di contributi vengano effettuati nel repository privato per il quale sono disponibili servizi di compilazione, convalida e gestione temporanea OPS integrati.

Alcuni esempi di questo tipo di contributi includono:

[!INCLUDE[contribute-how-to-write-workflows-major-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologia

Prima di iniziare, è opportuno rivedere alcuni dei termini di Git/GitHub usati in questo flusso di lavoro. Non è importante comprenderli appieno in questa fase. È sufficiente ricordarsi che verranno illustrati in maggiore dettaglio e che è possibile fare riferimento a questa sezione nel caso occorra verificare una definizione.

| Nome | Descrizione |
|-----------|-------------|
|fork|Normalmente usato come sostantivo per fare riferimento a una copia di un repository principale di GitHub. In pratica, un fork è semplicemente un altro repository, ma è speciale perché GitHub mantiene un collegamento con il repository principale/padre. A volte questo termine descrive un'operazione, come in "è necessario prima di tutto creare un fork del repository".|
|remoto|Connessione denominata a un repository remoto, ad esempio il remoto "origin" o "upstream". Git indica questi repository come remoti perché vengono usati per fare riferimento a un repository ospitato in un altro computer. In questo flusso di lavoro, un remoto è sempre un repository di GitHub.|
|origin|Nome assegnato alla connessione tra il repository locale e il repository da cui è stato clonato. In questo flusso di lavoro, origin indica la connessione al fork. Questo termine viene a volte usato per fare riferimento in modo abbreviato al repository origin, come in "Ricordarsi di eseguire il push delle modifiche nell'origine".|
|upstream|Come nel caso del remoto origin, upstream è una connessione denominata a un altro repository. In questo flusso di lavoro, upstream rappresenta la connessione tra il repository locale e il repository principale, da cui è stato creato il fork. Questo termine viene a volte usato per fare riferimento in modo abbreviato al repository upstream, come in "Ricordarsi di effettuare il pull delle modifiche dall'upstream".|

## <a name="workflow"></a>Flusso di lavoro

>[!IMPORTANT]
> Se non è già stato fatto, è necessario completare i passaggi della sezione di [configurazione](get-started-setup-github.md). Questa sezione descrive come configurare l'account GitHub, installare Git Bash e il Markdown editor, creare un fork e configurare il repository locale. Se non si ha familiarità con i concetti principali di Git e GitHub, come repository o ramo, leggere prima di tutto [Concetti di base per Git e GitHub](git-github-fundamentals.md).

In questo flusso di lavoro, le modifiche seguono un ciclo ripetitivo. A partire dal repository locale nel dispositivo dell'utente, il flusso torna verso il fork di GitHub, poi nel repository principale di GitHub, quindi di nuovo in locale quando si incorporano le modifiche di altri collaboratori.

### <a name="use-github-flow"></a>Usare il flusso GitHub

Si ricorderà da [Concetti di base per Git e GitHub](git-github-fundamentals.md#git) che un repository Git contiene un ramo master, oltre a eventuali rami aggiuntivi per il lavoro in corso non integrati in master. Ogni volta che si introduce un set di modifiche correlate dal punto di vista logico, è buona norma creare un *ramo di lavoro* per gestire le modifiche in tutte le fasi del flusso di lavoro. Viene definito ramo di lavoro perché si tratta di uno spazio di lavoro per l'iterazione e la rifinitura delle modifiche, fino a quando non sono pronte per l'integrazione nel ramo master.

La possibilità di isolare modifiche correlate in un ramo specifico consente di controllare e introdurre tali modifiche in modo indipendente, destinandole a una fase di rilascio specifica nel ciclo di pubblicazione. In contesti reali, a seconda del tipo di lavoro svolto, è facile ritrovarsi con vari rami di lavoro nel repository a lavorare su più rami contemporaneamente, ognuno dei quali rappresenta un progetto diverso.

>[!TIP]
>*Non* è buona norma apportare modifiche nel ramo master. Si immagini di usare il ramo master per introdurre un set di modifiche per un rilascio di funzionalità programmato. Dopo aver completato le modifiche si aspetta il momento previsto per il rilascio. Nel frattempo arriva una richiesta urgente di correzione, quindi si apporta la modifica necessaria in un file nel ramo master e la si pubblica. In questo esempio, vengono pubblicate inavvertitamente sia la correzione *che* le modifiche che erano in attesa della data specifica di rilascio.

Di seguito viene descritta la procedura per creare un nuovo ramo di lavoro nel repository locale, per raccogliere le modifiche proposte. Poiché ogni client Git presenta differenze, consultare la documentazione relativa al client in uso. È possibile visualizzare una panoramica del processo relativo al [flusso GitHub](https://guides.github.com/introduction/flow/) nella Guida di GitHub.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Passaggi successivi
Questo è tutto. Il proprio contributo è stato inserito nei contenuti di docs.microsoft.com.

- Per altre informazioni su argomenti come la sintassi per Markdown e le estensioni Markdown, continuare con la sezione Informazioni di base per la scrittura.
