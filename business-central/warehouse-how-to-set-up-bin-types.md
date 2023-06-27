---
title: Configurer des types d’emplacement
description: 'Affectez des types et des activités de flux de base aux emplacements et, ce faisant, définissez la manière dont les emplacements sont utilisés pour des activités d’entrepôt particulières.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-bin-types" />Configurer des types d’emplacement

Vous pouvez diriger la circulation des articles vers les emplacements que vous avez définis pour des activités entrepôt particulières. Vous attribuez à chaque emplacement des activités circulation de base, et définissez de cette façon la manière dont un emplacement est utilisé, en lui affectant un type.  

Il existe six types. Votre entrepôt peut fonctionner avec la totalité de ces six types d’emplacement, mais vous pouvez également décider de n’utiliser que les types RECEPT., RANGPRELEV., EXPED. et CQ. Ces quatre types d’emplacement permettent à des propositions relatives à la prise en charge de la circulation des articles d’être effectuées et vous permettent d’enregistrer les différences de stock.  

## <a name="to-set-up-the-bin-types-you-want-to-use" />Pour configurer les types d’emplacement que vous souhaitez utiliser

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Types d’emplacement**, puis sélectionnez le lien associé.  
2.  Sur la page **Types emplacement**, créez un code à 10 caractères pour chaque type d’emplacement.  
3.  Sélectionnez les activités qui peuvent être effectuées avec chaque type d’emplacement.  

> [!NOTE]  
>  Les types d’emplacement ne sont applicables qu’en cas d’utilisation d’un prélèvement et d’un rangement suggérés dans le magasin.  

Le type d’emplacement ne définit que la manière dont un emplacement donné est utilisé lors du traitement de la circulation des articles dans l’entrepôt. Vous pouvez toujours remplacer les propositions d’un document entrepôt, et vous pouvez également placer ou prendre des articles dans un emplacement en réalisant un mouvement entrepôt.  

Les types d’emplacement que vous pouvez créer sont répertoriés ciaprès.  

|Type emplacement|Désignation|  
|------------------|---------------------------------------|  
|RECEPTION|Les articles enregistrés en tant que réceptions enregistrées, mais pas encore rangés.|  
|EXPED.|Les articles prélevés pour des lignes expédition entrepôt, mais pas encore validés en tant qu’articles expédiés.|  
|RANG.|Généralement, les articles devant être stockés dans de grandes unités, mais auxquels vous ne souhaitez pas accéder à des fins de prélèvement. Étant donné que ces emplacements ne sont pas utilisés pour le prélèvement, que ce soit pour des ordres de fabrication ou des expéditions, l’utilisation d’un emplacement de type Rangement risque d’être limitée, mais ce type d’emplacement peut se révéler utile si vous avez acheté une grande quantité d’articles. La priorité emplacement des emplacements de ce type doit toujours être peu élevée. Ainsi, lors du rangement des articles reçus, ce sont les emplacements RANGPRELEV. de priorité plus élevée associés à l’article concerné qui sont utilisés. Lorsque vous utilisez ce type d’emplacement, vous devez régulièrement procéder au réapprovisionnement des emplacements, afin que les articles stockés dans ces emplacements puissent également être disponibles dans les emplacements de type RANGPRELEV. ou PRELEV.|  
|PRELEV.|Les articles devant être utilisés uniquement pour des prélèvements (par exemple, des articles dont la date d’expiration est proche et que vous avez déplacés dans ce type d’emplacement). Attribuez un classement élevé à ces emplacements afin qu’ils soient proposés en premier pour le prélèvement.|  
|RANGPRELEV.|Articles dans des emplacements qui sont proposés à la fois pour les fonctions de rangement et de prélèvement. Les emplacements de ce type ont vraisemblablement un classement différent. Vous pouvez configurer vos emplacements de stockage en vrac comme ce type d’emplacement avec un classement peu élevé par rapport à vos emplacements prélèvement ordinaires ou vos emplacements prélèvement en aval.|  
|CQ|Cet emplacement est utilisé pour des ajustements stock, si vous le spécifiez sur la fiche magasin dans le champ **Code empl. ajustement**. Vous pouvez également configurer des emplacements de ce type pour des articles défectueux ou en cours de contrôle. vous pouvez déplacer des articles vers ce type d’emplacement afin que la circulation habituelle des articles ne puisse pas y accéder.<br /><br /> **REMARQUE :** contrairement à tous les autres types d’emplacement, les cases à cocher pour le traitement des articles sont toutes désactivées par défaut pour le type **CQ**. Cela signifie que tout contenu que vous placez dans un emplacement de type CQ est exclu des flux d’articles.|  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/set-up-zones-bins/) associée

## <a name="see-also" />Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
