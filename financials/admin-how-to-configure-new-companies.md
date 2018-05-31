---
title: Nieuwe bedrijven configureren | Microsoft Docs
description: U kunt een nieuw bedrijf dat u hebt gemaakt configureren en aanpassen. U kunt uw implementatie verder afstellen door de configuratie te voltooien in drie fasen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f99f4f7576e72d1ca0fbc6ecaa51d6c7bc15aa9f
ms.contentlocale: nl-nl
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies"></a>Nieuwe bedrijven configureren
Als u een nieuw bedrijf in uw oplossingimplementatie wilt configureren, volgt u doorgaans drie fasen. In de eerste fase importeert u het configuratiepakket. Dit is een .rapidstart-bestand met de configuratie-informatie. In de tweede fase wijzigt u de configuratiegegevens en past u deze vervolgens toe op uw nieuwe bedrijf. In de laatste fase controleert en corrigeert u fouten.  

Bij de volgende procedures wordt ervan uitgegaan dat u een configuratiepakket hebt gemaakt en opgeslagen. Zie [Een configuratiepakket voorbereiden](admin-how-to-prepare-a-configuration-package.md) voor meer informatie.  

In de volgende procedure wordt ervan uitgegaan dat u uw nieuwe bedrijf hebt geïnitialiseerd en geopend, en dat u zich in het Rolcentrum RapidStart Services-implementatie bevindt.

## <a name="to-import-a-configuration-package"></a>Een configuratiepakket importeren  
1. Open het nieuwe bedrijf in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.  
2. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de actie **Pakket importeren**.  
4. Navigeer naar de locatie waar u het .rapidstart-configuratiepakketbestand hebt opgeslagen, en kies vervolgens de knop **Openen**.  
5. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bedrijfsgegevens** in en klik vervolgens op de gerelateerde koppeling. Voer informatie over het bedrijf in op de bedrijfsgegevenskaart. Neem informatie op, zoals bankgegevens. U kunt ook een logo voor het bedrijf opgeven.  

Alle tabellen die u hebt aangewezen voor opname in het nieuwe bedrijf worden geïmporteerd. Op dit punt kunt u de gegevens van het pakket toepassen op de database of de tabelgegevens aanpassen en wijzigen om te voldoen aan de specificaties van de klant.  

## <a name="to-apply-package-data"></a>Pakketgegevens toepassen  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de tabel waarvoor u gegevens wilt wijzigen en kies vervolgens de actie **Gegevens toepassen**. Kies de knop **Ja** om de toepassing te bevestigen.
3. Ga terug naar het venster **Configuratiewerkblad** om te bevestigen dat de gegevens zich nu in de database bevinden en dat de toepassing is geslaagd, en kies de actie **Databasegegevens**.  

> [!NOTE]  
>  Nadat u gegevens hebt toegepast, kunt u deze alleen bekijken in de database. Ze bevinden zich niet langer in het pakket.  

## <a name="to-modify-and-apply-package-data"></a>Pakketgegevens wijzigen en toepassen  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de tabel waarvoor u gegevens wilt wijzigen en kies vervolgens de actie **Pakketgegevens**.  
3. Breng uw wijzigingen aan in het venster **Pakketrecords voor configuratie**. Zo kunt u bijvoorbeeld opties verwijderen die niet van toepassing zijn.  
4. Kies de actie **Gegevens toepassen** en kies vervolgens de knop **OK**.  
5. Ga terug naar het venster **Configuratiewerkblad** om te bevestigen dat de gegevens zich nu in de database bevinden en dat de toepassing is geslaagd, en kies de actie **Databasegegevens**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Een configuratiefout zoeken en identificeren  
Er zijn bepaalde typen fouten die kunnen optreden wanneer u gegevens toepast op een database. De meest voorkomende fout is dat vereiste tabellen niet zijn opgenomen. U corrigeert dergelijke fouten in het configuratiewerkblad.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiepakketten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het pakket dat u wilt controleren en kies vervolgens de actie **Bewerken**.  

    Een tabel met fouten wordt gemarkeerd weergegeven. Het aantal pakketfouten wordt weergegeven in het veld **Aantal pakketfouten**.  

3. Kies het veld **Aantal pakketfouten** om het venster **Pakketrecords voor configuratie** te openen, met de lijst met records met fouten.  

### <a name="to-fix-an-error"></a>Een fout corrigeren  
1. Open het bedrijf dat is gebaseerd op uw configuratiepakket.  
2. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Configuratiewerkblad** in en kies vervolgens de gerelateerde koppeling.  
3. Corrigeer fouten, zoals ontbrekende gerelateerde tabellen, in het werkblad.  
4. Voeg de tabellen toe aan het bestaande configuratiepakket of maak een nieuw pakket dat alleen de nieuwe tabellen bevat. Zie [Een configuratiepakket voorbereiden](admin-how-to-prepare-a-configuration-package.md) voor meer informatie.  
5. Open het nieuwe bedrijf waarvoor u de configuratie implementeert.  
6. Importeer het configuratiepakket.  

    > [!NOTE]  
    >  Als u hetzelfde pakket opnieuw importeert, kunt u eventuele gegevenswijzigingen overschrijven die u al hebt aangebracht. Om die reden wilt u wellicht nieuwe tabellen toevoegen aan een nieuw pakket en in plaats daarvan dit importeren.  

7. Pas de gegevens op de database toe, zoals in het gedeelte "Pakketgegevens wijzigen en toepassen" is beschreven.

## <a name="see-also"></a>Zie ook  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
