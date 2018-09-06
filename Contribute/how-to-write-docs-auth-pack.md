---
title: Docs Authoring Pack per VS Code
description: Questo articolo illustra il pacchetto di estensioni VS Code per facilitare la creazione di codice Markdown per docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.openlocfilehash: b9fedce0a73c5c4212ffd0893c745fab56677c8c
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308917"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack per VS Code

Docs Authoring Pack è una raccolta di estensioni VS Code che facilita la creazione di codice Markdown per docs.microsoft.com. Il pacchetto, [disponibile nel Marketplace di VS Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), contiene le estensioni seguenti:

- [markdownlint:](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) linter Markdown di ampia diffusione, creato da David Anson, che consente di assicurarsi che il codice Markdown segua le procedure consigliate.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): correttore ortografico completamente offline di Street Side Software.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): usa CSS di docs.microsoft.com per una visualizzazione in anteprima del Markdown più accurata, incluso il Markdown personalizzato.
- [Docs Markdown:](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) offre assistenza per la creazione di codice Markdown per contenuto docs.microsoft.com in Open Publishing System (OPS). Offre sia supporto di base che per la sintassi Markdown personalizzata in OPS. Il resto di questo argomento descrive l'estensione Docs Markdown.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): consente agli utenti di applicare contenuto modello Markdown ai nuovi file.

## <a name="prerequisites-and-assumptions"></a>Prerequisiti e presupposti

Per inserire in modo corretto collegamenti relativi, immagini e altro contenuto incorporato con l'estensione Docs Markdown, è necessario che l'area di lavoro VS Code faccia parte dell'ambito della radice del repository OPS (Open Publishing System) clonato.

Parte della sintassi supportata dall'estensione, ad esempio avvisi e frammenti di codice, è sintassi Markdown per OPS personalizzata il cui rendering viene eseguito correttamente solo con la pubblicazione tramite OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Come usare l'estensione Docs Markdown

Per accedere al menu Docs Markdown, digitare `ALT+M`. Per selezionare una funzione, è possibile fare clic su di essa o usare Freccia GIÙ/Freccia SU. Per creare un filtro è sufficiente digitare e quindi premere `ENTER` quando la funzione voluta viene evidenziata nel menu. Sono disponibili le funzioni seguenti:

|Funzione     |Descrizione           |
|-------------|----------------------|
|Anteprima      |Visualizza l'anteprima dell'argomento attivo in una finestra affiancata usando l'estensione Docs Preview. Questa opzione è disponibile solo se l'estensione Docs Preview è installata.|
|Grassetto         |Formatta il testo in **grassetto**.|
|Corsivo       |Formatta il testo in *corsivo*.|
|Codice         |Se è selezionata fino a una riga di testo, questa viene formattata come `inline code`.<br><br>Se sono selezionate più righe, queste vengono formattate come blocco di codice delimitato e, facoltativamente, è possibile selezionare un linguaggio di programmazione supportato da OPS.|
|Avviso        |Inserisce una nota, un'informazione importante, un avviso o un suggerimento.<br><br>Selezionare il comando relativo all'avviso dal menu e quindi selezionare il tipo di avviso. Se in precedenza è stato selezionato del testo, questo viene racchiuso all'interno della sintassi del tipo di avviso selezionato. Se non è selezionato alcun testo, viene aggiunto un nuovo avviso con testo segnaposto.|
|Elenco numerato|Inserisce un nuovo elenco numerato.<br><br> Se sono selezionate più righe, ognuna costituisce un elemento dell'elenco. Si noti che nel codice Markdown gli elementi dell'elenco numerato hanno tutti il numero 1. Nel rendering in docs.microsoft.com, tuttavia, hanno numeri in sequenza o, per gli elenchi annidati, lettere in sequenza. Per creare un elenco numerato annidato, premere TAB all'interno dell'elenco padre.|
|Elenco puntato|Inserisce un nuovo elenco puntato.|
|Tabella        |Inserisce la struttura Markdown di una tabella.<br><br>Dopo aver inserito il comando per la tabella, specificare il numero di colonne e di righe nel formato colonne:righe, ad esempio 3:4. Si noti che il numero massimo di colonne che è possibile specificare tramite questa estensione è 5, che rappresenta il limite massimo consigliato per la leggibilità.|
|Collegamento a file nel repository|Inserisce un collegamento relativo a un altro file nel repository corrente. Dopo aver selezionato questa opzione, digitare nella finestra di comando in modo da filtrare i file per nome e quindi selezionare il file voluto. In presenza di testo selezionato in precedenza, questo diventerà il testo del collegamento. In caso contrario, come testo del collegamento verrà usato il titolo H1 del file di destinazione.|
|Collegamento a pagina Web    |Inserisce un collegamento a una pagina Web. Dopo aver selezionato questa opzione, incollare o digitare l'URI nella finestra di comando. `https://` è obbligatorio. In presenza di testo selezionato in precedenza, questo diventerà il testo del collegamento. In caso contrario, come testo del collegamento verrà usato l'URI.|
|Collegamento a titolo     |Aggiunge un collegamento a un segnalibro nel file corrente o in un altro file nel repository.<br>`Bookmark in this file`: scegliere da un elenco di intestazioni nel file corrente per inserire un segnalibro formattato in modo corretto.<br>`Bookmark in another file`: prima filtrare in base al nome e selezionare il file a cui collegarsi e quindi scegliere l'intestazione appropriata all'interno del file selezionato.|
|Immagine        |Digitare testo alternativo (necessario per l'accessibilità) e selezionarlo, quindi chiamare questo comando per filtrare l'elenco dei file di immagine supportati presenti nel repository e selezionare il file voluto. Se quando si chiama questo comando non è stato selezionato testo alternativo, verrà richiesto di farlo per poter selezionare un file di immagine.|
|Inclusione      |Consente di trovare un file da incorporare nel file corrente.|
|Frammento di codice      |Consente di trovare un frammento di codice nel repository da incorporare nel file corrente.|
|Video        |Aggiunge un video incorporato.|
|Modello     |Crea un nuovo file e applica un modello di Markdown. Per altre informazioni, vedere [Modelli](#how-to-use-docs-templates) di seguito.|

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

## <a name="how-to-show-the-legacy-toolbar"></a>Come visualizzare la barra degli strumenti legacy

Gli utenti della versione precedente dell'estensione noteranno che la barra degli strumenti di creazione non viene più visualizzata nella parte inferiore della finestra di VS Code quando è installata l'estensione Docs Markdown. Il motivo è che la barra degli strumenti occupava molto spazio nella barra di stato di VS Code e non seguiva le procedure consigliate per l'esperienza utente dell'estensione. È stata quindi dichiarata deprecata nella nuova estensione. Facoltativamente, tuttavia, è possibile visualizzare la barra degli strumenti aggiornando il file settings.json di VS Code come segue:

1. In VS Code passare a File -> Preferenze -> Impostazioni (`CTRL+Comma`).
1. Selezionare Impostazioni utente per modificare le impostazioni per tutte le aree di lavoro di VS Code oppure Impostazioni area di lavoro per modificarle solo per l'area di lavoro corrente.
1. Nel riquadro Impostazioni predefinite trovare Docs Authoring Extension Configuration (Configurazione estensione creazione Docs) e selezionare l'icona della matita accanto all'impostazione desiderata. Verrà quindi richiesto di selezionare `true` o `false`. VS Code aggiungerà automaticamente il valore della selezione al file settings.json e verrà richiesto di ricaricare la finestra per rendere effettive le modifiche.

## <a name="how-to-use-docs-templates"></a>Come usare i modelli di Docs

L'estensione Docs Article Templates consente ai redattori che usano VS Code di eseguire il pull di un modello di Markdown da un archivio centralizzato e applicarlo a un file. I modelli sono utili per assicurarsi che i metadati richiesti siano inclusi negli articoli, che siano rispettati gli standard per il contenuto e così via. I modelli sono gestiti come file Markdown in un repository GitHub pubblico.

### <a name="to-apply-a-template-in-vs-code"></a>Per applicare un modello in VS Code

1. Se l'estensione Docs Markdown non è installata, premere F1 per aprire il riquadro comandi, iniziare a digitare "template" per filtrare e quindi fare clic su `Docs: Template`. Se l'estensione Docs Markdown è installata, è possibile usare il riquadro comandi o fare clic su `Alt+M` per visualizzare il menu Docs Markdown QuickPick e quindi selezionare `Template` nell'elenco.
1. Selezionare il modello desiderato nell'elenco visualizzato.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Per aggiungere l'ID GitHub e/o l'alias Microsoft alle impostazioni di VS Code

L'estensione Templates supporta tre campi di metadati dinamici: author, ms.author e ms.date. Questo significa che se un autore di modelli usa questi campi nell'intestazione dei metadati di un modello di Markdown, i campi verranno popolati automaticamente nel file quando si applica il modello, come segue:

|Metadati  |Valore|
|----------|---------------|
|author    |ID GitHub, se specificato nel file di impostazioni di VS Code.|
|ms.author |Alias Microsoft, se specificato nel file di impostazioni di VS Code. Se non si è un dipendente Microsoft, non specificare questo campo.|
|ms.date   |Data corrente nel formato supportato da Docs, MM/GG/AAAA. Si noti che la data non viene aggiornata automaticamente se si aggiorna il file in seguito, ma è necessario aggiornarla manualmente per indicare la data di aggiornamento del file.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>Per impostare author (ID GitHub) e/o ms.author (alias Microsoft)

1. In VS Code passare a File -> Preferenze -> Impostazioni (`CTRL+Comma`).
1. Selezionare Impostazioni utente per modificare le impostazioni per tutte le aree di lavoro di VS Code oppure Impostazioni area di lavoro per modificarle solo per l'area di lavoro corrente.
1. Nel riquadro Impostazioni predefinite sulla sinistra trovare Docs Article Templates Extension Configuration (Configurazione dell'estensione Docs Article Templates), fare clic sull'icona a forma di matita accanto all'impostazione desiderata e quindi fare clic su Sostituisci in Impostazioni.
1. Il riquadro Impostazioni utente verrà aperto a fianco, con una nuova voce nella parte inferiore.
1. Aggiungere l'ID GitHub o l'alias di posta elettronica Microsoft, come appropriato, e salvare il file.
1. Potrebbe essere necessario chiudere e riavviare VS Code per rendere effettive le modifiche.
1. A questo punto, quando si applica un modello che usa campi dinamici, l'ID GitHub e/o l'alias Microsoft verranno popolati automaticamente nell'intestazione dei metadati.
