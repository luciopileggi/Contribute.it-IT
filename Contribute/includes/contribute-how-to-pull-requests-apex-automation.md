---
ms.openlocfilehash: b64e8dd4c62ca05b6e04ef404ebf98a618d0171e
ms.sourcegitcommit: 2563918217ba0760a4f3877af2272a0a4b2c3052
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/30/2019
ms.locfileid: "66391464"
---
L'automazione dei commenti consente agli utenti con autorizzazioni di lettura, ovvero quelli senza autorizzazioni di scrittura in un repository, di eseguire un'azione di scrittura tramite l'assegnazione dell'etichetta appropriata a una richiesta pull. Se si sta lavorando in un repository in cui è stata abilitata l'automazione dei commenti, usare i commenti hashtag elencati nella tabella seguente per assegnare e modificare etichette o chiudere una richiesta pull. Ogni volta che vengono proposte modifiche ai propri articoli, i dipendenti Microsoft riceveranno inoltre notifiche tramite posta elettronica per la revisione e l'approvazione delle richieste pull del repository pubblico.

| Commento hashtag | Risultato | Disponibilità repository |
| --- | --- | --- |
| `#sign-off` |Quando l'autore di un articolo digita il commento `#sign-off` nel flusso di commenti, viene assegnata l'etichetta **ready-to-merge**. Questa etichetta consente ai revisori nel repository di sapere quando una richiesta pull è pronta per la revisione/unione. <br/><br/> Se un collaboratore che *non* è l'autore indicato tenta di approvare una richiesta pull di un repository pubblico usando il commento `#sign-off`, nella richiesta pull viene scritto un messaggio indicante che solo l'autore è autorizzato ad assegnare l'etichetta. |Pubblico e privato |
| `#hold-off` |Se l'autore cambia idea o commette un errore, può digitare `#hold-off` nel commento di una richiesta pull per rimuovere l'etichetta **ready-to-merge**. Nel repository privato viene assegnata l'etichetta **do-not-merge**. |Pubblico e privato |
| `#please-close` |Se l'autore decide di non unire le modifiche, può digitare `#please-close` nel flusso dei commenti per chiudere la richiesta pull. |Pubblico |
