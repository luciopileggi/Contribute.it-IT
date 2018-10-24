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
# <a name="docs-pr-validation-service"></a>Servizio di convalida PR Docs

Il servizio di convalida PR Docs è un'applicazione GitHub che esegue regole di convalida sui file in un PR.

Quando il servizio di convalida è abilitato in un repository, verrà visualizzato il seguente comportamento:

1. Viene inviato un PR.
1. Nel commento di GitHub che indica lo stato del PR, verrà visualizzato lo stato dei "controlli" abilitati sul repository. Si noti che in questo esempio, sono abilitati due controlli, "Commit Validation" e "OpenPublishing.Build":

   ![alcuni controlli non sono riusciti](media/validation-failed.png)

   Build può essere eseguito anche se la convalida del commit non riesce.

1. Per altre informazioni, fare clic su **Dettagli**.
1. Nella pagina Dettagli, verranno visualizzati tutti i controlli di convalida non riusciti, con informazioni su come risolvere i problemi:

   ![messaggio di convalida](media/validation-details.png)

Vedere il TOC riportato a sinistra del presente articolo per l'elenco delle convalide attualmente incluse nel servizio.