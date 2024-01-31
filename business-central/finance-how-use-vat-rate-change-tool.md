---
title: Styre ændringer af momssats
description: 'Lære, hvordan du bruger Momssatsændringsværktøjet til at ændre Dynamics 365 Business Central-momssatser, der er baseret på lokal lovgivning.'
author: jswymer
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Styre ændringer af momssats

Momssatser kan ændres i henhold til lokal lovgivning. Eventuelle ændringer i moms påvirker dine data i [!INCLUDE[prod_short](includes/prod_short.md)], uanset om momssatsen bliver lavere, højere eller fjernet. Moms er knyttet til mange objekter i [!INCLUDE[prod_short](includes/prod_short.md)], f.eks. debitorer, kreditorer, varer, ressourcer, varegebyrer og finanskonti. Ændringer af momssatser sker normalt på en bestemt dato, hvorfra du skal have ændret momsopsætningen, bogføringsgrupperne osv. for at sikre, at der oprettes nye salgsordrer og købsordrer med den nye momssats.

## Ændre momssatser

Den bedste metode til styring af momsændringer er at bogføre og lukke åbne ordrer og andre dokumenter før startdatoen for ændret momssats for at sikre, at de ikke påvirkes af ændringen. Det er den rene metode, der giver dig mulighed for at starte nye ordrer og dokumenter med den nye momssats.

Følgende fremgangsmåde foreslås til styring af en momssatsændring

1. Bogfør helt og luk åbne ordrer, kladder og andre dokumenter inden ændringsdatoen. Du kan vente til efter ændringsdatoen, så længe du ikke tilføjer nye linjer og sikrer dig, at ikrafttrædelsesdatoen ligger før ændringsdatoen.  
2. Opret den nye momsopsætning.  
3. Foretag momsændringen på enheder (relevante debitorer, kreditorer, varer osv.).  
4. På ændringsdatoen for momssatsen kan du oprette nye dokumenter, der skal bruge den nye sats.  


> [!NOTE]  
> Vi opdaterer aktuelt momssatsændringsværktøjet. Ovennævnte funktionalitet stemmer muligvis ikke overens med funktionaliteten i dit miljø. Opdateringen vil finde sted før 1. juli 2020 og vil ikke være en almindelig månedlig opdatering. Alle miljøer opdateres i stedet automatisk (hotfix). Når denne opdatering er fuldført, vises denne meddelelse ikke længere.  

## Momssatsændringsværktøjet

Momssatsændringsværktøjet kan hjælpe med at konvertere momssatser på stamdata, kladder og ordrer, i en vis grad. Dette er nyttigt, hvis du nemmere vil konvertere moms på stamdata, eller hvis du har ordrer, som du ikke kan lukke inden ændringsdatoen og vil blive behandlet over en længere periode, som krydser ændringsdatoen for momssatsen. Der gælder visse restriktioner og begrænsninger i momssatsændringsværktøjet.

## Forstå processen og begrænsningerne for konvertering af momssatsen

Momssatsændringsværktøjet udfører momssatskonverteringer for stamdata, kladder og ordrer på forskellige måder. De valgte masterdata og kladder opdateres af den nye generelle produktbogføringsgruppe eller momsproduktbogføringsgruppe. Hvis en ordre er blevet helt eller delvist leveret, bevarer de leverede varer den aktuelle generelle produktbogføringsgruppe eller momsproduktbogføringsgruppe. En ny ordrelinje oprettes for de ikke-leverede varer og opdateres for at justere aktuelle og nye momsbogføringsgrupper eller generelle produktbogføringsgrupper. Desuden opdateres oplysninger om varegebyrtildeling, konfigurationsskabeloner for varer, reservationer og varesporingsoplysninger tilsvarende. 

På ordrelinjerne opdateres enhedsprisen for alle linjer af typen Vare og Ressource, hvis der bruges priser med moms for varen. For andre linjetyper er det muligt at bestemme, om enhedsprisen skal opdateres.

Der er et par ting, som værktøjet ikke konverterer:

* Salgs- eller købsordrer og fakturaer, hvor leverancer er blevet bogført. Disse dokumenter bogføres ved hjælp af den aktuelle momssats.  
* Dokumenter, der har bogførte forudbetalingsfakturaer. For eksempel har du foretaget eller modtaget forudbetalinger på fakturaer, der ikke er afsluttet, før du bruger momssatsændringsværktøjet. I dette tilfælde vil der være en difference mellem det momsbeløb, der er forfaldent, og den moms, der er betalt i forudbetalinger, når fakturaen er fuldført. Momssatsændringsværktøj springer disse dokumenter over, og du skal opdatere dem manuelt.  
* Salgs- eller købsordrer med lagerintegration, hvis de er delvist leveret eller modtaget.  
* Direkte leveringer.
* Specialordrer. 
* Montageordrer.
* Servicekontrakter.  
* Kreditnotaer.
* Returvareordrer.
* Priser på varer (stamdata)
* Priser på salgspriser (stamdata)
* Virksomhedsbogføringsgrupper til debitorer og kreditorer.

### Sådan forberedes momssatsændringskonverteringer

Før du konfigurerer momssatsændringsværktøj, skal du foretage følgende forberedelser.

* Hvis du har transaktioner, der bruger forskellige satser, skal de adskilles i forskellige grupper ved enten at oprette nye finanskonti for hver sats eller ved hjælp af datafiltre til gruppering af transaktioner i henhold til sats.  
* Hvis du opretter nye finanskonti, skal du oprette nye generelle bogføringsgrupper.  
* For at reducere antallet af dokumenter, der konverteres, skal du postere så mange dokumenter som muligt og reducere antallet af dokumenter, der ikke posteres, til et minimum.  
* Sikkerhedskopiering af data.

### Sådan konfigureres momssatsændringsværktøjet

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af ændring af momssats** og vælg derefter det relaterede link.  
2. På oversigtspanelerne **Stamdata**, **Kladder** og **Dokumenter** skal du vælge en bogføringsgruppeværdi i indstillingslisten for nødvendige felter. For hver gruppe kan du vælge, om der skal konverteres momsproduktbogføringsgrupper eller generelle produktbogføringsgrupper, eller om begge værdier skal konverteres, hvis de er tilgængelige i stamdata. I nogle områder kan du også angive et filter for kun at konvertere et undersæt af værdier, f.eks. finanskonti. 
3. I oversigtspanelet **Priser inkl. moms** skal du vælge, hvilke linjetyper på ordrer du vil opdatere enhedspriser for. Enhedspriser på linjer af typen Vare og Ressource opdateres altid.

### Sådan konfigureres produktbogføringsgruppekonvertering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af ændring af momssats** og vælg derefter det relaterede link.  
2. På siden **Konfiguration af ændring af momssats** skal du vælge enten **Momsproduktbogf.gruppekonv.** eller **Gen. produktbogf.gruppekonv.**.  
3. Angiv den aktuelle bogføringsgruppe i feltet **Fra kode**.  
4. Angiv den nye bogføringsgruppe i feltet **Til kode**.  

### Sådan udføres konvertering af momssatsændring

Du bruger momssatsændringsværktøjet til at administrere ændringer i standardmomssatsen. Du udfører momsproduktbogføringsgruppekonverteringer og generelle produktbogføringsgruppekonverteringer for at ændre momssatser og opretholde nøjagtig momsafregning. Afhængigt af din opsætning foretages følgende ændringer:  

* Moms- og generelle bogføringsgrupper konverteres.  
* Ændringer implementeres i finanskonti, debitorer, kreditorer, åbne dokumenter, kladdelinjer osv.  

> [!IMPORTANT]  
> Inden du foretager konvertering af momssatsændringen, kan du teste konverteringen. Det gør du ved at følge fremgangsmåde nedenfor, men sørg for at fjerne markeringen i afkrydsningsfelterne **Udfør konvertering** og **Momssatsændringsværktøjet afsluttet**. Under testkonverteringen ryddes feltet **Konverteret** i tabellen **Momssatsændringslogpost** og feltet **Konverteringsdato** i tabellen **Momssatsændringslogpost** er tomt. Når konverteringen er afsluttet, skal du vælge **Ændringslogposter for momssats** for at få vist resultaterne af prøvekonverteringen. Kontroller hver post, før du udfører konverteringen. Kontroller især transaktioner, som bruger en gammel momssats.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momssatsændring**, og vælg derefter linket **Konfiguration af ændring af momssats**.  
2. Kontroller, at du allerede har oprettet momsproduktbogføringsgruppekonverteringen eller den generelle produktbogføringsgruppekonvertering.  
3. Markér afkrydsningsfeltet **Udfør konvertering**.  

    > [!IMPORTANT]  
    >  Fjern markeringen af afkrydsningsfeltet **Momssatsændringsværktøjet afsluttet**. Afkrydsningsfelt vælges automatisk, når konverteringen af momssatsændring er afsluttet.  

4. Vælg handlingen **Konverter**.  
5. Når konverteringen er afsluttet, skal du vælge handlingen **Ændringslogposter for momssats** for at få vist resultaterne af konverteringen.  

> [!IMPORTANT]  
> Efter konverteringen er feltet **Konverteret** valgt i tabellen **Momssatsændringslogpost**, og feltet **Konverteringsdato** i tabellen **Momssatsændringslogpost** viser konverteringsdatoen.  

## Se også

[Opsætte merværdiafgift (moms)](finance-setup-vat.md)  
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
