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
# <a name="included-file-redirected"></a>included-file-redirected

## <a name="warning"></a>Avviso

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a>Risoluzione

Ristrutturare il contenuto in modo da non includere un file reindirizzato. Ad esempio, creare un nuovo file per includere o rimuovere il riferimento incluso e il collegamento al contenuto o scriverlo inline.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
