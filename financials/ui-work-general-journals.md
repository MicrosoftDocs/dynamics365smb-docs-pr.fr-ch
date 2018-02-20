---
title: "Utilisation de feuilles comptabilité pour valider directement dans la comptabilité| Microsoft Docs"
description: "Découvrez comment utiliser des feuilles comptabilité pour valider des transactions financières dans les comptes généraux et dans d'autres comptes, tels que les comptes bancaires et fournisseur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2aac957fc253f6c7d2f621ea2e5e039733081a19
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-general-journals"></a>Utilisation de feuilles comptabilité
La plupart des transactions financières sont validées en comptabilité via les documents commerciaux dédiés, tels que des factures achat et des commandes vente. Pour les activités économiques qui ne sont pas représentés par un document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], comme de plus petits frais ou règlements, vous pouvez créer les transactions associées en validant des lignes de feuille dans la fenêtre **Feuille comptabilité**. Pour plus d'informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).

Par exemple, vous pouvez valider les dépenses d'argent propre de vos salariés pour des activités liées à l'entreprise, afin de les rembourser ultérieurement. Pour plus d'informations, voir [Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).

Les feuilles comptabilité vous permettent de valider des transactions financières directement dans les comptes généraux et dans d'autres comptes tels que les comptes bancaires, client, fournisseur et salarié. La validation avec une feuille comptabilité crée toujours des écritures dans les comptes généraux. C'est le cas même lorsque, par exemple, vous validez une ligne feuille dans un compte client, parce qu'une écriture est validée dans un compte client de la comptabilité via un groupe comptabilisation.

Les informations que vous saisissez dans une feuille sont temporaires et peuvent être modifiées tant qu'elles sont dans la feuille. Lorsque vous validez la feuille, les informations sont transférées vers des écritures de comptes individuels, où elles ne peuvent pas être modifiées. Toutefois, vous pouvez délettrer des écritures validées et valider des écritures de contrepassation ou de correction. Pour plus d'informations, reportez-vous à [Inversion d'une validation](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Utilisation de modèles feuille et feuilles
Il existe plusieurs modèles feuille. Chaque modèle feuille est représenté par une fenêtre dédiée avec des fonctions particulières et les champs nécessaires pour la prise en charge de ces fonctions, notamment la fenêtre **Feuille rapprochement bancaire** qui permet de traiter les paiements bancaires et la fenêtre **Feuille paiement** qui permet de payer vos fournisseurs ou rembourser vos employés. Pour plus d'informations, voir [Exécuter des paiements](payables-make-payments.md) et [Rapprocher des paiements client manuellement](receivables-how-apply-sales-transactions-manually.md).

Pour chaque modèle feuille, vous pouvez configurer votre propre feuille personnelle sous forme de nom de feuille. Par exemple, vous pouvez définir votre propre nom de feuille pour la feuille paiement dotée de votre présentation et de vos paramètres personnels. Le conseil suivant est un exemple de la manière de personnaliser une feuille.

> [!TIP]  
> Si vous cochez la case **Suggérer le montant contrepartie** de la ligne pour votre nom feuille dans la fenêtre **Noms feuilles comptabilité**, le champ **Montant** dans, par exemple, les lignes feuille comptabilité pour le même numéro de document est automatiquement prérempli avec la valeur nécessaire à la contrepartie dans le document. Pour plus d'informations, voir [Laisser [!INCLUDE[d365fin](includes/d365fin_md.md)] suggérer des valeurs](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Compte principaux et comptes contrepartie
Si vous avez configuré des comptes contrepartie par défaut pour les feuilles sur la page **Feuilles comptabilité**, le compte contrepartie sera renseigné automatiquement lorsque vous renseignez le champ **Numéro du compte**. Sinon, renseignez manuellement les champs **Numéro du compte** et **N° compte contrepartie**. Un montant positif dans le champ **Montant** est débité du compte principal et crédité dans le compte contrepartie. Un montant négatif est crédité sur le compte principal et débité du compte contrepartie.

> [!NOTE]  
>   La TVA est calculée séparément pour le compte principal et le compte contrepartie, afin qu'ils puissent utiliser des taux de pourcentage de TVA différents.

## <a name="working-with-recurring-journals"></a>Utilisation de feuilles abonnement
Une feuille récurrente est une feuille comptabilité contenant des champs spécifiques pour la gestion des transactions que vous validez fréquemment avec peu ou pas de modifications. Utilisez ces champs dans le cadre des transactions récurrentes pour valider les montants fixes et variables. Vous pouvez également définir des inversions automatiques d'écritures pour le lendemain de la date de validation et utiliser les clés de répartition avec les écritures récurrentes.

## <a name="working-with-standard-journals"></a>Utilisation de feuilles standard
Lorsque vous créez des lignes feuille dont vous savez que vous risquez de les recréer ultérieurement, vous pouvez les enregistrer en tant que feuille standard avant de valider la feuille. Cette fonctionnalité s'applique aux feuilles article et aux feuilles comptabilité.

> [!NOTE]  
>   la procédure suivante traite de la feuille article mais concerne également la feuille comptabilité.

### <a name="to-save-a-standard-journal"></a>Pour enregistrer une feuille standard
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles article**, puis sélectionnez le lien connexe.
2. Entrez le code sur une ou plusieurs lignes feuille.
3. Sélectionnez les lignes feuille à réutiliser.
4. Choisissez l'action **Enregistrer en tant que feuille standard**.
5. Dans le formulaire de sélection **Enregistrer en tant que feuille standard**, définissez une feuille article standard, nouvelle ou existante, dans laquelle enregistrer les lignes.

    Si vous avez déjà créé une ou plusieurs feuilles article standard et souhaitez en remplacer une avec la nouvelle série de lignes feuille article, dans le champ Code, sélectionnez le code souhaité.
6. Choisissez le bouton **OK** pour vérifier que vous souhaitez écraser la feuille article standard existante et remplacer tout son contenu.
7. Sélectionnez le champ **Enregistrer le montant unitaire** si vous souhaitez enregistrer les valeurs dans le champ **Montant unitaire** de la feuille article standard.
8. Sélectionnez le champ **Enregistrer la quantité** si vous souhaitez que le programme enregistre les valeurs dans le champ **Quantité**.
9. Cliquez sur le bouton **OK** pour enregistrer la feuille article standard.

Une fois l'enregistrement de la feuille article standard effectué, la fenêtre Feuille article s'affiche. Vous pouvez alors procéder à la validation tout en sachant que vous pouvez très facilement recréer cette feuille si vous devez valider des lignes identiques ou analogues.

### <a name="to-reuse-a-standard-journal"></a>Pour réutiliser une feuille standard
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles article**, puis sélectionnez le lien connexe.
2. Choisissez l'action **Obtenir les feuilles standard**.

    La fenêtre Feuilles article standard qui s'ouvre alors contient des codes et des descriptions de toutes les feuilles article standard existantes.
3. Pour passer en revue une feuille article standard avant de la sélectionner pour la réutiliser, choisissez l'action **Afficher la feuille**.

    Toutes les modifications que vous apportez dans une feuille article standard sont effectuées immédiatement. Elles seront là la prochaine fois que vous rouvrirez ou réutiliserez la feuille article en question. Il est donc recommandé de s'assurer que la modification en question est suffisamment importante pour devoir s'appliquer de manière générale. Sinon, effectuez la correction ponctuelle dans la feuille article après avoir inséré les lignes feuille article standard. Reportez-vous à l'étape 4 ci-dessous.
4. Dans la fenêtre **Feuilles article standard**, sélectionnez la feuille article standard à réutiliser et cliquez sur le bouton **OK**.

    La feuille article est alors remplie avec les lignes enregistrées en tant que feuille article standard. Si des lignes feuille figurent déjà dans la feuille article, les lignes insérées sont placées en dessous.

    Si vous n'avez pas coché le champ **Enregistrer le montant unitaire** au cours de la tâche de fonction **Enregistrer en tant que feuille article standard**, alors le champ **Montant unitaire** des lignes insérées adopte automatiquement la valeur actuelle de l'article, copiée du champ **Coût unitaire** de la fiche article.

    > [!NOTE]  
>   Si vous avez sélectionné les champs **Enregistrer le montant unitaire** ou **Enregistrer la quantité**, assurez-vous que les valeurs insérées sont adaptées à cet ajustement de stock précis avant de valider la feuille article.

    Si les lignes feuille article insérées contiennent des montants unitaires enregistrés que vous ne souhaitez pas valider, vous pouvez rapidement les ajuster à la valeur actuelle de l'article comme suit.

6. Sélectionnez les feuilles articles standard que vous souhaitez ajuster, puis sélectionnez l'action **Recalculer le montant unitaire**. Le champ Montant unitaire est mis à jour avec le coût unitaire actuel de l'article.
7. Sélectionnez l'action **valider**.

## <a name="to-renumber-document-numbers-in-journals"></a>Pour renuméroter des numéros de document dans les feuilles
Pour vous assurer de ne pas recevoir d'erreurs de validation en raison de l'ordre des numéros de document, vous pouvez utiliser la fonction **Renuméroter les numéros de document** avant de valider une feuille.

Dans toutes les feuilles basées sur la feuille comptabilité, le champ **N° document** est modifiable de sorte que vous puissiez spécifier des numéros de document différents pour des lignes feuille différentes, ou le même numéro de document pour les lignes feuille associées.

Si le champ **Souches de n°** du nom feuille est rempli, la fonction de validation dans les feuilles comptabilité nécessite que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Pour vous assurer de ne pas recevoir d'erreurs de validation en raison de l'ordre des numéros de document, vous pouvez utiliser la fonction **Renuméroter les numéros de document** avant de valider la feuille. Si les lignes feuille associées ont été regroupées par numéro de document avant d'utiliser la fonction, elles resteront groupées, mais peuvent être affectées à un autre numéro de document.

Cette fonction fonctionne également sur les vues filtrées.

Toute renumérotation des numéros de document respectera les lettrages associés, par exemple un lettrage de paiement qui a été effectué à partir du document de la ligne feuille pour un compte fournisseur. Par conséquent, les champs **ID lettrage** et les champs **N° doc. lettrage** sur les écritures comptables affectées peuvent être mis à jour.

La procédure suivante est basée sur la fenêtre **Feuille comptabilité**, mais s'applique à toutes les autres feuilles qui sont basées sur la feuille comptabilité, tel que la fenêtre **Feuille paiement**.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles comptabilité**, puis sélectionnez le lien connexe.
2. Lorsque vous êtes prêt à valider la feuille, choisissez l'action **Renuméroter les numéros de document**.

Les valeurs dans le champ **N° document** sont modifiées, le cas échéant, pour que le numéro de document sur les lignes feuille individuelles ou groupées soit dans un ordre séquentiel. Une fois que les documents sont renumérotés, vous pouvez procéder à la validation de la feuille.

## <a name="see-also"></a>Voir aussi
[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Inversion d'une validation](finance-how-reverse-journal-posting.md)  
[Répartition des coûts et du revenu](year-allocate-costs-income.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

