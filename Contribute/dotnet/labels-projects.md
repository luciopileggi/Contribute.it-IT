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
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="529a3-103">Roadmap per etichette e progetti</span><span class="sxs-lookup"><span data-stu-id="529a3-103">Labels and projects roadmap</span></span>

<span data-ttu-id="529a3-104">Per organizzare il lavoro, il team della documentazione di .NET fa ampio uso delle [etichette GitHub](https://github.com/dotnet/docs/labels).</span><span class="sxs-lookup"><span data-stu-id="529a3-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="529a3-105">L'applicazione di un filtro basato su una combinazione di etichette consente di concentrare l'attenzione sulle sezioni di interesse del sito Web [Documentazione di .NET](https://docs.microsoft.com/dotnet).</span><span class="sxs-lookup"><span data-stu-id="529a3-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="529a3-106">Vengono usati anche [progetti GitHub](https://github.com/dotnet/docs/projects) per organizzare sprint e altre epiche orientate agli obiettivi.</span><span class="sxs-lookup"><span data-stu-id="529a3-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="529a3-107">Questa roadmap illustra come vengono usati questi strumenti organizzativi e include collegamenti a filtri che consentono di individuare aree di interesse in modo pratico e veloce.</span><span class="sxs-lookup"><span data-stu-id="529a3-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="529a3-108">Etichette</span><span class="sxs-lookup"><span data-stu-id="529a3-108">Labels</span></span>

<span data-ttu-id="529a3-109">Se questa è la prima esperienza di collaborazione con [dotnet/docs](https://github.com/dotnet/docs), iniziare con i problemi [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs).</span><span class="sxs-lookup"><span data-stu-id="529a3-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="529a3-110">Questi problemi, dato l'ambito più mirato,</span><span class="sxs-lookup"><span data-stu-id="529a3-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="529a3-111">sono ideali per un primo contributo.</span><span class="sxs-lookup"><span data-stu-id="529a3-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="529a3-112">Dalla visualizzazione up-for-grabs è possibile filtrare ulteriormente i problemi in base alle aree e alla priorità.</span><span class="sxs-lookup"><span data-stu-id="529a3-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="529a3-113">Per chi vuole cimentarsi per la prima volta offrendo un contributo di portata minore, è disponibile un certo numero di problemi adatti ai principianti, contrassegnati dall'etichetta [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue).</span><span class="sxs-lookup"><span data-stu-id="529a3-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="529a3-114">È possibile usare etichette per classificare i problemi in molti modi diversi:</span><span class="sxs-lookup"><span data-stu-id="529a3-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="529a3-115">[Guide di .NET](#find-a-single-net-guide) e [sezioni di una guida](#search-one-section-of-a-guide).</span><span class="sxs-lookup"><span data-stu-id="529a3-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="529a3-116">Versione di destinazione</span><span class="sxs-lookup"><span data-stu-id="529a3-116">Target release</span></span>](#releases)
- [<span data-ttu-id="529a3-117">Priorità</span><span class="sxs-lookup"><span data-stu-id="529a3-117">Priority</span></span>](#priority)

<span data-ttu-id="529a3-118">È possibile combinare un'etichetta di ogni set (guida, versione, priorità) per ridurre l'ambito di ricerca e individuare i problemi di cui occuparsi.</span><span class="sxs-lookup"><span data-stu-id="529a3-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="529a3-119">Trovare una guida di .NET singola</span><span class="sxs-lookup"><span data-stu-id="529a3-119">Find a single .NET guide</span></span>

<span data-ttu-id="529a3-120">Vengono usate etichette per ogni e-book di architettura e per ogni guida di .NET.</span><span class="sxs-lookup"><span data-stu-id="529a3-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="529a3-121">![:book: guide con sfondo verde chiaro](./media/labels-projects/guide.png "Prefisso per le etichette della Guida all'architettura")</span><span class="sxs-lookup"><span data-stu-id="529a3-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="529a3-122">Gli e-book sulle architetture sono contrassegnati dal prefisso `:book: guide` e hanno uno sfondo verde chiaro.</span><span class="sxs-lookup"><span data-stu-id="529a3-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="529a3-123">Queste sono le aree in formato esteso che trattano l'architettura consigliata.</span><span class="sxs-lookup"><span data-stu-id="529a3-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="529a3-124">Di seguito sono riportati i problemi correnti filtrati per ognuna delle guide delle architetture .NET.</span><span class="sxs-lookup"><span data-stu-id="529a3-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="529a3-125">App Web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="529a3-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="529a3-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="529a3-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="529a3-127">Architetture native del cloud</span><span class="sxs-lookup"><span data-stu-id="529a3-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="529a3-128">Ciclo di vita di Docker</span><span class="sxs-lookup"><span data-stu-id="529a3-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="529a3-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="529a3-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="529a3-130">Modernizzazione con i contenitori di Windows</span><span class="sxs-lookup"><span data-stu-id="529a3-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="529a3-131">Microservizi .NET</span><span class="sxs-lookup"><span data-stu-id="529a3-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="529a3-132">App serverless</span><span class="sxs-lookup"><span data-stu-id="529a3-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="529a3-133">Questo stile di etichetta viene applicato anche alle [linee guida di progettazione di .NET Framework ](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="529a3-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="529a3-134">Quest'area ha la stessa struttura di etichetta, ma le richieste pull della community sono sconsigliate.</span><span class="sxs-lookup"><span data-stu-id="529a3-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="529a3-135">Questo è materiale ristampato dietro autorizzazione e non deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="529a3-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="529a3-136">![:books: Area con sfondo blu scuro](./media/labels-projects/area.png "Prefisso per le etichette delle aree della Guida a .NET")</span><span class="sxs-lookup"><span data-stu-id="529a3-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="529a3-137">Ogni guida di .NET è contrassegnata dal prefisso `:books: Area` e ha uno sfondo blu scuro.</span><span class="sxs-lookup"><span data-stu-id="529a3-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="529a3-138">Di seguito sono riportati i problemi correnti filtrati per ogni guida di .NET.</span><span class="sxs-lookup"><span data-stu-id="529a3-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="529a3-139">Informazioni di riferimento sulle API</span><span class="sxs-lookup"><span data-stu-id="529a3-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="529a3-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="529a3-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="529a3-141">Guida a C#</span><span class="sxs-lookup"><span data-stu-id="529a3-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="529a3-142">Guida alle architetture desktop</span><span class="sxs-lookup"><span data-stu-id="529a3-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="529a3-143">Guida a F#</span><span class="sxs-lookup"><span data-stu-id="529a3-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="529a3-144">Guida a ML.NET</span><span class="sxs-lookup"><span data-stu-id="529a3-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="529a3-145">[Guida all'architettura .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Potrebbe essere rimossa</span><span class="sxs-lookup"><span data-stu-id="529a3-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="529a3-146">Guida a .NET Core</span><span class="sxs-lookup"><span data-stu-id="529a3-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="529a3-147">Guida a .NET per Apache Spark</span><span class="sxs-lookup"><span data-stu-id="529a3-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="529a3-148">Guida a .NET Framework</span><span class="sxs-lookup"><span data-stu-id="529a3-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="529a3-149">Guida a .NET</span><span class="sxs-lookup"><span data-stu-id="529a3-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="529a3-150">[Informazioni di riferimento per l'API Roslyn](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - Potrebbe essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="529a3-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="529a3-151">Guida a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="529a3-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="529a3-152">Cercare una sezione di una guida</span><span class="sxs-lookup"><span data-stu-id="529a3-152">Search one section of a guide</span></span>

<span data-ttu-id="529a3-153">![:card_file_box: Area con sfondo blu](./media/labels-projects/technology.png "Prefisso per le etichette delle sottoaree della Guida a .NET")</span><span class="sxs-lookup"><span data-stu-id="529a3-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="529a3-154">Le guide relative a .NET sono di grandi dimensioni, pertanto queste etichette limitano ulteriormente l'ambito a una sezione di una guida.</span><span class="sxs-lookup"><span data-stu-id="529a3-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="529a3-155">Ogni sottoarea di .NET è contrassegnata dal prefisso `:card_file_box: Technology` e ha uno sfondo blu.</span><span class="sxs-lookup"><span data-stu-id="529a3-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="529a3-156">Molte di queste etichette si applicano a più guide, mentre altre si trovano in una sola guida.</span><span class="sxs-lookup"><span data-stu-id="529a3-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="529a3-157">Dopo aver filtrato in base a un'area, aggiungere una di queste etichette per limitare ulteriormente l'ambito dei problemi.</span><span class="sxs-lookup"><span data-stu-id="529a3-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="529a3-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="529a3-158">AppCompat</span></span>
- <span data-ttu-id="529a3-159">Async Task</span><span class="sxs-lookup"><span data-stu-id="529a3-159">Async Task</span></span>
- <span data-ttu-id="529a3-160">Concetti avanzati di C#</span><span class="sxs-lookup"><span data-stu-id="529a3-160">C# Advanced concepts</span></span>
- <span data-ttu-id="529a3-161">Compilatore C#</span><span class="sxs-lookup"><span data-stu-id="529a3-161">C# compiler</span></span>
- <span data-ttu-id="529a3-162">Concetti fondamentali</span><span class="sxs-lookup"><span data-stu-id="529a3-162">C# Fundamentals</span></span>
- <span data-ttu-id="529a3-163">Introduzione a C#</span><span class="sxs-lookup"><span data-stu-id="529a3-163">C# Get Started</span></span>
- <span data-ttu-id="529a3-164">Informazioni di riferimento per il linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="529a3-164">C# Language Reference</span></span>
- <span data-ttu-id="529a3-165">Sicurezza Null C#</span><span class="sxs-lookup"><span data-stu-id="529a3-165">C# Null safety</span></span>
- <span data-ttu-id="529a3-166">Novità su C#</span><span class="sxs-lookup"><span data-stu-id="529a3-166">C# What's new</span></span>
- <span data-ttu-id="529a3-167">CLI</span><span class="sxs-lookup"><span data-stu-id="529a3-167">CLI</span></span>
- <span data-ttu-id="529a3-168">Accesso ai dati</span><span class="sxs-lookup"><span data-stu-id="529a3-168">Data Access</span></span>
- <span data-ttu-id="529a3-169">Docker</span><span class="sxs-lookup"><span data-stu-id="529a3-169">Docker</span></span>
- <span data-ttu-id="529a3-170">Programmi di installazione</span><span class="sxs-lookup"><span data-stu-id="529a3-170">Installers</span></span>
- <span data-ttu-id="529a3-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="529a3-171">LINQ</span></span>
- <span data-ttu-id="529a3-172">NCL</span><span class="sxs-lookup"><span data-stu-id="529a3-172">NCL</span></span>
- <span data-ttu-id="529a3-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="529a3-173">.NET Standard</span></span>
- <span data-ttu-id="529a3-174">API Roslyn</span><span class="sxs-lookup"><span data-stu-id="529a3-174">Roslyn APIs</span></span>
- <span data-ttu-id="529a3-175">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="529a3-175">Security</span></span>
- <span data-ttu-id="529a3-176">WCF</span><span class="sxs-lookup"><span data-stu-id="529a3-176">WCF</span></span>
- <span data-ttu-id="529a3-177">WF</span><span class="sxs-lookup"><span data-stu-id="529a3-177">WF</span></span>
- <span data-ttu-id="529a3-178">WIF</span><span class="sxs-lookup"><span data-stu-id="529a3-178">WIF</span></span>
- <span data-ttu-id="529a3-179">Windows Form</span><span class="sxs-lookup"><span data-stu-id="529a3-179">WinForms</span></span>
- <span data-ttu-id="529a3-180">WPF</span><span class="sxs-lookup"><span data-stu-id="529a3-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="529a3-181">Versioni</span><span class="sxs-lookup"><span data-stu-id="529a3-181">Releases</span></span>

<span data-ttu-id="529a3-182">![:checkered_flag: Release: in giallo scuro](./media/labels-projects/release.png "Prefisso per le etichette di versione")</span><span class="sxs-lookup"><span data-stu-id="529a3-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="529a3-183">I problemi contrassegnati per una versione specifica sono indicati con il prefisso `:checkered_flag: Release:` e hanno uno sfondo giallo scuro.</span><span class="sxs-lookup"><span data-stu-id="529a3-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="529a3-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="529a3-184">.NET Core 2.2</span></span>
- <span data-ttu-id="529a3-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="529a3-185">.NET Core 3.0</span></span>
- <span data-ttu-id="529a3-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="529a3-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="529a3-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="529a3-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="529a3-188">Priorità</span><span class="sxs-lookup"><span data-stu-id="529a3-188">Priority</span></span>

<span data-ttu-id="529a3-189">Le etichette di priorità sono tutte contrassegnate da `P` seguita da una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="529a3-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="529a3-190">I numeri più bassi indicano una priorità più alta:</span><span class="sxs-lookup"><span data-stu-id="529a3-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="529a3-191">P0</span><span class="sxs-lookup"><span data-stu-id="529a3-191">P0</span></span>
- <span data-ttu-id="529a3-192">P1</span><span class="sxs-lookup"><span data-stu-id="529a3-192">P1</span></span>
- <span data-ttu-id="529a3-193">P2</span><span class="sxs-lookup"><span data-stu-id="529a3-193">P2</span></span>
- <span data-ttu-id="529a3-194">P3</span><span class="sxs-lookup"><span data-stu-id="529a3-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="529a3-195">Cosa significano le altre etichette?</span><span class="sxs-lookup"><span data-stu-id="529a3-195">What about the other labels?</span></span>

<span data-ttu-id="529a3-196">I team dei contenuti possono usare molte altre etichette per gestire le diverse classificazioni dei problemi.</span><span class="sxs-lookup"><span data-stu-id="529a3-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="529a3-197">Se non si fa parte di un team di contenuto, è possibile ignorare le altre etichette.</span><span class="sxs-lookup"><span data-stu-id="529a3-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="529a3-198">Progetti</span><span class="sxs-lookup"><span data-stu-id="529a3-198">Projects</span></span>

<span data-ttu-id="529a3-199">I progetti vengono usati in due modi:</span><span class="sxs-lookup"><span data-stu-id="529a3-199">We use projects in two ways:</span></span>

- <span data-ttu-id="529a3-200">Tipi di progetto Mese AAAA: Si tratta di lavagne delle attività per il piano di lavoro di ogni mese.</span><span class="sxs-lookup"><span data-stu-id="529a3-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="529a3-201">Epiche a esecuzione prolungata: Usate per organizzare le attività finalizzate a un obiettivo quando il lavoro richiederà diversi mesi.</span><span class="sxs-lookup"><span data-stu-id="529a3-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
