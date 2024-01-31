---
title: XML-skemaer til at forberede dataudvekslingsdefinitioner
description: 'Brug XML-skemaer til at angive data udvekslings strukturen for at definere, hvilke dataelementer du vil udveksle med.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner

Hvis du vil aktivere import/eksport af data i XML-filer via dataudvekslingsstrukturen i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge XML-skemaer til at definere, hvilke dataelementer du vil udveksle med [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan udføre dette arbejde på siden **XML-skemafremviser** ved at indlæse XML-skemafilen, vælge de relevante dataelementer og derefter initialisere en dataudvekslingsdefinition.  

 Når du har defineret, hvilke dataelementer der skal medtages, baseret på XML-skemaet, kan du bruge **Generer dataudvekslingsdefinition** som handling til at initialisere en dataudvekslingsdefinition, der er baseret på de valgte dataelementer, som du derefter udfører i dataudvekslingsstrukturen. Herved oprettes der en post på siden **Bogføringsudvekslingsdefinitioner**, hvor du kan fortsætte ved at definere, hvilke elementer i filen, der knyttes til hvilke felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

 Dette emne indeholder følgende procedurer:  

- Sådan indlæses en XML-skemafil  

- Sådan markeres eller fjernes markeringen af noder i et XML-skema  

- Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema  

## Sådan indlæses en XML-skemafil

1. Sørg for, at den pågældende XML-skemafil er tilgængelig. Filtypenavnet er .xsd.  

2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **XML-skemaer**, og vælg derefter det relaterede link.  

3. Vælg handlingen **Ny**.  

4. Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angiv en kode, der identificerer XML-skemaet.|  
    |**Beskrivelse**|Angiv en beskrivelse af XML-skemaet.|  

     Feltet **Målnavneområde** angiver navneområdet i den XML-skemafil, der er indlæst for linjen.  

5. Vælg handlingen **Indlæs skema**, og vælg derefter XML-skemafilen.  

     Når filen er indlæst, udfyldes resten af felterne på linjen med oplysninger fra filen, og afkrydsningsfeltet **Skema er indlæst** markeres.  

    > [!NOTE]  
    >  Som standard er træet for det indlæste indlæste XML-skema skjult. Udvid hver node ved at klikke på knappen **+** på noden. For at udvide alle noder skal du vælge **Udvid alle** på båndet.  

### Sådan markeres eller fjernes markeringen af noder i et XML-skema  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **XML-skemaviser**, og vælg derefter det relaterede link.  

2. Udfyld felterne i sidehovedet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode til XML-skema**|Angiv den XML-skemafil, du har indlæst i trin 5 i afsnittet "Sådan indlæses en XML-skemafil".|  
    |**Nyt XMLport-nr.**|Angiv nummeret på den XMLport, der er oprettet fra dette XML-skema, når du vælger handlingen **Generér XMLport**.|  

     Linjerne er nu udfyldt med noder, der repræsenterer alle elementer i XML-skemaet. Noder for elementer, der er obligatoriske i henhold til XML-skemaet, er som standard valgt.  

3. På den første linje i kolonnen **Nodenavn** skal du udvide noden **Dokument** og derefter gradvist udvide underliggende noder, du vil gennemgå.  

     Alternativt kan du højreklikke på en node og derefter vælge **Udvid alle**.  

4. Vælg en af følgende handlinger for at ændre, hvilke noder der vises.  

    |**Handling**|Beskrivelse|  
    |----------------|---------------------------------------|  
    |**Vis alle**|Alle noder vises.|  
    |**Skjul ikke-obligatoriske**|Der vises kun de noder, der repræsenterer elementer, der kræves i henhold til XML-skemaet. Disse noder er typisk angivet med **1** i feltet **MinOccurs**.<br /><br /> Vælg **Vis alle** for at tilbageføre visningen.|  
    |**Skjul ikke-valgte**|Kun noder, hvor afkrydsningsfeltet **Markeret** er markeret, vises.<br /><br /> Vælg **Vis alle** for at tilbageføre visningen.|  

5. Vælg handlingen **Rediger**.  

6. I afkrydsningsfeltet **Markeret** skal du angive for hver enkelt node, om elementet skal understøttes i dataudvekslingsdefinitionen for den relaterede SEPA-bankfil.  

    > [!NOTE]  
    >  Når du vælger en obligatorisk underordnet node, markeres alle overordnede noder ovenfor også.  

7. Vælg handlingen **Marker alle obligatoriske elementer** for at markere alle noder, der repræsenterer elementer, der er obligatoriske i henhold til XML-skemaet.  

8. Vælg handlingen **Afmarker alt** for at rydde alle markeringer.  

     Feltet **Valg** angiver, om noden har to eller flere sidestillede noder, der fungerer som valgmuligheder.  

### Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **XML-skemaer**, og vælg derefter det relaterede link.  

2. Vælg det relevante XML-skema, og vælg derefter handlingen **Åbn XML-skemafremviser**.  

3. Sørg for, at de relevante noder er valgt. Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".  

4. På siden **XML-skemafremviser** skal du vælge handlingen **Generer dataudvekslingsdefinition**.  

 Der oprettes en dataudvekslingsdefinition på siden **Bogføringsudvekslingsdefinition**, som du kan afslutte ved at angive, hvilke elementer i filen, der skal knyttes til hvilke felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Du kan også bruge funktionen **Hent filstruktur** på siden **Bogføringsudvekslingsdefinition**, som bruger funktionerne på siden **XML-skemafremviser** til at udfylde oversigtspanelet **Kolonnedefinitioner**.  

> [!NOTE]
> I frigivelsesbølge 1 i 2019 og tidligere versioner kan du generere en XMLport, der er baseret på skemaet, og derefter indlæse den i løsningen. Dette understøttes ikke længere.

## Se også

[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Om Data Exchange Framework](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]