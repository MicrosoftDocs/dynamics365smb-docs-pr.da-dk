---
title: Angive generelle oplysninger om anlægsaktiver
description: 'Inden du kan arbejde med anlægsaktiver, skal du konfigurere standardfinanskonti, bogføringsgrupper, fordelingsnøgler, kladdetyper og -navne samt klassekoder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Opsætte generelle oplysninger om anlægsaktiver

Inden du kan arbejde med anlægsaktiver, skal du konfigurere standardfinanskonti, bogføringsgrupper, fordelingsnøgler, kladdetyper og batches samt genklassificere anlægsaktiver. Du skal også definere et klassifikationshierarki (klasser og underklasser) for at strukturere dine aktiver og om nødvendigt definere de lokationer, hvor du gemmer aktiver.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>Sådan defineres generelle adfærd for funktionerne for anlægsaktiver

Definér den generelle funktionsmåde eller anlægsaktivets funktion og oprette dokumentnummerserier på siden **Anlægsopsætning**.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsopsætning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Sådan oprettes anlægsbogføringsgrupper

Bruge bogføringsgrupper til at definere grupper af anlægsaktiver. Disse bogføringsgruppers poster bogføres på samme finanskonti.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov på siden **Anlægsbogføringsgruppekort**.

    > [!NOTE]  
    >   For at sikre, at modkonti for forskellige anlægsbogføringer bliver indsat automatisk, når du vælger handlingen **Indsæt anlægsmodkonto** på kladdelinjer, skal du følge det næste trin baseret på opskrivningsbogføringer.
4. I oversigtspanelet **Modkonto** skal du vælge den finanskonto i feltet **Opskrivningsmodkonto**, som du vil bogføre modposter for ved opskrivning.

Yderligere oplysninger om brug af handlingen **Indsæt anlægsmodkonto** til anlægskassekladdelinjer finder du under [Regulere anlægsaktiver](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>Sådan defineres anlægskladdetyper

En type er et foruddefineret format for en kladde. Typen indeholder oplysninger om sporingskoder, rapporter og nummerserier. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] opretter automatisk en anlægskladdetype, første gang du åbner siden **Anlægskladde**, men du kan definere andre kladdetyper.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>Sådan angives anlægsklasse- og underklassekoder

I anlægssager kan du definere et klassifikationshierarki, der kan bruges til at gruppere aktiver. Hierarkiet har to niveauer: klasser og underklasser.

### <a name="fixed-asset-class-codes"></a>Anlægsklassekoder

Anlægsklasser er poster på øverste niveau i det klassifikationshierarki, som du grupperer aktiver i. Brug f.eks. klasser til at opdele aktiver i materielle eller immaterielle aktiver. Der skal oprettes mindst én anlægsart i opsætningen.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsarter**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de anlægsklasser, du vil oprette.

### <a name="fixed-asset-subclass-codes"></a>Anlægs-underklassekoder

Anlægs-underklasser er poster på nr. to niveau i det klassifikationshierarki, som du grupperer aktiver i. Hver underklasse peger på en klasse på øverste niveau. Brug anlægsgruppekoder til at gruppere anlægsaktiver i kategorier, f.eks. bygninger, køretøjer, møbler eller maskiner. Der skal oprettes mindst én anlægsunderklasse i opsætningen.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsgrupper**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de anlægsunderklasser, du vil oprette.

## <a name="start-to-register-assets"></a>Begynd at registrere aktiver

Hvis det er første gang, du bruger modulet Anlæg i [!INCLUDE[prod_short](includes/prod_short.md)], skal du konfigurere finansmodulet, før du konfigurerer anlægsaktiver. Hvordan du gør dette afhænger af, om anlægsaktiverne er integreret med regnskabet.  

Følgende fremgangsmåde bruges, hvis anlægstransaktioner skal bogføres til finansposterne.  

1. Fuldfør de grundlæggende opsætninger for anlægsaktiver.  
2. Udfyld et anlægskort for hvert anlæg, der allerede findes.  
3. Oprette en anlægsafskrivningsprofil til hvert afskrivningsformål, (f.eks. skatteregnskaber eller årsregnskaber). Du skal selv definere betingelserne for hver afskrivningsprofil som f.eks. integration med finansbogholderiet.

    Aktivér finansintegration ved hjælp af de næste trin. Først skal sikre dig, at finansintegration er deaktiveret for alle afskrivningsprofiler, og derefter skal du bogføre åbningsposter og endelig aktivere finansintegration.  
4. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
5. Vælg det relevante afskrivningsprofilkort, og vælg derefter handlingen **Rediger** for at åbne siden **Afskrivningsprofilkort**.
6. I oversigtspanelet **Integration** skal du slå alle til/fra-knapperne fra. Hvis du har mere end én afskrivningsprofil, skal du gentage dette trin for hver enkelt.  
7. Skriv følgende linjer for hvert aktiv i anlægskladden:
   * En linje med anskaffelsen.
   * En linje med den akkumulerede afskrivning i slutningen af det foregående regnskabsår.
   * En linje med den akkumulerede afskrivning fra begyndelsen af det aktuelle regnskabsår til den dato, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er indstillet til at starte afskrivningen.

    Hvis du har andre åbningsposter, kan du også angive dem nu, f.eks. nedskrivning og opskrivning.  
8. Når du har angivet og bogført kladdelinjerne for hvert anlæg, skal du aktivere finansintegration i afskrivningsprofilerne.

Hvis anlægsaktiverne ikke er integreret med finansposterne, skal du springe trin seks og otte over.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>Sådan angives anlægslokationskoder (valgfrit)

Lokationskoder for anlægsaktiver definerer identifikation for anlæggets lokation, f.eks. salgsafdelingen, receptionen, administrationen, produktionen eller lagerstedet. Du kan bruge dem til at registrere et anlægs lokation. Disse oplysninger er nyttige i forbindelse med forsikring og lagerstedet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægslokationer**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de anlægslokationer, du vil oprette.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>Sådan defineres allokeringsnøgler for anlægsaktiver (valgfrit)

Brug allokeringsnøgler til at allokere transaktioner på forskellige afdelinger eller projekter. Du kan f.eks. definere en allokeringsnøgle til at allokere afskrivningerne på køretøjer med 35 procent til administrationsafdelingen og 65 procent til salgsafdelingen. Du kan finde flere oplysninger i [Fordele omkostninger og indtægter](year-allocate-costs-income.md).

Allokeringsnøgler gælder for anlægsarter og ikke for de enkelte anlægsaktiver.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. På siden **Anlægsbogføringsgrupper** skal du vælge handlingen **Allokeringer** og derefter vælge en bogføringstype.
3. På siden **Anlægsallokeringer** skal du udfylde felterne efter behov.
4. Gentag trin 2 og 3 for hver bogføringstype, du vil definere allokeringsnøgler for.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>Sådan defineres anlægsomposteringskladdenavne (valgfrit)

Du kan angive flere kladdenavne, som er individuelle kladder for hver kladdetype. En medarbejder kan f.eks. have sin egen kladde, hvor medarbejderens initialer anvendes som kladdenavn. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskladdetyper**, og vælg derefter det relaterede link.  
2. Markér den relevante kladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Anlægskladdenavne** skal du udfylde felterne efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>Sådan defineres anlægsomposteringskladdetyper (valgfrit)

Brug dedikerede omposteringskladder til at overføre, opdele eller kombinere anlægsaktiver. [!INCLUDE[prod_short](includes/prod_short.md)] opretter automatisk en anlægsomposteringskladdetype, første gang du åbner siden **Anlægsompost.kladde**, men du kan definere andre omposteringskladdetyper. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsompost.kladdetype**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>Sådan defineres anlægsomposteringskladdenavne (valgfrit)

Du kan angive flere kladdenavne, som er individuelle kladder for hver omposteringskladdetype. En medarbejder kan f.eks. have sin egen omposteringskladde, hvor medarbejderens initialer anvendes som omposteringskladdenavn. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsompost.kladdetype**, og vælg derefter det relaterede link.  
2. Markér den relevante kladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Anlægsompost.kld.navne** skal du udfylde felterne efter behov.

## <a name="see-also"></a>Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Oversigt over anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
