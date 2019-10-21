---
title: h1-in-moniker
description: Spiegazione e risoluzione del problema di compilazione di Docs h1-in-moniker
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246361"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="61b7a-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="61b7a-103">h1-in-moniker</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="61b7a-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="61b7a-104">Suggestion</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="61b7a-105">H1 si riferisce alla prima intestazione di un file Markdown.</span><span class="sxs-lookup"><span data-stu-id="61b7a-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="61b7a-106">Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.</span><span class="sxs-lookup"><span data-stu-id="61b7a-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="61b7a-107">Un H1 viene creato iniziando una riga con un singolo codice hash (#) seguito da uno spazio, quindi dal testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="61b7a-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="61b7a-108">È possibile avere solo un H1 in ogni file.</span><span class="sxs-lookup"><span data-stu-id="61b7a-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="61b7a-109">Le intestazioni H1 non sono consentite nelle sezioni del moniker, perché possono facilmente causare intestazioni H1 duplicate o mancanti a seconda della configurazione del controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="61b7a-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="61b7a-110">Questo messaggio potrebbe essere visualizzato anche se una sezione del moniker contiene una riga di segni di uguale per ottenere una doppia sottolineatura, come questa: `=======`.</span><span class="sxs-lookup"><span data-stu-id="61b7a-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="61b7a-111">Si tratta di una sintassi Markdown alternativa per un H1.</span><span class="sxs-lookup"><span data-stu-id="61b7a-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="61b7a-112">Viene anche comunemente visualizzato nei conflitti di merge:</span><span class="sxs-lookup"><span data-stu-id="61b7a-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="61b7a-113">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="61b7a-113">Resolution</span></span>

<span data-ttu-id="61b7a-114">Per risolvere il problema, rimuovere le intestazioni H1 da tutte le sezioni del moniker e assicurarsi che l'intestazione H1 all'inizio dell'articolo sia appropriata per tutte le sezioni del moniker.</span><span class="sxs-lookup"><span data-stu-id="61b7a-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="61b7a-115">Si noti che non è consentito saltare i livelli di intestazione, ad esempio fare seguire H1 da H3.</span><span class="sxs-lookup"><span data-stu-id="61b7a-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="61b7a-116">Se un'intestazione H1 in una sezione del moniker è effettivamente una doppia sottolineatura (`=======`), rimuoverla o sostituirla con un'intestazione hashtag, ad esempio `##`, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="61b7a-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="61b7a-117">Se la doppia sottolineatura fa parte di un conflitto di merge, assicurarsi di rimuovere anche gli indicatori di inizio e fine del conflitto di merge e il testo obsoleto.</span><span class="sxs-lookup"><span data-stu-id="61b7a-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
