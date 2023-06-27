---
title: Om montage til ordre og montage til lager
description: 'Få mere at vide om, hvordan du samler varer til salgsordrer eller på lager til senere salg.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Om montage til ordre og montage til lager

[!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt at samle varer på følgende måder:

* Montage til ordre  
* Montage til lager  

## <a name="assemble-to-order" />Montage til ordre

Brug montage til ordre-processen for varer, som du ikke vil have på lager. F. eks. af følgende årsager:

* Du skal tilpasse varerne til kundebehov.
* Du vil minimere omkostningerne til den disponible lagerbeholdning.

På følgende liste beskrives nogle af fordelene ved montage efter ordre-processen:  

* Tilpas montageelementer, når du tager imod en salgsordre.  
* Oversigt over tilgængeligheden af montageelementet og dets komponenter.  
* Reserver montagekomponenter med det samme for at sikre, at ordren kan opfyldes.  
* Bestem rentabiliteten af den tilpassede ordre ved at akkumulere pris og pris.  
* Integreret med lageret for at gøre montage og levering lettere.  
* Montage til ordre, når du opretter et salgstilbud eller en rammesalgsordre.  
* Kombiner lagerantal med montage til ordre-mængder.  

I montage til ordre-processen samler du varer til en salgsordre. Der er en én til en-kæde mellem montageordren og salgsordren.  

Når du indtaster en montage til ordre-vare på en salgsordrelinje, bliver der automatisk oprettet en montageordre. Montageordren er baseret på salgslinjen, og de tilhørende linjer er baseret på varens montagestykliste. Antallet af komponenter på montagestyklisten ganges med ordreantallet. Siden **montage til ordre-linjer** viser detaljer om tilknyttede montageordrelinjer. Du kan bruge oplysningerne til at tilpasse montageelementet. Leveringsdatoen er baseret på tilgængeligheden af varen. Du kan lære mere om montage efter ordre ved at gå til [Sælge varer, der er samlet til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Selvom det ikke er en del af standardprocessen, kan du sælge lagermængder med montage til ordre-mængderne på samme salgsordre. Du kan finde flere oplysninger om at kombinere varer og montage til lager-varer i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

En vare, der er konfigureret til montage efter ordre, når feltet **montagepolitik** på **varekortet** indeholder **montage til ordre**.  

## <a name="assemble-to-stock" />Montage til lager

Bruge montage til lager-processen til varer, som du samler og gemmer til fremtidige salg. Montage til lager-varer er standardvarer, f. eks. pakkede pakker, som du ikke kan tilpasse. Du kan også bruge disse varer som halvfabrikata. Varerne plukkes og behandles som en enkelt vare og behandles som en færdig produktionsvare. Hvis du vil vide mere om montageelementer, skal du gå til [montagevarer](assembly-how-to-assemble-items.md).  

Når du angiver en montage til lager-vare på en salgslinje, behandles varen som alle andre varer fra lageret. Hvis f.eks. [!INCLUDE [prod_short](includes/prod_short.md)] kun kontrollerer tilgængelighed for den monterede vare og ikke dens komponenter.  

> [!NOTE]  
> Selvom det ikke er en del af standardprocessen, kan du montere en vare efter ordre, selvom den er indstillet til montage til lager. Flere oplysninger [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

En vare, der er konfigureret til montage til ordre, når feltet **montagepolitik** på **varekortet** indeholder **montage til ordre**.  

## <a name="combination-scenarios" />Kombinationsscenarier

Når montage til ordre og lagermængder kombineres på en salgsordrelinje, skal montage til ordre-mængder leveres før lagerbeholdning.  

Hvis en montageordre er knyttet til en salgsordrelinje, kopieres værdien i feltet **Mgd. til montage til ordre** på salgsordrelinjen til feltet **Antal til montage** via feltet **Antal** på montageordrehovedet. Lær mere i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)  

Det betyder, at værdien i feltet **Antal til montage** svarer til værdien i feltet **Antal til levering** i salgsordrelinjen. Denne relation styrer, hvordan du leverer delvist og færdig montage til ordre-mængder:

* Når det fulde antal på salgslinjen er monteret efter ordre
* Det gælder også i kombinationsscenarier, hvor en del af den salgslinjeantallet er monteret efter ordre og en del er leveret fra lageret.

Kombinationsscenariet tillader større fleksibilitet i forbindelse med delleverancer. Du kan bruge feltet **Antal til montage** for at angive det antal, der skal leveres delvist fra lageret, og ved montage efter ordre.  

Hvis hele salgslinjemængden skal samles til ordre og leveres, så kopieres værdien i feltet **Levér (antal)** til feltet **Antal til montage** på den tilknyttede montageordre, når du ændrer den mængde, der skal leveres. Dette sikrer, at den mængde, der leveres, leveres fuldstændig af montage til ordre-mængden.  

Men i kombinationsscenarier kopieres den fulde værdi i **Levér (antal)** ikke til feltet **Antal til montage** på montageordrehovedet. I stedet indsættes en standardværdi i feltet **Antal til montage**. Værdien beregnes fra feltet **Levér (antal)** for at sikre, at montage efter ordre-mængderne først bevares.

Hvis du vil afvige fra denne standard, for eksempel fordi du kun vil montere mere eller mindre af mængden i feltet **Levér (antal)**, kan du ændre feltet **Antal til montage**, men kun inden for foruddefinerede regler som illustreret nedenfor.  

Som eksempel på, hvorfor det er klogt at ændre mængden, der skal monteres, er, at du vil bogføre leverancen af lagerbeholdninger delvist, inden montageoutput kan leveres.  

Følgende tabeller forklarer de regler, der definerer de minimale og maksimale værdier, du kan angive i feltet **Antal til montage**, for at afvige fra standardværdi i et kombinationsscenarie. Tabellen viser et kombinationsscenarie, hvor feltet **Lever (antal)** på den tilknyttede salgsordrelinje er ændret fra 7 til 4, og **Antal til montage** er derfor sat til standardværdien 4.  

**Salgsordrelinje**

|                | **Antal** | **Lever (antal)** | **Mgd. til montage til ordre** | **Leveret (antal)** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Oprindelig værdi**| 10          | 7                | 7                             | 0                    |
|**Ændring**      |              | 4                |                               |                      |

**Montageordrehoved**

|                | **Antal** | **Lever (antal)** | **Mgd. til montage til ordre** | **Leveret (antal)** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Oprindelig værdi**| 7           | 7                | 0                             | 7                    |
|**Ændring**      |              | 4 (indsat som standard)|                         |                      |

Baseret på dette eksempel kan du kun ændre feltet **Antal til montage** som følger:  

* Det mindste antal du kan angive er 1. Du skal mindst montere én enhed for at kunne sælge fire enheder, idet de resterende tre antages at være tilgængelig på lageret.  
* Det maksimale antal du kan angive er 4. Denne grænse sikrer, at du ikke samler mere af varen, end du skal bruge til salget.  

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
