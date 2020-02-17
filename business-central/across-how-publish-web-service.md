---
title: Vise objekter som webtjenester | Microsoft Docs
description: Publicer objekter som webtjenester for at gøre dem umiddelbart tilgængelige for din Business Central-løsning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/04/2020
ms.author: edupont
ms.openlocfilehash: 4e09df754895a8d0d3a1cc1ed84a7c8332e32880
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030240"
---
# <a name="publish-a-web-service"></a>Udgive en webtjeneste

Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for en række eksterne systemer og brugere. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en lang række objekter, der vises som webtjenester som standard, på grund af integration med andre Microsoft-tjenester, men du kan også tilføje andre webtjenester.  

Du kan oprette en webtjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten. Du skal derefter publicere webtjenesten, så den er tilgængelig for serviceanmodninger via netværket. Brugere kan se webtjenester ved at pege på en browser på serverplaceringen og anmode om en oversigt over tilgængelige tjenester. Når du publicerer en webtjeneste, bliver den straks tilgængelig over netværket for godkendte brugere. Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.

## <a name="creating-and-publishing-a-web-service"></a>Oprettelse og publicering af en webtjeneste  
Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.  

### <a name="to-create-and-publish-a-web-service"></a>Sådan oprettes og publiceres en webtjeneste  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjenester**, og vælg derefter det relaterede link.  
2. På siden **Webtjeneste** skal du vælge **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Forespørgsel** er gyldige typer for OData-webtjenester.  
    > Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.  
    > Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.

3. Marker afkrydsningsfeltet i kolonnen **Udgivet**.  

Når du publicerer en webtjeneste, kan du i felterne **URL-adresse til OData** og **URL-adresse til SOAP** se de URL'er, der er genereret for webtjenesten. Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**. Du kan vælge at kopiere værdien af feltet og gemme det til senere brug.  

> [!IMPORTANT]
> For codeunits, der er publiceret som en SOAP-webtjeneste, skal de metoder, som vises i den pågældende codeunit, markeres som `[External]` i koden.

Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter. Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket på siden **URL-adresse til OData** og **URL-adresse til SOAP** på siden **Webtjenester**. Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Sådan kontrolleres tilgængeligheden af en webtjeneste  

1. Indtast den relevante URL-adresse i din browser Følgende tabel viser de typer URL'er, som du kan angive for forskellige typer webtjenester.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaks|Eksempel|
    > |----------------|------|-------|
    > |SOAP|https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/ |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |V4-adresse til OData|https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*|https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument<br/>    Der skelnes mellem små og store bogstaver i firmanavnet.|

2. Gennemse de oplysninger, der vises i browseren. Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.  

Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive firmanavnet. Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene. F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  
[Business Centrale-webtjenester til udviklere](/dynamics365/business-central/dev-itpro/webservices/web-services)  
