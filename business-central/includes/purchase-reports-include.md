---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Le tableau suivant décrit certains des principaux états dans les états des achats.



| État | Description | ID | 
|---------|---------|---------|
|[Statistiques achat](https://businesscentral.dynamics.com?report=312)|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|312|
|[Fournisseur – Liste des 10 meilleurs](https://businesscentral.dynamics.com?report=311)|Affiche des informations sur les achats aux fournisseurs pour une période déterminée. Vous pouvez choisir le nombre de fournisseurs inclus dans l’état.<br>Les fournisseurs sont triés par montant, et vous pouvez choisir s’ils doivent être triés par montant d’achat ou par solde. L’état vous donne un bref aperçu des fournisseurs à qui vous achetez le plus et ceux à qui vous devez le plus d’argent.|311|
|[Fournisseur : Catalogue articles](https://businesscentral.dynamics.com?report=320)|Affiche une liste des fournisseurs pour les articles sélectionnés ou des articles pour les fournisseurs sélectionnés. Pour chaque combinaison d’article et de fournisseur, l’état indique le coût unitaire direct, le délai de réapprovisionnement et la référence fournisseur.<br>Cet état n’est pas disponible aux États-Unis, au Canada et au Mexique. Utilisez plutôt l’état **Catalogue Article/Fournisseur** (10164).|320|
|[Catalogue d’articles par fournisseur](https://businesscentral.dynamics.com?report=720)|Affiche une liste des fournisseurs pour les articles sélectionnés ou des articles pour les fournisseurs sélectionnés. Pour chaque combinaison d’article et de fournisseur, l’état indique le coût unitaire direct, le délai de réapprovisionnement et la référence fournisseur.<br>Cet état n’est pas disponible aux États-Unis, au Canada et au Mexique. Utilisez plutôt l’état **Catalogue Article/Fournisseur** (10164).|720|
|[Achats Fournisseur/Article](https://businesscentral.dynamics.com?report=313)|Affiche la liste des écritures article de chaque fournisseur pendant la période choisie. L’état affiche des informations sur la quantité facturée, le montant et les remises possibles. Il peut être utilisé, par exemple, pour analyser les achats d’articles d’une société et pour voir s’il existe une relation entre les remises et les achats d’articles.|313|
|[Liste prix et coûts stocks](https://businesscentral.dynamics.com?report=716)|Affiche la liste d’informations sur les prix des articles sélectionnés ou des points de stock : coût unitaire direct, dernier coût direct, prix unitaire, pourcentage de marge et marge.|716|
|[Échéancier des dispo. de stock](https://businesscentral.dynamics.com?report=707)|Si vous souhaitez avoir un aperçu d’articles/de points de stock spécifiques et de leur disponibilité. Cet état affichera des valeurs cumulées telles que les besoins bruts, les réceptions planifiées et prévues, le stock, etc. |707|
|[Achats fournisseur stock](https://businesscentral.dynamics.com?report=714)|Affiche la liste des fournisseurs auxquels votre société a acheté des articles dans la période sélectionnée. Il indique la quantité facturée, le montant et la remise. L’état peut être utilisé pour analyser les achats de la société.|714|
|[Commandes achat de stock](https://businesscentral.dynamics.com?report=709)|Affiche la liste des articles commandés chez les fournisseurs. Il indique aussi la date de réception prévue, la quantité et le montant des commandes en souffrance. Par exemple, utilisez l’état pour visualiser le moment où les articles doivent être réceptionnés et si un rappel de commande en souffrance doit être émis.|709|
|[Disponibilité réservation achat](https://businesscentral.dynamics.com?report=409)|Affiche la disponibilité des articles pour les livraisons effectuées à partir de documents achat, par exemple les retours. Vous déterminez si l’état indique le statut de chaque document ou de chaque ligne achat. <br>Lorsque vous imprimez l’état, vous pouvez également mettre à jour les quantités disponibles pour livraison dans le champ **Quantité à recevoir** des lignes achat. Sur les avoirs achat et les lignes commande achat négative, le champ **Quantité à recevoir** indique la quantité à livrer. Vous pouvez alors utiliser cet état pour déterminer les documents à valider. **Remarque** : cet état n’est pas disponible pour les fonctionnalités d’entrepôt avancées.|409|
<!--|[](https://businesscentral.dynamics.com?report=)Fournisseur : Écritures échues|11006| Spécifique à DACH : état qui pourrait être utilisé par le chef d’équipe de votre département d’achat ainsi que par la comptabilité. Vous aurez ici un aperçu des factures fournisseurs impayées, y compris les dates d’échéance, les devises et les montants. La base est constituée des écritures comptables fournisseur ouvertes.| -->

