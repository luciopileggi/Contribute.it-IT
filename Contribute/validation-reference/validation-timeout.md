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
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Avviso

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

In alcuni casi, problemi temporanei nel servizio di convalida, ad esempio un server in uno stato non valido, impediscono alla compilazione di Docs di chiamare correttamente il servizio. Dopo diversi tentativi, la chiamata raggiunge il timeout e la convalida viene annullata per evitare ritardi nella compilazione e il blocco delle pipeline di compilazione.

## <a name="resolution"></a>Risoluzione

Provare a chiudere e riaprire la richiesta pull oppure a eseguire nuovamente una compilazione manuale tramite il portale Docs (solo amministratori di repository). Spesso i problemi del servizio si risolvono automaticamente dopo il primo nuovo tentativo. Se è necessaria assistenza da parte di un amministratore o il messaggio continua a essere visualizzato, i dipendenti Microsoft possono segnalare il problema tramite [https://SiteHelp](https://SiteHelp). I collaboratori esterni possono invece indicare l'autore di un articolo nella richiesta pull per ottenere assistenza.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
