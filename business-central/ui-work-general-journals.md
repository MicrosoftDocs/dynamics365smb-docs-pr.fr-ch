---
title: Utilisation de feuilles comptabilité pour valider directement dans la comptabilité| Microsoft Docs
description: Découvrez comment utiliser les feuilles pour valider des transactions financières dans les comptes généraux et dans d’autres comptes, tels que les comptes bancaires et fournisseur.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 18c36bf409b2bb5d4e67eeccfdf16193ec4dac62
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760136"
---
# <a name="working-with-general-journals"></a>Utilisation de feuilles comptabilité

La plupart des transactions financières sont validées en comptabilité via les documents commerciaux dédiés, tels que des factures achat et des commandes vente. Mais vous pouvez également traiter des activités commerciales comme l’achat, le paiement, à l’aide des feuilles périodiques pour valider les régularisations, ou le remboursement des frais d’un salarié en validant des lignes feuille dans les diverses feuilles de [!INCLUDE[prod_short](includes/prod_short.md)].  

La plupart des feuilles sont basées sur la *Feuille comptabilité*, et vous pouvez traiter toutes les transactions sur la page **Feuille comptabilité**. Pour plus d’informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).  

Par exemple, vous pouvez valider les dépenses d’argent propre de vos salariés pour des activités liées à l’entreprise, afin de les rembourser ultérieurement. Pour plus d’informations, voir [Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).

Mais dans de nombreux cas, vous devrez utiliser les feuilles qui sont optimisées pour les types de transactions spécifiques, telles que **Feuille paiement** pour enregistrer les paiements. Pour plus d’informations, voir [Enregistrer les paiements et remboursements dans la feuille paiement](payables-how-post-payments-refunds.md).  

Les feuilles comptabilité vous permettent de valider des transactions financières directement dans les comptes généraux et dans d’autres comptes tels que les comptes bancaires, client, fournisseur et salarié. La validation avec une feuille comptabilité crée toujours des écritures dans les comptes généraux. C’est le cas même lorsque, par exemple, vous validez une ligne feuille dans un compte client, parce qu’une écriture est validée dans un compte client de la comptabilité via un groupe comptabilisation.

Les informations que vous saisissez dans une feuille sont temporaires et peuvent être modifiées tant qu’elles sont dans la feuille. Lorsque vous validez la feuille, les informations sont transférées vers des écritures de comptes individuels, où elles ne peuvent pas être modifiées. Toutefois, vous pouvez délettrer des écritures validées et valider des écritures de contrepassation ou de correction. Pour plus d’informations, voir [Inversion d’une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Utilisation de modèles feuille et feuilles

Il existe plusieurs modèles feuille. Chaque modèle feuille est représenté par une page dédiée avec des fonctions particulières et les champs nécessaires pour la prise en charge de ces fonctions, notamment la page **Feuille rapprochement bancaire** qui permet de traiter les paiements bancaires et la page **Feuille paiement** qui permet de payer vos fournisseurs ou rembourser vos employés. Pour plus d’informations, consultez [Exécuter des paiements](payables-make-payments.md) et [Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client](receivables-how-apply-sales-transactions-manually.md).

Pour chaque modèle feuille, vous pouvez configurer votre propre feuille personnelle sous forme de nom de feuille. Par exemple, vous pouvez définir votre propre nom de feuille pour la feuille paiement dotée de votre présentation et de vos paramètres personnels. Le conseil suivant est un exemple de la manière de personnaliser une feuille.

> [!TIP]  
> Si vous cochez la case **Suggérer le montant contrepartie** de la ligne pour votre nom feuille sur la page **Noms feuilles comptabilité**, le champ **Montant** dans, par exemple, les lignes feuille comptabilité pour le même numéro de document est automatiquement prérempli avec la valeur nécessaire à la contrepartie dans le document. Pour plus d’informations, voir [Laisser [!INCLUDE[prod_short](includes/prod_short.md)] suggérer des valeurs](ui-let-system-suggest-values.md).

> [!TIP]
> Pour ajouter ou supprimer des champs dans des journaux, utilisez la bannière **Personnalisation**. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Validation Noms feuilles comptabilité
Pour éviter les retards lors de la validation, vous pouvez activer une vérification des antécédents qui vous avertira en cas d’erreur dans la feuille financière sur laquelle vous travaillez et qui vous empêchera de valider la feuille. Sur la page **Noms feuilles comptabilités**, vous pouvez choisir **Vérification des erreurs d’arrière-plan** pour que [!INCLUDE[prod_short](includes/prod_short.md)] valide les feuilles financières, telles que les feuilles comptabilité ou règlements, pendant que vous les utilisez. 

Lorsque vous activez la validation, le Récapitulatif **Vérification de feuille** s’affiche à côté des lignes feuille et affiche les problèmes de la ligne actuelle et du lot entier. La validation se produit lorsque vous chargez une Feuille financière et lorsque vous choisissez une autre ligne feuille. La vignette **Nombre total d’erreurs** du Récapitulatif montre le nombre total de problèmes que [!INCLUDE[prod_short](includes/prod_short.md)] a trouvées, et vous pouvez le choisir pour ouvrir un aperçu des problèmes. 

Vous pouvez utiliser les actions **Afficher les lignes avec des problèmes** et **Afficher toutes les lignes** pour basculer entre les lignes feuille qui ont ou n’ont pas de problèmes. Le nouveau Récapitulatif **Détails de la ligne feuille** fournit un aperçu rapide et un accès aux données des lignes feuille, telles que le compte général, le client ou le fournisseur, ainsi que la configuration de la validation pour des comptes spécifiques.     

### <a name="reversing-journals-to-correct-mistakes"></a>Annulation de feuilles pour corriger les erreurs
Lorsque vous travaillez avec des feuilles qui comportent de nombreuses lignes et que quelque chose ne va pas, il est important de disposer d’un moyen simple de corriger les erreurs. La page **Feuille comptabilité validée** propose quelques actions qui peuvent vous aider.

* **Copier les lignes sélectionnées dans la feuille** : Copiez uniquement les lignes que vous sélectionnez.
* **Copier l’historique des transactions de comptabilité dans la feuille** : Copiez toutes les lignes appartenant au même historique des transactions de comptabilité.

Ces actions vous permettent de créer une copie d’une ligne feuille comptabilité ou d’un lot, puis de spécifier les éléments suivants :

* La feuille dans laquelle copier les lignes
* Avec ou sans signes opposés (une feuille de contrepassation)
* Une date comptabilisation ou un numéro de document différent

Pour permettre la copie de feuilles dans des feuilles comptabilité validées, sur la page **Modèles de feuilles comptabilité**, cochez la case **Copier sur les lignes feuille validées**. Une fois que vous avez autorisé les utilisateurs à copier des feuilles comptabilité validées, si nécessaire, vous pouvez désactiver la copie pour des lots spécifiques.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Compte principaux et comptes contrepartie
Si vous avez configuré des comptes contrepartie par défaut pour les feuilles sur la page **Feuilles comptabilité**, le compte contrepartie sera renseigné automatiquement lorsque vous renseignez le champ **Numéro du compte**. Sinon, renseignez manuellement les champs **Numéro du compte** et **N° compte contrepartie**. Un montant positif dans le champ **Montant** est débité du compte principal et crédité dans le compte contrepartie. Un montant négatif est crédité sur le compte principal et débité du compte contrepartie.

> [!NOTE]  
>   La TVA est calculée séparément pour le compte principal et le compte contrepartie, afin qu’ils puissent utiliser des taux de pourcentage de TVA différents.

## <a name="working-with-recurring-journals"></a>Utilisation de feuilles abonnement
Une feuille abonnement est une feuille comptabilité contenant des champs spécifiques pour la gestion des transactions que vous validez fréquemment avec peu ou pas de modifications comme le bail, les abonnements, l’électricité et le chauffage. Utilisez ces champs dans le cadre des transactions récurrentes pour valider les montants fixes et variables. Vous pouvez également définir des écritures de contrepassation automatique le lendemain de la date de validation. Vous pouvez également utiliser les clés de ventilation pour répartir les écritures récurrentes entre plusieurs comptes. Pour plus d’informations, reportez-vous à [Ventilation des montants feuille abonnement sur plusieurs comptes](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Avec une feuille abonnement, les écritures qui sont régulièrement validées ne sont saisies qu’une fois. Les comptes, axes, sections analytiques, etc., que vous saisissez restent ainsi dans la feuille après validation. Si des ajustements sont nécessaires, vous pouvez les faire à chaque validation.

### <a name="recurring-method-field"></a>Champ Mode abonnement
Ce champ détermine la manière dont le montant de la ligne feuille est traité après validation. Par exemple, si vous utilisez le même montant chaque fois que vous validez la ligne, vous pouvez conserver ce montant. Si vous utilisez les mêmes comptes et le même texte pour la ligne mais que le montant varie chaque fois que vous validez, vous pouvez choisir de supprimer le montant après validation.

| À | Voir |
| --- | --- |
|Statique|Le montant de la ligne feuille est conservé après validation.|
|Variable|Le montant de la ligne feuille est supprimé après validation.|
|Solde|Le montant validé sur le compte de la ligne est ventilé sur les comptes spécifiés pour la ligne de la table Ventilation feuille compta. Le solde du compte est donc positionné à zéro. Pensez à renseigner le champ **% ventilation** sur la page **Ventilations**. Pour plus d’informations, reportez-vous à [Ventilation des montants feuille abonnement sur plusieurs comptes](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|FI Fixe Inverse|Le montant de la ligne feuille est conservé après validation, et une écriture contrepartie est validée le lendemain.|
|VI Variable Inverse|Le montant de la ligne feuille est supprimé après validation, et une écriture contrepartie est validée le lendemain.|
|SI Solde Inverse|Le montant validé sur le compte de la ligne est ventilé sur les comptes spécifiés pour la ligne de la page **Ventilations**. Le solde du compte est défini sur zéro, et une écriture contrepartie est validée le lendemain.|

> [!NOTE]  
>  Les champs TVA peuvent être renseignés sur la ligne feuille abonnement ou sur la ligne feuille ventilation, mais pas sur les deux. Ils peuvent être renseignés sur la page **Ventilations** uniquement si les lignes correspondantes de la feuille abonnement ne sont pas renseignées.

### <a name="recurring-frequency-field"></a>Champ Périodicité abonnement
Ce champ détermine la fréquence de validation de l’écriture de la ligne feuille. Il s’agit d’un champ de formule de date qui doit être renseigné pour les lignes feuille abonnement. Pour plus d’informations, voir [Utilisation de formules date](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Exemples
Si la ligne feuille doit être validée tous les mois, saisissez "1M." Après chaque validation, la date du champ **Date comptabilisation** est mise à jour, elle est remplacée par la même date du mois suivant.

Si vous souhaitez valider une écriture le dernier jour de chaque mois, vous pouvez suivre l’un des deux exemples ci-dessous :

- Validez la première écriture le dernier jour d’un mois en saisissant la formule 1J+1M-1J (1 jour + 1 mois - 1 jour). Avec cette formule, la date de validation est calculée correctement, quel que soit le nombre de jours que comprend le mois.

- Validez la première écriture n’importe quel jour en saisissant la formule : 1M+FM. Avec cette formule, la date de validation sera située après un mois entier + le nombre de jours restants du mois en cours.

### <a name="expiration-date-field"></a>Champ Date expiration
Ce champ détermine la date à laquelle la ligne est validée pour la dernière fois. La ligne n’est plus validée après cette date.

L’avantage d’utiliser ce champ réside dans le fait que la ligne n’est pas immédiatement supprimée de la feuille et que vous pouvez toujours remplacer la date d’expiration par une date ultérieure afin de pouvoir continuer à utiliser la ligne.

Si le champ est blanc, la ligne est validée à chaque validation, jusqu’à ce qu’elle soit supprimée de la feuille.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Ventilation des montants feuille abonnement sur plusieurs comptes
Sur la page **Feuille abonnement**, vous pouvez choisir l’action **Ventilations** pour visualiser ou gérer la manière dont les montants de la ligne feuille abonnement sont affectés à plusieurs comptes et axes analytiques. Notez qu’une ventilation fonctionne comme une ligne compte contrepartie pour la ligne feuille abonnement.

Tout comme dans une feuille abonnement, vous n’avez à saisir qu’une fois une ventilation. La ventilation reste dans la feuille ventilation après validation, ainsi vous n’avez pas à saisir les montants et les ventilations chaque fois que vous validez la ligne feuille abonnement.

Si le mode récurrent est paramétré sur **Solde** ou sur **Solde inverse**, tous les codes axe analytique de la feuille récurrente sont ignorés lorsque le compte est défini sur zéro. Par conséquent, si vous ventilez une ligne abonnement vers diverses sections analytiques sur la page **Ventilations**, une seule écriture opposée est créée. De ce fait, si vous ventilez une ligne feuille abonnement qui comporte un code section, vous ne devez pas saisir le même code sur la page **Ventilations**. Si vous le faites, les sections analytiques sont incorrectes.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Exemple : Ventilation des paiements du loyer entre plusieurs départements
Vous payez un loyer tous les mois, vous avez saisi le montant du loyer sur le compte règlement d’une ligne feuille abonnement. Sur la page **Ventilations**, vous pouvez diviser les dépenses entre plusieurs départements (section analytique Département) selon le nombre de mètres carrés occupé par chacun d’eux. Le calcul est basé sur le pourcentage de ventilation de chaque ligne. Vous pouvez saisir divers comptes sur différentes lignes ventilation (si le loyer est aussi divisé entre plusieurs comptes) ou saisir le même compte, mais avec divers codes section de la section analytique Département sur chaque ligne.

### <a name="reversal-date-calculation"></a>Calcul de date de contrepassation
Lorsque vous utilisez des feuilles comptabilité périodiques pour comptabiliser les régularisations à la fin d’une période, il est important d’avoir un contrôle total sur les écritures de contrepassation. Sur la page **Feuilles comptabilité périodiques**, le champ **Calcul de date de contrepassation** vous permet de contrôler la date à laquelle les écritures de contrepassation seront validées lorsque les méthodes de contrepassation périodiques seront utilisées.

#### <a name="example"></a>Exemple :
Les régularisations sont généralement validées avec des méthodes périodiques Fixe, Variable ou Solde sur la ligne feuille. La date comptabilisation du montant comptabilisé sur le compte sur la ligne feuille est calculée en utilisant la fréquence périodique. La date comptabilisation de l’écriture contrepartie est calculée à l’aide du champ **Calcul de la date de contrepassation**, comme suit :

* Si le champ est vide, l’écriture contrepartie sera validée le jour suivant.
* Si le champ contient une formule de date (par exemple, **5D** pendant cinq jours), l’écriture contrepartie sera validée avec une date comptabilisation calculée à l’aide du calcul de la date de contrepassation.

> [!NOTE]
> Par défaut, le champ **Calcul de la date de contrepassation** n’est pas disponible sur la page **Feuilles comptabilité périodiques**. Pour utiliser le champ, vous devez l’ajouter en personnalisant la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## <a name="working-with-standard-journals"></a>Utilisation de feuilles standard
Lorsque vous créez des lignes feuille dont vous savez que vous risquez de les recréer ultérieurement, vous pouvez les enregistrer en tant que feuille standard avant de valider la feuille. Cette fonctionnalité s’applique aux feuilles article et aux feuilles comptabilité.

> [!NOTE]  
>   la procédure suivante traite de la feuille article mais concerne également la feuille comptabilité.

### <a name="to-save-a-standard-journal"></a>Pour enregistrer une feuille standard
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles article**, puis sélectionnez le lien associé.
2. Entrez le code sur une ou plusieurs lignes feuille.
3. Sélectionnez les lignes feuille à réutiliser.
4. Choisissez l’action **Enregistrer en tant que feuille standard**.
5. Sur la page de demande **Enregistrer en tant que feuille standard**, définissez une feuille article standard, nouvelle ou existante, dans laquelle enregistrer les lignes.

    Si vous avez déjà créé une ou plusieurs feuilles article standard et souhaitez en remplacer une avec la nouvelle série de lignes feuille article, dans le champ Code, sélectionnez le code souhaité.
6. Cliquez sur le bouton **OK** pour vérifier que vous souhaitez écraser la feuille article standard existante et remplacer tout son contenu.
7. Sélectionnez le champ **Enregistrer le montant unitaire** si vous souhaitez enregistrer les valeurs dans le champ **Montant unitaire** de la feuille article standard.
8. Sélectionnez le champ **Enregistrer la quantité** si vous souhaitez que l’application enregistre les valeurs dans le champ **Quantité**.
9. Cliquez sur le bouton **OK** pour enregistrer la feuille article standard.

Une fois l’enregistrement de la feuille article standard effectué, la page Feuille article s’affiche. Vous pouvez alors procéder à la validation tout en sachant que vous pouvez très facilement recréer cette feuille si vous devez valider des lignes identiques ou analogues.

### <a name="to-reuse-a-standard-journal"></a>Pour réutiliser une feuille standard
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles article**, puis sélectionnez le lien associé.
2. Choisissez l’action **Obtenir les feuilles standard**.

    La page Feuilles article standard qui s’ouvre alors contient des codes et des descriptions de toutes les feuilles article standard existantes.
3. Pour passer en revue une feuille article standard avant de la sélectionner pour la réutiliser, choisissez l’action **Afficher la feuille**.

    Toutes les modifications que vous apportez dans une feuille article standard sont effectuées immédiatement. Elles seront là la prochaine fois que vous rouvrirez ou réutiliserez la feuille article en question. Il est donc recommandé de s’assurer que la modification en question est suffisamment importante pour devoir s’appliquer de manière générale. Sinon, effectuez la correction ponctuelle dans la feuille article après avoir inséré les lignes feuille article standard. Reportez-vous à l’étape 4 ci-dessous.
4. Sur la page **Feuilles article standard**, sélectionnez la feuille article standard à réutiliser et cliquez sur le bouton **OK**.

    La feuille article est alors remplie avec les lignes enregistrées en tant que feuille article standard. Si des lignes feuille figurent déjà dans la feuille article, les lignes insérées sont placées en dessous.

    Si vous n’avez pas coché le champ **Enregistrer le montant unitaire** au cours de la tâche de fonction **Enregistrer en tant que feuille article standard**, alors le champ **Montant unitaire** des lignes insérées adopte automatiquement la valeur actuelle de l’article, copiée du champ **Coût unitaire** de la fiche article.

    > [!NOTE]  
    >   Si vous avez sélectionné les champs **Enregistrer le montant unitaire** ou **Enregistrer la quantité**, assurez-vous que les valeurs insérées sont adaptées à cet ajustement de stock précis avant de valider la feuille article.

    Si les lignes feuille article insérées contiennent des montants unitaires enregistrés que vous ne souhaitez pas valider, vous pouvez rapidement les ajuster à la valeur actuelle de l’article comme suit.

6. Sélectionnez les feuilles articles standard que vous souhaitez ajuster, puis sélectionnez l’action **Recalculer le montant unitaire**. Le champ Montant unitaire est mis à jour avec le coût unitaire actuel de l’article.
7. Sélectionnez l’action **valider**.

## <a name="to-renumber-document-numbers-in-journals"></a>Pour renuméroter des numéros de document dans les feuilles
Pour vous assurer de ne pas recevoir d’erreurs de validation en raison de l’ordre des numéros de document, vous pouvez utiliser la fonction **Renuméroter les numéros de document** avant de valider une feuille.

Dans toutes les feuilles basées sur la feuille comptabilité, le champ **N° document** est modifiable de sorte que vous puissiez spécifier des numéros de document différents pour des lignes feuille différentes, ou le même numéro de document pour les lignes feuille associées.

Si le champ **Souches de n°** du nom feuille est rempli, la fonction de validation dans les feuilles comptabilité nécessite que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Pour vous assurer de ne pas recevoir d’erreurs de validation en raison de l’ordre des numéros de document, vous pouvez utiliser la fonction **Renuméroter les numéros de document** avant de valider la feuille. Si les lignes feuille associées ont été regroupées par numéro de document avant d’utiliser la fonction, elles resteront groupées, mais peuvent être affectées à un autre numéro de document.

Cette fonction fonctionne également sur les vues filtrées.

Toute renumérotation des numéros de document respectera les lettrages associés, par exemple un lettrage de paiement qui a été effectué à partir du document de la ligne feuille pour un compte fournisseur. Par conséquent, les champs **ID lettrage** et les champs **N° doc. lettrage** sur les écritures comptables affectées peuvent être mis à jour.

La procédure suivante est basée sur la page **Feuille comptabilité**, mais s’applique à toutes les autres feuilles qui sont basées sur la feuille comptabilité, tel que la page **Feuille paiement**.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé.
2. Lorsque vous êtes prêt à valider la feuille, choisissez l’action **Renuméroter les numéros de document**.

Les valeurs dans le champ **N° document** sont modifiées, le cas échéant, pour que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Une fois que les documents sont renumérotés, vous pouvez procéder à la validation de la feuille.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi

[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Contrepasser une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md)  
[Répartition des coûts et du revenu](year-allocate-costs-income.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Réévaluer le stock dans la Feuille réévaluation](inventory-how-revalue-inventory.md)  
[Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md)  
[Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client](receivables-how-apply-sales-transactions-manually.md)  
[Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md)  
[Utiliser les documents et les feuilles intersociétés](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]