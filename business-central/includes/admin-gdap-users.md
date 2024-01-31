---
author: brentholtorf
ms.topic: include
ms.date: 05/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Du vil muligvis kunne se andre brugere på listen over **Brugere**, der ikke tilhører dem fra din egen virksomhed. Når en gruppe, der er delegeret af en partnervirksomhed, logger ind i et [!INCLUDE [prod_short](prod_short.md)]-miljø på vegne af sin kunde, oprettes de automatisk som en bruger i [!INCLUDE [prod_short](prod_short.md)]. På den måde registreres de handlinger, der udføres af en administrativ administrator, [!INCLUDE [prod_short](prod_short.md)] f.eks. bogføring af dokumenter, og som er knyttet til deres bruger-id.  

Med *detaljeret uddelegerede administratorrettigheder (GDAP)*, vises brugeren på listen **Brugere** og kan tildeles alle tilladelser. De vises ikke med navn og andre personlige oplysninger, men har deres virksomhedsnavn og et entydigt ID. Både interne og eksterne administratorer kan se disse brugere på listen **Brugere**, og de har fuld gennemsigtighed for, hvad disse brugere gør f.eks. i [ændringsloggen](../across-log-changes.md). Men de kan ikke se brugerens faktiske navn. GDAP-brugere vises med brugernavne i følgende format: `User123456@partnerdomain.com`. De kan have et Brugernavn, der afspejler partnerens firmanavn, og e-mail-adressen er ikke personens aktuelle e-mail-adresse. På den måde viser GDAP brugerkonti ikke personlige oplysninger. Hvis du har brug for at finde ud af, hvem der befinder sig bag et sådant pseudonym, skal du kontakte den virksomhed, som denne bruger arbejder på eller har arbejdet for.  
