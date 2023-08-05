---
title: Utilisation de feuilles comptabilité pour valider directement dans la comptabilité
description: 'Découvrez comment utiliser les feuilles pour valider des transactions financières dans les comptes généraux et dans d’autres comptes, tels que les comptes bancaires et fournisseur.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/27/2022
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# Utiliser des feuilles comptabilité

La plupart des transactions financières sont validées en comptabilité via les documents, tels que des factures achat et des commandes vente. Cependant, vous pouvez également traiter des activités commerciales telles que :

* Achats
* Paiements
* Utilisation de feuilles abonnement pour valider les régularisations
* Remboursement des dépenses des employés en validant des lignes feuille dans les feuilles  

La plupart des feuilles sont basées sur la feuille comptabilité, et vous pouvez traiter toutes les transactions sur la page **Feuille comptabilité**. En savoir plus sur [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).  

Par exemple, vous pouvez utiliser les dépenses des employés pour le remboursement. En savoir plus sur [Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).

Cependant, [!INCLUDE [prod_short](includes/prod_short.md)] propose également des feuilles qui sont optimisées pour les types de transactions spécifiques, telles que **Feuille paiement** pour enregistrer les paiements. Pour plus d’informations, consultez [Enregistrer les paiements et remboursements dans la feuille paiement](payables-how-post-payments-refunds.md).  

Vous utilisez les feuilles comptabilité pour valider des transactions financières dans les comptes généraux et autres comptes divers. Parmi les autres comptes figurent les comptes bancaires, clients, fournisseurs et employés. La validation avec une feuille comptabilité génère des écritures sur les comptes généraux même lorsque, par exemple, vous validez une ligne feuille sur un compte client. L’écriture est validée sur un compte client général via un groupe de validation.

Les informations que vous saisissez dans une feuille sont temporaires et peuvent être modifiées tant qu’elles sont dans la feuille. Lorsque vous validez la feuille, les informations sont transférées vers des écritures de comptes individuels, où elles ne peuvent pas être modifiées. Toutefois, vous pouvez délettrer des écritures validées et valider des écritures de contrepassation ou de correction. En savoir plus, [Inverser des validations feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## Utiliser des modèles feuille et des feuilles

Il existe plusieurs modèles feuille. Chaque modèle feuille est représenté par une page dédiée avec des fonctions particulières et les champs nécessaires pour la prise en charge de ces fonctions, notamment la page **Feuille rapprochement bancaire** qui permet de traiter les paiements bancaires et la page **Feuille paiement** qui permet de payer vos fournisseurs ou rembourser vos employés. Pour plus d’informations, consultez [Exécuter des paiements](payables-make-payments.md) et [Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client](receivables-how-apply-sales-transactions-manually.md).

Pour chaque modèle feuille, vous pouvez configurer votre propre feuille personnelle sous forme de nom de feuille. Par exemple, vous pouvez définir votre propre nom de feuille pour la feuille paiement dotée de votre présentation et de vos paramètres personnels. Le conseil suivant est un exemple de la manière de personnaliser une feuille.

> [!TIP]  
> Si vous cochez la case **Suggérer le montant contrepartie** de la ligne pour votre nom feuille sur la page **Noms feuilles comptabilité**, le champ **Montant** dans, par exemple, les lignes feuille comptabilité pour le même numéro de document est automatiquement prérempli avec la valeur nécessaire à la contrepartie dans le document. Learn more at [Laisser [!INCLUDE[prod_short](includes/prod_short.md)] suggérer des valeurs](ui-let-system-suggest-values.md).

> [!TIP]
> Vous pouvez ajouter ou supprimer des champs dans les feuilles en personnalisant celles-ci. Pour plus d’informations, consultez [Personnaliser votre espace de travail](ui-personalization-user.md).

### Validation Noms feuilles comptabilité

Vous pouvez activer une vérification des antécédents qui aidera à éviter les retards lors de la validation. Le contrôle vous informe lorsqu’une erreur dans le journal financier sur lequel vous travaillez vous empêche de valider le journal. Sur la page **Noms feuilles comptabilités**, vous pouvez choisir **Vérification des erreurs d’arrière-plan** pour que [!INCLUDE[prod_short](includes/prod_short.md)] valide les feuilles financières, telles que les feuilles comptabilité ou règlements, pendant que vous les utilisez.

Lorsque vous activez la validation, le Récapitulatif **Vérification de feuille** affiche les problèmes de la ligne actuelle et du lot entier. La validation se produit lorsque vous chargez une Feuille financière et lorsque vous choisissez une autre ligne feuille. La vignette **Nombre total d’erreurs** du Récapitulatif montre le nombre total de problèmes que [!INCLUDE[prod_short](includes/prod_short.md)] a trouvées, et vous pouvez le choisir pour ouvrir un aperçu des problèmes.

Vous pouvez utiliser les actions **Afficher les lignes avec des problèmes** et **Afficher toutes les lignes** pour basculer entre les lignes feuille qui ont ou n’ont pas de problèmes. Le nouveau Récapitulatif **Détails de la ligne feuille** fournit un aperçu rapide et un accès aux données des lignes feuille, telles que le compte général, le client ou le fournisseur, ainsi que la configuration de la validation pour des comptes spécifiques.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## Compte principaux et comptes contrepartie

Si vous avez configuré des comptes contrepartie par défaut pour les feuilles sur la page **Feuilles comptabilité**, le compte contrepartie sera renseigné automatiquement lorsque vous renseignez le champ **Numéro du compte**. Sinon, renseignez manuellement les champs **Numéro du compte** et **N° compte contrepartie**. Un montant positif dans le champ **Montant** est débité du compte principal et crédité dans le compte contrepartie. Un montant négatif est crédité sur le compte principal et débité du compte contrepartie.

> [!NOTE]  
> La TVA est calculée séparément pour le compte principal et le compte contrepartie, afin qu’ils puissent utiliser des taux de pourcentage de TVA différents.

## Utiliser des feuilles abonnement

Une feuille abonnement est une feuille comptabilité contenant des champs spécifiques pour la gestion des transactions que vous validez fréquemment avec peu ou pas de modifications. Par exemple, les transactions pour les dépenses telles que le loyer, les abonnements, l’électricité et le chauffage. L’utilisation de feuilles abonnement vous permet de valider des montants fixes et variables et de spécifier des écritures d’annulation automatique pour le jour suivant la date de validation. Les clés de ventilation vous permettent de répartir les écritures récurrentes entre plusieurs comptes. Learn more at [Ventilation des montants feuille abonnement sur plusieurs comptes](#allocating-recurring-journal-amounts-to-several-accounts).

Avec une feuille abonnement, vous ne créez les écritures qui sont régulièrement validées qu’une fois. Par exemple, les comptes, axes, sections analytiques, etc. que vous saisissez restent dans la feuille après validation. Si des modifications sont nécessaires, vous pouvez les apporter à chaque validation.

### Champ Mode abonnement

Le champ **Mode abonnement** est important. Il détermine la manière dont le montant de la ligne feuille est traité après validation. Par exemple, si vous utilisez le même montant chaque fois que vous validez la ligne, vous pouvez conserver ce montant. Si vous utilisez les mêmes comptes et le même texte pour la ligne, mais que le montant varie chaque fois que vous validez, vous pouvez choisir de supprimer le montant après validation.

| À | Voir |
| --- | --- |
|F Fixe|Le montant de la ligne feuille est conservé après validation.|
|V Variable|Le montant de la ligne feuille est supprimé après validation.|
|S Solde|Le montant validé sur le compte de la ligne est ventilé sur les comptes spécifiés pour la ligne de la table Ventilation feuille compta. Le solde du compte est positionné à zéro. Pensez à renseigner le champ **% ventilation** sur la page **Ventilations**. Pour plus d’informations, reportez-vous à [Ventilation des montants feuille abonnement sur plusieurs comptes](#allocating-recurring-journal-amounts-to-several-accounts).|
|FI Fixe inverse|Le montant de la ligne feuille est conservé après validation, et une écriture contrepartie est validée le lendemain.|
|VI Variable inverse|Le montant de la ligne feuille est supprimé après validation, et une écriture contrepartie est validée le lendemain.|
|SI Solde inverse|Le montant validé sur le compte de la ligne est ventilé sur les comptes spécifiés pour la ligne de la page **Ventilations**. Le solde du compte est défini sur zéro, et une écriture contrepartie est validée le lendemain.|
|Solde BD par axe analytique|La ligne feuille répartit les coûts en fonction du solde d’un compte général par dimension. Vous serez invité à définir les filtres axe à utiliser pour calculer le solde du compte général source par dimension à partir de laquelle vous souhaitez allouer les coûts. Sinon, choisissez l’action **Définir des filtres axe** ultérieurement.|
|Solde inverse RBD par axe analytique|La ligne feuille répartit les coûts en fonction du solde inverse d’un compte général par dimension. Vous serez invité à définir les filtres axe à utiliser pour calculer le solde du compte général source par dimension à partir de laquelle vous souhaitez allouer les coûts. Sinon, choisissez l’action **Définir des filtres axe** ultérieurement.|

> [!NOTE]  
> Les champs TVA peuvent être renseignés sur la ligne feuille abonnement ou sur la ligne feuille ventilation, mais pas sur les deux. Ils peuvent être renseignés sur la page **Ventilations** uniquement si les lignes correspondantes de la feuille abonnement ne sont pas renseignées.

### Champ Périodicité abonnement

Ce champ de formule de date détermine la fréquence de validation de l’écriture sur la ligne feuille et doit être renseigné. En savoir plus sur [Utiliser des formules de date](ui-enter-date-ranges.md#use-date-formulas).

#### Exemples

Si la ligne feuille doit être validée tous les mois, saisissez "1M." Après chaque validation, la date du champ **Date comptabilisation** est mise à jour, elle est remplacée par la même date du mois suivant.

Si vous souhaitez valider une écriture le dernier jour de chaque mois, vous pouvez suivre l’un des deux exemples ci-dessous :

* Validez la première écriture le dernier jour d’un mois en saisissant la formule 1J+1M-1J (1 jour + 1 mois - 1 jour). Avec cette formule, la date de validation est calculée correctement, quel que soit le nombre de jours que comprend le mois.

* Validez la première écriture n’importe quel jour en saisissant la formule : 1M+FM. Avec cette formule, la date de validation sera située après un mois entier + le nombre de jours restants du mois en cours.

### Champ Date expiration

Ce champ détermine la date à laquelle la ligne est validée pour la dernière fois. La ligne n’est plus validée après cette date.

L’avantage d’utiliser le champ Date d’expiration est que la ligne n’est pas supprimée immédiatement de la feuille. Vous pouvez entrer une date ultérieure afin de pouvoir utiliser la ligne à l’avenir.

Si le champ est blanc, la ligne est validée à chaque validation, jusqu’à ce qu’elle soit supprimée de la feuille.

### Ventilation des montants feuille abonnement sur plusieurs comptes

Sur la page **Feuille abonnement**, vous pouvez choisir l’action **Ventilations** pour spécifier la manière dont les montants de la ligne feuille abonnement sont affectés à plusieurs comptes et axes analytiques. Une ventilation fonctionne comme une ligne compte contrepartie pour la ligne feuille abonnement.

À l’instar d’une feuille abonnement, vous entrez une ventilation une fois et elle reste dans la feuille ventilation après validation. Vous n’avez pas besoin d’entrer des montants et des ventilations chaque fois que vous validez la ligne feuille abonnement.

Si le mode récurrent est paramétré sur **Solde** ou sur **Solde inverse**, tous les codes axe analytique de la feuille récurrente sont ignorés lorsque le compte est défini sur zéro. Si vous ventilez une ligne abonnement vers diverses sections analytiques sur la page **Ventilations**, une seule écriture opposée est créée.

> [!NOTE]
> Si vous ventilez une ligne feuille abonnement qui comporte un code section, vous ne devez pas saisir le même code sur la page **Ventilations**. Si vous le faites, les sections analytiques sont incorrectes.  

Pour allouer des montants de feuille abonnement en fonction des axes analytiques, définissez le champ **Mode abonnement** sur **Solde par axe analytique** ou **Solde inverse par axe analytique**. Si le mode abonnement est paramétré sur **Solde par axe analytique** ou sur **Solde inverse par axe analytique**, tous les codes axe analytique de la feuille abonnement sont pris en compte lorsque le compte est défini sur zéro. Si vous allouez une ligne abonnement à différentes sections analytiques sur la page **Ventilations**, alors un certain nombre d’écritures contrepassées correspondant au nombre de combinaisons de section analytique dont le solde est composé sont créés. Si vous allouez le solde du compte via la feuille abonnement qui contient un code section, n’oubliez pas d’utiliser **Solde par axe analytique** ou **Solde inverse par axe analytique** pour vous assurer que les sections analytiques sont correctement équilibrées ou inversées à partir du compte source.  

Par exemple, votre société a quelques centres de profit et une poignée de départements que vos contrôleurs ont configurés en tant qu’axes analytiques. Pour accélérer le processus de saisie des factures achat, vous décidez de demander aux personnes chargées des comptes fournisseurs de saisir uniquement les axes analytiques des centres de profit. Étant donné que chaque centre de profit dispose de clés de ventilation spécifiques pour l’axe analytique Département, par exemple en fonction du nombre d’employés, vous pouvez utiliser les modes abonnement **Solde BD par axe analytique** ou **Solde inverse RBD par axe analytique** pour réaffecter les dépenses de chaque centre de profit aux départements qui conviennent en fonction des clés de ventilation.  

> [!NOTE]
> Les dimensions que vous définissez sur les lignes ventilation ne sont pas calculées automatiquement et vous devez spécifier les sections analytiques à définir sur les comptes de ventilation. Si vous souhaitez conserver le lien entre l’axe analytique du compte source et l’axe analytique du compte de ventilation, nous vous recommandons d’utiliser la fonctionnalité [Comptabilité analytique](finance-about-cost-accounting.md) à la place.

#### Exemple : Ventilation des paiements du loyer entre plusieurs départements

Vous payez un loyer tous les mois, vous avez saisi le montant du loyer sur le compte règlement d’une ligne feuille abonnement. Sur la page **Ventilations**, vous pouvez utiliser l’axe analytique Département pour répartir les dépenses entre plusieurs départements. Par exemple, selon le nombre de pieds carrés qu’occupe chaque département. Le calcul est basé sur le pourcentage de ventilation de chaque ligne. Vous pouvez ventiler de diverses manières :

* Saisissez différents comptes sur différentes lignes de ventilation pour répartir les dépenses de location entre plusieurs comptes.
* Entrez le même compte, mais utilisez des codes de valeur d’axe analytique différents pour l’axe analytique Département sur chaque ligne.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### Calcul de date de contrepassation

Lorsque vous utilisez des feuilles comptabilité périodiques pour comptabiliser les régularisations à la fin d’une période, il est important d’avoir un contrôle total sur les écritures de contrepassation. Sur la page **Feuilles comptabilité périodiques**, le champ **Calcul de date de contrepassation** vous permet de contrôler la date à laquelle les écritures de contrepassation seront validées lorsque les méthodes de contrepassation périodiques seront utilisées.

#### Exemple :

Les régularisations sont généralement validées avec des méthodes périodiques **Fixe**, **Variable** ou **Solde** sur la ligne feuille. La date comptabilisation du montant comptabilisé sur le compte sur la ligne feuille est calculée en utilisant la fréquence périodique. La date comptabilisation de l’écriture contrepartie est calculée à l’aide du champ **Calcul de la date de contrepassation**, comme suit :

* Si le champ est vide, l’écriture contrepartie sera validée le jour suivant.
* Si le champ contient une formule de date (par exemple, **5D** pendant cinq jours), l’écriture contrepartie sera validée avec une date comptabilisation calculée à l’aide du calcul de la date de contrepassation.

> [!NOTE]
> Par défaut, le champ **Calcul de la date de contrepassation** n’est pas disponible sur la page **Feuilles comptabilité périodiques**. Pour utiliser le champ, vous devez l’ajouter en personnalisant la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## Utiliser des feuilles standard

Lorsque vous créez des lignes feuille dont vous savez que vous risquez de les recréer ultérieurement, vous pouvez les enregistrer en tant que feuille standard avant de valider la feuille. La même chose s’applique aux feuilles article et aux feuilles comptabilité.

> [!NOTE]
> Les feuilles standard peuvent ne pas contenir tous les champs que vous souhaitez inclure dans les écritures comptables résultantes. Par exemple, si vous utilisez une feuille comptabilité standard pour enregistrer un paiement, les écritures comptables ne contiendront pas le champ Code mode de paiement.

> [!NOTE]  
> Les procédures suivantes traitent de la feuille article, mais concernent également la feuille comptabilité.

### Pour enregistrer une feuille standard

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles article**, puis choisissez le lien associé.
2. Entrez le code sur une ou plusieurs lignes feuille.
3. Sélectionnez les lignes feuille à réutiliser.
4. Choisissez l’action **Enregistrer en tant que feuille standard**.
5. Sur la page de demande **Enregistrer en tant que feuille standard**, définissez une feuille article standard, nouvelle ou existante, dans laquelle enregistrer les lignes.

    Si vous avez déjà créé une ou plusieurs feuilles article standard et souhaitez en remplacer une avec la nouvelle série de lignes feuille article, dans le champ **Code**, sélectionnez la feuille article.
6. Cliquez sur le bouton **OK** pour vérifier que vous souhaitez remplacer le contenu de la feuille article standard existante.
7. Pour enregistrer les valeurs dans le champ **Montant unitaire** de la feuille article standard, sélectionnez **Enregistrer le montant unitaire**.
8. Pour enregistrer les valeurs dans le champ **Quantité**, choisissez le champ **Enregistrer la quantité**.
9. Sélectionnez **OK** pour enregistrer la feuille article standard.

Lorsque vous enregistrez la feuille article standard, la page Feuille article s’affiche afin que vous puissiez la valider.

### Pour réutiliser une feuille standard

> [!NOTE]
> Les feuilles standards n’ont pas toujours les mêmes champs que les feuilles comptabilité. Lorsque vous utilisez l’action Extraire les feuilles standards pour copier les champs dans la feuille comptabilité, la feuille comptabilité peut contenir moins d’informations que si vous l’aviez créée manuellement. 

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles article**, puis choisissez le lien associé.
2. Choisissez l’action **Obtenir les feuilles standard**.
3. Pour passer en revue une feuille article standard avant de la sélectionner pour la réutiliser, choisissez l’action **Afficher la feuille**.

    Toute modification apportée à une feuille article standard est immédiatement appliquée et reste en vigueur lorsque vous rouvrez ou réutilisez cette feuille. Il est donc recommandé de s’assurer que la modification en question est suffisamment importante pour devoir s’appliquer de manière générale. Sinon, effectuez la correction ponctuelle dans la feuille article après avoir inséré les lignes feuille article standard. Reportez-vous à l’étape 4.
4. Sur la page **Feuilles article standard**, sélectionnez la feuille article standard à réutiliser et cliquez sur le bouton **OK**.

    La feuille article contient les lignes que vous avez enregistrées. Si la feuille article comporte déjà des lignes, les nouvelles lignes apparaissent après celles-ci.

    Si vous n’avez pas activé le bouton à bascule **Enregistrer le montant unitaire** lorsque vous avez enregistré la feuille, le champ **Montant unitaire** sur les lignes ajoutées à partir de la feuille standard contient la valeur du champ **Coût unitaire** sur la fiche article.

    > [!NOTE]  
    > Si vous avez activé les boutons à bascule **Enregistrer le montant unitaire** ou **Enregistrer la quantité** lorsque vous avez enregistré la feuille, assurez-vous que les valeurs insérées sont adaptées à cet ajustement de stock précis avant de valider la feuille article.
    >
    > Si les lignes feuille article insérées contiennent des montants unitaires enregistrés que vous ne souhaitez pas valider, vous pouvez les ajuster à la valeur actuelle de l’article.

5. Sélectionnez les feuilles articles standard que vous souhaitez ajuster, puis sélectionnez l’action **Recalculer le montant unitaire**. Cette action met à jour avec le champ Montant unitaire avec le coût unitaire actuel de l’article.
6. Sélectionnez l’action **Valider**.

## Pour renuméroter des numéros de document dans les feuilles

Pour éviter de valider les erreurs associées au numéro de document, vous pouvez utiliser l’action **Renuméroter les numéros de document** avant de valider une feuille.

Dans toutes les feuilles basées sur la feuille comptabilité, le champ **N° document** est modifiable de sorte que vous puissiez spécifier des numéros de document différents pour des lignes feuille différentes, ou le même numéro de document pour les lignes feuille associées.

Si le champ **Souches de n°** du nom feuille est rempli, la fonction de validation dans les feuilles comptabilité nécessite que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Choisissez simplement l’action **Renuméroter les numéros de document** et les champs **N° de document** pertinents sont alors mis à jour. Si les lignes feuille associées ont été regroupées par numéro de document avant d’utiliser la fonction, elles resteront groupées, mais peuvent être affectées à un autre numéro de document.  

Cette fonction fonctionne également sur les vues filtrées.

Toute renumérotation des numéros de document respectera les lettrages associés, par exemple un lettrage de paiement qui a été effectué à partir du document de la ligne feuille pour un compte fournisseur. Par conséquent, les champs **ID lettrage** et les champs **N° doc. lettrage** sur les écritures comptables peuvent être mises à jour.

### Pour renuméroter des documents dans les feuilles

La procédure suivante est basée sur la page **Feuille comptabilité**, mais s’applique à toutes les autres feuilles qui sont basées sur la feuille comptabilité, tel que la page **Feuille paiement**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilité**, puis choisissez le lien associé.
2. Lorsque vous êtes prêt à valider la feuille, choisissez l’action **Renuméroter les numéros de document**.

Les valeurs dans le champ **N° document** sont modifiées, le cas échéant, pour que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Une fois que les documents sont renumérotés, vous pouvez procéder à la validation de la feuille.

## Voir la [formation Microsoft](/training/paths/use-journals-dynamics-365-business-central/) associée

## Voir aussi

[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Inverser des validations feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md)  
[Répartition des coûts et du revenu](year-allocate-costs-income.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Réévaluer le stock dans la Feuille réévaluation](inventory-how-revalue-inventory.md)  
[Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md)  
[Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client](receivables-how-apply-sales-transactions-manually.md)  
[Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md)  
[Utiliser les documents et les feuilles intersociétés](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
