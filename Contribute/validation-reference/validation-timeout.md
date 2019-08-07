---
title: validation-timeout
description: Spiegazione e risoluzione del problema di compilazione di Docs validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817406"
---
# <a name="validation-timeout"></a><span data-ttu-id="198b3-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="198b3-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="198b3-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="198b3-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="198b3-105">In alcuni casi, problemi temporanei nel servizio di convalida, ad esempio un server in uno stato non valido, impediscono alla compilazione di Docs di chiamare correttamente il servizio.</span><span class="sxs-lookup"><span data-stu-id="198b3-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="198b3-106">Dopo diversi tentativi, la chiamata raggiunge il timeout e la convalida viene annullata per evitare ritardi nella compilazione e il blocco delle pipeline di compilazione.</span><span class="sxs-lookup"><span data-stu-id="198b3-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="198b3-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="198b3-107">Resolution</span></span>

<span data-ttu-id="198b3-108">Provare a chiudere e riaprire la richiesta pull oppure a eseguire nuovamente una compilazione manuale tramite il portale Docs (solo amministratori di repository).</span><span class="sxs-lookup"><span data-stu-id="198b3-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="198b3-109">Spesso i problemi del servizio si risolvono automaticamente dopo il primo nuovo tentativo.</span><span class="sxs-lookup"><span data-stu-id="198b3-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="198b3-110">Se è necessaria assistenza da parte di un amministratore o il messaggio continua a essere visualizzato, i dipendenti Microsoft possono segnalare il problema tramite [https://SiteHelp](https://SiteHelp). I collaboratori esterni possono invece indicare l'autore di un articolo nella richiesta pull per ottenere assistenza.</span><span class="sxs-lookup"><span data-stu-id="198b3-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
