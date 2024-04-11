---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!IMPORTANT]
> Når du ændrer når-hændelsen for et trin i arbejdsprocessen, ændres så-svarene også. Nogle gange henviser så-svar fra andre når-hændelser til disse så-svar som det næste trin i arbejdsgangen. Når du har ændret en når-hændelse, skal du kontrollere, at de næste trin for dens så-hændelser er korrekte.  
>
> Skabelonen til arbejdsgangen **Godkendelsesworkflow for kreditor** har f.eks. den primære når-hændelse **Der anmodes om godkendelse af en kreditor**. Denne når-hændelse har så-svaret **Send godkendelsesanmodning for posten, og opret en notifikation**, som andre så-svar refererer til. Hvis du ændrer den primære når-hændelse **Der anmodes om godkendelse af en kreditor** til f.eks. **En kreditorpost er ændret**, ryddes så-svaret sammen med referencerne.
>
> Så-svarene for når-hændelserne **En godkendelsesanmodning er delegeret** og **En godkendelsesanmodning er godkendt** (med **På betingelse** angivet til **Afventende godkendelser >0**) er eksempler på, hvor ændring af en primær når-hændelse kan forårsage problemer. Deres så-svar har derefter et næste trin, der refererer til så-svaret **Send godkendelsesanmodning for posten, og opret en meddelelse** for når-hændelsen **Der anmodes om godkendelse af en kreditor**. Da så-svaret for når-hændelsen **Der anmodes om godkendelse af en kreditor** ikke længere er tilgængeligt, fungerer de tilsigtede når-hændelser ikke som forventet.
>
> Du skal angive de næste trin for så-svarene for de når-hændelser, der henviste til den ændrede når-hændelse.