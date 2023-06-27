---
title: Om Kostprisberegning
description: 'Vide, hvordan kostmetoden og andre faktorer påvirker feltet Kostpris på varekortet.'
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: a-reishima
---
# <a name="about-unit-cost-calculation"></a>Om Kostprisberegning

Hver vare har en kostpris, der er beregnet på basis af virksomhedens kostmetode og andre faktorer. Som regel er værdien i feltet *Kostpris* på varekortet baseret på **standardkostprisen** for varer, der følger standardkostmetoden. For alle andre kostmetoder (*FIFO*, *LIFO*, *specifik* og *gennemsnit*) beregnes kostprisen ud fra den gennemsnitlige kostpris på en tidsperiode.  

Der er flere oplysninger i [Administration af lageromkostninger](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Når kostprisen for enheden opdateres

Den valgte omkostningsmetode påvirkes, når **Kostprisen** er opdateret.

Når kostmetoden er angivet som *standard*, opdateres feltet **Kostpris** hver gang standardkostprisen ændres, og brugerne kan ikke redigere feltet **Kostpris**. Du kan finde flere oplysninger i [Opdatere standardkostpriser](finance-how-to-update-standard-costs.md).

Hvis kostmetoden er *FIFO*, *LIFO*, *Specific* eller *Gennemsnit*, når **Kostprisen** opdateres i følgende tilfælde:

* Når varen kostreguleres automatisk eller vha. en [Reguler kostpris](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Under bogføringen af købsfakturaer, output eller positiv regulering , hvis en af følgende betingelser er opfyldt:
  * Den fakturerede beholdning af varen ændres fra negativ eller nul til positiv.
  * Den aktuelle enhedspris er nul.

Hvis en af disse forudsætninger er til stede, opdateres feltet **Kostprisen** med oplysningerne i feltet **Sidste købspris** for varen.

> [!NOTE]
> Feltet **Kostpris** opdateres ikke, hvis den aktuelle kostpris er højere end nul, og den nye kostpris er nul. En kostpris på nul betragtes som en undtagelse fra den almindelige virksomhed. Derfor bevares den aktuelle kostpris for at levere den sidst kendte, relevante værdi. Denne undtagelse gælder, selvom det eksisterende lager er blevet værdireguleret til nul.

I feltet **Kostpris** på varekortet kan du specificere for at vise en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra siden **Oversigt over beregning af gns. kostpris**.

## <a name="unit-cost-calculation-for-purchases"></a>Beregne kostpris ved køb

Når du køber varer, overføres værdien i feltet **Sidste købspris** på varekortet altid til feltet **Direct Unit Cost** på en købslinje eller til linjen **Pris** på en serviceartikelkladdelinje.

Det, du vælger i feltet **Kostmetode**, har indflydelse på, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner indholdet i felterne **Kostpris** på linjerne.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Kostmetoden FIFO, LIFO, Specifik eller Gennemsnit

[!INCLUDE[prod_short](includes/prod_short.md)] beregner indholdet af feltet **Kostpris RV** på købslinjen og indholdet af feltet **Kostpris** på serviceartikelkladdelinjen beregnes efter følgende formel:

*Kostpris (RV) = (Direkte kostpris - (Fakturarabatbeløb/Antal)) x (1 + Omkostningspct./100) + IPO-bidrag*

### <a name="costing-method-standard"></a>Standardkostmetoden

Feltet **Kostpris (RV)** på købslinjen eller feltet **Kostpris** udfyldes på varekladdelinjen ved at kopiere værdien i feltet **Kostpris** på varekortet. Ved at bruge kostmetoden som *Standard*, er værdien altid baseret på standardkostprisen.

Når du bogfører købet, anvender [!INCLUDE[prod_short](includes/prod_short.md)] kostprisen fra købslinjen eller varekladdelinjen til købsfakturaposten. Den kan ses på varens postoversigt.

### <a name="all-costing-methods"></a>Alle kostmetoder

Programmet bruger altid kostprisen fra kildedokumentlinjen til at beregne indholdet af feltet **Kostbeløb faktisk**, eller hvis det er relevant, feltet **Kostbeløb forventet** i forbindelse med denne post, uanset hvilken kostmetode der anvendes for varen.

## <a name="unit-cost-calculation-for-sales"></a>Beregne kostpris ved salg

Når du sælger varer, overføres kostprisen altid fra feltet **Kostpris** på varekortet til salgslinjen eller serviceartikelkladdelinjen.

Når du bogfører overføres kostprisen til salgsfakturaposten, og den kan ses på varens postoversigt. [!INCLUDE[prod_short](includes/prod_short.md)] bruger kostprisen fra kildedokumentlinjen til beregne indholdet af feltet **Kostbeløb faktisk** eller, hvis det er relevant, feltet **Kostbeløb forventet** i den værdipost, der er forbundet med denne varepost.

## <a name="see-also"></a>Se også

[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Om lagerkostmetode](finance-learn-about-costing.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Konfigurere bedste fremgangsmåder: kostmetode](setup-best-practices-costing-method.md)  
[Designoplysninger: Kostmetoder](design-details-costing-methods.md)  
[Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
