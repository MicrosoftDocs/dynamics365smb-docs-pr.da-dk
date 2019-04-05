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
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aaeb98aa5e3c48a92be71546be33b1494a751cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792086"
---
# <a name="creating-contacts"></a>Oprettelse af kontakter
Dit firma har regelmæssigt møder med mulige firmakunder, hvilket som regel udvikler sig til forretningsforhold. Oplysninger om en ny kontaktperson skal registreres, så kommunikationen kan fortsættes.

Når du tilknytter flest mulige data om et bestemt firma, sikrer du, at kommunikationen bliver effektiv. Hvis du f.eks. tilknytter den relevante branche, sikrer du dig, at specifikke firmaer inkluderes i al relevant kommunikation. Du kan også definere det forretningsforhold, du har til en kontaktperson. En kontaktperson kan f.eks. være et emne, en bank eller en kontrahent.

> [!NOTE]
> I feltet **Type** på siden **Kontaktkort** kan du oprette en kontakt som en person eller en virksomhed, typisk afhængigt af om du kender navnet på kontaktpersonen på tidspunktet for oprettelsen. Funktionaliteten er den samme for begge typer med undtagelse af nogle af typer yderligere oplysninger, der kan tildeles. Du kan ændre værdien i feltet senere, eller du kan bruge felterne i oversigtspanelet **Overførte oplysninger** på siden **Marketingopsætning** til at styre, hvilke data der skal deles mellem en person og den relaterede virksomhed.

Du kan oprette en kontakt for hver ny person eller virksomhed, du er i interaktion med, f.eks. en kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.

Der er to måder at oprette en kontakt på:
 * Manuelt.
 * Ud fra en eksisterende kunde, leverandør eller bankkonto.

## <a name="to-create-a-contact-manually"></a>Sådan oprettes en kontakt manuelt
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på Enter for at indsætte det næste tilgængelige nummer.  
5. Udfyld de resterende felter efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto.
Hvis du har debitorer, kreditorer og bankkonti, som du vil oprette kontaktkort for, kan du bruge **Opret kontakter fra**-kørsler til at oprette kontakter på grundlag af de eksisterende data. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor eller bankkonto. Du kan finde flere oplysninger under [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette kontakter baseret på eksisterende data, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Du kan finde flere oplysninger under [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv en af følgende, afhængigt af hvad du vil oprette kontakter ud fra, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Opret kontakter fra kreditorer**
   * **Opret kontakter fra bankkonti**
2. På den anmodningsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

De næste numre i nummerserien er tildelt de nye kontakter. De forretningsrelationer, som er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
> Du kan også gøre dette modsat, nemlig ved at oprette en debitor, kreditor eller bankkonto ud fra en kontaktperson. Du kan finde flere oplysninger under [Sådan oprettes en kontakt som debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

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

* Når du knytte kontakter sammen med eksisterende debitorer, kreditorer eller bankkonti fra kontaktkortet. Se [Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* Når du opretter debitorer, kreditorer eller bankkonti på grundlag af kontakter. Se [Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du opretter kontakter som debitorer, kreditorer eller bankkonti. Se [Sådan oprettes en kontakt som debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto.
Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden, så fælles data synkroniseres.

1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter handlingen **Debitor**, **Kreditor** eller **Bank**.
3. På den side, der åbnes, skal du vælge den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.
4. I feltet **Aktuelle overord. felter** skal du angive, hvis felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen. Hvis f.eks. sælgerkoden er forskellig på kontaktkortet og kundekortet, kan du vælge at beholde den på kontaktkortet ved at vælge **Kontakt**.
5. Vælg knappen **OK**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt som debitor, kreditor eller bankkonto.
Hvis du har en debitor, kreditor eller bankkonto for et firma, som du vil oprette en kontakt til, kan du bruge funktionen **Opret som**. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor eller bankkonto. Du kan finde flere oplysninger under [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette debitorer, kreditorer eller bankkonti baseret på kontakter, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Du kan finde flere oplysninger under [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.
4. Vælg knappen **OK**.

Kontaktoplysningerne overføres fra kortet kontaktkortet til det nye debitor-, kreditor- eller bankkontokort. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger. Du kan f.eks. finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Arbejde med Business Central](ui-work-product.md)
