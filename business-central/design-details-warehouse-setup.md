---
title: Designoplysninger – Opsætning af lager | Microsoft Docs
description: Lagerfunktioner i Business Central indeholder forskellige niveauer af kompleksitet, som defineret af licenstilladelser i de tilbudte moduler. Niveauet af kompleksitet i en løsning på lagerstedet defineres i høj grad af placeringsopsætningen på lokationskort, som til gengæld licensstyres, så adgang til placeringens opsætningsfelter er defineret af licensen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/04/2020
ms.author: sgroespe
ms.openlocfilehash: cd2a282e95e324e3adbf06cb72c53467f63c227b
ms.sourcegitcommit: ccae3ff6aaeaa52db9d6456042acdede19fb9f7b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435227"
---
# <a name="design-details-warehouse-setup"></a>Designoplysninger: Opsætning af lager

Lagerfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder forskellige niveauer af kompleksitet, som defineret af licenstilladelser i de tilbudte moduler. Niveauet af kompleksitet i en løsning på lagerstedet defineres i høj grad af placeringsopsætningen på lokationskort, som til gengæld licensstyres, så adgang til placeringens opsætningsfelter er defineret af licensen. Desuden styrer programobjekter i licensen, hvilket UI-dokument der skal bruges til de understøttede lageraktiviteter.  

Der findes følgende lagerrelaterede moduler:  

- Grundlæggende lagerbeholdning (4010)  
- Placering (4170)  
- Læg-på-lager (4180)  
- Lagermodtagelse (4190)  
- Pluk (4200)  
- Lagerleverance (4210)  
- Logistiksystemer (4620)  
- Interne pluk og læg-på-lager (4630)  
- Automated Data Capture System (4640)
- Opsætning af placering (4660)  

Du kan finde flere oplysninger om hvert begreb i [[!INCLUDE[d365fin](includes/d365fin_md.md)]-prisark](https://go.microsoft.com/fwlink/?LinkId=238341) (kræver PartnerSource-konto).  

Følgende tabel viser, hvilke moduler der er nødvendige for at definere forskellige lagerkompleksitetsniveauer, hvilke dokumenter til brugergrænsefladen der understøtter hvert niveau, og hvilke lokationskoder der afspejler disse niveauer i [!INCLUDE[d365fin](includes/d365fin_md.md)]-demodatabasen.  

|Kompleksitetsniveau|Beskrivelse|Brugergrænsefladedokument|CRONUS-lokation|Mindste modulkrav|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Ingen dedikeret lageraktivitet.<br /><br /> Modtag/levér-bogføring fra ordrer.|Ordre|BLÅ|Grundlæggende lagerbeholdning|  
|2|Ingen dedikeret lageraktivitet.<br /><br /> Modtag/levér-bogføring fra ordrer.<br /><br /> Placeringskode er påkrævet.|Ordre, med placeringskode|SØLV|Grundlæggende lagerbeholdning/Placering|  
|3 <br /><br /> **Bemærk:** Selvom indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.|Grundlæggende lageraktivitet, ordre-for-ordre.<br /><br /> Modtag/levér-bogføring fra lager, læg-på-lager/plukdokumenter. <br /><br /> Placeringskode er påkrævet.|Lager, læg-på lager/flytning (lager)/lagerpluk med placeringskode|(SØLV + Kræv læg-på-lager eller Kræv læg-på-lager)|Grundlæggende lagerbeholdning/Placering/Læg-på-lager/Pluk|  
|4|Avanceret lageraktivitet for flere ordrer.<br /><br /> Konsolideret modtag/levér-bogføring baseret på lagerstedets læg-på-lager-/plukregistreringer.|Lagermodtagelse/Læg-på-lager (logistik)/Pluk (logistik)/Pluk (logistik)/Plukkladde|GRØN|Grundlæggende lagerbeholdning/Lagermodtagelse/Læg-på-lager/Pluk/Lagerleverance|  
|5|Avanceret lageraktivitet for flere ordrer.<br /><br /> Konsolideret modtag/levér-bogføring baseret på lagerstedets læg-på-lager-/plukregistreringer.<br /><br /> Placeringskode er påkrævet.|Lagermodtagelse/Læg-på-lager (logistik)/Pluk (logistik)/Pluk (logistik)/Plukkladde/Læg på lager-kladde, med placeringskode|(GRØN + Tvungen placering)|Grundlæggende lagerbeholdning/Placering/Lagermodtagelse/Læg-på-lager/Pluk/Lagerleverance|  
|6 <br /><br /> **Bemærk**: Dette niveau omtales som "Logistik", da det kræver de mest avancerede detaljerede logistiksystemer.|Avanceret lageraktivitet for flere ordrer<br /><br /> Konsolideret modtag/levér-bogføring baseret på lagerstedets læg-på-lager-/plukregistreringer<br /><br /> Placeringskode er påkrævet.<br /><br /> Zone/klassekode er valgfrit.<br /><br /> Lagermedarbejdere, der er styret af arbejdsproces<br /><br /> Planlægning af placeringsgenbestilling<br /><br /> Placeringsniveau<br /><br /> Opsætning af placering efter kapacitet<br /><br /> Allokering <!-- Hand-held device integration -->|Lagermodtagelse/Læg-på-lager (logistik)/Pluk (logistik)/Pluk (logistik)/Bevægelse (logistik)/Plukkladde/Læg på lager-kladde/Internt lagerpluk/Internt læg-på-lager, med placering/klasse/zonekode<br /><br /> Forskellige kladder til styring af placering<br /><br /> ADCS-skærme|HVID|Grundlæggende lagerbeholdning/Placering/Læg-på-lager/Lagermodtagelse/Pluk/Lagerleverance/Logistik/Internt pluk og læg-på lager/Placeringsopsætning/<!-- Automated Data Capture System/ -->Opsætning af placering|  

Se eksempler på, hvordan brugergrænsefladeelementer bruges afhængigt af kompleksitetsniveauet på lageret, i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Placering og placeringsindhold

En placering er en lagerenhed, der er beregnet til at indeholde adskilte dele. Det er den mindste containerenhed i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Antal varer på placeringer kaldes placeringsindhold. Et opslag fra feltet **Vare** eller feltet **Placeringskode** i enhver lagerrelateret dokumentlinje viser den beregnede beholdning af varen på placeringen.  

Placeringsindhold kan gives egenskaben Fast, Dedikeret eller Standard for at definere, hvordan du kan bruge placeringsindholdet. Placeringer uden nogen af disse egenskaber kaldes løse placeringer.  

En fast placering indeholder varer, der er tildelt den pågældende placeringskode. Egenskaben Fast placering sikrer, at selvom placeringsindholdet tømmes et øjeblik, vil placeringsindholdet ikke forsvinde, og placeringen er derfor valgt igen, så snart det er genopfyldt.  

En dedikeret placering indeholder placeringsindhold, der kun kan plukkes til den dedikerede ressource, som f.eks. en produktionsressource, der bruger den pågældende placering. Andet ikke-plukindhold som f.eks. antal udgående på en leverancebogføring kan stadig forbruges fra en dedikeret placering. Det er kun placeringsindhold, der tages i betragtning af algoritmen **Opret pluk**, der er beskyttet i en dedikeret placering.  

Egenskaben for standardplacering bruges af systemet til at foreslå placeringer til lageraktiviteter. Ved WMS-lokationer bruges standardegenskaben for placeringer ikke. På steder, hvor der kræves placeringer, bruges egenskaben i indgående flows til at angive, hvor varer skal placeres. Egenskaben bruges til at angive, hvor du kan tage varer fra, i udgående strømme.  

> [!NOTE]  
>  Hvis udgående varer bliver anbragt på flere placeringer, tages varer først fra de placeringer, der ikke er standard, for at tømme placeringens indhold, og de resterende varer tages fra standardplaceringen.  

Der kan kun være en standardplacering pr. vare pr. lokation.  

## <a name="bin-type"></a>Placeringstype

I logistikinstallationer kan du begrænse de lageraktiviteter, der er tilladt for en placering, ved at tildele en placeringstype. Der findes følgende placeringstyper:  

|Placeringstype|Beskrivelse|  
|------------------|---------------------------------------|  
|MODTAG|Varer, der er bogført som modtagne, men endnu ikke lagt på lager.|  
|LEVER|Varer, der er plukket til lagerleverancelinjer, men som endnu ikke er bogført som leveret.|  
|LGT-PÅ-LGR|Typisk varer, der skal opbevares i store måleenheder, men som du ikke ønsker, der skal oprettes pluk af. Da der ikke plukkes fra disse placeringer, hverken til produktionsordrer eller leverancer, kan brugen af placeringer af typen Læg-på-lager være begrænset, men denne type placering kan være nyttig, hvis du har købt en stort antal varer. Placeringer af denne type skal altid have et lavt placeringsniveau, hvilket medfører, at når modtagne varer lægges på lager, lægges andre først på lager på placeringer af typen LPLPLUK med et højere niveau, og som er fast tilknyttet varen. Hvis du bruger denne type placering, skal du regelmæssigt udføre placeringsgenopfyldning, så de varer, der opbevares på disse placeringer, også er tilgængelige på placeringer af typen LPLPLUK eller PLUK.|  
|PLUK|Elementer, der kun skal bruges til plukning. Genopfyldning af disse placeringer kan kun foretages ved flytning, ikke som læg-på-lager.|  
|LPLPLUK|Varer på placeringer, der foreslås for både læg-på-lager og pluk-funktioner. Placeringer af denne type har som regel forskellige placeringsniveau. Du kan fastsætte massevareplaceringer til denne placeringstype og give dem lave placeringsniveauer sammenlignet med de almindelige plukplaceringer eller forreste placeringer i plukområdet.|  
|KK|Denne placering bruges til lagerreguleringer, hvis du angiver placeringen i feltet **Reguleringsplaceringskode** på lokationskortet. Du kan også bruge denne type placeringer til defekte varer og varer, der skal kontrolleres. Du kan flytte varer til den type placering, hvis du ikke vil have, at de indgår i den normale varestrøm. **Bemærk:** I modsætning til alle andre placeringstyper har placeringstypen **KK** ingen af afkrydsningsfelterne til håndtering af varen markeret som standard. Dette angiver, at ethvert indhold, du placerer i en KK-placering er udelukket fra vareforløb.|  

For alle placeringstyper, undtagen PLUK, LPLPLUK og LÆGPÅLAGER, tillades ingen andre aktiviteter for placeringen, end dem der er defineret af placeringstypen. For eksempel kan en placering af typen **Modtag** kun bruges til at modtage varer eller plukke varer fra.  

> [!NOTE]  
> Kun bevægelse kan gøres på placeringer af typen MODTAG og KK. Ligeledes kan kun bevægelser foretages fra placeringer af typen LEVER og KK.  

## <a name="bin-ranking"></a>Placeringsniveau

I avancerede lagerfunktioner kan du automatisere og optimere, hvordan varerne samles i læg-på-lager- og plukkladder ved at rangere placeringer, så varer foreslås taget eller anbragt i henhold til rangkriterier for at bruge lagerplads optimalt i avanceret logistik.  

Læg-på-lager-processer er optimeret efter placeringsniveau ved at foreslå placeringer på højt niveau før placeringer på lavt niveau. På samme måde bliver plukprocesser optimeret ved først at foreslå varer fra placeringsindhold med højt placeringsniveau. Desuden foreslås placeringsgenbestillinger fra placeringer på lavt placeringsniveau til placeringer på højt placeringsniveau.  

Placeringsniveau sammen med placeringsindholdsoplysninger er de grundlæggende indstillinger, der gør det muligt for brugere at lægge varer på lageret.  

## <a name="bin-setup"></a>Opsætning af placering  
I avanceret logistik kan placeringer konfigureres med værdier for kapacitet, f.eks. antal, samlede rummål og vægt, for at styre, hvor og hvordan varer opbevares på placeringen.  

Du kan tildele en måleenhed for varen, f.eks. stykker, paller, liter, gram eller kasser, på hvert enkelt varekort. Du kan også have en grundlæggende enhed for en vare og angive større enheder, der er baseret på den. Du kan f.eks. definere, at en palle skal være lig med 16 stykker med sidstnævnte som den grundlæggende måleenhed.  

Hvis du vil angive en maksimal mængde af en bestemt vare, der skal gemmes i en enkelt placering, og varen har mere end én enhed, skal du angive det maksimale antal for hver enhed, der findes på varekortet. Hvis en vare er oprettet til at skulle håndteres i enheder og paller, skal feltet **Maks.antal** på siden **Placeringsindhold** for den pågældende vare også være i enheder og paller. Ellers beregnes det tilladte antal for placeringen ikke korrekt.  

Før du kan angive kapacitetsbegrænsninger for placeringsindhold på en placering, skal du først sikre dig, at varens måleenheder og dimensioner er blevet indstillet på varekortet.  

> [!NOTE]  
> Det er kun muligt at operere med flere måleenheder i logistikinstallationer. I alle andre konfigurationer kan placeringsindhold kun være i basismåleenheden. I alle transaktioner med en måleenhed, der er højere end varens grundlæggende måleenhed, konverteres antallet til den grundlæggende enhed.  

## <a name="zone"></a>Zone

Placeringer kan grupperes i zoner til at styre, hvordan arbejdsprocessen for lageraktiviteter ledes i avanceret logistik.  

En zone kan være en modtagelseszone eller en lagerzone, og hver zone kan bestå af en eller flere placeringer.  

De fleste egenskaber, der er tildelt en zone, tildeles som standard den placering, der er oprettet fra denne zone.  

## <a name="class"></a>Klasse  
Du kan tildele lagerklassekoder i avanceret logistik til varer, placeringer og zoner for at styre, hvor forskellige vareklasser gemmes som frosne varer. Du kan opdele en zone i flere lagerklasser. Varer på modtagelseszonen kan f.eks. gemmes som frosne, farlige eller andre kategorier.  

Når du arbejder med lagerklasser og en standardplacering for modtagelse/afsendelse, skal du manuelt udfylde de korrekte placeringer for modtagelses- og leverancelinjer for lagerstedet.  

Klassekoden fremhæves kun i indgående strømme på indgående linjer, hvor vareklassekoden ikke stemmer overens med standardmodtagelsesplacering. Hvis der ikke er tildelt korrekte standardplaceringer, kan antallet ikke modtages.  

## <a name="location"></a>Lokation

En lokation er en fysisk struktur eller et sted, hvor lagerbeholdning modtages, opbevares og forsendes, muligvis organiseret efter placering. En lokation kan være et lagersted, en bil, et showroom, en fabrik eller et område på en fabrik.  

## <a name="first-expired-first-out"></a>Først udløbet først ude

Hvis du markerer afkrydsningsfeltet **Pluk i overensstemmelse med FEFO** i oversigtspanelet **Placeringsmetode** på lokationskortet, bliver varesporede varer plukket i henhold til deres udløbsdato. Varer med den tidligste udløbsdato plukkes først.  

Lageraktiviteter i alle pluk- og bevægelsesdokumenter er sorteret i overensstemmelse med FEFO, medmindre de pågældende varer allerede har tildelte serienumre/lotnumre. Hvis det kun er en del af antallet på linjen, der er tildelt lot-/serienumre, bestemmes det resterende antal, der skal plukkes, vha. FEFO-metoden.  

Når der plukkes varer efter FEFO-metoden, samles de tilgængelige varer, der udløber først, på en midlertidig varesporingsliste, der er baseret på udløbsdatoen. Hvis der er to varer med samme udløbsdato, vælges varen med det laveste lot- eller serienummer. Hvis lot- eller serienumrene er ens, vælges den vare først, der blev registreret først. Standardkriterierne for udvælgelse af varer på plukplaceringer, f.eks. Placeringsniveau og Nedbrydning, anvendes på denne midlertidige FEFO-varesporingsliste.  

## <a name="put-away-template"></a>Læg-på-lager-skabelon

Læg-på-lager-skabelonen kan tildeles til en vare og en lokation. Læg-på-lager-skabelonen angiver en række prioriterede regler, der skal overholdes ved oprettelse af læg-på-lager-aktiviteter. En læg-på-lager-skabelon kan f.eks. kræve, at varen placeres på en placering med placeringsindhold, der svarer til enheden, og hvis der ikke findes en lignende placering med tilstrækkelig kapacitet, skal varen placeres på en tom placering.  

## <a name="see-also"></a>Se også

[Designoplysninger: Logistik](design-details-warehouse-management.md)   
[Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md)
