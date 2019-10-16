---
title: Concetti di base di Git e GitHub per la documentazione
description: Questo articolo offre una panoramica di Git,  del repository GitHub e dell'organizzazione del contenuto, oltre alle convenzioni di denominazione usate per docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/30/2017
ms.openlocfilehash: 5154b80102069f1d5526b744637f8ba854f1fe3f
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288432"
---
# <a name="git-and-github-essentials-for-docs"></a>Concetti di base di Git e GitHub per Docs

## <a name="overview"></a>Panoramica

I collaboratori che contribuiscono al contenuto delle pagine Docs interagiscono con più strumenti e svariati processi, lavorando parallelamente ad altri collaboratori sullo stesso progetto, potenzialmente sullo stesso contenuto, persino nello stesso tempo. Tutto ciò è reso possibile dal software Git e GitHub.

Git è un sistema di controllo delle versioni open source che facilita questo tipo di collaborazione ai progetti tramite il *controllo delle versioni distribuito* dei file archiviati in *repository*. In sintesi, Git rende possibile l'integrazione dei flussi di lavoro svolto da più collaboratori nel tempo per un determinato repository.

GitHub è un servizio di hosting basato sul Web per i repository Git, come quelli usati per archiviare il contenuto di [docs.microsoft.com](https://docs.microsoft.com). Per ogni progetto, GitHub ospita il repository principale, dal quale i collaboratori possono creare copie per il loro lavoro,

## <a name="git"></a>Git

Gli utenti che hanno familiarità con i sistemi di controllo delle versioni centralizzati (come Team Foundation Server, SharePoint o Visual SourceSafe) noteranno che il flusso di lavoro per i contributi e la terminologia a supporto del modello distribuito di Git sono peculiari. Ad esempio, non è previsto il blocco dei file solitamente associato alle operazioni di estrazione/archiviazione. In effetti, Git tiene traccia delle modifiche a un livello ancora più dettagliato, confrontando i file byte per byte.

Git usa anche una struttura su più livelli per l'archiviazione e la gestione del contenuto per un progetto:

- *Repository*: noto anche come *repo*, è l'unità di archiviazione di livello più alto. Un repository contiene uno o più rami.
- *Ramo*: unità di archiviazione che contiene i file e le cartelle che costituiscono il set di contenuti di un progetto. I rami separano flussi di lavoro, in genere definiti versioni. I contributi vengono sempre creati in un ramo specifico, che ne rappresenta anche l'ambito. Tutti i repository contengono un ramo predefinito, solitamente denominato "master", e uno o più rami destinati a essere riuniti nel ramo master. Il ramo master funge da versione corrente e punto di riferimento assoluto per il progetto e rappresenta il ramo padre da cui vengono creati tutti gli altri rami nel repository.

I collaboratori interagiscono con Git per aggiornare e modificare i repository sia a livello locale che di GitHub:

- A livello locale tramite strumenti come la console di Git Bash, che supporta comandi Git per la gestione dei repository locali e la comunicazione con i repository di GitHub.
- Tramite [www.github.com](https://www.github.com), che integra Git per gestire la riconciliazione dei contributi che confluiscono nel repository principale.

## <a name="github"></a>GitHub

> [!NOTE]
> Anche se le linee guida per Docs sono basate sull'uso di GitHub, alcuni team usano Visual Studio Team Services per ospitare i repository di Git. Il client Visual Studio Team Explorer offre un'interfaccia utente grafica per l'interazione con i repository di Team Services, in alternativa all'uso dei comandi Git tramite la riga di comando.
> </br>
> Molte delle linee guida seguenti, poi, sono state sviluppate come procedure consigliate sulla base di anni di esperienza nell'hosting del contenuto del servizio Azure in GitHub e potrebbero essere obbligatorie per alcuni repository di Docs.

Tutti i flussi di lavoro iniziano e finiscono a livello di GitHub, dove è archiviato il repository principale per qualsiasi progetto Docs. Le copie che i collaboratori creano per uso personale vengono distribuite tra più computer e alla fine vengono riconciliate nel repository GitHub principale del progetto.

### <a name="directory-organization"></a>Organizzazione delle directory

Come accennato in precedenza, il ramo predefinito/master di un progetto rappresenta la versione corrente del contenuto del progetto stesso. Il contenuto del ramo master e dei rami creati a partire da questo è allineato in modo generico con l'organizzazione degli articoli nelle pagine corrispondenti di Docs. Le sottodirectory vengono usate per separare il contenuto specifico (ad esempio per i servizi), il contenuto multimediale (come i file immagine) e i file di inclusione che consentono il riutilizzo del contenuto.

È in genere possibile trovare una directory `articles` principale dalla radice del repository. La directory articles contiene una serie di sottodirectory. Gli articoli nelle sottodirectory sono formattati come file markdown con estensione *md*. Alcuni repository che supportano più servizi usano una sottodirectory `/articles` generica, come il repository [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs). Altri potrebbero usare un nome specifico del servizio, ad esempio il repository [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) che usa `/IntuneDocs`.

Alla radice di questa directory sono disponibili gli articoli generali correlati al servizio o al prodotto nel suo insieme. Esiste in genere un'altra serie di sottodirectory corrispondenti a funzionalità/servizi o scenari comuni. Ad esempio, gli articoli relativi alle macchine virtuali di Azure sono inclusi nella sottodirectory `/virtual-machines` e gli articoli dedicati ai concetti e all'esplorazione di Intune sono nella sottodirectory `/understand-explore`.

### <a name="media-subdirectory"></a>Sottodirectory media

Ogni directory di articoli contiene una sottodirectory `/media` per i file multimediali corrispondenti. I file multimediali contengono le immagini usate dagli articoli che includono riferimenti a immagini.

### <a name="includes-subdirectory"></a>Sottodirectory includes

L'eventuale contenuto riutilizzabile condiviso da due o più articoli viene posizionato in una sottodirectory `/includes` all'interno della directory `articles` principale. In un file markdown che usa il file di inclusione viene inserita un'estensione Markdown "include" corrispondente nel punto in cui è necessario fare riferimento al file di inclusione.

Vedere [Come usare Markdown: file di inclusione](how-to-write-use-markdown.md#include-files) per informazioni aggiuntive.

### <a name="markdown-file-template"></a>Modello di file markdown

Per comodità, la directory radice di ogni repository contiene in genere un file modello Markdown denominato `template.md`. Se è necessario creare un nuovo articolo per l'invio al repository, è possibile partire da questo file. Il file contiene:

- Un'**intestazione metadati** all'inizio del file, delimitata da due linee a 3 trattini. L'intestazione contiene i vari tag usati per tenere traccia delle informazioni correlate all'articolo. I metadati dell'articolo consentono alcune funzionalità, ad esempio l'attribuzione dell'autore e/o del collaboratore, i percorsi di navigazione e le descrizioni dell'articolo. Includono anche le ottimizzazioni SEO e i processi di creazione di report usati da Microsoft per valutare le prestazioni del contenuto. I metadati sono quindi importanti.
- Una **sezione metadati** che descrive i vari tag e i diversi valori dei metadati. Se non si conoscono con certezza i valori da usare per la sezione metadati, è possibile non specificarli o impostarli come commenti con un hashtag iniziale (#). Verranno esaminati o completati dal revisore della richiesta pull per il repository.
- Diversi **esempi di uso di Markdown** per formattare gli elementi di un articolo.
- **Istruzioni generali sull'uso delle estensioni Markdown** per diversi tipi di avvisi.
- Esempi di **incorporamento di video** tramite un iframe.
- **Istruzioni generali sull'uso delle estensioni docs.microsoft.com** per controlli speciali come pulsanti e selettori.

## <a name="pull-requests"></a>Richieste pull

Una *richiesta pull* rappresenta un modo comodo per proporre un set di modifiche da applicare al ramo predefinito. Le modifiche (dette anche *commit*) vengono archiviate in un ramo del collaboratore, consentendo a GitHub di valutare in via preliminare l'impatto della loro *unione* nel ramo predefinito. Una richiesta pull è anche un meccanismo per fornire al collaboratore un riscontro dal processo di compilazione/convalida da parte del revisore della richiesta pull, per risolvere potenziali problemi o dubbi prima dell'unione delle modifiche nel ramo predefinito.

Esistono due modi per collaborare tramite richiesta pull, a seconda delle dimensioni delle modifiche che si vogliono proporre. Questo aspetto verrà illustrato in maggiore dettaglio nella sezione dedicata ai [flussi di lavoro di GitHub](how-to-write-workflows-major.md) di questa guida.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
