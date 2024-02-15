---
title: Oprette forretningskontakter
description: 'Beskriver de opgaver, der er behov for til at oprette kontakter og definere forretningsrelationer på kontaktkortet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-contacts"></a>Oprette kontakter

Når du udvikler en forretningsrelation med en person i et andet firma, kan du tilføje dem som en kontakt i [!INCLUDE[prod_short](includes/prod_short.md)]. Tilføj derefter alle oplysninger om dem eller deres firma, som kunne være nyttige i fremtidige meddelelser. På siden **Kontaktkort** kan du oprette følgende typer kontakter:

* **Person** - Brug dette er typisk, når du har haft direkte kontakt med en person og har deres kontaktoplysninger.
* **Virksomhed** - Brug dette til en kontakt, der ikke er en enkelt person, men en enhed, f.eks. en kontrahent eller bank.

De oplysninger, der er relevante for hver kontakttype, er forskellige, så de tilgængelige felter og handlinger er forskellige. Du kan f.eks. kun tildele ansvarsområder til en person og branche til en virksomhed.

Du kan også ændre værdien i feltet **Type**. Du kan også bruge felterne i oversigtspanelet **Arv** på siden **Marketingopsætning** til at angive de oplysninger, der skal deles mellem en person og deres virksomhed. Flere oplysninger i [Konfigurere kontakter](marketing-setup-contacts.md).

Når en kontakt konverteres til en debitor, bliver kontakten eller kontaktvirksomheden f.eks. navnet på debitoren. Kontaktens post bevares, og du kan knytte kontaktpersonen og kunden til hinanden, så deres data synkroniseres fremadrettet.

> [!NOTE]
> Hvis du skifter til [funktionsopdateringen til konverteringsskabeloner](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), kan du også oprette kreditorer eller medarbejdere fra forretningskontakter.
>
> Hvis du allerede bruger den indbyggede funktionalitet til automatisk at oprette debitorer eller varer, understøtter denne funktion imidlertid ikke brugerdefinerede felter, og nyoprettede kunder eller varer medtager ikke sådanne oplysninger.

## <a name="to-create-a-contact-manually"></a>Sådan oprettes en kontakt manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

   Hvis du har defineret en nummerserie for kontakter på siden **Marketingopsætning**, kan du i stedet trykke på <kbd>Enter</kbd> for at indsætte det næste tilgængelige nummer.
4. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt fra en debitor, kreditor eller bankkonto.

Hvis du har eksisterende debitorer, kreditorer og bankkonti, som du vil oprette kontaktkort for, kan du bruge **Opret kontakter fra** batch jobs. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne senere med oplysningerne om relateret debitor, kreditor eller bankkonto. Flere oplysninger i [Synkronisering af kontakter med debitorer, kreditorer, medarbejdere og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Før du kan oprette kontakter baseret på eksisterende data, skal du angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti i oversigtspanelet **Interaktioner** på siden **Marketingopsætning**. Flere oplysninger [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv et af følgende, der matcher den enhed, du vil oprette kontakter fra, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Opret kontakter fra kreditorer**
   * **Opret kontakter fra bankkonti**
2. På den anmodningsside, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at oprette kontakterne.

De næste numre i nummerserien er tildelt de nye kontakter. Den forretningsrelationskode, der er angivet på siden **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
> Du kan også gøre dette modsat, nemlig ved at oprette en debitor, kreditor, medarbejder eller bankkonto ud fra en kontaktperson. Flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Sådan oprettes en debitor, kreditor, ansat eller bankkonto på grundlag af en kontakt

Hvis du har en debitor, kreditor, medarbejder eller bankkonto for en virksomhed, du vil oprette en kontakt for, kan du bruge handlingen **Opret som**. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne senere med oplysningerne om relateret debitor, kreditor, medarbejder eller bankkonto. Flere oplysninger i [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Før du kan oprette kunder, debitorer, ansatte eller bankkonti fra kontakter, skal du angive en forretningsrelationskode på siden **Marketingopsætning** på oversigtspanelet **Interaktioner**. Flere oplysninger i [Konfigurere kontakter](marketing-setup-contacts.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor, ansat eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor**, **Bank** eller **Medarbejder**.
4. Vælg **OK**.

Kontaktoplysningerne overføres fra kortet kontaktkortet til det nye debitor-, kreditor-, ansat- eller bankkontokort. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger. Se f.eks. i [Registrere nye debitorer](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Sådan sammenkædes en kontakt til en eksisterende debitor, kreditor, ansat eller bankkonto.

Hvis du har en kontakt og enten en debitor, kreditor, ansat eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden for at synkronisere data.

1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter handlingen **Debitor**, **Kreditor**, **Bank** eller **Medarbejder**.
3. På den side, der åbnes, skal du vælge den debitor, kreditor, ansat eller bankkonto, der skal oprettes en tilknytning til.
4. I feltet **Aktuelle overord. felter** skal du angive de felter, der skal have prioritet, hvis der er uoverensstemmende oplysninger i felter, som er fælles for både den eksisterende kontakt og debitor-, kreditor, medarbejder eller bankkontoen. Så hvis f.eks. sælgerkoden er forskellig på kontaktkortet og kundekortet, kan du vælge at beholde den på kontaktkortet ved at vælge **Kontakt**.
5. Vælg **OK**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Sådan fjernes et link mellem en kontakt og en eksisterende debitor, kreditor, ansat eller bankkonto.

Hvis du har forbundet kontakten med en uønsket debitor, kreditor, medarbejder eller bankkonto, skal du fjerne forbindelsen mellem objekterne, så dataene ikke længere synkroniseres.

1. Åbn den kontaktperson, der har det forkerte link.  
2. Vælg handlingen **forretningsrelationer**.  
3. På den side, der åbnes, skal du vælge den debitor, kreditor, ansat eller bankkonto, der skal fjernes et link fra.  
4. Vælg handlingen **Slet**.  

> [!NOTE]  
> Du kan ikke bruge vinduet **Forretningsrelationer** til at ændre eksisterende relationer. I stedet skal du fjerne relationen og bruge **Link til den eksisterende**. Flere oplysninger i [Sådan knyttes en kontakt til en eksisterende debitor, kreditor, medarbejder eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synkronisering af kontakter med debitorer, kreditorer, medarbejdere og bankkonti

Hvis nogle af dine kontakter også er debitorer, kreditorer, medarbejdere eller bankkonti, kan du synkronisere dem med data fra kontakten og få følgende fordele:

* Du behøver kun opdatere oplysninger ét sted. Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren, medarbejderen eller bankkontoen.
* Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor-, ansat- eller bankkontokort, oprettes der automatisk et kontaktkort.
* Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.
* Du kan registrere dine interaktioner, når du udfører handlinger som f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.
* Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor, ansatte eller bankkonto, er det kun kontakten, som bliver slettet. Debitor, kreditor, ansatte eller bankkonto slettes ikke.
* Ligeledes hvis du sletter en debitor, kreditor, medarbejder eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.

> [!NOTE]  
> Visse detaljer, som fakturerings og bogføringsoplysninger, er ikke tilgængelige for kontakter. Når du opretter kontakter som debitorer, kreditorer, medarbejdere eller bankkonti, kan det være en god idé at tilføje disse oplysninger manuelt.

Der kan aktiveres datasynkronisering mellem kontakter og relaterede debitorer, kreditorer, ansatte eller bankkonti på tre måder:

* Når du opretter kontakter på grundlag af debitorer, kreditorer eller bankkonti. Flere oplysninger i [Sådan oprettes en kontrakt fra en debitor, kreditor, medarbejder eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du opretter debitorer, kreditorer, ansatte eller bankkonti fra kontakter. Flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Når du knytter kontakter sammen med eksisterende debitorer, kreditorer, medarbejdere eller bankkonti fra kontaktkortet. Flere oplysninger i [Sådan knyttes en kontakt til en eksisterende debitor, kreditor, medarbejder eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Sådan får du vist, hvilken debitor, kreditor, ansat eller bankkonto en kontaktperson vedrører

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontakter**, og vælg derefter det relaterede link.
2. Marker linjen for en kontakt, vælg handlingen **Relaterede oplysninger**, og vælg derefter handlingen **Debitor/Kreditor/Bankkonto/Medarbejder**.

## <a name="see-also"></a>Se også

[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Bruge online kort til at finde steder og vejledninger](across-online-maps.md)  
[Arbejde med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
