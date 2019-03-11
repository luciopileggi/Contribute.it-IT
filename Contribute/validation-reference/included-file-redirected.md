---
title: included-file-redirected
description: Spiegazione e risoluzione del problema di compilazione di Docs included-file-redirected
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459074"
---
# <a name="included-file-redirected"></a><span data-ttu-id="20716-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="20716-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="20716-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="20716-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="20716-105">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="20716-105">Resolution</span></span>

<span data-ttu-id="20716-106">Ristrutturare il contenuto in modo da non includere un file reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="20716-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="20716-107">Ad esempio, creare un nuovo file per includere o rimuovere il riferimento incluso e il collegamento al contenuto o scriverlo inline.</span><span class="sxs-lookup"><span data-stu-id="20716-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
