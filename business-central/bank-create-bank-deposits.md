---
title: Créer des dépôts bancaires
description: Vous pouvez effectuer des dépôts pour conserver un enregistrement de transaction contenant des informations pouvant être appliquées aux factures en attente et aux avoirs.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="create-bank-deposits" />Créer des dépôts bancaires
> [!NOTE]
> La possibilité de créer des dépôts bancaires est nouvelle dans la 1re vague de lancement 2022 de Business Central pour de nombreuses versions nationales. Si vous utilisiez Business Central aux États-Unis, au Canada ou au Mexique avant cette version, vous utilisiez peut-être les fonctionnalités antérieures. Vous pouvez continuer, mais les nouvelles fonctionnalités remplaceront les anciennes dans une prochaine version. Pour commencer à utiliser les nouvelles fonctionnalités décrites dans cet article, votre administrateur peut accéder à la page **Gestion des fonctionnalités** et activer **Mise à jour des fonctionnalités : rapprochements et dépôts bancaires standardisés**.  

Utilisez la page **Dépôts bancaires** pour enregistrer les dépôts sous la forme d’un document unique qui valide une ou plusieurs écritures sur un compte bancaire. Généralement, les dépôts bancaires sont utilisés pour enregistrer les dépôts en espèces. La page Dépôts bancaires est disponible dans le menu **Banques** du tableau de bord Business Manager et d’autres tableaux de bord traitant de la gestion de la trésorerie.

Les montants sur les dépôts bancaires peuvent provenir de plusieurs sources :

* Ventes, en utilisant un compte général pour les revenus.
* Paiements client.
* Remboursements en espèces des fournisseurs ou paiements en espèces aux fournisseurs. 

Les lignes de dépôt bancaire contiennent des informations sur les dépôts individuels, tels que les chèques des clients. Le total des montants inscrits sur les lignes doit correspondre au montant total du dépôt.

Après avoir rempli les informations et les lignes relatives au dépôt, vous devez les valider. La validation mettra à jour les livres comptables appropriés. Ces livres comptables comprennent la comptabilité ainsi que la comptabilité bancaire, la comptabilité client et la comptabilité fournisseur. Les dépôts affichés sont stockés sur la page **Dépôts bancaires validés**, afin que vous puissiez vous y référer par la suite.

L’état **Dépôt bancaire** affiche les dépôts des clients et des fournisseurs avec le montant du dépôt initial, le montant du dépôt qui reste ouvert et le montant appliqué. L’état indique également le montant total du dépôt validé à rapprocher.

## <a name="before-you-start" />Avant de commencer
Avant de pouvoir utiliser les dépôts bancaires, plusieurs éléments doivent être définis. Vous devez disposer d’une souche de numéros et d’un modèle de feuille comptabilité. Vous devez également spécifier si vous souhaitez valider les montants des dépôts bancaires sous forme de somme forfaitaire. C’est-à-dire comme un total de tous les montants sur les lignes de dépôt. Sinon, chaque ligne est validée comme une entrée individuelle. La validation d’un dépôt sous la forme d’une seule écriture comptable bancaire peut faciliter le rapprochement bancaire.

### <a name="number-series-and-lump-sum-deposits" />Souches de numéros et dépôts forfaitaires
Vous devez paramétrer une souche de numéros pour les dépôts bancaires, puis spécifier la souche dans le champ **Numéros de dépôt bancaire** sur la page **Paramètres ventes**. Pour plus d’informations, voir [Créer des souches de numéros](ui-create-number-series.md). 

Sur la page **Paramètres ventes** également, si vous souhaitez valider des dépôts sous forme de montants forfaitaires plutôt que sous forme de lignes individuelles, activez le bouton bascule **Valider les montants des dépôts bancaires sous forme de somme forfaitaire**. La validation d’un dépôt sous forme de somme forfaitaire, qui crée une écriture bancaire pour le montant total du dépôt, peut faciliter le rapprochement bancaire.

### <a name="general-journal-templates-for-bank-deposits" />Modèles feuille comptabilité pour les dépôts bancaires
Vous devez également créer un modèle feuille comptabilité pour les dépôts. Vous utilisez les feuilles comptabilité pour valider des entrées dans les comptes banque, client, fournisseur, immobilisation et généraux. Les modèles feuille comptabilité conçoivent la feuille comptabilité en fonction de l’objectif de votre travail. Autrement dit, les champs du modèle de feuille sont exactement ceux dont vous avez besoin. 

Les dépôts seront des encaissements. Vous pouvez donc réutiliser votre souche de numéros pour les feuilles règlement. Sinon, si vous devez faire la distinction entre les écritures feuille des dépôts bancaires et des encaissements, utilisez une souche de numéros différente.

Vous devrez également créer un traitement par lots pour le modèle. Pour créer un traitement par lots, sur la page **Modèles feuille comptabilité**, choisissez l’action **Lots**. Pour plus d’informations, voir [Utilisation de modèles feuille et de lots](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines" />Dimensions sur les lignes de dépôt bancaire
Les lignes du dépôt bancaire utiliseront automatiquement les dimensions par défaut que vous avez spécifiées dans les champs **Code emplacement immo** et **Code groupe clients**. Lorsque vous choisissez **Client** ou **Fournisseur** dans le champ **Type de compte**, les dimensions spécifiées pour le client ou le fournisseur remplaceront les valeurs par défaut. Au besoin, vous pouvez modifier les axes analytiques sur les lignes.

> [!TIP]
> Les axes analytiques sur les lignes sont définis en fonction des affectations analytiques prioritaires. Les axes analytiques ligne sont prioritaires par rapport aux axes analytiques en-tête. Pour éviter les conflits, vous pouvez créer des règles qui déterminent quand utiliser un axe analytique en fonction de la source. Si vous souhaitez modifier la priorité des axes analytiques, vous pouvez modifier leur classement dans l’onglet **Affect. analytique prioritaire**. Pour plus d’informations, voir [Pour configurer des affectations analytiques prioritaires](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit" />Créer un dépôt bancaire
1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dépôts bancaires**, puis sélectionnez le lien associé.
2. Choisissez **Nouveau** pour ouvrir la page **Dépôt bancaire**. 
3. Choisissez le modèle feuille comptabilité que vous avez créé pour les dépôts bancaires.  

    > [!NOTE]
    > Si le modèle feuille comptabilité comporte plusieurs lots, vous serez invité à en choisir un.

4. Dans le champ **N° compte bancaire**, choisissez le compte bancaire sur lequel effectuer le dépôt.

    > [!TIP]
    > Vous pouvez vérifier que vous déposez sur le compte correct en utilisant les actions **Fiche compte** et **Écritures comptables compte** pour rechercher les écritures comptables pour le compte bancaire sélectionné. Par exemple, pour voir si des dépôts similaires ont été effectués sur le compte.

5. Dans le champ **Montant total du dépôt**, entrez le montant total du dépôt. Ce total doit être la somme des montants de toutes les lignes.
6. Renseignez les champs restants selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    La date du champ **Date de validation** et les axes analytiques des champs **Code département** et **Code groupe clients** seront affectés aux lignes que vous créez pour le dépôt bancaire. Si nécessaire, vous pouvez les modifier. 

7. Selon que vous souhaitez valider le dépôt bancaire sous forme de somme forfaitaire ou chaque ligne individuellement dans la comptabilité, activez ou désactivez le bouton **Valider sous forme de somme forfaitaire**. Le paramètre par défaut provient du même bouton bascule sur la page **Paramètres ventes**.

    > [!NOTE]
    > Le champ **Code devise** indique la devise spécifiée pour le compte bancaire que vous avez choisi. Vous ne pouvez pas choisir une devise différente.

8. Sur le raccourci **Lignes**, créez une nouvelle ligne pour chaque paiement en espèces que vous souhaitez déposer.
9. Dans le champ **Type de compte**, précisez d’où provient le paiement. Pour les dépôts bancaires, le type est généralement **Client** ou **Fournisseur**. 

    > [!NOTE]
    > Vous pouvez également enregistrer un paiement en espèces pour un fournisseur. Pour ce faire, choisissez **Fournisseur**, puis entrez le montant du paiement sous la forme d’un nombre négatif dans le champ **Montant du crédit** sur la ligne. 

10. Dans le champ **N° document**, saisissez le numéro de document de la facture d’où provient le montant crédit. Vous pouvez utiliser un numéro de document pour chaque ligne ou le même numéro pour toutes les lignes.

    > [!TIP]
    > En règle générale, vous n’avez pas besoin de remplir le champ **Type de document** pour les écritures financières. Par exemple, si vous déposez de l’argent provenant de la vente d’une journée, vous laissez le champ vide. Si vous déposez de l’argent provenant d’un paiement client, vous choisissez **Paiement**.

11. Si vous déposez un paiement en espèces pour une facture client spécifique, choisissez l’action **Lettrer écritures**, puis saisissez le numéro de facture dans le champ **ID lettrage**. 
12. Si vous êtes prêt à valider le virement bancaire, choisissez l’action **Valider**.

    > [!TIP]
    > Avant de valider le dépôt, vous pouvez utiliser l’action **Impression test** pour vérifier vos données. L’état indiquera s’il existe des problèmes, tels que des données manquantes, qui empêcheront la validation.  

## <a name="finding-posted-bank-deposits" />Recherche de dépôts bancaires validés
La page **Dépôts bancaires validés** répertorie les dépôts antérieurs de votre société. Dans la liste, vous pouvez vérifier les commentaires et les axes analytiques qui ont été spécifiés pour les dépôts. Vous pouvez ouvrir le dépôt bancaire pour afficher plus de détails, et à partir de là, vous pouvez approfondir vos recherches. Par exemple, vous pouvez choisir l’action Rechercher des écritures pour afficher les écritures bancaires validées. À partir de l’écriture comptable compte bancaire, vous pouvez trouver l’écriture comptable correspondante validée.

Si vous voulez consulter toutes les écritures comptables pour les lignes de dépôt validées, accédez à la page **Hist. trans. comptabilité** et utilisez l’action **Comptabilité**. Vous y trouverez toutes les écritures comptables, y compris les écritures pour les clients et les fournisseurs.

## <a name="reversing-a-posted-bank-deposit" />Annulation d’un dépôt bancaire validé
Pour annuler un dépôt validé, accédez à la page **Hist. trans. comptabilité**, identifiez l’historique du dépôt, puis choisissez l’action **Contrepasser l’historique des transactions**.

> [!NOTE]
> Vous ne pouvez uniquement contrepasser un historique des transactions contenant un seul type d’entrée. Autrement dit, l’historique ne doit contenir que des écritures client ou des écritures fournisseur, mais ne peut pas contenir les deux. Si un historique contient les deux, vous devez contrepasser manuellement le dépôt.      

## <a name="see-also" />Voir aussi
[Finances](finance.md)  
[Configuration de Finance](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



