---
title: Docs Authoring Pack per Visual Studio Code
description: Questo articolo illustra il pacchetto di estensione di Visual Studio Code che facilita la creazione di codice Markdown per docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336419"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack per VS Code

Docs Authoring Pack è una raccolta di estensioni VS Code che facilita la creazione di codice Markdown per docs.microsoft.com. Il pacchetto, [disponibile nel Marketplace di VS Code](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), contiene le estensioni seguenti:

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): offre assistenza per la creazione di codice Markdown per il contenuto di docs.microsoft.com (Docs), incluso sia il supporto di base per Markdown sia il supporto per la sintassi Markdown personalizzata in Docs, come avvisi, frammenti di codice e testo non localizzabile. Include ora anche alcune informazioni di base per la creazione di contenuto YAML, ad esempio l'inserimento di voci di sommario.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): linter Markdown di ampia diffusione, creato da David Anson, che consente di assicurarsi che il codice Markdown sia valido.
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): correttore ortografico completamente offline di Street Side Software.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): usa CSS di docs.microsoft.com per una visualizzazione in anteprima del Markdown più accurata, incluso il Markdown personalizzato.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): consente agli utenti di eseguire lo scaffolding dei moduli Learn e di applicare il contenuto dello scheletro Markdown ai nuovi file.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): offre funzionalità di completamento automatico e convalida dello schema YAML per Docs.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): offre funzionalità di compressione e ridimensionamento delle immagini per cartelle e singoli file per aiutare gli autori di docs.microsoft.com.

## <a name="prerequisites-and-assumptions"></a>Prerequisiti e presupposti

Per inserire collegamenti relativi, immagini e altro contenuto incorporato con l'estensione Docs Markdown, è necessario che l'area di lavoro VS Code faccia parte dell'ambito della radice del repository OPS (Open Publishing System) clonato. Se, ad esempio, si è clonato il repository Docs in `C:\git\SomeDocsRepo\`, aprire tale cartella o una sottocartella in VS Code: menu **File** > **Apri cartella** o `code C:\git\SomeDocsRepo\` dalla riga di comando.

Parte della sintassi supportata dall'estensione, ad esempio avvisi e frammenti di codice, è sintassi Markdown per OPS personalizzata il cui rendering viene eseguito correttamente solo con la pubblicazione tramite OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Come usare l'estensione Docs Markdown

Per accedere al menu **Docs Markdown**, digitare <kbd>ALT+M</kbd>. È possibile fare clic o usare le frecce su e giù per selezionare il comando desiderato. In alternativa è possibile digitare per iniziare a filtrare e quindi premere <kbd>INVIO</kbd> quando la funzione desiderata viene evidenziata nel menu.

Per un elenco aggiornato dei comandi, vedere il [readme di Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown).

## <a name="how-to-generate-a-master-redirect-file"></a>Come generare un file di reindirizzamento master

L'estensione Docs Markdown include uno script per generare o aggiornare un file di reindirizzamento master per un repository, in base ai metadati `redirect_url` nei singoli file. Questo script controlla ogni file Markdown nel repository per `redirect_url`, aggiunge i metadati di reindirizzamento al file di reindirizzamento master (*.openpublishing.redirection.json*) per il repository e sposta i file reindirizzati in una cartella all'esterno del repository. Per eseguire lo script:

1. Selezionare <kbd>F1</kbd> per aprire il riquadro comandi di VS Code.
2. Iniziare a digitare "Docs: Generate..."
3. Selezionare il comando `Docs: Generate master redirection file`.
4. Al termine dell'esecuzione dello script, i risultati del reindirizzamento verranno visualizzati nel riquadro di output di VS Code e i file Markdown rimossi verranno aggiunti alla cartella Authoring\redirects di Docs nel percorso predefinito.
5. Rivedere i risultati. Se sono come previsto, inviare una richiesta pull per aggiornare il repository.

## <a name="how-to-assign-keyboard-shortcuts"></a>Come assegnare tasti di scelta rapida

1. Digitare <kbd>CTRL+K</kbd> e quindi <kbd>CTRL+S</kbd> per aprire l'elenco **Tasti di scelta rapida**.
1. Cercare il comando, ad esempio `formatBold`, per il quale si vuole creare un tasto di scelta rapida personalizzato.
1. Fare clic sul segno più visualizzato accanto al nome del comando quando si passa il mouse sulla linea.
1. Dopo che è stata visualizzata una nuova casella di input, digitare il tasto di scelta rapida che si vuole associare a quel comando specifico. Ad esempio, per usare il tasto di scelta rapida comune per il grassetto, digitare <kbd>CTRL+B</kbd>.
1. È una buona idea inserire una clausola `when` nel tasto di scelta rapida, in modo che questo sia disponibile solo per i file Markdown. A tale scopo, aprire *keybindings.json* e inserire la linea seguente sotto il nome del comando, assicurandosi di aggiungere una virgola tra le linee:

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Nel file *keybindings.json* il tasto di scelta rapida completato dovrebbe avere l'aspetto seguente:

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > Inserire i tasti di scelta rapida in questo file per sovrascrivere le impostazioni predefinite

1. Salvare *keybindings.json*.

Per altre informazioni sui tasti di scelta rapida, vedere la [documentazione di VS Code](https://code.visualstudio.com/docs/getstarted/keybindings).

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Come visualizzare la barra degli strumenti legacy di "Gauntlet"

Gli utenti che in precedenza usavano il codice di estensione denominato "Gauntlet" noteranno che la barra degli strumenti di creazione non viene più visualizzata nella parte inferiore della finestra di VS Code quando è installata l'estensione Docs Markdown. Il motivo è che la barra degli strumenti occupava molto spazio nella barra di stato di VS Code e non seguiva le procedure consigliate per l'esperienza utente dell'estensione. È stata quindi dichiarata deprecata nella nuova estensione. Facoltativamente, tuttavia, è possibile visualizzare la barra degli strumenti aggiornando il file settings.json di VS Code come segue:

1. In VS Code passare a **File** > **Preferenze** > **Impostazioni** oppure premere <kbd>CTRL+,</kbd>.
1. Selezionare **Impostazioni utente** per modificare le impostazioni per tutte le aree di lavoro di VS Code oppure **Impostazioni area di lavoro** per modificarle solo per l'area di lavoro corrente.
1. Selezionare **Estensioni** > **Docs Markdown Extension Configuration** (Configurazione dell'estensione Docs Markdown) e quindi selezionare **Show the legacy toolbar in the bottom status bar** (Mostra la barra degli strumenti legacy nella barra di stato inferiore).

   ![Impostazione per mostrare la barra degli strumenti legacy in VS Code](docs-authoring/media/show-gauntlet-bar.png)

Al termine della selezione, VS Code aggiorna il file *settings.json*. Verrà quindi chiesto di ricaricare la finestra per rendere effettive le modifiche.

I comandi più recenti aggiunti all'estensione non saranno disponibili dalla barra degli strumenti.

## <a name="how-to-use-docs-templates"></a>Come usare i modelli di Docs

L'estensione Docs Article Templates consente ai redattori che usano VS Code di eseguire il pull di un modello di Markdown da un archivio centralizzato e applicarlo a un file. I modelli sono utili per assicurarsi che i metadati richiesti siano inclusi negli articoli, che siano rispettati gli standard per il contenuto e così via. I modelli sono gestiti come file Markdown in un repository GitHub pubblico.

### <a name="to-apply-a-template-in-vs-code"></a>Per applicare un modello in VS Code

1. Verificare che l'estensione Docs Article Templates sia installata e abilitata.
1. Se l'estensione Docs Markdown non è installata, premere <kbd>F1</kbd> per aprire il riquadro comandi, iniziare a digitare "template" per filtrare e quindi fare clic su `Docs: Template`. Se l'estensione Docs Markdown è installata, è possibile usare il riquadro comandi oppure premere <kbd>ALT+M</kbd> per visualizzare il menu QuickPick di Docs Markdown e quindi selezionare `Template` dall'elenco.
1. Selezionare il modello desiderato nell'elenco visualizzato.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Per aggiungere l'ID GitHub e/o l'alias Microsoft alle impostazioni di VS Code

L'estensione Templates supporta tre campi di metadati dinamici: author, ms.author e ms.date. Questo significa che se un autore di modelli usa questi campi nell'intestazione dei metadati di un modello di Markdown, i campi verranno popolati automaticamente nel file quando si applica il modello, come segue:

| Campo dei metadati | Valore |
|--|--|
| `author` | Alias GitHub, se specificato nel file di impostazioni di VS Code. |
| `ms.author` | Alias Microsoft, se specificato nel file di impostazioni di VS Code. Se non si è un dipendente Microsoft, non specificare questo campo. |
| `ms.date` | Data corrente nel formato supportato da Docs, `MM/DD/YYYY`. Si noti che la data non viene aggiornata automaticamente se si aggiorna il file in un secondo momento, ma è necessario aggiornarla manualmente. Questo campo viene usato per indicare lo stato di aggiornamento degli articoli. |

### <a name="to-set-author-andor-msauthor"></a>Per impostare author e/o ms.author

1. In VS Code passare a **File** > **Preferenze** > **Impostazioni** oppure premere <kbd>CTRL+,</kbd>.
1. Selezionare **Impostazioni utente** per modificare le impostazioni per tutte le aree di lavoro di VS Code oppure **Impostazioni area di lavoro** per modificarle solo per l'area di lavoro corrente.
1. Nel riquadro Impostazioni predefinite sulla sinistra trovare **Docs Article Templates Extension Configuration** (Configurazione dell'estensione Docs Article Templates), fare clic sull'icona a forma di matita accanto all'impostazione desiderata e quindi fare clic su Sostituisci nelle impostazioni.
1. Il riquadro **Impostazioni utente** verrà aperto a fianco, con una nuova voce nella parte inferiore.
1. Aggiungere l'ID GitHub o l'alias di posta elettronica Microsoft, come appropriato, e salvare il file.
1. Potrebbe essere necessario chiudere e riavviare VS Code per rendere effettive le modifiche.
1. A questo punto, quando si applica un modello che usa campi dinamici, l'ID GitHub e/o l'alias Microsoft verranno popolati automaticamente nell'intestazione dei metadati.

### <a name="to-make-a-new-template-available-in-vs-code"></a>Per rendere disponibile un nuovo modello in VS Code

1. Preparare il modello come file Markdown.
1. Inviare una richiesta pull alla cartella templates del repository [MicrosoftDocs/Content-Templates](https://github.com/MicrosoftDocs/content-templates).

Il team di docs.microsoft.com esaminerà il modello e unirà la richiesta pull se soddisfa le linee guida per lo stile di docs.microsoft.com. Una volta unito, il modello sarà disponibile per tutti gli utenti dell'estensione Docs Article Templates.

## <a name="demo-several-features"></a>Demo di alcune funzionalità

Ecco un breve video che illustra le funzionalità seguenti di Docs Authoring Pack:

* **File YAML**
  * Supporto per "Docs: Link to file in repo"
* **File Markdown**
  * Aggiornare l'opzione del menu di scelta rapida del valore di metadati "ms.date"
  * Supporto del completamento automatico del codice per gli identificatori di linguaggio code-fence
  * Avvisi di identificatore di linguaggio code-fence non riconosciuto/supporto per la correzione automatica
  * Ordinamento crescente della selezione (dalla A alla Z)
  * Ordinamento decrescente della selezione (dalla Z alla A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>Aspettative relative ai contributi

Docs Authoring Pack è un'estensione open source ed è disponibile per i contributi di chiunque abbia un account GitHub. Un team Microsoft interno dedicato lavora attivamente a questo progetto, monitorando i problemi e le richieste pull. Per il contratto di servizio (SLA) e per l'esame di una richiesta pull è attualmente previsto un tempo pari a una settimana. Il team è attualmente impegnato ad automatizzare il processo per migliorare questo tempo di risposta.

## <a name="next-steps"></a>Passaggi successivi

Esplorare le varie funzionalità disponibili nell'estensione Docs Authoring Pack di Visual Studio Code.

* [Completamento dei linguaggi di sviluppo](docs-authoring/dev-lang-completion.md)
* [Compressione delle immagini](docs-authoring/image-compression.md)
* [Aggiornamenti dei metadati](docs-authoring/metadata-updates.md)
* [Riformattazione delle tabelle](docs-authoring/reformat-table.md)
* [Sostituzione delle virgolette curve](docs-authoring/smart-quote-replacement.md)
* [Ordinamento dei reindirizzamenti](docs-authoring/sort-redirects.md)
* [Ordinamento della selezione](docs-authoring/sort-selection.md)
