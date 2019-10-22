---
title: Linee guida specifiche per la scrittura di informazioni di riferimento sui cmdlet
description: Questo articolo include le regole specifiche per la formattazione degli esempi di codice di PowerShell. Tali regole sono valide sia per gli articoli concettuali con esempi, che per le informazioni di riferimento sui cmdlet.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290289"
---
# <a name="updating-reference-articles"></a>Aggiornamento degli articoli di riferimento

Gli articoli di riferimento sui cmdlet hanno una struttura specifica. Questa struttura è definita da [PlatyPS][].
PlatyPS è lo strumento usato da Microsoft per generare la Guida dei cmdlet per i moduli di PowerShell. PlatyPS crea il file markdown di base per un cmdlet. Dopo aver modificato i file markdown, si usa PlatyPS per creare i file della Guida MAML usati dal cmdlet `Get-Help`.

PlatyPS dispone di uno schema hardcoded per le informazioni di riferimento sui cmdlet scritte nel codice. Il documento [platyPS.schema.md][] tenta di descrivere la struttura. Le violazioni dello schema causano errori di compilazione che devono essere corretti prima di poter accettare il contributo.

## <a name="general-guidelines"></a>Linee guida generali

- Non rimuovere alcuna struttura nell'intestazione. PlatyPS prevede un set specifico di intestazioni.
- Le intestazioni **Input type** e **Output type** devono avere un tipo. Se il cmdlet non accetta input o restituisce un valore, usare il valore "None".
- I blocchi di codice delimitati sono consentiti solo nella sezione [Esempi](#format-for-examples).
- Gli intervalli di codice inline possono essere usati in qualsiasi paragrafo.

## <a name="formatting-about_-files"></a>Formattazione dei file About_

I file `About_*` vengono ora elaborati da [Pandoc][], anziché da PlatyPS. I file `About_*` sono formattati in modo da ottenere la massima compatibilità con tutte le versioni di PowerShell e con gli strumenti di pubblicazione.
Non modificare la formattazione dei file `about_*` senza verificare prima con un responsabile della manutenzione del repository.

Linee guida di base per la formattazione:

- Limitare le righe a 80 caratteri
- I blocchi di codice, le citazioni e le tabelle sono limitati a 76 caratteri perché Pandoc applica un rientro di quattro spazi a questi elementi durante la conversione
- Le tabelle devono rientrare nei 76 caratteri
  - Mandare a capo manualmente il contenuto delle celle su più righe
  - Usare i caratteri `|` di apertura e chiusura per ogni riga
  - Vedere un esempio funzionante in [about_Comparison_Operators][about-example]
- Quando si usano i caratteri speciali di Pandoc `\`, `$`, `` ` `` e `<`
  - All'interno di un'intestazione questi caratteri devono essere preceduti dal carattere di escape `\`
  - All'interno di un paragrafo questi caratteri devono essere inseriti in intervalli di codice. Ad esempio:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Formato per gli esempi

Nello schema PlatyPS l'intestazione **EXAMPLES** è un'intestazione H2 e ogni esempio è un'intestazione H3.

All'interno di un esempio, lo schema non consente la separazione dei blocchi di codice tramite paragrafi. Lo schema valido è:

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Numerare ogni esempio e aggiungere un breve titolo.

Ad esempio:

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org