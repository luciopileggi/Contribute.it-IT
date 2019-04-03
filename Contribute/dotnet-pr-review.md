---
title: Processo di revisione delle richieste pull nella documentazione relativa a .NET
description: Nella documentazione relativa a .NET i webhook di fusione di richieste pull non sono abilitati. Questo articolo descrive il processo di richiesta pull per questi repository
ms.date: 01/04/2019
ms.openlocfilehash: f710e330e31e56887d43030290d5aa6a5c62961b
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653598"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>Processo di revisione delle richieste pull per i repository di documenti su .NET

In molti repository non sono abilitati i webhook di fusione delle richieste pull, che uniscono automaticamente le richieste pull secondarie. Questo articolo descrive il processo di revisione delle richieste pull per questi repository. Il processo di revisione delle richieste pull è stato progettato con questi obiettivi:

1. Pubblicare contenuti di alta qualità dal team, dai membri del team di prodotto e dai membri della community.
1. Fornire commenti e suggerimenti tempestivi e utilizzabili agli autori in modo coerente.
1. Agevolare gli scambi tra autori e revisori.

I processi continuano a evolversi man mano che i team adottano nuove soluzioni e di pari passo con la maturazione della piattaforma.

## <a name="reviewers"></a>Revisori

Uno dei membri del team del contenuto rivede ogni richiesta pull. I membri del team del contenuto possono richiedere una revisione a membri del team di prodotto specifico per verificare l'accuratezza tecnica. Il team del contenuto usa la funzionalità di proprietà del codice di GitHub per richiedere automaticamente le revisioni ai membri del team del contenuto. Nell'ambito di questo processo, un revisore può contrassegnare altri membri del team per la revisione delle richieste pull interne. I membri del team vedono le revisioni richieste dai membri del team e dai membri della community nella stessa coda.

Anche i membri della community possono rivedere le richieste pull e fornire commenti e suggerimenti. Tuttavia, almeno un membro del team del contenuto principale deve approvare qualsiasi richiesta pull prima del merge.

## <a name="review-process"></a>Processo di revisione

La revisione segue uno di tre percorsi in base alla richiesta pull:

- **Richieste pull di piccole dimensioni** - Le richieste pull di piccole dimensioni sono singole correzioni di bug: errori di digitazione, collegamenti interrotti, modifiche minime al codice o modifiche simili.
- **Contributi di rilievo** - Questi contributi sono modifiche significative a un articolo esistente, nuovi articoli o modifiche a vari articoli.
- **Lavori in corso** - Gli autori possono richiedere una revisione durante il lavoro aprendo una richiesta pull con il tag "[WIP]" nel titolo. "WIP" è l'acronimo di "Work in Progress" (Lavori in corso). 

Il processo usato dal bot del contratto di licenza per i collaboratori rappresenta una buona indicazione per distinguere tra contributi "piccoli" ed "estesi". Le richieste pull che non richiedono la firma del contratto di licenza per i contributi sono probabilmente "piccole". Le richieste pull che richiedono la firma del contratto di licenza per i contributi sono probabilmente "grandi".

### <a name="small-prs"></a>Richieste pull piccole

Le modifiche nelle richieste pull piccole vengono riviste per verificarne l'accuratezza e controllate usando la compilazione nel sito di revisione. Essendo piccole, queste richieste pull non implicano la revisione dell'intero articolo. 

I revisori potrebbero notare altre piccole modifiche che consentono di migliorare un articolo. Se anche queste modifiche sono di piccola entità, verranno suggerite come commenti di revisione. Se le modifiche suggerite richiedono una revisione più estesa, aprire un problema ed esaminarle in un secondo momento. 

### <a name="larger-changes"></a>Modifiche più estese

Le richieste pull più estese sono sottoposte a una revisione più accurata. Vengono controllati tutti gli aspetti seguenti:

- Il codice di esempio deve essere incluso nella richiesta pull, nell'origine e come file ZIP scaricabile.
- Il codice di esempio viene compilato ed eseguito correttamente.
- L'articolo descrive in modo chiaro gli obiettivi per il lettore e questi obiettivi sono soddisfatti.
- L'articolo rispetta le [linee guida di stile e grammatica](dotnet-style-guide.md) e segue i [principi relativi a tono e forma](dotnet-voice-tone.md).
- Tutti i collegamenti vengono risolti correttamente.

I membri del team del contenuto eseguiranno la revisione della richiesta pull e invieranno la revisione con commenti. Se sono richieste solo modifiche di minore entità, i membri del team possono "approvare" la richiesta pull con i commenti e suggerimenti. L'autore può a questo punto implementare commenti e suggerimenti, quindi eseguire il merge della richiesta pull. Per la maggior parte delle revisioni saranno richieste modifiche e dopo la loro implementazione, il revisore ripeterà la revisione.

Se le modifiche richiedono una revisione tecnica, il revisore del team del contenuto richiedere una revisione al membro del team del prodotto appropriato.

### <a name="review-wip-pull-requests"></a>Revisione di richieste pull "WIP"

I nuovi autori possono richiedere commenti e suggerimenti nelle fasi iniziali del processo, aprendo una richiesta pull con l'etichetta "[WIP]" nel titolo. Possono usare un commento per richiedere una revisione anticipata.

Queste revisioni anticipate non sono accurate come una revisione completa di richiesta pull. Il team del contenuto aggiungerà commenti, ma non "approverà" o "richiederà modifiche" usando la funzionalità di revisione di GitHub. Le revisioni anticipate si concentrano su alcuni aspetti generali dell'articolo: struttura, contenuto complessivo ed esempi. Queste revisioni non includono un controllo grammaticale completo e il controllo della correttezza dei collegamenti.

## <a name="respond-to-reviews"></a>Rispondere alle revisioni

L'autore aggiorna la richiesta pull per rispondere ai commenti contrassegnando ogni commento implementato con la reazione "+ 1" per indicare che è stato accolto. Se l'autore non è d'accordo con un commento o implementa le modifiche richieste diversamente, l'autore aggiunge un commento per spiegare le modifiche.

L'autore usa @-mentions per menzionare il revisore originale in un commento per richiedere una nuova revisione. 

## <a name="response-time-expectations"></a>Tempi di risposta previsti

I membri del team del contenuto impiegano in genere meno di due giorni lavorativi per completare la revisione di nuove richieste pull. Se la revisione richiede più tempo, uno dei membri del team aggiungerà un commento per confermare la presa in carico della richiesta pull e fissare i tempi previsti.

Dopo l'invio di una revisione, gli autori devono tentare di rispondere ai commenti entro una settimana. È possibile che i volontari non riescano a rispettare questi tempi a causa di altri impegni. In questi casi, i membri del team chiederanno all'autore della community se aggiornerà la richiesta pull. Se la risposta è negativa, un membro del team aggiorna la richiesta pull e ne esegue il merge per conto dell'autore.
