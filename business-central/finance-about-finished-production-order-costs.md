---
title: Om de færdige produktionsomkostninger
description: 'Når produktionsordren afsluttes, er nøglen til at udføre en produktions vares efterkalkulerede levetid. De endelige omkostninger beregnes i kørslen Reguler kostværdi-vareposter.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="about-finished-production-order-costs"></a>Om de færdige produktionsomkostninger

Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres. Endelige omkostninger, inklusive afvigelser i et standardkostprismiljø, faktiske omkostninger i et FIFO-, gennemsnits- eller LIFO-kostprismiljø, beregnes vha. kørslen **Juster kostpris – vareposter**, der gør det muligt at udføre en økonomisk afstemning af de omkostninger, der er forbundet med produktionen af varer. En produktionsordre kan kun indgå i en kostregulering, hvis dens status er **Færdig**. Derfor er det afgørende, at produktionsordrens status ændres til **Færdig**, når varerne er færdigproducerede.  

## <a name="example"></a>Eksempel

Hvis du forbruger materiale for at producere en vare i et standardkostprismiljø, vil varens kostpris plus arbejdskraft og omkostninger indgå i det igangværende arbejde. Når varen er fremstillet, reduceres mængden af igangværende arbejde til standardkostprisen for varen. Disse omkostninger giver typisk ikke nul tilsammen. For at disse omkostninger skal give nul tilsammen, skal du udføre kørslen **Juster kostpris – vareposter** og være opmærksom på, at det kun er produktionsordrer med statussen **Færdig**, der kommer i betragtning ved regulering.  

## <a name="see-also"></a>Se også

[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
