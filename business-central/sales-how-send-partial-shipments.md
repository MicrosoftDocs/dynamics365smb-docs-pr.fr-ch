---
title: Traiter les livraisons partielles
description: Les expéditions des commandes client peuvent être traitées dans Business Central avec des expéditions partielles à l’aide des champs Avis d’expédition et Quantité à expédier.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: a-reishima
---
# <a name="process-partial-shipments" />Traiter les livraisons partielles

Dans une expédition partielle, une commande n’est pas expédiée en une seule fois. Par exemple, pour une commande de 100 unités, vous en expédiez 40 immédiatement et 60 ultérieurement. Il n’y a aucune limite quant au nombre de livraisons pouvant être effectuées pour une commande.

Cependant, avant de pouvoir utiliser des livraisons partielles dans [!INCLUDE [prod_short](includes/prod_short.md)], vous devez spécifier que le client accepte les livraisons partielles en définissant le champ **Avis d’expédition** sur la page **Fiche client**. Sinon, si le client n’accepte généralement que des expéditions complètes, mais demande ensuite ou accepte une expédition partielle pour une commande client spécifique, vous pouvez modifier le champ **Avis d’expédition** avant validation.

Par défaut, [!INCLUDE [prod_short](includes/prod_short.md)] définit le champ dans la page **Fiche client** comme **Partiel**, ce qui permet des livraisons partielles. Si, toutefois, le champ a été ajusté pour spécifier **Complet**, puis le champ **Qté à expédier** est bloqué dans les commandes client pour ce client.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also" />Voir aussi

[Vente de produits avec une commande vente client](sales-how-sell-products.md)  
[Expédier des articles](warehouse-how-ship-items.md)  
[Effectuer des livraisons directes](sales-how-drop-shipment.md)  
[Ventes](sales-manage-sales.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
