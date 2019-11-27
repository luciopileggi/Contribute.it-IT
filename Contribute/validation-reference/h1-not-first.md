---
title: h1-not-first
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528921"
---
# <a name="h1-not-first"></a><span data-ttu-id="a8c71-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="a8c71-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="a8c71-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="a8c71-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="a8c71-105">Solo l'intestazione dei metadati YAML può venire prima di H1 in un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="a8c71-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="a8c71-106">Ad esempio, se si vuole aggiungere una nota o un'immagine all'inizio dell'articolo, deve essere successiva a H1.</span><span class="sxs-lookup"><span data-stu-id="a8c71-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="a8c71-107">Questa disposizione non è consentita:</span><span class="sxs-lookup"><span data-stu-id="a8c71-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="a8c71-108">Usare invece:</span><span class="sxs-lookup"><span data-stu-id="a8c71-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="a8c71-109">Un'altra causa comune di questo problema è la presenza di [byte order mark (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) prima dell'intestazione YAML,</span><span class="sxs-lookup"><span data-stu-id="a8c71-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="a8c71-110">introdotti a volta da problemi di codifica durante il commit del contenuto nei repository.</span><span class="sxs-lookup"><span data-stu-id="a8c71-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="a8c71-111">Questi BOM causano problemi di rendering in GitHub e devono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="a8c71-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="a8c71-112">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="a8c71-112">Resolution</span></span>

<span data-ttu-id="a8c71-113">Rimuovere eventuale contenuto diverso dall'intestazione dei metadati YAML prima di H1.</span><span class="sxs-lookup"><span data-stu-id="a8c71-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
