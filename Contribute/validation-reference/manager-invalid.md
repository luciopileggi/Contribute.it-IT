---
title: manager-invalid
description: Spiegazione e risoluzione del problema di compilazione di Docs manager-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637231"
---
# <a name="manager-invalid"></a><span data-ttu-id="fa5fc-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="fa5fc-103">manager-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="fa5fc-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="fa5fc-104">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="fa5fc-105">Alcuni gruppi di contenuto richiedono l'attributo `manager` per identificare il manager dell'autore.</span><span class="sxs-lookup"><span data-stu-id="fa5fc-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="fa5fc-106">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="fa5fc-106">Resolution</span></span>

<span data-ttu-id="fa5fc-107">Il valore di `manager` deve essere un alias valido per un singolo dipendente di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa5fc-107">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="fa5fc-108">Verificare l'alias del manager dell'autore e aggiornare il valore.</span><span class="sxs-lookup"><span data-stu-id="fa5fc-108">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
