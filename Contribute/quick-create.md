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
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805746"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="1e1e4-103">Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="1e1e4-104">Questa guida introduttiva illustra come archiviare un segreto in Key Vault e come recuperarlo usando un'app Web.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="1e1e4-105">Per visualizzare il valore del segreto, è necessario eseguire la procedura in Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="1e1e4-106">La guida introduttiva usa Node.js e identità del servizio gestite.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-106">The quickstart uses Node.js and Managed service identities (MSIs).</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="1e1e4-107">Creare un insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="1e1e4-108">Archiviare un segreto nell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-108">Store a secret in the Key Vault.</span></span>
> * <span data-ttu-id="1e1e4-109">Recuperare un segreto da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="1e1e4-110">Creare un'applicazione Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="1e1e4-111">[Abilitare le identità del servizio gestite](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="1e1e4-112">Concedere le autorizzazioni necessarie per l'applicazione Web per la lettura dei dati da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="1e1e4-113">Prima di procedere, assicurarsi di avere familiarità con i [concetti di base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="1e1e4-114">Per capire i motivi per cui l'esercitazione seguente rappresenta la procedura consigliata, è necessario comprendere alcuni concetti.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="1e1e4-115">Key Vault è un repository centrale per archiviare i segreti a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="1e1e4-116">Per farlo, tuttavia, le applicazioni o gli utenti devono prima autenticarsi in Key Vault, ad esempio presentando un segreto.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="1e1e4-117">Per seguire le procedure consigliate per la sicurezza, questo primo segreto deve essere ruotato periodicamente.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="1e1e4-118">Con l'[identità del servizio gestita](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), alle applicazioni in esecuzione in Azure viene assegnata un'identità gestita automaticamente da Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="1e1e4-119">Ciò aiuta a risolvere il **problema di introduzione del segreto**, con utenti o applicazioni che possono seguire le procedure consigliate senza doversi preoccupare della rotazione del primo segreto</span><span class="sxs-lookup"><span data-stu-id="1e1e4-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e1e4-120">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="1e1e4-120">Prerequisites</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="1e1e4-121">Node JS</span><span class="sxs-lookup"><span data-stu-id="1e1e4-121">Node JS</span></span>](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* <span data-ttu-id="1e1e4-122">[Visual Studio 2017 versione 15.7.3 o successiva](https://www.microsoft.com/net/download/windows) con i carichi di lavoro seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-122">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="1e1e4-123">Sviluppo Web e ASP.NET</span><span class="sxs-lookup"><span data-stu-id="1e1e4-123">ASP.NET and web development</span></span>
  * <span data-ttu-id="1e1e4-124">Sviluppo multipiattaforma .NET Core</span><span class="sxs-lookup"><span data-stu-id="1e1e4-124">.NET Core cross-platform development</span></span>
* [<span data-ttu-id="1e1e4-125">.NET Core 2.1 SDK o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1e1e4-125">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/windows)
::: zone-end
* <span data-ttu-id="1e1e4-126">Git ([download](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-126">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="1e1e4-127">Una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-127">An Azure subscription.</span></span> <span data-ttu-id="1e1e4-128">Se non si ha una sottoscrizione di Azure, creare un [account gratuito](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) prima di iniziare.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-128">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="1e1e4-129">[Interfaccia della riga di comando di Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) versione 2.0.4 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="1e1e4-130">È disponibile per Windows, Mac e Linux.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-130">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="1e1e4-131">Accesso ad Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-131">Login to Azure</span></span>

<span data-ttu-id="1e1e4-132">Per accedere ad Azure tramite l'interfaccia della riga di comando è possibile digitare:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-132">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="1e1e4-133">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1e1e4-133">Create resource group</span></span>

<span data-ttu-id="1e1e4-134">Creare un gruppo di risorse usando il comando [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-134">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="1e1e4-135">Un gruppo di risorse di Azure è un contenitore logico in cui vengono distribuite e gestite risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-135">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="1e1e4-136">Selezionare il nome di un gruppo di risorse e compilare il segnaposto.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-136">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="1e1e4-137">L'esempio seguente crea un gruppo di risorse denominato *<YourResourceGroupName>* nella località *eastus*.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-137">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="1e1e4-138">In tutta l'esercitazione viene usato il gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-138">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="1e1e4-139">Creare un Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-139">Create an Azure Key Vault</span></span>

<span data-ttu-id="1e1e4-140">Successivamente si crea un'istanza di Key Vault usando il gruppo di risorse creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-140">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="1e1e4-141">Anche se in tutto l'articolo viene usato "ContosoKeyVault" come nome per l'istanza di Key Vault, è necessario usare un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-141">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="1e1e4-142">Specificare le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-142">Provide the following information:</span></span>

* <span data-ttu-id="1e1e4-143">Nome dell'istanza di Key Vault - **Selezionare qui un nome per l'istanza di Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-143">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="1e1e4-144">Nome gruppo di risorse - **Selezionare qui un nome di gruppo di risorse**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-144">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="1e1e4-145">Località - **Stati Uniti orientali**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-145">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="1e1e4-146">A questo punto, l'account di Azure è l'unico autorizzato a eseguire qualsiasi operazione su questo nuovo insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-146">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="1e1e4-147">Aggiungere un segreto all'insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="1e1e4-147">Add a secret to key vault</span></span>

<span data-ttu-id="1e1e4-148">Verrà aggiunto un segreto per illustrare il funzionamento di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-148">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="1e1e4-149">Si potrebbe archiviare una stringa di connessione SQL o qualsiasi altra informazione che è necessario conservare in modo sicuro, rendendola però disponibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-149">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="1e1e4-150">In questa esercitazione la password sarà denominata **AppSecret** e archivierà il valore **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-150">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="1e1e4-151">Digitare i comandi seguenti per creare un segreto in Key Vault chiamato **AppSecret** che archivierà il valore **MySecret**:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-151">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="1e1e4-152">Per visualizzare il valore contenuto nel segreto come testo normale:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-152">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="1e1e4-153">Questo comando mostra le informazioni del segreto, incluso l'URI.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-153">This command shows the secret information including the URI.</span></span> <span data-ttu-id="1e1e4-154">Dopo aver completato questi passaggi sarà disponibili un URI per un segreto in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-154">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="1e1e4-155">Annotare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-155">Write this information down.</span></span> <span data-ttu-id="1e1e4-156">Saranno necessarie in un passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-156">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="1e1e4-157">Clonare il repository</span><span class="sxs-lookup"><span data-stu-id="1e1e4-157">Clone the Repo</span></span>

<span data-ttu-id="1e1e4-158">Clonare il repository per creare una copia locale e modificare l'origine eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-158">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a><span data-ttu-id="1e1e4-159">Installare le dipendenze</span><span class="sxs-lookup"><span data-stu-id="1e1e4-159">Install dependencies</span></span>

<span data-ttu-id="1e1e4-160">Qui si installano le dipendenze.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-160">Here we install the dependencies.</span></span> <span data-ttu-id="1e1e4-161">Eseguire i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-161">Run the following commands:</span></span>

    cd key-vault-node-quickstart
    npm install

<span data-ttu-id="1e1e4-162">Questo progetto usa 2 moduli Node:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-162">This project used 2 node modules:</span></span>

* [<span data-ttu-id="1e1e4-163">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-163">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="1e1e4-164">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-164">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="1e1e4-165">Pubblicare l'applicazione Web in Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-165">Publish the web application to Azure</span></span>

<span data-ttu-id="1e1e4-166">Di seguito sono illustrati alcuni passaggi necessari per la pubblicazione dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-166">Below are the few steps we need to do to publish the application to Azure.</span></span>

* <span data-ttu-id="1e1e4-167">Il primo passaggio consiste nel creare un piano del [servizio app di Azure](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-167">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="1e1e4-168">In questo piano è possibile archiviare più app Web.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-168">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="1e1e4-169">Successivamente verrà creata un'app Web.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-169">Next we create a web app.</span></span> <span data-ttu-id="1e1e4-170">Nell'esempio seguente sostituire <app_name> con un nome app univoco a livello globale. I caratteri validi sono a-z, 0-9 e -.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-170">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="1e1e4-171">Il runtime è impostato su NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-171">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="1e1e4-172">Per visualizzare tutti i runtime supportati, eseguire `az webapp list-runtimes`</span><span class="sxs-lookup"><span data-stu-id="1e1e4-172">To see all supported runtimes, run `az webapp list-runtimes`</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="1e1e4-173">Dopo la creazione dell'app Web, l'interfaccia della riga di comando di Azure mostra un output simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-173">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="1e1e4-174">Passare all'app Web appena creata, che dovrebbe essere funzionante.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-174">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="1e1e4-175">Sostituire <app_name> con un nome app univoco.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-175">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="1e1e4-176">Il comando precedente crea anche un'app abilitata per Git che consente la distribuzione in Azure dal proprio repository Git locale.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-176">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="1e1e4-177">Il repository Git locale è configurato con l'URL 'https://<username>@<nome_app>.scm.azurewebsites.net/<nome_app>.git'</span><span class="sxs-lookup"><span data-stu-id="1e1e4-177">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="1e1e4-178">Creare un utente di distribuzione. Al termine del comando precedente, è possibile aggiungere una distribuzione remota di Azure al repository Git locale.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-178">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="1e1e4-179">Sostituire <url> con l'URL della distribuzione remota Git ottenuto da Abilitare la distribuzione Git per l'app.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-179">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="1e1e4-180">Aprire e modificare la soluzione</span><span class="sxs-lookup"><span data-stu-id="1e1e4-180">Open and edit the solution</span></span>

<span data-ttu-id="1e1e4-181">Modificare il file program.cs per eseguire l'esempio con il nome dell'insieme di credenziali delle chiavi specifico:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-181">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="1e1e4-182">Passare alla cartella key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-182">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="1e1e4-183">Aprire il file key-vault-dotnet-core-quickstart.sln in Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-183">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="1e1e4-184">Aprire il file Program.cs e aggiornare il segnaposto *YourKeyVaultName* con il nome dell'insieme di credenziali delle chiavi creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-184">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="1e1e4-185">Questa soluzione usa le librerie NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) e [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-185">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="1e1e4-186">Eseguire l'app</span><span class="sxs-lookup"><span data-stu-id="1e1e4-186">Run the app</span></span>

<span data-ttu-id="1e1e4-187">Dal menu principale di Visual Studio 2017 selezionare **Debug** > **Avvia** senza eseguire debug.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-187">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="1e1e4-188">Quando viene visualizzato il browser, passare alla pagina **Informazioni su**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-188">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="1e1e4-189">Viene visualizzato il valore per **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-189">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="1e1e4-190">Pubblicare l'applicazione Web in Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-190">Publish the web application to Azure</span></span>

<span data-ttu-id="1e1e4-191">Pubblicare questa app in Azure per visualizzarla come un'app Web e per verificare che venga recuperato il valore del segreto:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-191">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="1e1e4-192">In Visual Studio selezionare il progetto **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-192">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="1e1e4-193">Selezionare **Pubblica** > **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-193">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="1e1e4-194">Creare un nuovo **servizio app** e quindi selezionare **Pubblica**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-194">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="1e1e4-195">Modificare il nome dell'app in **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-195">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="1e1e4-196">Selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-196">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a><span data-ttu-id="1e1e4-197">Abilitare le identità del servizio gestite</span><span class="sxs-lookup"><span data-stu-id="1e1e4-197">Enable managed service identities</span></span>

<span data-ttu-id="1e1e4-198">Azure Key Vault consente di archiviare in modo sicuro le credenziali e altri segreti e chiavi, ma è necessario autenticare il codice in Azure Key Vault per recuperarli.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-198">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="1e1e4-199">L'identità del servizio gestita semplifica questa attività, assegnando ai servizi di Azure un'identità gestita automaticamente in Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1e1e4-199">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="1e1e4-200">È possibile usare questa identità per l'autenticazione a qualsiasi servizio che supporti l'autenticazione di Azure AD, incluso Key Vault, senza inserire le credenziali nel codice.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-200">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="1e1e4-201">Tornare all'interfaccia della riga di comando di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-201">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="1e1e4-202">Eseguire il comando assign-identity per creare l'identità per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-202">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="1e1e4-203">Il comando in questa procedura equivale a passare al portale e impostare **Identità del servizio gestita** su **Attivato** nelle proprietà dell'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-203">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="1e1e4-204">Assegnare le autorizzazioni all'applicazione per la lettura dei segreti da Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-204">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="1e1e4-205">Prendere nota dell'output quando si pubblica l'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-205">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="1e1e4-206">Deve essere nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-206">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="1e1e4-207">Eseguire quindi questo comando usando il nome dell'insieme di credenziali delle chiavi e il valore **PrincipalId**:</span><span class="sxs-lookup"><span data-stu-id="1e1e4-207">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="1e1e4-208">Distribuire l'app Node in Azure e recuperare il valore del segreto</span><span class="sxs-lookup"><span data-stu-id="1e1e4-208">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="1e1e4-209">Ora che tutto è pronto,</span><span class="sxs-lookup"><span data-stu-id="1e1e4-209">Now that everything is set.</span></span> <span data-ttu-id="1e1e4-210">usare il comando seguente per distribuire l'app in Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-210">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="1e1e4-211">Successivamente sarà possibile vedere il valore del segreto passando a https://<nome_app>.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-211">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="1e1e4-212">Assicurarsi di aver sostituito il nome <YourKeyVaultName> con il nome dell'insieme di credenziali</span><span class="sxs-lookup"><span data-stu-id="1e1e4-212">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

::: zone-end

::: zone pivot="dotnet"
<span data-ttu-id="1e1e4-213">A questo punto, quando si esegue l'applicazione, viene visualizzato il valore del segreto recuperato.</span><span class="sxs-lookup"><span data-stu-id="1e1e4-213">Now when you run the application, you should see your secret value retrieved.</span></span>
::: zone-end

## <a name="next-steps"></a><span data-ttu-id="1e1e4-214">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="1e1e4-214">Next steps</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="1e1e4-215">Home page di Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-215">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="1e1e4-216">Documentazione su Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-216">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="1e1e4-217">Azure SDK per Node</span><span class="sxs-lookup"><span data-stu-id="1e1e4-217">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [<span data-ttu-id="1e1e4-218">Informazioni di riferimento sull'API REST di Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-218">Azure REST API Reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [<span data-ttu-id="1e1e4-219">Home page di Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-219">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="1e1e4-220">Documentazione su Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e1e4-220">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="1e1e4-221">Azure SDK per .NET</span><span class="sxs-lookup"><span data-stu-id="1e1e4-221">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* [<span data-ttu-id="1e1e4-222">Informazioni di riferimento sull'API REST di Azure</span><span class="sxs-lookup"><span data-stu-id="1e1e4-222">Azure REST API reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
