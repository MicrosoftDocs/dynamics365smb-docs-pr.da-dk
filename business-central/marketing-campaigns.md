---
title: Opsætning af marketingkampagner i Business Central | Microsoft Docs
description: 'Beskriver, hvordan du kan oprette og styre marketingkampagner i Business Central som en hjælp til at identificere og tiltrække potentielle kunder og bibeholde kunder.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'marketing, campaign, promo, prospect'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="managing-marketing-campaigns"></a><a name="managing-marketing-campaigns"></a>Administration af marketingkampagner
Når du har fastlagt en stærk marketingplan, kan du identificere og tiltrække kunder og holde på dem. En marketingplan består af forskellige kampagner og andre interaktioner i forbindelse med salgs- og marketingaktiviteter. Mens du planlægger en kampagne, skal du beslutte, hvilke kontaktpersoner der skal være målet, hvilken type kampagne kampagnen skal være (f.eks. en messe eller direct mail), og hvilke sælgere der skal udføre de enkelte opgaver.

Hver kampagne består af forskellige aktiviteter eller opgaver. Du kan samle flere opgaver, for eksempel opgaver, der hver repræsenterer et trin, i aktiviteter. Aktivitetsopgaver er forbundet med hinanden vha. en datoformel. Individuelle opgaver kan kun tildeles til sælgere. Aktiviteter kan tildeles til leads, sælgere, grupper af sælgere og kontaktpersoner. Du kan finde flere oplysninger i [Konfigurere salgsprocesser og -procesfaser for leads](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a><a name="defining-individual-campaigns"></a>Definere individuelle kampagner
Når du vil oprette en kampagne, skal du først definere *statuskoder for kampagnen*. Via. disse koder kan du styre dine kampagner ved at tildele kampagnen en status. Efterhånden som du arbejder dig gennem faserne i en kampagne, kan du se, hvilket trin en kampagne er på, og hvilket trin der følger efter. Du kan definerer statuskoder for kampagner på siden **Kampagnestatus**.

Du kan oprette et kampagnekort til hver kampagne, som du vil holde styr på. Du kan også få vist disse kampagnekort, så du kan se generelle oplysninger om dine kampagner.
Du kan slette kampagneposter, f.eks. hvis de registrerer en handling, der er annulleret. Kun annullerede kampagneposter kan slettes.

### <a name="selecting-the-target-audience"></a><a name="selecting-the-target-audience"></a>Vælge målgruppen
Når du har oprettet en kampagne, kan du begynde at oprette målgrupper, der specificerer målgruppen for kampagnen. Der kan finde flere oplysninger under [Administrere målgrupper](marketing-segments.md).

### <a name="registering-discount-percentages"></a><a name="registering-discount-percentages"></a>Registrere rabatprocenter
Når du har oprettet en kampagne, besluttet, hvilken målgruppe kampagnen skal rettes mod, og angivet start- og slutdato, skal du registrere den rabatprocent, som kunden får på de individuelle varer på linjerne på siden **Salgslinjerabatter**. Du kan også registrere salgsprisen for de enkelte varer på linjerne på siden **Salgspriser**. Du kan få adgang til begge sider fra kampagnekortet.

 Når du har angivet salgspriserne/linjerabatterne og målgrupperne på kampagnekortet, skal de aktiveres, så kampagnepriserne og -rabatterne vises på linjerne.

> [!NOTE]  
>   Hvis du vil aktivere salgspriserne/linjerabatterne, skal du angive, om kampagnen er henvendt til hele målgruppen eller kun bestemte kontakter. Hvis salgspriserne/linjerabatterne dækker alle kontakter i målgruppen, skal du markere feltet **Kampagnemålgruppe** i oversigtspanelet **Kampagne** på **målgruppekortet**.

Hvis salgspriserne/linjerabatterne ikke skal tilbydes til alle kontakter i målgruppen, skal markeringen fjernes fra feltet **Kampagnemålgruppe** for de relevante kontakter. Hvis feltet ikke vises, kan du føje det til visningen. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="conducting-campaigns"></a><a name="conducting-campaigns"></a>Udføre kampagner
Efterhånden som en kampagne kører, registreres alle interaktioner med kontaktpersonerne, eller målgruppen, så du kan få vist statistik og andre oplysninger om kostpriser og kampagnens succeshyppigheder.

Kampagner udføres af sælgere, og du skal oprette aktiviteter, der repræsenterer hver opgave, og tildele dem til de relevante sælgere. Du kan finde flere oplysninger i [Konfigurere salgsprocesser og -procesfaser for leads](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a><a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere målgrupper](marketing-segments.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
