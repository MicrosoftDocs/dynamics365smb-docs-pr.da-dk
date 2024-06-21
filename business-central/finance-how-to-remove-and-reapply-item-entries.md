---
title: Fjerne og genanvende vareposter
description: 'Du kan få vist og manuelt ændre visse vareudligningsposter, der oprettes automatisk under lagerposteringer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '506, 521, 9125'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="remove-and-reapply-item-ledger-entries"></a>Fjerne og genanvende vareposter
På siden **Udligningskladde** kan du få vist og manuelt ændre visse vareudligningsposter, der oprettes automatisk under lagertransaktioner.  

Når du bogfører en transaktion, hvor varer flyttes ind i eller ud af lageret, oprettes en vareudligning mellem hver lagerforøgelse og lagerreduktion. Disse udligninger bestemmer flowet af omkostninger fra de varer, der modtages på lageret, til de varer, der tages ud af lageret. På grund af den måde som kostprisen beregnes på kan en forkert vareudligning medføre en forkert gennemsnitlig kostpris og en forkert kostpris. Du kan finde flere oplysninger i Designoplysninger: Vareudligning.

Følgende scenarier kræver muligvis, at du fortryder en udligning eller udligner vareposter igen:

- Du har glemt at foretage en fast udligning.
- Du har oprettet en forkert fast udligning.
- Du skal returnere en vare, der allerede er udlignet et salg for.

Brug om muligt et dokument til at udligne en varepost igen. Hvis du f.eks. skal håndtere en købsreturvareordre, hvor salget allerede er udlignet, kan du udligne igen ved at oprette og bogføre købsreturvareordredokumentet ved hjælp af den korrekte udligning i feltet **Udl.varepostløbenr.** på købsreturvareordrelinjen. Du kan bruge funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** eller funktionen **Kopiér fra dokument** i købsreturvareordredokumentet for at gøre det nemmere. Når du bogfører dokumentet, udlignes vareposten automatisk igen. Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

Hvis du ikke kan bruge et dokument til genudligning, f.eks når du skal rette en fast udligning, skal du bruge siden **Udligningskladde** til at rette en udligning.

> [!Warning]  
> Det er vigtigt at overveje følgende ting, når du arbejder med applikationskladden:
    - Du bør ikke lade udligningsposter være ikke-udlignede i længere perioder, da andre brugere ikke kan behandle elementerne, før du udligner udligningsposterne igen eller lukker siden **Applikationskladde**. Brugere, der forsøger at udføre handlinger, der omfatter en manuelt ikke-udlignet udligningspost modtager følgende fejlmeddelelse: "Du kan ikke udføre denne handling, fordi posterne for vare XXX ikke er udlignede i Applikationskladden af bruger XXX."
    - Du bør kun foretage genudligninger uden for normal arbejdstid, så der ikke opstår konflikter, hvis andre brugere bogfører transaktioner med de samme varer.
    - Når du lukker udligningskladden, udfører [!INCLUDE[prod_short](includes/prod_short.md)] en kontrol for at sikre, at alle poster er udlignet. Hvis du f.eks. fjerner en antalsudligning, men ikke opretter en ny udligning, og du derefter lukker applikationskladden, oprettes en ny udligning. Dette er med til at bevare kostprisen. Hvis du fjerner en fast udligning, oprettes en ny fast udligning dog ikke automatisk, når du lukker kladden. Dette skal du gøre manuelt ved at oprette en ny udligning i kladden.
    - Det er muligt at fjerne udligninger fra mere end en post ad gangen i applikationskladden. Da udligning af poster har indflydelse på hele sættet af poster, der er disponible for udligningen, er det ikke muligt at oprette en udligning for mere end en post ad gangen.
    - Applikationskladden kan ikke foretage en udligning i følgende situationer: Hvis der ikke er nok varer på lageret til udligningen, kan applikationskladden ikke foretage udligningen, når du forsøger at udligne en lagerreduktionspost uden varesporingsoplysninger til en lagerforøgelsespost med varesporingsoplysninger.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Sådan fjernes en vareudligning ved brug af applikationskladden

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udligningskladde**, og vælg derefter det relaterede link.  
2.  Siden **Udligningskladde** åbnes med eksisterende vareposter for alle varer.  
3.  Angiv filtre i oversigtspanelet **Generelt** for at gøre det lettere at finde den varepost, du vil ændre udligningen for.  
4.  Vælg vareposten, og vælg derefter handlingen **Udlignede poster**. Siden **Vis udlignede poster- Udlignede poster** åbner, så den varepost eller -poster, der p.t. er udlignet til den valgte post, bliver vist.  
5.  Vælg den varepost i den anden tabel, hvor du vil fjerne udligningen.  
6.  Vælg handlingen **Fjern udligning**. Dette fjerner den vareudligningspost, der knytter de to vareposter til hinanden, og flytter den til siden **Vis udlignede poster - Udlignede poster**.  
7.  Luk siden **Vis udlignede poster – Udlignede poster**.  

 Feltet **Restantal** for de to vareposter øges med det antal, der ikke længere er udlignet. Den fjernede varepost er nu igen tilgængelig for udligning på siden **Vis udlignede poster – Ikke-udlignede poster**.  

> [!IMPORTANT]  
>  Du bør ikke lade udligningsposter være ikke-udlignede i længere perioder, da andre brugere ikke kan behandle de berørte elementer, før du udligner udligningsposterne igen eller lukker siden **Udligningskladde**. Hvis du forsøger at udføre handlinger, der omfatter en manuelt ikke-udlignet udligningspost, vises følgende fejlmeddelelse:  
>   
>  **Du kan ikke udføre denne handling, fordi poster for vare \<item\> er ikke-udlignede på Udligningskladden af bruger \<user\>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Sådan udlignes en vareudligning igen ved brug af applikationskladden

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udligningskladde**, og vælg derefter det relaterede link.  
2.  Siden **Udligningskladde** åbnes med eksisterende vareposter for alle varer.  
3.  For at udligne poster igen, som har været fjernet, siden kladden blev åbnet, skal du vælge den varepost, som du vil udligne igen og derefter vælge handlingen **Udlign igen**.  

    > [!NOTE]  
    >  Denne udligning af den oprindelige balance sker også automatisk, når du lukker siden **Udligningskladde** .  
4.  Hvis du vil udligne en tilgængelig åben varepost til en anden post, skal du vælge den varepost , du vil udligne. Vælg handlingen **Ikke-udlignede poster**. Siden **Vis udlignede poster – Ikke-udlignede poster** åbnes.  
5.  Vælg en eller flere vareposter, som du gerne vil udligne på den valgte post på siden **Udligningskladde**, og klik derefter på knappen **OK**.  

     Der oprettes en vareudligningspost mellem de to vareposter. Feltet **Restantal** for de to poster reduceres med det udlignede antal.  

    > [!NOTE]  
    >  Hvis du har valgt at lave en udligning, der opretter en uendelig løkke i kostreguleringen, oprettes den udligning, du foreslog, ikke. Dette kan ske, når de oprindelige poster har oprettet en negativ lagerbeholdning. Udligningen foretages ikke. Derfor skal du vælge en anden post til udligningen.  
6.  Hvis feltet **Automatisk omkostningsregulering** er angivet til **Altid** i **Opsætning af lager**, vil programmet automatisk udføre kørslen til omkostningsregulering, når du har udlignet igen. Ellers skal du udføre kørslen **Juster kostpris – vareposter** for at sikre, at alle kostpriser er opdaterede.  

## <a name="see-also"></a>Se også

[Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)   
 [Designoplysninger: Vareudligning](design-details-item-application.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
