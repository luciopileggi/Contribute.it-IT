---
title: title-missing
description: Spiegazione e risoluzione del problema di compilazione della documentazione title-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236563"
---
# <a name="title-missing"></a>title-missing

## <a name="warning"></a>Avviso

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a>Risoluzione

Aggiungere stringa per il titolo da visualizzare nei risultati della ricerca. In generale, i titoli devono avere una lunghezza compresa tra 19 e 59 caratteri, devono essere diversi dall'intestazione H1 dell'articolo e devono includere parole di personalizzazione pertinenti. Non è necessario includere "| Microsoft Docs " nel titolo, perché viene aggiunto automaticamente da Docs e viene ignorato se lo si aggiunge in modo esplicito. Se si vogliono aggiungere ulteriori indicazioni di personalizzazione, ad esempio " - Azure", a tutti i titoli di un set di contenuti, impostare il valore dei metadati `titleSuffix` a livello globale o per una cartella.

Per visualizzare in anteprima quale aspetto avrà il titolo in Google, accedere a [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).

Per altre informazioni sui titoli validi e sull'ottimizzazione motore di ricerca (SEO), i dipendenti di Microsoft possono fare riferimento alle [nozioni di base SEO](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) nella guida per i collaboratori interna.

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
