---
title: "Oprette XMLporte baseret på XML-skemaer | Microsoft Docs"
description: Bruge XML-skemaer til at konfigurere til dokumentudvekslingsstrukturen.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 06e0de9409fa26d18f051d84b39d021227a55191
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner
Hvis du vil aktivere import/eksport af data i XML-filer via dataudvekslingsstrukturen i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge XML-skemaer til at definere, hvilke dataelementer du vil udveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan udføre dette arbejde i vinduet **XML-skemafremviser** ved at indlæse XML-skemafilen, vælge de relevante dataelementer og derefter initialisere enten en dataudvekslingsdefinition eller en XMLport.  

 Når du har defineret, hvilke dataelementer der skal medtages, baseret på XML-skemaet, kan du bruge handlingen **Generér XMLport** til at oprette XMLport-objektet.  

 Alternativt kan du bruge **Generer dataudvekslingsdefinition** som handling til at initialisere en dataudvekslingsdefinition, der er baseret på de valgte dataelementer, som du derefter udfører inden for rammerne til udveksling af data. Herved oprettes der en post i vinduet **Bogføringsudvekslingsdefinitioner**, hvor du kan fortsætte ved at definere, hvilke elementer i filen, der knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

 Dette emne indeholder følgende procedurer:  

-   Sådan indlæses en XML-skemafil  

-   Sådan markeres eller fjernes markeringen af noder i et XML-skema  

-   Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema  

-   Sådan oprettes en XMLport for filen, der er baseret på et XML-skema  

-   Sådan importeres en XMLport i Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Sådan indlæses en XML-skemafil  

1.  Sørg for, at den pågældende XML-skemafil er tilgængelig. Filtypenavnet er .xsd.  

2.  I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.  

3.  Under fanen **Startside** i gruppen **Ny** skal du vælge **Ny**.  

4.  Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angiv en kode, der identificerer XML-skemaet.|  
    |**Beskrivelse**|Angiv en beskrivelse af XML-skemaet.|  

     Feltet **Målnavneområde** angiver navneområdet i den XML-skemafil, der er indlæst for linjen.  

5.  Under fanen **Startside** i gruppen **Proces** skal du vælge **Indlæs skema** og derefter vælge XML-skemafilen.  

     Når filen er indlæst, udfyldes resten af felterne på linjen med oplysninger fra filen, og afkrydsningsfeltet **Skema er indlæst** markeres.  

    > [!NOTE]  
    >  Som standard er træet for det indlæste indlæste XML-skema skjult. Udvid hver node ved at klikke på knappen **+** på noden. For at udvide alle noder skal du vælge **Udvid alle** på båndet.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Sådan markeres eller fjernes markeringen af noder i et XML-skema  

1.  I feltet **Søg** skal du indtaste **XML-skemafremviser** og derefter vælge det relaterede link.  

2.  Udfyld felterne i sidehovedet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode til XML-skema**|Angiv den XML-skemafil, du har indlæst i trin 5 i afsnittet "Sådan indlæses en XML-skemafil".|  
    |**Nyt XMLportnummer**|Angiv nummeret på den XMLport, der er oprettet fra dette XML-skema, når du vælger handlingen **Generér XMLport**.|  

     Linjerne er nu udfyldt med noder, der repræsenterer alle elementer i XML-skemaet. Noder for elementer, der er obligatoriske i henhold til XML-skemaet, er som standard valgt.  

3.  På den første linje i kolonnen **Nodenavn** skal du udvide noden **Dokument** og derefter gradvist udvide underliggende noder, du vil gennemgå.  

     Alternativt kan du højreklikke på en node og derefter vælge **Udvid alle**.  

4.  Brug fanen **Startside** og gruppen **Vis** til at vælge en af følgende handlinger for at ændre, hvilke noder der vises.  

    |**Handling**|Beskrivelse|  
    |----------------|---------------------------------------|  
    |**Vis alle**|Alle noder vises.|  
    |**Skjul ikke-obligatoriske**|Der vises kun de noder, der repræsenterer elementer, der kræves i henhold til XML-skemaet. Disse noder er typisk angivet med **1** i feltet **MinOccurs**.<br /><br /> Vælg **Vis alle** for at tilbageføre visningen.|  
    |**Skjul ikke-valgte**|Kun noder, hvor afkrydsningsfeltet **Markeret** er markeret, vises.<br /><br /> Vælg **Vis alle** for at tilbageføre visningen.|  

5.  Under fanen **Startside** i gruppen **Administrer** skal du vælge **Rediger**.  

6.  I afkrydsningsfeltet **Markeret** skal du angive for hver enkelt node, om elementet skal understøttes i dataudvekslingsdefinitionen for den relaterede SEPA-bankfil.  

    > [!NOTE]  
    >  Når du vælger en obligatorisk underordnet node, markeres alle overordnede noder ovenfor også.  

7.  Vælg handlingen **Marker alle obligatoriske elementer** for at markere alle noder, der repræsenterer elementer, der er obligatoriske i henhold til XML-skemaet.  

8.  Vælg handlingen **Afmarker alt** for at rydde alle markeringer.  

     Feltet **Valg** angiver, om noden har to eller flere sidestillede noder, der fungerer som valgmuligheder.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema  

1.  I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.  

2.  Vælg det relevante XML-skema, og vælg **Åbn XML-skemafremviser** i gruppen **Proces** under fanen **Startside**.  

3.  Sørg for, at de relevante noder er valgt. Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".  

4.  I vinduet **XML-skemafremviser** under fanen **Startside** skal du i gruppen **Proces** vælge **Generer dataudvekslingsdefinition**.  

 Der oprettes en dataudvekslingsdefinition i vinduet **Bogføringsudvekslingsdefinition**, som du kan afslutte ved at angive, hvilke elementer i filen, der skal knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Du kan også bruge funktionen **Hent filstruktur** i vinduet **Bogføringsudvekslingsdefinition**, som bruger funktionerne i vinduet **XML-skemafremviser** til at udfylde oversigtspanelet **Kolonnedefinitioner**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Sådan oprettes en XMLport, der er baseret på et XML-skema  

1.  I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.  

2.  Vælg det relevante XML-skema, og vælg **Åbn XML-skemafremviser** i gruppen **Proces** under fanen **Startside**.  

3.  I feltet **Nyt XMLportnummer** skal du angive det nummer, der tildeles det nye XMLport-objekt, når det er oprettet.  

4.  Sørg for, at de relevante noder er valgt. Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".  

5.  Brug fanen **Startside** og gruppen **Proces** til at vælge **Generér XMLPort**, og gem derefter objektet som en .txt-fil på en passende placering.  

6. Indlæs den nye XMLport til [!INCLUDE[d365fin](includes/d365fin_md.md)]-udviklingsmiljøet, og kompiler den.

## <a name="see-also"></a>Se også  
[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)   
[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)   
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)   
[Om Data Exchange Framework](across-about-the-data-exchange-framework.md)

