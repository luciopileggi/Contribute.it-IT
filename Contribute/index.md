---
title: Panoramica della guida per i collaboratori di Microsoft Docs
description: La guida spiega in che modo si può contribuire al sito della documentazione Microsoft docs.microsoft.com.
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 95dadff41bb31e0b34ee34f85ae47708297954f1
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "81784286"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Panoramica della guida per i collaboratori di Microsoft Docs

Questa è la Guida per i collaboratori di [docs.microsoft.com](https://docs.microsoft.com).

Diversi set di documentazione Microsoft sono open source e ospitati in GitHub. Non tutti i set di documenti sono completamente open source, ma per molti sono disponibili repository pubblici dove è possibile suggerire modifiche tramite richieste pull. Questo approccio open source semplifica e migliora la comunicazione tra i progettisti del prodotto, i team dei contenuti e i clienti, oltre a offrire altri vantaggi:

- La _pianificazione dei repository open source è visibile_ per poter ricevere commenti e suggerimenti sugli argomenti che più necessitano di documentazione.
- La _revisione dei repository open source è visibile_ per poter pubblicare il contenuto più utile già nella prima versione.
- Gli _aggiornamenti dei repository open source sono visibili_ per poter migliorare costantemente il contenuto con facilità.

L'esperienza utente in [docs.microsoft.com](https://docs.microsoft.com) viene direttamente integrata con i flussi di lavoro di [GitHub](https://github.com) così da risultare ancora più semplice. È possibile iniziare [modificando il documento visualizzato](#quick-edits-to-existing-documents), dare un contributo [revisionando i nuovi argomenti](#review-open-prs) o [segnalare problemi di qualità elevata](#create-quality-issues).

> [!IMPORTANT]
> Tutti i repository che pubblicano contenuto in docs.microsoft.com adottano il [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) (Codice di comportamento Open Source di Microsoft) o il [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct) (Codice di comportamento di .NET Foundation). Per altre informazioni, vedere [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) (Domande frequenti sul Codice di comportamento Open Source di Microsoft) oppure contattare [opencode@microsoft.com](mailto:opencode@microsoft.com) o [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) per eventuali domande o commenti.<br>
>
> Le correzioni minori o i chiarimenti inviati per la documentazione e gli esempi di codice nei repository pubblici sono coperti dalle [Condizioni per l'utilizzo di docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Per le novità o le modifiche significative viene generato un commento nella richiesta pull con la richiesta di inviare un contratto di licenza online per contributi se non si è dipendenti Microsoft. Prima che la richiesta pull venga esaminata o accettata, è necessario completare il modulo online.

## <a name="quick-edits-to-existing-documents"></a>Modifiche rapide ai documenti esistenti

Le modifiche rapide semplificano il processo di segnalazione e correzione di piccoli errori e omissioni. Nonostante l'impegno, nei documenti pubblicati _si possono riscontrare_ piccoli errori grammaticali e ortografici. Anche se è possibile segnalare problemi per informare di errori, è più facile e veloce creare una richiesta pull per risolvere il problema, quando questa opzione è disponibile.

1. Alcune pagine della documentazione consentono di modificare il contenuto direttamente nel browser. In questo caso, sarà visualizzato un pulsante **Modifica** come quello mostrato di seguito. Facendo clic sul pulsante **Edit** (o sulla versione equivalente localizzata) si accede al file di origine in GitHub. Se il pulsante **Modifica** (icona a forma di matita senza testo) non è disponibile, ciò indica che la pagina della documentazione non è disponibile per la modifica.

   ![Percorso del collegamento Modifica](./media/index/edit-article.png)

2. Fare quindi clic sull'icona a forma di matita per modificare l'articolo come illustrato. Se l'icona a forma di matita è inattiva, è necessario accedere all'account GitHub o crearne uno nuovo. 

   ![Posizione dell'icona a forma di matita](./media/index/edit-icon.png)


3. Apportare le modifiche nell'editor Web. Fare clic sulla scheda **Preview changes** (Anteprima modifiche) per controllare la formattazione della modifica.

4. Dopo avere apportato le modifiche, scorrere fino alla fine della pagina. Immettere un titolo e una descrizione per le modifiche e fare clic su **Propose file change** (Proponi modifica file), come illustrato nella figura seguente:

   ![Propose file change (Proponi modifica file)](./media/index/submit-pull-request.png)

5. Dopo aver proposto la modifica, è necessario chiedere ai proprietari del repository di eseguire il "pull" delle modifiche nel loro repository. Questa operazione viene eseguita tramite una "richiesta pull". Quando si fa clic su **Propose file change** (Proponi modifica file) nella figura precedente, dovrebbe essere visualizzata una pagina simile a quella nella figura seguente:

   ![creare una richiesta pull](media/index/create-pull-request.png)

   Fare clic su **Crea richiesta pull**, immettere un titolo (e facoltativamente una descrizione) per la richiesta pull e quindi fare di nuovo clic su **Crea richiesta pull**. (Se non si ha familiarità con GitHub, vedere la pagina delle [informazioni sulle richieste pull](https://help.github.com/en/articles/about-pull-requests).)

6. Questo è tutto. I membri del team dei contenuti esamineranno ed eseguiranno il merge della richiesta pull. Se sono state apportate modifiche più significative, è possibile ricevere alcune richieste di modifica.

L'interfaccia utente di modifica di GitHub è diversa a seconda delle autorizzazioni per il repository. Le immagini precedenti si riferiscono a collaboratori che non hanno autorizzazioni di scrittura per il repository di destinazione. GitHub crea automaticamente un fork del repository di destinazione nell'account. Se si ha l'accesso in scrittura al repository di destinazione, GitHub crea una nuovo ramo nel repository di destinazione. Il nome del ramo ha il formato **\<GitHubId\>-patch-n**, che usa l'ID GitHub e un identificatore numerico per il ramo della patch.

Le richieste pull vengono usate per tutte le modifiche, anche per i collaboratori che hanno l'accesso in scrittura. La maggior parte dei repository ha il ramo `master` protetto e quindi gli aggiornamenti devono essere inviati come richieste pull.

L'esperienza di modifica nel browser è ideale per modifiche secondarie o poco frequenti. Per pubblicare contributi più estesi oppure se si usano funzionalità Git avanzate, come la gestione dei rami o la risoluzione avanzata dei conflitti di merge, è necessario [creare una copia tramite fork del repository e lavorare in locale](how-to-write-workflows-major.md).

> [!NOTE]
> Se abilitato, è possibile modificare un articolo in **qualsiasi lingua** e, in base al tipo di modifica, si verificherà quanto segue:
> 1. Qualsiasi modifica linguistica approvata migliorerà anche il motore di traduzione automatica.
> 2. Qualsiasi modifica che cambia in modo significativo il contenuto dell'articolo verrà gestita internamente per inviare una modifica allo stesso articolo in inglese, in modo che venga localizzata in tutte le lingue in caso di approvazione.
> I miglioramenti consigliati non influiranno positivamente solo sugli articoli nella propria lingua, ma per tutte le lingue disponibili.

## <a name="review-open-prs"></a>Esaminare le richieste pull aperte

Per leggere i nuovi argomenti prima che vengano pubblicati, è possibile controllare le richieste pull attualmente aperte. Le revisioni seguono il processo del [flusso GitHub](https://guides.github.com/introduction/flow/). È possibile visualizzare gli aggiornamenti proposti o i nuovi articoli nei repository pubblici. Esaminarli e aggiungere i commenti. Esaminare i repository di documenti e controllare le richieste pull aperte per le aree a cui si è interessati. I commenti e suggerimenti della community sugli aggiornamenti proposti sono utili all'intera community.

## <a name="create-quality-issues"></a>Segnalare problemi di qualità

I documenti vengono continuamente rielaborati. La corretta formulazione dei problemi consente a Microsoft di impegnarsi maggiormente sulle priorità principali della community. Specificare il maggior numero possibile di dettagli. In questo modo la segnalazione sarà più utile. Indicare le informazioni cercate. Indicare i termini di ricerca usati. Se non si riesce a iniziare, spiegare come si vuole iniziare a esplorare una tecnologia con cui non si ha familiarità.

Molte delle pagine della documentazione di Microsoft includono una sezione **Commenti** nella parte inferiore, in cui è possibile fare clic per inviare **Commenti sul prodotto** oppure **Commenti sul contenuto** per registrare segnalazioni specifiche per l'articolo in questione.

Le segnalazioni danno avvio a una conversazione su ciò che è necessario. Il team dei contenuti risponderà a queste segnalazioni elencando le idee su ciò che è possibile aggiungere e chiederà l'opinione dell'utente. Quando viene creata una bozza, viene chiesto all'utente di [esaminare la richiesta pull](#review-open-prs).

## <a name="get-more-involved"></a>Maggiore coinvolgimento

Altri argomenti consentono di iniziare a contribuire concretamente a Microsoft Docs. Questi argomenti illustrano l'uso dei repository GitHub, gli strumenti Markdown e le estensioni usate nella piattaforma Microsoft Docs.
