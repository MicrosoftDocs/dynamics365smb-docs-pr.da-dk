---
title: Vise objekter som webtjenester
description: Publicer objekter som webtjenester for at gøre dem umiddelbart tilgængelige for din Business Central-løsning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 94a4752abc133e59169209b94a145d2195ce783d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384620"
---
# <a name="publish-a-web-service"></a>Udgive en webtjeneste

Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for forskellige eksterne systemer og brugere. Som standard [!INCLUDE[prod_short](includes/prod_short.md)]viser en række objekter som webtjenester, hvilket giver en bedre integration med andre Microsoft-tjenester. Du kan tilføje andre webtjenester, efterhånden som virksomheden kræver det.  

Opret en webtjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], og udgiv derefter webtjenesten, så den er tilgængelig for godkendte brugere. Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.  

## <a name="creating-and-publishing-a-web-service"></a>Oprettelse og publicering af en webtjeneste

Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.  

### <a name="to-create-and-publish-a-web-service"></a>Sådan oprettes og publiceres en webtjeneste  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjenester**, og vælg derefter det relaterede link.  
2. På siden **Webtjeneste** skal du vælge **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Forespørgsel** er gyldige typer for OData-webtjenester. Fra og med version 16.3 **Codeunit**, som også er en gyldig type til OData v4-webtjenester, men derefter vises der ikke nogen URL-adresse i brugergrænsefladen. Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.  
    > Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.

3. Marker afkrydsningsfeltet i kolonnen **Udgivet**.  

Når du udgiver webtjenesten, viser felterne **OData URL** og **SOAP-URL** nye URL-adresser. For de kodeenheder, der eksponeres som Odata v4-ubundne handlinger, vises URL-felterne imidlertid ikke.  

Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**. Du kan vælge at kopiere værdien af feltet og gemme det til senere brug. Hvis du vil teste kodeenheder, som er eksponerede som OData v4-ubundne handlinger, skal du følge instruktionerne i afsnittet [Kontroller webtjenestetilgængelighed](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i udviklerindholdet.

> [!NOTE]
> Hvis du ikke kan få adgang til de objekter, du fremviser som webtjenester, i [!INCLUDE[prod_short](includes/prod_short.md)] online, skal du markere de metoder, der vises i koden, som `[Scope('OnPrem')]`. Du kan finde flere oplysninger i [Områdeattribut](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter. Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket på siden **URL-adresse til OData** og **URL-adresse til SOAP** på siden **Webtjenester**. Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Sådan kontrolleres tilgængeligheden af en webtjeneste  

1. Indtast den relevante URL-adresse i din browser Følgende tabel viser de typer URL'er, som du kan angive for forskellige typer webtjenester.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaks|Eksempel|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |V4-adresse til OData|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Der skelnes mellem små og store bogstaver i firmanavnet.|

2. Gennemse de oplysninger, der vises i browseren. Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.  

Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive firmanavnet. Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene. F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Business Centrale-webtjenester til udviklere](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Anmodningsgrænser for OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]