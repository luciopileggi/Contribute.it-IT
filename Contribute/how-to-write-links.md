---
title: Come usare collegamenti nella documentazione
description: Questo articolo rappresenta materiale sussidiario per la creazione di collegamenti a contenuto all'interno di docs.microsoft.com.
ms.date: 06/29/2017
ms.openlocfilehash: 92c23f2b91c67d7a1695c5f1e5dcdc80a8517f6e
ms.sourcegitcommit: 37cd16636d7dcfc5222ef5a5d60e4ff30f74485c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2018
ms.locfileid: "48030934"
---
# <a name="using-links-in-documentation"></a>Uso di collegamenti nella documentazione
Questo articolo descrive come usare collegamenti ipertestuali da pagine ospitate in docs.microsoft.com. È facile aggiungere collegamenti all'interno di markdown, con alcune convenzioni. I collegamenti possono indirizzare gli utenti a contenuto all'interno della stessa pagina, ad altre pagine vicine o a siti e URL esterni.

Il back-end del sito docs.microsoft.com usa Open Publishing Services (OPS), che implementa DocFX Flavored Markdown (DFM). DFM ha un'elevata compatibilità con GitHub Flavored Markdown (GFM) e aggiunge altre funzionalità tramite estensioni Markdown.

> [!IMPORTANT]
> Tutti i collegamenti devono essere protetti (`https` invece di `http`) ogni volta che la destinazione lo supporta (come dovrebbe essere nella maggior parte dei casi).

## <a name="link-text"></a>Testo del collegamento

Le parole che vengono incluse nel testo del collegamento devono essere semplici. Devono quindi essere parole normali o il titolo della pagina alla quale porta il collegamento.

> [!IMPORTANT]
> Non usare "fare clic qui". È una scelta inefficace per l'ottimizzazione dei motori di ricerca e non descrive adeguatamente la destinazione.

**Corretto:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Non corretto:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Collegamenti da un articolo a un altro

Per creare un collegamento inline da un articolo tecnico di Docs a un altro articolo tecnico di Docs all'interno dello stesso docset, usare la sintassi seguente per i collegamenti:

- Un articolo in una directory si collega a un altro articolo nella stessa directory:

  `[link text](article-name.md)`

- Un articolo si collega da una sottodirectory a un articolo nella directory radice:

  `[link text](../article-name.md)`

- Un articolo nella directory radice si collega a un articolo in una sottodirectory:

  `[link text](./directory/article-name.md)`

- Un articolo in una sottodirectory si collega a un articolo in un'altra sottodirectory:

  `[link text](../directory/article-name.md)`

- Un articolo che si collega a più docset (anche se nello stesso repository): `[link text](./directory/article-name)`

> [!IMPORTANT]
> Nessuno degli esempi precedenti utilizza `~/` come parte del collegamento. Se ci si collega a un percorso alla radice del repository, iniziare con `/`. Quando ci si sposta nei repository di origine in GitHub, l'inserimento di `~/` genera collegamenti non validi. Iniziare il percorso con `/` risolve correttamente il problema.

## <a name="links-to-anchors"></a>Collegamenti agli ancoraggi

Non è necessario creare ancoraggi. Vengono generati automaticamente in fase di pubblicazione per tutti i titoli H2. L'unica operazione necessaria è creare collegamenti alle sezioni H2.

- Per impostare un collegamento a un titolo nello stesso articolo:

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- Per impostare un collegamento a un ancoraggio in un altro articolo nella stessa sottodirectory:

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- Per impostare un collegamento a un ancoraggio nella sottodirectory di un altro servizio:

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Collegamenti da file di inclusione

Dato che i file di inclusione sono posizionati in un'altra directory, è necessario usare percorsi relativi più lunghi. Per impostare un collegamento a un articolo da un file di inclusione, usare questo formato:

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Collegamenti nei selettori

In presenza di selettori incorporati in un file di inclusione, come quelli usati dal team della documentazione di Azure, è necessario usare la struttura seguente per i collegamenti:

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Testo1 | Esempio1)](../articles/folder/article-name1.md)
    - [(Testo1 | Esempio2)](../articles/folder/article-name2.md)
    - [(Testo2 | Esempio3)](../articles/folder/article-name3.md)
    - [(Testo2 | Esempio4)](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Collegamenti in stile riferimento

È possibile usare i collegamenti in stile riferimento per rendere più leggibile il contenuto di origine. I collegamenti in stile riferimento sostituiscono la sintassi dei collegamenti inline con una sintassi semplificata che consente di spostare gli URL lunghi alla fine dell'articolo. Ecco un esempio tratto da [Daring Fireball](https://daringfireball.net/projects/markdown/):

Testo inline:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Collegamenti di riferimento alla fine dell'articolo:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Assicurarsi di includere lo spazio dopo i due punti, prima del collegamento. Quando si imposta un collegamento ad altri articoli tecnici, se si dimentica di includere lo spazio il collegamento non funzionerà nell'articolo pubblicato.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Collegamenti a pagine non incluse nel set di documentazione tecnica

Per impostare un collegamento a una pagina in un'altra area di proprietà Microsoft, ad esempio una pagina dei prezzi, la pagina del contratto di servizio o qualsiasi altro contenuto che non sia un articolo della documentazione, usare un URL assoluto omettendo le impostazioni locali. L'obiettivo è che i collegamenti funzionino in GitHub e nel sito di rendering:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Collegamenti a siti di terze parti

Per un'esperienza utente ottimale, è consigliabile evitare il più possibile i reindirizzamenti degli utenti a un altro sito. Basare quindi i collegamenti a siti di terze parti, a volte necessari, su queste informazioni:

- **Responsabilità:**: impostare un collegamento a contenuti di terze parti quando le informazioni da condividere sono di proprietà di terzi. Ad esempio, non è compito di Microsoft comunicare agli utenti come usare gli strumenti per sviluppatori Android, è una responsabilità di Google. Se necessario, Microsoft può spiegare come usare gli strumenti per sviluppatori di Android *con* Azure, ma è Google ad avere la responsabilità di pubblicare contenuti con istruzioni per l'uso dei suoi strumenti.
- **Approvazione del PM**: richiedere che Microsoft approvi il contenuto di terze parti. Con l'inserimento di questo tipo di collegamenti Microsoft fa una dichiarazione implicita in merito all'attendibilità del contenuto collegato e si impegna nei confronti dei clienti che seguono le istruzioni.
- **Verifica dello stato di aggiornamento**: assicurarsi che le informazioni di terze parti siano ancora aggiornate, corrette e pertinenti e che il collegamento non sia stato modificato.
- **Uscita dal sito**: comunicare agli utenti che stanno passando a un altro sito. Se dal contesto non risulta chiaro, aggiungere una frase esplicativa. Ad esempio, "I prerequisiti includono Android Developer Tools, scaricabile dal sito di Android Studio".
- **Passaggi successivi**: è appropriato aggiungere un collegamento, ad esempio a un blog MVP, nella sezione "Passaggi successivi". Anche in questo caso, assicurarsi che gli utenti capiscano che stanno per passare a un altro sito.
- **Informazioni legali**: la copertura legale Microsoft è disponibile in **Collegamenti a siti di Terzi** nel piè di pagina **Condizioni per l'utilizzo** in tutte le pagine di ms.com.

## <a name="links-to-msdn-or-technet"></a>Collegamenti a MSDN o TechNet

Quando è necessario inserire un collegamento a MSDN o TechNet, usare il collegamento completo all'argomento rimuovendo l'indicatore della lingua delle impostazioni locali "it-it" dal collegamento.

## <a name="links-to-azure-powershell-reference-content"></a>Collegamenti a contenuto di riferimento di Azure PowerShell

Il contenuto di riferimento di Azure PowerShell è stato sottoposto a numerose modifiche da novembre 2016. Usare le linee guida seguenti per aggiungere collegamenti a questo contenuto da altri articoli in docs.microsoft.com.

Struttura dell'URL:

* Per i cmdlet:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Per gli argomenti concettuali:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

La parte &lt;moniker-name&gt; è facoltativa. Se omessa, si verrà indirizzati alla versione più recente del contenuto. La parte &lt;service-name&gt; è uno degli esempi indicati negli URL di base seguenti:

- Contenuto di Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Contenuto di Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Contenuto di PowerShell per Azure Active Directory (AzureAD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- PowerShell per Azure Service Fabric: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- PowerShell per Azure Information Protection: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- PowerShell per i processi di database elastici di Azure: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

Quando si usano questi URL si verrà indirizzati alla versione più recente del contenuto. In questo modo non è necessario specificare un moniker di versione. E non si avranno collegamenti a contenuto concettuale che dovranno essere aggiornati in seguito a modifiche di versione.

Per creare il collegamento corretto, trovare la pagina a cui collegarsi nel browser e copiare l'URL.
Rimuovere quindi ´ "https://docs.microsoft.com" ´ e le informazioni delle impostazioni locali.

Per i collegamenti da un sommario, è necessario usare l'URL completo senza le informazioni delle impostazioni locali.

Markdown di esempio:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
