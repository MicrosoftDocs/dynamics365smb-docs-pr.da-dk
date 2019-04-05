---
title: Gennemgang - Gennemførsel af en salgskampagne | Microsoft Docs
description: En kampagne er enhver aktivitet, der involverer flere kontakter. En vigtig del af oprettelsen af en kampagne er at vælge målgruppen for kampagnen. Til dette formål kan du i Business Central oprette en målgruppe eller en gruppe af kontakter ved hjælp af filtre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1922c9c2112006b302851301224818f803d9f4e2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792901"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Gennemgang: Gennemførsel af en salgskampagne
En kampagne er enhver aktivitet, der involverer flere kontakter. En vigtig del af oprettelsen af en kampagne er at vælge målgruppen for kampagnen. Til dette formål kan du i [!INCLUDE[d365fin](includes/d365fin_md.md)] oprette en målgruppe eller en gruppe af kontakter ved hjælp af filtre.  

 Du bruger disse funktioner i Salg & Marketing til omhyggelig planlægning af dine marketingaktiviteter og til administration af dine interaktioner med kontakter og kunder. Du kan oprette kampagner og målgrupper med dine kontakter til mailadresselister og andre typer interaktion med dine kontakter og kundeemner.  

 Funktionen til kampagner og målgrupper med aktivering af de automatisk processer giver dig mulighed for at planlægge, organisere og holde styr på dine marketingaktiviteter. Dette øger dine chancer for at få nye kunder og bibeholde eksisterende kunder.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
 Denne gennemgang viser processen til opfølgning på en handelsmesse og fokusering på potentielle kunder (kontakter) i en opfølgningskampagne.  

 Gennemgangen introducerer funktionen til kampagne- og målgruppeadministration i Salg & Marketing-afdelingen. Denne gennemgang illustrerer følgende opgaver:  

-   Oprettelse af en kampagne.  
-   Valg af målgruppe.  
-   Søgning efter data.  
-   Afsendelse af breve til kontakter.  
-   Registrering af kampagnesvar.  

## <a name="roles"></a>Roller  
 Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Marketingchef eller salgschef  
-   Marketingmedarbejder  

## <a name="prerequisites"></a>Forudsætninger  
 Før du kan udføre opgaverne i denne gennemgang, skal du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Historie  
 Marketingmanager i salgsafdelingen for CRONUS er ansvarlig for planlægning af kampagner og for at udføre dem. Han træffer også beslutninger om, hvilke handelsmesser, de skal deltage i, og han evaluerer kampagnefremskridt.  

 Marketingmedarbejderen fra marketingafdelingen tager sig af produktion, distribution og udleveringen af marketingmaterialer.  

 Virksomheden har lige lanceret et nyt produkt med navnet Millennium Server. Produktet blev for nyligt markedsført på en handelsmesse, Computer Futurus. Mange kunder udtrykte deres store interesse for produktet, og som del af en markedsføringsmæssig indsats blev de kunder, der købte Millennium Server i en kampagneperiode, tilbudt en særlig kampagnepris.  

 En af marketingmedarbejderens opgaver efter handelsmessen er at angive de potentielle kunder som kontakter.  

 Marketingchefen opretter en kampagne, opretter en målgruppe med alle de nye kontakter og søger derefter efter kontaktdata for at vælge målgruppen for kampagnen.  

 Medarbejderen med at sende et takkebrev ud til alle de kontakter, der har givet deres kort til medarbejderne på standen, og til sidst registrerer chefen alle de svar, der blev modtaget fra kundeemnerne.  

## <a name="setting-up-a-campaign"></a>Oprette en kampagne  
 Når medarbejderen har indtastet de modtagne forretningskort fra handelsmessen, opretter marketingchefen et kampagnekort til administration af de aktiviteter, der er involveret i kampagnen.  

### <a name="to-set-up-a-campaign"></a>Sådan oprettes en kampagne  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kampagner**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny** for at oprette en ny kampagne. På kampagnekortet skal du trykke på Enter for få indsat et kampagnenummer automatisk.  
3.  Gå til feltet **Beskrivelse**, og indtast en beskrivelse af kampagnen, f.eks. **FUTURUS-handelsmesse**.  
4.  Vælg feltet **Statuskode**, og vælg en statuskode fra listen, der åbnes på siden **Kampagnestatus**.  
5.  Udfyld felterne **Startdato** og **Slutdato** for kampagnen som ønsket.  

## <a name="selecting-the-target-audience"></a>Vælge målgruppe  
 Marketingchefen opretter en målgruppe for at vælge de kontakter, som han vil interagere med.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Sådan oprettes en målgruppe med de relevante kontakter  

1.  Vælg handlingen **Målgrupper**.  
2.  Vælg handlingen **Ny** for at oprette en ny målgruppe. På kampagnekortet skal du trykke på Enter for få indsat et målgruppenummer automatisk.  
3.  Gå til oversigtspanelet **Generelt** og feltet **Beskrivelse**, og indtast f.eks. **Besøgende på FUTURUS-handelsmessen**.  

     Når du har indtastet de generelle oplysninger om målgruppen, skal du vælge de kontakter, der skal inkluderes i målgruppen.  

     Du kan bruge en række forskellige kriterier til at vælge kontakter, f.eks. kan du vælge kontaktpersoner, der arbejder hos en kunde eller hos en mulig kunde og er ansvarlige for indkøb i virksomheden.  

     Du kan bruge filtre til at tilføje kontaktpersoner i henhold til de kriterier, der passer bedst til dit formål. Du kan f.eks. filtrere efter kontaktpersonens ansvarsområde eller forretningsforbindelse eller kontaktvirksomhedens branche. I denne gennemgang skal du vælge filteret **Ansvarsområde** for at vælge kontakter.  

4.  På siden **Målgruppe** skal du vælge handlingen **Tilføj kontakter** for at åbne filteret **Tilføj kontakter**.  
5.  Gå til oversigtspanelet **Ansvarsområde**, vælg filteret **Køb** som **Ansvarsområdekode**, og klik på **OK**.  

     Siden **Målgruppe** indeholder nu en liste over kontakter, der er baseret på det filter, du har angivet. I feltet **Antal linjer** i oversigtspanelet **Generelt** kan du se en oversigt over antallet af kontaktpersoner, der opfylder disse kriterier.  

    > [!NOTE]  
    >  Du kan gemme målgruppekriterierne, så de kan bruges igen senere.

    1.  På siden **Målgruppe** skal du vælge handlingen **Målgruppe** og derefter vælge handlingen **Gem kriterier**.  
    2.  På siden **Gem målgruppekriterie** skal du indtaste koden for målgruppen. I feltet **Beskrivelse** skal du indtaste beskrivelsen af målgruppekriterierne.
    3.  Vælg knappen **OK**.  

## <a name="mining-the-data"></a>Søge efter data  
 Marketingchefen ser nærmere på listen med udvalgte kontakter og kan se, at listen er alt for lang. Han beslutter at reducere listen ud fra de reelle kundeemner for at sikre, at han fokuserer på den rigtige målgruppe. Denne proces med at finjustere og/eller reducere dataene kaldes datasøgning.  

### <a name="to-remove-contacts-from-the-segment"></a>Sådan fjernes kontakter fra målgruppen  

1.  Gå til siden **Målgruppe**, vælg handlingen **Kontakter**, og vælg derefter handlingen **Reducer kontakter** for at åbne siden **Fjern kontakter - fjern**.  
2.  Gå til oversigtspanelet **Forretningsrelation**, vælg filteret **EMNE** som **Forretningsrelationskode**, og klik på **OK**.  

     Siden **Målgruppe** indeholder nu en reduceret liste over kontakter, og i feltet **Antal linjer**, kan du se antallet af kontakter, der nu passer til de nye kriterier.  

    > [!NOTE]  
    >  Hvis du skal tilbageføre denne fjernelse af en gruppe kontakter, kan du gøre det ved hjælp af funktionen **Gå tilbage**. Med andre ord kan du fortryde dine sidste segmentering.  
    >   
    >  På siden **Målgruppe** skal du vælge handlingen **Målgruppe** og derefter vælge handlingen **Gå tilbage**.  
    >   
    >  De kontaktpersoner, du lige har fjernet, føjes til listen over kontaktpersoner.  

## <a name="linking-a-segment-to-a-campaign"></a>Knytte en målgruppe til en kampagne  
 Marketingchefen beslutter, at den reducerede liste er den endelige liste over kontakter, der skal være en del af kampagnen. Han knytter derfor denne målgruppe til kampagnen FUTURUS-handelsmesse.  

### <a name="to-link-a-segment-to-the-campaign"></a>Sådan knyttes en målgruppe til kampagnen  

1.  På siden **Målgruppe** i oversigtspanelet **Kampagne** skal du vælge feltet **Kampagnenr.** for at vælge den kampagne, du ønsker, at målgruppen skal knyttes til, f.eks., **CP0001**.  
2.  Da denne målgruppe er målet for kampagnen, skal du markere afkrydsningsfeltet **Kampagnemålgruppe**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Sende breve og mails til kontakter  
 Marketingsmedarbejderen hjælper marketingchefen med at sende korrespondance ud til kundeemner, hvor han takker dem for, at de besøgte handelsmessen.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Bruge en målgruppe til at sende et brev til en kontakt  

1.  Åbn kortet **Målgruppe** for **Besøgende på FUTURUS-handelsmessen**.  
2.  Gå til oversigtspanelet **Interaktion** og feltet **Interaktionsskabelonkode**, og vælg skabelonen Brev, kode **BUS**.  
3.  I feltet **Emne (standard)** kan du indtaste følgende eksempel på tekst: **Tak, fordi du besøgte handelsmessen**.  

    > [!NOTE]  
    >  Denne skabelon består af mere end ét vedhæftet dokument, der hver er skrevet på forskellige sprog. Sprogene inkluderer f.eks. engelsk og dansk.  

4.  Vælg feltet **Sprogkode (standard)** ved at åbne siden **Målgruppeinteraktionssprog**. Vælg en sprogkode, og vælg derefter knappen **OK**.  
5.  Du kan få vist dokumentet på det valgte sprog. Vælg handlingen **Vedhæftet fil**, og vælg derefter handlingen **Åbn**.  

     Hvis du vil besvare meddelelsen med anmodning om tilladelse til at starte Word, skal du vælge indstillingen **Tillad for denne klientsession**.  

     Dette åbner vedhæftede Word-dokumenter, så du kan kontrollere den. Du kan også bruge denne lejlighed til at redigere og ændre brevet. Luk Word, når du er færdig.  

6.  Indtast emnet for brevet i feltet **Emne** på det sprog, der er valgt for skabelonen.  
7.  Vælg handlingen **Log**.
8.  Markér afkrydsningsfeltet **Send vedhæftede filer** for at få de vedhæftede filer udskrevet.  

    1. Markér afkrydsningsfeltet **Opret opfølgningsmålgruppe**.  
    2. Vælg knappen **OK** for at starte kørslen **Gem målgruppe**.  

9. De vedhæftede filer sendes. Når processen er færdig, skal du vælge knappen **OK** for den meddelelse, der angiver, at målgruppen er registreret.  

     Brevene udskrives automatisk, og målgruppen registreres. Da målgruppen er registreret, findes den ikke længere på listen over målgrupper, men er flyttet til listen over registrerede målgrupper. For at se listen skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Gemte målgrupper**, og vælg derefter det relaterede link.  

10. Når målgruppen er registreret, registreres hvert brev, der er sendt, som en interaktion, som du kan se i logfilen.  

     Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Interaktionslogposter**, og vælg derefter det relaterede link. Der er en post for hvert brev, der er sendt.  

### <a name="to-send-an-email-message-to-a-contact"></a>Sende en mail til en kontakt  

1.  Gå til oversigtspanelet **Interaktion** og feltet **Interaktionsskabelonkode**, og vælg skabelonen Brev, kode **BUS**.  
2.  I feltet **Emne (standard)** kan du indtaste følgende eksempel på tekst: **Tak, fordi du besøgte handelsmessen**.  
3.  Vælg **Mail** i feltet **Korrespondancetype**.  
4.  Angive sprogindstillinger, som i den foregående procedure.  
5.  Vælg handlingen **Log**. Siden **Gemt målgruppe** åbnes.  
6.  Markér afkrydsningsfeltet **Send vedhæftede filer** for at få de vedhæftede filer sendt pr. mail.  
7.  Markér afkrydsningsfeltet **Opret opfølgningsmålgruppe**.  
8.  Vælg knappen **OK**.  

     Brevene sendes automatisk pr. mail, og målgruppen registreres. Da målgruppen er registreret, findes den ikke længere på listen over målgrupper, men er gemt på listen over registrerede målgrupper. For at se listen skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Gemte målgrupper**, og vælg derefter det relaterede link.  

## <a name="registering-campaign-responses"></a>Registrere kampagnesvar  
 I løbet af de næste par uger svarer kundeemnerne på brevet. Marketingchefen ønsker at holde styr på svarene og registrerer disse interaktioner.  

 Opret en målgruppe med de kontakter, der svarer på brevet, til dette formål.  

### <a name="to-register-campaign-responses"></a>Sådan registreres kampagnesvar.  

1.  Gå til siden **Målgruppe**, og udvid oversigtspanelet **Interaktion**.  
2.  Vælg feltet **Interaktionsskabelonkode**.  

     Der er ingen interaktionsskabelon til registrering af svar på kampagner. Opret derfor en ny skabelon.  

3.  På siden **Interaktionsskabeloner** skal du vælge handlingen **Ny**.  
4.  Gå til feltet **Kode**, indtast **SVAR**, og gå til feltet **Beskrivelse**, og indtast **Kampagnesvar**.  
5.  Vælg knappen **OK**.  
6.  Vælg denne interaktionsskabelon i feltet **Interaktionsskabelonkode**, og bekræft den meddelelse, hvor du bliver spurgt, om du vil opdatere målgruppelinjen med den samme interaktionsskabelonkode.  

     Angiv nu, at disse kontakter har svaret på kampagnen:  
7.  I feltet **Kampagnenr.** i oversigtspanelet **Kampagne** skal du vælge en kampagne.  
8.  Forlad feltet **Kampagnenr.**, og bekræft den meddelelse, hvori du bliver spurgt, om du vil opdatere målgruppelinjen med den samme interaktionsskabelonkode.  
9. Vælg feltet **Kampagnereaktion**, og bekræft den efterfølgende meddelelse.  

     Log målgruppen for at sikre, at interaktionerne er registreret.  
10. Vælg handlingen **Logfør** under på siden **Målgruppe**.  
11. Gå til siden **Gem målgruppe**, fjern markeringen i afkrydsningsfeltet **Send vedhæftede filer**, og klik derefter på **OK**, og bekræft den meddelelse, der vises.  

     Når målgruppen er gemt, oprettes der automatisk en post for kampagnen, så denne handling kan registreres på siden **Kampagneposter**.  

## <a name="see-also"></a>Se også  
[Relationsstyring](marketing-relationship-management.md)  
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
