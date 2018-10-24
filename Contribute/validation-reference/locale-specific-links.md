# <a name="locale-specific-links"></a>Collegamenti delle impostazioni locali

I codici delle impostazioni locali, come `en-us`, non devono essere inclusi nei collegamenti a determinati siti Microsoft. Se si include il codice di un'impostazione locale in un collegamento con contenuto in inglese, verrà incluso anche nei collegamenti localizzati, producendo un'esperienza localizzata errata. Ad esempio, se un collegamento in un contenuto localizzato in tedesco include `en-us`, i clienti tedeschi si troveranno a collegarsi all'articolo in inglese, anche se è disponibile una versione in tedesco.

Rimuovere i codici delle impostazioni locali dai collegamenti ai siti Microsoft. Di seguito è riportato un esempio.

Prima:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Dopo:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

I siti seguenti rientrano nell'ambito di questa convalida:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com