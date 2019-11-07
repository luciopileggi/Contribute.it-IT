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
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Avviso

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

In alcuni casi, problemi temporanei nel servizio di convalida, ad esempio un server in uno stato non valido, impediscono alla compilazione di Docs di chiamare correttamente il servizio. Dopo diversi tentativi, la chiamata raggiunge il timeout e la convalida viene annullata per evitare ritardi nella compilazione e il blocco delle pipeline di compilazione.

## <a name="resolution"></a>Risoluzione

Provare a chiudere e a riaprire la richiesta pull o a forzare una compilazione completa tramite il [portale di Docs](https://ops.microsoft.com/#/). Spesso i problemi del servizio si risolvono automaticamente dopo il primo nuovo tentativo.

Si noti che è necessario essere un amministratore di repository per forzare una compilazione tramite il portale di Docs. Se non si conosce l'amministratore del repository oppure se il messaggio continua a essere visualizzato dopo una compilazione forzata, i dipendenti Microsoft possono segnalare il problema tramite [https://SiteHelp](https://SiteHelp). I collaboratori esterni possono invece menzionare l'autore di un articolo nella richiesta pull per ottenere assistenza.

Un amministratore di repository può forzare una compilazione completa come segue:

1. Passare al [portale di Docs](https://ops.microsoft.com/#/) ed effettuare l'accesso.
1. Trovare il repository eseguendo una ricerca nell'angolo superiore sinistro e selezionarlo.

   :::image type="content" source="media/find-repo.png" alt-text="trovare il repository tramite la casella di ricerca del portale di Docs":::
1. Nella scheda **Build History** (Cronologia di compilazione) fare clic su **+ Manual Publish** (Pubblicazione manuale).
1. Selezionare il ramo che riceve l'avviso, ad esempio il ramo master.
1. Per la destinazione mantenere il valore predefinito, ovvero **Docs Site** (Sito Docs).
1. Selezionare la casella di controllo **Force Publish** (Forza pubblicazione).
1. Fare clic su **Publish** (Pubblica).

   :::image type="content" source="media/force-build.png" alt-text="passaggi per forzare una compilazione completa":::

Verrà forzata una compilazione completa sul ramo.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
