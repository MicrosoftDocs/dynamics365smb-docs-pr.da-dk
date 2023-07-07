---
title: 'Kør opgaver i baggrunden, og løbende'
description: Konfigurere synkronisering af data mellem Business central og Shopify i baggrunden.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# <a name="run-tasks-in-the-background"></a>Kør opgaver i baggrunden

Det er effektivt at køre nogle opgaver samtidig og på en automatiseret måde. Du kan udføre disse opgaver i baggrunden, og du kan også angive en tidsplan, når opgaverne skal afvikles automatisk. Der understøttes to tilstande for at udføre opgaver i baggrunden:

- Manuelt udløste opgaver planlægges øjeblikkeligt via **Opgavekøposter**.
- Tilbagevendende opgaver er planlagt i **Opgavekøposter**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Udføre opgaver i baggrunden for et bestemt trykkeri

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil køre synkronisering i baggrunden for at åbne **Shopify Butikskort**-siden.
3. Aktivér **Tillad baggrundssynkronisering** til/fra.

Når synkroniseringshandlingen udløses i stedet for en opgave, der kører i forgrunden, bliver du nu bedt om at vente. Når den er fuldført, kan du fortsætte til næste handling. Opgaven oprettes som en **Opgavekøpost** og starter straks.

## <a name="to-schedule-recurring-tasks"></a>Sådan planlægges tilbagevendende opgaver

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Flere oplysninger om at planlægge opgaver under [Opgavekø](../admin-job-queues-schedule-tasks.md).

|Opgave|Objekt|
|------|------------|
|**Synkroniser ordrer fra Shopify**|Rapport 30104 Synkroniser ordrer fra Shopify|
|**Behandle Shopify ordrer**|Rapport 30103 Shopify oprette slagsordrer|
|**Synkroniser forsendelser til Shopify**|Rapport 30109 synkronisering af forsendelse til Shopify|
|**Synkronisere produkter og/eller priser**|Rapport 30108 Shopify synkroniser produkter|
|**Synkroniser lager**|Rapport 30102 Synkroniser lager til Shopify|
|**Synkroniser billeder**|Rapport 30107 Shopify Synkroniser billeder|
|**Synkroniser debitorer**|Rapport 30100 Shopify Synkroniser kunder|
|**Synkroniser betalinger**|Rapport 30105 Shopify Synkroniser betalinger|

> [!NOTE]
> Nogle elementer kan opdateres af flere forskellige opgaver, f.eks. når du importerer ordrer, afhængigt af indstillingen på **Shopify-butikskort**, kan systemet måske også importere og opdatere debitor-og/eller produktdata. Husk at bruge den samme jobkøkategori for at undgå konflikter.

Andre opgaver, der kan være en hjælp til at automatisere behandlingen af salgsdokumenter:

- reportere 297 Massebogfør salgsfakturaer
- rapportere 296 Massebogfør salgsordrer

Du kan bruge **Shopify-ordrenr.** feltet til at identificere de salgsdokumenter, der er indlæst fra Shopify.

Hvis du vil vide mere om bogføring af salgsordrer i en batch, skal du gå til [Oprette en opgavekøpost for massebogføring af salgsordrer](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
