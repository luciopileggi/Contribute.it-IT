## <a name="pull-request-processing"></a>Elaborazione delle richieste pull

Nella sezione precedente è stato illustrato il processo di invio delle modifiche proposte raggruppandole in una nuova richiesta pull che viene quindi aggiunta alla coda delle richieste pull del repository di destinazione. Una richiesta pull attiva il modello per la collaborazione di GitHub, richiedendo il pull delle modifiche dal ramo di lavoro e la loro unione in un altro ramo. Nella maggior parte dei casi l'unione avviene nel ramo predefinito/master nel repository principale.

### <a name="validation"></a>Convalida

Prima di poter essere unita al ramo di destinazione, la richiesta pull potrebbe dover superare uno o più processi di convalida. I processi possono variare a seconda della portata delle modifiche proposte e delle regole del repository di destinazione. I passaggi successivi all'invio di una richiesta pull possono essere i seguenti:

- **Test dell'unione**: in primo luogo viene eseguito un test dell'unione di base di GitHub, per verificare se le modifiche proposte nel ramo sono in conflitto con il ramo di destinazione. Se il test ha esito negativo per la richiesta pull, prima di poter continuare l'elaborazione è necessario riconciliare il contenuto che causa i conflitti di unione.
- **Contratto di licenza per contributi**: se si inviano contributi a un repository pubblico e non si è un dipendente Microsoft, a seconda della portata delle modifiche proposte potrebbe essere richiesto di completare un breve contratto di licenza per contributi in occasione del primo invio di una richiesta pull al repository in questione. Una volta inoltrato il contratto, la richiesta pull viene elaborata.
- **Etichettatura**: alla richiesta pull vengono applicate automaticamente etichette, usate per indicarne lo stato durante i vari passaggi del flusso di lavoro di convalida. Ad esempio alle nuove richieste pull può essere assegnata automaticamente l'etichetta "do-not-merge", a indicare che per la richiesta devono ancora essere completati i passaggi di convalida, revisione e approvazione.
- **Convalida e compilazione**: una serie di controlli automatici verificano se le modifiche superano i test di convalida. I test di convalida possono restituire avvisi o errori, rendendo necessaria la modifica di uno o più file nella richiesta pull prima di poter procedere con l'unione. I risultati dei test di convalida vengono aggiunti come commenti nella richiesta pull per consentire la consultazione e possono essere inviati all'autore tramite posta elettronica.
- **Gestione temporanea**: dopo il completamento corretto della convalida e della compilazione, le pagine di articoli interessate dalle modifiche vengono distribuite automaticamente in un ambiente di gestione temporanea per la revisione. Gli URL di anteprima appaiono in un commento della richiesta pull.
- **Unione automatica**: la richiesta pull può essere unita automaticamente se supera i test di convalida e soddisfa determinati criteri. In tal caso non è necessario eseguire altre operazioni.

### <a name="review-and-sign-off"></a>Revisione e approvazione

Dopo il completamento di tutti i passaggi di elaborazione della richiesta pull, è necessario rivedere i risultati (commenti, URL di anteprima e così via) per stabilire se sono necessarie ulteriori modifiche ai file prima dell'approvazione per l'unione. Se la richiesta pull è stata verificata da un revisore di richieste pull, il revisore può aggiungere commenti se rileva domande/problemi in sospeso da risolvere prima dell'unione.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Quando la richiesta pull è corretta e approvata le modifiche vengono unite nel ramo padre e la richiesta viene chiusa.

### <a name="publishing"></a>Pubblicazione

Ricordare che la richiesta pull deve essere unita da un revisore di richieste pull prima che le modifiche possano essere incluse nella successiva operazione di pubblicazione pianificata. Le richieste pull vengono in genere riviste/unite nell'ordine di invio. Se la richiesta pull deve essere unita per una scadenza di pubblicazione specifica è consigliabile collaborare con il revisore della richiesta pull con il dovuto anticipo, per assicurarsi che l'unione avvenga prima della pubblicazione.

Dopo l'approvazione e l'unione, i contributi inviati vengono prelevati dal processo di pubblicazione di docs.microsoft.com. I tempi di pubblicazione possono variare a seconda del team che gestisce il repository di destinazione dei contributi. Gli articoli pubblicati nei percorsi seguenti vengono in genere distribuiti alle 10.30 e alle 15.30 circa (ora del Pacifico) dal lunedì al venerdì:

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Per la visualizzazione online degli articoli dopo la pubblicazione possono essere richiesti fino a 45 minuti. Dopo la pubblicazione dell'articolo è possibile verificare che le modifiche siano disponibili nell'URL appropriato: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
