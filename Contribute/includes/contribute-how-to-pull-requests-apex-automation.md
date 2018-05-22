L'automazione dei commenti consente agli utenti con autorizzazioni di lettura, ovvero quelli senza autorizzazioni di scrittura in un repository, di eseguire un'azione di scrittura tramite l'assegnazione dell'etichetta appropriata a una richiesta pull. Se si sta lavorando in un repository in cui è stata abilitata l'automazione dei commenti, usare i commenti hashtag elencati nella tabella seguente per assegnare e modificare etichette o chiudere una richiesta pull. Ogni volta che vengono proposte modifiche ai propri articoli, i dipendenti Microsoft riceveranno inoltre notifiche tramite posta elettronica per la revisione e l'approvazione delle richieste pull del repository pubblico.


| Commento hashtag | Risultato | Disponibilità repository |
| --- | --- | --- |
| #sign-off |Quando l'autore di un articolo digita il commento **#sign-off** nel flusso di commenti, viene assegnata l'etichetta **ready-to-merge**. Questa etichetta consente ai revisori nel repository di sapere quando una richiesta pull è pronta per la revisione/unione. |Pubblico e privato |
| #sign-off |Se un collaboratore che *non* è l'autore indicato tenta di approvare una richiesta pull pubblica usando il commento **#sign-off**, nella richiesta pull viene scritto un messaggio che indica che solo l'autore è autorizzato ad assegnare l'etichetta. |Pubblico |
| #hold-off |Nel caso in cui l'autore cambi idea o commetta un errore può digitare **#hold-off** nel commento di una richiesta pull per rimuovere l'etichetta **ready-to-merge**. Nel repository privato viene assegnata l'etichetta **do-not-merge**. |Pubblico e privato |
| #please-close |Nel caso in cui l'autore decida di non unire le modifiche, può digitare **#please-close** nel flusso dei commenti per chiudere la richiesta pull. |Pubblico |
