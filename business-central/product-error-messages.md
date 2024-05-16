---
title: Advarsler og fejlmeddelelser
description: 'Få mere at vide om, hvordan du kan foretage fejlfinding og finde løsninger på fejlmeddelelser, når du arbejder i Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# <a name="warnings-and-error-messages"></a>Advarsler og fejlmeddelelser

Mens du arbejder, kan du få vist meddelelser i [!INCLUDE [prod_short](includes/prod_short.md)] om, at noget gik galt, eller at det f.eks. ikke var muligt at bogføre noget. I mange tilfælde gør meddelelsen det nemt at løse problemet, eller du kan annullere de ændringer, du har foretaget. I andre tilfælde har du måske ikke de oplysninger, du skal bruge for at fjerne blokeringen. Denne artikel giver tip til, hvordan du kommer videre.  

## <a name="in-product-user-assistance"></a>Hjælp til brugere i produktet

Standardversionen af [!INCLUDE [prod_short](includes/prod_short.md)] indeholder beskrivelser af de fleste felter, kolonner og handlinger, som du kan få vist ved at vælge navnet. I kombination med undervisningstip for vigtige sider, beskrivende billedtekster og instruktioner er disse værktøjstip eller billedforklaringer vores nuværende implementering af *integreret brugerhjælp*, som er et vigtigt princip inden for moderne softwaredesign.  

Hvis du har et spørgsmål om et felt eller et andet element på brugergrænsefladen, skal du vælge navnet for at læse en kort beskrivelse. Vælg linket **Spørg Copilot**, hvis det ikke er tilstrækkeligt. Du kan også bruge ruden i produkthjælp til at finde svar på dine spørgsmål.  

Du kan finde flere oplysninger i [Dynamics 365 Business Central-modelle til brugerhjælp](/dynamics365/business-central/dev-itpro/user-assistance) i administrationen for [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="help-and-support-page"></a>Siden Hjælp og support

Menupunktet Hjælp i [!INCLUDE[prod_short](includes/prod_short.md)], (spørgsmålstegnet i øverste højre hjørne) giver dig adgang til siden **Hjælp og support**, hvor du kan finde links til ressourcer, der kan besvare dine spørgsmål. Du kan finde flere oplysninger i [Ressourcer til hjælp og support](product-help-and-support.md).  

## <a name="help-others"></a>Hjælpe andre

Hvis du er administrator eller superbruger, kan du hjælpe andre ved at søge efter fejlmeddelelser på siden **Registrering af fejlmeddelelser** eller i administrationen. I mange tilfælde vises en advarsel eller fejlmeddelelse om opsætningen eller manglende tilladelse og lignende problemer, som superbrugeren eller administratoren nemt kan få hjælp til. I andre tilfælde kan det være nødvendigt at undersøge sider for at identificere årsagen. Du kan finde flere oplysninger i [Finde tekniske oplysninger](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) i administrationen for [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="share-error-details-for-faster-assistance"></a>Del fejloplysninger for at få hurtigere hjælp

Brug kollegers eller fageksperters ekspertise til at overvinde forhindringer og minimere nedetid. Når du er blokeret af en fejl, kan du nemt dele fejloplysningerne, når du får hjælp.

Oplysningerne omfatter fejlmeddelelsen, fejlkoden og andre oplysninger, der er nyttige ved fejlfinding af en fejl. Ved at dele fejloplysningerne kan du effektivt beskrive det specifikke problem, du står over for, hvilket hjælper dine kolleger med at hjælpe dig.  

Du kan kopiere detaljer ved at vælge **ikonet Del** i indbyggede valideringsdialogbokse eller i menuen **Del detaljer** i fejldialogbokse.  

Ud over at kopiere fejloplysninger kan du også vælge at dele detaljer via Microsoft Teams ved at vælge **Del detaljer med Teams** for at gøre følgende:

* Kopiere fejldetaljerne.
* Åbn vinduet **Del med Teams**, hvor du kan indsætte de fejloplysninger, du har kopieret, og angive, hvem du vil bede om hjælp. [!INCLUDE [prod_short](includes/prod_short.md)] tilføjer et link til den side, hvor du oplevede fejlen, for at gøre fejlfinding nemmere.

Du kan også vælge at dele oplysninger via mail ved at vælge **Del oplysninger via mail** for at gøre følgende:

* Kopiere fejldetaljerne.
* Åbn din standardmaileditor, hvor du kan indsætte de fejloplysninger, du har kopieret, og angive, hvem du vil bede om hjælp. [!INCLUDE [prod_short](includes/prod_short.md)] tilføjer et link til den side, hvor du oplevede fejlen.

## <a name="help-yourself"></a>Hjælp dig selv

Fejlmeddelelser indeholder oplysninger og handlinger, der gør det nemmere at forstå, gå til og løse fejl, der kommer fra platformen.

De fejlmeddelelser, som [!INCLUDE [prod_short](includes/prod_short.md)]-platformen genererer, indeholder alle tekniske detaljer, herunder feltnavne, i sektionen **Detaljeret fejlmeddelelse**. Vælg ikonet **Kopiér detaljer** for indbyggede valideringsfejl eller i en fejlmeddelelse for at få adgang til de tekniske oplysninger.

Handlinger på fejlmeddelelser fører dig direkte til den side, hvor et felt er skyld i fejlen. Du behøver ikke at bruge tid på at finde siden eller feltet selv. Løs fejlen ved bare at vælge handlingen i fejlmeddelelsen, så fører [!INCLUDE [prod_short](includes/prod_short.md)] dig til det relevante sted for at løse fejlen.

Følgende video viser, hvordan du bruger handlingsrettede fejlmeddelelser til at fjerne blokeringen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### <a name="tip-for-developers"></a>Tip til udviklere

Hvis du er udvikler, og du kalder metoden [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method)-metoden, men ikke overfører objektet |`ErrorInfo`, genererer [!INCLUDE [prod_short](includes/prod_short.md)] automatisk et link til en side, hvor en bruger kan løse problemet. [!INCLUDE [prod_short](includes/prod_short.md)] henter først opslags- eller specifikationssiden for posten og finder derefter kortsiden eller opslagssiden og tilføjer et navigationslink til kortsiden. [!INCLUDE [prod_short](includes/prod_short.md)] tilføjer ikke et link i følgende situationer:

* Hvis fejlen findes på den side, der aktuelt er åben.
* Hvis brugeren ikke har tilladelse til at ændre den underliggende post.

## <a name="see-also"></a>Se også

[Ressourcer til hjælp og support](product-help-and-support.md)  
[Ofte stillede spørgsmål](across-faq.yml)  
[Ofte stillede spørgsmål om Fortæl mig](ui-search-faq.md)  
[Ofte stillede spørgsmål om søgning og filtrering](ui-search-filter-faq.yml)  
[Ofte stillede spørgsmål om kopiering og indsætning](faq-copy-paste.yml)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Blive køreklar](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
