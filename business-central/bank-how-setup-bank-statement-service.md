---
title: Konfigurere Yodlee Bank Feeds
description: Du kan konvertere betalingsoplysninger til ethvert dataformat, som din bank kræver, og aktivere eksporten eller importen af bankfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.search.form: 1280, 1290
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 325ac8b5e1cd0be6909fe80ab6d073be914d33b9
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973092"
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Konfigurere tjenesten Envestnet Yodlee Bank Feeds

Du kan importere elektroniske bankkontoudtog fra din bank, så du hurtigt kan udfylde siden **Betalingsudligningskladde** og kan udligne betalinger og afstemme bankkontoen. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> På grund af betalingstjenestedirektivet i Europa (PSD2) kan du efter den 14. september 2019 ikke længere automatisk importere bankkontoudtog fra banker i Storbritannien til [!INCLUDE[prod_short](includes/prod_short.md)]. Vi overvejer evt. at tilbyde denne funktion igen i fremtiden.

> [!NOTE]
> Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i onlineversionen af Business Central. Hvis du vil bruge denne funktion i det lokale miljø, skal du anskaffe en cobrand-konto fra Envestnet, og du skal tilføje kode for at integrere med Yodlee-API'en.
>
> Tjenesten Envestnet Yodlee Bank Feeds understøttes kun i USA og Canada.
> Kun banker, der er hjemmehørende i disse lande/områder, understøttes, selvom bankerne fra andre lande/områder kan blive vist i Envestnet Yodlee Bank Feeds-vinduet til bankvalg i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Kontakt Microsoft Support for at få teknisk hjælp til funktionen Envestnet Yodlee. Kontakt ikke Envestnet Yodlee. Du kan finde flere oplysninger i [Konfigurere teknisk support til Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

Tjenesten Envestnet Yodlee Bank Feeds er installeret som en udvidelse af [!INCLUDE[prod_short](includes/prod_short.md)] online og er klar til at blive aktiveret i understøttede lande/områder. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md).

Når du har aktiveret bankfeedtjenesten, skal du knytte en bankkonto til onlinebankkontoen, som feedet kommer fra. Du kan knytte bankkonti til online bankkonti i forskellige følgende scenarier:

* Der findes ikke en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] for din onlinebankkonto. Derfor skal du oprette bankkontoen ved at tilknytte den fra onlinebankkontoen.
* Der findes en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)], som du kan tilknytte en onlinebankkonto.
* Tilknytningen skal fjernes fra en tilknyttet bankkonto, fordi du ikke længere vil bruge bankfeedtjenesten for kontoen.
* Onlinebankkonti er ændret, og du kan opdatere oplysninger om bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)].

Når bankfeedtjenesten er aktiveret, kan du indstille en bankkonto til automatisk at importere nye kontoudtog fra banken til siden **Betalingsudligningskladde** hver anden time. Transaktioner for betalinger, der allerede er bogført som udlignet og/eller afstemt på siden **Betalingsudligningskladde** importeres ikke. Du kan finde flere oplysninger i afsnittet “Sådan aktiveres automatisk import af kontoudtog fra banken”.

> [!NOTE]  
> Hvis du bruger den assisterede opsætningsvejledning Konfigurer virksomhed, udføres nogle af trinnene i følgende procedurer automatisk, når du kommer til opsætning af virksomhedens bankkonto. Du kan finde flere oplysninger i [Blive klar til at handle](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>Sådan aktiveres bankfeedtjenesten
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn den bankkonto, som du vil bruge til bankfeedtjenesten.
3. På siden **Bankkonto** skal du i feltet **Format til import af bankkontoudtog** , vælge YODLEEBANKFEED.  

Bankfeedtjenesten aktiveres, når du knytter en bankkonto til dens relaterede onlinebankkonto. Se den næste fremgangsmåde.  

> [!NOTE]
> Hvis du bruger **Virksomhedsopsætning**-guiden til assisteret opsætning, aktiverer du tjenesten ved at markere afkrydsningsfeltet **Brug en bankfeedtjeneste**. Du kan finde flere oplysninger i [Oprettelse af ny virksomheder i Business Central](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Sådan oprettes en ny tilknyttet bankkonto
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den relevante bankkonto, og vælg derefter **Opret ny tilknyttet bankkonto**. Siden **Tilknytning af bankkonto** åbnes efter et kort øjeblik.

    > [!NOTE]  
    > På denne side vises den faktiske webside for tjenesten Envestnet Yodlee Bank Feeds. Terminologi og funktioner på siden stemmer muligvis ikke overens med de instruktioner, der er angivet i dette emne.  
3. På siden **Tilknytning af online bankkonto** i ruden **Tilknyt konto** skal du bruge søgefunktionen til at finde den bank, hvor du har en eller flere online bankkonti.
4. Vælg bankens navn. Ruden **Log på** åbnes.
5. Angiv det brugernavn og den adgangskode, som du bruger til at logge på onlinebanken, og vælg derefter knappen **Næste**.  
6. Bankfeedtjenesten forbereder at knytte den første onlinebankkonto i den angivne bank til en ny bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Hvis du har mere end én onlinebankkonto i banken, skal du oprette flere bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] for kontiene. Se trin 8 til 10.  

    Når processen er fuldført, vises bankens navn i ruden **Mine konti** på fanen **Tilknyttet**. Tallet i parentes angiver, hvor mange online bankkonti der er tilknyttet.  
7. Vælg knappen **OK**.

    Hvis du kun sammenkæder én onlinebankkonto, åbnes siden **Bankkontokort** og viser navnet på onlinebankkontoen. Hvis det er tilfældet, er processen med at tilknytte bankkontoen fuldført. Nu mangler du kun at konfigurere bankkontoen. Du kan finde flere oplysninger i [Oprette bankkonti](bank-how-setup-bank-accounts.md).

    Hvis du tilknytter mere end én onlinebankkonto, åbnes siden **Tilknytning af bankkonto** og viser de onlinebankkonti, der endnu ikke er knyttet til bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)]. I dette tilfælde skal du følge det næste trin.  
8. På siden **Tilknytning af bankkonto** skal du vælge linjen for en onlinebankkonto og derefter vælge handlingen **Sammenkæd med ny bankkonto**.  

    Siden **Bankkontokort** for en ny bankkonto åbnes og viser navnet på onlinebankkontoen.

    Hvis der findes allerede en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)], som du vil knytte den ekstra onlinebankkonto til, skal du følge næste trin.  
9. På siden **Tilknytning af bankkonto** skal du vælge linjen for en onlinebankkonto og derefter vælge handlingen **Sammenkæd med eksisterende bankkonto**.
10. Brug siden **Bankkontooversigt** til at vælge den bankkonto, som du vil oprette en tilknytning til, og vælg derefter knappen **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Sådan knyttes en bankkonto til en onlinebankkonto
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg linjen for en bankkonto, der ikke er knyttet til en onlinebankkonto, og vælg derefter handlingen **Tilknyt til onlinebankkonto**. Siden **Tilknytning af online bankkonto** åbnes med navnet på banken angivet i ruden **Tilknyt konto**.
3. Vælg bankens navn. Ruden **Log på** åbnes.
4. Angiv det brugernavn og den adgangskode, som du bruger til at logge på onlinebanken, og vælg derefter knappen **Næste**.  

    Bankfeedtjenesten forbereder at knytte din bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] til den relaterede onlinebankkonto.  

    Når processen er fuldført, vises bankens navn i ruden **Mine konti** på fanen **Tilknyttet**. Hvis banken har mere end en bankkonto, knyttes den bankkonto, som du valgte i trin 2.  
5. Vælg knappen **OK**.

På siden **Bankkontooversigt** er afkrydsningsfeltet **Tilknyttet** markeret.

## <a name="to-edit-the-credentials-for-an-online-bank-account"></a>Sådan redigeres legitimationsoplysningerne for en online bankkonto
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.  
2. Vælg linjen for en bankkonto, der ikke er knyttet til en onlinebankkonto, og vælg derefter handlingen **Rediger onlinebankkontooplysninger**.
3. Opdater oplysninger.

## <a name="to-unlink-a-bank-account"></a>Sådan fjernes tilknytningen til en bankkonto
1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.  
2. Vælg linjen for en tilknyttet bankkonto, som du vil fjerne tilknytningen for til den relaterede onlinebankkonto, og vælg derefter handlingen **Fjern tilknytning til onlinebankkonto**.

> [!NOTE]  
> Hvis du vælger **Ja** i bekræftelsesdialogboksen, fjernes tilknytningen til onlinebankkontoen og logondetaljer ryddes. Hvis du vil knytte bankkontoen til onlinebankkontoen igen, skal du logge på banken igen. Du kan finde flere oplysninger i afsnittet “Sådan knyttes en bankkonto til en onlinebankkonto“.

## <a name="to-update-bank-account-linking"></a>Sådan opdateres tilknytning af bankkonto
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den relevante bankkonto, og vælg derefter handlingen **Opdater tilknytning af bankkonto**.

Hvis der er problemer med nogen af de tilknyttede bankkonti på siden **Bankkontooversigt**, åbnes siden **Tilknytning af bankkonto** og angiver, hvilke konti der er problemer med. Problemer kan bedst løses ved at fjerne tilknytningen af onlinebankkontoen og derefter at oprette tilknytningen igen. Du kan finde flere oplysninger i afsnittet "Sådan knyttes en bankkonto til en onlinebankkonto".

## <a name="to-enable-automatic-import-of-bank-statements"></a>Sådan aktiveres automatisk import af kontoudtog fra banken
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg linjen for en tilknyttet bankkonto og vælg derefter handlingen **Opsætning af automatisk import af bankkontoudtog**.
3. På siden **Opsætning af automatisk import af bankkontoudtog** skal du i feltet **Antal dage inkluderet** angive, hvor langt tilbage i tiden, der skal hentes nye banktransaktioner.

    > [!NOTE]  
    > Det anbefales, at du angiver denne værdi til 7 dage eller derover.  
4. Marker afkrydsningsfeltet **Aktiveret**.  

Hver time viser siden **Betalingsudligningskladde** nye betalinger, der foretages på onlinebankkontoen.

> [!NOTE]  
> Transaktioner for betalinger, der allerede er bogført som udlignet og/eller afstemt på siden **Betalingsudligningskladde** importeres ikke.

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]