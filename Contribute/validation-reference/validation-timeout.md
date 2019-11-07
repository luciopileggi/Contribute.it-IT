---
title: validation-timeout
description: Spiegazione e risoluzione del problema di compilazione di Docs validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592529"
---
# <a name="validation-timeout"></a><span data-ttu-id="36dd4-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="36dd4-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="36dd4-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="36dd4-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="36dd4-105">In alcuni casi, problemi temporanei nel servizio di convalida, ad esempio un server in uno stato non valido, impediscono alla compilazione di Docs di chiamare correttamente il servizio.</span><span class="sxs-lookup"><span data-stu-id="36dd4-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="36dd4-106">Dopo diversi tentativi, la chiamata raggiunge il timeout e la convalida viene annullata per evitare ritardi nella compilazione e il blocco delle pipeline di compilazione.</span><span class="sxs-lookup"><span data-stu-id="36dd4-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="36dd4-107">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="36dd4-107">Resolution</span></span>

<span data-ttu-id="36dd4-108">Provare a chiudere e a riaprire la richiesta pull o a forzare una compilazione completa tramite il [portale di Docs](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="36dd4-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="36dd4-109">Spesso i problemi del servizio si risolvono automaticamente dopo il primo nuovo tentativo.</span><span class="sxs-lookup"><span data-stu-id="36dd4-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="36dd4-110">Si noti che è necessario essere un amministratore di repository per forzare una compilazione tramite il portale di Docs.</span><span class="sxs-lookup"><span data-stu-id="36dd4-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="36dd4-111">Se non si conosce l'amministratore del repository oppure se il messaggio continua a essere visualizzato dopo una compilazione forzata, i dipendenti Microsoft possono segnalare il problema tramite [https://SiteHelp](https://SiteHelp). I collaboratori esterni possono invece menzionare l'autore di un articolo nella richiesta pull per ottenere assistenza.</span><span class="sxs-lookup"><span data-stu-id="36dd4-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="36dd4-112">Un amministratore di repository può forzare una compilazione completa come segue:</span><span class="sxs-lookup"><span data-stu-id="36dd4-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="36dd4-113">Passare al [portale di Docs](https://ops.microsoft.com/#/) ed effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="36dd4-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="36dd4-114">Trovare il repository eseguendo una ricerca nell'angolo superiore sinistro e selezionarlo.</span><span class="sxs-lookup"><span data-stu-id="36dd4-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="36dd4-115">:::image type="content" source="media/find-repo.png" alt-text="trovare il repository tramite la casella di ricerca del portale di Docs":::</span><span class="sxs-lookup"><span data-stu-id="36dd4-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="36dd4-116">Nella scheda **Build History** (Cronologia di compilazione) fare clic su **+ Manual Publish** (Pubblicazione manuale).</span><span class="sxs-lookup"><span data-stu-id="36dd4-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="36dd4-117">Selezionare il ramo che riceve l'avviso, ad esempio il ramo master.</span><span class="sxs-lookup"><span data-stu-id="36dd4-117">Select the branch that's getting the Warning, such as master.</span></span>
1. <span data-ttu-id="36dd4-118">Per la destinazione mantenere il valore predefinito, ovvero **Docs Site** (Sito Docs).</span><span class="sxs-lookup"><span data-stu-id="36dd4-118">For target, keep the default, **Docs Site**.</span></span>
1. <span data-ttu-id="36dd4-119">Selezionare la casella di controllo **Force Publish** (Forza pubblicazione).</span><span class="sxs-lookup"><span data-stu-id="36dd4-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="36dd4-120">Fare clic su **Publish** (Pubblica).</span><span class="sxs-lookup"><span data-stu-id="36dd4-120">Click **Publish**.</span></span>

   <span data-ttu-id="36dd4-121">:::image type="content" source="media/force-build.png" alt-text="passaggi per forzare una compilazione completa":::</span><span class="sxs-lookup"><span data-stu-id="36dd4-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="36dd4-122">Verrà forzata una compilazione completa sul ramo.</span><span class="sxs-lookup"><span data-stu-id="36dd4-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
