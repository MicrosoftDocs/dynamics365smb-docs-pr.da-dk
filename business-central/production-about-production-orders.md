---
title: Om produktionsordrer
description: 'Flere oplysninger om produktionsordrer gør det muligt at styre produktionsprocessen, dvs. den proces, hvorved de indkøbte materialer forarbejdes til færdige varer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-production-orders"></a>Om produktionsordrer

Produktionsordrer gør det muligt at styre produktionsprocessen, dvs. den proces, hvorved de indkøbte materialer forarbejdes til færdige varer. Produktionsordrer dirigerer arbejdet via ruter gennem forskellige arbejdscentre eller produktionsressourcer på produktionsstedet.  

Før de fortsætter med produktion, udfører de fleste virksomheder forsyningsplanlægning, typisk én gang om ugen, for at beregne, hvor mange produktionsordrer og købsordrer, der skal udføres for at opfylde et salgsbehovet for den pågældende uge. Købsordrer leverer de komponenter, der kræves i henhold til produktionsstyklisten for at producere færdigvarerne.

Produktionsordrer udgør den centrale komponent i produktionsfunktionaliteten. De indeholder følgende oplysninger:  

- Produkter, som skal produceres ifølge planen  
- Materialer, der skal bruges til de planlagte produktionsordrer  
- Produkter, der er produceret  
- Materialer, der allerede er valgt  
- Produkter, der blev produceret på et tidligere tidspunkt  
- Materialer, der indgik i tidligere produktionsprocesser  

Produktionsordrer er udgangspunktet for:  

- Planlægning af fremtidig produktion  
- Overvågning af den igangværende produktion  
- Sporing af afsluttet produktion  

## <a name="production-order-creation"></a>Oprette produktionsordrer

Du kan manuelt oprette produktionsordrer på ordre til ordre-basis på siden **Produktionsordre** eller generere dem fra siderne **Salgsordreplanlægning** eller **Ordreplanlægning**. Du kan også oprette flere ordrer fra siden **Planlægningskladde**.  

Du kan oprette produktionsordrer med udgangspunkt i oplysninger fra:  

- Varer  
- Produktionsstyklister
- Ruter  
- Produktionsressourcer  
- Arbejdscentre  

## <a name="limitations-on-creating-production-orders"></a>Begrænsninger ved oprettelse af produktionsordrer

Produktionsordrer reserveres automatisk og spores til kilden, når:  

- De oprettes i [Planlægningskladde](production-how-to-run-mps-and-mrp.md)  
- Oprettet på siden [Salgsordreplanlægning](production-how-to-create-production-orders-from-sales-orders.md)  
- De oprettes på siden [Ordreplanlægning](production-how-to-plan-for-new-demand.md)  
- Funktionen [Omplanlæg](production-how-to-replan-refresh-production-orders.md) bruges på produktionsordrer  

Du kan finde flere oplysninger i [Spore relationer mellem behov og forsyning](production-how-track-demand-supply.md).

Produktionsordrer, der oprettes på anden måde, reserveres og spores ikke automatisk.

## <a name="production-order-status"></a>Produktionsordrestatus

Produktionsordrestatus kontrollerer produktionsordrens vej gennem programmet. Produktionens form og indhold dikteres af ordrens status. Produktionsordrer vises i forskellige sider i henhold til deres status. Du kan ikke ændre status på en produktionsordre manuelt. Du skal bruge funktionen **Skift status** i den enkelte produktionsordre eller på siden **Skift prod. ordrestatus**.  

### <a name="simulated-production-order"></a>Simuleret produktionsordre

En simuleret produktionsordre kendetegnes ved følgende:  

- Som navnet antyder, er det en simulering, du kan bruge til tilbud og omkostninger. Det kan f.eks. være, hvis forsknings- og udviklingsafdelingen vil have et overslag over omkostningerne ved en foreslået vare. En simuleret produktionsordre fungerer som et eksempel på en produktionsordre.  
- De påvirker ikke ordreplanlægningen. Planlægning (MPS og MRP) tager ikke højde for og påvirkes ikke af simulerede produktionsordrer. En simuleret produktionsordre kan heller ikke bruges som skabelon, fordi den forsvinder, når du ændrer dens status.  

### <a name="planned-production-order"></a>Planlagt produktionsordre

En planlagt produktionsordre kendetegnes ved følgende:  

- Du kan oprette en planlagt produktionsordre automatisk på basis af en salgsordre.  
- Planlagte produktionsordrer fungerer på samme måde som frigivne produktionsordrer og leverer oplysninger til kapacitetsplanlægningen ved at vise det samlede kapacitetsbehov for hvert arbejdscenter eller for hver produktionsressource.  
- En planlagt produktionsordre udgør det bedst mulige estimat over den fremtidige belastning på arbejdscentret eller produktionsressourcen baseret på de oplysninger, der er til rådighed. De oprettes typisk med udgangspunkt i planlægningen, men kan også oprettes manuelt. Det er dog ikke så hensigtsmæssigt at oprette dem manuelt, fordi de slettes i forbindelse med efterfølgende planlægning.  
- Når en planlagt produktionsordre oprettes som et led i planlægningen, udløser den et forslag til en "planlagt ordrefrigivelse", der omfatter antal, frigivelsesdato og forfaldsdato. Planlægningssystemet er baseret på genbestillingssystemet, genbestillingsmetoder og ordremodifikatorer, som det møder i forbindelse med planlægningen af nettobehov.  
- Du kan se, hvordan de påvirker planlægningen, ved at se nærmere på belastningen for hvert enkelt arbejdscenter eller produktionsressource i den planlagte produktionsordres rute.  

### <a name="firm-planned-production-order"></a>Fastlagt produktionsordre

En fastlagt produktionsordre kendetegnes ved følgende:  

- Du kan oprette en fastlagt produktionsordre automatisk på basis af en salgsordre.  
- En fastlagt produktionsordre fungerer som pladsholder i planlægningen for et fremtidig projekt, der frigives til produktion.  
- En fastlagt produktionsordre kan oprettes i forbindelse med planlægningen, oprettes manuelt eller oprettes på basis af salgsordrer. Den slettes ikke i forbindelse med den efterfølgende planlægning.  
- Når en fastlagt produktionsordre oprettes som et led i planlægningen, udløser den en foreslået "planlagt ordrefrigivelse", der omfatter: antal, frigivelsesdato og forfaldsdato. Planlægningssystemet er baseret på genbestillingssystemet, genbestillingsmetoder og ordremodifikatorer, som det møder i forbindelse med planlægningen af nettobehov.  
- Du kan se, hvordan de påvirker planlægningen, ved at se nærmere på belastningen for hvert enkelt arbejdscenter eller produktionsressource på den fastlagte produktionsordres rute.  

### <a name="released-production-order"></a>Frigivet produktionsordre

En frigivet produktionsordre kendetegnes ved følgende:  

- Du kan oprette en frigivet produktionsordre automatisk på basis af en salgsordre.  
- Når en produktionsordre er frigivet, betyder det ikke nødvendigvis, at materialerne er plukket, eller at projektet fysisk er flyttet til den første operation.  
- I virksomheder, der fremstiller til ordre, er det ikke usædvanligt, at der oprettes en frigivet produktionsordre umiddelbart efter, at salgsordren er registreret.  
- Faktisk materialeforbrug og produktafgang kan registreres manuelt vha. en frigivet produktionsordre. Desuden sker der kun automatisk træk af forbrug og produktafgang for frigivne produktionsordrer.  

### <a name="finished-production-order"></a>Færdig produktionsordre

En færdig produktionsordre kendetegnes ved følgende:  

- En færdig produktionsordre er typisk en, hvor produkterne er færdige.  
- Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres. Når du afslutter en produktionsordre, kan du regulere og afstemme omkostninger.  
- Færdige produktionsordrer bruges til rapportering af statistiske oplysninger og er med til at gøre det muligt at spore oplysninger tilbage til andre ordrer (f.eks. salgs-, produktions- og købsordrer). Muligheden for at følge et spor tilbage til en færdig produktionsordre betyder, at du kan gennemgå detaljerede historikoplysninger.  
- Færdige produktionsordre kan aldrig ændres.  

## <a name="production-order-execution"></a>Udføre produktionsordrer

Når du har oprettet og planlagt en produktionsordre, skal den frigives til produktion, så den kan udføres. Under udførelsen af ordren kan du registrere:  

- De materialer, der blev plukket eller forbrugt  
- Hvor meget tid, der er brugt på det arbejde, der er angivet i ordren  
- Hvor mange enheder, der er fremstillet af den samlede eller overordnede vare  

Du kan registrere disse oplysninger manuelt eller vha. automatisk rapportering. Metoden afhænger af opsætningen i feltet Trækmetode for varen og arbejdscentret.  

### <a name="material-consumption"></a>Materialeforbrug

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder forskellige muligheder for, hvordan materialeforbrug registreres. Materialeforbruget kan f.eks. registreres manuelt, hvilket kan være nyttigt, hvis flere forskellige komponenter bruges på skift, eller hvis flere dele end forventet går til spilde.  

Forbruget af materialer kan behandles vha. [forbrugskladden](production-how-to-post-consumption.md), men kan også registreres automatisk i programmet af [!INCLUDE [prod_short](includes/prod_short.md)], hvilket kaldes automatisk rapportering (træk). Du kan vælge rapporteringsmetoderne Manuel, Forlæns og Baglæns.

Manuel forbrugsrapportering anvender forbrugskladden til at angive materialeplukning.  

Forlæns forbrugsrapportering antager, at det forventede antal af alle materialer til hele ordren er forbrugt, når produktionsordren frigives, medmindre der bruges rutebindingskoder. Hvis du bruger rutebindingskoder, registreres de materialer, der forbruges ved starten af et operationstrin, i afgangskladden. Hvis hele produktionsordren skal trække forlæns, skal du gøre to ting:  

- Der skal være valgt forlæns træk på varekortene for alle de varer, der indgår i produktionsstyklisten på det øverste niveau.  
- Alle rutebindingskoder på produktionsstyklisten skal fjernes.  

Baglæns forbrugsrapportering registrerer det faktiske antal materialer, der enten er plukket eller forbrugt, når en produktionsordres status ændres til *Færdig*, medmindre der bruges rutebindingskoder. Hvis du bruger rutebindingskoder, forbruges materialet, efter at et antal af den samlede eller overordnede vare registreres for operationstrinnet i afgangskladden.  

Når produktionsordren fornys, kopieres trækmetoden fra varekortet. Eftersom trækmetoden for hver enkelt komponent på produktionsordren bestemmer, hvordan og hvor forbruget registreres, er det vigtigt at være opmærksom på, at du kan ændre trækmetoden for enkelte varer direkte i produktionsordren. Du kan finde flere oplysninger i [Udtrække komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).

### <a name="production-output"></a>Produktionsafgang

[!INCLUDE [prod_short](includes/prod_short.md)] giver dig mulighed for at spore, hvor meget tid der er gået med at arbejde på en produktionsordre, ud over registreringen af det producerede antal. Disse oplysninger gør det lettere at bestemme produktionsomkostningerne mere nøjagtigt. Produktionsvirksomheder, der bruger et standardsystem til kostprisberegning, vil måske også gerne registrere faktiske oplysninger, som kan gøre det nemmere at forbedre standarderne.  

Afgang kan behandles via [afgangskladden](production-how-to-post-output-quantity.md), men kan også registreres automatisk. [!INCLUDE [prod_short](includes/prod_short.md)] kopierer trækmetoden fra produktionsressourcens eller arbejdscentrets kort til produktionsordreruten, når det opdaterer. Som med materialeforbrug er der tre måder at rapportere afgang på: Manuel, Forlæns og Baglæns.

Den manuelle metode anvender afgangskladden, som angiver tidsforbrug og produceret antal.  

Forlænsmetoden registrerer den forventede afgang (og tid), som registreres automatisk ved frigivelsen af en produktionsordre. Rutebindingskoder er ikke en faktor, der indgår i det forlæns træk af afgangen.  

Baglænsmetoden registrerer den forventede afgang (og tid), som registreres automatisk ved færdiggørelsen af en produktionsordre. Rutebindingskoder er ikke en faktor, der indgår i det baglæns træk af afgangen.  

### <a name="posting-consumption-and-output"></a>Bogføre forbrug og afgang

Du kan bruge en hvilken som helst kombination af automatisk træk og manuelt registrerede oplysninger til både forbrug og afgang. Du kan f.eks. trække komponenter automatisk, men stadig registrere spild i forbrugskladden. På samme måde kan du registrere afgang automatisk, men registrere spild for den samlede vare eller ekstra tid, der er brugt på ordren, i afgangskladden.  

Hvis du registrerer forbrug og afgang manuelt, er du nødt til at vælge en rækkefølge at registrere disse oplysninger i. Du kan registrere forbrug først og bruge en genvejsmetode, når du skal registrere de oplysninger, der er baseret på forventet afgangsantal. Eller du kan angive afgang først ved at bruge funktionen **Udfold rute**. Derefter kan du registrere forbruget på basis af det faktiske afgangsantal.  

### <a name="production-journal"></a>Produktionskladde

[Produktionskladden](production-how-to-register-consumption-and-output.md) er en kombination af funktionerne i forbrugskladden og afgangskladden. Du kan åbne produktionskladden direkte fra den frigivne produktionsordre.  

Formålet med produktionskladden er at give dig mulighed for at registrere forbrug og afgang fra en produktionsordre ét sted.  

Produktionskladder er overskuelige, og du kan nemt:  

- Registrere afgang og forbrug for en produktionsordre  
- Knytte komponenterne til operationer  
- Knytte faktiske operationsdata til anslåede standardværdier på en produktionsordres rute- og komponentlinjer  
- Bogføre og udskrive en oversigt over de operationsdata, der er registreret for en produktionsordre  

I produktionskladden kan du udføre mange af de samme funktioner som i forbrugs- og afgangskladderne. Dimensioner, varesporing og placeringsindhold håndteres på samme måde.  

Men produktionskladden adskiller sig dog fra forbrugs- og afgangskladderne på følgende måder:  

- Den kaldes direkte fra en frigivet produktionsordrelinje med alle relevante data indsat.  
- Den giver dig mulighed for at angive, hvilke komponenttyper der skal kunne behandles med udgangspunkt i et trækmetodefilter på kladden.  
- Antal og tider, der allerede er bogført for ordren, vises nederst i kladden som faktiske angivelser.  
- Felter, som ikke er relevante, er tomme og kan ikke redigeres.  
- Du kan selv bestemme, hvordan afgangsantal skal indsættes automatisk i kladden &#8211 den sidste operation skal f.eks. have nul som afgangsantal.  
- Hvis du kommer til at afslutte kladden uden at bogføre ændringerne, vises en anmodningsmeddelelse, der giver dig mulighed for ikke at afslutte kladden alligevel.  
- Operationer og komponenter vises sammen i en logisk struktur, der giver et bedre overblik over produktionsprocessen.  

I produktionskladden bogføres forbrugsantal som negative vareposter, mens afgangsantal bogføres som positive vareposter, og tidsforbruget bogføres som kapacitetsposter.  

## <a name="see-also"></a>Se også

[Produktion](production-manage-manufacturing.md)
[Konfigurere produktion](production-configure-production-processes.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
