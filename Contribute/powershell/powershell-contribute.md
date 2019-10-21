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
# <a name="contributing-to-powershell-documentation"></a>Contributi alla documentazione di PowerShell

Grazie per l'interesse dimostrato nella documentazione di PowerShell.

Questo documento illustra il processo per fornire contributi per gli articoli e gli esempi di codice ospitati nel sito della documentazione di PowerShell. Possono essere semplici contribuiti, ad esempio la correzione di errori di battitura oppure contribuiti più complessi, come nuovi articoli.

Il sito della documentazione di PowerShell è composto da più repository che contengono uno o più docset:

- [Concetti e informazioni di riferimento sui cmdlet di PowerShell][psdocs]
- Esempi di codice di PowerShell SDK - Repository privato contenente gli esempi usati negli articoli dell'SDK
- [Informazioni di riferimento su PowerShell .NET SDK ](/dotnet/api/?view=pscore-6.2.0) - Contenuto del repository privato generato dal codice sorgente di PowerShell

I problemi per tutto questo contenuto vengono registrati nel repository [PowerShell-Docs][docsrepo].

## <a name="repository-structure"></a>Struttura del repository

Il repository PowerShell-Docs è costituito da tre docset pubblicati in [Microsoft Docs][psdocs]. I docset sono contenuti nelle cartelle seguenti:

- [/reference/][ref] - Contiene le informazioni di riferimento sui cmdlet di PowerShell per i cmdlet forniti in PowerShell. Le informazioni di riferimento sono raccolte in cartelle specifiche delle versioni (3.0, 4.0, 5.0, 5.1, 6 e 7). Questo docset non contiene informazioni di riferimento per i moduli forniti con Windows o altri prodotti Microsoft.
- [/reference/docs-conceptual][conceptual] - Contiene la documentazione concettuale di PowerShell. Sono incluse istruzioni per l'installazione, script di esempio, procedure e altro ancora.
- [/developer/][SDK] - Contiene la documentazione concettuale di PowerShell SDK.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
