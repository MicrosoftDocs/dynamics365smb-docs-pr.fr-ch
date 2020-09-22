---
title: Rapprocher des comptes bancaires | Microsoft Docs
description: Décrit la manière dont la valeur du stock fait l'objet d'un rapprochement avec la comptabilité.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/19/2020
ms.author: edupont
ms.openlocfilehash: d97c1d937d2a9c90d086528d0f2fe70ea5a29502
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782208"
---
# <a name="reconcile-bank-accounts"></a>Rapprochement des comptes bancaires

Un rapprochement bancaire permet de vous assurer que vos diverses dépenses et transactions commerciales sont correctement reflétées dans les livres de la société. Pour ce faire, vous comparez et faites correspondre les écritures de vos comptes bancaires internes avec les transactions bancaires de votre banque, puis vous validez les soldes sur vos comptes bancaires internes pour mettre les totaux à la disposition des responsables financiers. Le rapprochement bancaire est également un moyen pratique de découvrir et de résoudre les paiements manquants et les erreurs de comptabilité.

Les paragraphes qui suivent décrivent comment effectuer un rapprochement bancaire avec la page **Rapprochement bancaire**.

> [!TIP]
> Vous pouvez également rapprocher des comptes bancaires sur la page **Feuille rapprochement bancaire** en relation avec le traitement des paiements. Toutes les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées lorsque vous sélectionnez l'action **Valider les paiements et rapprocher les comptes bancaires**. Cela signifie que le compte bancaire est automatiquement rapproché pour les paiements que vous validez avec le journal. Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Dans les versions nord-américaines, vous pouvez également effectuer cette tâche sur la page **Feuille rapprochement bancaire**, qui est mieux adaptée pour les chèques et les acomptes, mais ne prend pas en charge l'importation de fichiers de relevé bancaire. Pour utiliser cette page à la place de la page **Rapprochement bancaire**, désélectionnez le champ **Rapprochement bancaire avec correspondance auto.** sur la page **Paramètres comptabilité**. Pour plus d'informations, voir [Rapprocher des comptes bancaires](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sous Fonctionnalité locale, États-Unis.

Les lignes de la page **Rapprochement bancaire** sont réparties sur deux volets. Le volet **Lignes relevé bancaire** indique le volet des transactions bancaires importées ou les écritures comptables comportant des arriérés de paiement. Le volet **Écritures comptables compte bancaire** affiche les écritures comptables dans le compte bancaire interne.

L'activité de rapprochement des transactions bancaires avec les écritures bancaires internes est appelée *correspondance*. Vous pouvez choisir d'effectuer la correspondance automatiquement à l'aide de la fonction **Faire correspondre automatiquement**. Sinon, vous pouvez sélectionner manuellement des lignes dans les deux volets pour lier chaque ligne relevé bancaire à une ou plusieurs écritures comptables compte bancaire correspondantes, puis utiliser la fonction **Faire correspondre manuellement**. La case **Lettré** est cochée sur les lignes pour lesquelles les écritures correspondent. Pour plus d'informations, voir [Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Si les lignes relevé bancaire se rapportent à des écritures comptables chèque, vous ne pouvez pas utiliser les fonctions de correspondance. Au lieu de cela, vous devez sélectionner l'action **Lettrer écritures**, puis sélectionner l'écriture comptable chèque appropriée avec laquelle mettre en correspondance la ligne de relevé bancaire.

Lorsque la valeur du champ **Solde final** du volet **Lignes relevé bancaire** est égale à celle du champ **Solde à simuler** du volet **Écritures comptables compte bancaire**, vous pouvez sélectionner l'action **Valider**. Toutes les écritures comptables de compte bancaire sans correspondance resteront sur la page, indiquant l'existence de différences que vous devez résoudre pour rapprocher le compte bancaire.

Toutes les lignes qui ne peuvent pas être mises en correspondance, indiquées par une valeur dans le champ **Différence**, resteront sur la page **Rapprochement bancaire** après validation. Elles représentent une certaine forme de différence que vous devez résoudre avant de pouvoir effectuer le rapprochement des comptes bancaires. Situations commerciales typiques pouvant entraîner des différences :

|Différence|Motif|Résolution|
|-|-|
|Une transaction dans le compte bancaire interne ne figure pas sur le relevé bancaire.|La transaction bancaire n'a pas eu lieu alors qu'une validation a été effectuée dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|Effectuez la transaction d'argent qui n'a pas eu lieu (ou demandez à un débiteur de la faire), puis réimportez le fichier de relevé bancaire ou saisissez la transaction manuellement.|
|Une transaction sur le relevé bancaire n'existe pas en tant que ligne feuille ou document dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|Une transaction bancaire a été effectuée sans validation correspondante dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple la validation d'une ligne feuille pour une dépense.|Créez et validez l'écriture manquante. Pour plus d'informations sur un moyen rapide de lancer cette opération, voir [Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des transactions bancaires](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Une transaction dans le compte bancaire interne correspond à une transaction bancaire, mais certaines informations sont trop différentes pour établir une correspondance.|Des informations, telles que le montant ou le nom du client, ont été saisies différemment concernant la transaction bancaire ou la validation interne.|Vérifiez les informations, puis faites les correspondre manuellement. Corrigez éventuellement la non-concordance des informations.||

Vous devez résoudre les différences, par exemple en créant des écritures manquantes et en corrigeant les informations qui ne correspondent pas, ou en effectuant les transactions d'argent qui n'ont pas eu lieu, jusqu'à ce que le rapprochement du compte bancaire soit terminé et validé.

Vous pouvez renseigner le volet **Lignes relevé bancaire** de la page **Rapprochement bancaire** des manières suivantes :

* Automatiquement, à l'aide de la fonction **Importer le relevé bancaire** pour renseigner le volet **Lignes relevé bancaire** avec des transactions bancaires en fonction d'un flux ou d'un fichier importé fourni par la banque.
* Manuellement, en utilisant la fonction **Proposer lignes** pour renseigner le volet **Lignes relevé bancaire** en fonction des factures dans [!INCLUDE[d365fin](includes/d365fin_md.md)] qui comportent des arriérés de paiement.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pour renseigner les lignes rapprochement bancaire en important un relevé bancaire

Le volet **Lignes relevé bancaire** sera renseigné avec des transactions bancaires en fonction d'un flux ou d'un fichier importé fourni par la banque.

Pour activer l'importation des relevés bancaires en tant que flux bancaires, vous devez d'abord configurer et activer le service Envestnet Yodlee Bank Feeds, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d'informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Rapprochement bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N° compte bancaire**, sélectionnez le compte bancaire approprié. Les écritures comptables compte bancaire qui existent pour le compte bancaire s'affichent le volet **Écritures comptables compte bancaire**.
4. Dans le champ **Date relevé**, saisissez la date du relevé de banque.
5. Dans le champ **Solde final du relevé**, saisissez le solde du relevé de banque.
6. Si vous avez un fichier de relevé bancaire, sélectionnez l'action **Importer le relevé bancaire**.
7. Localisez le fichier, puis sélectionnez le bouton **Ouvrir** pour importer les transactions bancaires dans le volet **Lignes relevé bancaire** sur la page **Rapprochement bancaire**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pour renseigner les lignes rapprochement bancaire avec la fonction Proposer lignes

Le volet **Lignes relevé bancaire** sera renseigné en fonction des factures dans [!INCLUDE[d365fin](includes/d365fin_md.md)] qui comportent des arriérés de paiement.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l'action **Proposer lignes**.
2. Dans le champ **Date de début**, saisissez la date de validation la plus précoce des écritures comptables à rapprocher.
3. Dans le champ **Date de fin**, saisissez la date de validation la plus tardive des écritures comptables à rapprocher.
4. Cochez la case **Inclure les chèques** pour les écritures comptables chèque proposées au lieu des écriture comptables compte bancaire correspondantes.
5. Cliquez sur le bouton **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pour mettre en correspondance automatiquement des lignes de relevé bancaire avec des écritures comptables compte bancaire

La page **Rapprochement bancaire** propose une fonctionnalité de correspondance automatique basée sur une correspondance entre le texte d'une ligne relevé bancaire (volet gauche) et celui d'une ou de plusieurs écritures comptables compte bancaire (volet droit). Notez que vous pouvez remplacer la correspondance automatique suggérée, et que vous pouvez choisir de ne pas utiliser du tout la correspondance automatique. Pour plus d'informations, voir [Pour faire correspondre manuellement des lignes relevé bancaire avec des écritures comptables compte bancaire](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. Sur la page **Rapprochement bancaire**, sélectionnez l'action **Faire correspondre automatiquement**. La page **Faire correspondre les écritures bancaires** s'ouvre.
2. Dans le champ **Tolérance date transaction (jours)**, spécifiez le nombre de jours avant et après la date comptabilisation de l'écriture comptable compte bancaire pendant lesquels la fonction recherchera des dates transaction correspondantes dans le relevé bancaire.

    Si vous saisissez 0 ou laissez le champ vide, la fonction **Faire correspondre automatiquement** recherchera uniquement les dates de transaction correspondantes sur la date comptabilisation de l'écriture comptable compte bancaire.
3. Cliquez sur le bouton **OK**.

    Toutes les lignes de relevé bancaire et les écritures comptables compte bancaire qui peuvent être rapprochées deviennent vertes, et la case **Lettré** est cochée.
4. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pour mettre en correspondance des lignes de relevé bancaire avec les écritures comptables compte bancaire manuellement

1. Sur la page **Rapprochement bancaire**, sélectionnez une ligne non lettrée dans le volet **Lignes relevé bancaire**.
2. Dans le volet **Écritures comptables compte bancaire**, sélectionnez une ou plusieurs écritures comptables compte bancaire qui peuvent être mise en correspondance avec la ligne de relevé bancaire sélectionnée. Pour choisir plusieurs lignes, appuyez et maintenez la touche Ctrl enfoncée.
3. Sélectionnez l'action **Faire correspondre manuellement**.

    La ligne de relevé bancaire sélectionnée et les écritures comptables compte bancaire sélectionnées deviennent vertes, et la case à cocher **Lettré** du volet de droite est activée.
4. Répétez les étapes 1 à 3 pour toutes les lignes de relevé bancaire qui ne sont pas mises en correspondance.
5. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des lignes relevé bancaire

Les relevés bancaires comportent parfois des montants correspondant à la facturation d'intérêts ou de frais. Ces lignes relevé bancaire ne peuvent pas être mises en correspondance, car il n'existe aucune écriture comptable associée dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous devez ensuite valider une ligne feuille pour chaque transaction afin de créer une écriture comptable associée avec laquelle elle peut être mise en correspondance.

1. Sur la page **Rapprochement bancaire**, sélectionnez l'action **Transférer vers feuille comptabilité**.  
2. Sur la page **Trans. rappr. banc. -> f. cpta**, indiquez la feuille de comptabilité à utiliser, puis cliquez sur le bouton **OK**.

    La page **Feuille comptabilité** s'ouvre. Elle contient de nouvelles lignes feuille pour toutes les lignes de relevé bancaire dont les écritures comptables sont manquantes.
3. Renseignez la ligne feuille avec les informations appropriées, comme le compte de contrepartie. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  
4. Pour examiner le résultat de la validation avant de valider, choisissez l'action **Impression test**. L'état **Relevé bancaire** s'ouvre et affiche les mêmes champs que dans l'en-tête de la page **Rapprochement bancaire**.
5. Sélectionnez l'action **Valider**.

    Lorsque l'écriture est validée, poursuivez en faisant correspondre la ligne relevé bancaire avec celle-ci.
6. Réactualisez ou rouvrez la page **Rapprochement bancaire**. La nouvelle écriture comptable s'affiche dans le volet **Écritures comptables compte bancaire**.
7. Faites correspondre la ligne relevé bancaire à l'écriture comptable compte bancaire, manuellement ou automatiquement.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
