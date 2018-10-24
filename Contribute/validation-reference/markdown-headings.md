---
title: Intestazioni Markdown
description: Descrive i requisiti per le intestazioni Markdown.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084491"
---
# <a name="markdown-headings"></a><span data-ttu-id="97747-103">Intestazioni Markdown</span><span class="sxs-lookup"><span data-stu-id="97747-103">Markdown headings</span></span>

<span data-ttu-id="97747-104">I seguenti requisiti di convalida si applicano alle intestazioni dei file Markdown di OPS.</span><span class="sxs-lookup"><span data-stu-id="97747-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="97747-105">H1</span><span class="sxs-lookup"><span data-stu-id="97747-105">H1</span></span>

<span data-ttu-id="97747-106">`H1` si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="97747-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="97747-107">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="97747-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="97747-108">Un H1 viene creato iniziando una riga con un singolo codice hash (`#`) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="97747-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="97747-109">Ad esempio, l'H1 di questo articolo è:</span><span class="sxs-lookup"><span data-stu-id="97747-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="97747-110">In queste intestazioni H1 vengono applicate le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="97747-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="97747-111">Nel file deve essere presente un H1.</span><span class="sxs-lookup"><span data-stu-id="97747-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="97747-112">Può essere presente solo un carattere H1.</span><span class="sxs-lookup"><span data-stu-id="97747-112">There can only be one H1.</span></span>
- <span data-ttu-id="97747-113">L'H1 deve includere contenuto.</span><span class="sxs-lookup"><span data-stu-id="97747-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="97747-114">Deve essere presente uno spazio tra `#` e il contenuto H1.</span><span class="sxs-lookup"><span data-stu-id="97747-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="97747-115">Un H1 senza spazio non viene visualizzato come intestazione nella pagina pubblicata.</span><span class="sxs-lookup"><span data-stu-id="97747-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="97747-116">L'H1 deve essere il primo contenuto del file dopo il titolo dei metadati YML.</span><span class="sxs-lookup"><span data-stu-id="97747-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="97747-117">È consentita l'assenza di contenuto, come testo o immagini, tra la fine del titolo YML e l'H1.</span><span class="sxs-lookup"><span data-stu-id="97747-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="97747-118">Non dovrebbe essere usato l'elemento HTML per le intestazioni di primo livello, `<h1>`.</span><span class="sxs-lookup"><span data-stu-id="97747-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="97747-119">Usare la sintassi di Markdown (`# `).</span><span class="sxs-lookup"><span data-stu-id="97747-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="97747-120">L'H1 non deve essere più lungo di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="97747-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="97747-121">Si tratta di una linea guida di stile.</span><span class="sxs-lookup"><span data-stu-id="97747-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="97747-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="97747-122">H2 - H6</span></span>

<span data-ttu-id="97747-123">In OPS sono consentiti i caratteri da H2 (`## `) a H6 (`###### `).</span><span class="sxs-lookup"><span data-stu-id="97747-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="97747-124">Per creare le intestazioni, usare i titoli Markdown, non l'elemento HTML (`<h2>` - `<h6>`).</span><span class="sxs-lookup"><span data-stu-id="97747-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
