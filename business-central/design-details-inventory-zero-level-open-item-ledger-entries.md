---
title: Åbn vareposter for lagerbeholdning nul
description: 'Denne artikel vedrører et problem, hvor lagerniveauet er nul, selvom der findes åbne vareposter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designoplysninger: Kendt problem med vareudligning
Denne artikel vedrører et problem, hvor lagerniveauet er nul, selvom der findes åbne vareposter [!INCLUDE[prod_short](includes/prod_short.md)].  

Artiklen starter ved at angive typiske symptomer på problemet, efterfulgt af de grundlæggende oplysninger om vareudligning til at understøtte de beskrevne årsager til problemet. I slutningen af artiklen er en løsning til at løse sådanne åbne vareposter.  

## Symptomer på problemet  
 De typiske symptomer på problemet med nul lager, selvom der findes åbne vareposter, er følgende:  

-   Du får vist følgende meddelelse, når du forsøger at lukke en lagerperiode: "Lageret kan ikke lukkes, fordi der er negativt lager for én eller flere varer".  

-   En situation med en varepost, hvor både en udgående varepost og dens relaterede indgående varepost er åben.  

     Se følgende eksempel på en situation med en varepost.  

     |Løbenummer|Bogføringsdato|Postens type|Dokumenttype|Bilagsnr.|Varenr.|Lokationskode|Antal|Kostbeløb (faktisk)|Faktureret antal|Restantal|Åbn|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
     |334|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|1|10|1|1|Ja|  

## Grundlæggende oplysninger om vareudligning  
 Der oprettes en vareudligningspost for hver lagertransaktion for at kæde omkostningsmodtageren sammen med omkostningskilden, så omkostningerne kan videresendes i henhold til kostmetoden. Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).  

-   For en indgående varepost oprettes vareudligningsposten, når vareposten oprettes.  

-   For en udgående varepost oprettes vareudligningsposten, når finansposten bogføres, hvis der er en åben indgående varepost med et disponibelt antal, den kan anvendes på. Hvis der ikke er nogen åben indgående varepost, som den kan anvendes på, så forbliver den udgående varepost åben, indtil der posteres en indgående varepost, som den kan anvendes på.  

 Der er to typer af vareudligning:  

-   Mængdeudligning  

-   Kostprisudligning  

### Mængdeudligning  
 Mængdeudligninger foretages for alle lagertransaktioner, og de oprettes automatisk eller manuelt i særlige processer. Når de foretages manuelt, kaldes mængdeudligninger for fast udligning.  

 I følgende diagram vises, hvordan mængdeudligninger foretages.  

![Flow af udgiftsjustering fra køb til salg.](media/helene/TechArticleInventoryZero2.png "Flow af udgiftsjustering fra køb til salg")

 Bemærk ovenfor, at vareposten 1 (køb) både er leverandør af varen og omkostningskilden til den udlignende varepost, varepost 2 (salg).  

> [!NOTE]  
>  Hvis den udgående varepost værdiansættes fra gennemsnitlige kostpris, er den anvendte indgående varepost ikke den entydige omkostningskilde. Den spiller blot en rolle i beregningen af den gennemsnitlige kostpris for perioden.  

### Kostprisudligning  
Kostprisudligninger oprettes kun for indgående transaktioner, hvor feltet **Udlign fra-varepost** er udfyldt for at oprette en fast udligning. Dette sker typisk i forbindelse med en salgskreditnota og et scenarie med annullering af leverance. Kostprisudligningen sikre, at varen går ind på lageret igen med samme kostpris, som da den blev leveret.  

I følgende diagram vises, hvordan kostprisudligninger foretages.  

|Løbenummer|Bogføringsdato|Postens type|Dokumenttype|Bilagsnr.|Varenr.|Lokationskode|Antal|Kostbeløb (faktisk)|Faktureret antal|Restantal|Åbn|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
|334|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|1|10|1|1|Ja|  

 Bemærk over den indgående varepost 3 (salgsreturvareordre) er en omkostningsmodtager for den oprindelige udgående varepost 2 (salg).  

## Illustration af et grundlæggende omkostningsflow  
 Forudsæt et komplet omkostningsflow, hvor en vare modtages, leveres og faktureres og returneres med nøjagtig\-kostpristilbageførsel og derefter sendes igen.  

 I følgende diagram illustreres omkostningsflowet.  

![Flow af udgiftsjustering fra salg til salgsreturvare.](media/helene/TechArticleInventoryZero4.png "Flow af udgiftsjustering fra salg til salgsreturvare")

 Bemærk over kostprisen overføres til vareposten 2 (salg) og derefter til vareposten 3 (salgsreturvareordre), og til sidst til vareposten 4 (salg 2).  

## Årsager til problemet  
 Problemet med nul lager, selvom der findes åbne vareposter, kan være forårsaget af følgende scenarier:  

-   Scenarie 1: En leverance og en faktura bogføres, selvom varen ikke er tilgængelig. Bogføringen tilbageføres derefter med præcis kostprisudligning med en salgskreditnota.  

-   Scenarie 2: En leverance bogføres, selvom varen ikke er tilgængelig. Bogføring annulleres derefter med funktionen Annuller leverance.  

 I følgende diagram illustreres, hvordan vareudligninger foretages i begge scenarier.  

![Flow af udgiftsjustering vises i begge retninger..](media/helene/TechArticleInventoryZero6.png "Flow af udgiftsjustering vises i begge retninger")  

 Bemærk, at der foretages en kostprisudligning (vises med blå pil) for at sikre, at post 2 (salgsreturvareordre) tildeles samme omkostninger som den varepost, den udligner, varepost 1 (salg 1). Men, der foretages ikke en antalsudligning (repræsenteret af den røde pil).  

 Varepost 2 (salgsreturvareordre) kan ikke være både omkostningsmodtager for den oprindelige varepost og samtidig være en leverandør af varer og deres omkostningskilde. Derfor kan den oprindelige varepost 1 (salg 1) forblive åben, indtil der vises en gyldig kilde.  

## Identificere problemet  
 Gør følgende i det respektive scenarie for at finde ud af, om de åbne vareposter er oprettet:  

 I scenarie 1 kan du identificere problemet på følgende måde:  

-   På siden **Bogført salgskreditnota** eller **Bogført returvaremodt.** skal du foretage opslag fra feltet **Udlign\-fra-vareposten** for at se, om feltet er udfyldt, og så tilfælde til hvilken varepost returneringsmodtagelsen er omkostningsudlignet.  

 I scenarie 2 kan du identificere problemet på en af følgende måder:  

-   Søg efter en åben udgående varepost og en indgående varepost med samme nummer i feltet **Bilagsnr.** og Ja i feltet **Rettelse**. Se følgende eksempel på en sådan situation med en varepost.  

|Løbenummer|Bogføringsdato|Postens type|Dokumenttype|Bilagsnr.|Varenr.|Lokationskode|Antal|Kostbeløb (faktisk)|Faktureret antal|Restantal|Åbn|Rettelse|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|Nej|  
|334|28-01-2018|Salg|Salgsleverance|102043|TEST|BLÅ|1|10|1|1|Ja|**Ja**|  

-   På siden **Bogført salgsleverance** skal du foretage opslag fra feltet **Udlign fra-varepost** for at se, om feltet er udfyldt, og så tilfælde til hvilken varepost returneringsmodtagelsen er omkostningsudlignet.  

> [!NOTE]  
>  Kostprisudligning kan ikke identificeres på siden **Udlignede vareposter**, da siden kun viser mængdeudligninger.  

 I begge scenarier kan du identificere den involverede kostprisudligning på følgende måde:  

1.  Åbn tabellen **Vareudligningspost**.  

2.  Filtrer efter **Varepostløbenr.** ved hjælp af nummeret på vareposten for salgsreturvareordren.  

3.  Analysér vareudligningsposten og vær opmærksom på følgende:  

     Hvis feltet **Udgående varepostløbenr.** er udfyldt for en indgående varepost (positivt antal), betyder det, at den indgående varepost er omkostningsmodtager for den udgående varepost.  

     Se følgende eksempel på en vareudligningspost.  

     |Løbenummer|Varepostløbenr.|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|Bogføringsdato|Kostprisudligning|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28-01-2018|Ja|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Læg mærke til ovenfor, at den indgående varepost 334 er omkostningsudlignet til den udgående varepost 333.  

## Løsning til problemet  
 På siden **Varekladde** skal du bogføre følgende linjer for den pågældende vare:  

-   En opregulering for at lukke den åbne udgående varepost.  

-   En nedregulering med det samme antal.  

     Denne regulering balancerer den lagerforøgelse, der er forårsaget af opreguleringen og lukker den åbne indgående varepost.  

 Resultatet er, at lageret er nul, og alle vareposter er lukket.  

## Se også  
[Designoplysninger: Vareudligning](design-details-item-application.md)   
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]