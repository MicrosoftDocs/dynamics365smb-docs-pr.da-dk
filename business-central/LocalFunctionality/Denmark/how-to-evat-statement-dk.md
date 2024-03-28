---
title: Indsend momsafgivelser elektronisk
description: 'Denne artikel beskriver, hvordan du opretter og indsender momsangivelser elektronisk i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'vat, return, statement, electronic, denmark, submission'
ms.search.form: null
ms.date: 11/17/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="submit-vat-returns-electronically"></a>Indsend momsafgivelser elektronisk

I den danske lokalisering understøtter Microsoft Dynamics 365 Business Central i at bruge Skattestyrelsens VAT API til at indberette momsangivelser (moms).

For at generere en momsangivelse og sende den direkte til Skattestyrelsens VAT API skal du udføre følgende opsætning:

- På siden **Virksomhedsoplysninger** skal du konfigurere felterne **Registreringsnr.** og **momsregistreringsnr.** for den juridiske enhed. I feltet **Registreringsnr.** skal du indtaste den juridiske enheds CVR-nummer (Central Business Register).
- På siden **Opsætning af momsbogføring SAF-T** tilknytter du en opsætning af momsbogføringsgruppe med **Indberetningskode for salgsmoms** og **Købsmomsindberetningskode**.
- Anskaf certifikater til at arbejde med Skattestyrelsens VAT API, og gem dem i Azure key vault.

## <a name="set-up-vat-return-submission"></a>Konfigurere momsreturafsendelse

Udfør følgende procedurer for at oprette momsangivelse.

### <a name="set-up-certificates"></a>Konfigurere certifikater

Før du kan begynde opsætningen, skal en administrator konfigurere certifikater.

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Certifikater**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette _klientcertifikat_. Dette certifikat er et virksomhedscertifikat (VOCES3), der er udstedt af MitID Erhverv (OCES3). Den skal indeholde en privat nøgle til underskrift.
3. Vælg **Ny** for at oprette _servercertifikat_. Dette certifikat er et certifikat, som NemVirksomhed udleverer til at verificere svar XML.

### <a name="set-up-vat-statements"></a>Konfigurer momsangivelser

Hvis du vil definere en momsangivelse, skal du gøre følgende.

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikon, angiv **Momsangivelser**, og vælg derefter det relaterede link.
2. På siden **Momsopgørelser** skal du oprette en ny momsopgørelse ved at bruge siden **Momsopgørelsesnavn** eller bruge en standarderklæring.
3. På siden **Momsopgørelse** skal du bruge **Kasse nr.** felt for at opsætte momsopsætningslinjer, så de peger momsopsætninger til de korrekte eksportbokse. Hvert boksnummer er knyttet til `ModtagMomsangivelseForeloebig` XML-feltet.
4. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **E-afsendelse af momsopgørelsesopsætning**, og vælg derefter det relaterede link.
5. Opsæt endepunkter for **VirksomhedKalenderHent**, **ModtagMomsangivelseForeloebig** og **MomsangivelseKvitteringHent**-tjenester. Du kan vælge **Indstil standardslutpunkter** for at få systemet til at køre automatisk. Alternativt kan du foretage opdateringer, hvis standardværdierne ikke længere er brugbare.
6. Indstil **Klientcertifikatkode** og **Servercertifikatkode** til de certifikater, som du tidligere har oprettet og uploadet på siden **Certificeringer**.

## <a name="use-and-submit-a-vat-return"></a>Brug og indsend en momsangivelse

Hvis du vil indsende en momsangivelse, skal du gøre følgende:

1. Vælg ![Forstørrelsesglas-knap, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsangivelsesperioder**, og vælg derefter det relaterede link.
2. Vælg **Hent momsangivelsesperioder**. Dynamics 365 Business Central kontakter **VirksomhedKalenderHent**-slutpunktet og får momsangivelsesperioder for din virksomhed.
3. Vælg en eksisterende momsangivelsesperiode, og vælg derefter **Opret momsangivelse**. Business Central opretter en ny **Moms retur**-post.
4. Vælg **Foreslå linjer** for at få foreslået og oprettet linjer/poster til momsangivelsen.
5. Når du kontrollerer og bekræfter gyldigheden af ​​de foreslåede linjer, skal du vælge **Frigøre** for at beskytte eventuelle ændringer i momsangivelsen, inden du indsender selvangivelsen.
6. Når du er klar til at indsende momsangivelsen, skal du vælge **Indsend** for at generere XML-legemet til anmodningen og sende anmodningen til **ModtagMomsangivelseForeloebig**-tjenesten.

Hvis processen er udført korrekt, modtager du meddelelsen "Anmodning er sendt", og momsangivelsens status ændres til **Indsendt**.

Du kan dobbelttjekke anmodningsmeddelelsen til momsangivelsen senere ved at vælge **Hent**.

## <a name="after-a-vat-return-is-submitted"></a>Efter indsendelse af momsangivelse

Du vil ikke altid kende den endelige status, der er bekræftet af myndighederne. Derfor tjekker Business Central løbende **MomsangivelseKvitteringHent**-tjenesten gennem det konfigurerede slutpunkt, for at se efter ethvert svar om indsendte momsangivelser. Hvis et svar er tilgængeligt, modtages det, og status for virksomhedens momsangivelse ændres til **Accepteret** eller **Afvist**.

Du kan downloade en **Svar**-meddelelse ved at vælge **Hent**. Hvis status er **Accepteret**, kan du gemme kvitteringslinket til momsangivelsen.

## <a name="see-also"></a>Se også

[Økonomistyring](../../finance.md)  
[Oversigt over momsstyring](../../finance-manage-vat.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
