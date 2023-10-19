---
title: Registrere nye debitorer ved at oprette debitorkort (indeholder video)
description: 'Beskriver, hvordan du opretter et debitorkort for at registrere oplysninger om hver ny kunde, du sælger til.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: bholtorf
---
# <a name="register-new-customers"></a>Registrere nye debitorer

Debitorer er din kilde til din indtægt. Du skal registrere hver debitor, du sælger til som et debitorkort. Debitorkort indeholder de oplysninger, som er en forudsætning for at sælge produkter til debitoren. Flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).  

Før du kan registrere nye debitorer, skal du oprette forskellige salgskoder, som du kan vælge mellem, når du udfylder debitorkort. Flere oplysninger i [Konfigurere salg](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Tilføje nye debitorer

Du kan tilføje nye debitorer manuelt ved at udfylde felterne på siden **Debitorkort**, eller du kan bruge skabeloner, der indeholder foruddefinerede oplysninger. Du kan f. eks. oprette en skabelon til forskellige typer debitorprofiler. Du kan spare tid ved at bruge skabeloner, når du tilføjer nye debitorer, så oplysningerne bliver korrekte hver gang. 

Hvis du opretter:
* Flere skabeloner til brug mere end én type debitor, kan du vælge den passende skabelon, du vil bruge, når du tilføjer en debitor.
* Kun én skabelon, der vil blive brugt til alle nye debitorer. 

Når du har oprettet en skabelon, kan du bruge handlingen **Anvend skabelon** for at anvende den på en eller flere valgte debitorer. Hvis du vil oprette en skabelon, skal du angive de oplysninger, du vil genbruge, på siden **Kreditorkort** og derefter gemme den som en skabelon. Flere oplysninger i afsnittet [Sådan gemmes debitorkortet som en skabelon](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Det kan være nyttigt at tilpasse siden **Debitorskabeloner**, når du opretter en skabelon. Det kan f.eks. være en god ide at føje feltet **Kreditmaksimum** til en skabelon. Flere oplysninger i [Tilpasse dit arbejdsområde](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode).

Du kan også oprette en debitor ud fra en kontakt. Flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Sådan oprettes et nyt debitorkort

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

**Priser og rabatter** indeholder indstillinger for styring af special priser eller rabatter for en kunde, når en ordre opfylder bestemte kriterier. Eksempler på sådanne kriterier kan være, når de køber en bestemt vare, bestiller et minimum eller køber før en dato, f. eks. når en kampagne afsluttes. Flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

Debitoren er nu registreret, og debitorkortet er klar til at blive brugt i salgsdokumenter.  

### <a name="to-save-the-customer-card-as-a-template"></a>Sådan gemmes debitorkortet som en skabelon

Du kan bruge et debitorkort som skabelon, når du opretter nye debitorkort.

1. På siden **Debitorkort** skal du vælge handlingen **Gem som skabelon**. Siden **Debitorskabelon** åbnes med debitorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for debitoren.
4. Rediger eller angiv dimensionskoder, du vil anvende for nye debitorkort, oprettes ved hjælp af denne skabelon.  
5. Når du har fuldført den nye debitorskabelon, skal du vælge **OK**.

Debitorskabelonen føjes til listen over debitorskabeloner, og du kan bruge den til at oprette nye debitorkort.

## <a name="deleting-customer-cards"></a>Slette debitorkort

Hvis du har bogført en postering for en debitor, kan du ikke slette debitorkortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette debitorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.  

## <a name="managing-credit-limits"></a>Administrere kreditgrænser

Kreditgrænser, saldobeløb og betalingsbetingelser gør det f.eks. muligt for [!INCLUDE [prod_short](includes/prod_short.md)] at udstede kredit og en forfaldsadvarsel, når du behandler en salgsordre. Desuden kan du med rykker- og rentebetingelserne fakturere rente og/eller ekstra opkrævningsgebyrer.  

Feltet **Kreditmaksimum** på debitorkortet angiver det maksimale beløb, som du tillader, at debitoren overskrider betalings saldoen, før der udstedes advarsler. Når du derefter indtaster oplysninger i kladder, tilbud, ordrer og fakturaer, [!INCLUDE [prod_short](includes/prod_short.md)] tester salgshovedet og de enkelte salgslinjer, om kreditmaksimum er overskredet.

Du kan bogføre, selv om kreditgrænsen er overskredet. Hvis ikke feltet udfyldes, betyder det, at der ikke er nogen kreditgrænse for debitoren.  

Du kan vælge ikke at få vist advarsler om, at debitorens kreditmaksimum er overskredet, og du kan angive, hvilke typer advarsel du vil se.

### <a name="to-specify-credit-limit-warnings"></a>Sådan angiver du advarsler om kreditmaksimum

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.

2. I oversigtspanelet **Generelt** i feltet **Kreditmeddelelser** skal du vælge den relevante indstilling som beskrevet i følgende tabel:

    |Indstilling| Description|
    |------|------------|
    |**Begge advarsler**| Både feltet **Kreditmaksimum** og feltet **Forf. beløb** på debitorkortet kontrolleres, og der vises en advarsel, hvis kunden overskrider kreditmaksimum, eller hvis kunden har et forfaldent beløb.|
    |**Kreditmaksimum**|Værdien i feltet **Kreditmaksimum** på debitorkortet sammenlignes med kundens saldo, og der vises en advarsel, hvis kundens saldo overskrider dette beløb.|
    |**Forfaldne beløb**|Feltet **Forf. beløb** på debitorens kort kontrolleres, og en advarsel vises, hvis debitorens saldo er forfalden.|
    |**Ingen advarsel**|Der vises ingen advarsler om debitorens status.|

## <a name="see-also"></a>Se også

[Definere betalingsformer](finance-payment-methods.md)  
[Flette dublerede poster](sales-how-merge-duplicate-records.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Aktivere delleverancer med Afsendelsesadvis](sales-how-send-partial-shipments.md)  
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Bruge online kort til at finde steder og vejledninger](across-online-maps.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
