---
title: Oprette forretningskontakter
description: Beskriver de opgaver, der er involveret i oprettelse af kontakter og definition af forretningsrelationer på kontaktkortet.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 07/08/2021
ms.author: edupont
ms.openlocfilehash: 31fa33a1842a7e825872b13f6f7a2fb65c517ffa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140887"
---
# <a name="create-contacts"></a>Oprette kontakter

Når du udvikler en forretningsrelation til en person i et andet firma, kan du tilføje dem som en kontakt i [!INCLUDE[prod_short](includes/prod_short.md)]. Tilføj derefter alle oplysninger om dem eller deres firma, som kan være nyttige i forbindelse med fremtidige meddelelser. På siden **Kontaktkort** kan du oprette følgende typer kontakter:

* **Person** - dette er typisk, når du har haft direkte kontakt med en person og har deres kontaktoplysninger.
* **Virksomhed** - Hvis kontakten ikke er en enkelt person, men en enhed, f.eks. en kontrahent eller bank. 

De oplysninger, der er relevante for hver kontakttype, er forskellige, så de tilgængelige felter og handlinger er forskellige. Du kan f.eks. kun tildele ansvarsområder til en person og branche til en virksomhed. 

Du kan også ændre værdien i feltet **Type**. Du kan også bruge felterne i oversigtspanelet **Arv** på siden **Marketingopsætning** til at angive de oplysninger, der skal deles mellem en person og deres virksomhed. Du kan finde flere oplysninger i [Konfigurere kontakter](marketing-setup-contacts.md).

Når en kontakt konverteres til en debitor, bliver kontakten eller kontaktvirksomheden f.eks. navnet på debitoren. Kontaktens post bevares, og du kan knytte kontaktpersonen og kunden til hinanden, så deres data synkroniseres frem.

> [!NOTE]
> Hvis du skifter til [funktionsopdateringen til konverteringsskabeloner](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), kan du også oprette kreditorer eller medarbejdere fra forretningskontakter.
>
> Hvis du allerede bruger den indbyggede funktionalitet til automatisk oprettelse af debitorer eller varer, understøtter denne funktion imidlertid ikke brugerdefinerede felter, og nyoprettede kunder eller varer medtager ikke sådanne oplysninger.

## <a name="to-create-a-contact-manually"></a>Sådan oprettes en kontakt manuelt
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på **Enter** for at indsætte det næste tilgængelige nummer.  
5. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto.
Hvis du har debitorer, kreditorer og bankkonti, som du vil oprette kontaktkort for, kan du bruge **Opret kontakter fra**-kørsler til at oprette kontakter på grundlag af de eksisterende data. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor eller bankkonto. Du kan finde flere oplysninger i [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette kontakter baseret på eksisterende data, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Der er flere oplysninger i [Opsætning af kontakter](marketing-setup-contacts.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv et af følgende, afhængigt af hvorfra du vil oprette kontaktpersoner, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Opret kontakter fra kreditorer**
   * **Opret kontakter fra bankkonti**
2. På den anmodningsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

De næste numre i nummerserien er tildelt de nye kontakter. De forretningsrelationer, som er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
> Du kan også gøre dette modsat, nemlig ved at oprette en debitor, kreditor eller bankkonto ud fra en kontaktperson. Du kan finde flere oplysninger i [Sådan oprettes en kontakt som debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Sådan oprettes en debitor, kreditor, ansat eller bankkonto på grundlag af en kontakt
Hvis du har en debitor, kreditor, ansat eller bankkonto for en virksomhed, du vil oprette en kontakt for, kan du bruge handlingen **Opret som**. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne bagefter med oplysningerne om relateret debitor, kreditor, ansat eller bankkonto. Du kan finde flere oplysninger i [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette kunder, debitorer, ansatte eller bankkonti fra kontakter, skal du angive en forretningsrelationskode på siden **Marketingopsætning** på oversigtspanelet **Interaktioner**. Du kan finde flere oplysninger i [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor, ansat eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor**, **Bank** eller **Ansat**.
4. Vælg knappen **OK**.

Kontaktoplysningerne overføres fra kortet kontaktkortet til det nye debitor-, kreditor-, ansat- eller bankkontokort. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger. Du kan f.eks. finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor, ansat eller bankkonto.
Hvis du har en kontakt og enten en debitor, kreditor, ansat eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden for at synkronisere data.

1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter handlingen **Debitor**, **Kreditor**, **Bank** eller **Ansat**.
3. På den side, der åbnes, skal du vælge den debitor, kreditor, ansat eller bankkonto, der skal oprettes en tilknytning til.
4. I feltet **Aktuelle overord. felter** skal du angive, hvis felter der skal have prioritet, når der er uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitor-, kreditor-, ansat- eller bankkontoen. Hvis f.eks. sælgerkoden er forskellig på kontaktkortet og kundekortet, kan du vælge at beholde den på kontaktkortet ved at vælge **Kontakt**.
5. Vælg knappen **OK**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Sådan fjernes et link mellem en kontakt og en eksisterende debitor, kreditor, ansat eller bankkonto.

Hvis du har kædet kontakten sammen med en debitor, kreditor, medarbejder eller bankkonto, skal du fjerne kæden mellem objekterne, så dataene ikke længere synkroniseres.

1. Åbn den kontaktperson, der har det forkerte link.  
2. Vælg handlingen **forretningsrelationer**.  
3. På den side, der åbnes, skal du vælge den debitor, kreditor, ansat eller bankkonto, der skal fjernes et link fra.  
4. Vælg handlingen **Slet**.  

> [!NOTE]  
> Du kan ikke bruge vinduet **Forretningsrelationer** til at ændre eksisterende relationer. I stedet skal du fjerne relationen og bruge **Link til den eksisterende**. Du kan finde flere oplysninger i [Sådan knyttes en kontakt til en eksisterende debitor-, kreditor-eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synkronisering af kontakter med debitorer, kreditorer, ansatte og bankkonti
Hvis nogle af dine kontakter også er debitorer, kreditorer, ansatte eller bankkonti, kan du synkronisere kontaktoplysningerne med data fra kontakten og få følgende fordele:

* Du behøver kun opdatere oplysninger ét sted. Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren, den ansatte eller bankkontoen.
* Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor-, ansat- eller bankkontokort, oprettes der automatisk et kontaktkort.
* Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.
* Du kan registrere dine interaktioner, når du udfører handlinger som f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.
* Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor, ansatte eller bankkonto, er det kun kontakten, som bliver slettet. Debitor, kreditor, ansatte eller bankkonto slettes ikke.
* Hvis du sletter en debitor, kreditor, ansat eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.

> [!NOTE]  
> Visse detaljer, som fakturerings og bogføringsoplysninger, er ikke tilgængelige for kontakter. Når du opretter kontakter som debitorer, kreditorer, ansatte, medarbejdere eller bankkonti, kan det være en god idé at tilføje dem manuelt.

Der kan aktiveres datasynkronisering mellem kontakter og relaterede debitorer, kreditorer, ansatte eller bankkonti på tre måder:

* Når du opretter kontakter på grundlag af debitorer, kreditorer, ansatte eller bankkonti. Se [Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du opretter debitorer, kreditorer, ansatte eller bankkonti fra kontakter. Se [Sådan oprettes en debitor, kreditor eller bankkonto på grundlag af en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Når du knytter kontakter sammen med eksisterende debitorer, kreditorer, ansatte eller bankkonti fra kontaktkortet. Se [Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Sådan får du vist, hvilken debitor, kreditor, ansat eller bankkonto en kontaktperson vedrører
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Marker linjen for en kontakt, vælg handlingen **Relaterede oplysninger**, og vælg derefter handlingen **Debitor/Kreditor/Bankkto,Ansat**.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Arbejde med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]