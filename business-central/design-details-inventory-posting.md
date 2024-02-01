---
title: Détails de conception - Compta. stock | Microsoft Docs
description: 'Chaque mouvement stock, par exemple une réception achat ou une expédition vente, valide deux écritures de différents types.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-inventory-posting"></a>Détails de conception : comptabilisation stock

Chaque mouvement stock, par exemple une réception achat ou une expédition vente, valide deux écritures de différents types.  

|Type écriture|Désignation|  
|----------|-----------|  
|Quantité|Reflète la modification de la quantité en stock. Ces informations sont stockées dans les écritures comptables article.<br /><br /> Accompagné des écritures lettrage article.|  
|Valeur|Reflète la modification de la valeur stock. Ces informations sont stockées dans les écritures valeur.<br /><br /> Chaque écriture comptable article ou écriture comptable capacité peut posséder une ou plusieurs écritures valeur.<br /><br /> Pour plus d’informations sur les écritures de valeur de capacité liées à l’utilisation des ressources de production ou d’assemblage, reportez\-vous à [Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md).|  

 En rapport avec les validations de quantité, les écritures lettrage article existent pour lier l’entrée de stock avec la sortie de stock. Cela permet au moteur d’évaluation de transférer les cous des augmentations aux diminutions liées et vice versa. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-application.md).  

 Les écritures comptables article, les écritures valeur, ainsi que les écritures lettrage article sont créées suite à la validation d’une ligne feuille article, soit indirectement lors de la validation d’une ligne commande, soit directement sur la page feuille article.  

 À intervalles réguliers, les écritures valeur créées parmi les écritures comptables d’inventaire sont validées en comptabilité pour rapprocher les deux comptabilités à des fins de contrôle financier. Pour plus d’informations, voir [Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md).  

 ![Flux d’écriture lors du rapprochement du stock avec la comptabilité.](media/design_details_inventory_costing_1_entry_flow.png "Flux d’écriture lors du rapprochement du stock avec la comptabilité")  

## <a name="example"></a>Exemple :

L’exemple suivant indique comment les écritures comptables article, les écritures valeur et les écritures lettrage article créent des écritures comptables.  

 Vous validez une commande achat comme reçue et facturée pour 10 articles avec un coût unitaire direct de 7 LCY et des frais généraux d’1 LCY. La date comptabilisation est 01-01-20. Les écritures suivantes sont créées.  

### <a name="item-ledger-entries-1"></a>Écritures comptables article (1)

|Date comptabilisation|Type écriture|Coût total (réel)|Quantité|Numéro de la séquence|  
|------------|----------|--------------------|--------|---------|  
|01/01/20|Achats|80,00|10|1|  

### <a name="value-entries-1"></a>Écritures valeur (1)

|Date comptabilisation|Type écriture|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------|----------|--------------------|---------------------|---------|  
|01/01/20|Coût direct|70,00|1|1|  
|01/01/20|Coût indirect|10,00|1|2|  

### <a name="item-application-entries-1"></a>Écritures lettrage article (1)

|Numéro de la séquence|N° écriture comptable article|N° écriture article entrant|N° écriture article sortant|Quantité|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Ensuite, vous validez une vente de 10 unités de l’article avec une date validation de 15/01/20.  

### <a name="item-ledger-entries-2"></a>Écritures comptables article (2)

|Date comptabilisation|Type écriture|Coût total (réel)|Quantité|Numéro de la séquence|  
|------------|----------|--------------------|--------|---------|  
|15/01/20|Vente|-80,00|-10|2|  

### <a name="value-entries-2"></a>Écritures valeur (2)

|Date comptabilisation|Type écriture|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------|----------|--------------------|---------------------|---------|  
|15/01/20|Coût direct|-80,00|2|3|  

### <a name="item-application-entries-2"></a>Écritures lettrage article (2)

|Numéro de la séquence|N° écriture comptable article|N° écriture article entrant|N° écriture article sortant|Quantité|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

À la fin de la période comptable, vous exécutez le traitement par lots **Valider coûts ajustés** pour effectuer un rapprochement entre ces mouvements de stock et la comptabilité.  

 Pour plus d’informations, voir [Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).  

 Les tables suivantes indiquent le résultat du rapprochement des mouvements de stock de cet exemple avec la comptabilité.  

### <a name="value-entries-3"></a>Écritures valeur (3)

|Date comptabilisation|Type écriture|Coût total (réel)|Coût validé en comptabilité|N° écriture comptable article|Numéro de la séquence|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01/01/20|Coût direct|70,00|70,00|1|1|  
|01/01/20|Coût indirect|10,00|10,00|1|2|  
|15/01/20|Coût direct|-80,00|-80,00|2|3|  

### <a name="general-ledger-entries-3"></a>Écritures comptables (3)

|Date comptabilisation|Compte général|N° compte (démonstration Fr-FR)|Montant|Numéro de la séquence|  
|------------|-----------|------------------------|------|---------|  
|01/01/20|[Compte stocks]|2 130|70,00|1|  
|01/01/20|[Compte coût direct lettré]|7 291|-70,00|2|  
|01/01/20|[Compte stocks]|2 130|10,00|3|  
|01-01-07|[Compte frais généraux lettrés]|7 292|-10,00|4|  
|15/01/20|[Compte stocks]|2 130|-80,00|5|  
|15/01/20|[Compte variation stock]|7 290|80,00|6|  

> [!NOTE]  
> La date comptabilisation des écritures comptables est la même que pour les écritures valeur associées.  
> 
> Le champ **Coût validé en comptabilité** de la table **Ecritures valeur** est renseigné.  

 La relation entre les écritures valeur et les écritures comptables est stockée dans la table **Compta. Relation écritures article**.  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a>Liens écritures dans la comptabilité – Table Écriture comptable article (3)

|N° séquence compta.|N° écriture valeur|N° hist. transaction compta.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Validation d’assemblage et de production

Les écritures comptables capacité et ressource représentent le délai qui est validé comme étant consommé dans la production ou l’assemblage. Ces coûts opératoires sont validés comme écritures valeur en comptabilité en même temps que les coûts matière impliqués dans une structure similaire telle que décrite pour les écritures comptables article de cette rubrique.  

Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md).  

## <a name="see-also"></a>Voir aussi

 [Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
 [Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md)  
 [Détails de conception : Ajustement des coûts](design-details-cost-components.md) [Gestion des composants des coûts](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
