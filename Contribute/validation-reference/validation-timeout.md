---
title: validation-timeout
description: Spiegazione e risoluzione del problema di compilazione di Docs validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024211"
---
# <a name="validation-timeout"></a><span data-ttu-id="12e8e-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="12e8e-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="12e8e-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="12e8e-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="12e8e-105">In alcuni casi, problemi temporanei nel servizio di convalida, ad esempio un server in uno stato non valido, impediscono alla compilazione di Docs di chiamare correttamente il servizio.</span><span class="sxs-lookup"><span data-stu-id="12e8e-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="12e8e-106">Dopo tre tentativi, la chiamata raggiunge il timeout e viene annullata la convalida per evitare ritardi nella compilazione e il blocco delle pipeline di compilazione.</span><span class="sxs-lookup"><span data-stu-id="12e8e-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="12e8e-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="12e8e-107">Resolution</span></span>

<span data-ttu-id="12e8e-108">Provare a chiudere e riaprire la richiesta pull oppure a eseguire nuovamente una compilazione manuale (solo amministratori di repository).</span><span class="sxs-lookup"><span data-stu-id="12e8e-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="12e8e-109">Spesso i problemi del servizio si risolvono automaticamente dopo il primo nuovo tentativo.</span><span class="sxs-lookup"><span data-stu-id="12e8e-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="12e8e-110">Se il messaggio continua a essere visualizzato, i dipendenti Microsoft possono segnalare il problema tramite [https://SiteHelp](https://SiteHelp). I collaboratori esterni possono invece indicare l'autore di un articolo nella richiesta pull per ottenere assistenza.</span><span class="sxs-lookup"><span data-stu-id="12e8e-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
