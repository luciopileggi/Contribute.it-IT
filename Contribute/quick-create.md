---
title: 'Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault | Microsoft Docs'
description: 'Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308825"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="00840-103">Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="00840-104">Questa guida introduttiva illustra come archiviare un segreto in Key Vault e come recuperarlo usando un'app Web.</span><span class="sxs-lookup"><span data-stu-id="00840-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="00840-105">Per visualizzare il valore del segreto, è necessario eseguire la procedura in Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="00840-106">La guida introduttiva usa Node.js e identità del servizio gestite</span><span class="sxs-lookup"><span data-stu-id="00840-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="00840-107">Creare un insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="00840-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="00840-108">Archiviare un segreto in Key Vault.</span><span class="sxs-lookup"><span data-stu-id="00840-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="00840-109">Recuperare un segreto da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="00840-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="00840-110">Creare un'applicazione Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="00840-111">[Abilitare le identità del servizio gestite](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="00840-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="00840-112">Concedere le autorizzazioni necessarie per l'applicazione Web per la lettura dei dati da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="00840-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="00840-113">Prima di procedere, assicurarsi di avere familiarità con i [concetti di base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="00840-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="00840-114">Per capire i motivi per cui l'esercitazione seguente rappresenta la procedura consigliata, è necessario comprendere alcuni concetti.</span><span class="sxs-lookup"><span data-stu-id="00840-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="00840-115">Key Vault è un repository centrale per archiviare i segreti a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="00840-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="00840-116">Per farlo, tuttavia, le applicazioni o gli utenti devono prima autenticarsi in Key Vault, ad esempio presentando un segreto.</span><span class="sxs-lookup"><span data-stu-id="00840-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="00840-117">Per seguire le procedure consigliate per la sicurezza, questo primo segreto deve essere ruotato periodicamente.</span><span class="sxs-lookup"><span data-stu-id="00840-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="00840-118">Con l'[identità del servizio gestita](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), alle applicazioni in esecuzione in Azure viene assegnata un'identità gestita automaticamente da Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="00840-119">Ciò aiuta a risolvere il **problema di introduzione del segreto**, con utenti o applicazioni che possono seguire le procedure consigliate senza doversi preoccupare della rotazione del primo segreto</span><span class="sxs-lookup"><span data-stu-id="00840-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00840-120">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="00840-120">Prerequisites</span></span>

<span data-ttu-id="00840-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="00840-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="00840-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="00840-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="00840-123">[Visual Studio 2017 versione 15.7.3 o successiva](https://www.microsoft.com/net/download/windows) con i carichi di lavoro seguenti:</span><span class="sxs-lookup"><span data-stu-id="00840-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="00840-124">Sviluppo Web e ASP.NET</span><span class="sxs-lookup"><span data-stu-id="00840-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="00840-125">Sviluppo multipiattaforma .NET Core</span><span class="sxs-lookup"><span data-stu-id="00840-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="00840-126">[.NET Core 2.1 SDK o versioni successive](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="00840-127">Git ([download](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="00840-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="00840-128">Una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-128">An Azure subscription.</span></span> <span data-ttu-id="00840-129">Se non si ha una sottoscrizione di Azure, creare un [account gratuito](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) prima di iniziare.</span><span class="sxs-lookup"><span data-stu-id="00840-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="00840-130">[Interfaccia della riga di comando di Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) versione 2.0.4 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="00840-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="00840-131">È disponibile per Windows, Mac e Linux.</span><span class="sxs-lookup"><span data-stu-id="00840-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="00840-132">Accesso ad Azure</span><span class="sxs-lookup"><span data-stu-id="00840-132">Login to Azure</span></span>

<span data-ttu-id="00840-133">Per accedere ad Azure tramite l'interfaccia della riga di comando è possibile digitare:</span><span class="sxs-lookup"><span data-stu-id="00840-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="00840-134">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="00840-134">Create resource group</span></span>

<span data-ttu-id="00840-135">Creare un gruppo di risorse usando il comando [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="00840-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="00840-136">Un gruppo di risorse di Azure è un contenitore logico in cui vengono distribuite e gestite risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="00840-137">Selezionare il nome di un gruppo di risorse e compilare il segnaposto.</span><span class="sxs-lookup"><span data-stu-id="00840-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="00840-138">L'esempio seguente crea un gruppo di risorse denominato *<YourResourceGroupName>* nella località *eastus*.</span><span class="sxs-lookup"><span data-stu-id="00840-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="00840-139">In tutta l'esercitazione viene usato il gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="00840-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="00840-140">Creare un Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="00840-141">Successivamente si crea un'istanza di Key Vault usando il gruppo di risorse creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="00840-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="00840-142">Anche se in tutto l'articolo viene usato "ContosoKeyVault" come nome per l'istanza di Key Vault, è necessario usare un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="00840-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="00840-143">Specificare le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="00840-143">Provide the following information:</span></span>

* <span data-ttu-id="00840-144">Nome dell'istanza di Key Vault - **Selezionare qui un nome per l'istanza di Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="00840-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="00840-145">Nome gruppo di risorse - **Selezionare qui un nome di gruppo di risorse**.</span><span class="sxs-lookup"><span data-stu-id="00840-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="00840-146">Località - **Stati Uniti orientali**.</span><span class="sxs-lookup"><span data-stu-id="00840-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="00840-147">A questo punto, l'account di Azure è l'unico autorizzato a eseguire qualsiasi operazione su questo nuovo insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="00840-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="00840-148">Aggiungere un segreto all'insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="00840-148">Add a secret to key vault</span></span>

<span data-ttu-id="00840-149">Verrà aggiunto un segreto per illustrare il funzionamento di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00840-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="00840-150">Si potrebbe archiviare una stringa di connessione SQL o qualsiasi altra informazione che è necessario conservare in modo sicuro, rendendola però disponibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="00840-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="00840-151">In questa esercitazione la password sarà denominata **AppSecret** e archivierà il valore **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="00840-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="00840-152">Digitare i comandi seguenti per creare un segreto in Key Vault chiamato **AppSecret** che archivierà il valore **MySecret**:</span><span class="sxs-lookup"><span data-stu-id="00840-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="00840-153">Per visualizzare il valore contenuto nel segreto come testo normale:</span><span class="sxs-lookup"><span data-stu-id="00840-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="00840-154">Questo comando mostra le informazioni del segreto, incluso l'URI.</span><span class="sxs-lookup"><span data-stu-id="00840-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="00840-155">Dopo aver completato questi passaggi sarà disponibili un URI per un segreto in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="00840-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="00840-156">Annotare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="00840-156">Write this information down.</span></span> <span data-ttu-id="00840-157">Saranno necessarie in un passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="00840-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="00840-158">Clonare il repository</span><span class="sxs-lookup"><span data-stu-id="00840-158">Clone the Repo</span></span>

<span data-ttu-id="00840-159">Clonare il repository per creare una copia locale e modificare l'origine eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="00840-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="00840-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="00840-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="00840-161">Installare le dipendenze</span><span class="sxs-lookup"><span data-stu-id="00840-161">Install dependencies</span></span>

<span data-ttu-id="00840-162">Qui si installano le dipendenze.</span><span class="sxs-lookup"><span data-stu-id="00840-162">Here we install the dependencies.</span></span> <span data-ttu-id="00840-163">Eseguire il comando cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="00840-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="00840-164">Questo progetto usa 2 moduli Node:</span><span class="sxs-lookup"><span data-stu-id="00840-164">This project used 2 node modules:</span></span>

* [<span data-ttu-id="00840-165">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="00840-165">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="00840-166">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="00840-166">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="00840-167">Pubblicare l'applicazione Web in Azure</span><span class="sxs-lookup"><span data-stu-id="00840-167">Publish the web application to Azure</span></span>

<span data-ttu-id="00840-168">Di seguito sono riportati i pochi passaggi necessari</span><span class="sxs-lookup"><span data-stu-id="00840-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="00840-169">Il primo passaggio consiste nel creare un piano del [servizio app di Azure](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="00840-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="00840-170">In questo piano è possibile archiviare più app Web.</span><span class="sxs-lookup"><span data-stu-id="00840-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="00840-171">Successivamente verrà creata un'app Web.</span><span class="sxs-lookup"><span data-stu-id="00840-171">Next we create a web app.</span></span> <span data-ttu-id="00840-172">Nell'esempio seguente sostituire <app_name> con un nome app univoco a livello globale. I caratteri validi sono a-z, 0-9 e -.</span><span class="sxs-lookup"><span data-stu-id="00840-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="00840-173">Il runtime è impostato su NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="00840-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="00840-174">Per visualizzare tutti i runtime supportati, eseguire az webapp list-runtimes</span><span class="sxs-lookup"><span data-stu-id="00840-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="00840-175">Dopo la creazione dell'app Web, l'interfaccia della riga di comando di Azure mostra un output simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="00840-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    <span data-ttu-id="00840-176">Passare all'app Web appena creata, che dovrebbe essere funzionante.</span><span class="sxs-lookup"><span data-stu-id="00840-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="00840-177">Sostituire <app_name> con un nome app univoco.</span><span class="sxs-lookup"><span data-stu-id="00840-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="00840-178">Il comando precedente crea anche un'app abilitata per Git che consente la distribuzione in Azure dal proprio repository Git locale.</span><span class="sxs-lookup"><span data-stu-id="00840-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="00840-179">Il repository Git locale è configurato con l'URL 'https://<username>@<nome_app>.scm.azurewebsites.net/<nome_app>.git'</span><span class="sxs-lookup"><span data-stu-id="00840-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="00840-180">Creare un utente di distribuzione. Al termine del comando precedente, è possibile aggiungere una distribuzione remota di Azure al repository Git locale.</span><span class="sxs-lookup"><span data-stu-id="00840-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="00840-181">Sostituire <url> con l'URL della distribuzione remota Git ottenuto da Abilitare la distribuzione Git per l'app.</span><span class="sxs-lookup"><span data-stu-id="00840-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="00840-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-182">::: zone-end</span></span>

<span data-ttu-id="00840-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="00840-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="00840-184">Aprire e modificare la soluzione</span><span class="sxs-lookup"><span data-stu-id="00840-184">Open and edit the solution</span></span>

<span data-ttu-id="00840-185">Modificare il file program.cs per eseguire l'esempio con il nome dell'insieme di credenziali delle chiavi specifico:</span><span class="sxs-lookup"><span data-stu-id="00840-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="00840-186">Passare alla cartella key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="00840-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="00840-187">Aprire il file key-vault-dotnet-core-quickstart.sln in Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="00840-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="00840-188">Aprire il file Program.cs e aggiornare il segnaposto *YourKeyVaultName* con il nome dell'insieme di credenziali delle chiavi creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="00840-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="00840-189">Questa soluzione usa le librerie NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) e [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="00840-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="00840-190">Eseguire l'app</span><span class="sxs-lookup"><span data-stu-id="00840-190">Run the app</span></span>

<span data-ttu-id="00840-191">Dal menu principale di Visual Studio 2017 selezionare **Debug** > **Avvia** senza eseguire debug.</span><span class="sxs-lookup"><span data-stu-id="00840-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="00840-192">Quando viene visualizzato il browser, passare alla pagina **Informazioni su**.</span><span class="sxs-lookup"><span data-stu-id="00840-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="00840-193">Viene visualizzato il valore per **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="00840-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="00840-194">Pubblicare l'applicazione Web in Azure</span><span class="sxs-lookup"><span data-stu-id="00840-194">Publish the web application to Azure</span></span>

<span data-ttu-id="00840-195">Pubblicare questa app in Azure per visualizzarla come un'app Web e per verificare che venga recuperato il valore del segreto:</span><span class="sxs-lookup"><span data-stu-id="00840-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="00840-196">In Visual Studio selezionare il progetto **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="00840-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="00840-197">Selezionare **Pubblica** > **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="00840-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="00840-198">Creare un nuovo **servizio app** e quindi selezionare **Pubblica**.</span><span class="sxs-lookup"><span data-stu-id="00840-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="00840-199">Modificare il nome dell'app in **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="00840-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="00840-200">Selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="00840-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="00840-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="00840-202">Abilitare le identità del servizio gestite</span><span class="sxs-lookup"><span data-stu-id="00840-202">Enable managed service identities</span></span>

<span data-ttu-id="00840-203">Azure Key Vault consente di archiviare in modo sicuro le credenziali e altri segreti e chiavi, ma è necessario autenticare il codice in Azure Key Vault per recuperarli.</span><span class="sxs-lookup"><span data-stu-id="00840-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="00840-204">L'identità del servizio gestita semplifica questa attività, assegnando ai servizi di Azure un'identità gestita automaticamente in Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="00840-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="00840-205">È possibile usare questa identità per l'autenticazione a qualsiasi servizio che supporti l'autenticazione di Azure AD, incluso Key Vault, senza inserire le credenziali nel codice.</span><span class="sxs-lookup"><span data-stu-id="00840-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="00840-206">Tornare all'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="00840-207">Eseguire il comando assign-identity per creare l'identità per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="00840-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="00840-208">Il comando in questa procedura equivale a passare al portale e impostare **Identità del servizio gestita** su **Attivato** nelle proprietà dell'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="00840-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="00840-209">Assegnare le autorizzazioni all'applicazione per la lettura dei segreti da Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="00840-210">Prendere nota dell'output quando si pubblica l'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="00840-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="00840-211">Deve essere nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="00840-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="00840-212">Eseguire quindi questo comando usando il nome dell'insieme di credenziali delle chiavi e il valore **PrincipalId**:</span><span class="sxs-lookup"><span data-stu-id="00840-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="00840-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="00840-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="00840-214">Distribuire l'app Node in Azure e recuperare il valore del segreto</span><span class="sxs-lookup"><span data-stu-id="00840-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="00840-215">Ora che tutto è pronto,</span><span class="sxs-lookup"><span data-stu-id="00840-215">Now that everything is set.</span></span> <span data-ttu-id="00840-216">usare il comando seguente per distribuire l'app in Azure</span><span class="sxs-lookup"><span data-stu-id="00840-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="00840-217">Successivamente sarà possibile vedere il valore del segreto passando a https://<nome_app>.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="00840-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="00840-218">Assicurarsi di aver sostituito il nome <YourKeyVaultName> con il nome dell'insieme di credenziali</span><span class="sxs-lookup"><span data-stu-id="00840-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="00840-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-219">::: zone-end</span></span>

<span data-ttu-id="00840-220">::: zone pivot="dotnet" A questo punto, quando si esegue l'applicazione viene visualizzato il valore del segreto recuperato.</span><span class="sxs-lookup"><span data-stu-id="00840-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="00840-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="00840-222">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="00840-222">Next steps</span></span>

<span data-ttu-id="00840-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="00840-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="00840-224">Home page di Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="00840-225">Documentazione su Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="00840-226">Azure SDK per Node</span><span class="sxs-lookup"><span data-stu-id="00840-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="00840-227">[Informazioni di riferimento sull'API REST di Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="00840-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="00840-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="00840-229">Home page di Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="00840-230">Documentazione su Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="00840-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="00840-231">Azure SDK per .NET</span><span class="sxs-lookup"><span data-stu-id="00840-231">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="00840-232">[Informazioni di riferimento sull'API REST di Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="00840-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
