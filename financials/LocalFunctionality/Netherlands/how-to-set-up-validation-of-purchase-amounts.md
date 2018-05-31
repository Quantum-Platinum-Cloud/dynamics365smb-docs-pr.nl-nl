---
title: Validatie van inkoopbedragen instellen
description: In Finance and Operations, Business edition kunt u de functie **Totaalbedragen documenten controleren** activeren om het totaalbedrag van inkoopdocumenten te valideren voordat een inkoopfactuur en inkoopcreditnota worden geboekt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8855584a8c7f2d3c8126862bdef19b86e35be5a6
ms.contentlocale: nl-nl
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-validation-of-purchase-amounts"></a>Validatie van inkoopbedragen instellen
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u de functie **Totaalbedragen documenten controleren** activeren om het totaalbedrag van inkoopdocumenten te valideren voordat een inkoopfactuur en inkoopcreditnota worden geboekt. Standaard wordt het totale inkoopdocumentbedrag gevalideerd wanneer u boekt. Het totale bedrag van de ingevoegde inkoopregels moet gelijk zijn aan het bedrag inclusief btw en het btw-bedrag. Als u het inkoopdocumentbedrag automatisch wilt valideren, moet u het documentbedrag inclusief btw en de btw van het documentbedrag in het venster **Inkoopfactuur** of **Inkoopcreditnota** invoeren.  

Als u slechts één inkoopregel of meer verkoopregels met hetzelfde btw-percentage hebt, wordt de juiste documentbedrag-btw automatisch berekend wanneer u de inkoopregels en het documentbedrag inclusief btw invoegt. Als u verschillende inkoopregels met verschillende btw-percentages hebt, moet de waarde van de documentbedrag-btw handmatig worden gewijzigd.  

U kunt ook bepalen wanneer de documenttotaalbedragen en de totaalbedragen van de ingevoegde inkoopregels verschillen. U kunt de optie **Totale op inkoopfactuur/CR-nota weergeven** activeren om het volgende weer te geven in de ingevoegde inkoopregels:  

- Totaalbedrag  
- Totaalbasisbedrag  
- Totaal btw-bedrag  
- Totaalbedrag incl. btw  

De berekende bedragen worden weergegeven in de inkoopfactuur of de inkoopcreditnota. Standaard wordt dit totaalbedrag niet weergegeven.  

U kunt deze optie alleen inschakelen als de inkoopfactuur of de inkoopcreditnota het volgende heeft:  

- Een minimum van één inkoopregel.  
- Het aantalveld opgegeven.  

## <a name="to-set-up-validation-of-total-amounts-for-purchase-documents"></a>Validatie van totaalbedragen voor inkoopdocumenten instellen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul in het sneltabblad **Algemeen** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Totale op inkoopfactuur/CR-nota weergeven.**|Selecteren om de totalen opnieuw te berekenen van alle inkoopfacturen en creditnota's. Dit kan een tijdrovend proces zijn, afhankelijk van het aantal documenten dat moet worden herberekend.|  
    |**Totaalbedragen documenten controleren**|Selecteren om de velden **Documentbedrag incl. btw** en **Btw documentbedrag** in de vensters **Inkoopfactuur** en **Inkoopcreditnota** te wijzigen.|  

3.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
[Nederlandse lokale functionaliteit](netherlands-local-functionality.md)  
[Inkopen instellen](../../sales-how-work-standard-lines.md)
