---
title: Oprette kontaktvirksomheder | Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: 5ec6a7580cd4211b33d276f5523bfcf34b91ad59
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985834"
---
# <a name="create-contacts"></a>Oprette kontakter
Du møder regelmæssigt personer fra andre virksomheder, hvilket kan udvikle sig til forretningsforhold, f.eks. en kunderelation. Når en sådan ny kontakt opstår, skal der registreres flest mulige oplysninger på et kontaktkort, så kommunikationen kan fortsættes.

Du kan oprette en kontakt som typen **Virksomhed**, f. eks. hvis relationen ikke er en enkelt person, men en enhed, f. eks. en kontrahent eller bank. Du kan også oprette en kontakt som typen **Person**. Funktionen er mere eller mindre den samme for begge typer, og begge kan ændres, efterhånden som relationen udvikles.

Når et kontaktkort konverteres til et debitorkort, bliver kontakten eller kontaktvirksomheden f. eks. navnet på debitoren. Kontaktkortet slettes ikke, og data på de to kort synkroniseres fremad, efterhånden som du kæder dem sammen.

## <a name="person-or-company"></a>Person eller virksomhed
Du kan beslutte, om du vil oprette en kontakt som en person eller en virksomhed. Det afhænger typisk af, om du kender navnet på kontaktpersonen på tidspunktet for oprettelsen. Det gør du, når du udfylder feltet **Type** på siden **Kontaktkort**. Du kan også have kontaktkort for både en virksomhed og en eller flere personer, der arbejder i virksomheden. Det sker automatisk, når du udfylder feltet **Virksomhedsnavn** på et kontaktkort af typen **Person**.

Funktionaliteten er den samme for begge typer, bortset fra at valgmulighederne for yderligere oplysninger ændres afhængigt af typen. Du kan f.eks. kun tildele ansvarsområder til en person og branche til en virksomhed. Dette er angivet i brugergrænsefladen, hvor felter og handlinger, der ikke anvendes, er gråmarkeret. Du kan ændre værdien i feltet **Type** senere, eller du kan bruge felterne i oversigtspanelet **Overførte oplysninger** på siden **Marketingopsætning** til at styre, hvilke data der skal deles mellem en person og personens relaterede virksomhed. Du kan finde flere oplysninger under [Konfigurere kontakter](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Sådan oprettes en kontakt manuelt
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på Enter for at indsætte det næste tilgængelige nummer.  
5. Udfyld de resterende felter efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto.
Hvis du har debitorer, kreditorer og bankkonti, som du vil oprette kontaktkort for, kan du bruge **Opret kontakter fra**-kørsler til at oprette kontakter på grundlag af de eksisterende data. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor eller bankkonto. Du kan finde flere oplysninger under [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette kontakter baseret på eksisterende data, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Der er flere oplysninger i [Opsætning af kontakter](marketing-setup-contacts.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv en af følgende, afhængigt af hvad du vil oprette kontakter ud fra, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Opret kontakter fra kreditorer**
   * **Opret kontakter fra bankkonti**
2. På den anmodningsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

De næste numre i nummerserien er tildelt de nye kontakter. De forretningsrelationer, som er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
> Du kan også gøre dette modsat, nemlig ved at oprette en debitor, kreditor eller bankkonto ud fra en kontaktperson. Du kan finde flere oplysninger under [Sådan oprettes en kontakt som debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Sådan oprettes en debitor, kreditor eller bankkonto på grundlag af en kontakt
Hvis du har en debitor, kreditor eller bankkonto for en virksomhed, du vil oprette en kontakt for, kan du bruge funktionen **Opret som**. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor eller bankkonto. Du kan finde flere oplysninger under [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette debitorer, kreditorer eller bankkonti baseret på kontakter, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Du kan finde flere oplysninger under [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.
4. Vælg knappen **OK**.

Kontaktoplysningerne overføres fra kortet kontaktkortet til det nye debitor-, kreditor- eller bankkontokort. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger. Du kan f.eks. finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto.
Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden, så fælles data synkroniseres.

1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter handlingen **Debitor**, **Kreditor** eller **Bank**.
3. På den side, der åbnes, skal du vælge den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.
4. I feltet **Aktuelle overord. felter** skal du angive, hvis felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen. Hvis f.eks. sælgerkoden er forskellig på kontaktkortet og kundekortet, kan du vælge at beholde den på kontaktkortet ved at vælge **Kontakt**.
5. Vælg knappen **OK**.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisering af kontakter med debitorer, kreditorer og bankkonti
Hvis nogle af dine kontakter også er debitorer, kreditorer eller bankkonti, kan du synkronisere kontaktoplysningerne med den relaterede debitor, kreditor eller bankkonto.

Der er følgende fordele, når en kontakt synkroniseres med en debitor, kreditor eller bankkonto.

* Du behøver kun opdatere oplysninger ét sted. Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren eller bankkontoen.
* Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor- eller bankkontokort, oprettes der automatisk et kontaktkort for den pågældende debitor, kreditor eller bankkonto.
* Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.
* Du kan automatisk få registreret dine interaktioner, når du udfører handlinger, f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.
* Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor eller bankkonto, er det kun kontakten, som bliver slettet. Debitor, kreditor eller bankkonto slettes ikke.
* Hvis du sletter en debitor, kreditor eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.

> [!NOTE]  
> Visse detaljer, som fakturerings og bogføringsoplysninger, vises ikke på kontaktkortet. Derfor kan du tilføje dem manuelt på debitorkortet, kreditorkortet eller bankkontokortet, når du opretter kontakter som debitorer, kreditorer eller bankkonti.

Synkronisering af fælles data mellem kontakter og relaterede debitorer, kreditorer eller bankkonti kan aktiveres på tre måder:

* Når du opretter kontakter på grundlag af debitorer, kreditorer eller bankkonti. Se [Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du opretter debitorer, kreditorer eller bankkonti på grundlag af kontakter. Se [Sådan oprettes en debitor, kreditor eller bankkonto på grundlag af en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Når du knytte kontakter sammen med eksisterende debitorer, kreditorer eller bankkonti fra kontaktkortet. Se [Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Sådan får du vist, hvilken debitor, kreditor eller bankkonto en kontaktperson vedrører
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Marker linjen for en kontakt, vælg handlingen **Relaterede oplysninger**, og vælg derefter handlingen **Debitor/Kreditor/Bankkto**.

Siden for det relaterede kort åbnes.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Arbejde med Business Central](ui-work-product.md)
