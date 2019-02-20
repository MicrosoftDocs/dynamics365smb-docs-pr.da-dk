---
title: Oprette kontaktvirksomheder | Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: da-dk
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Oprette kontaktvirksomheder
Dit firma har regelmæssigt møder med mulige firmakunder, hvilket som regel udvikler sig til forretningsforhold. Oplysninger om en ny kontaktperson skal registreres, så kommunikationen kan fortsættes.

Hvis du tilknytter flest mulige data om et bestemt firma, sikrer du, at kommunikationen bliver effektiv. Hvis du f.eks. tilknytter den relevante branche, sikrer du dig, at specifikke firmaer inkluderes i al relevant kommunikation.

Du kan også definere det forretningsforhold, du har til en kontaktperson. En kontaktperson kan f.eks. være et emne, en bank eller en kontrahent.

## <a name="creatinge-contact-companies"></a>Oprette kontaktvirksomheder
Du kan oprette en kontakt for hver ny virksomhed, du er i interaktion med, f.eks. kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.

Du kan oprette en kontakt på to måder: forfra eller fra en eksisterende debitor, kreditor eller bankkonto.

Kontroller eventuelt indstillingerne på siden **Marketingopsætning**, før du opretter en kontakt. Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Sådan oprettes en virksomhedskontakt fra bunden
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på Enter og vælge det næste tilgængelige nummer.  
4. Indstil **Type** til **Virksomhed**.
5. Udfyld de øvrige felter efter behov.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en virksomhedskontakt fra en debitor, kreditor eller bankkonto
Hvis du allerede har defineret en række debitorer, kreditorer eller bankkonti, kan du oprette kontakter på grundlag af de eksisterende kreditordata. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne med oplysningerne om debitor, kreditor eller bankkonto.

> [!NOTE]  
>   Før du kan oprette kontaktvirksomheder på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti på siden **Marketingopsætning**. Hvis du vil oprette kontakter fra en bankkonto, skal du også angive nummerserier for bankkonti på siden **Opsætning af Finans**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv en af følgende, afhængigt af hvor du vil oprette kontakter, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Opret kontakter fra kreditorer**
   * **Opret kontakter fra bankkonti**
2. I den kørselsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

    De næste numre i nummerserien er tildelt de nye kontakter. Den forretningsrelation for kreditorer, som er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
>   Du kan også oprette en debitor, kreditor eller bankkonto fra en kontakt. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisering af kontakter med debitorer, kreditorer og bankkonti
Hvis nogle af dine kontakter også er debitorer, kreditorer eller bankkonti, kan du synkronisere kontaktoplysningerne med den relaterede debitor, kreditor eller bankkonto. Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.  

Du skal angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti på siden **Marketingopsætning**, før du kan synkronisere kontakter med disse. Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Forskellige måder at synkronisere kontakter med debitorer, kreditorer og bankkonti
Du kan synkronisere kontakter med debitorer, kreditorer eller bankkonti på tre måder:

* knytte kontakter sammen med eksisterende debitorer, kreditorer eller bankkonti fra kontaktkortet. Du kan finde flere oplysninger under [Knytte kontakter til debitorer, kreditorer og bankkonti](marketing-how-link-contact.md).
* Opret debitorer, kreditorer eller bankkonti ud fra kontakten. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Oprette kontakter ud fra debitorer, kreditorer eller bankkonti. Du kan finde flere oplysninger under [Oprette en virksomhedskontakt ud fra en debitor, kreditor eller bankkonto](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Resultater af synkronisering
Hvis kontakten synkroniseres med debitoren, kreditoren, bankkontoen:

* Du behøver kun opdatere oplysninger ét sted. Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren eller bankkontoen.
* Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor- eller bankkontokort, oprettes der automatisk et kontaktkort for den pågældende debitor, kreditor eller bankkonto.
* Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.
* Du kan automatisk få registreret dine interaktioner, når du udfører handlinger, f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.
* Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor eller bankkonto, er det kun kontakten, som bliver slettet. Debitor, kreditor eller bankkonto slettes ikke.
* Hvis du sletter en debitor, kreditor eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.

> [!NOTE]  
>   Visse detaljer, som fakturerings og bogføringsoplysninger, vises ikke på kontaktkortet. Derfor kan du tilføje dem manuelt på debitorkortet, kreditorkortet eller bankkontokortet, når du opretter kontakter som debitorer, kreditorer eller bankkonti.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Sammenkædning af kontakter med debitorer, kreditorer og bankkonti
Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden. Når du knytter de to poster til hinanden, kan du synkronisere data, som er fælles, så det er de samme i begge steder.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto.
1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter **Debitor**, **Kreditor** eller **Bank**.
3. Vælg den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.

   I **Aktuelle overord. felter** kan du angive, hvilke felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen. Hvis sælgerkoden f.eks. ikke er ens for kontakten og debitoren, kan du ved at markere **Kontakt** bestemme, at det er oplysningerne for kontakten, som skal bruges.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Oprette en debitor, kreditor eller bankkonto fra en kontakt
   Du har mulighed for at registrere eksisterende kontakter som debitorer, kreditorer eller bankkonti. Når du opretter en debitor, kreditor eller bankkonto fra en kontakt, kan bruge du eksisterende data. Når du opretter en debitor, kreditor eller bankkonto på denne måde, synkroniseres den med kontakten. Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.

   Før du kan registrere kontakter på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti på siden **Marketingopsætning**. Hvis du vil registrere kontakter som bankkonti, skal du også angive nummerserier for bankkonti på siden **Opsætning af Finans**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt som debitor, kreditor eller bankkonto.
   1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
   2. Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.
   3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.
   4. Bekræft den efterfølgende meddelelse.

   Kontaktoplysningerne overføres fra kortet **Kontakt** til kortet **Bankkonto**, kortet **Debitor** eller kortet **Kreditor**. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger.

## <a name="setting-up-business-relations-on-contact-companies"></a>Opsætning af forretningsrelationer i kontaktvirksomheder
Du kan bruge forretningsrelationer til at angive det forretningsforhold, som findes mellem din virksomhed og dine kontakter, f.eks. et kundeemne, bank, konsulent, serviceleverandør osv.

Brug af forretningsrelationer i kontakter er en totrinsproces. Først skal du definere koden for forretningsrelationen. Du behøver kun at udføre dette trin én gang for hver forretningsrelation. Når du har en forretningsrelationskode, kan du begynde at tildele koden til kontaktvirksomheder.

> [!NOTE]  
>   Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.

### <a name="to-define-a-business-relation-code"></a>Sådan defineres en forretningsrelationskode
Forretningsrelationskoden definerer en kategori eller type af forretningsrelation, f.eks BANK eller Law. Du kan have flere forretningsrelationskoder. Du kan definere forretningsrelationen fra siden **Forretningsrelationer**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsrelationer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

### <a name="AssignBusRelContact"></a> Sådan tildeles forretningsrelationer til en kontakt
Du kan ikke tildele forretningsrelationer til en kontaktperson – kun til virksomheder.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Forretningsrelationer**.

    Siden **Kontakt til forretningsrelation** åbnes.
3. I feltet **Forretningsrelationskode** skal du vælge den forretningsrelation, du vil tildele.

Gentag disse trin for hver forretningsrelation, du vil tildele. Du kan også tildele forretningsrelationer fra kontaktoversigten ved at udføre samme procedure.

Det antal relationer, du har tildelt kontakten, vises i feltet **Antal forretningsrelationer** i sektionen **Segmentering** på siden **Kontakt**.

Når du har tildelt forretningsrelationer til kontakter, kan du bruge oplysningerne til at udvælge kontakter til dine målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Oprette kontaktpersoner](marketing-create-contact-persons.md)   
[Arbejde med Business Central](ui-work-product.md)

