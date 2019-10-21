---
title: Fornire contributi per i repository della documentazione di PowerShell
description: Questo articolo illustra i repository che costituiscono la documentazione di PowerShell.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290174"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="5f43b-103">Contributi alla documentazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f43b-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="5f43b-104">Grazie per l'interesse dimostrato nella documentazione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f43b-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="5f43b-105">Questo documento illustra il processo per fornire contributi per gli articoli e gli esempi di codice ospitati nel sito della documentazione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f43b-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="5f43b-106">Possono essere semplici contribuiti, ad esempio la correzione di errori di battitura oppure contribuiti più complessi, come nuovi articoli.</span><span class="sxs-lookup"><span data-stu-id="5f43b-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="5f43b-107">Il sito della documentazione di PowerShell è composto da più repository che contengono uno o più docset:</span><span class="sxs-lookup"><span data-stu-id="5f43b-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="5f43b-108">[Concetti e informazioni di riferimento sui cmdlet di PowerShell][psdocs]</span><span class="sxs-lookup"><span data-stu-id="5f43b-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="5f43b-109">Esempi di codice di PowerShell SDK - Repository privato contenente gli esempi usati negli articoli dell'SDK</span><span class="sxs-lookup"><span data-stu-id="5f43b-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="5f43b-110">[Informazioni di riferimento su PowerShell .NET SDK ](/dotnet/api/?view=pscore-6.2.0) - Contenuto del repository privato generato dal codice sorgente di PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f43b-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="5f43b-111">I problemi per tutto questo contenuto vengono registrati nel repository [PowerShell-Docs][docsrepo].</span><span class="sxs-lookup"><span data-stu-id="5f43b-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="5f43b-112">Struttura del repository</span><span class="sxs-lookup"><span data-stu-id="5f43b-112">Repository Structure</span></span>

<span data-ttu-id="5f43b-113">Il repository PowerShell-Docs è costituito da tre docset pubblicati in [Microsoft Docs][psdocs]. I docset sono contenuti nelle cartelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f43b-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="5f43b-114">[/reference/][ref] - Contiene le informazioni di riferimento sui cmdlet di PowerShell per i cmdlet forniti in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f43b-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="5f43b-115">Le informazioni di riferimento sono raccolte in cartelle specifiche delle versioni (3.0, 4.0, 5.0, 5.1, 6 e 7).</span><span class="sxs-lookup"><span data-stu-id="5f43b-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="5f43b-116">Questo docset non contiene informazioni di riferimento per i moduli forniti con Windows o altri prodotti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f43b-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="5f43b-117">[/reference/docs-conceptual][conceptual] - Contiene la documentazione concettuale di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f43b-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="5f43b-118">Sono incluse istruzioni per l'installazione, script di esempio, procedure e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="5f43b-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="5f43b-119">[/developer/][SDK] - Contiene la documentazione concettuale di PowerShell SDK.</span><span class="sxs-lookup"><span data-stu-id="5f43b-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
