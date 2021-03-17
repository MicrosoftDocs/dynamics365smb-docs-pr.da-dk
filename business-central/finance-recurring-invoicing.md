---
title: Arbejde med tilbagevendende indtægt | Microsoft-dokumenter
description: Få mere at vide om de tilgængelige muligheder for at automatisere afsendelse af abonnementsfakturaer til kunder og registrering af tilbagevendende indtægter.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: recurring, invoicing, subscription, billing
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: andreipa
ms.openlocfilehash: 657c473301b52011c1f1cbe2767f3c0ceaeb4725
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379998"
---
# <a name="work-with-recurring-revenue-in-prod_short"></a>Arbejde med tilbagevendende indtægt i [!INCLUDE[prod_short](includes/prod_short.md)]

Mange virksomheder skifter fra en forretningsindtægtsmodel, hvor indtægten kommer fra en kundes engangskøb, til en abonnementsmodel, hvor indtægten sker på en tilbagevendende basis, så der er uafbrudt adgang til levering af en vare eller en service.
[!INCLUDE[prod_short](includes/prod_short.md)] giver følgende muligheder for at automatisere, hvordan du afsender abonnementsfakturaer til kunder og registrerer tilbagevendende indtægter. 

## <a name="register-revenue-with-a-recurring-general-journal"></a>Registrere indtægt via en finansgentagelseskladde

En gentagelseskladde er en finanskladde med specifikke felter til styring af transaktioner, som bogføres ofte med få eller ingen ændringer, f.eks. leje, abonnementer, elektricitet eller varmeforbrug. Med disse felter til gentagelsestransaktioner kan du bogføre både faste og variable beløb. Med gentagelseskladder skal poster, der bogføres regelmæssigt, kun indtastes én gang. Det vil sige, at de konti, dimensioner og dimensionsværdier osv., som angives, bevares i kladden efter bogføringen. Hvis du vil foretage ændringer, kan du gøre det ved hver bogføring.

### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Med denne mulighed kan du angive fleksible faktureringsperioder med [datoformler](ui-enter-date-ranges.md#using-date-formulas).

Men hvis du vælger denne mulighed, kan du ikke udskrive og sende fakturaer i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)].  

Du kan finde flere oplysninger under [Arbejde med gentagelseskladder](ui-work-general-journals.md#working-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Oprette flere fakturaer på basis af en sagsgentagelseskladde

Sagsgentagelseskladden er et mere avanceret alternativ til finanskladden. Du kan definere varer, ressourcer og finanskonti, der skal gentages for hver opgave, og du angiver hyppigheden af gentagelser.  

Når du har bogført en sagsgentagelseskladde, kan du oprette flere fakturaer med opgaven **Opret salgsfaktura for sag**. Du kan gennemse og bogføre oprettede fakturaer på siden **Salgsfakturaer**.

### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Hvis du vælger denne mulighed, følger du standardproceduren for fakturering med alle de fordele, der er forbundet med dette, herunder standard- og kundelayout til kommunikationspræferencer. Du kan også definere priser for hver enkelt sag.

Du skal imidlertid oprette en ny sag og føje linjer til gentagelseskladden. 

Du kan finde flere oplysninger under [Oprette sagskladdelinjer](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) og [Oprette flere salgsfakturaer for sager](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Oprette flere fakturaer baseret på tilbagevendende salgslinjer

Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette tilbagevendende salgslinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer. Brug kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med tilbagevendende salgslinjer, som er tildelt kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i de tilbagevendende salgslinjer.  

### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Med denne indstilling kan du tildele samme gentagelseslinjer til flere kunder. Du kan definere gyldighedsperioden for tilbagevendende salgslinjer for en specifik kunde. Du kan tildele flere gentagelseslinjer for den samme kunde, og alle disse vil blive medtaget i fakturaen.

Det er imidlertid ikke muligt at angive faste priser for varer, da [!INCLUDE[prod_short](includes/prod_short.md)] bruger faktiske priser og rabatter, der er gældende på bilagsdatoen, og forsøger derefter at finde den bedste kombination, der giver den laveste pris.  

Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a>Tilbagevendende fakturaer med servicekontrakt

En servicekontrakt indeholder servicekontraktaftaler mellem kunderne og virksomheden. En servicekontrakt omfatter aftaler og de serviceartikler, som du yder service på som del af kontrakten.  

Du kan definere startdatoen for kontrakten, faktureringsperioden, uanset om kontrakten er forudbetalt, prisreguleringsspecifikationer, hvis du har planer om at ændre priserne, mens kontrakten er aktiv. Du kan bruge både serviceartikler eller varer i servicekontraktlinjer.
Du kan oprette kontraktskabeloner for at definere, hvordan bestemte kontrakttyper skal oprettes.  

### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Med denne mulighed kan du bruge en del af den avancerede servicestyringsfunktion, som ikke er begrænset til at udstede tilbagevendende fakturaer, men som understøtter reparations- og servicehandlinger.

Denne indstilling kræver imidlertid en Premium-licens. Konfiguration af servicestyring og vedligeholdelse af den vil muligvis ikke give enorme fordele ved enklere abonnementsscenarier.  

Du kan finde flere oplysninger under [Arbejde med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md) og [Fakturere flere servicekontrakter](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a>Relaterede funktioner
Der er flere relaterede funktioner i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a>Rammesalgsordrer

En rammesalgsordre udgør rammen for en langsigtet aftale mellem dit firma og en kunde.
Der indgås ofte en rammeaftale, hvor en kunde har forpligtet sig til at købe et stort antal varer, der skal leveres i flere mindre portioner i løbet af en bestemt periode. En rammeordre omfatter ofte kun en enkelt vare med leveringsdatoer, der er fastsat på forhånd. Den væsentligste årsag til at bruge en rammeordre i stedet for en salgsordre er, at de antal, der angives i en rammeordre, ikke påvirker varedisponeringen, men kan bruges til planlægningsformål.

#### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Med denne mulighed kan du bruge den forventede efterspørgsel, så oplysningerne tages i betragtning i de normale planlægningsrutiner. Du kan finde flere oplysninger under [Behovsprognoser og rammeordrer](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Standardversionen giver dog ikke mulighed for som standard at behandle flere rammeordrer ad gangen.

Du kan finde flere oplysninger under [Arbejde med rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a>Tilbagevendende ordrer (Norge)

Du kan bruge tilbagevendende ordrer til at oprette rammeordreskabeloner, så salgsordrer kan oprettes på basis af de datointervaller, du definerer. Hvis du f.eks. leverer den samme salgsordre hver anden uge, kan du bruge en rammesalgsordre til at oprette tilbagevendende ordrer.
Du kan bruge tilbagevendende grupper til at definere en række parametre, der viser, hvordan du opretter ordrerne. Disse grupper tildeles rammeordrer, der skal oprettes regelmæssigt. Hvis du vil oprette tilbagevendende ordrer, skal du regelmæssigt køre processen Opret tilbagevendende ordrer. 

#### <a name="why-use-this-option"></a>Hvorfor bruge denne mulighed

Med denne mulighed kan du vælge mellem faste og "bedste" priser.

Dette er dog kun tilgængeligt i Norge. Gyldighedsperioden kan defineres på tilbagevendende grupperingsniveau.

Du kan finde flere oplysninger i [Gentagelse af ordrer](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Tilbagevendende indtægt og abonnementsfakturering fra andre udbydere

På [AppSource.microsoft.com](https://appsource.microsoft.com/) kan du få udvidelser til Business Central. Nogle udvidelser er fra Microsoft, mens andre udvidelser leveres af andre virksomheder. Oversigten over udvidelserne fra andre firmaer vokser hver måned. Så hold øje med [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646), og få apps, der kan hjælpe dig med at arbejde i Business Central.  

## <a name="see-also"></a>Se også

[Datoformler](ui-enter-date-ranges.md#using-date-formulas)  
[Arbejde med gentagelseskladder](ui-work-general-journals.md#working-with-recurring-journals)  
[Oprette sagskladdelinjer](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Oprette flere salgsfakturaer for sager](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)  
[Arbejde med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Fakturere flere servicekontrakter](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Behovsprognoser og rammeordrer](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Arbejde med rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md)  
[Tilbagevendende ordrer (Norge)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]