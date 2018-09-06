---
title: 'Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault | Microsoft Docs'
description: 'Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239544"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Guida introduttiva: Impostare e recuperare un segreto da Azure Key Vault

Questa guida introduttiva illustra come archiviare un segreto in Key Vault e come recuperarlo usando un'app Web. Per visualizzare il valore del segreto, è necessario eseguire la procedura in Azure. La guida introduttiva usa Node.js e identità del servizio gestite

> [!div class="checklist"]
> * Creare un insieme di credenziali delle chiavi.
> * Archiviare un segreto in Key Vault.
> * Recuperare un segreto da Key Vault.
> * Creare un'applicazione Web di Azure.
> * [Abilitare le identità del servizio gestite](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Concedere le autorizzazioni necessarie per l'applicazione Web per la lettura dei dati da Key Vault.

Prima di procedere, assicurarsi di avere familiarità con i [concetti di base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

>[!NOTE]
Per capire i motivi per cui l'esercitazione seguente rappresenta la procedura consigliata, è necessario comprendere alcuni concetti. Key Vault è un repository centrale per archiviare i segreti a livello di codice. Per farlo, tuttavia, le applicazioni o gli utenti devono prima autenticarsi in Key Vault, ad esempio presentando un segreto. Per seguire le procedure consigliate per la sicurezza, questo primo segreto deve essere ruotato periodicamente. Con l'[identità del servizio gestita](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), alle applicazioni in esecuzione in Azure viene assegnata un'identità gestita automaticamente da Azure. Ciò aiuta a risolvere il **problema di introduzione del segreto**, con utenti o applicazioni che possono seguire le procedure consigliate senza doversi preoccupare della rotazione del primo segreto

## <a name="prerequisites"></a>Prerequisiti

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/) ::: zone-end

::: zone pivot="dotnet, windows"
* [Visual Studio 2017 versione 15.7.3 o successiva](https://www.microsoft.com/net/download/windows) con i carichi di lavoro seguenti:
  * Sviluppo Web e ASP.NET
  * Sviluppo multipiattaforma .NET Core
* [.NET Core 2.1 SDK o versioni successive](https://www.microsoft.com/net/download/windows) :::zone-end

::: zone pivot="dotnet, mac"
* Vedere [Novità di Visual Studio per Mac](https://visualstudio.microsoft.com/vs/mac/).
:::zone-end

* Git ([download](https://git-scm.com/downloads)).
* Una sottoscrizione di Azure. Se non si ha una sottoscrizione di Azure, creare un [account gratuito](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) prima di iniziare.
* [Interfaccia della riga di comando di Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) versione 2.0.4 o versioni successive. È disponibile per Windows, Mac e Linux.

## <a name="login-to-azure"></a>Accesso ad Azure

Per accedere ad Azure tramite l'interfaccia della riga di comando è possibile digitare:

```azurecli
az login
```

## <a name="create-resource-group"></a>Creare un gruppo di risorse

Creare un gruppo di risorse usando il comando [az group create](/cli/azure/group#az-group-create). Un gruppo di risorse di Azure è un contenitore logico in cui vengono distribuite e gestite risorse di Azure.

Selezionare il nome di un gruppo di risorse e compilare il segnaposto.
L'esempio seguente crea un gruppo di risorse denominato *<YourResourceGroupName>* nella località *eastus*.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

In tutta l'esercitazione viene usato il gruppo di risorse appena creato.

## <a name="create-an-azure-key-vault"></a>Creare un Azure Key Vault

Successivamente si crea un'istanza di Key Vault usando il gruppo di risorse creato nel passaggio precedente. Anche se in tutto l'articolo viene usato "ContosoKeyVault" come nome per l'istanza di Key Vault, è necessario usare un nome univoco. Specificare le informazioni seguenti:

* Nome dell'istanza di Key Vault - **Selezionare qui un nome per l'istanza di Key Vault**.
* Nome gruppo di risorse - **Selezionare qui un nome di gruppo di risorse**.
* Località - **Stati Uniti orientali**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

A questo punto, l'account di Azure è l'unico autorizzato a eseguire qualsiasi operazione su questo nuovo insieme di credenziali.

## <a name="add-a-secret-to-key-vault"></a>Aggiungere un segreto all'insieme di credenziali delle chiavi

Verrà aggiunto un segreto per illustrare il funzionamento di questa operazione. Si potrebbe archiviare una stringa di connessione SQL o qualsiasi altra informazione che è necessario conservare in modo sicuro, rendendola però disponibile per l'applicazione. In questa esercitazione la password sarà denominata **AppSecret** e archivierà il valore **MySecret**.

Digitare i comandi seguenti per creare un segreto in Key Vault chiamato **AppSecret** che archivierà il valore **MySecret**:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Per visualizzare il valore contenuto nel segreto come testo normale:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Questo comando mostra le informazioni del segreto, incluso l'URI. Dopo aver completato questi passaggi sarà disponibili un URI per un segreto in Azure Key Vault. Annotare queste informazioni. Saranno necessarie in un passaggio successivo.

## <a name="clone-the-repo"></a>Clonare il repository

Clonare il repository per creare una copia locale e modificare l'origine eseguendo il comando seguente:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Installare le dipendenze

Qui si installano le dipendenze. Eseguire il comando cd key-vault-node-quickstart npm install

Questo progetto usa 2 moduli Node:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Pubblicare l'applicazione Web in Azure

Di seguito sono riportati i pochi passaggi necessari

* Il primo passaggio consiste nel creare un piano del [servizio app di Azure](https://azure.microsoft.com/services/app-service/). In questo piano è possibile archiviare più app Web.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Successivamente verrà creata un'app Web. Nell'esempio seguente sostituire <app_name> con un nome app univoco a livello globale. I caratteri validi sono a-z, 0-9 e -. Il runtime è impostato su NODE|6.9. Per visualizzare tutti i runtime supportati, eseguire az webapp list-runtimes

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Dopo la creazione dell'app Web, l'interfaccia della riga di comando di Azure mostra un output simile all'esempio seguente:

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
    Passare all'app Web appena creata, che dovrebbe essere funzionante. Sostituire <app_name> con un nome app univoco.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Il comando precedente crea anche un'app abilitata per Git che consente la distribuzione in Azure dal proprio repository Git locale. 
    Il repository Git locale è configurato con l'URL 'https://<username>@<nome_app>.scm.azurewebsites.net/<nome_app>.git'

* Creare un utente di distribuzione. Al termine del comando precedente, è possibile aggiungere una distribuzione remota di Azure al repository Git locale. Sostituire <url> con l'URL della distribuzione remota Git ottenuto da Abilitare la distribuzione Git per l'app.

    ```bash
    git remote add azure <url>
    ```
::: zone-end

::: zone pivot="dotnet"

## <a name="open-and-edit-the-solution"></a>Aprire e modificare la soluzione

Modificare il file program.cs per eseguire l'esempio con il nome dell'insieme di credenziali delle chiavi specifico:

1. Passare alla cartella key-vault-dotnet-core-quickstart.
2. Aprire il file key-vault-dotnet-core-quickstart.sln in Visual Studio 2017.
3. Aprire il file Program.cs e aggiornare il segnaposto *YourKeyVaultName* con il nome dell'insieme di credenziali delle chiavi creato in precedenza.

Questa soluzione usa le librerie NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) e [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).

## <a name="run-the-app"></a>Eseguire l'app

Dal menu principale di Visual Studio 2017 selezionare **Debug** > **Avvia** senza eseguire debug. Quando viene visualizzato il browser, passare alla pagina **Informazioni su**. Viene visualizzato il valore per **AppSecret**.

## <a name="publish-the-web-application-to-azure"></a>Pubblicare l'applicazione Web in Azure

Pubblicare questa app in Azure per visualizzarla come un'app Web e per verificare che venga recuperato il valore del segreto:

1. In Visual Studio selezionare il progetto **key-vault-dotnet-core-quickstart**.
2. Selezionare **Pubblica** > **Avvia**.
3. Creare un nuovo **servizio app** e quindi selezionare **Pubblica**.
4. Modificare il nome dell'app in **keyvaultdotnetcorequickstart**.
5. Selezionare **Crea**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

::: zone-end

## <a name="enable-managed-service-identities"></a>Abilitare le identità del servizio gestite

Azure Key Vault consente di archiviare in modo sicuro le credenziali e altri segreti e chiavi, ma è necessario autenticare il codice in Azure Key Vault per recuperarli. L'identità del servizio gestita semplifica questa attività, assegnando ai servizi di Azure un'identità gestita automaticamente in Azure Active Directory (Azure AD). È possibile usare questa identità per l'autenticazione a qualsiasi servizio che supporti l'autenticazione di Azure AD, incluso Key Vault, senza inserire le credenziali nel codice.

1. Tornare all'interfaccia della riga di comando di Azure.
2. Eseguire il comando assign-identity per creare l'identità per l'applicazione:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>Il comando in questa procedura equivale a passare al portale e impostare **Identità del servizio gestita** su **Attivato** nelle proprietà dell'applicazione Web.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Assegnare le autorizzazioni all'applicazione per la lettura dei segreti da Key Vault

Prendere nota dell'output quando si pubblica l'applicazione in Azure. Deve essere nel formato seguente:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Eseguire quindi questo comando usando il nome dell'insieme di credenziali delle chiavi e il valore **PrincipalId**:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Distribuire l'app Node in Azure e recuperare il valore del segreto

Ora che tutto è pronto, usare il comando seguente per distribuire l'app in Azure

```bash
git push azure master
```

Successivamente sarà possibile vedere il valore del segreto passando a https://<nome_app>.azurewebsites.net.
Assicurarsi di aver sostituito il nome <YourKeyVaultName> con il nome dell'insieme di credenziali ::: zone-end

::: zone pivot="dotnet" A questo punto, quando si esegue l'applicazione viene visualizzato il valore del segreto recuperato.
::: zone-end

## <a name="next-steps"></a>Passaggi successivi

::: zone pivot="nodejs"
* [Home page di Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentazione su Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK per Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Informazioni di riferimento sull'API REST di Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end

::: zone pivot="dotnet"
* [Home page di Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentazione su Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK per .NET](https://github.com/Azure/azure-sdk-for-net)
* [Informazioni di riferimento sull'API REST di Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end