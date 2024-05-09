---
title: Indsend momsafgivelser elektronisk
description: 'Denne artikel beskriver, hvordan du opretter og indsender momsangivelser elektronisk i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'vat, return, statement, electronic, denmark, submission, skat'
ms.search.form: null
ms.date: 04/24/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Indsend momsafgivelser elektronisk

I den danske lokalisering understøtter Microsoft Dynamics 365 [!INCLUDE [prod_short](../../includes/prod_short.md)] i at bruge Skattestyrelsens VAT API til at indberette momsangivelser (moms).  

> [!IMPORTANT]
> Denne funktion gør det muligt at rapportere **_udkast til momsangivelsesversion_** til skat.dk websted fra [!INCLUDE [prod_short](../../includes/prod_short.md)]. Du skal stadig manuelt logge ind på din konto på skattemyndighedernes websted, gennemgå udkastet og indsende det endeligt. Rapportering af sådanne udkast skal først oprettes på skattemyndighedernes konto. (Se "Onboarding juridiske enheder" på skat.dk)

> [!NOTE]
> Før du begynder, skal du sørge for, at appen **E-afsendelse af momsopgørelsesopsætning** er installeret og aktiveret. 

For at generere en momsangivelse og sende den direkte til Skattestyrelsens VAT API skal du udføre følgende opsætning:

- På siden **Virksomhedsoplysninger** skal du konfigurere felterne **Registreringsnr.** og **momsregistreringsnr.** for den juridiske enhed. I feltet **Registreringsnr.** skal du indtaste den juridiske enheds CVR-nummer (Central Business Register).
- På siden **Opsætning af momsbogføring SAF-T** tilknytter du en opsætning af momsbogføringsgruppe med **Indberetningskode for salgsmoms** og **Købsmomsindberetningskode**.
- Anskaf certifikater til at arbejde med Skattestyrelsens VAT API, og gem dem i Azure key vault.

## Konfigurere momsreturafsendelse

Udfør følgende procedurer for at oprette momsangivelse.

### Konfigurere certifikater

> [!NOTE]
> Hvis du bruger [!INCLUDE [prod_short](../../includes/prod_short.md)] online, behøver du ikke konfigurere dine certifikater, da du skal bruge forudinstalleret Microsoft-sikkerhedscertifikat til momsindsendelse. 

Hvis du bruger en version i det lokale [!INCLUDE [prod_short](../../includes/prod_short.md)]-miljø, skal en administrator konfigurere certifikaterne på følgende måde, før du starter opsætningen: 

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Certifikater**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette _klientcertifikat_. Dette certifikat er et virksomhedscertifikat (VOCES3), der er udstedt af MitID Erhverv (OCES3). Den skal indeholde en privat nøgle til underskrift.
3. Vælg **Ny** for at oprette _servercertifikat_. Dette certifikat er et certifikat, som NemVirksomhed udleverer til at verificere svar XML.

### Opsætning af elektronisk momsangivelse 

Benyt følgende fremgangsmåde for at konfigurere elektronisk momsangivelse:

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af elektronisk momsangivelse**, og vælg derefter det relaterede link.  
2. På siden **Opsætning af elektronisk momsangivelse** skal du angive dit juridiske SE/CVR-nummer i feltet **ERP SE-nummer** som et nummer, der bruges til at indberette momsangivelsen til Skat-service. Når du har indtastet dit CVR-nummer, skal du give samtykke til, at dine data deles med tredjepartssystemet (skat.dk) i denne proces. Hvis du accepterer, skal du vælge knappen **Jeg accepterer**.  

### Konfigurere momsrapport  

Hvis du vil definere en momsrapport, skal du gøre følgende.

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Konfiguration af momsrapporter**, og vælg derefter det relaterede link.  
2. Sørg for, at opsætningen til momsangivelse med version **DK ELE.Moms** findes og vælges i feltet **Momsrapportversion** på siden **Momsrapportkonfiguration**. Denne opsætning aktiverer følgende felter: **Foreslå Lines Codeunit ID**, **Content Codeunit ID**, **Submission Codeunit ID** og **Validate Codeunit ID** og udfylder værdierne.
3. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsrapportkonfiguration**, og vælg derefter det relaterede link. 
4. På siden **Momsrapportopsætning** skal du vælge oversigtspanelet **Returperiode** og kontrollere, at feltet **Rapportversion** indeholder **DK ELE.Moms**-opsætningsrapportversion, som du tidligere har konfigureret.
5. Feltet **Manuel modtagelse af Codeunit-id**, hvor du kan angive det codeunit-id, der er knyttet til en manuel modtagelse af momsangivelsesperioder. Hvis codeunit `13610` er valgt, udfyldes feltet **Manuel modtagelse af Codeunit-tekst** automatisk med værdien **Elec. moms Hent perioder**.

### Konfigurer momsangivelser

Hvis du vil definere en momsangivelse, skal du gøre følgende:

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikon, angiv **Momsangivelser**, og vælg derefter det relaterede link.
2. På siden **Momsopgørelser** skal du oprette en ny momsopgørelse ved at bruge siden **Momsopgørelsesnavn** eller bruge en standarderklæring.
3. På siden **Momsopgørelse** skal du bruge **Kasse nr.** felt for at opsætte momsopsætningslinjer, så de peger momsopsætninger til de korrekte eksportbokse. Hvert boksnummer er knyttet til `ModtagMomsangivelseForeloebig` XML-feltet.
4. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **E-afsendelse af momsopgørelsesopsætning**, og vælg derefter det relaterede link.
5. Opsæt endepunkter for **VirksomhedKalenderHent**, **ModtagMomsangivelseForeloebig** og **MomsangivelseKvitteringHent**-tjenester. Du kan vælge **Indstil standardslutpunkter** for at få systemet til at køre automatisk. Alternativt kan du foretage opdateringer, hvis standardværdierne ikke længere er brugbare.
6. Indstil **Klientcertifikatkode** og **Servercertifikatkode** til de certifikater, som du tidligere har oprettet og uploadet på siden **Certificeringer**.

## Brug og indsend en momsangivelse

Hvis du vil indsende en momsangivelse, skal du gøre følgende:

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsangivelsesperioder**, og vælg derefter det relaterede link. 
2. Vælg **Hent momsangivelsesperioder**. Dynamics 365 [!INCLUDE [prod_short](../../includes/prod_short.md)] kontakter **VirksomhedKalenderHent**-slutpunktet og får momsangivelsesperioder for din virksomhed.  
3. Vælg en eksisterende momsangivelsesperiode, og vælg derefter **Opret momsangivelse**. [!INCLUDE [prod_short](../../includes/prod_short.md)] opretter en ny **Momsopgørelsespost**.  
4. Vælg **Foreslå linjer** for at få foreslået og oprettet linjer/poster til momsangivelsen.   
5. Når du kontrollerer og bekræfter gyldigheden af ​​de foreslåede linjer, skal du vælge **Frigøre** for at beskytte eventuelle ændringer i momsangivelsen, inden du indsender selvangivelsen. 
6. Når du er klar til at indsende momsangivelsen, skal du vælge **Indsend** for at generere XML-legemet til anmodningen og sende anmodningen til **ModtagMomsangivelseForeloebig**-tjenesten. 

Hvis processen er udført korrekt, modtager du meddelelsen "Anmodning er sendt", og momsangivelsens status ændres til **Indsendt**.

Du kan dobbelttjekke anmodningsmeddelelsen til momsangivelsen senere ved at vælge **Hent**.  

## Efter indsendelse af momsangivelse

Du vil ikke altid kende den endelige status, der er bekræftet af myndighederne. Derfor tjekker [!INCLUDE [prod_short](../../includes/prod_short.md)] løbende **MomsangivelseKvitteringHent**-tjenesten gennem det konfigurerede slutpunkt, for at se efter ethvert svar om indsendte momsangivelser. Hvis et svar er tilgængeligt, modtages det, og status for virksomhedens momsangivelse ændres til **Accepteret** eller **Afvist**.

Du kan downloade en **Svar**-meddelelse ved at vælge **Hent**. Hvis status er **Accepteret**, kan du gemme kvitteringslinket til momsangivelsen.

## Se også

[Økonomistyring](../../finance.md)    
[Oversigt over momsstyring](../../finance-manage-vat.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
