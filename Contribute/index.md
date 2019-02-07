---
title: Panoramica della guida per i collaboratori di Microsoft Docs
description: La guida spiega in che modo si può contribuire al sito della documentazione Microsoft docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 04/17/2018
ms.openlocfilehash: 4a9a7573a62cfc7d5187b90de7e1fe147825273e
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712856"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Panoramica della guida per i collaboratori di Microsoft Docs

Questa è la Guida per i collaboratori di [docs.microsoft.com](https://docs.microsoft.com).

Diversi set di documentazione sono open source e disponibili su GitHub. Sempre più team a Microsoft stanno adottando regolarmente questo modello. Anche i set di documenti non completamente open source hanno repository pubblici dove è possibile eseguire richieste pull. Ciò permette di semplificare e migliorare le comunicazioni tra gli sviluppatori, i team dei contenuti e i clienti. Operare in modo visibile offre diversi vantaggi:

- La pianificazione dei repository open source è visibile per poter ricevere commenti e suggerimenti sugli argomenti che più necessitano di documentazione.
- La revisione dei repository open source è visibile per poter pubblicare il contenuto più utile già nella prima versione.
- Gli aggiornamenti dei repository open source sono visibili per poter migliorare costantemente il contenuto con facilità.

L'esperienza utente in [docs.microsoft.com](https://docs.microsoft.com) viene direttamente integrata con i flussi di lavoro di [GitHub](https://github.com) così da risultare ancora più semplice. È possibile iniziare [modificando il documento visualizzato](#quick-edits-to-existing-documents), dare un contributo [revisionando i nuovi argomenti](#review-open-prs) o [creare problemi di qualità elevata](#create-quality-issues).

> [!IMPORTANT]
> Tutti i repository che pubblicano contenuto in docs.microsoft.com adottano il [Codice di comportamento Open Source di Microsoft](https://opensource.microsoft.com/codeofconduct/) o il [Codice di comportamento di .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Per altre informazioni, vedere [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) (Domande frequenti sul Codice di comportamento Open Source di Microsoft) oppure contattare [opencode@microsoft.com](mailto:opencode@microsoft.com) o [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) per eventuali domande o commenti.<br>
>
> Le correzioni minori o i chiarimenti inviati per la documentazione e gli esempi di codice nei repository pubblici sono coperti dalle [Condizioni per l'utilizzo di docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Per le novità o le modifiche significative viene generato un commento nella richiesta pull con la richiesta di inviare un contratto di licenza online per contributi se non si è dipendenti Microsoft. Prima che la richiesta pull venga esaminata o accettata, è necessario completare il modulo online.

## <a name="quick-edits-to-existing-documents"></a>Modifiche rapide ai documenti esistenti

Le modifiche rapide semplificano il processo di segnalazione e correzione di piccoli errori e omissioni. Nonostante l'impegno, nei documenti pubblicati si possono riscontrare piccoli errori grammaticali e ortografici. Anche se è possibile creare problemi per segnalare gli errori, è più facile e veloce creare una richiesta pull per risolvere il problema. In quasi tutti gli articoli è presente un pulsante di modifica, come illustrato nella figura seguente. Facendo clic sul pulsante **Edit** (o sulla versione equivalente localizzata) si accede al file di origine in GitHub.

![Percorso del collegamento Modifica](./media/index/edit-article.png)

Fare quindi clic sull'icona a forma di matita illustrata nella figura seguente per modificare l'articolo.

![Posizione dell'icona a forma di matita](./media/index/edit-icon.png)

> [!NOTE]
> Se l'icona a forma di matita è inattiva, è necessario accedere all'account GitHub o crearne uno nuovo.

Apportare le modifiche nell'editor Web. È possibile fare clic sulla scheda **Preview changes** (Anteprima modifiche) per controllare la formattazione della modifica.

Dopo avere apportato le modifiche, scorrere fino alla fine della pagina. Immettere un titolo e una descrizione per la richiesta pull e fare clic su **Propose file change** (Proponi modifica file), come illustrato nella figura seguente:

![Proposta della modifica](./media/index/submit-pull-request.png)

Dopo aver proposto la modifica, è necessario chiedere ai proprietari del repository di eseguire il "pull" delle modifiche nel loro repository. Questa operazione viene eseguita tramite una "richiesta pull". Quando si fa clic su **Propose file change** (Proponi modifica file) nella figura precedente, dovrebbe essere visualizzata una pagina simile a quella nella figura seguente:

![creare una richiesta pull](media/index/create-pull-request.png)

Fare clic su **Crea richiesta pull**, immettere un titolo (e facoltativamente una descrizione) per la richiesta pull e quindi fare di nuovo clic su **Crea richiesta pull**.

Questo è tutto. I membri del team dei contenuti esamineranno e uniranno la richiesta pull. Se sono state apportate modifiche più significative, è possibile ricevere alcune richieste di modifica.

L'interfaccia utente di modifica di GitHub è diversa a seconda delle autorizzazioni per il repository. Le immagini precedenti si riferiscono a collaboratori che non hanno autorizzazioni di scrittura per il repository di destinazione. GitHub crea automaticamente un fork del repository di destinazione nell'account. Se si ha l'accesso in scrittura al repository di destinazione, GitHub crea una nuovo ramo nel repository di destinazione. Il nome del ramo ha il formato **\<GitHubId\>-patch-n**, che usa l'ID GitHub e un identificatore numerico per il ramo della patch.

Le richieste pull vengono usate per tutte le modifiche, anche per i collaboratori che hanno l'accesso in scrittura. La maggior parte dei repository ha il ramo `master` protetto e quindi gli aggiornamenti devono essere inviati come richieste pull.

L'esperienza di modifica nel browser è ideale per modifiche secondarie o poco frequenti. Per pubblicare contributi più estesi oppure se si usano funzionalità Git avanzate, come la gestione dei rami o la risoluzione avanzata dei conflitti di merge, è necessario [creare una copia tramite fork del repository e lavorare in locale](how-to-write-workflows-major.md).

> [!NOTE]
> Se abilitato, è possibile modificare un articolo in **qualsiasi lingua** e, in base al tipo di modifica, si verificherà quanto segue:
> 1. qualsiasi modifica linguistica approvata migliorerà anche il motore di traduzione automatica
> 2. qualsiasi modifica che cambia in modo significativo il contenuto dell'articolo verrà gestita internamente per inviare un modifica allo stesso articolo in inglese, in modo che venga localizzata in tutte le lingue in caso di approvazione.
> I miglioramenti consigliati, quindi, non influiranno positivamente solo sugli articoli nella propria lingua, ma in tutte le lingue disponibili.

## <a name="review-open-prs"></a>Esaminare le richieste pull aperte

Per leggere i nuovi argomenti prima che vengano pubblicati, è possibile controllare le richieste pull attualmente aperte. Le revisioni seguono il processo del [flusso GitHub](https://guides.github.com/introduction/flow/). È possibile visualizzare gli aggiornamenti proposti o i nuovi articoli nei repository pubblici. Esaminarli e aggiungere i commenti. Esaminare i repository di documenti e controllare le richieste pull aperte per le aree a cui si è interessati. I commenti e suggerimenti della community sugli aggiornamenti proposti sono utili all'intera community.

## <a name="create-quality-issues"></a>Creare problemi di qualità

I documenti vengono continuamente rielaborati. La corretta formulazione dei problemi consente a Microsoft di impegnarsi maggiormente sulle priorità principali della community. Specificare il maggior numero possibile di dettagli. In questo modo il problema sarà più utile. Indicare le informazioni cercate. Indicare i termini di ricerca usati. Se non si riesce a iniziare, spiegare come si vuole iniziare a esplorare una tecnologia con cui non si ha familiarità.

I problemi danno avvio a una conversazione su ciò che è necessario. Il team dei contenuti risponderà a questi problemi elencando le idee su ciò che è possibile aggiungere e chiederà l'opinione dell'utente. Quando viene creata una bozza, viene chiesto all'utente di [esaminare la richiesta pull](#review-open-prs).

## <a name="get-more-involved"></a>Maggiore coinvolgimento

Altri argomenti consentono di iniziare a contribuire concretamente a Microsoft Docs. Questi argomenti illustrano l'uso dei repository GitHub, gli strumenti Markdown e le estensioni usate nella piattaforma Microsoft Docs.
