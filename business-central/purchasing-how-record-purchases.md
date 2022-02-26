---
title: Registrere køb med købsfakturaer (indeholder video)
description: Beskriver, hvordan du køber lagervarer, varer, der ikke er på lager, eller ressourcer ved at oprette og bogføre købsfakturaer eller ordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146
ms.date: 09/07/2021
ms.author: edupont
ms.openlocfilehash: 3d634e1ffb34cfdc0e4e7f6fc5e6ad4805cdabb5
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953030"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrere køb med købsfakturaer

Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer og købsordrer også til at opdatere lagerniveauer dynamisk, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer eller ordrer, bidrager til avancebeløb og andre finansielle nøgletal i dit Rollecenter.

## <a name="create-purchase-invoices"></a>Oprette købsfakturaer

Du kan både købe fysiske varer (varetypen **Lager**), som påvirker lagerværdien, og købe tjenester, der repræsenteres af tidsenheder. Du kan enten gøre dette med varetypen **Tjeneste** eller med linjetypen **Ressource**.

Når du modtager lagervarerne, eller når den købte tjeneste er fuldført, skal du bogføre købsfakturaen eller -ordren for at opdatere lager- og finansposter og aktivere betaling til kreditor i henhold til betalingsbetingelserne. Du kan få flere oplysninger i [Bogføring af køb](ui-post-purchases.md) og [Foretage betaling](payables-make-payments.md).

> [!CAUTION]  
> Bogfør ikke en købsfaktura for fysiske varer, før du har modtaget varerne og kender de endelige omkostninger for købet, herunder eventuelle ekstra gebyrer. Ellers kan din lagerværdi og avancetal blive skævt.

### <a name="to-create-a-purchase-invoice"></a>Sådan oprettes en købsfaktura

Følgende afsnit handler om, hvordan du opretter en købsfaktura. Fremgangsmåden er den samme for en købsordre. Den væsentligste forskel er, at købsordrer har yderligere felter og handlinger til fysisk håndtering af varer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.

    Andre felter på siden **Købsfaktura** er nu udfyldt med standardoplysningerne for den valgte kreditor. Hvis kreditoren ikke er registreret, skal du følge disse trin:

    1. I feltet **Kreditor** skal du indtaste navnet på den nye kreditor.
    2. I dialogboksen, hvor du registrerer den nye kreditor, skal du trykke på knappen **Ja**.
    3. Du kan finde flere oplysninger om, hvordan du udfylder kreditorkortet, i [registrere nye kreditorer](purchasing-how-register-new-vendors.md).  
    4. Når du er færdig med kreditorkortet, skal du vælge **OK** for at vende tilbage til siden **Købsfaktura**.

3. Udfylde de resterende felter efter behov på siden **Købsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde købsfakturalinjerne med varer eller ressourcer, som du har købt af kreditoren.

    > [!NOTE]  
    > Hvis du har konfigureret de tilbagevendende købslinjer for kreditoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i fakturaen ved at vælge handlingen **Hent tilbagevendende købslinjer**.
4. I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.
5. Angiv antal varer, der skal købes, i feltet **Antal**.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbet vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på kreditorkortet.

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

6. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i fakturaen.

    > [!NOTE]  
    > Hvis du har konfigureret fakturarabatter til kreditoren, indsættes den angivne procentværdi automatisk i feltet **Leverandørfakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabatbeløb**.
7. Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.

Købet afspejles nu i lagerposter, ressourceposter og finansposter, og kreditorbetalingen aktiveres. Købsfakturaen fjernes fra listen over købsfakturaer og erstattes med et nyt bilag i oversigten over bogførte købsfakturaer.  

> [!NOTE]
> I sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.
>
> Hvis du vil kontrollere de beløb, der faktisk bogføres, kan du bruge siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.

## <a name="when-to-use-purchase-orders"></a>Hvornår skal købsordrer bruges?

Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer. Følgende procedure er baseret på en købsfaktura. Fremgangsmåden er den samme for en købsordre.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="selling-non-inventory-items"></a>Sælge varer, der ikke er lagervarer

Varerne på en købsfaktura kan være af typen **Lager**, **Service**, **Ressource** og **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke opbevares på lageret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md). Købsfakturaprocessen er den samme for alle tre varetyper.

> [!NOTE]
> Du kan også købe eksterne ressourcer med købslinjetypen **Ressource**, f.eks. for at fakturere en kreditor for udført arbejde. Der er flere oplysninger i [Konfigurere ressourcer](projects-how-setup-resources.md).
>
> Hvis du vil bruge en købt ressource, skal du muligvis angive ressourcens kapacitet og knytte den til en sag manuelt. Når en ressource købes, oprettes en ressourcepost, men ressourceposternes antal og værdi spores ikke, ligesom det f.eks. er tilfældet med varer. Hvis antal og værdi skal spores, skal du overveje at bruge andre typer linjeelementer.

## <a name="posted-invoices"></a>Bogførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan nemt rette eller annullere en bogført købsfaktura, før du betaler kreditoren. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen. Du kan finde flere oplysninger i [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varer eller tjenester på den bogførte købsfaktura, skal du oprette en købskreditnota for at tilbageføre købet. Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

[Åbne listen **Bogførte købsfakturaer**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Konfigurere ressourcer](projects-how-setup-resources.md)  
[Bogføring af køb](ui-post-purchases.md)  
[Anmode om tilbud](purchasing-how-request-quotes.md)  
[Købe varer til et salg](purchasing-how-purchase-products-sale.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Forberede direkte leveringer](sales-how-drop-shipment.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]