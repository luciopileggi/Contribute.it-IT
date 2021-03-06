---
title: Apportare contribuiti ai repository della documentazione .NET
description: Questo articolo descrive come fornire contributi per gli articoli e gli esempi di codice disponibili nei repository che costituiscono la documentazione .NET.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 948c96a63754566fc73e54c722998739984977d6
ms.sourcegitcommit: 43a4f52ab827a7cf4609cc592483595efde3ceae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2020
ms.locfileid: "83203054"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a>Informazioni su come apportare contributi ai repository della documentazione .NET

Grazie per l'interesse rivolto ai contribuiti nella documentazione .NET.

Questo documento illustra il processo per apportare contribuiti agli articoli e agli esempi di codice ospitati nel [sito della documentazione .NET](https://docs.microsoft.com/dotnet). Possono essere semplici contribuiti, ad esempio la correzione di errori di battitura oppure contribuiti più complessi, come nuovi articoli.

Il sito della documentazione .NET è costituito da più repository:

- [Articoli concettuali .NET](https://github.com/dotnet/docs)
- [Esempi di codice e frammenti di codice](https://github.com/dotnet/samples)
- [Informazioni di riferimento sulle API .NET Standard, .NET Core, .NET Framework](https://github.com/dotnet/dotnet-api-docs)
- [Informazioni di riferimento su .NET Compiler Platform SDK](https://github.com/dotnet/roslyn-api-docs)
- [Informazioni di riferimento sulle ML.NET](https://github.com/dotnet/ml-api-docs)

I problemi relativi a tutti questi repository sono monitorati nel repository [dotnet/docs](https://github.com/dotnet/docs/issues).

## <a name="guidelines-for-contributions"></a>Linee guida per i contributi

I contributi della community alla documentazione sono molto apprezzati. L'elenco seguente include alcune regole di massima da tenere presenti per l'invio di contributi per la documentazione di .NET:

- **NON** inviare a sorpresa richieste pull di grandi dimensioni. Registrare invece un problema e avviare una discussione, in modo da poter concordare una direzione prima di investire molto tempo.
- **SEGUIRE** queste istruzioni e le linee guida per [voce e tono](dotnet-voice-tone.md).
- **USARE** il file [modello](dotnet-style-guide.md) come punto di partenza per il lavoro.
- **CREARE** un ramo separato nel fork personale prima di iniziare a lavorare agli articoli.
- **SEGUIRE** il [flusso di lavoro GitHub Flow](https://guides.github.com/introduction/flow/).
- **PUBBLICARE AGGIORNAMENTI** di frequente tramite blog e tweet (o altri strumenti) sui contributi.

Seguendo queste linee guida si garantirà un'esperienza migliore per tutti.

## <a name="make-a-contribution-to-net-docs"></a>Creare un contributo per la documentazione di .NET

**Passaggio 1:** ignorare questo passaggio per le modifiche di piccola entità. Se si è interessati alla scrittura di nuovo contenuto o a una revisione consistente di contenuto esistente, aprire un [problema](https://github.com/dotnet/docs/issues) per descrivere le proprie intenzioni.

Il contenuto all'interno della cartella **docs** è organizzato in sezioni rispecchiate nel sommario. Definire la posizione dell'argomento nel sommario. Ottenere commenti e suggerimenti per la proposta.

-oppure-

È anche possibile scegliere tra i problemi esistenti per cui sono benvenuti i contributi della community. In [Projects for .NET Community contributors](https://github.com/dotnet/docs/projects/35) (Progetti per i collaboratori della community .NET) sono elencati molti dei problemi disponibili per i collaboratori della community. A seconda dei propri interessi e del livello di impegno, è possibile scegliere tra i problemi nelle categorie seguenti:

- **Maintenance (Manutenzione)** . Questa categoria include contributi piuttosto semplici, come la correzione di collegamenti interrotti o non corretti, l'aggiunta di esempi di codice mancanti o la correzione di problemi limitati del contenuto. Questi problemi possono a volte interessare numerosi file. In tal caso, è opportuno fare sapere a Microsoft su cosa si vorrebbe lavorare prima di iniziare. Aggiungere un commento al problema per segnalare che si sta lavorando al problema.

- **Content updates (Aggiornamenti del contenuto)** . Considerata la vastità del set di documenti, i contenuti diventano facilmente obsoleti e richiedono una revisione. Inoltre, per svariati motivi, certi contenuti sono duplicati o persino triplicati. L'aggiornamento del contenuto comporta assicurarsi che i singoli argomenti siano aggiornati oppure rivedere il contenuto in un'area funzionale per eliminare duplicati e assicurarsi che tutto il contenuto univoco sia mantenuto nel set di documentazione più ridotto.

- **New content authoring (Creazione di nuovo contenuto)** . Se si è interessati a creare un nuovo argomento, questi problemi elencano gli argomenti che Microsoft vorrebbe aggiungere al set di documenti. Prima di iniziare a lavorare a un argomento, però, farlo sapere a Microsoft. Se si è interessati a scrivere un argomento non presente in questo elenco, aprire un problema.

È anche possibile dare un'occhiata all'elenco dei [problemi aperti](https://github.com/dotnet/docs/issues) e offrirsi come volontari per lavorare a quelli di proprio interesse. Viene usata l'etichetta [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) per contrassegnare i problemi identificati come candidati per il contributo della community. Per questi problemi sono in genere necessarie informazioni di contesto minime e sono per questo adatti per le prime esperienze. Invitiamo i collaboratori esperti della community a individuare eventuali problemi di interesse. Quando se ne trova uno, aggiungere un commento per richiedere se è aperto.

Dopo aver selezionato un'attività su cui lavorare, seguire la [guida introduttiva](../get-started-setup-github.md) per creare un account GitHub e configurare l'ambiente.

**Passaggio 2:** creare una copia tramite fork dei repository `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` o `dotnet/ml-api-docs` in base alle specifiche esigenze e creare un ramo per le modifiche.

Per le modifiche di minore entità, vedere le istruzioni per la modifica in GitHub nella [home page](../index.md#quick-edits-to-existing-documents) della guida per i collaboratori.

**Passaggio 3:** apportare le modifiche nel nuovo ramo.

Nel caso di un nuovo argomento, è possibile usare questo [file modello](dotnet-style-guide.md) come punto di partenza. Il file contiene linee guida per la redazione del contenuto e spiega anche i metadati richiesti per ogni articolo, come le informazioni sull'autore.

Passare alla cartella corrispondente alla posizione del sommario stabilita per l'articolo nel passaggio 1. Tale cartella contiene i file Markdown per tutti gli articoli in quella sezione. Se necessario, creare una nuova cartella in cui posizionare i file per il contenuto. L'articolo principale per tale sezione è denominato *index.md*.

Per le immagini e altre risorse statiche, creare una sottocartella denominata **media** all'interno della cartella che contiene l'articolo, se non esiste già. All'interno della cartella **media** creare una sottocartella con il nome dell'articolo (ad eccezione del file index). 

Per i **frammenti di codice** creare una sottocartella denominata **snippets** all'interno della cartella che contiene l'articolo, se non esiste già. Nella maggior parte dei casi saranno disponibili frammenti di codice per tutti e tre i principali linguaggi .NET, ovvero C#, F# e Visual Basic. In tal caso, creare sottocartelle denominate **csharp**, **fsharp** e **vb** per ognuno dei tre progetti. Per semplicità, usare la cartella **snippets** per il progetto nella guida per C#, nella guida per F# e nella guida per Visual Basic. Tali aree contengono in genere i frammenti di codice per un linguaggio. I frammenti di codice sono esempi di codice piccoli e mirati che illustrano i concetti trattati in un articolo. I programmi più grandi, destinati al download e all'esplorazione, devono essere posizionati nel repository [dotnet/samples](https://github.com/dotnet/samples). Gli esempi completi sono trattati nella sezione [Contributi per gli esempi](#contributing-to-samples).

Assicurarsi di usare la sintassi Markdown corretta. Per esempi comuni, vedere le [informazioni di riferimento su modelli e Markdown](dotnet-style-guide.md).

## <a name="example-structure"></a>Struttura di esempio

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png
          /snippets
            /porting-overview
              /csharp
                porting.csproj
                porting-overview.cs
                Program.cs
              /fsharp
                porting.fsproj
                porting-overview.fs
                Program.fs
               /vb
                porting.vbproj
                porting-overview.vb
                Program.vb

La struttura illustrata in precedenza include un'immagine, *portability_report.png*, e tre progetti di codice che includono i **frammenti di codice** inclusi nell'articolo *porting-overview.md*. Una struttura alternativa accettata contiene un progetto per ogni linguaggio, che contiene tutti i frammenti di codice per tutti gli articoli in tale cartella. Questa alternativa è stata usata nelle aree dedicate alle informazioni di riferimento sul linguaggio, considerata la presenza di frammenti molto piccoli per dimostrare la sintassi del linguaggio. È sconsigliata in altre aree.

Per motivi cronologici, molti dei frammenti di codice inclusi vengono archiviati nella cartella */samples* nel repository *dotnet/docs*. Se si apportano modifiche sostanziali a un articolo, i frammenti di codice devono essere spostati nella nuova struttura. Non spostare i frammenti di codice per piccole modifiche.

**Passaggio 4:** inviare una richiesta pull (PR) dal ramo personale al ramo master.

> [!IMPORTANT]
> La funzionalità di [automazione dei commenti](../how-to-write-workflows-major.md#review-and-sign-off) non è attualmente disponibile per alcun repository della documentazione di .NET. I membri del team della documentazione di .NET si occuperanno della revisione e del merge della richiesta pull.

Ogni richiesta pull deve in genere riguardare un problema alla volta e può includere modifiche per uno o più file. Per la risoluzione di più problemi in file diversi, sono preferibili richieste pull separate. Se si creano esempi e allo stesso tempo si aggiorna il Markdown, sarà necessario creare una richiesta pull separata per gli esempi.

Se la richiesta pull risolve un problema esistente, aggiungere la parola chiave `Fixes #Issue_Number` nel messaggio di commit o nella descrizione della richiesta pull. In questo modo, il problema viene chiuso automaticamente al momento del merge della richiesta pull. Per altre informazioni, vedere [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (Chiusura dei problemi tramite messaggi di commit).

Il team .NET effettuerà la revisione della richiesta pull e avviserà nel caso siano necessari altri aggiornamenti o modifiche per l'approvazione.

**Passaggio 5:** apportare eventuali modifiche necessarie al ramo in base a quanto concordato con il team.

I responsabili della manutenzione effettueranno il merge della richiesta pull nel ramo master dopo l'applicazione di commenti e suggerimenti e l'approvazione della modifica.

Viene eseguito regolarmente il push di tutti i commit dal ramo master al ramo pubblico e sarà quindi possibile vedere il proprio contributo pubblicato in https://docs.microsoft.com/dotnet/. La pubblicazione avviene di solito giornalmente nei giorni lavorativi. Attività di manutenzione potrebbero ritardare la pubblicazione di alcuni giorni.

## <a name="contributing-to-samples"></a>Contributi per gli esempi

Il repository [dotnet/samples](https://github.com/dotnet/samples) contiene tutti il codice di esempio che fa parte di qualsiasi argomento nella documentazione di .NET. Esistono svariati progetti diversi organizzati in sottocartelle. Queste sottocartelle hanno un'organizzazione simile a quella della documentazione per .NET.

Viene fatta la distinzione seguente per il codice che supporta il contenuto:

- Esempi: i lettori possono scaricare ed eseguire gli esempi. Tutti gli esempi devono essere applicazioni o librerie complete. Se l'esempio crea una libreria, deve includere unit test o un'applicazione che consenta ai lettori di eseguire il codice. Spesso vengono usati più toolkit, tecnologie o funzionalità. Il file readme.md per ogni esempio farà riferimento all'articolo in modo da poter leggere altre informazioni sui concetti illustrati.
- Frammenti di codice: illustrano un concetto o un'attività più limitati. Possono essere compilati, ma non sono progettati per essere applicazioni complete. Devono poter essere eseguiti correttamente, ma non rappresentano un'applicazione di esempio per uno scenario tipico. Sono invece progettati per illustrare singoli concetti o funzionalità con il minor codice possibile. Non dovrebbero essere composti da più di una schermata di codice.

Gli esempi vengono archiviati nel repository [dotnet/samples](https://github.com/dotnet/samples). È in progetto l'elaborazione di un modello nel quale la struttura di cartelle degli esempi corrisponde a quella della documentazione. Questi sono gli standard adottati:

- Le cartelle di primo livello corrispondono alle cartelle di primo livello nel repository *docs*. Ad esempio, il repository docs include una cartella *machine-learning/tutorials* e gli esempi per le esercitazioni di Machine Learning sono nella cartella *samples/machine-learning/tutorials*.

Inoltre, tutti gli esempi nelle cartelle *core* e *standard* devono poter essere compilati ed eseguiti su tutte le piattaforme supportate da .NET Core. Il sistema di compilazione CI imporrà tale requisito. La cartella *framework* di primo livello contiene esempi compilati e convalidati solo in Windows.

I progetti di esempio devono poter essere compilati ed eseguiti nel set di piattaforme più ampio possibile per l'esempio specifico. In pratica ciò significa creare applicazioni console basate su .NET Core quando possibile. Gli esempi specifici per il Web o per un framework di interfaccia utente devono includere gli strumenti appositi. Sono esempi di questo tipo le applicazioni Web, le app per dispositivi mobili, le app WPF o WinForms e così via.

È in progetto l'implementazione di un sistema CI per tutto il codice. Quando si aggiornano gli esempi, assicurarsi che ogni aggiornamento faccia parte di un progetto compilabile. Idealmente, aggiungere anche test per verificare la correttezza degli esempi.

Ogni esempio completo creato deve contenere un file *readme.md*. Questo file deve contenere una breve descrizione dell'esempio (uno o due paragrafi). Il file *readme.md* deve indicare ai lettori i concetti illustrati dall'esempio. Il file *readme.md* deve anche contenere un collegamento al documento online nel [sito della documentazione di .NET](https://docs.microsoft.com/dotnet/welcome). Per stabilire se un determinato file nel repository corrisponde a tale sito, sostituire `/docs` nel percorso del repository con `https://docs.microsoft.com/dotnet`.

L'argomento includerà anche collegamenti all'esempio. Aggiungere un collegamento diretto alla cartella dell'esempio in GitHub.

### <a name="writing-a-new-sample"></a>Scrittura di un nuovo esempio

Gli esempi sono programmi completi e librerie destinati al download. Possono avere un ambito ridotto, ma illustrano i concetti in modo da consentire agli utenti di esplorare e sperimentare autonomamente. Le linee guida per gli esempi assicurano che i lettori possano scaricarli ed esplorarli. Esaminare gli esempi per [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) come esempio di ciascuna delle linee guida.

1. L'esempio **deve fare parte di un progetto compilabile**. Se possibile, i progetti devono poter essere compilati per tutte le piattaforme supportate da .NET Core. Rappresentano un'eccezione gli esempi dimostrativi di una funzionalità specifica di una piattaforma o di uno strumento specifico di una piattaforma.

2. L'esempio deve essere conforme allo [stile di scrittura del codice corefx](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) per mantenere la coerenza.

    - È inoltre preferibile usare metodi `static` anziché metodi di istanza per la dimostrazione di scenari che non richiedono la creazione di una nuova istanza di oggetto.

3. L'esempio deve includere **codice appropriato per la gestione delle eccezioni** e prevedere la gestione di tutte le eccezioni che è probabile vengano generate nel contesto dell'esempio. Ad esempio, un esempio che chiama il metodo [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) per recuperare l'input dell'utente deve usare codice di gestione delle eccezioni appropriato quando la stringa di input viene passata come argomento a un metodo. In modo analogo, se una chiamata di metodo nell'esempio potrebbe avere esito negativo, occorre gestire l'eccezione risultante. Gestire sempre le eccezioni specifiche generate dal metodo, piuttosto che le eccezioni della classe di base, come [Exception](https://docs.microsoft.com/dotnet/api/system.exception) o [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. Se l'esempio compila un pacchetto autonomo, è necessario includere i runtime usati dal sistema di compilazione CI, oltre ai runtime usati dall'esempio:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

Sarà presto disponibile un sistema CI per compilare questi progetti.

Per creare un esempio:

1. Registrare un [problema](https://github.com/dotnet/docs/issues) o aggiungere un commento a uno esistente per indicare l'intenzione di lavorarci.
2. Scrivere l'argomento che spiega i concetti dimostrati dall'esempio (ad esempio: `docs/standard/linq/where-clause.md`).
3. Scrivere l'esempio (ad esempio: `WhereClause-Sample1.cs`).
4. Creare un file Program.cs con un punto di ingresso Main che chiama gli esempi. Se è già disponibile, aggiungere la chiamata all'esempio:

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

Per compilare qualsiasi frammento di codice o esempio .NET Core si usa l'interfaccia della riga di comando di .NET Core, installabile con [.NET Core SDK](https://www.microsoft.com/net/download). Per compilare ed eseguire l'esempio:

1. Passare alla cartella dell'esempio e compilarlo per verificare se sono presenti errori:

    ```console
    dotnet build
    ```
2. Eseguire l'esempio:

    ```console
    dotnet run
    ```

3. Aggiungere un file readme.md nella directory radice dell'esempio.

   Il file deve includere una breve descrizione del codice e indirizzare gli utenti all'articolo che fa riferimento all'esempio. Nella parte superiore del file *readme.md* devono essere presenti i metadati necessari per il sito di [esplorazione degli esempi](https://docs.microsoft.com/samples). Il blocco di intestazione deve contenere i campi seguenti:

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - La raccolta `languages` deve includere solo i linguaggi disponibili per l'esempio.
   - La raccolta `products` deve includere solo i prodotti rilevanti per l'esempio.

Se non quando indicato, tutti gli esempi possono essere compilati dalla riga di comando su qualsiasi piattaforma supportata da .NET Core. Esistono alcuni esempi specifici di Visual Studio che richiedono Visual Studio 2017 o versioni successive. Alcuni esempi, inoltre, illustrano funzionalità specifiche di una piattaforma e richiederanno una piattaforma specifica. Altri esempi e frammenti di codice richiedono .NET Framework e verranno eseguiti su piattaforme Windows e sarà necessario il Developer Pack per la versione di .NET Framework di destinazione.

## <a name="the-c-interactive-experience"></a>Esperienza C# Interactive

Tutti gli esempi inclusi in un articolo usano un [tag di linguaggio](../code-in-docs.md) per indicare il linguaggio sorgente. Per brevi esempi di codice in C# è possibile usare il tag di linguaggio `csharp-interactive` per specificare un esempio C# eseguito nel browser. (Gli esempi di codice inline usano il tag `csharp-interactive`. Per i frammenti di codice inclusi dall'origine, usare il tag `code-csharp-interactive`.) Questi esempi di codice visualizzano una finestra del codice e una finestra di output nell'articolo. La finestra di output mostra l'eventuale output dell'esecuzione del codice interattivo dopo l'esecuzione dell'esempio da parte dell'utente.

L'esperienza C# Interactive cambia il modo di utilizzare gli esempi. I visitatori possono eseguire l'esempio per visualizzare i risultati. Sono numerosi i fattori che consentono di determinare se l'esempio o il testo corrispondente devono includere informazioni sull'output.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Quando visualizzare l'output previsto senza eseguire l'esempio

- Gli articoli destinati ai principianti devono includere l'output, in modo che i lettori possano confrontare l'output da loro ottenuto con la risposta prevista.
- Gli esempi in cui l'output è fondamentale per l'argomento devono visualizzarlo. Ad esempio, gli articoli dedicati alla formattazione del testo dovrebbero mostrare il testo formattato senza eseguire l'esempio.
- Quando sia l'esempio che l'output previsto sono brevi, valutare la possibilità di mostrare l'output, perché permette di risparmiare tempo.
- Gli articoli che spiegano gli effetti delle impostazioni cultura o delle impostazioni cultura inglese non dipendenti da paese/area geografica correnti devono spiegare l'output previsto. Il ciclo Read–Eval–Print (REPL) interattivo viene eseguito su un host basato su Linux. Le impostazioni cultura predefinite e le impostazioni cultura inglese non dipendenti da paese/area geografica producono output diverso su sistemi operativi e computer diversi. L'articolo deve spiegare l'output nei sistemi Windows, Linux e Mac.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Quando escludere l'output previsto dall'esempio

- Gli articoli con esempi che generano output esteso non dovrebbero includerlo nei commenti, perché copre il codice dopo l'esecuzione dell'esempio.
- Articoli in cui l'esempio dimostra un argomento, ma l'output non è fondamentale per la comprensione. Ad esempio, codice che esegue una query LINQ per spiegare la sintassi della query e poi visualizza ogni elemento nella raccolta di output.

> [!NOTE]
> Si potrebbe notare che alcuni argomenti non seguono in effetti tutte le linee guida qui presentate. Il nostro scopo è ottenere coerenza in tutto il sito. Vedere l'elenco dei [problemi aperti](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) correlati a questo obiettivo specifico.

### <a name="contributing-to-international-content"></a>Contributi per il contenuto internazionale

I contributi per il contenuto tradotto automaticamente non sono attualmente accettati. Per migliorare la qualità del contenuto tradotto automaticamente, è stato effettuato il passaggio a un motore di traduzione automatica neurale. Microsoft accetta e incoraggia i contributi per il contenuto con traduzione umana, usato per il training del motore di traduzione automatica neurale. Nel corso del tempo i contributi per il contenuto tradotto miglioreranno la qualità sia della traduzione umana che della traduzione automatica. Gli argomenti tradotti in modo automatico includeranno una dichiarazione di non responsabilità che informa che parte dell'argomento potrebbe essere tradotta automaticamente e il pulsante **Modifica** non verrà visualizzato, perché la modifica è disabilitata.

## <a name="contributor-license-agreement"></a>Contratto di licenza per i collaboratori

Prima del merge della richiesta di pull, è necessario sottoscrivere il [Contratto di licenza per contributi (CLA) di .NET Foundation](https://cla.dotnetfoundation.org). La sottoscrizione è richiesta una sola volta per i progetti in .NET Foundation. È possibile leggere altre informazioni sui [contratti di licenza per contributi](http://en.wikipedia.org/wiki/Contributor_License_Agreement) su Wikipedia.

Il contratto: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

Non è necessario sottoscrivere il contratto anticipatamente. È possibile clonare il ramo, creare una copia tramite fork e inviare la richiesta pull come di consueto. Al momento della creazione, la richiesta pull viene classificata da un bot CLA. Se la modifica è minima (ad esempio, la correzione di un errore ortografico) alla richiesta pull viene assegnata l'etichetta `cla-not-required`. In caso contrario, viene classificata come `cla-required`. Dopo la sottoscrizione del contratto di licenza per contributi, tutte le richieste pull correnti e future vengono classificate come `cla-signed`.
