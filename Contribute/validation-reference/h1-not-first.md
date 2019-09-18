---
title: h1-not-first
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895463"
---
# <a name="h1-not-first"></a><span data-ttu-id="ce38e-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="ce38e-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ce38e-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="ce38e-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="ce38e-105">Solo l'intestazione dei metadati YAML può venire prima di H1 in un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="ce38e-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="ce38e-106">Ad esempio, se si vuole aggiungere una nota o un'immagine all'inizio dell'articolo, deve essere successiva a H1.</span><span class="sxs-lookup"><span data-stu-id="ce38e-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="ce38e-107">Questa disposizione non è consentita:</span><span class="sxs-lookup"><span data-stu-id="ce38e-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="ce38e-108">Usare invece:</span><span class="sxs-lookup"><span data-stu-id="ce38e-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="ce38e-109">Un'altra causa comune di questo problema è la presenza di [byte order mark (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) prima dell'intestazione YAML,</span><span class="sxs-lookup"><span data-stu-id="ce38e-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="ce38e-110">introdotti a volta da problemi di codifica durante il commit del contenuto nei repository.</span><span class="sxs-lookup"><span data-stu-id="ce38e-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="ce38e-111">Questi BOM causano problemi di rendering in GitHub e devono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="ce38e-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce38e-112">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="ce38e-112">Resolution</span></span>

<span data-ttu-id="ce38e-113">Rimuovere eventuale contenuto diverso dall'intestazione dei metadati YAML prima di H1.</span><span class="sxs-lookup"><span data-stu-id="ce38e-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
