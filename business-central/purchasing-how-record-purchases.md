---
title: Oprette en købsfaktura og registrere indkøb | Microsoft Docs
description: Beskriver, hvordan du køber lager- eller serviceartikler ved at oprette og bogføre købsfakturaer eller ordrer.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 078313bb3f437734b6e52f51b6d6512ebf09f1df
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881422"
---
# <a name="record-purchases"></a>Registrere køb
Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer og købsordrer også til at opdatere lagerniveauer dynamisk, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer eller ordrer, bidrager til avancebeløb og andre finansielle nøgletal i dit Rollecenter.

> [!NOTE]  
>   Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer. Følgende procedure er baseret på en købsfaktura. Fremgangsmåden er den samme for en købsordre.

Når du modtager lagervarerne, eller når den købte service er fuldført, skal du bogføre købsfakturaen eller -ordren for at opdatere lager- og finansrecords og aktivere betaling til kreditor i henhold til betalingsbetingelserne. Du kan finde flere oplysninger under [Foretage betalinger](payables-make-payments.md).

> [!CAUTION]  
>   Bogfør ikke en købsfaktura, før du modtager varerne og kender de endelige omkostninger for købet, herunder eventuelle yderligere udgifter. Ellers kan din lagerværdi og avancetal blive skævt.

Du kan nemt rette eller annullere en bogført købsfaktura, før du betaler kreditoren. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen. Du kan finde flere oplysninger under [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varer på den bogførte købsfaktura, skal du oprette en købskreditnota for at tilbageføre købet. Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

Varekortet kan være af typen **Lager**, **Service** og **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke opbevares på lageret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md). Købsfakturaprocessen er den samme for alle tre varetyper.

Du kan udfylde kreditorfelter i købsfakturaen på to måder, afhængigt af om debitoren er registreret.
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt]

## <a name="to-create-a-purchase-invoice"></a>Sådan oprettes en købsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.

    Andre felter på siden **Købsfaktura** er nu udfyldt med standardoplysningerne for den valgte kreditor. Hvis kreditoren ikke er registreret, skal du følge disse trin:
3. I feltet **Kreditor** skal du indtaste navnet på den nye kreditor.
4. I dialogboksen, hvor du registrerer den nye kreditor, skal du trykke på knappen **Ja**.
5. På siden **Vælg en skabelon til en ny kreditor** skal du vælge en skabelon, som det nye kreditorkort skal baseres på, og derefter vælge knappen **OK**.
6. Et nyt kreditorkort åbnes, udfyldt med oplysninger om den valgte kreditorskabelon. Feltet **Navn** udfyldes på forhånd med den nye kreditors navn, som du har angivet på købsfakturaen.
7. Fortsæt med at udfylde resten af felterne på kreditorkortet. Du kan finde flere oplysninger i [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).  
8. Når du er færdig med kreditorkortet, skal du vælge **OK** for at vende tilbage til siden **Købsfaktura**.

    Flere felter på siden **Købsfaktura** udfyldes med de oplysninger, som du angav på det nye kreditorkort.
9. Udfylde de resterende felter efter behov på siden **Købsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde købsfakturalinjerne med lagervarer eller services, som du har købt af kreditoren.

    > [!NOTE]  
    >   Hvis du har konfigureret de tilbagevendende købslinjer for kreditoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i fakturaen ved at vælge handlingen **Hent tilbagevendende købslinjer**.
10. I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.
11. Angiv antal varer, der skal købes, i feltet **Antal**.

    > [!NOTE]  
    >   For varer af typen **Service** er antallet en tidsenhed, f.eks. timer, der er angivet i feltet **Enhedskode** på linjen.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbet vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på kreditorkortet.

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

    > [!NOTE]
    > I meget sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.<br /><br />Hvis du vil kontrollere de beløb, der faktisk bogføres, kan du bruge siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.

12. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i fakturaen.

    > [!NOTE]  
    >   Hvis du har konfigureret fakturarabatter til kreditoren, indsættes den angivne procentværdi automatisk i feltet **Leverandørfakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabatbeløb**.
13. Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.

Købet afspejles nu i lager- og finansrecords, og kreditorbetalingen aktiveres. Købsfakturaen fjernes fra listen over købsfakturaer og erstattes med et nyt bilag i oversigten over bogførte købsfakturaer.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Anmode om tilbud](purchasing-how-request-quotes.md)  
[Købe varer til et salg](purchasing-how-purchase-products-sale.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Forberede direkte leveringer](sales-how-drop-shipment.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
