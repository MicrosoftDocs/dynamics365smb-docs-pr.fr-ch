---
title: États et analyses des achats
description: Découvrez les états et analyses des achats disponibles dans la version standard de Business Central afin que vous puissiez suivre votre activité.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543185"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>États et analyses des achats dans Business Central

Les états des achats dans [!INCLUDE [prod_short](includes/prod_short.md)] permettent aux professionnels de l’approvisionnement et des affaires d’obtenir des informations et des statistiques sur les activités d’achat actuelles et passées.  

## <a name="reports"></a>États

Le tableau suivant décrit certains des principaux états dans les états des achats.

|État |ID d’objet|Description  |
|---------|---------|---------|
|**Statistiques achat**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**Fournisseur – Liste des 10 meilleurs**|311|Affiche des informations sur les achats aux fournisseurs pour une période déterminée. Vous pouvez choisir le nombre de fournisseurs inclus dans l’état.<br>Les fournisseurs sont triés par montant, et vous pouvez choisir s’ils doivent être triés par montant d’achat ou par solde. L’état vous donne un bref aperçu des fournisseurs à qui vous achetez le plus et ceux à qui vous devez le plus d’argent.|
|**Catalogue article fournisseur** ou **Catalogue fournisseur/article**|320 ou 720|Affiche une liste des fournisseurs pour les articles sélectionnés ou des articles pour les fournisseurs sélectionnés. Pour chaque combinaison d’article et de fournisseur, l’état indique le coût unitaire direct, le délai de réapprovisionnement et la référence fournisseur.<br>Cet état n’est pas disponible aux États-Unis, au Canada et au Mexique. Utilisez plutôt l’état **Catalogue Article/Fournisseur** (10164).|
|**Achats Fournisseur/Article**|313|Affiche la liste des écritures article de chaque fournisseur pendant la période choisie. L’état affiche des informations sur la quantité facturée, le montant et les remises possibles. Il peut être utilisé, par exemple, pour analyser les achats d’articles d’une société et pour voir s’il existe une relation entre les remises et les achats d’articles.|
|**Liste prix et coûts stocks**|716|Affiche la liste d’informations sur les prix des articles sélectionnés ou des points de stock : coût unitaire direct, dernier coût direct, prix unitaire, pourcentage de marge et marge.|
|**Échéancier des dispo. de stock**|707|Si vous souhaitez avoir un aperçu d’articles/de points de stock spécifiques et de leur disponibilité. Cet état affichera des valeurs cumulées telles que les besoins bruts, les réceptions planifiées et prévues, le stock, etc. |
|**Achats fournisseur stock**|714|Affiche la liste des fournisseurs auxquels votre société a acheté des articles dans la période sélectionnée. Il indique la quantité facturée, le montant et la remise. L’état peut être utilisé pour analyser les achats de la société.|
|**Commandes achat de stock**|709|Affiche la liste des articles commandés chez les fournisseurs. Il indique aussi la date de réception prévue, la quantité et le montant des commandes en souffrance. Par exemple, utilisez l’état pour visualiser le moment où les articles doivent être réceptionnés et si un rappel de commande en souffrance doit être émis.|
|**Disponibilité réservation achat**|409|Affiche la disponibilité des articles pour les livraisons effectuées à partir de documents achat, par exemple les retours. Vous déterminez si l’état indique le statut de chaque document ou de chaque ligne achat. <br>Lorsque vous imprimez l’état, vous pouvez également mettre à jour les quantités disponibles pour livraison dans le champ **Quantité à recevoir** des lignes achat. Sur les avoirs achat et les lignes commande achat négative, le champ **Quantité à recevoir** indique la quantité à livrer. Vous pouvez alors utiliser cet état pour déterminer les documents à valider. **Remarque** : cet état n’est pas disponible pour les fonctionnalités d’entrepôt avancées.|
<!--|**Fournisseur - Écritures échues**|11006| Spécifique à DACH : état qui pourrait être utilisé par le chef d’équipe de votre département d’achat ainsi que par la comptabilité. Vous aurez ici un aperçu des factures fournisseurs impayées, y compris les dates d’échéance, les devises et les montants. La base est constituée des écritures comptables fournisseur ouvertes.| -->




## <a name="tasks"></a>Tâches

Les articles suivants décrivent certaines des tâches clés pour analyser l’état de votre entreprise :

* [Créer des rapports d’analyse](bi-how-create-analysis-views-reports.md)  
* [Voir la disponibilité des articles](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Voir aussi

[Définition des achats](purchasing-setup-purchasing.md)  
[Achats](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
