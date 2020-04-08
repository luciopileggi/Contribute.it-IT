---
title: Linee guida su voce e stile nei contributi alla documentazione .NET
description: Linee guida su voce e stile in esempi in cui le linee guida sono adottate e in altri in cui non vengono seguite.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 4108019ac50d703c6dd509eca7a6394cc1c9dc18
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/03/2020
ms.locfileid: "80625190"
---
# <a name="voice-and-tone-guidelines"></a>Linee guida su voce e stile

Moltissime persone, tra cui professionisti IT e sviluppatori, leggono i documenti Microsoft per avere informazioni su .NET e usarlo nelle proprio lavoro quotidiano. L'obiettivo è creare una documentazione utile che accompagni il lettore. Le linee guida sono pensate per questo. La guida di stile contiene le indicazioni seguenti:

In questa guida di stile sono disponibili esempi di linee guida. Questa guida è stata scritta adottando le linee guida in modo da includere esempi utili per scrivere una documentazione .NET. Sono disponibili anche esempi di confronto per poter vedere quale sarà aspetto di un articolo se non vengono adottate le linee guida consigliate.

## <a name="use-a-conversational-tone"></a>Usare uno stile colloquiale

### <a name="appropriate-style"></a>Stile appropriato

La documentazione deve avere uno stile colloquiale. Deve sembrare che si stia parlando con l'autore mentre si legge una delle esercitazioni o delle spiegazioni. L'esperienza deve risultare informale, colloquiale e informativa, come se i lettori stessero ascoltando l'autore mentre spiega loro i concetti.

### <a name="inappropriate-style"></a>Stile non appropriato

È possibile notare la differenza tra uno stile colloquiale e lo stile adottato in argomenti tecnici in cui si usa un tono più accademico. Queste risorse sono molto utili, ma gli autori hanno scritto tali articoli usando uno stile molto diverso rispetto a quello di questa documentazione. Leggendo una rivista accademica, si nota uno stile molto diverso e un modo di scrivere altrettanto differente. L'impressione è quella di leggere un argomento monotono scritto da un autore di poche parole.  

Il primo paragrafo sopra segue lo stile colloquiale consigliato, mentre il secondo uno stile più accademico. La differenza è immediatamente riconoscibile. 

## <a name="write-in-second-person"></a>Scrivere in seconda persona

### <a name="appropriate-style"></a>Stile appropriato

È consigliabile scrivere gli articoli come se si parlasse direttamente al lettore, usando quindi spesso la seconda persona. Usare la seconda persona non significa usare sempre il "tu", ma scrivere direttamente al lettore e scrivere frasi imperative, dicendo al lettore quello che deve sapere.

### <a name="inappropriate-style"></a>Stile non appropriato

Un autore può scegliere di scrivere in terza persona. In tale modello l'autore deve trovare un pronome o un nome da usare quando si rivolge al lettore. Per il lettore, lo stile in terza persona potrebbe spesso risultare meno coinvolgente e la lettura sembrare meno interessante.

Il primo paragrafo segue lo stile consigliato. Il secondo usa la terza persona. Scrivere in seconda persona. Probabilmente la lettura risulterà molto facilitata.

## <a name="use-active-voice"></a>Usare la voce attiva

Scrivere gli articoli usando la voce attiva. Significa che,se si usa la voce attiva, il soggetto della frase esegue l'azione (verbo) di tale frase, mentre se si usa la voce passiva, la frase è strutturata in modo che il soggetto della frase subisca l'azione. Mettere a confronto questi due esempi:

>Il compilatore ha trasformato il codice sorgente in un eseguibile.

>Il codice sorgente è stato trasformato in un eseguibile dal compilatore.

La prima frase usa la voce attiva. La seconda frase è stata scritta usando la voce passiva. Queste due frasi sono un altro esempio dei due stili.

È consigliabile usare la voce attiva perché risulta più leggibile. La voce passiva è più difficile da leggere.

## <a name="target-a-fifth-grade-reading-level"></a>Rivolgersi a lettori non laureati

L'ultima linea guida è importante perché molti lettori non sono inglesi. Gli articoli sono indirizzati a lettori di tutto il mondo. Considerare che il vocabolario potrebbe non essere sempre a portata di mano.

I destinatari degli articoli sono tuttavia professionisti tecnici. Si presume quindi che abbiano conoscenze nel campo della programmazione e conoscano i termini tecnici di questo settore. Programmazione orientata agli oggetti, classe, oggetto, funzione e metodo sono termini familiari. Non tutti i lettori sono tuttavia laureati in informatica. Termini come "idempotente" necessita probabilmente di una definizione qualora si voglia usarlo:

>Il metodo `Close()` è idempotente, vale a dire che può essere chiamato più volte e l'effetto sarà lo stesso come se fosse chiamato una volta.

## <a name="avoid-future-tense"></a>Evitare il tempo futuro

In alcune lingue, il concetto di futuro è diverso rispetto all'inglese. L'uso del futuro rende difficoltosa la lettura. In più, se si usa il futuro, la domanda che ovviamente sorge è "Quando accadrà?". Quindi, se si dice "Sarà importante conoscere PowerShell", il lettore si domanderà ovviamente quando sarà importante. È invece meglio scrivere "È importante conoscere PowerShell".

## <a name="what-is-it---so-what"></a>Cos'è e a cosa serve

Quando si presenta al lettore un nuovo concetto, definire tale concetto prima di spiegare perché è utile. È importante che il lettore capisca cos'è prima di capirne i vantaggi o eventualmente gli svantaggi.
