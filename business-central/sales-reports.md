---
title: États et analyses de vente
description: Découvrez les états et analyses de vente disponibles dans la version standard de Business Central afin que vous puissiez suivre votre activité.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 76f93a75f9f7fd52b2495d75bffe648d53f9c844
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543262"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>États et analyses de vente dans Business Central

Les états de vente dans [!INCLUDE [prod_short](includes/prod_short.md)] permettent aux professionnels des ventes et des affaires d’obtenir des informations et des statistiques sur les activités de vente actuelles et passées.  

## <a name="reports"></a>États

Le tableau suivant décrit certains des principaux états dans les états de vente.

|État |ID d’objet|Description  |
|---------|---------|---------|
|**Clients : Liste des commandes**|107| Affiche le détail de la commande avec la quantité qui n’est pas encore livrée, de chaque client sur 3 périodes de 30 jours chacune commençant à la date spécifiée. Il contient également des colonnes avec les commandes à livrer avant et après les 3 périodes et une colonne avec le détail de la commande totale de chaque client. Utilisez l’état pour analyser le volume de vente attendu d’une société. |
|**Client – Liste des 10 meilleurs**|111| Affiche des informations sur les achats et les soldes des clients pour la période sélectionnée. Vous pouvez choisir le nombre de clients qui sont inclus dans l’état. Seuls les clients qui ont des achats pour cette période ou un solde à la fin de la période sont inclus.<br>Les clients sont triés par montant, et vous pouvez choisir s’ils doivent être triés par montant de ventes ou par solde. L’état vous donne un bref aperçu des clients qui achètent le plus et de ceux qui doivent le plus d’argent.|
|**Ventes Client/Article**|113|Affiche la liste des ventes article pour chaque client pendant la période choisie. L’état donne des informations sur la quantité, le montant des ventes, la marge et les remises possibles. Il peut servir, par exemple, à l’analyse des groupes clients d’une société.|
|**Stocks – Vente client**|713|Aperçu du point de vue de l’entrepôt. Il s’agit d’un point de vue différent de celui de l’état **Vente Client/Article**, et il montre d’abord l’article, puis le client qui a acheté ce produit.|
|**Clients – Liste des ventes**|119|Affiche les ventes client pour une période. Vous l’utilisez pour les déclarations auprès des administrations douanières et fiscales. Vous pouvez choisir de n’inclure que les clients dont le total des ventes excède un montant minimum. Vous pouvez également spécifier si vous souhaitez que l’état reprenne les informations adresse de chaque client.<br>L’état est basé sur les ventes enregistrées (DS) provenant des écritures comptables client. En bas de l’état, le total des ventes déclarées est indiqué en DS. Le total est basé sur les clients que vous avez inclus dans l’état, autrement dit ceux qui figurent dans les filtres du raccourci Client et dont le total des ventes est supérieur au montant spécifié dans le champ **Montants DS supérieurs à** du raccourci **Options**.|
|**Clients – Solde cumulé**|121|Affiche un solde détaillé des clients sélectionnés. Utlisez l’état lors de la clôture d’une période comptable ou d’un exercice comptable, par exemple.|
|**Clients –– Balance**|129|Affiche le solde détaillé de clients sélectionnés. Vous pouvez utiliser l’état pour vérifier que le solde pour un groupe comptabilisation client est égal à celui du compte général correspondant à une certaine date. Utlisez l’état lors de la clôture d’une période comptable ou d’un exercice comptable, par exemple. Si vous avez besoin d’une version plus détaillée de ce type d’état, utilisez l’état **Grand livre clients** (104).|
|**Statistique vente**|112|[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)] |
|**Dispo. réservation vente**|209|Affiche la disponibilité des articles pour les livraisons faites à partir de documents vente. Vous déterminez si l’état indique le statut de chaque document ou de chaque ligne vente. Lorsque vous imprimez l’état, vous pouvez également mettre à jour les quantités disponibles pour livraison dans le champ **Qté à expédier** des lignes vente. Vous pouvez alors utiliser cet état pour déterminer les documents à valider.<br>Il existe également une capacité avec laquelle vous pouvez définir la quantité de produits à expédier. **Remarque** : cet état n’est pas disponible pour les fonctionnalités d’entrepôt avancées.|
|**Statut expédition entrepôt**|7313|Cet état peut être utilisé pour tous les magasins pour lesquels le champ **Envoi requi** est sélectionné. L’état **Statut expédition entrepôt** vous montre tous les documents d’expédition d’entrepôt non validés, y compris les magasins, les codes emplacement, le statut des document, les quantités, etc. Cet état est parfait pour avoir une vue d’ensemble.|
|**Liste des prélèvements stock**|813|Affiche la liste des commandes vente dans lesquelles un article est inclus. Les informations suivantes sont données pour chaque article : ligne commande vente avec le nom du client, code variante, code magasin, code emplacement, date d’expédition, quantité à expédier et unité. La quantité à livrer est totalisée pour chaque article. L’état peut être utilisé lorsque des articles vont être retirés du stock.<br>**Remarque** : cet état n’est pas disponible pour les fonctionnalités d’entrepôt avancées.|
|**Commandes en souffrance du stock**|718|Affiche une liste qui comprend les lignes commande dont la date d’expédition est dépassée. Les informations suivantes sont données pour chaque article d’une commande : numéro, nom du client, numéro de téléphone du client, date d’expédition, quantité commandée et quantité sur commande en attente. L’état indique aussi s’il y a d’autres articles en commande en souffrance pour le client.|



## <a name="tasks"></a>Tâches

Les articles suivants décrivent certaines des tâches clés pour analyser l’état de votre entreprise :

* [Créer des rapports d’analyse](bi-how-create-analysis-views-reports.md)  
* [Voir la disponibilité des articles](inventory-how-availability-overview.md)


## <a name="see-also"></a>Voir aussi

[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
