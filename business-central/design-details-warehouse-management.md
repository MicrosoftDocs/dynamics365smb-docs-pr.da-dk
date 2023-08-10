---
title: Administrere lageraktiviteter
description: Ud over modtagelser og leverancer understøtter Business central en række interne lagerstedsaktiviteter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Oversigt over logistik

Der er to ting, der er vigtige for alle virksomheder, der fysisk kan flytte varer på og ud af deres lagersted:

* De har en oversigt over lagerniveauer og vareplaceringer på lagerstedet.
* De kan hurtigt og præcist modtage, plukke og levere varer.

Hvis du vil hjælpe virksomheder med at opnå disse ting, kan logistikfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] føje følgende funktioner til lagerstyring:

* Placering
* Lagerstedsleverancer
* Lagerpluk
* Bevægelseskladde

Implementer disse funktioner i forskellige kombinationer for at skræddersy lagerprocesserne til virksomheden. Giver større kompleksitet, når virksomheden vokser, og processerne ændres.

## <a name="overview-of-different-configuration-options"></a>Oversigt over forskellige konfigurationsindstillinger

Du kan konfigurere lagerfunktioner på forskellige måder. Det er vigtigt at vælge de indstillinger, der forbedrer processerne uden at medføre spild. Følgende tabel indeholder en oversigt over typiske konfigurationer til at håndtere fysiske varer.

|Kompleksitetsniveau|Beskrivelse|Indstillinger|Placeringskode|Eksempel på indgående flow|Eksempel på udgående flow|Eksempel på internt flow|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikeret lageraktivitet.|Bogføring af ordrer og kladder||Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Købsordre|Salgsordre| Produktionsordre -> Forbrugskladde|  
|Basis|Konsolideret modtagelse/levering for flere ordrer.|**Kræv modtagelse**<br>**Kræv leverance**|Valgfri. Kontrolleret af Placeringskoden er obligatorisk til/fra|Købsordrer-> lagerstedsmodtagelse|Salgsordre -> Lagerstedsleverance|Samme som ovenfor.|
|Basis|Ordre for ordre|Kræv læg på lager eller Kræv pluk. </br><br/> **Bemærk**: Selvom indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.|Valgfri. Kontrolleret af **Placeringskoden er obligatorisk** til/fra.|Købsordre -> Læg-på-lager|Salgsordre -> Lagerpluk|Produktionsordre -> Lagerpluk|
|Avanceret|Konsolideret modtagelse/levering for flere ordrer.<br /><br />Konsoliderede pluk/læg på lager-aktiviteter for flere kildedokumenter.|Kræv tilgang + Kræv læg på lager</br> Kræv leverance + Kræv pluk|Valgfri. Kontrolleret af Placeringskoden er obligatorisk til/fra|Købsordrer -> lagerstedsmodtagelse -> læg på lagersted|Salgsordrer -> lagerstedsleverancer -> Plukkladde -> pluk fra lagersted| Produktionsordrer -> Pluk arbejdsordre -> Lagerstedspluk -> Forbrugskladde|
|Avanceret|Samme som over + Styret pluk/læg-på-lager-aktiviteter|Styret pluk og læg-på-lager (afhængige Skift aktiveres automatisk)|Obligatorisk|Samme som ovenfor.|Samme som ovenfor.| Produktionsordrer -> Pluk arbejdsordre -> Lagerstedspluk Forbrugskladde|

Kompleksiteten øges med organisationens størrelse, og hvor mange afdelinger og personer der er involveret. En proces kan være simpel, f. eks. når den samme person opretter og bogfører et salgsdokument. Processer kan også være mere komplekse og omfatte flere trin og personer. Følgende trin er et eksempel på en mere kompleks proces:

1. En ordrebehandler opretter salgsordrer.
1. Lagerstedschefen opretter plukinstruktioner.
1. En lagermedarbejder afslutter forløbet ved at bogføre lagerleverancen.

Kompleksitetsniveauet påvirkes også af den type dokumenter, du bruger i lageraktiviteterne. Du kan f. eks. bruge lagermodtagelse og læg-på-lager-dokumenter til indgående flow, men bruge lagerplukdokumenter til udgående flow.

En anden faktor, der påvirker kompleksiteten, er den måde, dit fysiske lager er repræsenteret på i [!INCLUDE[prod_short](includes/prod_short.md)]. Lær mere i [Modellering af det fysiske lagersted](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Modellering af det fysiske lagersted

Der er flere muligheder for at repræsentere den real-verden, der er konfigureret på lagerstedet, i [!INCLUDE[prod_short](includes/prod_short.md)]. Dine valg bestemmer, hvordan du kan arbejde med lagerfunktioner.

Placeringen af varer kan være hylder, lokationer eller placeringer, og der er forskellige muligheder og ulemper ved hver indstilling.

### <a name="locations-and-bins"></a>Lokationer og placeringer

Hvis du vil håndtere fysiske varer, skal du have mindst én lokation. Du kan bruge flere lokationer eller bruge placeringer til at udforme lagerstedet og organisationsstrukturen.

Typisk er lokationer den foretrukne metode til at organisere operationer, som er fordelt på tværs af geografiske områder. I nogle tilfælde kan det imidlertid være, at du vil oprette flere lokationer, der er placeret samme sted. Der er følgende fordele ved at bruge lokationerne:

* Tildele adgang ved hjælp af siderne **Lagermedarbejder** og **Ansvarscentre**.
* Definere kalendere, ruter og indgående og udgående tid til datoberegning og planlægning. flere oplysninger i [Om planlægningsfunktionen](production-about-planning-functionality.md).
* Angive standarddimensioner og bruge forskellige vare bogføringsopsætninger.
* Opsætte planlægningsparametre. Få mere at vide i [Planlægning af parametre](production-about-planning-functionality.md#planning-parameters).  
* Brug forskellige lagerfunktioner for hver lokation.

### <a name="shelves-and-bins"></a>Hylder og placeringer

Hvis du altid gemmer en vare på samme sted, kan du bruge feltet **Hyldenr.** feltet **varekortet** eller **lageropbevaringskortet** på siderne. Feltet kan bruges som et grundlæggende manuelt lagersystem i miljøer uden placeringer. Det kopieres fra varekortet til dokumentlinjer og rapporter, men det er kun til orientering. Værdien anvendes ikke i lageraktivitetsanmodninger eller i disponeringsberegninger.

Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer:

* En eller flere faste placeringer for en vare.
* Placeringer for bestemte operationer, f. eks. en leveringsplacering eller en produktionsoutputplacering.
* Placeringskapacitet og vægtbegrænsninger (kun ved styret læg-på-lager og pluk).
* Placeringsvurdering (for styret læg-på-lager og pluk).

## <a name="typical-warehouse-workflow"></a>Typisk lagergang for lager

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|I en grundlæggende proces for ordre-til-ordre-du kan bruge en læg-på-lager-aktivitet til at registrere modtagelsen af varer på lokationer, inklusive eventuel overlevering. Hvis du konsoliderer flere ordrer i modtagelsen, skal du bruge en lagermodtagelse.|[Indgående strøm](design-details-inbound-warehouse-flow.md)|
|Registrere leveringen af varer fra lagerlokationen. Brug et lagerpluk på grundlag af ordre pr. ordre. Hvis du konsoliderer flere ordrer i modtagelsen, skal du bruge en lagermodtagelse.|[Udgående strøm](design-details-outbound-warehouse-flow.md)|
|Håndtere varer på lagerlokationen. Hvis du f. eks. flytter komponenter til produktion eller foretager en fysisk lageroptælling.|[Internt forløb](design-details-internal-warehouse-flows.md)|

Konfigurere de lagerprocesser, der passer bedst til virksomheden. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Terminologi, der relaterer til lokationsstyring

### <a name="complexity-levels"></a>Kompleksitetsniveauer

Vi bruger termerne "grundlæggende" og "avanceret" til at skelne mellem niveauer af kompleksitet. Denne simple differentiering dækker flere forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning, hver understøttet af forskellige brugergrænsefladedokumenter. Det mest avancerede opbevarings niveau kaldes "styret læg-på-lager og pluk". Hvis du vil bruge styret læg-på-lager og pluk for en lokation, skal du aktivere funktionen **styret læg-på-lager og pluk** på **lokationskortet** .

### <a name="warehouse-flows"></a>Lagerflows

* Indgående flow - Varer, der flyttes til lagerlokationen, som køb og indgående overflytninger.
* Udgående flow - Plukke og levere varer til debitorer eller andre lokationer.
* Internt flow - Håndter varer på en lokation. Hvis du f. eks. flytter komponenter til produktion eller foretager en fysisk lageroptælling.

### <a name="basic-documents"></a>Grundlæggende dokumenter

Følgende dokumenter bruges i grundlæggende lagerflows.

* Læg-på-lager
* Pluk
* Flytning (lager)
* Varekladde
* Vareomposteringskladde

### <a name="advanced-documents"></a>Avancerede dokumenter

Følgende dokumenter bruges i avancerede lagerflows.

* Lagermodtagelse
* Læg-på-lager-kladde
* Læg-på-lager (logistik)
* Plukkladde
* Pluk (logistik)
* Bevægelseskladde
* Bevægelse (logistik)
* Internt lagerstedspluk
* Intern læg-på-lager
* Placeringsopr.kladde
* Opr.kladde til placeringsindh.
* Lagerkladde
* Lagervare - omposteringskladde

### <a name="pages-and-settings"></a>Sider og indstillinger

I dette afsnit beskrives begreberne bag nøglesiderne og indstillingerne for lager.

#### <a name="bins-and-bin-content"></a>Placeringer og placeringsindhold

En placering er en lagerenhed, der er beregnet til at indeholde adskilte dele. Det er den mindste containerenhed i [!INCLUDE[prod_short](includes/prod_short.md)]. Antal varer på placeringer kaldes *placeringsindhold*. Et opslag fra feltet **Vare** eller feltet **Placeringskode** i enhver lagerrelateret dokumentlinje viser den beregnede beholdning af varen på placeringen.  

Placeringsindhold kan gives egenskaben **Fast**, **Dedikeret** eller **Standard** for at definere, hvordan du kan bruge placeringsindholdet. Placeringer uden nogen af disse egenskaber kaldes *løse* placeringer.  

En fast placering indeholder varer, der er tildelt den pågældende placeringskode. Egenskaben fast placering sikrer, at placeringsindholdet ikke forsvinder, selvom placeringen er tømt. Du kan vælge placeringen igen, så snart indholdet genopfyldes.  

En dedikeret placering indeholder placeringsindhold, der kun kan plukkes til den dedikerede ressource, der bruger den pågældende placering. F.eks. en produktionsressource. Andet ikke-plukindhold som f.eks. antal udgående på en leverancebogføring kan stadig forbruges fra en dedikeret placering. Det er kun placeringsindhold, der tages i betragtning af algoritmen **Opret pluk**, der er beskyttet i en dedikeret placering.  

[!INCLUDE [prod_short](includes/prod_short.md)] bruger **Standard**-placeringsegenskab til at foreslå placeringer til lageraktiviteter. På lokationer, der bruger styret læg-på-lager og pluk, bruges egenskaben standardplacering ikke. På steder, hvor der kræves placeringer, bruges egenskaben i indgående flows til at angive, hvor varer skal placeres. Egenskaben bruges til at angive, hvor du kan tage varer fra, i udgående strømme.  

> [!NOTE]  
> Hvis udgående varer bliver anbragt på flere placeringer, tages varer først fra de placeringer, der ikke er standard, for at tømme placeringens indhold, og de resterende varer tages fra standardplaceringen.  

Der kan kun være en standardplacering pr. vare pr. lokation.  

#### <a name="bin-type"></a>Placeringstype

Lokationer, der bruger styret læg-på-lager og pluk, kan bruge placeringstyper. Placeringstyper styrer de aktiviteter, du tillader en placering. Der er følgende placeringsmuligheder:  

|Placeringstype|Beskrivlse|  
|------------------|---------------------------------------|  
|MODTAG|Varer, der modtages, men som ikke er lagt på lager.|  
|LEVER|Varer, der er plukket til lagerleverancelinjer, men som endnu ikke er bogført som leveret.|  
|LGT-PÅ-LGR|Typisk varer, der skal opbevares i store måleenheder, men som du ikke ønsker, der skal oprettes pluk af. Disse placeringer bruges ikke til pluk, enten til produktionsordrer eller forsendelser, så brugen af dem kan være begrænset. Denne type placering er nyttig, når du køber et stort antal varer. Placeringerne bør altid have et lavt placeringsniveau, så varer med LPLPLUK-placeringer med højere rangering først lægges på lager. Genbestiller regelmæssigt denne type placering, så deres varer er tilgængelige på LPLPLUK eller PLUK-type placeringer.|  
|PLUK|Elementer, der kun skal bruges til plukning. Genopfyldning af disse placeringer kan kun foretages ved flytning, ikke som læg-på-lager.|  
|LPLPLUK|Varer på placeringer, der foreslås for både læg-på-lager og pluk-funktioner. Placeringer af denne type har som regel forskellige placeringsniveau. Du kan fastsætte massevareplaceringer til denne placeringstype og give dem lave placeringsniveauer sammenlignet med de almindelige plukplaceringer eller forreste placeringer i plukområdet.|  
|KK|Denne placering bruges til lagerreguleringer, hvis du angiver placeringen i feltet **Reguleringsplaceringskode** på lokationskortet. Du kan også bruge denne type placeringer til defekte varer og varer, der skal kontrolleres. Du kan flytte varer til den type placering, hvis du ikke vil have, at de indgår i den normale varestrøm. **Bemærk:** I modsætning til alle andre placeringstyper har placeringstypen **KK** ingen af afkrydsningsfelterne til håndtering af varen markeret som standard. Dette angiver, at ethvert indhold, du placerer i en KK-placering er udelukket fra vareforløb.|  

Med undtagelserne af PLLUK-, LPLPLUK- og PUTAWAY typerne angiver placeringstypen den aktivitet, der er tilladt for en placering. For eksempel kan en placering af typen Modtag kun bruges til at modtage varer eller plukke varer fra.  

> [!NOTE]  
> Du skal bruge bevægelser for at flytte varer til MODTAG-og KK-placeringer. bruge bevægelser til at flytte varer fra LEVER- og KK-placeringer.  

#### <a name="bin-ranking"></a>Placeringsniveau

I avancerede lagerfunktioner kan du automatisere og optimere, hvordan varerne samles i læg-på-lager- og plukkladder ved at rangere placeringer, så varer foreslås taget eller anbragt i henhold til rangkriterier for at bruge lagerplads optimalt i avanceret logistik.

Læg-på-lager-processer er optimeret efter placeringsniveau ved at foreslå placeringer på højt niveau før placeringer på lavt niveau. På samme måde bliver plukprocesser optimeret ved først at foreslå varer fra placeringsindhold med højt placeringsniveau. Desuden foreslås placeringsgenbestillinger fra placeringer på lavt placeringsniveau til placeringer på højt placeringsniveau.  

Placeringsniveau og placeringsindhold er de grundlæggende egenskaber, der fører lagermedarbejderne på lagerstedet.  

#### <a name="bin-setup"></a>Opsætning af placering

I avanceret logistik kan du angive følgende kapacitets værdier for at styre, hvordan og hvor som helst-placeringer, varer:

* Antal
* Rummål
* Vægt  

Du kan tildele en basisenhed (UOM) til varer. En basisenhed kan være dele, paller, liter, gram eller kasser. Du kan også oprette større UOMs baseret på din basisenhed. Hvis stykenheder f. eks. er en basisenhed, kan en palle være lig med 16 styk.  

Hvis en vare har mere end én enhed, skal du angive maksimumantallet for hver enhed på varekortet. Hvis en vare er oprettet til at skulle håndteres i enheder og paller, skal feltet **Maks.antal** på siden **Placeringsindhold** for den pågældende vare også være i enheder og paller. Ellers beregnes det tilladte antal for placeringen ikke korrekt.  

Før du kan angive kapacitetsbegrænsninger for placeringsindhold på en placering, skal du først sikre dig, at varens måleenheder og dimensioner er blevet indstillet på varekortet.  

> [!NOTE]  
> Du kan kun bruge flere UOM'er på lokationer, der bruger styret læg-på-lager og pluk. I alle andre konfigurationer kan placeringsindhold kun være i basismåleenheden. I alle transaktioner med en måleenhed, der er højere end varens grundlæggende måleenhed, konverteres antallet til den grundlæggende enhed.  

#### <a name="zone"></a>Zone

Placeringer kan grupperes i zoner til at styre, hvordan arbejdsprocessen for lageraktiviteter ledes i avanceret logistik til lokationer.  

En zone kan være en modtagelseszone eller en lagerzone, og hver zone kan bestå af en eller flere placeringer.  

De fleste egenskaber, der er tildelt en zone, tildeles som standard den placering, der er oprettet fra denne zone.  

#### <a name="warehouse-class"></a>Lagerklasse

I avanceret logistik kan du tildele lagerklassekoder til følgende enheder: 

* Varer
* Placering
* Zoner

Lagerklasser styrer, hvor du kan lagre varer. Du kan opdele en zone i flere lagerklasser. Varer på modtagelseszonen kan f.eks. gemmes som frosne, farlige eller andre kategorier.

Når du arbejder med lagerklasser og en standardplacering for modtagelse/afsendelse, skal du manuelt udfylde de korrekte placeringer for modtagelses- og leverancelinjer for lagerstedet.  

Klassekoden fremhæves kun i indgående strømme på indgående linjer, hvor vareklassekoden ikke stemmer overens med standardmodtagelsesplacering. Hvis der ikke er tildelt korrekte standardplaceringer, kan antallet ikke modtages.  

#### <a name="location"></a>Lokation

En lokation er en fysisk struktur eller et sted, hvor lageret modtages, opbevares og leveres. En lokation kan være et lagersted, en service bil, en showroom, et anlæg eller et område på en fabrik. Lagerbeholdningen er ofte organiseret i placeringer og zoner.

#### <a name="first-expired-first-out"></a>Først udløbet først ude

Hvis du markerer afkrydsningsfeltet **Pluk i overensstemmelse med FEFO** i oversigtspanelet **Placeringsmetoder** på **lokationskortet**, bliver varesporede varer plukket i henhold til deres udløbsdato. Varer med den tidligste udløbsdato plukkes først.  

Lageraktiviteter i alle pluk- og bevægelsesdokumenter er sorteret i overensstemmelse med FEFO, medmindre de pågældende varer allerede har tildelte serienumre/lotnumre. Hvis det kun er en del af antallet på linjen, der er tildelt lot-/serienumre, bestemmes det resterende antal, der skal plukkes, vha. FEFO-metoden.  

Når der plukkes varer efter FEFO-metoden, samles de tilgængelige varer, der udløber først, på en midlertidig varesporingsliste, der er baseret på udløbsdatoen. Hvis der er to varer med samme udløbsdato, vælges varen med det laveste lot- eller serienummer. Hvis lot- eller serienumrene er ens, vælges den vare først, der blev registreret først. Standardkriterierne for udvælgelse af varer på plukplaceringer, f.eks. Placeringsniveau og Nedbrydning, anvendes på denne midlertidige FEFO-varesporingsliste.  

#### <a name="put-away-template"></a>Læg-på-lager-skabelon

Læg-på-lager-skabelonen angiver en række prioriterede regler, der skal overholdes ved oprettelse af læg-på-lager-aktiviteter. En læg-på-lager-skabelon kan f. eks. kræve, at du anbringer varer på en placering med placeringsindhold, der har samme ENHEDsindhold. Hvis der ikke findes en lignende placering med tilstrækkelig kapacitet, skal varen placeres på en tom placering. Læg-på-lager-skabelonen kan tildeles til en vare og en lokation.  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
