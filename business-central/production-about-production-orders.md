---
title: Om produktionsordrer | Microsoft Docs
description: Produktionsordrer gør det muligt at styre produktionsprocessen, dvs. den proces, hvorved de indkøbte materialer forarbejdes til færdige varer. Produktionsordrer (sags- eller arbejdssedler) dirigerer arbejdet via ruter gennem forskellige faciliteter (arbejdscentre eller produktionsressourcer) på produktionsstedet, f.eks. en fabrik.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b02aa262089d5c341fb3b535f2af82c7085e99ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "937917"
---
# <a name="about-production-orders"></a>Om produktionsordrer
Produktionsordrer gør det muligt at styre produktionsprocessen, dvs. den proces, hvorved de indkøbte materialer forarbejdes til færdige varer. Produktionsordrer dirigerer arbejdet via ruter gennem forskellige arbejdscentre eller produktionsressourcer på produktionsstedet.  

Før du fortsætter med produktion udfører de fleste virksomheder forsyningsplanlægning, typisk én gang om ugen, for at beregne, hvor mange produktionsordrer og købsordrer, der skal udføres for at opfylde et salgsbehovet for den pågældende uge. Købsordrer leverer de komponenter, der kræves i henhold til produktionsstyklisten for at producere færdigvarerne.

Produktionsordrer udgør den centrale komponent i produktionsfunktionaliteten. De indeholder følgende oplysninger:  

-   Produkter, som skal produceres ifølge planen  
-   Materialer, der skal bruges til de planlagte produktionsordrer  
-   Produkter, der netop er produceret  
-   Materialer, der allerede er valgt  
-   Produkter, der blev produceret på et tidligere tidspunkt  
-   Materialer, der indgik i tidligere produktionsprocesser  

Produktionsordrer er udgangspunktet for:  

-   Planlægning af fremtidig produktion  
-   Overvågning af den igangværende produktion  
-   Sporing af afsluttet produktion  

## <a name="production-order-creation"></a>Oprette produktionsordrer  
Produktionsordrer kan oprettes manuelt på ordre til ordre-basis fra siden **Produktionsordre**, eller genereres fra siderne **Salgsordreplanlægning** eller **Ordreplanlægning**. Der oprettes flere ordrer fra siden **Planlægningskladde**.  

Produktionsordrer oprettes med udgangspunkt i oplysninger fra:  

- Varer  
- Produktionsstyklister
- Ruter  
- Produktionsressourcer  
- Arbejdscentre  

## <a name="limitations-on-production-order-creation"></a>Begrænsninger ved oprettelse af produktionsordrer  
Produktionsordrer reserveres automatisk og spores til kilden, når:  

-   De oprettes i **Planlægningskladde**  
-   De oprettes med ordrefunktionen på sien **Salgsordreplanlægning**  
-   De oprettes på siden **Ordreplanlægning**  
-   Funktionen **Omplanlæg** bruges på produktionsordrer  

Du kan finde flere oplysninger i [Spore relationer mellem behov og forsyning](production-how-track-demand-supply.md).

Produktionsordrer, der oprettes på anden måde, reserveres og spores ikke automatisk.   

## <a name="production-order-status"></a>Produktionsordrestatus  
Produktionsordrestatus kontrollerer produktionsordrens vej gennem processen. Produktionens form og indhold dikteres af ordrens status. Produktionsordrer vises i forskellige sider i henhold til deres status. Du kan ikke ændre en produktionsordres status manuelt, men kun bruge funktionen **Skift status**.  

### <a name="simulated-production-order"></a>Simuleret produktionsordre  
En simuleret produktionsordre kendetegnes ved følgende:  

- Som navnet angiver, er der tale om en simulering, og den bruges først og fremmest ved udarbejdelse af tilbud og beregning af omkostninger. En simuleret produktionsordre fungerer som et eksempel på en produktionsordre.  
- Den påvirker ikke ordreplanlægningen. Planlægning (hovedplanlægning og MRP) tager hverken højde for simulerede produktionsordrer eller påvirkes af dem. En simuleret produktionsordre kan heller ikke bruges som skabelon, fordi den forsvinder, når du ændrer dens status.  

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
- En fastlagt produktionsordre fungerer som pladsholder i planlægningen for en fremtidig sag, der frigives til produktion.  
- En fastlagt produktionsordre kan oprettes i forbindelse med planlægningen, oprettes manuelt eller oprettes på basis af salgsordrer. Den slettes ikke i forbindelse med den efterfølgende planlægning.  
- Når en fastlagt produktionsordre oprettes som et led i planlægningen, udløser den en foreslået "planlagt ordrefrigivelse", der omfatter: antal, frigivelsesdato og forfaldsdato. Planlægningssystemet er baseret på genbestillingssystemet, genbestillingsmetoder og ordremodifikatorer, som det møder i forbindelse med planlægningen af nettobehov.  
- Du kan se, hvordan de påvirker planlægningen, ved at se nærmere på belastningen for hvert enkelt arbejdscenter eller produktionsressource på den fastlagte produktionsordres rute.  

### <a name="released-production-order"></a>Frigivet produktionsordre  
En frigivet produktionsordre kendetegnes ved følgende:  

- Du kan oprette en frigivet produktionsordre automatisk på basis af en salgsordre.  
- Når en produktionsordre er frigivet, betyder det ikke nødvendigvis, at materialerne er plukket, eller at sagen fysisk er flyttet til den første operation.  
- I virksomheder, der fremstiller til ordre, er det ikke usædvanligt, at der oprettes en frigivet produktionsordre umiddelbart efter, at salgsordren er registreret.  
- Faktisk materialeforbrug og produktafgang kan registreres manuelt vha. en frigivet produktionsordre. Desuden sker der kun automatisk træk af forbrug og produktafgang for frigivne produktionsordrer.  

### <a name="finished-production-order"></a>Færdig produktionsordre  
En færdig produktionsordre kendetegnes ved følgende:  

- En færdig produktionsordre er typisk en, hvor produkterne er færdige.  
- Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres. Når produktionsordren afsluttes, kan omkostningsberegningen reguleres og afstemmes.  
- Færdige produktionsordrer bruges til rapportering af statistiske oplysninger og er med til at gøre det muligt at spore oplysninger tilbage til andre ordrer (f.eks. salgs-, produktions- og købsordrer). Muligheden for at følge et spor tilbage til en færdig produktionsordre betyder, at du kan gennemgå detaljerede historikoplysninger.  
- Færdige produktionsordre kan aldrig ændres.  

## <a name="production-order-execution"></a>Udføre produktionsordrer  
Når en produktionsordre er oprettet og planlagt, skal den frigives til produktion, så den kan udføres. Under udførelsen af ordren kan du registrere:  

- Plukkede eller forbrugte materialer  
- Hvor meget tid, der er brugt på det arbejde, der er angivet i ordren  
- Hvor mange enheder, der er fremstillet af den samlede eller overordnede vare  

Disse oplysninger kan registreres manuelt eller via automatisk rapportering, i overensstemmelse med varer i feltet Trækmetode.  

### <a name="material-consumption"></a>Materialeforbrug  
Programmet omfatter en række indstillinger, som gør det muligt at angive, hvordan materialeforbrug skal registreres i en produktionsvirksomhed. Materialeforbruget kan f.eks. registreres manuelt, hvilket kan være nyttigt, hvis flere forskellige komponenter bruges på skift, eller hvis flere dele end forventet går til spilde.  

Forbruget af materialer kan behandles vha. forbrugskladden, men kan også registreres automatisk i programmet, hvilket kaldes automatisk rapportering. Der er følgende rapporteringsmetoder:  

-   Manuelt  
-   Fremad  
-   Baglæns  

Manuel forbrugsrapportering anvender forbrugskladden til at angive materialeplukning.  

Forlæns forbrugsrapportering antager, at det forventede antal af alle materialer til hele ordren er forbrugt, når produktionsordren frigives, medmindre der bruges rutebindingskoder. Hvis der bruges rutebindingskoder, registreres de materialer, der forbruges ved starten af et operationstrin, i afgangskladden. Hvis hele produktionsordren skal trække forlæns, skal du gøre to ting:  

- Der skal være valgt forlæns træk på varekortene for alle de varer, der indgår i produktionsstyklisten på det øverste niveau.  
- Alle rutebindingskoder på produktionsstyklisten skal fjernes.  

Baglæns forbrugsrapportering registrerer det faktiske antal materialer, der enten er plukket eller forbrugt, når en produktionsordres status ændres til *Færdig*, medmindre der bruges rutebindingskoder. Hvis der bruges rutebindingskoder, forbruges materialet, efter at et antal af den samlede eller overordnede vare registreres for operationstrinnet i afgangskladden.  

Når produktionsordren fornys, kopieres trækmetoden fra varekortet. Eftersom trækmetoden for hver enkelt komponent på produktionsordren bestemmer, hvordan og hvor forbruget registreres, er det vigtigt at være opmærksom på, at du kan ændre trækmetoden for enkelte varer direkte i produktionsordren.  

#### <a name="automatic-consumption-posting-flushing"></a>Automatisk bogføring af forbrug (træk)  
Fordelen ved automatisk træk er, at det i vidt omfang reducerer behovet for dataregistrering. Når det er muligt at trække en operation automatisk, kan hele processen til registrering af forbrug og afgang automatiseres. Ulempen ved at bruge automatisk træk er, at du muligvis ikke kan registrere spild, eller måske ikke engang er opmærksom på spild. Der findes følgende metoder til automatisk rapportering:  

- Forlæns træk af hele ordren  
- Forlæns træk for én operation ad gangen  
- Baglæns træk for én operation ad gangen  
- Baglæns træk af hele ordren  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisk rapportering – forlæns træk af hele ordren  
Hvis du bruger forlæns træk til produktionsordren ved sagens start, opfører programmet sig stort set på samme måde som ved manuelt forbrug. Den væsentligste forskel er, at forbruget sker automatisk.  

- Alt indhold på produktionsstyklisten forbruges og trækkes fra lagerbeholdningen på det tidspunkt, hvor den frigivne produktionsordre fornys.  
- Forbrugsantallet er det antal pr. samling, der er angivet på produktionsstyklisten, ganget med det antal samlede eller overordnede varer, der skal produceres.  
- Det er ikke nødvendigt at registrere oplysninger i forbrugskladden, hvis alle varerne skal trækkes.  
- Når der forbruges varer fra lagerbeholdningen, spiller det ingen rolle, hvornår oplysningerne registreres i afgangskladden, fordi afgangskladden ikke har nogen indflydelse på denne form for forbrugsbogføring.  
- Der kan ikke angives rutebindingskoder.  

Forlæns træk af en hel ordre er velegnet i produktionsmiljøer med:  

-   Få defekter  
-   Få operationer  
-   Højt komponentforbrug i tidligere operationer  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisk rapportering – forlæns træk for én operation ad gangen  
Hvis du vælger træk for én operation ad gangen, kan du fratrække lagervarer, mens en bestemt operation udføres på den samlede vares rute. Materialet er knyttet til ruten vha. rutebindingskoder, som svarer til de rutebindingskoder, der bruges til komponenter i produktionsstyklisten.  

Trækket finder sted, når den operation, der har den samme rutebindingskode, starter. At den starter betyder, at der registreres en aktivitet i afgangskladden for den pågældende operation. Aktiviteten behøver ikke være andet end, at der angives en opstillingstid.  

Trækmængden er det antal pr. samling, der er angivet i produktionsstyklisten ganget med det antal samlede varer, der skal produceres (forventet antal).  

Denne teknik egner sig bedst til forhold, hvor der er mange operationer, og hvor visse komponenter først skal bruges sent i samlingsforløbet. I en produktionsmiljø med JIT-produktion (Just-in-Time) er det ikke engang sikkert, at varerne er på lager, når den frigivne produktionsordre sættes i gang.  

Materialet kan forbruges under operationerne vha. rutebindingskoder. Nogle komponenter skal måske først bruges på de sidste produktionsstadier og skal derfor ikke trækkes fra lageret før det tidspunkt, hvor de skal bruges i operationerne.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisk rapportering – baglæns træk for én operation ad gangen  
Hvis du bruger baglæns træk for én operation ad gangen, registreres forbruget, efter at operationen er bogført i afgangskladden.  

Fordelen ved denne metode er, at antallet af færdige samlede varer i denne operation er kendt.  

Materialet i produktionsstyklisten knyttes sammen med ruteposterne vha. rutebindingskoder. Det baglæns træk sker, når en operation med en bestemt rutebindingskode bogføres med et færdigt antal.  

Trækmængden er det antal pr. samling, der er angivet i produktionsstyklisten, ganget med det antal samlede varer, der er bogført som afgangsantal på den pågældende operation. Det kan være anderledes end det forventede antal.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisk rapportering – baglæns træk af hele ordren  
I denne rapporteringsmetode tages der ikke højde for rutebindingskoder.  

Der plukkes ingen komponenter, før den frigivne ordres status ændres til *Færdig*. Trækmængden er det antal pr. samling, der er angivet på produktionsstyklisten, ganget med det antal samlede varer, der er færdige og overført til lageret.  

Baglæns træk af hele produktionsordren forudsætter samme opsætning som til fremadtræk: Rapporteringsmetoden skal være angivet til baglæns på hvert enkelt varekort for alle varer inden for den overordnede stykliste, der skal rapporteres. Desuden skal alle rutebindingskoder fjernes fra produktionsstyklisten.  

### <a name="production-output"></a>Produktionsafgang  
Programmet giver dig mulighed for at spore, hvor meget tid der er medgået til arbejdet på en produktionsordre, ud over registreringen af det producerede antal. Disse oplysninger gør det lettere at bestemme produktionsomkostningerne mere nøjagtigt. Produktionsvirksomheder, der bruger et standardsystem til kostprisberegning, vil måske også gerne registrere faktiske oplysninger, som kan gøre det nemmere at forbedre standarderne.  

Afgang kan behandles via afgangskladden, men kan også registreres automatisk af programmet. Programmet kopierer trækmetoden fra produktionsressourcens eller arbejdscentrets kort til produktionsordreruten, når det opdaterer. Som med materialeforbrug er der tre måder at rapportere afgang på:  

- Manuelt  
- Forlæns  
- Baglæns  

Manuel metode anvender afgangskladden, som angiver tidsforbrug og produceret antal.  

Forlænsmetoden registrerer den forventede afgang (og tid), som registreres automatisk ved frigivelsen af en produktionsordre. Rutebindingskoder er ikke en faktor, der indgår i det forlæns træk af afgangen.  

Baglænsmetoden registrerer den forventede afgang (og tid), som registreres automatisk ved færdiggørelsen af en produktionsordre. Rutebindingskoder er ikke en faktor, der indgår i det baglæns træk af afgangen.  

### <a name="posting-consumption-and-output"></a>Bogføre forbrug og afgang  
Du kan bruge en hvilken som helst kombination af automatisk træk og manuelt registrerede oplysninger til både forbrug og afgang. Du kan f.eks. trække komponenter automatisk, men stadig registrere spild i forbrugskladden. På samme måde kan du registrere afgang automatisk, men registrere spild for den samlede vare eller ekstra tid, der er brugt på ordren, i afgangskladden.  

Hvis du registrerer forbrug og afgang manuelt, er du nødt til at vælge en rækkefølge at registrere disse oplysninger i. Du kan registrere forbrug først og bruge en genvejsmetode, når du skal registrere de oplysninger, der er baseret på forventet afgangsantal. Eller du kan angive afgang først ved at bruge funktionen **Udfold rute**. Derefter kan du registrere forbruget på basis af det faktiske afgangsantal.  

### <a name="production-journal"></a>Produktionskladde  
Produktionskladden er en kombination af funktionerne i forbrugskladden og afgangskladden. Du kan åbne produktionskladden direkte fra den frigivne produktionsordre.  

Formålet med produktionskladden er at give dig mulighed for at registrere forbrug og afgang fra en produktionsordre ét sted.  

Produktionskladden er overskuelig, og du kan nemt:  

- Registrere afgang og forbrug for en produktionsordre  
- Knytte komponenterne til operationer  
- Knytte faktiske operationsdata til anslåede standardværdier på produktionsordrens rute- og komponentlinjer  
- Bogføre og udskrive en oversigt over de operationsdata, der er registreret for produktionsordren  

I produktionskladden kan du udføre mange af de samme funktioner som i forbrugs- og afgangskladderne. Dimensioner, varesporing og placeringsindhold håndteres på samme måde som i forbrugs- og afgangskladderne.  

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
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
