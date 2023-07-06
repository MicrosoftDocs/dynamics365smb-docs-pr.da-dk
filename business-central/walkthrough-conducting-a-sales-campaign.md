---
title: 'Gennemgang: Gennemførsel af en salgskampagne'
description: 'Denne gennemgang giver en detaljeret oversigt over alle de opgaver, der er forbundet med at udføre en salgskampagne i Business central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-conducting-a-sales-campaign"></a><a name="walkthrough-conducting-a-sales-campaign"></a><a name="walkthrough-conducting-a-sales-campaign"></a>Gennemgang: Gennemførsel af en salgskampagne

En kampagne er enhver aktivitet, der involverer flere kontakter. En vigtig del af oprettelsen af en kampagne er at vælge målgruppen for kampagnen. Til dette formål kan du i [!INCLUDE[prod_short](includes/prod_short.md)] oprette en målgruppe eller en gruppe af kontakter ved hjælp af filtre.  

 Du bruger disse funktioner i Salg & Marketing til omhyggelig planlægning af dine marketingaktiviteter og til administration af dine interaktioner med kontakter og kunder. Du kan oprette kampagner og målgrupper med dine kontakter til mailadresselister og andre typer interaktion med dine kontakter og kundeemner.  

 Funktionen til kampagner og målgrupper med aktivering af de automatisk processer giver dig mulighed for at planlægge, organisere og holde styr på dine marketingaktiviteter. Dette øger dine chancer for at få nye kunder og bibeholde eksisterende kunder.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Om denne gennemgang

 Denne gennemgang viser processen til opfølgning på en handelsmesse og fokusering på potentielle kunder (kontakter) i en opfølgningskampagne.  

 Gennemgangen introducerer funktionen til kampagne- og målgruppeadministration i Salg & Marketing-afdelingen. Denne gennemgang illustrerer følgende opgaver:  

- Forbereder dataene.
- Oprettelse af en kampagne.  
- Valg af målgruppe.  
- Søgning efter data.  
- Afsendelse af breve til kontakter.  
- Registrering af kampagnesvar.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Roller

 Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

- Marketingchef eller salgschef  
- Marketingmedarbejder  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger

 Før du kan udføre opgaverne i denne gennemgang, skal du installere [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="story"></a><a name="story"></a><a name="story"></a>Historie

 Marketingmanager i salgsafdelingen for CRONUS er ansvarlig for planlægning af kampagner og for at udføre dem. Marketingchefen træffer også beslutninger om, hvilke handelsmesser, de skal deltage i, og han evaluerer kampagnefremskridt.  

 Marketingmedarbejderen fra marketingafdelingen tager sig af produktion, distribution og udleveringen af marketingmaterialer.  

 Virksomheden har lige lanceret et nyt produkt med navnet Rome Guest Chair. Produktet blev for nyligt markedsført på en handelsmesse, Office Futurus. Mange kunder udtrykte deres store interesse for produktet, og som del af en markedsføringsmæssig indsats blev de kunder, der købte Rome Guest Chair i en kampagneperiode, tilbudt en særlig kampagnepris.  

 En af marketingmedarbejderens opgaver efter handelsmessen er at angive de potentielle kunder som kontakter.  

 Marketingchefen opretter en kampagne, opretter en målgruppe med alle de nye kontakter og søger derefter efter kontaktdata for at vælge målgruppen for kampagnen.  

 Medarbejderen med at sende et takkebrev ud til alle de kontakter, der har givet deres kort til medarbejderne på standen, og til sidst registrerer chefen alle de svar, der blev modtaget fra kundeemnerne.  

## <a name="setting-up-a-campaign"></a><a name="setting-up-a-campaign"></a><a name="setting-up-a-campaign"></a>Oprette en kampagne

 Når medarbejderen har indtastet de modtagne forretningskort fra handelsmessen, opretter marketingchefen et kampagnekort til administration af de aktiviteter, der er involveret i kampagnen.  

### <a name="to-set-up-a-campaign"></a><a name="to-set-up-a-campaign"></a><a name="to-set-up-a-campaign"></a>Sådan oprettes en kampagne

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kampagner**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** for at oprette en ny kampagne. På kampagnekortet skal du trykke på <kbd>Enter</kbd> for få indsat et kampagnenummer automatisk.  
3. Gå til feltet **Beskrivelse**, og indtast en beskrivelse af kampagnen, f.eks. **Office Futurus-handelsmesse**.  
4. Vælg feltet **Statuskode**, og vælg statuskode "1-plan". 
5. Udfyld felterne **Startdato** og **Slutdato** for kampagnen som ønsket.  

## <a name="selecting-the-target-audience"></a><a name="selecting-the-target-audience"></a><a name="selecting-the-target-audience"></a>Vælge målgruppe

 Marketingchefen opretter en målgruppe for at vælge de kontakter, som han vil interagere med.  
 
 Når du opretter en målgruppe, kan du bruge en række kriterier til at vælge de kontakter, der skal være mål for målgruppen. Du kan f.eks. bruge en række forskellige kriterier til at vælge kontakter, f.eks. kontaktpersoner, der arbejder hos en kunde eller hos en mulig kunde og er ansvarlige for indkøb i virksomheden. Du kan bruge filtre til at tilføje kontaktpersoner i henhold til de kriterier, der passer bedst til dit formål. Du kan f.eks. filtrere efter kontaktpersonens ansvarsområde eller forretningsforbindelse eller kontaktvirksomhedens branche. I denne gennemgang skal du vælge filteret **Ansvarsområde** for at vælge kontakter.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a><a name="to-create-a-segment-with-the-relevant-contacts"></a><a name="to-create-a-segment-with-the-relevant-contacts"></a>Sådan oprettes en målgruppe med de relevante kontakter

1. Vælg **Naviger**, og vælg derefter handlingen **Målgrupper**.  
2. Vælg handlingen **Ny** for at oprette en ny målgruppe. På kampagnekortet skal du trykke på **Enter** for få indsat et målgruppenummer automatisk.  
3. Gå til oversigtspanelet **Generelt** og feltet **Beskrivelse**, og indtast f.eks. *Besøgende på Office Futurus-handelsmessen*.
4. Vælg handlingen **Tilføj kontakter** for at åbne filteret **Tilføj kontakter**.  
5. Gå til oversigtspanelet **Kontakts ansvarsområde**, vælg filteret **Køb** som **Ansvarsområdekode**, og klik på **OK**.  

Siden **Målgruppe** indeholder nu en liste over kontakter, der er baseret på det filter, du har angivet. I feltet **Antal linjer** i oversigtspanelet **Generelt** kan du se en oversigt over antallet af kontaktpersoner, der opfylder disse kriterier.  

> [!NOTE]  
> Du kan gemme målgruppekriterierne, så de kan bruges igen senere.

### <a name="to-save-your-segmentation-criteria"></a><a name="to-save-your-segmentation-criteria"></a><a name="to-save-your-segmentation-criteria"></a>Sådan gemmes målgruppekriterier

1. Vælg handlingen **Handlinger** på siden **Målgruppe**.
2. Vælg **Funktioner**, **Målgruppe** og vælg derefter **Gem kriterie**.  
3. På siden **Gem målgruppekriterie** skal du indtaste koden for målgruppen. I feltet **Beskrivelse** skal du indtaste beskrivelsen af målgruppekriterierne.
4. Vælg knappen **OK**.  

## <a name="mining-the-data"></a><a name="mining-the-data"></a><a name="mining-the-data"></a>Søge efter data

 Marketingchefen ser nærmere på listen med udvalgte kontakter og kan se, at listen er alt for lang. Chefen beslutter at reducere listen ud fra de reelle kundeemner for at sikre, at han fokuserer på den rigtige målgruppe. Denne proces med at finjustere og/eller reducere dataene kaldes datasøgning.  

### <a name="to-remove-contacts-from-the-segment"></a><a name="to-remove-contacts-from-the-segment"></a><a name="to-remove-contacts-from-the-segment"></a>Sådan fjernes kontakter fra målgruppen

1. Vælg handlingen **Handlinger** på siden **Målgruppe**.
2. På menulinjen nedenfor skal du vælge **Funktioner**, Vælg **Kontakter** og derefter **Reducér kontakter**.  

  Siden **Fjern kontakter - reducér** åbnes.  
4. Gå til oversigtspanelet **Kontakt forretningsrelation**, vælg filteret **CUST** som **Forretningsrelationskode**, og klik på **OK**.

 Siden **Målgruppe** indeholder nu en reduceret liste over kontakter, og i feltet **Antal linjer**, kan du se antallet af kontakter, der nu passer til de nye kriterier.  

 > [!NOTE]  
 > Hvis du skal tilbageføre denne fjernelse af en gruppe kontakter, kan du gøre det ved hjælp af funktionen **Gå tilbage**. Med andre ord kan du fortryde dine sidste segmentering.  

### <a name="to-bring-back-the-removed-contacts"></a><a name="to-bring-back-the-removed-contacts"></a><a name="to-bring-back-the-removed-contacts"></a>Sådan tilbageføres de fjernede kontaktpersoner

1. Vælg handlingen **Målgruppe** på siden **Målgruppe**.
2. Vælg handlingen **Gå tilbage**.

De kontaktpersoner, du lige har fjernet, føjes til listen over kontaktpersoner.

## <a name="linking-a-segment-to-a-campaign"></a><a name="linking-a-segment-to-a-campaign"></a><a name="linking-a-segment-to-a-campaign"></a>Knytte en målgruppe til en kampagne

Marketingchefen beslutter, at den reducerede liste er den endelige liste over kontakter, der skal være en del af kampagnen. De knytter derfor denne målgruppe til kampagnen FUTURUS-handelsmesse.  

### <a name="to-link-a-segment-to-the-campaign"></a><a name="to-link-a-segment-to-the-campaign"></a><a name="to-link-a-segment-to-the-campaign"></a>Sådan knyttes en målgruppe til kampagnen

1. På siden **Målgruppe** i oversigtspanelet **Kampagne** skal du vælge feltet **Kampagnenr.** for at vælge den kampagne, du ønsker, at målgruppen skal knyttes til, f.eks., **CP0001**.
2. Vælg **Ja**.  
3. Da denne målgruppe er målet for kampagnen, skal du markere afkrydsningsfeltet **Kampagnemålgruppe** og vælge **Ja**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a><a name="sending-letters-and-email-messages-to-contacts"></a><a name="sending-letters-and-email-messages-to-contacts"></a>Sende breve og mails til kontakter

 Marketingsmedarbejderen hjælper marketingchefen med at sende korrespondance ud til kundeemner, hvor han takker dem for, at de besøgte handelsmessen.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a><a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a><a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Bruge en målgruppe til at sende et brev til en kontakt

> [!NOTE]  
> I denne procedure skal du vedhæfte et Word-dokument. Du kan tilføje vedhæftede filer på alle sprog.

> [!NOTE]  
> Klik eventuelt på ikonet **Rediger blyant** for at åbne siden i redigeringstilstand.

1. Åbn kortet **Målgruppe** for **Besøgende på FUTURUS-handelsmessen**.  
2. Gå til oversigtspanelet **Interaktion** og feltet **Interaktionsskabelonkode**, og vælg skabelonen Brev, kode **BUS** og vælg **Ja**.
3. Vælg feltet **Sprogkode (standard)** ved at åbne siden **Målgruppeinteraktionssprog**. Vælg en **sprogkode**, og vælg derefter knappen **OK**.
4. Kontroller, at **korrespondancetypen (standard)** er indstillet til **papirformat**.
5. Marker **Ellipsefeltet** i feltet **Vedhæftet fil**. Derved åbnes dialogboksen Indlæs vedhæftet fil.
    1. Klik på knappen **Vælg** for at vælge filen.
    1. Find filen, og klik på knappen **Åbn** for at vedhæfte filen.
6. I feltet **Emne (standard)** kan du indtaste følgende eksempel på tekst: **Tak, fordi du besøgte handelsmessen**. Tryk på <kbd>Tab</kbd> for at lukke feltet, og klik på knappen **Ja**.
7. Skub **Send Word-dok. som vedh. filer** til på, og vælg knappen **Ja**.
8. Vælg handlingen **Log**. I pop op-vinduet Log målgruppe aktivere: **Opret opfølgningsmålgruppe**
9. Vælg knappen **OK** for at starte kørslen **Gem målgruppekørsel**.  

De vedhæftede filer sendes. Når processen er færdig, skal du vælge knappen **OK** for den meddelelse, der angiver, at målgruppen er registreret.  

 Brevene udskrives automatisk, og målgruppen registreres. Da målgruppen er registreret, findes den ikke længere på listen over målgrupper, men er flyttet til listen over registrerede målgrupper. Du kan se den liste ved at vælge ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Gemte målgrupper**, og vælg derefter det relaterede link.  

Når målgruppen er registreret, registreres hvert brev, der er sendt, som en interaktion, som du kan se i logfilen.  

Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Interaktionslogposter**, og vælg derefter det relaterede link. Der er en post for hvert brev, der er sendt.  

### <a name="to-send-an-email-message-to-a-contact"></a><a name="to-send-an-email-message-to-a-contact"></a><a name="to-send-an-email-message-to-a-contact"></a>Sende en mail til en kontakt

1. Gå til oversigtspanelet **Interaktion** og feltet **Interaktionsskabelonkode**, og vælg skabelonen Brev, kode **BUS**.  
2. I feltet **Emne (standard)** kan du indtaste følgende eksempel på tekst: **Tak, fordi du besøgte handelsmessen**.  
3. Vælg **Mail** i feltet **Korrespondancetype**.  
4. Angive sprogindstillinger og vedhæfte et Word-dokument som i den foregående procedure.  
5. Vælg handlingen **Log**. Siden **Gemt målgruppe** åbnes.  
6. Markér afkrydsningsfeltet **Send vedhæftede filer** for at få de vedhæftede filer sendt pr. mail.  
7. Markér afkrydsningsfeltet **Opret opfølgningsmålgruppe**.  
8. Vælg knappen **OK**.  

 Brevene sendes automatisk pr. mail, og målgruppen registreres. Da målgruppen er registreret, findes den ikke længere på listen over målgrupper, men er gemt på listen over registrerede målgrupper. Du kan se den liste ved at vælge ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Gemte målgrupper**, og vælg derefter det relaterede link.  

## <a name="registering-campaign-responses"></a><a name="registering-campaign-responses"></a><a name="registering-campaign-responses"></a>Registrere kampagnesvar

 I løbet af de næste par uger svarer kundeemnerne på brevet. Marketingchefen ønsker at holde styr på svarene og registrerer disse interaktioner.  

 Opret en målgruppe med de kontakter, der svarer på brevet, til dette formål.  

### <a name="to-register-campaign-responses"></a><a name="to-register-campaign-responses"></a><a name="to-register-campaign-responses"></a>Sådan registreres kampagnesvar.

1. Vælg feltet **Interaktionsskabelonkode** på siden **Målgruppe** i oversigtspanelet **Interaktion**.  

 Der er ingen interaktionsskabelon til registrering af svar på kampagner. Opret derfor en ny skabelon.  

2. På siden **Interaktionsskabeloner** skal du vælge handlingen **Ny**.  
3. Gå til feltet **Kode**, indtast **SVAR**, og gå til feltet **Beskrivelse**, og indtast **Kampagnesvar**.  
4. Vælg knappen **OK**.
5. Vælg **Ja** for at bekræfte, at du vil knytte denne interaktionsskabelonkode til alle målgruppelinjer.
6. Klik på oversigtspanelet **Kampagne**, og marker afkrydsningsfeltet **Kampagnesvar**. Vælg **Ja** for at bekræfte meddelelsen *Du har ændret kampagneresponset*.  
7. Vælg handlingen **Logfør** under på siden **Målgruppe**.  
8. Fjern markeringen i afkrydsningsfeltet **Send vedhæftede filer** på siden **Gemt målgruppe**. Klik derefter på **OK** for at bekræfte meddelelsen om, at målgruppen er gemt.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Relationsstyring](marketing-relationship-management.md)  
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
