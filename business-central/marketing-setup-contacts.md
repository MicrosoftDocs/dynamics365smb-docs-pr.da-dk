---
title: Angive oplysninger om kontakter | Microsoft Docs
description: "Beskriver, de opgaver du skal udføre for at angive oplysninger og koder, f.eks. om brancher og forretningsrelationer, før du opretter kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: da-dk
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Konfigurere kontakter
Når du opretter kontakter, kan du angive specifikke oplysninger, f.eks. den branche som virksomhederne tilhører og dine forretningsmæssige forhold til kontakterne.

Før du opretter kontakter og registrerer oplysninger om forretningsforhold, skal du definere forskellige koder, som skal bruges til at tildele oplysningerne til virksomheder og personer. Der kan defineres koder til mailgrupper, brancher, forretningsforhold, webkilder, kompetenceniveau og ansvarsområder.

Når disse oplysninger er defineret, er det væsentligt mere organiseret at oprette kontakter, og det er langt mere effektivt, når du kan finde alle kontakter baseret på en bestemt gruppe. Hver gruppe i firmaet kan finde disse oplysninger, hvilket giver en meget bedre kommunikationen med disse kontakter.

I forbindelse med konfiguration af dine kontakter, skal du konfigurere den forretningsrelation, du har med dine kontakter, f.eks. kundeemne, bank, konsulent eller serviceleverandør. Du kan finde flere oplysninger i [Opsætning af forretningsrelationer i kontaktvirksomheder](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Konfigurere brancher for kontaktvirksomheder
Du bruger brancher til at angive, hvilken branchetype dine kontakter tilhører, f.eks. detailbranchen eller automobilbranchen.

Brug af brancher i kontakter er en totrinsproces. Først skal du definere branchekoden. Du behøver kun at udføre dette trin én gang for hver branche. Når du har en branchekode, kan du begynde at tildele koden til kontaktvirksomheder.

> [!NOTE]  
>   Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.

### <a name="to-define-an-industry-group-code"></a>Sådan defineres en branchekode
Koden for branchen definerer type eller kategori for gruppen, f.eks REKLAME for reklame, eller PRESSE for tv og radio. Du kan have flere branchekoder. Du definerer brancherne på siden **Brancher**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brancher**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

### <a name="AssignIndustryGroupContact"></a> Sådan tildeles brancher til en kontakt
Du kan ikke tildele brancher til en kontaktperson – kun til virksomheder.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Brancher**. Siden **Branchegrupper** åbnes.
3. I feltet **Branchekode** skal du vælge den branche, du vil tildele.

Gentag disse trin for hver branche, du vil tildele. Du kan også tildele brancher fra kontaktoversigten ved at udføre samme procedure.

Det antal brancher, du har tildelt til kontakten, vises i feltet **Antal brancher** i sektionen **Segmentering** på siden **Kontakt**.

Når du har tildelt brancher til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Oprette mailgrupper til kontakter
Du kan bruge mailgrupper til at angive grupper af kontakter, som skal modtage de samme oplysninger. F.eks. kan du oprette en mailgruppe til de kontakter, du vil sende en meddelelse til om at skifte kontor, og en anden gruppe om at sende gaver til andre kontakter.

Brug af mailgrupper til kontakter er en totrinsproces. Først skal du definere mailgruppekoden. Du behøver kun at udføre dette trin én gang for hver mailgruppe. Når du har en mailgruppekode, kan du begynde at tildele koden til kontaktvirksomheder.

### <a name="to-define-mailing-group-codes"></a>Sådan defineres mailgruppekoder
Feltet Mailgruppekode definerer type eller kategori af gruppen, f.eks SKIFT i forbindelse med skift af kontor eller GAVE i forbindelse med barsel. Du kan have flere branchekoder. Du definerer brancherne på siden **Mailgrupper**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Mailgrupper**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

### <a name="AssignMailGroupContact"></a> Sådan tildeles mailgrupper til en kontakt
1. Åbn kontakten.
2. Vælg handlingen **Mailgrupper**. Siden **Mailgrupper for kontakt** åbnes.
3. I feltet **Mailgruppekode** skal du vælge den mailgruppe, du vil tildele.

Gentag disse trin for hver mailgruppe, du vil tildele. Du kan også tildele mailgrupper fra kontaktoversigten ved at udføre samme procedure.

Det antal mailgrupper, du har tildelt kontakten, vises i feltet **Antal mailgrupper** i sektionen **Segmentering** på siden **Kontakt**.

Når du har tildelt mailgrupper til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Konfigurere alternative adresser for kontakter
Du kan tildele en alternativ adresse, som en kontaktperson i perioder får sendt post til, f.eks. et sommerhus. Du kan også tildele en eller flere datointervaller til hver af kontaktpersonens alternative adresser og på den måde angive, hvornår en bestemt adresse er gyldig.

### <a name="to-assign-an-alternate-address"></a>Sådan tildeles alternative adresser
1. Åbn kontakten.
2. Vælg handlingen **Alternativ adresse**, og vælg derefter **Kort**. Siden **Alt. adresser på kontakter** åbnes.
3. Indtast en ny alternativ adresse og udfyld felterne på siden **Kontaktens alternative adresse**.

Gentag disse trin for hver alternativ adresse, du vil tildele. Du kan angive flere datointervaller til hver alternativ adresser.

Du kan også tildele alternative adresser fra siden Kontaktoversigt ved at udføre samme procedure.

### <a name="to-assign-an-alternate-address-date-range"></a>Sådan tildeles et datointerval til en alternativ adresse
1. Åbn kontakten.
2. Vælg handlingen **Alternativ adresse**, og vælg derefter **Datointerval**. Siden **Alt. adr.datointv. - kontakt** åbnes.
3. Vælg handlingen **Ny**.
4. I feltet **Kontaktens alt. adr.kode** skal du vælge en alternativ adresse for kontakten og derefter udfylde felterne **Startdato** og **Slutdato**.

Gentag disse trin for hvert datointerval, du vil tildele.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Definere dine kontaktpersoners ansvarsområder
Du kan tilføje oplysninger om ansvarsområder for kontaktpersoner for at angive, hvad kontaktpersonen er ansvarlig for i virksomheden, f.eks. IT, administration eller produktion. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af ansvarsområder for kontakter er en totrinsproces. Først skal du definere koden for ansvarsområdet. Du behøver kun at udføre dette trin én gang for hvert ansvarsområde. Når du har et ansvarsområde, kan du begynde at tildele koden til kontakter.

### <a name="to-define-a-job-responsibility-code"></a>Sådan defineres en ansvarsområdekode
Ansvarsområdekoden definerer jobtypen eller -kategorien, f.eks. MARKETING eller INDKØB. Du kan have flere ansvarsområdekoder. Du definerer ansvarsområdet fra siden **Ansvarsområder**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ansvarsområder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Sådan tildeles ansvarsområder til en kontaktperson
Du kan ikke tildele ansvarsområder til kontaktvirksomheder.

1. Åbn kontaktpersonen.
2. Vælg handlingen **Person**, og vælg derefter handlingen **Ansvarsområder**. Siden **Kontakts ansvarsområder** åbnes.
3. I feltet **Ansvarsområdekode** skal du vælge det ansvarsområde, du vil tildele.

Gentag disse trin for hver ansvarsområde, du vil tildele. Du kan også tildele ansvarsområder fra kontaktoversigten ved at udføre samme procedure.

Det antal ansvarsområder, du har tildelt til kontakten, vises i feltet **Antal ansvarsområder** i sektionen **Segmentering** på siden **Kontakt**.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Opsætning af kompetenceniveauer for kontaktpersoner
Du kan bruge kompetenceniveauer til kontakter, så de selv kan angive den stilling, som de har i virksomheden, f.eks. ledelse. Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.

Brug af kompetenceniveauer til kontakter er en totrinsproces. Først skal du definere koden for kompetenceniveauet. Du behøver kun at udføre dette trin én gang for hvert kompetenceniveau. Når du har et kompetenceniveau, kan du begynde at tildele koden til kontakter.

### <a name="to-define-an-organizational-level-code"></a>Sådan defineres en kompetenceniveaukode
Kompetenceniveaukoden definerer kompetenceniveautypen eller -kategorien, f.eks. ADMINDIR eller ØKODIR. Du kan have flere kompetenceniveaukoder. Du definerer kompetenceniveauet fra siden **Kompetenceniveauer**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kompetenceniveauer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og indtast en kode og beskrivelse. Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Sådan tildeles kompetenceniveauer til en kontaktperson
Du kan kun tilknytte organisationsniveau til kontaktpersoner, ikke kontaktvirksomheder. Du kan kun tildele ét kompetenceniveau pr. kontakt.

1. Åbn kontakten.
2. I feltet **Kompetenceniveauer** skal du vælge den kode, du vil tildele.

Når du har tildelt kompetenceniveauer til dine kontakter, kan du bruge oplysningerne til at oprette målgrupper.

Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper. Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Opsætning af webkilder for kontaktvirksomheder
Du kan bruge webkilder til dine kontaktvirksomheder for at identificere f.eks. søgemaskiner og websteder på internettet, som du vil bruge til at søge efter oplysninger om kontakterne. Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

Brug af webkilder for kontakter er totrinsproces. Først skal du angive webkildekoden. Du behøver kun at udføre dette trin én gang for hver webkilde. Når du har en webkildekode, kan du begynde at tildele koden til kontakter.

### <a name="to-define-a-web-source-code"></a>Sådan defineres en webkildekode
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webkilder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne **Kode**, **Beskrivelse** og **URL**.

    Indtast %1 i feltet **URL** for at indsætte en pladsholder for et søgeord i URL-adressen. Når du starter webkilden fra en kontakt, erstattes %1 med det søgeord, du har indtastet på siden **Webkilder for kontakter**, f.eks. navnet på virksomheden.

Gentag disse trin for hver webkilde, du vil oprette.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Sådan tildeles webkilder til en kontaktvirksomhed
Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.

1. Åbn kontakten.
2. Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Webkilder**. Siden **Webkilder for kontakt** åbnes.
3. I feltet **Webkildekode** skal du vælge den webkilde , du vil tildele.
4. Brug feltet **Søgeord** til at indtaste det søgeord, som du vil bruge til at finde oplysningerne.

Gentag disse trin for hver webkilde, du vil tildele.

Du kan også tildele webkilder fra siden **Kontaktoversigt** ved at udføre samme procedure.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

