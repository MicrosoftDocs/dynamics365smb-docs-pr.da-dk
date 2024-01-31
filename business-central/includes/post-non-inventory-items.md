---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Lagermedarbejdere kan sende og modtage ikke-lagervarer sammen med fysiske varer på salgs- og købsordrer. Ikke-lagerførte varer er immaterielle aktiver, f.eks. forsikring eller ekstraomkostninger.

Salgs- og købsordrer har ofte forskellige typer ting på linjerne. Ordrer kan f.eks. omfatte finansvarer, konti og anlægsaktiver. Hvis du bruger lagerdokumenter til at håndtere fysiske varer, kan du også bogføre visse typer ikke-lagervarer. Der findes følgende eksempler på lagerdokumenter:

* Læg-på-lager-akt. (lager)
* Lagerstedsmodtagelser
* Lagerpluk
* Lagerstedsleverancer

Hvis du vil gøre det muligt for lagermedarbejdere at levere og modtage ikke-lagervarer, skal du udfylde feltet **Bogfør automatisk ikke-lager via lager.** feltet på siderne **Salgsopsætning** og **Købsopsætning**. Der er følgende indstillinger til feltet:

|Indstilling  |Beskrivelse  |
|---------|---------|
|Ingen     |Du må ikke sende eller modtage ikke-lagervarer.         |
|Tilknyttet/tildelt     | Bogføre varegebyrer og andre ikke-lagerførte varelinjer, der er tildelt eller knyttet til fysiske varer. Hvis du vil knytte ikke-lagerrelaterede linjer til fysiske varer, skal du bruge handlingen **Vedhæft til lagerlinje** .        |
|Alle     | Bogføre alle ikke-lagerførte linjer på kildedokumentet, så snart lagerdokumentet har bogført mindst én vare.        |

> [!NOTE]
> Indstillingen **Komplet** i feltet **Afsendelsesadvis** i salgsordren har forrang for valget i feltet **Bogfør automatisk ikke-lager via lager.** feltet på siden **Salgsopsætning**.