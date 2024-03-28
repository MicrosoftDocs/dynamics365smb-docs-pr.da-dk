---
title: Opsætning af onlinekort
description: 'Flere oplysninger om, hvordan du konfigurerer Business Central til at tilbyde vejledning og oplysninger om steder med en onlinekort-tjeneste.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.search.form: '800, 804'
ms.date: 07/15/2022
ms.author: bholtorf
---
# <a name="set-up-online-maps"></a>Opsætning af onlinekort

Hvis du planlægger at besøge en adresse, der er gemt på et kort, f.eks. en kunde, kan du hente et kort fra en onlinekorttjeneste med ruteangivelser på det sprog, du vælger. Hvis denne onlinekorttjeneste skal kunne finde det rigtige kort og vejlede dig korrekt, er du nødt til at vælge indstillinger til det i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-online-map-feature"></a>Konfigurer funktionen onlinekort

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af onlinekort**, og vælg derefter det relaterede link.
2. På siden **Opsætning af onlinekort** skal du udfylde følgende felter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Aktivér **Aktiveret**-feltet til/fra.

### <a name="customize-the-online-map-provider-features"></a>Tilpasning af funktioner til onlinekort-udbyder

Hvis du vil tilpasse funktionen Onlinekort ud over de indstillinger, der vises på siden **Opsætning af onlinekort**, eller du vil bruge en anden kortudbyder, skal du følge disse trin:

1. Vælg handlingen **Opsætning af parameter** på siden **Opsætning af onlinekort**.
2. Vælg handlingen **Ny** på siden **Opsætning af parameter til onlinekort**.
3. Udfyld felterne for at tilpasse, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] genererer URL-adresserne til de tilgængelige tjenester. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
   * Se **Erstatningsparameter til onlinekort** i ruden **Faktaboks** for de data, der er tilgængelige for oprettelse af URL-adresser.

## <a name="see-also"></a>Se også

[Bruge online kort til at finde steder og vejledninger](across-online-maps.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Opsætning](admin-setup-and-administration.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
