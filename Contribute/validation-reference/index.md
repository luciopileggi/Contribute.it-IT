---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084531"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="f0347-101">Servizio di convalida PR Docs</span><span class="sxs-lookup"><span data-stu-id="f0347-101">Docs PR validation service</span></span>

<span data-ttu-id="f0347-102">Il servizio di convalida PR Docs è un'applicazione GitHub che esegue regole di convalida sui file in un PR.</span><span class="sxs-lookup"><span data-stu-id="f0347-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="f0347-103">Quando il servizio di convalida è abilitato in un repository, verrà visualizzato il seguente comportamento:</span><span class="sxs-lookup"><span data-stu-id="f0347-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="f0347-104">Viene inviato un PR.</span><span class="sxs-lookup"><span data-stu-id="f0347-104">You submit a PR.</span></span>
1. <span data-ttu-id="f0347-105">Nel commento di GitHub che indica lo stato del PR, verrà visualizzato lo stato dei "controlli" abilitati sul repository.</span><span class="sxs-lookup"><span data-stu-id="f0347-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="f0347-106">Si noti che in questo esempio, sono abilitati due controlli, "Commit Validation" e "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="f0347-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![alcuni controlli non sono riusciti](media/validation-failed.png)

   <span data-ttu-id="f0347-108">Build può essere eseguito anche se la convalida del commit non riesce.</span><span class="sxs-lookup"><span data-stu-id="f0347-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="f0347-109">Per altre informazioni, fare clic su **Dettagli**.</span><span class="sxs-lookup"><span data-stu-id="f0347-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="f0347-110">Nella pagina Dettagli, verranno visualizzati tutti i controlli di convalida non riusciti, con informazioni su come risolvere i problemi:</span><span class="sxs-lookup"><span data-stu-id="f0347-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![messaggio di convalida](media/validation-details.png)

<span data-ttu-id="f0347-112">Vedere il TOC riportato a sinistra del presente articolo per l'elenco delle convalide attualmente incluse nel servizio.</span><span class="sxs-lookup"><span data-stu-id="f0347-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>