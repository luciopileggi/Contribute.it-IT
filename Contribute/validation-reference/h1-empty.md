---
title: h1-empty
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427689"
---
# <a name="h1-empty"></a><span data-ttu-id="638a7-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="638a7-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="638a7-104">Avviso</span><span class="sxs-lookup"><span data-stu-id="638a7-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="638a7-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="638a7-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="638a7-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="638a7-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="638a7-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="638a7-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="638a7-108">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="638a7-108">Resolution</span></span>

<span data-ttu-id="638a7-109">Per risolvere questo problema, assicurarsi che H1 includa il contenuto, non solo un codice hash.</span><span class="sxs-lookup"><span data-stu-id="638a7-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="638a7-110">Valore non valido:</span><span class="sxs-lookup"><span data-stu-id="638a7-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="638a7-111">Valore valido:</span><span class="sxs-lookup"><span data-stu-id="638a7-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]