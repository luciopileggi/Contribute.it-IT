---
title: Come contribuire a docs.microsoft.com
description: Questo articolo descrive diversi modi in cui è possibile fornire il proprio contributo per i contenuti di docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a>Come contribuire a docs.microsoft.com

Esistono diversi modi per contribuire a migliorare i contenuti disponibili in [docs.microsoft.com](https://docs.microsoft.com):

- È possibile [creare problemi](#create-issues) per consigliare nuovi articoli o migliorare quelli esistenti.
- È possibile [modificare rapidamente](#quick-edits) articoli per apportare piccole modifiche nell'editor online di GitHub.
- È possibile [rivedere le bozze di nuovi articoli](#review-new-articles) per garantire qualità e precisione tecnica.
- È possibile [creare nuovi articoli](#create-new-articles) per argomenti quando si vuole contribuire a sviluppare i contenuti.
- È possibile [aggiornare](#update-samples) o [creare](#create-samples) esempi per migliorare gli esempi di codice a supporto di concetti importanti.

In questo articolo verranno illustrati i diversi modi in cui è possibile contribuire, sarà descritto come eseguire ognuna di queste attività e saranno forniti riferimenti per accedere ad altre informazioni su ognuna delle attività.

Tutti i repository pubblici sono ospitati in [GitHub](https://wwww.GitHub.com).  Sarà necessario creare un account in GitHub per partecipare ai repository della documentazione.

Sarà inoltre necessario un editor di testo per aggiornare i documenti. È consigliabile usare [Visual Studio Code](https://www.visualstudio.com/code). È necessaria una conoscenza di base della sintassi [Markdown](https://daringfireball.net/projects/markdown/syntax).

Se si vuole aggiungere o modificare gli esempi, è necessario un ambiente di sviluppo. È consigliabile usare [Visual Studio](https://www.visualstudio.com) su PC e Mac o [Visual Studio Code](https://www.visualstudio.com/code) su tutte le piattaforme.

## <a name="create-issues"></a>Creare problemi

Se si rilevano omissioni o inesattezze in un articolo, creare un problema relativo all'articolo. Il modo più semplice per trovare il percorso corretto è fare clic sul pulsante "Edit" (Modifica) nel browser, che consente di accedere all'origine dell'articolo nel repository GitHub pubblico appropriato. Da qui è possibile recuperare l'URL per l'origine dell'articolo dalla barra degli indirizzi. Fare clic su "Crea problema" per creare un nuovo problema per l'articolo.

> [!NOTE]
> Se si rilevano problemi che possono essere corretti con piccole modifiche, ad esempio errori di digitazione o problemi di grammatica, è possibile risparmiare tempo [inviando la correzione](#quick-edits) tramite il browser per modificare l'origine.

La maggior parte dei repository pubblici contiene modelli per i nuovi problemi che offrono assistenza per fornire le informazioni necessarie per la risoluzione del problema.

È anche possibile creare nuovi problemi quando non si riesce a trovare le informazioni necessarie. Il processo è lo stesso: creare un nuovo problema in uno dei repository di documenti pubblici. Specificare quali informazioni si stavano cercando, quale attività si voleva eseguire e perché gli articoli trovati non hanno consentito di ottenere l'assistenza desiderata.

## <a name="review-new-articles"></a>Rivedere i nuovi articoli

Se si lavora con nuovi software, eventualmente in versione CTP o beta, è possibile che la creazione della documentazione sia ancora in corso nel momento in cui si esplorano le tecnologie. È possibile trovare i documenti in fase di sviluppo nei repository pubblici. Se si hanno commenti, è possibile contribuire a migliorare i documenti prima della pubblicazione.

I nuovi articoli vengono rivisti pubblicamente, usando il processo del [flusso GitHub](https://guides.github.com/introduction/flow/). Esaminare i repository di documenti e controllare le richieste pull aperte. I commenti e le revisioni su tutte le richieste pull aperte sono molto apprezzati. In questo modo è possibile pubblicare contenuti migliori fin dalla prima versione, anziché attendere feedback dopo la pubblicazione.

Siamo sempre interessati a migliorare la precisione tecnica, la chiarezza delle descrizioni e l'accuratezza grammaticale della documentazione.

## <a name="quick-edits"></a>Modifiche rapide

Le modifiche rapide consentono di apportare piccole correzioni usando l'editor basato sul browser. Se si rilevano errori di ortografia, grammaticali o nei nomi delle API, è possibile apportare la modifica e inviare una richiesta pull, invece di creare un problema.

In qualsiasi articolo, fare clic sul pulsante "Edit" (Modifica), in genere nell'angolo superiore destro della pagina, apportare le modifiche desiderate e fare clic su "Submit PR" (Invia richiesta pull) nella parte inferiore della pagina. La richiesta pull sarà esaminata e ne verrà eseguita l'unione durante la revisione quotidiana delle richieste pull.

## <a name="create-new-articles"></a>Creare nuovi articoli

Se si ha una conoscenza approfondita di determinati concetti e si vuole spiegarli ad altri utenti, è possibile creare gli articoli e inviare una richiesta pull.

La creazione di nuovi articoli richiede molto tempo: per questo i contributi dagli utenti sono molto apprezzati. Vogliamo essere coinvolti nelle prime fasi del processo, per essere certi che fin dall'inizio vengano seguiti le linee guida e lo stile appropriati. È consigliabile eseguire queste operazioni:

1. [Creare un problema](#create-issues) descrivendo gli elementi mancanti e come si potrebbe risolvere il problema.
1. Inserire un commento relativo al problema, indicando che si vorrebbe lavorare su di esso e suggerendo una struttura e un sunto per l'articolo.
1. Si riceverà una risposta con suggerimenti. Potrebbero essere inclusi collegamenti ad articoli correlati, suggerimenti per gli esempi o indicazioni su come organizzare l'articolo.
1. Una volta concordata la struttura, eseguire il fork del repository e iniziare a lavorare.
1. Nelle prime fasi del processo, aprire una richiesta pull con "[WIP]" all'inizio del titolo.
1. Uno dei collaboratori principali fornirà feedback iniziale.
1. Continuare a scrivere e menzionare (@-mention) la persona che ha esaminato la prima bozza quando si è pronti per ricevere altri commenti e suggerimenti.
1. Rimuovere "[WIP]" quando si è pronti per la revisione finale.
1. Rispondere al feedback
1. I collaboratori principali eseguiranno l'unione della richiesta pull.

Vi sono un paio di aspetti da tenere presente, in aggiunta a questo elenco. In generale, viene seguito il processo del [flusso GitHub](https://guides.github.com/introduction/flow/) per esaminare il contenuto appena possibile. In questo modo, è possibile concordare la posizione di un articolo nel sommario, i vantaggi del nuovo articolo per il lettore e l'ambito degli eventuali esempi che verranno creati. Possiamo apportare le eventuali correzioni necessarie in modo tempestivo, prima che l'autore dedichi molto tempo alla scrittura.

## <a name="update-samples"></a>Aggiornare gli esempi

Alcuni esempi potrebbero essere stati originariamente scritti diverse versioni prima, usando procedure non più consigliate. È possibile contribuire ad aggiornare questi esempi. In alternativa, si potrebbe notare che una semplice modifica del nome di una variabile consentirebbe di aumentare la chiarezza di una spiegazione.

Il codice di esempio fornito con ogni articolo fa parte di programmi che vengono compilati e spesso testati nel nostro sistema di integrazione continua.

Per apportare piccoli aggiornamenti, individuare l'origine nel repository appropriato, apportare la modifica al codice nel browser e inviare una richiesta pull. Il sistema di integrazione continua compilerà le modifiche, che al termine verranno unite alla richiesta pull.

Per modifiche su scala più ampia, eseguire il fork del repository e apportare le modifiche nel proprio ambiente di sviluppo preferito. Assicurarsi di aggiungere alcuni test per verificare che le modifiche funzionino come previsto. Inviare una richiesta pull per la revisione.

Per tutte le modifiche del codice, seguire le convenzioni del codice esistenti per il codice di esempio che si sta modificando. Gli standard di codifica dei repository di esempi rispecchiano quelli dei team dei prodotti corrispondenti. Controllare ogni repository per indicazioni specifiche.

> [!NOTE]
> Noi stessi stiamo lavorando per il rispetto di queste indicazioni. Alcuni degli esempi sono precedenti ai nostri standard correnti e non sono ancora stati aggiornati. Il nostro obiettivo è fare in modo che tutto il codice di esempio in esecuzione sia visualizzato da esempi funzionanti e testati.

## <a name="create-samples"></a>Creare gli esempi

È inoltre possibile creare nuovi esempi per illustrare concetti o scenari. Gli esempi devono essere accompagnati da un articolo che illustra le principali informazioni relative all'esempio.

Se il nuovo esempio integra un articolo esistente, aggiungere un riferimento all'esempio in tale articolo. In caso contrario, collaborare per [scrivere l'articolo](#create-new-articles) che accompagna l'esempio.

In tutti i casi, il codice di esempio segue le convenzioni di codifica usate dai team dei prodotti correlati. L'unica eccezione è il più ampio uso di variabili tipizzate in modo esplicito rispetto a quelle tipizzate in modo implicito (dichiarate con `var`) per maggiore chiarezza quando tali dichiarazioni sono incluse nell'articolo.

Seguire il processo di esempio descritto nella sezione precedente per i [nuovi articoli](#create-new-articles), in modo da consentire di rivedere il codice fin dalle prime fasi del processo di sviluppo.
