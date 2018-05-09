---
title: Docs Authoring Pack per VS Code
description: Questo articolo illustra il pacchetto di estensioni VS Code per facilitare la creazione di codice Markdown per docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d0d61db2faf88598ecd2c800fb5fbe8df8ec44f5
ms.sourcegitcommit: 7b668124f25b8ad0442937a3ad05b19a47af5970
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/03/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack per VS Code

Docs Authoring Pack è una raccolta di estensioni VS Code che facilita la creazione di codice Markdown per docs.microsoft.com. Il pacchetto, [disponibile nel Marketplace di VS Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), contiene le estensioni seguenti:

- **DocFx:** consente l'anteprima di codice Markdown specifico di docs.microsoft.com. Per altre informazioni, vedere [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX).
- **markdownlint:** linter Markdown di ampia diffusione, creato da David Anson, che consente di assicurarsi che il codice Markdown segua le procedure consigliate. Per altre informazioni, vedere [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).
- **Docs Markdown:** offre assistenza per la creazione di codice Markdown per contenuto docs.microsoft.com in Open Publishing System (OPS). Offre sia supporto di base che per la sintassi Markdown personalizzata in OPS. Il resto di questo argomento descrive l'estensione Docs Markdown.

## <a name="prerequisites-and-assumptions"></a>Prerequisiti e presupposti

Per inserire in modo corretto collegamenti relativi, immagini e altro contenuto incorporato con l'estensione Docs Markdown, è necessario che l'area di lavoro VS Code faccia parte dell'ambito della radice del repository OPS clonato.

Parte della sintassi supportata dall'estensione, ad esempio avvisi e frammenti di codice, è sintassi Markdown per OPS personalizzata il cui rendering viene eseguito correttamente solo con la pubblicazione tramite OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Come usare l'estensione Docs Markdown

Per accedere al menu Docs Markdown, digitare `ALT+M`. Per selezionare una funzione, è possibile fare clic su di essa o usare Freccia GIÙ/Freccia SU. Per creare un filtro è sufficiente digitare e quindi premere `ENTER` quando la funzione voluta viene evidenziata nel menu. Sono disponibili le funzioni seguenti:

|Funzione     |Comando             |Descrizione           |
|-------------|--------------------|----------------------|
|Grassetto         |`formatBold`        |Formatta il testo in **grassetto**.|
|Corsivo       |`formatItalic`      |Formatta il testo in *corsivo*.|
|Codice         |`formatCode`        |Se è selezionata fino a una riga di testo, questa viene formattata come `inline code`.<br><br>Se sono selezionate più righe, queste vengono formattate come blocco di codice delimitato e, facoltativamente, è possibile selezionare un linguaggio di programmazione supportato da OPS.|
|Avviso        |`insertAlert`       |Inserisce una nota, un'informazione importante, un avviso o un suggerimento.<br><br>Selezionare il comando relativo all'avviso dal menu e quindi selezionare il tipo di avviso. Se in precedenza è stato selezionato del testo, questo viene racchiuso all'interno della sintassi del tipo di avviso selezionato. Se non è selezionato alcun testo, viene aggiunto un nuovo avviso con testo segnaposto.|
|Elenco numerato|`insertNumberedList` |Inserisce un nuovo elenco numerato.<br><br> Se sono selezionate più righe, ognuna costituisce un elemento dell'elenco. Si noti che nel codice Markdown gli elementi dell'elenco numerato hanno tutti il numero 1. Nel rendering in docs.microsoft.com, tuttavia, hanno numeri in sequenza o, per gli elenchi annidati, lettere in sequenza. Per creare un elenco numerato annidato, premere TAB all'interno dell'elenco padre.|
|Elenco puntato|`insertBulletedList` |Inserisce un nuovo elenco puntato.|
|Tabella        |`insertTable`        |Inserisce la struttura Markdown di una tabella.<br><br>Dopo aver inserito il comando per la tabella, specificare il numero di colonne e di righe nel formato colonne:righe, ad esempio 3:4. Si noti che il numero massimo di colonne che è possibile specificare tramite questa estensione è 5, che rappresenta il limite massimo consigliato per la leggibilità.|
|Collegamento         |`selectLinkType`      |Inserisce un collegamento. Quando si seleziona questo comando, viene visualizzato il sottomenu seguente.<br><br>`External`: crea un collegamento a una pagina Web tramite URI. È necessario includere "http" o "https".<br>`Internal`: inserisce un collegamento relativo a un altro file nello stesso repository. Dopo aver selezionato questa opzione, digitare nella finestra di comando in modo da filtrare i file per nome e quindi selezionare il file voluto. <br>`Bookmark in this file`: scegliere da un elenco di intestazioni nel file corrente per inserire un segnalibro formattato in modo corretto.<br>`Bookmark in another file`: prima filtrare in base al nome e selezionare il file a cui collegarsi e quindi scegliere l'intestazione appropriata all'interno del file selezionato.|
|Immagine        |`insertImage`     |Digitare testo alternativo (necessario per l'accessibilità) e selezionarlo, quindi chiamare questo comando per filtrare l'elenco dei file di immagine supportati presenti nel repository e selezionare il file voluto. Se quando si chiama questo comando non è stato selezionato testo alternativo, verrà richiesto di farlo per poter selezionare un file di immagine.|
|Inclusione      |`insertInclude`   |Consente di trovare un file da incorporare nel file corrente.|
|Frammento di codice      |`insertSnippet`   |Consente di trovare un frammento di codice nel repository da incorporare nel file corrente.|
|Video        |`insertVideo`     |Aggiunge un video incorporato.|
|Anteprima      |`previewTopic`    |Visualizza l'anteprima dell'argomento attivo in una finestra affiancata usando l'estensione DocFX.  Se l'estensione DocFX non è installata oppure se è installata ma e disabilitata, non viene eseguito il rendering dell'argomento.


## <a name="how-to-assign-keyboard-shortcuts"></a>Come assegnare tasti di scelta rapida

1. Digitare `CTRL+K` e quindi `CTRL+S` per aprire l'elenco dei tasti di scelta rapida.
1. Cercare il comando, ad esempio `formatBold`, per il quale si vuole creare un tasto di scelta rapida personalizzato.
1. Fare clic sul segno più visualizzato accanto al nome del comando quando si passa il mouse sulla linea.
1. Dopo che è stata visualizzata una nuova casella di input, digitare il tasto di scelta rapida che si vuole associare a quel comando specifico. Ad esempio, per usare il tasto di scelta rapida comune per il grassetto, digitare `ctrl+b`.
1. È una buona idea inserire una clausola `when` tasto di scelta rapida, in modo che questo sia disponibile solo in file Markdown. A tale scopo, aprire *keybindings.json* e inserire la linea seguente sotto il nome del comando, assicurandosi di aggiungere una virgola tra le linee:
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Il tasto di scelta rapida completato deve avere l'aspetto seguente nel file keybindings.json:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Salvare keybindings.json.

Per altre informazioni, vedere [Keybindings](https://code.visualstudio.com/docs/getstarted/keybindings) (Tasti di scelta rapida) nella documentazione di VS Code.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Come visualizzare la barra degli strumenti legacy di "Gauntlet"

Gli utenti che in precedenza usavano il codice di estensione denominato "Gauntlet" noteranno che la barra degli strumenti di creazione non viene più visualizzata nella parte inferiore della finestra di VS Code quando è installata l'estensione Docs Markdown. Il motivo è che la barra degli strumenti occupava molto spazio nella barra di stato di VS Code e non seguiva le procedure consigliate per l'esperienza utente dell'estensione. È stata quindi dichiarata deprecata nella nuova estensione. Facoltativamente, tuttavia, è possibile visualizzare la barra degli strumenti aggiornando il file settings.json di VS Code come segue:

1. In VS Code passare a File -> Preferenze -> Impostazioni (`CTRL+Comma`).
1. Selezionare Impostazioni utente per modificare le impostazioni per tutte le aree di lavoro di VS Code oppure Impostazioni area di lavoro per modificarle solo per l'area di lavoro corrente.
1. Nel riquadro Impostazioni predefinite trovare Docs Authoring Extension Configuration (Configurazione estensione creazione Docs) e selezionare l'icona della matita accanto all'impostazione desiderata. Verrà quindi richiesto di selezionare `true` o `false`. VS Code aggiungerà automaticamente il valore della selezione al file settings.json e verrà richiesto di ricaricare la finestra per rendere effettive le modifiche.

## <a name="known-issues"></a>Problemi noti

- Anteprima di DocFX: in MacOS e Linux l'anteprima di DocFX non viene avviata correttamente. Per impostazione predefinita, per queste piattaforme viene usata l'anteprima Markdown di VS Code.
- Anteprima di DocFX: in tutte le piattaforme, nell'anteprima di alcuni elementi della sintassi, ad esempio i collegamenti xref (riferimenti incrociati) ad API, il rendering non viene eseguito correttamente, con lacune di contenuto in alcuni casi.
- Segnalibri esterni: in Linux l'elenco file viene visualizzato, ma non vengono visualizzate intestazioni da selezionare.
- File di inclusione: in Linux l'elenco file viene visualizzato, ma non viene aggiunto alcun collegamento dopo la selezione.
