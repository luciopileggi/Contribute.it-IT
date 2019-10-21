---
title: Linee guida specifiche per la scrittura di esempi di script
description: Questo articolo include le regole specifiche per la formattazione degli esempi di codice di PowerShell. Tali regole sono valide sia per gli articoli concettuali con esempi, che per le informazioni di riferimento sui cmdlet.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290266"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="c833e-104">Formattazione degli esempi di codice</span><span class="sxs-lookup"><span data-stu-id="c833e-104">Formatting code samples</span></span>

<span data-ttu-id="c833e-105">Nella documentazione esistente sono stati usati più stili nel tempo e le regole di formattazione sono cambiate più volte.</span><span class="sxs-lookup"><span data-stu-id="c833e-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="c833e-106">L'obiettivo è quello di definire uno stile coerente per i blocchi di codice e l'output di PowerShell nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="c833e-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="c833e-107">Markdown supporta due stili di codice diversi:</span><span class="sxs-lookup"><span data-stu-id="c833e-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="c833e-108">Intervalli di codice (inline) contrassegnati da un singolo carattere di apice inverso (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="c833e-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="c833e-109">Stile usato inline in un paragrafo anziché come blocco autonomo.</span><span class="sxs-lookup"><span data-stu-id="c833e-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="c833e-110">Usato più di frequente per racchiudere i nomi dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c833e-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="c833e-111">Vedere [Formattazione degli elementi della sintassi dei comandi ](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="c833e-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="c833e-112">Blocchi di codice, ovvero un blocco di più righe racchiuso tra stringhe con triplo apice inverso (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="c833e-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="c833e-113">Uso di blocchi di codice</span><span class="sxs-lookup"><span data-stu-id="c833e-113">Using code blocks</span></span>

<span data-ttu-id="c833e-114">Markdown consente di applicare il rientro per evidenziare un blocco di codice, ma questo modello può essere problematico ed è consigliabile evitarlo.</span><span class="sxs-lookup"><span data-stu-id="c833e-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="c833e-115">Tutti i blocchi di codice devono essere contenuti in una sequenza di delimitazione del codice.</span><span class="sxs-lookup"><span data-stu-id="c833e-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="c833e-116">Con codice delimitato si intende un blocco di codice racchiuso tra stringhe con triplo apice inverso (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="c833e-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="c833e-117">Gli indicatori di codice delimitato devono trovarsi sulla stessa riga, prima e dopo l'esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="c833e-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="c833e-118">L'indicatore all'inizio del blocco di codice può avere un'etichetta di linguaggio facoltativa.</span><span class="sxs-lookup"><span data-stu-id="c833e-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="c833e-119">Open Publishing System (OPS) di Microsoft usa l'etichetta del linguaggio per supportare la funzionalità di evidenziazione della sintassi.</span><span class="sxs-lookup"><span data-stu-id="c833e-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="c833e-120">OPS aggiunge anche un pulsante **Copy** per copiare il contenuto del blocco di codice negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c833e-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="c833e-121">In questo modo è possibile incollare rapidamente il codice in uno script per il test dell'esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="c833e-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="c833e-122">Tuttavia, non tutti gli esempi nella documentazione sono destinati a essere eseguiti in questo modo.</span><span class="sxs-lookup"><span data-stu-id="c833e-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="c833e-123">Alcuni blocchi di codice possono essere una semplice illustrazione di un concetto di PowerShell o una rappresentazione astratta della sintassi.</span><span class="sxs-lookup"><span data-stu-id="c833e-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="c833e-124">Nella documentazione vengono usati due tipi di blocchi di codice:</span><span class="sxs-lookup"><span data-stu-id="c833e-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="c833e-125">Esempi illustrativi</span><span class="sxs-lookup"><span data-stu-id="c833e-125">Illustrative examples</span></span>
2. <span data-ttu-id="c833e-126">Esempi eseguibili</span><span class="sxs-lookup"><span data-stu-id="c833e-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="c833e-127">Formattazione degli esempi illustrativi</span><span class="sxs-lookup"><span data-stu-id="c833e-127">Formatting illustrative examples</span></span>

<span data-ttu-id="c833e-128">Gli esempi illustrativi vengono usati per spiegare un concetto di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c833e-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="c833e-129">Non sono pensati per essere copiati negli Appunti per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c833e-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="c833e-130">Questo è il tipo di esempio usato più di frequente per semplici esempi facili da digitare.</span><span class="sxs-lookup"><span data-stu-id="c833e-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="c833e-131">Viene anche usato per esempi di sintassi in cui viene illustrata la sintassi di un comando.</span><span class="sxs-lookup"><span data-stu-id="c833e-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="c833e-132">Gli esempi illustrativi usano una sequenza di delimitazione del codice "vuota" per contrassegnare l'inizio e la fine del blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="c833e-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="c833e-133">Il blocco di codice può contenere l'output di esempio del comando illustrato.</span><span class="sxs-lookup"><span data-stu-id="c833e-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="c833e-134">Blocco di sintassi</span><span class="sxs-lookup"><span data-stu-id="c833e-134">Syntax block</span></span>

<span data-ttu-id="c833e-135">Questo esempio illustra tutti i possibili parametri del cmdlet `Get-Command`.</span><span class="sxs-lookup"><span data-stu-id="c833e-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="c833e-136">In questo esempio viene illustrata l'istruzione `for` in termini generalizzati:</span><span class="sxs-lookup"><span data-stu-id="c833e-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="c833e-137">Esempio di illustrazione semplice</span><span class="sxs-lookup"><span data-stu-id="c833e-137">Simple illustration example</span></span>

<span data-ttu-id="c833e-138">Di seguito è riportato un esempio che illustra gli operatori di confronto di PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c833e-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="c833e-139">Si noti che questo esempio include il prompt di PowerShell semplificato e mostra l'output risultante.</span><span class="sxs-lookup"><span data-stu-id="c833e-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="c833e-140">In questo caso, non è previsto che il lettore copi ed esegua l'esempio.</span><span class="sxs-lookup"><span data-stu-id="c833e-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="c833e-141">Formattazione degli esempi eseguibili</span><span class="sxs-lookup"><span data-stu-id="c833e-141">Formatting executable examples</span></span>

<span data-ttu-id="c833e-142">Per gli esempi più complessi o per quelli di utilità progettati per poter essere copiati ed eseguiti, è previsto l'uso del markup dello stile di blocco seguente:</span><span class="sxs-lookup"><span data-stu-id="c833e-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="c833e-143">L'output visualizzato dai comandi di PowerShell deve essere racchiuso in un blocco di codice **Output** per evitare l'evidenziazione della sintassi.</span><span class="sxs-lookup"><span data-stu-id="c833e-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="c833e-144">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c833e-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="c833e-145">L'etichetta del codice **Output** non è una "linguaggio" ufficiale supportato dal sistema di evidenziazione della sintassi.</span><span class="sxs-lookup"><span data-stu-id="c833e-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="c833e-146">Questa etichetta è tuttavia utile perché OPS aggiunge l'etichetta "Output" alla casella del codice nella pagina Web</span><span class="sxs-lookup"><span data-stu-id="c833e-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="c833e-147">e per questa casella del codice "Output" non è prevista alcuna evidenziazione della sintassi.</span><span class="sxs-lookup"><span data-stu-id="c833e-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="c833e-148">Regole di stile di codifica</span><span class="sxs-lookup"><span data-stu-id="c833e-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="c833e-149">Evitare la continuazione di riga negli esempi di codice</span><span class="sxs-lookup"><span data-stu-id="c833e-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="c833e-150">Evitare di usare i caratteri di continuazione di riga (`` ` ``) negli esempi di codice di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c833e-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="c833e-151">Si tratta di caratteri difficili da visualizzare e possono causare problemi se sono presenti spazi aggiuntivi alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="c833e-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="c833e-152">Usare la funzionalità di splatting di PowerShell per ridurre la lunghezza della riga per i cmdlet con numerosi parametri.</span><span class="sxs-lookup"><span data-stu-id="c833e-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="c833e-153">Sfruttare le opportunità di interruzione di riga naturali di PowerShell, come dopo i caratteri pipe (`|`), le parentesi graffe di apertura, le parentesi e le parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="c833e-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="c833e-154">Evitare di usare i prompt di PowerShell negli esempi</span><span class="sxs-lookup"><span data-stu-id="c833e-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="c833e-155">L'uso della stringa di prompt è sconsigliato e deve essere limitato agli scenari che hanno lo scopo di illustrare l'utilizzo della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c833e-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="c833e-156">I prompt sono necessari per esempi che illustrano comandi che modificano il prompt o quando il percorso visualizzato è significativo per lo scenario illustrato.</span><span class="sxs-lookup"><span data-stu-id="c833e-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="c833e-157">I prompt di PowerShell devono essere usati solo negli esempi illustrativi.</span><span class="sxs-lookup"><span data-stu-id="c833e-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="c833e-158">Per la maggior parte di questi esempi, la stringa di prompt deve essere "`PS>`".</span><span class="sxs-lookup"><span data-stu-id="c833e-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="c833e-159">Questo prompt è indipendente dagli indicatori specifici del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c833e-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="c833e-160">I prompt **NON** devono essere usati negli esempi eseguibili.</span><span class="sxs-lookup"><span data-stu-id="c833e-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="c833e-161">L'esempio seguente illustra come cambia il prompt quando si usa il provider del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c833e-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="c833e-162">Non usare alias negli esempi</span><span class="sxs-lookup"><span data-stu-id="c833e-162">Do not use aliases in examples</span></span>

<span data-ttu-id="c833e-163">È sempre consigliabile usare il nome completo di tutti i cmdlet e i parametri, a meno che l'esempio non sia pensato per illustrare in modo specifico l'alias.</span><span class="sxs-lookup"><span data-stu-id="c833e-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="c833e-164">I nomi di cmdlet e parametri devono usare l'ortografia con la combinazione di maiuscole/minuscole Pascal corretta definita nel codice.</span><span class="sxs-lookup"><span data-stu-id="c833e-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="c833e-165">Uso dei parametri negli esempi</span><span class="sxs-lookup"><span data-stu-id="c833e-165">Using parameters in examples</span></span>

<span data-ttu-id="c833e-166">Evitare di usare parametri posizionali.</span><span class="sxs-lookup"><span data-stu-id="c833e-166">Avoid using positional parameters.</span></span> <span data-ttu-id="c833e-167">In generale, è consigliabile usare sempre il nome del parametro in un esempio, anche se il parametro è posizionale.</span><span class="sxs-lookup"><span data-stu-id="c833e-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="c833e-168">In questo modo si riduce la possibilità di confusione negli esempi.</span><span class="sxs-lookup"><span data-stu-id="c833e-168">This reduces the chance of confusion in your examples.</span></span>
