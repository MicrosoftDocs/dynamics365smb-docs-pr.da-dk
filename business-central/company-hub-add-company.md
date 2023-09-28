---
title: Tilføj firmaer til virksomhedens hub
description: 'Få mere at vide om, hvordan du føjer virksomheder fra andre Business Central-miljøer til virksomhedens hub, så du kan administrere arbejde på tværs af miljøer.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, company hub'
ms.search.form: '1151, 1155, 1166, 1165'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="add-companies-to-your-company-hub"></a>Tilføj virksomheder til virksomhedens hub

Med virksomhedshubben kan du få adgang til dit arbejde fra tværs af flere firmaer fra flere forskellige [!INCLUDE [prod_short](includes/prod_short.md)] miljøer. Du kan tilføje et miljø og en virksomhed manuelt, hvis virksomhederne ikke vises automatisk i virksomhedens hub.  

Direkte på siden virksomhedshub finder du menuen **Opsætning**, hvorfra du kan få adgang til siden **Miljølinks**. Vælg **Ny**, og udfyld felterne. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Du kan tilslutte virksomhedens hub til så mange virksomheder, du har brug for. Du kan dog kun tilslutte virksomhedens hub til virksomheder, der er værtsbaseret på [!INCLUDE [prod_short](includes/prod_short.md)]-internettet.

## <a name="environment-links"></a>Miljølink

Et miljølink er et kort, hvor du angiver det [!INCLUDE [prod_short](includes/prod_short.md)]-miljø, der er vært for en eller flere virksomheder, som du arbejder med. Du angiver dataene i kortet for hvert miljø, og du kan ændre dem efter behov. Men feltet **Miljø-link** er vigtigt – det er her, du kan få adgang til den enkelte virksomhed i [!INCLUDE [prod_short](includes/prod_short.md)]. Brug handlingen **Test forbindelsen** på båndet til at kontrollere, at du har angivet det rigtige link. Det link, du skal angive, peger på miljøet, som er vært for det regnskab, du tilføjer, og det skal indeholde Azure Active Directory (Azure AD)-id eller organisationens domænenavn. Hvis de har angivet et domæne, f.eks. MyBusiness.com, så er linket til deres [!INCLUDE [prod_short](includes/prod_short.md)] ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Ellers ser det ud som følger: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Linket bruges, når du vælger virksomheden i virksomhedens hub.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Handlinger for en virksomhed, der er angivet i virksomhedshubben.":::

> [!TIP]
> Hvis du arbejder i den gratis prøveversion af [!INCLUDE [prod_short](includes/prod_short.md)], er det nemt at tilføje virksomhederne i din lejer. Du kan finde miljø linket ved at kopiere Azure Active Directory-id fra afsnittet om **Fejlfinding** på siden Hjælp & support. Miljønavnet er sandsynligvis standardværdien, PRODUKTION. Føj disse oplysninger til feltet **Miljølink**, f.eks.```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, og vælg derefter **Test forbindelse**. Evalueringsfirmaet vil blive føjet til oversigten.
>
> Hvis du har flyttet til den 30-dages prøveversion af firmaet, kan du føje det til oversigten ved at vælge handlingen **Genindlæs/Genindlæs alle regnskaber** på listen.

## <a name="load-companies"></a>Indlæse virksomheder

Når du har tilføjet dine miljøer, vises virksomhederne automatisk. Men hvis du ved, at der er føjet en ny virksomhed til et miljø, kan du vælge handlingen **Genindlæs alle regnskaber** for at opdatere listen. Bruge samme handling til at opdatere data fra tværs af virksomheder.  

> [!TIP]
> Hvis du vil opdatere dataene i virksomhedshub, skal du have adgang til dataene i de virksomheder, som dataene stammer fra.

## <a name="see-also"></a>Se også

[Administrere arbejde på tværs af flere regnskaber i virksomhedshub](company-hub.md)  
[Ressourcer til hjælp og support](product-help-and-support.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
