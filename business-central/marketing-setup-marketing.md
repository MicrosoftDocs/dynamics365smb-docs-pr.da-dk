---
title: Konfigurere marketing- og kontaktadministrationsoplysninger | Microsoft Docs
description: Du kan konfigurere marketing- og kontaktadministration i Business Central for at optimere relationer med kundeemner eller kunder og forbedre kampagner og salgsfremstød.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 02/26/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: e2fa7fc0c5f2e89f592dca84a89e5e5f551b0d28
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792319"
---
# <a name="setting-up-relationship-management"></a>Opsætning af Relationsstyring
Før du begynder arbejde med dine kontakter og marketinginteresser, er der nogle beslutninger og trin, der skal tages for at definere, hvordan bestemte aspekter af kontakter skal håndteres marketingområdet. F.eks. kan du bestemme, om kontaktkortet skal synkroniseres med debitorkortet, kreditorkortet og bankkontokortet, hvordan nummerserier defineres, eller hvad standardhilsenen skal være, når du skriver til dine kontakter.

Når du administrerer dine kontaktpersoner og har en strategi på plads, så du kan identificere, tiltrække og holde på kunderne, er det med til at optimere din virksomhed og øge kundetilfredsheden. Et godt system til styring af kontaktpersoner er desuden en hjælp, når du skal oprette og vedligeholde relationer med kunderne. Kommunikation er nøglen til disse relationer. Hvis firmaer skal have succes, er det vigtigt, at de kan tilpasse kommunikationen efter mulige og eksisterende kunder, leverandører og forretningspartnere efter disses behov. Oprettelse af en strategi og definition af, hvordan din virksomhed anvender kontaktoplysninger er et primært trin. Disse oplysninger skal vises for mange forskellige grupper i virksomheden, så et godt system hjælper alle med at blive mere produktive.

Du kan konfigurere marketing og administration af kontakter fra siden **Marketingopsætning**. Når du vil åbne siden **Marketingopsætning**, skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Marketingopsætning** og derefter vælge det relaterede link.

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Kopiere bestemte oplysninger automatisk fra kontaktvirksomheder til kontaktpersonerne
En del af virksomhedsoplysningerne er identiske med oplysningerne om de kontaktpersoner, som arbejder i virksomhederne, f.eks. adresseoplysningerne. I sektionen **Overførte oplysninger** på siden **Marketingopsætning** kan du indstille programmet til automatisk at kopiere bestemte felter fra kontaktvirksomhedskortet til kontaktkortet, hver gang du opretter en kontakt for en virksomhed. F.eks. kan du vælge at kopiere sælgerkode, adresseoplysninger (adresse, adresse 2, by, postnummer og region), kommunikationsoplysninger (telefaxnummer, tilbagesvar og telefonnummer) og mere.

Hvis du ændrer et af disse felter på virksomhedskortet, ændres det tilsvarende felt på kontaktkortet automatisk, medmindre du har ændret feltet på kontaktkortet manuelt.

Du kan finde flere oplysninger under [Oprette kontaktpersoner](marketing-how-create-contact-persons.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Bruge foruddefinerede standarder på de nye kontakter
Du kan vælge, at der automatisk skal tildeles bestemte standardværdier for sprogkode, distriktskode, sælgerkode og lande-/områdekode til hver ny kontakt, du opretter. Du kan også angive en standardværdi for salgsproceskode, som automatisk tildeles hvert nyt lead.

Ved kopieringen af felter overskrives de standardværdier, du har defineret. Hvis du f.eks. har angivet dansk som standardsprog, men kontaktvirksomhedens sprog er tysk, bliver sprogkoden for de kontaktpersoner, som er registreret for virksomheden, også tysk.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Automatisk registrere interaktioner
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan registrere salgs- og købsdokumenter automatisk som interaktioner (for eksempel ordrer, fakturaer, kvitteringer osv.) samt mails, telefonopkald og følgebreve.

Du kan finde flere oplysninger i [Automatisk registrere interaktioner med kontakter](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Synkronisere kontakter med debitorer m.m.
Du skal vælge en forretningsrelationskode for debitorer, kreditorer og bankkonti, hvis du vil synkronisere kontaktkortet med disse. Du kan f.eks. kun knytte en kontakt til en eksisterende debitor, hvis du har valgt en forretningsrelationskode for debitoren på siden **Marketingopsætning**.

Du kan finde flere oplysninger under [Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts/Synchronizing Contacts With Customers, Vendors, and Bank Accounts).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Tildele en nummerserie til kontakter og leads
Du kan konfigurere en nummerserie til kontakter og leads. Hvis du har oprettet en nummerserie for kontakter, og du opretter en kontakt og trykker på Enter i feltet Nr. på kontaktkortet, kopieres det næste tilgængelig kontaktnummer automatisk.

Du kan finde flere oplysninger om nummerserier under [Oprette nummerserier](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Søge efter dublerede kontakter, når der oprettes kontakter
Du kan vælge at lade programmet søge automatisk efter dubletter, hver gang du opretter en kontaktvirksomhed, eller du kan vælge at søge manuelt, når du har oprettet kontakten. Du kan også vælge at lade programmet opdatere søgestrenge automatisk, hver gang du har ændret kontaktoplysninger eller oprettet en kontakt. Du kan angive hitprocenten til søgning, dvs. den procentdel identiske strenge som to kontakter skal have, før de betragtes som dubletter.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
