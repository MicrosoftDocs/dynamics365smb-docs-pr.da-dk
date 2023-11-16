---
title: Definere lagermedarbejdere
description: 'Hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder, der er tildelt én standardlokation og evt. flere ikke-standardlokationer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees"></a>Konfigurere lagermedarbejdere

Du skal konfigurere hver bruger, som udfører lageraktiviteter, skal være defineret som en lagermedarbejder og tildele en standardlokation. [!INCLUDE [prod_short](includes/prod_short.md)] filtrerer lageraktiviteter til medarbejderens standardplacering. De kan kun udføre lageraktiviteter på lokationen. Du kan også tildele en bruger på andre lokationer. De kan få adgang til, men ikke udføre aktiviteter på disse placeringer.

## <a name="to-set-up-warehouse-employees"></a>Sådan defineres lagermedarbejdere

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Vælg feltet **Bruger-ID**, og vælg derefter brugeren, der skal tilføjes som lagermedarbejder. Vælg knappen **OK**.  
4. Angiv i feltet **Lokationskode** koden for den lokation, hvor brugeren skal arbejde.  
5. Aktiver til/fra-feltet **Standard** for at definere lokationen som den eneste lokation, hvor medarbejderen kan udføre lageraktiviteter.  
6. Gentag disse trin for at tildele andre medarbejdere til lokationer eller for at tildele andre lokationer til eksisterende lagermedarbejdere.  

> [!TIP]
> Du kan også bruge handlingen **Tilføj mig som lagermedarbejder** til hurtigt at føje dig selv til listen over lagermedarbejdere. Dette er f.eks. nyttigt, når du tester funktionerne.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definere politik til bogføring af faktura for brugere](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
