---
title: Roadmap per etichette e progetti
description: Questo articolo illustra il modo in cui le etichette e i progetti vengono usati nel repository dotnet/docs.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760377"
---
# <a name="labels-and-projects-roadmap"></a>Roadmap per etichette e progetti

Per organizzare il lavoro, il team della documentazione di .NET fa ampio uso delle [etichette GitHub](https://github.com/dotnet/docs/labels). L'applicazione di un filtro basato su una combinazione di etichette consente di concentrare l'attenzione sulle sezioni di interesse del sito Web [Documentazione di .NET](https://docs.microsoft.com/dotnet).

Vengono usati anche [progetti GitHub](https://github.com/dotnet/docs/projects) per organizzare sprint e altre epiche orientate agli obiettivi.

Questa roadmap illustra come vengono usati questi strumenti organizzativi e include collegamenti a filtri che consentono di individuare aree di interesse in modo pratico e veloce.

## <a name="labels"></a>Etichette

Se questa è la prima esperienza di collaborazione con [dotnet/docs](https://github.com/dotnet/docs), iniziare con i problemi [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs). Questi problemi, dato l'ambito più mirato, sono ideali per un primo contributo. Dalla visualizzazione up-for-grabs è possibile filtrare ulteriormente i problemi in base alle aree e alla priorità. Per chi vuole cimentarsi per la prima volta offrendo un contributo di portata minore, è disponibile un certo numero di problemi adatti ai principianti, contrassegnati dall'etichetta [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue).

È possibile usare etichette per classificare i problemi in molti modi diversi:

- [Guide di .NET](#find-a-single-net-guide) e [sezioni di una guida](#search-one-section-of-a-guide).
- [Versione di destinazione](#releases)
- [Priorità](#priority)

È possibile combinare un'etichetta di ogni set (guida, versione, priorità) per ridurre l'ambito di ricerca e individuare i problemi di cui occuparsi.

### <a name="find-a-single-net-guide"></a>Trovare una guida di .NET singola

Vengono usate etichette per ogni e-book di architettura e per ogni guida di .NET.

![:book: guide con sfondo verde chiaro](./media/labels-projects/guide.png "Prefisso per le etichette della Guida all'architettura")

Gli e-book sulle architetture sono contrassegnati dal prefisso `:book: guide` e hanno uno sfondo verde chiaro. Queste sono le aree in formato esteso che trattano l'architettura consigliata. Di seguito sono riportati i problemi correnti filtrati per ognuna delle guide delle architetture .NET.

- [App Web ASP.NET Core](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Architetture native del cloud](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Ciclo di vita di Docker](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizzazione con i contenitori di Windows](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [Microservizi .NET](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [App serverless](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Questo stile di etichetta viene applicato anche alle [linee guida di progettazione di .NET Framework ](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). Quest'area ha la stessa struttura di etichetta, ma le richieste pull della community sono sconsigliate. Questo è materiale ristampato dietro autorizzazione e non deve essere modificato.

![:books: Area con sfondo blu scuro](./media/labels-projects/area.png "Prefisso per le etichette delle aree della Guida a .NET")

Ogni guida di .NET è contrassegnata dal prefisso `:books: Area` e ha uno sfondo blu scuro. Di seguito sono riportati i problemi correnti filtrati per ogni guida di .NET.

- [Informazioni di riferimento sulle API](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [Guida a C#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Guida alle architetture desktop](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [Guida a F#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [Guida a ML.NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [Guida all'architettura .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Potrebbe essere rimossa
- [Guida a .NET Core](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [Guida a .NET per Apache Spark](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [Guida a .NET Framework](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [Guida a .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Informazioni di riferimento per l'API Roslyn](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - Potrebbe essere rimossa.
- [Guida a Visual Basic](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Cercare una sezione di una guida

![:card_file_box: Area con sfondo blu](./media/labels-projects/technology.png "Prefisso per le etichette delle sottoaree della Guida a .NET")

Le guide relative a .NET sono di grandi dimensioni, pertanto queste etichette limitano ulteriormente l'ambito a una sezione di una guida. Ogni sottoarea di .NET è contrassegnata dal prefisso `:card_file_box: Technology` e ha uno sfondo blu. Molte di queste etichette si applicano a più guide, mentre altre si trovano in una sola guida. Dopo aver filtrato in base a un'area, aggiungere una di queste etichette per limitare ulteriormente l'ambito dei problemi.

- AppCompat
- Async Task
- Concetti avanzati di C#
- Compilatore C#
- Concetti fondamentali
- Introduzione a C#
- Informazioni di riferimento per il linguaggio C#
- Sicurezza Null C#
- Novità su C#
- CLI
- Accesso ai dati
- Docker
- Programmi di installazione
- LINQ
- NCL
- .NET Standard
- API Roslyn
- Sicurezza
- WCF
- WF
- WIF
- Windows Form
- WPF

### <a name="releases"></a>Versioni

![:checkered_flag: Release: in giallo scuro](./media/labels-projects/release.png "Prefisso per le etichette di versione")

I problemi contrassegnati per una versione specifica sono indicati con il prefisso `:checkered_flag: Release:` e hanno uno sfondo giallo scuro.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Priorità

Le etichette di priorità sono tutte contrassegnate da `P` seguita da una sola cifra. I numeri più bassi indicano una priorità più alta:

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>Cosa significano le altre etichette?

I team dei contenuti possono usare molte altre etichette per gestire le diverse classificazioni dei problemi. Se non si fa parte di un team di contenuto, è possibile ignorare le altre etichette.

## <a name="projects"></a>Progetti

I progetti vengono usati in due modi:

- Tipi di progetto Mese AAAA: Si tratta di lavagne delle attività per il piano di lavoro di ogni mese.
- Epiche a esecuzione prolungata: Usate per organizzare le attività finalizzate a un obiettivo quando il lavoro richiederà diversi mesi.
