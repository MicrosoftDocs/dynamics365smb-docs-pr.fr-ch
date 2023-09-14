---
title: "Détails de conception\_: ajustement des coûts"
description: 'L’ajustement des coûts transfère les changements depuis les coûts des sources de coût aux destinataires de coût, selon le mode évaluation stock d’un article, pour fournir une évaluation du stock correcte.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="design-details-cost-adjustment"></a>Détails de conception : ajustement des coûts

L’objet principal de l’ajustement des coûts est de transférer les changements depuis les coûts des sources de coût aux destinataires de coût, selon le mode évaluation stock d’un article, pour fournir une évaluation du stock correcte.  

Un article peut faire l’objet d’une facture vente avant d’avoir été l’objet d’une facture achat, de sorte que la valeur de stock enregistrée de la vente ne corresponde pas au coût d’achat réel. L’ajustement des coûts met à jour le coût des biens vendus (COGS) des écritures vente historiques afin de s’assurer qu’elles correspondent aux coûts des transactions entrantes sur lesquelles elles sont appliquées. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-application.md).  

Voici l’autre objectif ou les autres fonctions de l’ajustement des coûts :  

* Facturer les ordres de fabrication terminés :  

  * Modifiez le statut des écritures valeur de **Prévu** en **Réel**.  
  * Effacer les comptes en-cours. Pour plus d’informations, voir [Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md).  
  * Validez l’écart. Pour plus d’informations, consultez [Détails de conception : écart](design-details-variance.md)  
  * Mettre à jour le coût unitaire de la fiche article.  

Les coûts de stock doivent être ajustés avant que les écritures valeur associées puissent être rapprochées avec les écritures comptables. Pour plus d’informations, voir [Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Détection de l’ajustement

La tâche de détecter si l’ajustement des coûts doit se produire est surtout effectuée par la routine Item Jnl.-Post Line, tandis que la tâche de calculer et générer des écritures d’ajustement des coûts est effectuée par le traitement par lots **Ajuster coûts - Écr. article**.  

Pour pouvoir transférer les coûts, le mécanisme de détection de détermine quelles sources ont changé en termes de coûts et vers quelle destination ces coûts doivent être transférés. Les trois fonctions de détection suivantes sont disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)] :  

* Écriture lettrage article  
* Point d’entrée d’ajustement de coût moyen  
* Niveau de commande  

### <a name="item-application-entry"></a>Écriture lettrage article

Cette fonction de détection est utilisée pour les articles qui utilisent les méthodes de coûts FIFO, LIFO, Standard et Specific et pour les scénarios d’applications fixes. La fonction opère comme suit :  

* L’ajustement des coûts est détecté en marquant les écritures comptables article d’origine en tant qu’*Écriture lettrée à ajuster* lorsqu’une écriture comptable article ou une écriture valeur article est validée.  
* Les coûts sont transférés en fonction des chaînes de coût qui sont stockées dans la table **Ecriture lettrage article**.  

### <a name="average-cost-adjustment-entry-point"></a>Point d’entrée d’ajustement de coût moyen

Cette fonction de détection est utilisée pour les articles qui utilisent le mode de coûts Average. La fonction opère comme suit :  

* L’ajustement des coûts est détecté en marquant un enregistrement dans la table **Point d’entrée ajustement coût moyen** chaque fois qu’une écriture valeur est validée.  
* Les coûts sont transférés en appliquant les coûts ajustés aux écritures valeur avec une date évaluation ultérieure.  

### <a name="order-level"></a>Niveau de commande

Cette fonction de détection est utilisée pour les scénarios de conversion, la production et l’assemblage. La fonction opère comme suit :  

* L’ajustement des coûts est détecté en marquant la commande chaque fois que des matières/ressources sont validées comme étant consommées/utilisées pour la commande.  
* Les coûts sont transférés en appliquant les coûts des matières/ressources aux écritures de production liées à la même commande.  

La fonction Niveau de commande est utilisée pour détecter les ajustements dans la validation d’assemblage. Le graphique suivant montre la structure d’écriture d’ajustement :  

![Flux des écritures dans l’ajustement des coûts.](media/design_details_assembly_posting_3.png "Flux des écritures dans l’ajustement des coûts")  

Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Comparaison entre ajustement des coûts automatique et manuel

Vous pouvez exécuter l’ajustement des coûts de deux manières :  

* Manuellement, en exécutant le traitement par lots **Ajuster coûts - Écr. article**. Vous pouvez exécuter ce traitement par lots pour tous les articles ou pour certains articles ou catégories d’article uniquement. Ce traitement par lots effectue un ajustement des coûts pour les articles du stock pour lesquels une transaction entrante a été réalisée, tel qu’un achat. Pour les articles qui utilisent le mode évaluation stock moyen, le traitement par lots effectue également un ajustement si les transactions sortantes sont créées.  
* Automatiquement, en ajustant les coûts chaque fois que vous validez un mouvement de stock et que vous clôturez un ordre de fabrication. L’ajustement des coûts est effectué uniquement pour l’article ou les articles spécifiques affectés par la validation. Ceci est configuré lorsque vous cochez la case **Ajustement automatique des coûts** sur la page **Paramètres stock**.  

C’est une bonne pratique d’exécuter l’ajustement des coûts automatiquement lors de la validation car les coûts unitaires sont plus fréquemment mis à jour et donc plus justes. L’inconvénient est que les performances de la base de données peut être affectées en exécutant l’ajustement des coûts si souvent.  

Comme il est important de mettre le coût unitaire d’un article à jour, il est recommandé d’exécuter le traitement par lots pour **Ajuster coûts - Écr. article** aussi souvent que possible, en dehors des heures de travail. Sinon, utilisez l’ajustement automatique des coûts. Cela garantit que le coût unitaire est mis à jour quotidiennement pour les articles.  

Que l’exécution de l’ajustement des coûts soit manuel ou automatique, le processus d’ajustement et ses conséquences sont les mêmes. [!INCLUDE[prod_short](includes/prod_short.md)] calcule la valeur de la transaction entrante et affecte également ce coût à toutes les transactions sortantes, telles que les ventes ou les consommations, qui ont été lettrées sur la transaction entrante. L’ajustement des coûts crée des écritures valeur qui contiennent des montants d’ajustement et des montants qui compensent l’arrondi.  

Les nouvelles écritures valeur ajustement et arrondi ont la date comptabilisation de la facture associée. Les exceptions sont si les écritures valeur tombent dans une période comptable ou une période inventaire clôturée ou si la date comptabilisation est antérieure à la date du champ **Début période validation** sur la page **Paramètres comptabilité**. Si cela se produit, le traitement par lots affecte la date comptabilisation comme la première date de la période ouverte suivante.  

## <a name="adjust-cost---item-entries-batch-job"></a>Traitement par lots Ajuster coûts - Écr. article

Lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, vous avez la possibilité d’exécuter le traitement par lots pour tous les articles ou pour certains articles ou catégories uniquement.  

> [!NOTE]  
> Nous vous recommandons de toujours exécuter le traitement par lots pour tous les articles et utilisez uniquement l’option de filtrage pour réduire le temps d’exécution du traitement par lots, ou pour résoudre le coût d’un article donné.  

### <a name="example"></a>Exemple :

L’exemple suivant montre le cas où vous validez un article acheté comme étant reçu et facturé le 01/01/20. Vous validez ultérieurement l’article vendu comme étant expédié et facturé le 01-15-20. Ensuite, vous exécutez les traitements par lots **Ajuster coûts - Écr. article** et **Valider coûts ajustés**. Les écritures suivantes sont créées.  

#### <a name="value-entries-1"></a>Écritures valeur (1)

|Date comptabilisation|Type écriture comptable article|Coût total (réel)|Coût validé en comptabilité|Quantité facturée|Numéro de la séquence|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01/01/20|Achats|10,00|10,00|1|1|  
|15/01/20|Vente|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Liens écritures dans la comptabilité – Table Écriture comptable article (1)

|N° séquence compta.|N° écriture valeur|N° hist. transaction compta.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Écritures comptables (1)

|Date comptabilisation|Compte général|N° compte (démonstration Fr-FR)|Montant|Numéro de la séquence|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01/01/20|[Compte stocks]|2 130|10,00|1|  
|01/01/20|[Compte coût direct lettré]|7 291|-10,00|2|  
|15/01/20|[Compte stocks]|2 130|-10,00|3|  
|15/01/20|[Compte variation stock]|7 290|10,00|4|  

Ultérieurement, vous validez des frais annexes achat associés de 2,00 DS facturés le 10/02/20. Vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, puis le traitement par lots **Valider coûts ajustés**. Le traitement par lots d’ajustement des coûts ajuste le coût de la vente de 2,00 DS en conséquence, et le traitement par lots **Valider coûts ajustés** valide les nouvelles écritures valeur en comptabilité. Le résultat est le suivant.  

#### <a name="value-entries-2"></a>Écritures valeur (2)

|Date comptabilisation|Type écriture comptable article|Coût total (réel)|Coût validé en comptabilité|Quantité facturée|Ajustement|Numéro de la séquence|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|10/02/20|Achats|2,00|2,00|0|Non|3|  
|15/01/20|Vente|-2,00|-2,00|0|Oui|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Liens écritures dans la comptabilité – Table Écriture comptable article (2)

|N° séquence compta.|N° écriture valeur|N° hist. transaction compta.|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Écritures comptables (2)

|Date comptabilisation|Compte général|N° compte (démonstration Fr-FR)|Montant|Numéro de la séquence|  
|------------|-----------|------------------------|------|---------|  
|10/02/20|[Compte stocks]|2 130|2,00|5|  
|10/02/20|[Compte coût direct lettré]|7 291|-2,00|6|  
|15/01/20|[Compte stocks]|2 130|-2,00|7|  
|15/01/20|[Compte variation stock]|7 290|2,00|8|  

## <a name="automatic-cost-adjustment"></a>Ajustement automatique des coûts

Pour configurer l’ajustement des coûts à exécuter automatiquement lorsque vous validez une transaction de stock, utilisez le champ **Ajustement automatique des coûts** sur la page **Paramètres stock**. Ce champ vous permet de sélectionner jusqu’où dans le passé vous voulez que l’ajustement automatique des coûts soit effectué. Les options possibles sont les suivantes.  

|Option|Désignation|
|------|-----------|
|Jamais|Les coûts ne sont jamais ajustés lors de la validation.|  
|Jour|Les coûts sont ajustés si la validation a lieu dans la journée commençant à la date de travail.|  
|Semaine|Les coûts sont ajustés si la validation a lieu dans la semaine commençant à la date de travail.|  
|Mois|Les coûts sont ajustés si la validation a lieu dans le mois commençant à la date de travail.|  
|Trimestre|Les coûts sont ajustés si la validation a lieu dans le trimestre commençant à la date de travail.|  
|Année|Les coûts sont ajustés si la validation a lieu dans l’année commençant à la date de travail.|  
|Toujours|Les coûts sont systématiquement ajustés en cas de validation, quelle que soit la date de comptabilisation.|  

La sélection effectuée dans le champ **Ajustement automatique des coûts** est importante pour les performances et la précision et de vos coûts. Des périodes plus courtes, telles que **Jour** ou **Semaine**, affectent moins les performances système, car elles offrent la condition plus stricte que seuls les prix validés le jour ou la semaine précédente peuvent être automatiquement ajustés. Cela signifie que l’ajustement automatique des coûts n’est pas effectué aussi fréquemment et affecte donc moins les performances du système. Toutefois, cela signifie également que les coûts unitaires peuvent être moins précis.  

### <a name="example-1"></a>Exemple :

L’exemple suivant présente scénario d’ajustement automatique des coûts :  

* Le 10 janvier, vous validez un article acheté comme étant reçu ou facturé.  
* Le 15 janvier, vous validez une commande vente pour l’article comme étant expédié et facturé.
* Le 5 février, vous recevez une facture pour des frais de transport sur l’achat initial. Vous validez ces frais de fret, en les appliquant à la facture achat originale, qui augmente le coût de l’achat d’origine.  

Si vous avez défini l’ajustement automatique des coûts pour l’appliquer aux validations qui se produisent à un mois ou une trimestre de la date en cours, l’ajustement automatique des coûts fonctionne et transmet le coût de l’achat à la vente.  

Si vous avez défini l’ajustement automatique des coûts pour l’appliquer aux validations qui se produisent à un jour ou une semaine de la date en cours, l’ajustement automatique des coûts ne fonctionne pas, et le coût de l’achat n’est pas transmis à la vente jusqu’à ce que vous exécutiez le traitement par lots **Ajuster coûts - Écr. article**.  

## <a name="see-also"></a>Voir aussi

[Ajuster coûts et prix article](inventory-how-adjust-item-costs.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md)  
[Détails de conception : comptabilisation stock](design-details-inventory-posting.md)  
[Détails de conception : écart](design-details-variance.md)  
[Détails de conception : validation d’ordre d’assemblage](design-details-assembly-order-posting.md)  
[Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
