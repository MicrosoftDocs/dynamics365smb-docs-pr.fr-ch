---
title: "Détails de conception\_-\_Validation d’ordre d’assemblage"
description: La validation d’ordre d’assemblage est basée sur les mêmes principes que la validation des activités similaires des commandes vente et de la consommation de production/production.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-assembly-order-posting"></a>Détails de conception : validation d’ordre d’assemblage
La validation d’ordre d’assemblage est basée sur les mêmes principes que la validation des activités similaires des commandes vente et de la consommation de production/production. Cependant, les principes sont combinés du fait que les ordres d’assemblage ont leur propre interface utilisateur de validation, comme celle des commandes vente, alors que la validation des écritures réelle se produit en arrière-plan en tant que validations directes d’article et de feuille ressource, comme pour la consommation de production, la production et la capacité.  

Comme pour la validation d’ordre de fabrication, les composants consommés et les ressources utilisées sont convertis et sortis en tant qu’élément d’assemblage lorsque l’ordre d’assemblage est validé. Pour plus d’informations, voir [Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md). Toutefois, le flux des coûts des ordres d’assemblage est moins complexe, notamment parce que la validation du coût d’assemblage ne se produit qu’une fois et ne génère donc pas de stock encours.  

Les validations feuille suivantes se produisent lors de la validation d’ordre d’assemblage :  

-   La feuille article valide les écritures comptables article positives, représentant la production de l’élément d’assemblage, à partir de l’en-tête de l’ordre d’assemblage.  
-   La feuille article valide les écritures comptables article négatives, représentant la consommation des composants d’assemblage, à partir des lignes d’ordre d’assemblage.  
-   La feuille ressource valide l’utilisation des ressources d’assemblage (en unités de temps), à partir des lignes d’ordre d’assemblage.  
-   La feuille capacité valide les écritures valeur concernant l’utilisation des ressources, à partir des lignes d’ordre d’assemblage.  

Le schéma suivant montre la structure des écritures comptables article et ressource qui résultent de la validation d’un ordre d’assemblage.  

![Écritures comptables article, ressource et capacité résultant de la validation d’ordre d’assemblage.](media/design_details_assembly_posting_1.png "Écritures comptables article, ressource et capacité résultant de la validation d’ordre d’assemblage")  

> [!NOTE]  
>  Les postes et centres de charge sont inclus pour illustrer que les écritures comptables capacité sont créées à la fois à partir de la production et de l’assemblage.  

Le schéma suivant montre la manière dont les données d’assemblage circulent dans les écritures comptables au cours de la validation :  

![Flux d’écritures lié à l’assemblage lors de la validation.](media/design_details_assembly_posting_2.png "Flux d’écritures lié à l’assemblage lors de la validation")  

## <a name="posting-sequence"></a>Séquence de validation
La validation d’un ordre d’assemblage se produit dans l’ordre suivant :  

1.  Les lignes ordre d’assemblage sont validées.  
2.  L’en-tête d’ordre d’assemblage est validé.  

Le tableau suivant indique la séquence d’actions.  

|Action|Désignation|  
|------------|-----------------|  
|Initialiser la validation|1. Effectuer une vérification préliminaire.<br />2. Ajoutez le numéro de validation et modifiez l’en\-tête d’ordre d’assemblage.<br />3. Lancez l’ordre d’assemblage.|  
|Comptabilisation|<ol><li>Créer l’en-tête d’ordre d’assemblage validé.</li><li>Copier les lignes commentaire.</li><li>Validez les lignes ordre d’assemblage (consommation) :<br /><br /> <ol><li>Créer une page statut pour calculer la consommation d’assemblage.</li><li>Obtenir la quantité restante sur laquelle la ligne feuille article est basée.</li><li>Réinitialisez les quantités consommées et les quantités d’assemblage.</li><li>Pour les lignes ordre d’assemblage de type Article :<br /><br /> <ol><li>Renseignez les champs dans la ligne feuille article.</li><li>Transférez les réservations vers la ligne feuille article.</li><li>Validez la ligne feuille article pour créer les écritures comptables article.</li><li>Créer les lignes feuille entrepôt et les valider.</li></ol></li><li>Pour les lignes ordre d’assemblage de type Ressource :<br /><br /> <ol><li>Renseignez les champs dans la ligne feuille article.</li><li>Validez la ligne feuille article. Cela crée des écritures comptables de capacité.</li><li>Créer et valider la ligne feuille ressources.</li></ol></li><li>Transférez des valeurs de champ de l’ordre d’assemblage dans une ligne d’ordre d’assemblage validé nouvellement créée.</li></ol></li><li>Validez l’en-tête d’ordre d’assemblage (résultat) :<br /><br /> <ol><li>Renseignez les champs dans la ligne feuille article.</li><li>Transférez les réservations vers la ligne feuille article.</li><li>Validez la ligne feuille article pour créer les écritures comptables article.</li><li>Créer les lignes feuille entrepôt et les valider.</li><li>Réinitialisez les quantités d’assemblage et les quantités restantes.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  Contrairement à la sortie de production, qui est validée au coût prévu, le résultat d’assemblage est validé au coût réel.  

## <a name="cost-adjustment"></a>Ajustement des coûts
 Une fois l’ordre d’assemblage validé, à savoir les composants (matériel) et ressources sont assemblés dans un nouvel article, il doit être possible de déterminer le coût réel de cet élément d’assemblage, et le coût de stock réel des composants impliqués. Ceci est obtenu en transférant les coûts des écritures validées de la source (les composants et ressources) aux écritures validées de la destination (l’élément d’assemblage). Le transfert des coûts est effectué en calculant et en générant de nouvelles écritures, appelées écritures ajustement qui sont associées aux écritures de destination.  

 Les coûts d’assemblage à transférer sont détectés grâce au mécanisme de détection du niveau de commande. Pour plus d’informations sur d’autres mécanismes de détection d’ajustement, reportez\-vous à [Détails de conception : ajustement des coûts](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Détection de l’ajustement
La fonction de détection du niveau de commande est utilisée pour les scénarios de conversion, de production et d’assemblage. La fonction opère comme suit :  

-   L’ajustement des coûts est détecté en marquant la commande chaque fois que des matières/ressources sont validées comme étant consommées/utilisées pour la commande.  
-   Les coûts sont transférés en appliquant les coûts des matières/ressources aux écritures de production liées à la même commande.  

Le graphique suivant montre la structure d’écriture d’ajustement et comment les coûts d’assemblage sont ajustés.  

![Flux d’écritures lié à l’assemblage lors de l’ajustement des coûts.](media/design_details_assembly_posting_3.png "Flux d’écritures lié à l’assemblage lors de la validation")  

### <a name="performing-the-adjustment"></a>Procéder à l’ajustement
La répartition des ajustements détectés entre les coûts matière et ressource et les écritures de résultat d’assemblage est effectuée par le traitement par lots **Ajuster coûts : Écr. article**. Il contient la fonction Effectuer un ajustement à plusieurs niveaux, qui se compose des deux éléments suivants :  

-   Effectuer un ajustement d’ordre d’assemblage : qui transmet le coût d’utilisation des matières et des ressources à l’écriture de résultat d’assemblage. Les lignes 5 et 6 dans l’algorithme ci-dessous sont responsables de cela.  
-   Effectuer des ajustements à un seul niveau : ce qui transfère les coûts des différents articles en utilisant leur mode d’évaluation du stock. Les lignes 9 et 10 dans l’algorithme ci-dessous sont responsables de cela.  

![Résumé de l’algorithme d’ajustement des coûts pour validation de l’assemblage.](media/design_details_assembly_posting_4.jpg "Résumé de l’algorithme d’ajustement des coûts pour validation de l’assemblage")  

> [!NOTE]  
>  L’élément Effectuer des ajustements de TEC, dans les lignes 7 et 8, est responsable du transfert du matériel de production et de l’utilisation de la capacité vers la production des ordres de fabrication non terminés. Ceci n’est pas utilisé lors de l’ajustement des coûts d’ordre d’assemblage car le concept de TEC ne s’applique pas à l’assemblage.  

Pour plus d’informations sur la manière dont les coûts d’assemblage ou de production sont validés dans la comptabilité, reportez\-vous à [Détails de conception : comptabilisation stock](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Les coûts d’assemblage sont toujours réels
 Le concept d’en-cours (TEC) ne s’applique pas à la validation d’ordre d’assemblage. Les coûts d’assemblage sont uniquement validés en tant que coûts réels, jamais en tant que coûts prévus. Pour plus d’informations, voir [Détails de conception : validation du coût prévu](design-details-expected-cost-posting.md).  

Ceci est activé par la structure de données suivante.  

-   Dans le champ **Type** des lignes feuille article, dans les tables **Écriture comptable capacité** et **Écriture valeur**, *Ressource* est utilisé pour identifier les écritures ressource d’assemblage.  
-   Dans le champ **Type écriture comptable article** sur les lignes feuille article, dans les tables **Écriture comptable capacité** et **Écriture valeur**, *Résultat d’assemblage* et *Consommation d’assemblage* permettent d’identifier les écritures d’élément d’assemblage de production et les écritures composant d’assemblage consommées respectivement.  

En outre, les champs de groupe comptabilisation dans l’en-tête d’ordre d’assemblage et les lignes d’ordre d’assemblage sont renseignés par défaut comme suit.  

|Entité|Type|Groupe comptabilisation|Groupe. Groupe compta. produit|  
|------------|----------|-------------------|------------------------------|  
|En-tête d’ordre d’assemblage|Article ;|Groupe compta. stock|Groupe. Groupe compta. produit|  
|Ligne d’ordre d’assemblage|Article ;|Groupe compta. stock|Groupe. Groupe compta. produit|  
|Ligne d’ordre d’assemblage|Ressource||Groupe. Groupe compta. produit|  

Par conséquent, seuls les coûts réels sont validés dans la comptabilité, et aucun compte d’attente n’est renseigné à partir de la validation d’ordre d’assemblage. Pour plus d’informations, voir [Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Assembler pour commande
L’écriture comptable article qui résulte de la validation d’une vente assembler pour commande est lettrée de façon fixe sur l’écriture comptable article associée pour les résultats d’assemblage. Par conséquent, le coût d’une vente assembler pour commande est dérivé de l’ordre d’assemblage auquel la vente a été liée.  

Les écritures comptables article de type Vente qui résultent de la validation des quantités assemblées pour commande sont identifiées par **Oui** dans le champ **Assembler pour commande**.  

La validation de lignes commande vente dont une partie est une quantité en stock et une autre partie est une quantité à assembler pour commande entraîne la création d’écritures comptables article distinctes, une pour la quantité en stock et une pour la quantité à assembler pour commande.  

### <a name="posting-dates"></a>Dates comptabilisation

En général, les dates comptabilisation sont copiées d’une commande client vers l’ordre d’assemblage lié. La date comptabilisation dans l’ordre d’assemblage est automatiquement mise à jour lorsque vous modifiez la date comptabilisation dans la commande client directement ou indirectement, par exemple si vous modifiez la date comptabilisation dans l’expédition d’entrepôt, le prélèvement de stock ou dans le cadre d’une validation groupée.

Vous pouvez modifier manuellement la date comptabilisation dans l’ordre d’assemblage. Cependant, elle ne peut pas être postérieure à la date comptabilisation dans la commande client liée. Le système conservera cette date, à moins que vous ne mettiez à jour la date comptabilisation dans la commande client.


## <a name="see-also"></a>Voir aussi
 [Détails de conception : stock évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
