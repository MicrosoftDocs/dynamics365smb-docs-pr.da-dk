---
title: Registrere særlige købspriser og rabatter
description: Du kan angive forskellige eller alternative priser og rabataftaler og anvende dem på købsdokumenter for kreditorer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Registrere særlige købspriser og rabatter

> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet strømlinede processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, der bruger den version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

De forskellige pris- og betalingsaftaler, der gælder, når du køber fra forskellige leverandører, skal defineres, så de aftalte regler og værdier anvendes i de købsdokumenter, der oprettes for leverandørerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[prod_short](includes/prod_short.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger i [Beregning af bedste pris](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

Med hensyn til priser kan du få en særlig købspris indsat på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes.

Med hensyn til rabatter kan du oprette og bruge to typer købsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Købslinjerabat** |En beløbsrabat, der indsættes på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes. Dette fungerer på samme måde som for købspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et købsdokument overstiger et bestemt minimum. |

Da købslinjerabatter og købspriser er baseret på en kombination af vare og leverandør, kan du også angive denne konfiguration fra det varekort, hvor reglerne og værdierne er defineret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

## Sådan oprettes en særlig købspris for en kreditor

#### [Aktuel oplevelse](#tab/current-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Priser**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

#### [Ny oplevelse](#tab/new-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Vælg debitoren, og vælg derefter handlingen **Salgsprislister**.
3. Vælg **Ny** for at oprette en ny købsprisliste.
4. Udfyld felterne efter behov i oversigtspanelerne **Generelt** og **Skat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Benyt en af følgende fremgangsmåder for at føje elementer til listen:
   * Hvis du vil tilføje mange varer, skal du vælge **Foreslå linjer** og derefter angive filterkriterier for at angive, hvilke varetyper der skal tilføjes. Du kan også vælge at angive yderligere indstillinger for de varer, der er specifikke for prislisten. Om nødvendigt kan du ændre den.
   * Hvis du vil kopiere varer fra en anden prisliste, skal du vælge **Kopier linjer** og derefter vælge den prisliste, der skal kopieres.
   * Hvis du vil tilføje varer manuelt i gitteret, skal du i feltet **Produkttype** vælge den produkttype, som prislisten vedrører. Afhængig af dine valg skal du udfylde de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynde at bruge prislisten, skal du vælge **Aktiv** i feltet **Status**.

---

## Sådan oprettes en linjerabat for en kreditor

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Linjerabatter**.

   Feltet **Leverandørnr.** er allerede udfyldt med kreditornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

## Sådan oprettes en fakturarabat for en kreditor

Når dine kreditorer har oplyst, hvilke fakturarabatter de yder, skal du angive fakturarabatkoden på kreditorkortene og definere betingelserne for hver kode.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn kreditorkortet for en kreditor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til kreditoren.

    > [!NOTE]  
    > Fakturarabatkoder repræsenteres af eksisterende kreditorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til kreditorer ved at vælge navnet på en anden leverandører, der skal have samme betingelser.

    Fortsæt med at angive nye fakturarabatbetingelser for køb.
4. På siden **Kreditorkort** skal du vælge handlingen **Fakturarabatter**. Siden **Kred./fakt.-rabatter** åbnes.
5. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for DKK.
6. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
7. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
8. Gentag trin 5-7 for hver valuta, som kreditoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende kreditor. Når du vælger kreditorkoden i feltet **Fakturarabatkode** på andre kreditorkort, knyttes samme fakturarabat til den pågældende kreditorer.

## Sådan vælges en metode til bogføring af rabatter

Når du bogfører en købsfaktura, som der ydes en eller to rabatter på, kan du vælge mellem to metoder til at bogføre mængderabatter. Du kan bogføre rabatter separat, eller du kan fratrække rabatter som fakturarabatter.  

Før du kan gøre dette, skal du allerede have oprettet de nødvendige konti til bogføring af rabatbeløb i kontoplanen. Du skal også kontrollere, at du har angivet de korrekte kontonumre i bogføringsopsætning i felterne **Købslinjerabatkonto** og **Købsfakturarabatkonto**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Købsopsætning** og derefter vælge det relaterede link.
2. Vælg et af følgende bogføringsmetoder i feltet **Bogføring med rabat**.

|**Metode til bogføring af rabat**|**Fakturarabat**|**Linjerabat**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle rabatter**|Bogført separat|Bogført separat|  
|**Fakturarabat**|Bogført separat|Fratrukket|  
|**Linjerabat**|Fratrukket|Bogført separat|  
|**Ingen rabat**|Fratrukket|Fratrukket|  

## Købsfakturarabatter og servicegebyrer

Du kan angive de faste betingelser for fakturarabat, som bruges af dine kreditorer. Rabatten beregnes automatisk, når du udfylder en købsfaktura.  

Før du kan bruge fakturarabatter ved køb, skal du angive de kreditorer, som yder rabat.  

Du kan knytte rabatter til bestemte fakturabeløb på siderne **Kred./fakt.-rabatter**. Du kan angive et vilkårligt antal procenter på hver side. Hver debitor kan have sin egen side, eller du kan sammenkæde flere debitorer på den samme side.  

Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til rabatprocenten.  

Du kan definere, at betingelserne for fakturarabatten er DKK for danske kreditorer og udenlandsk valuta for udenlandske kreditorer.  

Du kan få [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at beregne fakturarabatter i rekvisitioner, rammeordrer, ordrer, fakturaer og kreditnotaer.  

> [!TIP]  
> Det anbefales, at du forbereder en skitse over den rabatstruktur, der skal anvendes, før du begynder at indtaste disse oplysninger. Det gør det nemmere at se, hvilke kreditorer der kan knyttes til samme fakturarabatside. Jo færre sider, du har sat op, jo hurtigere kan du indtaste stamoplysningerne.

## Beregning af bedste pris

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[prod_short](includes/prod_short.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk denne pris, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
> I det følgende beskrives, hvordan den bedste pris beregnes for salg. Beregningen er den samme for køb.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    - Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    - Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    - Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om der ligger pris-/ rabataftaler i oplysningerne om dokument- eller kladdelinjen og indsætter derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    - Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom RV giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[prod_short](includes/prod_short.md)] den laveste pris og den højeste linjerabat i RV.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## Se også

[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
