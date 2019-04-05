---
title: Comment ranger la production | Microsoft Docs
description: Le mode de rangement de la production dépend du mode de configuration de l'entrepôt en tant qu'emplacement.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9092100816c58fe2882c61214a5008e27591d4f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820398"
---
# <a name="put-away-production-or-assembly-output"></a>Rangement du résultat de fabrication ou d'assemblage
Le mode de rangement de la production dépend du mode de configuration de l'entrepôt en tant qu'emplacement. Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

Dans les configurations de stockage de base où l'emplacement appelle un traitement de rangement, sans appeler de traitement de réception, vous pouvez utiliser le document **Rangement stock** pour organiser et enregistrer le rangement de la production.  

Dans les configurations de stockage avancées où l'emplacement nécessite un traitement à la fois de rangement et de réception, vous pouvez créer soit un document rangement interne soit un document mouvement pour ranger la production.  

La première étape dans la création d'un rangement de production consiste à créer la demande enlogement entrante. Cette demande indique à l'entrepôt que la production de l'O.F ou de l'assemblage est prête à être rangée.

## <a name="to-create-the-inbound-warehouse-request"></a>Pour créer la demande d'enlogement  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **O.F. lancé**, puis sélectionnez le lien associé.  
2.  Sur l’ordre de fabrication qui est prêt pour rangement, choisissez l'action **Créer demande d’enlogement**.  

> [!NOTE]  
>  Vous pouvez également créer la demande enlogement entrepôt en sélectionnant le champ **Créer demande d'enlogement** lors de l'actualisation de l'ordre de fabrication. Pour plus d'informations, voir [Actualiser ou replanifier des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Pour ranger la production avec un rangement stock  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Rangement stock**, puis sélectionnez le lien associé.  
2.  Créez un rangement stock. Pour plus d'informations, voir [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)
3.  Pour accéder aux composants de la production de l'O.F., choisissez l'action **Extraire documents origine**, puis sélectionnez l'ordre de fabrication lancé.  
4.  Renseignez les lignes rangement en fonction des besoins.
5.  Lorsque les lignes sont prêtes à être validées, choisissez l'action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la production des articles est validée.  

Vous pouvez également créer un **rangement stock** directement à partir de l'ordre de fabrication de lancé. Pour plus d'informations, voir [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  

Lorsque vous validez un rangement stock, on suppose que toutes les opérations sont validées en fonction de la gamme standard, à savoir que la quantité produite est validée en fonction de la dernière opération. Vous pouvez utiliser la feuille production pour valider les écarts de quantité produite et les temps d'exécution et de préparation. S'il est nécessaire d'effectuer une validation partielle après la création d'un rangement stock, vous pouvez le faire au niveau des temps de préparation et des quantités pour toutes les opérations, à l'exception de la dernière. Dans ce cas, la dernière opération est contrôlée par le rangement stock.  

Si vous devez juste validé le temps d'exécution ou de préparation de la dernière opération, définissez la quantité produite de la dernière opération sur 0. Vous pouvez également choisir de ne pas valider la dernière ligne en la supprimant  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Pour ranger la production dans le cadre d'un rangement interne ou d'un mouvement
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Rangement interne entrepôt**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.
3. Renseignez l'en-tête d'un nouveau rangement interne en y indiquant au moins le **code magasin**.  
4. Renseignez une ligne pour chaque article à déplacer vers l'entrepôt. Vous ne devez renseigner que les champs **N° article** et **Quantité**.  

    > [!NOTE]  
    >  Lorsque vous sélectionnez le champ **N° article**, la **liste des contenus emplacement** s'ouvre à la place de la **liste des articles**. En effet, vous souhaitez ranger un article qui se trouve dans un emplacement particulier (le contenu d'un emplacement et pas uniquement un article) et vous connaissez déjà l'emplacement dans lequel l'article doit être prélevé.  

4.  Pour compléter les lignes de la feuille en y indiquant l'ensemble du contenu emplacement ou le contenu emplacement filtré des emplacements du magasin, choisissez l'action **Extraire contenu emplacement**.  
5.  Choisissez l'action **Créer rangement**, et les articles que vous souhaitez sortir de l'unité de production figurent maintenant sur des instructions de rangement et attendent d'être stockés dans l'entrepôt.  

> [!NOTE]  
>  Lorsque l'entrepôt est configuré pour utiliser un prélèvement et un rangement suggérés, l'entrepôt est relié au centre de fabrication via les emplacements de fabrication par défaut : les emplacements enlogement et désenlogement et l'emplacement atelier ouvert que vous pouvez définir sur le raccourci **Emplacements** de la fiche magasin. Lorsque vous validez la production d'un O.F.,la production est placée automatiquement dans l' **emplacement désenlogement**. Suivez la procédure décrite ci-dessus pour ranger la production, mais au lieu d'utiliser l'emplacement par défaut de l'article, vous devez déplacer ou ranger les articles de l' **emplacement désenlogement** dans l'emplacement par défaut de l'article.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Pour spécifier manuellement un emplacement devant stocker des articles issus de l'unité de production  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille mouvement**, puis sélectionnez le lien associé.  
2.  Renseignez l'en-tête et créez une ligne pour chaque article à déplacer vers l'entrepôt.  
3.  Renseignez les champs **Du code emplacement** et **Du code emplacement**, puis entrez la quantité dans le champ **Quantité**.  
4.  Pour compléter les lignes de la feuille en y indiquant l'ensemble du contenu emplacement ou le contenu emplacement filtré des emplacements du magasin, choisissez l'action **Extraire contenu emplacement**.  
5. Choisissez l'action **Créer mouvement**. Des instruction de mouvement entrepôt sont créées contenant des lignes Prélever et Emplacement s'adressant aux magasiniers.  

> [!NOTE]  
>  Vous ne pouvez pas saisir le numéro document origine, tel que le N° O.F., rangement interne, rangement ou documents de mouvement pour l'une ou l'autre de ces procédures.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
