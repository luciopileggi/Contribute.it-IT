---
title: Linee guida per la formattazione del testo
description: Informazioni su quando usare il grassetto, il corsivo, lo stile codice e altri stili di testo negli articoli pubblicati sul sito docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336512"
---
# <a name="text-formatting-guidelines"></a>Linee guida per la formattazione del testo

L'uso coerente e appropriato degli stili grassetto e corsivo e dello stile codice per gli elementi di testo migliora la leggibilità e la chiarezza del testo.

## <a name="bold"></a>Grassetto

Usare il grassetto per gli elementi dell'interfaccia utente, ad esempio le voci di menu, i nomi delle finestre di dialogo e i nomi dei campi di input.

### <a name="examples"></a>Esempio

* **Usare**: In **Esplora soluzioni** fare clic con il pulsante destro del mouse sul nodo del progetto e quindi scegliere **Aggiungi > Nuovo elemento**.
* **Non usare**: In Esplora soluzioni fare clic con il pulsante destro del mouse sul nodo del progetto e quindi scegliere Aggiungi > Nuovo elemento.
* **Non usare**: In *Esplora soluzioni* fare clic con il pulsante destro del mouse sul nodo del progetto e quindi scegliere *Aggiungi > Nuovo elemento*.

## <a name="italics"></a>Corsivo

Usare il corsivo per:

* Introduzione di nuovi termini con una definizione o una spiegazione.
* Nomi di file, nomi di cartelle, percorsi.
* Input utente.

### <a name="examples"></a>Esempio

* **Usare**: Nel servizio app, un'app viene eseguita in un *piano di servizio app*. Un piano di servizio app definisce un set di risorse di calcolo per l'esecuzione di un'app Web.
* **Non usare**: Nel servizio app, un'app viene eseguita in un "piano di servizio app". Un piano di servizio app definisce un set di risorse di calcolo per l'esecuzione di un'app Web.
* **Usare**: Sostituire il codice in *HttpTriggerCSharp.cs* con il codice seguente.
* **Non usare**: Sostituire il codice in `HttpTriggerCSharp.cs` con il codice seguente.
* **Usare**: Immettere *ContosoUniversity* nel campo **Nome** e quindi selezionare **Aggiungi**.
* **Non usare**: Immettere "ContosoUniversity" nel campo **Nome** e quindi selezionare **Aggiungi**.

## <a name="code-style"></a>Stile codice

Usare lo stile di codice per:

* Elementi di codice come i nomi dei metodi, i nomi delle proprietà e le parole chiave del linguaggio.
* Comandi SQL
* Nomi dei pacchetti NuGet
* Comandi della riga di comando
* Nomi di tabelle e colonne di database
* Nomi di risorse che non devono essere localizzati, come i nomi delle macchine virtuali
* URL da rendere non selezionabili

**Motivo** Nelle guide di stile precedenti era indicato di usare il grassetto per molti di questi elementi di testo. La maggior parte degli articoli viene tuttavia localizzata e lo stile di codice indica al traduttore di lasciare invariata la specifica parte del testo.

Lo stile di codice può essere *inline* (racchiuso tra \`) o su più righe separate in blocchi di codice *delimitati* (racchiusi tra \`\`\`). È consigliabile inserire gli snippet di codice e i percorsi lunghi in blocchi di codice delimitati.

### <a name="examples-using-inline-styles"></a>Esempi d'uso di stili inline

* **Usare**: Per impostazione predefinita, Entity Framework interpreta una proprietà denominata `Id` o `ClassnameID` come la chiave primaria.
* **Non usare**: Per impostazione predefinita, Entity Framework interpreta una proprietà denominata *Id* o *ClassnameID* come la chiave primaria.
* **Usare**: Il pacchetto `Microsoft.EntityFrameworkCore` garantisce il supporto runtime per EF Core.
* **Non usare**: Il pacchetto *Microsoft.EntityFrameworkCore* garantisce il supporto runtime per EF Core.

### <a name="examples-of-fenced-code-blocks"></a>Esempi di blocchi di codice delimitati

* **Usare**: Il database non riceve nessun comando dalle istruzioni che modificano solo un elemento `IQueryable`, ad esempio il codice seguente:

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **Non usare**: Il database non riceve nessun comando dalle istruzioni che modificano solo un elemento **IQueryable**, ad esempio **var students = context.Students.Where(s => s.LastName == "Davolio")** .

* **Usare**: Ad esempio, per eseguire lo script `Get-ServiceLog.ps1` nella directory `C:\Scripts` digitare:

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **Non usare**: Ad esempio, per eseguire lo script **Get-ServiceLog.ps1** nella directory **C:\Scripts** digitare: "C:\Scripts\Get-ServiceLog.ps1."

* **Tutti** i blocchi di codice delimitati devono avere un tag di linguaggio approvato. Per un elenco dei tag di linguaggio supportati, vedere [Come includere codice in Docs](./code-in-docs.md#supported-languages).

## <a name="headings-and-link-text"></a>Intestazioni e testo dei collegamenti

Non applicare uno stile inline, come il corsivo, il grassetto o lo stile di codice, al testo delle intestazioni o dei collegamenti ipertestuali.

**Motivo**

Le persone identificano gli elementi di testo come collegamenti selezionabili in base alla formattazione standard del testo del collegamento ipertestuale. Se ad esempio si formatta un collegamento con lo stile codice, può risultare difficile capire che il testo è un collegamento. Le intestazioni hanno stili propri che, se combinati con altri stili, possono restituire formattazioni non adeguate.

### <a name="examples"></a>Esempio

* **Usare**: Il file *function.json* viene generato dal pacchetto NuGet [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).
* **Non usare**: Il file *function.json* viene generato dal pacchetto NuGet [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).

* **Usare**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **Non usare**:

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>Tasti e scelte rapide da tastiera

Quando si fa riferimento a tasti o combinazioni di tasti, attenersi alle convenzioni seguenti:

* Usare l'iniziale maiuscola per i nomi dei tasti.
* Non applicare uno stile inline, come il corsivo, il grassetto o lo stile di codice.
* Usare il segno più (+) per unire i tasti che vengono premuti contemporaneamente.

### <a name="examples"></a>Esempio

* **Usare**: Premere Alt+Ctrl+S.
* **Non usare**: Premere **ALT+CTRL+S**.
* **Non usare**: Premere `ALT+CTRL+S`.

Per altre informazioni, vedere [Descrizione delle interazioni con l'interfaccia utente](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472).

## <a name="exceptions"></a>Eccezioni

Le linee guida per gli stili non sono regole rigide. Nei contesti in cui queste regole peggiorano la leggibilità, è possibile effettuare scelte differenti. Ad esempio una tabella HTML composta principalmente da elementi di codice può apparire confusa se formattata interamente con lo stile codice. In questo contesto è possibile scegliere di usare lo stile grassetto.

Se si sceglie uno stile di testo alternativo quando è normalmente richiesto lo stile di codice, assicurarsi che il testo debba essere tradotto nelle versioni localizzate dell'articolo. Lo stile di codice è l'unico stile che impedisce automaticamente la traduzione del testo. Per gli scenari in cui si vuole impedire la localizzazione senza usare lo stile di codice, vedere [Stringhe non localizzate](markdown-reference.md#non-localized-strings).
