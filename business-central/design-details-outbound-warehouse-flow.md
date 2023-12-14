---
title: Vue d’ensemble des processus sortants de l’entrepôt
description: Cet article décrit le flux de travail sortant de l’entrepôt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a>Processus sortants de l’entrepôt

Les processus sortants de l’entrepôt démarrent lorsque vous validez un document origine pour sortir des articles d’un magasin d’entrepôt. Par exemple, soit pour expédier les articles quelque part, soit pour les déplacer vers un autre magasin de l’entreprise. Vous pouvez expédier des articles physiques et hors inventaire. Pour en savoir plus sur la réception d’articles hors inventaire, consultez [Valider des articles hors inventaire](#post-non-inventory-items). 

En principe, le processus d’expédition des commandes sortantes se compose de deux activités :

* Prélever des articles sur les étagères.
* Expédier les articles hors de l’entrepôt.

Les documents origine pour le flux d’entrepôt sortant sont les suivants :  

* Commande vente  
* Commande désenlogement transfert  
* Retour commande achat  
* Commande service  

> [!NOTE]
> Les besoins en composants des ordres de fabrication et d’assemblage représentent également des documents origine sortants. Les ordres de fabrication et d’assemblage sont un peu différents car il s’agit généralement de processus internes qui n’impliquent pas d’expédition. Au lieu de cela, ils sont utilisés pour ranger les articles produits ou déplacer les composants nécessaires pour assembler un article vers une zone d’assemblage. Pour en savoir plus sur ces processus, consultez [Design Details : flux d’entrepôt internes](design-details-internal-warehouse-flows.md).  

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous prélevez et expédiez des articles en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus sortant|Prélèvement requis|Expédition requise|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l’expédition à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock|Activé||De base : commande par commande.|  
|A|Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt||Activé|De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation du prélèvement à partir d’un document prélèvement entrepôt, et validation de l’expédition à partir d’un document expédition entrepôt|Activé|Activé|Avancé|  

Le choix d’une méthode dépend des pratiques de stockage de votre société et de la complexité de son organisation. Voici quelques exemples qui peuvent vous aider à décider.

* Dans un environnement par commande avec des processus et une structure d’emplacement simples, la méthode A, de prélèvement et d’expédition à partir de la ligne commande, est appropriée.
* Si les articles d’une ligne commande proviennent de plusieurs emplacements, ou si les magasiniers ne peuvent pas travailler avec des documents de commande, l’utilisation de documents de prélèvement distincts est appropriée ; c’est la méthode B.
* Si vos processus de prélèvement et d’expédition impliquent plusieurs commandes et nécessitent un contrôle et une vue d’ensemble accrus, vous pouvez choisir d’utiliser un document d’expédition entrepôt et un document de prélèvement entrepôt pour séparer les tâches de prélèvement et d’expédition : méthodes C et D.  

Dans les méthodes A, B et C, les activités de prélèvement et d’expédition sont combinées en une étape lors de la validation d’un document comme étant expédié. Dans la méthode D, vous enregistrez d’abord le prélèvement, puis vous validez ensuite l’expédition à partir d’un document différent.

> [!NOTE]
> Bien que les prélèvements entrepôt et les prélèvements stock semblent similaires, ce sont des documents différents et ils sont utilisés dans des processus différents.
> * Le prélèvement stock utilisé dans la méthode B, ainsi que l’enregistrement des informations de prélèvement, valide également l’expédition du document source.
> * Le prélèvement entrepôt utilisé dans la méthode D ne peut pas être validé et enregistre uniquement le prélèvement. L’enregistrement rend les articles disponibles pour l’expédition entrepôt, mais ne valide pas l’expédition. Dans le flux sortant, le prélèvement entrepôt nécessite une expédition entrepôt.

## <a name="no-dedicated-warehouse-activity"></a>Aucune activité entrepôt dédiée

Les articles suivants fournissent des informations sur le traitement des réceptions pour les documents origine si vous n’avez pas d’activités entrepôt dédiées.

* [Vendre des produits](sales-how-sell-products.md)
* [Ordres de transfert](inventory-how-transfer-between-locations.md)
* [Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md)
* [Créer commande service](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a>Configurations d’entrepôt de base

Le schéma suivant présente les processus d’entrepôt sortants pour différents types de document dans les configurations d’entrepôt de base. Les numéros dans le schéma correspondent aux étapes dans les sections suivant le schéma.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Affiche les étapes d’un flux sortant de base dans un entrepôt.":::

### <a name="1-release-a-source-document"></a>1 : Lancer un document origine

Lorsque vous utilisez l’action **Lancer** sur un document origine, tel qu’une commande vente ou un ordre de transfert, les articles du document sont prêts à être traités dans l’entrepôt. Par exemple, prélevés et placés dans l’emplacement spécifié sur le document. Sinon, vous pouvez créer des documents prélèvement stock pour des lignes commande individuelles, en mode « push », selon les emplacements spécifiés et les quantités à traiter.  

### <a name="2-create-an-inventory-pick"></a>2 : Créer un prélèvement stock

Sur la page **Prélèvement stock**, le magasinier récupère, en mode « pull », les lignes du document origine. Sinon, les lignes prélèvement stock sont déjà créées, par déplacement, par l’utilisateur responsable du document origine.  

### <a name="3-post-an-inventory-pick"></a>3 : Valider un prélèvement stock

Sur chaque ligne pour les articles qui ont été prélevés ou déplacés, entièrement ou partiellement, renseignez le champ **Quantité**, puis validez le prélèvement stock. Les documents origine associé au prélèvement stock sont validés comme étant expédiés ou consommés.  

Pour les prélèvements stock, les écritures comptables article négatives sont créées, les écritures entrepôt sont créées, et la demande de prélèvement est supprimée, si entièrement enregistrée. Par exemple, le champ **Qté expédiée** sur la ligne document origine sortant est mis à jour. Un document expédition validé est créé et indique la commande vente, par exemple, ainsi que les articles expédiés.  

## <a name="advanced-warehouse-configurations"></a>Configurations d’entrepôt avancées

Le schéma suivant présente les processus d’entrepôt sortants pour différents types de document dans les configurations d’entrepôt avancées. Les numéros dans le schéma correspondent aux étapes dans les sections suivant le schéma.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Affiche les étapes d’un flux sortant avancé dans un entrepôt.":::

### <a name="1-release-a-source-document-1"></a>1 : Lancer un document origine

Le lancement d’un document origine dans les configurations avancées a le même effet que pour les configurations de base. Les articles deviennent disponibles pour être manipulés dans l’entrepôt. Par exemple, ils peuvent être inclus dans une expédition.  

### <a name="2-create-a-warehouse-shipment"></a>2 : Créer une expédition entrepôt

Sur la page **Expédition entrepôt**, récupérez les lignes du document origine lancé. Vous pouvez combiner des lignes de plusieurs documents dans une expédition entrepôt.  

### <a name="3-create-a-warehouse-pick"></a>3 : Créer un prélèvement entrepôt

Sur la page **Expédition entrepôt**, créez des activités de prélèvement entrepôt pour les expéditions entrepôt de l’une des deux manières suivantes :

- En mode « push », où vous utilisez l’action **Créer prélèvement**. Sélectionnez les lignes à prélever et préparez les prélèvements en spécifiant, par exemple, à partir de quels emplacements les prendre, à quels emplacements les placer, et le nombre d’unités à traiter. Les emplacements peuvent être prédéfinis pour l’entrepôt ou la ressource.
- En mode « pull », où vous utilisez l’action **Lancer**. Sur la page **Feuille prélèvement**, les magasiniers peuvent utiliser l’action **Extraire documents entrepôt** pour récupérer les prélèvements qui leur sont assignés. Lorsque les prélèvements entrepôt sont entièrement enregistrés, les lignes dans la **Feuille prélèvement** sont supprimées.

### <a name="4-register-a-warehouse-pick"></a>4 : Enregistrer un prélèvement entrepôt

Sur la page **Prélèvement entrepôt**, un magasinier renseigne le champ **Quantité** pour chaque ligne qu’il a prélevée entièrement ou partiellement, puis enregistre le prélèvement.

Les écritures d’entrepôt sont créées, et les lignes prélèvement entrepôt sont supprimées si la quantité entière a été prélevée. Le document de prélèvement entrepôt reste ouvert jusqu’à ce que la quantité totale de l’expédition entrepôt soit enregistrée. Le champ **Qté prélevée** sur les lignes expédition entrepôt est mis à jour en conséquence.  

### <a name="5-post-the-warehouse-shipment"></a>5 : Valider l’expédition entrepôt

Lorsque tous les articles du document d’expédition entrepôt sont enregistrés comme prélevés, le magasinier valide l’expédition. La validation met à jour les écritures du registre des articles pour refléter la réduction du stock. Par exemple, le champ **Qté expédiée** sur la ligne document origine sortant est mis à jour.  

## <a name="post-non-inventory-items"></a>Valider des articles hors inventaire

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
