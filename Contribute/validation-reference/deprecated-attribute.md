---
title: deprecated-attribute
description: Spiegazione e risoluzione del problema di compilazione della documentazione deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236223"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="8bd49-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="8bd49-103">deprecated-attribute</span></span>

## <a name="warning"></a><span data-ttu-id="8bd49-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="8bd49-104">Warning</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="8bd49-105">Usare `ms.service` per specificare i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="8bd49-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="8bd49-106">Per specificare informazioni più dettagliate su `ms.service`, è facoltativamente possibile specificare `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8bd49-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="8bd49-107">Non usare `ms.component` perché è deprecato per questo contenuto.</span><span class="sxs-lookup"><span data-stu-id="8bd49-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="8bd49-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="8bd49-108">Resolution</span></span>

<span data-ttu-id="8bd49-109">Verificare che il valore di `ms.service` sia corretto per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="8bd49-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="8bd49-110">Scegliere quindi un valore di `ms.subservice` valido.</span><span class="sxs-lookup"><span data-stu-id="8bd49-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="8bd49-111">I valori validi sono disponibili in [questo sito interno di Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8bd49-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
