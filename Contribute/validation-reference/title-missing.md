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
# <a name="title-missing"></a><span data-ttu-id="b27b9-103">title-missing</span><span class="sxs-lookup"><span data-stu-id="b27b9-103">title-missing</span></span>

## <a name="warning"></a><span data-ttu-id="b27b9-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="b27b9-104">Warning</span></span>

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a><span data-ttu-id="b27b9-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="b27b9-105">Resolution</span></span>

<span data-ttu-id="b27b9-106">Aggiungere stringa per il titolo da visualizzare nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="b27b9-106">Add a title string to show in search results.</span></span> <span data-ttu-id="b27b9-107">In generale, i titoli devono avere una lunghezza compresa tra 19 e 59 caratteri, devono essere diversi dall'intestazione H1 dell'articolo e devono includere parole di personalizzazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="b27b9-107">In general, titles should be between 19 and 59 characters, should be distinct from the H1 of the article, and should include relevant branding words.</span></span> <span data-ttu-id="b27b9-108">Non è necessario includere "| Microsoft Docs " nel titolo, perché viene aggiunto automaticamente da Docs e viene ignorato se lo si aggiunge in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="b27b9-108">You shouldn't include " | Microsoft Docs" in your title - this is added automatically by Docs, and is ignored if you add it explicitly.</span></span> <span data-ttu-id="b27b9-109">Se si vogliono aggiungere ulteriori indicazioni di personalizzazione, ad esempio " - Azure", a tutti i titoli di un set di contenuti, impostare il valore dei metadati `titleSuffix` a livello globale o per una cartella.</span><span class="sxs-lookup"><span data-stu-id="b27b9-109">If you want to add additional branding, such as " - Azure", to all titles in a content set, set the `titleSuffix` metadata value globally or for a folder.</span></span>

<span data-ttu-id="b27b9-110">Per visualizzare in anteprima quale aspetto avrà il titolo in Google, accedere a [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).</span><span class="sxs-lookup"><span data-stu-id="b27b9-110">You can preview how your title will look in Google on [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).</span></span>

<span data-ttu-id="b27b9-111">Per altre informazioni sui titoli validi e sull'ottimizzazione motore di ricerca (SEO), i dipendenti di Microsoft possono fare riferimento alle [nozioni di base SEO](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) nella guida per i collaboratori interna.</span><span class="sxs-lookup"><span data-stu-id="b27b9-111">If you're a Microsoft employee, see [SEO Basics](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) in the internal Contributor Guide for more information about good titles and search engine optimization (SEO).</span></span>

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
