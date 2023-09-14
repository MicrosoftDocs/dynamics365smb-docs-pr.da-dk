---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2022
ms.author: bholtorf
---
[!INCLUDE[prod_short](prod_short.md)]-brugere understøtter undertiden mere end én afdeling eller underorganisation i en koncernvirksomhed. F.eks. kan en virksomhed have salgskontorer i flere og lande/områder, så den har oprettet en separat afdeling for hvert kontor. De kontorer, der befinder sig i samme land/område, oprettes som separate *virksomheder* i et delt *miljø*. Andre kontorer oprettes som virksomheder i separate miljøer, fordi de er geografisk baseret i andre lande/områder.

- Hvad er en virksomhed?

  En *virksomhed* skal opfattes som en beholder, der indeholder oplysninger om en juridisk enhed. Hvis du bruger eksemplet ovenfor, har firmaet et salgskontor i Seattle og et andet i New York, så det opretter en virksomhed i [!INCLUDE[prod_short](prod_short.md)] for hvert kontor, så det kan håndtere operationer for hvert kontor separat.

- Hvad er et miljø?

  Virksomheder i [!INCLUDE[prod_short](prod_short.md)] online findes i det, der kaldes *miljøer*. Der findes to typer miljøer, **Produktion** og **Sandkasse**. Kort sagt indeholder produktionsmiljøer live forretningsdata, og sandkassemiljøer bruges som et sikkert sted til at afprøve ting som nye forretningsprocesser eller -funktioner. Du kan finde flere oplysninger i [Typer af miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (kun på engelsk). Hvis du har adgang til en virksomhed, har du adgang til det miljø, hvor den er installeret. Hvis du har adgang til mere end én virksomhed, og disse virksomheder er i forskellige miljøer, skal du angive det miljø, du vil arbejde i, når du logger på [!INCLUDE[prod_short](prod_short.md)]. Miljøer er specifikke for et bestemt land/område, så hvis din organisation arbejder i flere lande/områder, skal du bruge separate miljøer for hvert land/område. Du kan finde flere oplysninger i [Miljøer og virksomheder](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (kun på engelsk).
