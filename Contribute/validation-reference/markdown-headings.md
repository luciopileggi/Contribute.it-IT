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
# <a name="markdown-headings"></a>Intestazioni Markdown

I seguenti requisiti di convalida si applicano alle intestazioni dei file Markdown di OPS.

## <a name="h1"></a>H1

`H1` si riferisce alla prima intestazione di un file Markdown. Quando viene pubblicato in docs.microsoft.com, l'H1 viene visualizzato nella parte superiore della pagina in caratteri grandi.

Un H1 viene creato iniziando una riga con un singolo codice hash (`#`) seguito da uno spazio, quindi dal testo dell'intestazione. Ad esempio, l'H1 di questo articolo è:

```md
# Markdown headings
```

In queste intestazioni H1 vengono applicate le regole seguenti:

- Nel file deve essere presente un H1.
- Può essere presente solo un carattere H1.
- L'H1 deve includere contenuto.

  ```markdown
  # 
  This is not allowed.
  ```
- Deve essere presente uno spazio tra `#` e il contenuto H1. Un H1 senza spazio non viene visualizzato come intestazione nella pagina pubblicata.

  ```markdown
  #This looks bad on the site.
  ```
- L'H1 deve essere il primo contenuto del file dopo il titolo dei metadati YML. È consentita l'assenza di contenuto, come testo o immagini, tra la fine del titolo YML e l'H1.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- Non dovrebbe essere usato l'elemento HTML per le intestazioni di primo livello, `<h1>`. Usare la sintassi di Markdown (`# `).
- L'H1 non deve essere più lungo di 100 caratteri. Si tratta di una linea guida di stile.

## <a name="h2---h6"></a>H2 - H6

In OPS sono consentiti i caratteri da H2 (`## `) a H6 (`###### `). Per creare le intestazioni, usare i titoli Markdown, non l'elemento HTML (`<h2>` - `<h6>`).
