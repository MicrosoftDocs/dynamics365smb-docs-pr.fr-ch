---
title: Rapprocher des comptes bancaires | Microsoft Docs
description: Décrit la manière dont la valeur du stock fait l’objet d’un rapprochement avec la comptabilité.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 746fd31dfad378bd067e977f2a55a5cf329b7aaa
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013651"
---
# <a name="reconcile-bank-accounts"></a>Rapprochement des comptes bancaires

Un rapprochement bancaire permet de vous assurer que vos diverses dépenses et transactions commerciales sont correctement reflétées dans les livres de la société. Pour ce faire, vous comparez et faites correspondre les écritures de vos comptes bancaires internes avec les transactions bancaires de votre banque, puis vous validez les soldes sur vos comptes bancaires internes pour mettre les totaux à la disposition des responsables financiers. Le rapprochement bancaire est également un moyen pratique de découvrir et de résoudre les paiements manquants et les erreurs de comptabilité.

Les paragraphes qui suivent décrivent comment effectuer un rapprochement bancaire avec la page **Rapprochement bancaire**.

> [!TIP]
> Vous pouvez également rapprocher des comptes bancaires sur la page **Feuille rapprochement bancaire** lorsque vous traitez les paiements. Toutes les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées lorsque vous sélectionnez l’action **Valider les paiements et rapprocher les comptes bancaires**. Cela rapproche automatiquement le compte bancaire pour les paiements que vous validez avec le journal. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Dans les versions nord-américaines, vous pouvez également effectuer cette tâche sur la page **Feuille rapprochement bancaire**, qui est mieux adaptée pour les chèques et les acomptes, mais ne prend pas en charge l’importation de fichiers de relevé bancaire. Pour utiliser cette page à la place de la page **Rapprochement bancaire**, désélectionnez le champ **Rapprochement bancaire avec correspondance auto.** sur la page **Paramètres comptabilité**. Pour plus d’informations, voir [Rapprocher des comptes bancaires](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sous Fonctionnalité locale, États-Unis.

Les lignes de la page **Rapprochement bancaire** sont réparties sur deux volets. Le volet **Lignes relevé bancaire** indique le volet des transactions bancaires importées ou les écritures comptables comportant des arriérés de paiement. Le volet **Écritures comptables compte bancaire** affiche les écritures comptables dans le compte bancaire interne.

Le rapprochement des transactions bancaires avec les écritures bancaires internes est appelé *correspondance*. Vous pouvez choisir d’effectuer la correspondance automatiquement à l’aide de la fonction **Faire correspondre automatiquement**. Sinon, vous pouvez sélectionner manuellement des lignes dans les deux volets pour lier chaque ligne relevé bancaire à une ou plusieurs écritures comptables compte bancaire correspondantes, puis utiliser la fonction **Faire correspondre manuellement**. La case **Lettré** est cochée sur les lignes pour lesquelles les écritures correspondent. Pour plus d’informations, voir [Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Si les lignes relevé bancaire se rapportent à des écritures comptables chèque, vous ne pouvez pas utiliser les fonctions de correspondance. Au lieu de cela, vous devez sélectionner l’action **Lettrer écritures**, puis sélectionner l’écriture comptable chèque appropriée avec laquelle mettre en correspondance la ligne de relevé bancaire.

Lorsque la valeur du champ **Solde final** du volet **Lignes relevé bancaire** est égale à celle du champ **Solde à simuler** du volet **Écritures comptables compte bancaire**, vous pouvez sélectionner l’action **Valider**. Toutes les écritures comptables de compte bancaire sans correspondance resteront sur la page, indiquant l’existence de différences que vous devez résoudre pour rapprocher le compte bancaire.

Toutes les lignes qui ne peuvent pas être mises en correspondance, indiquées par une valeur dans le champ **Différence**, resteront sur la page **Rapprochement bancaire** après validation. Elles représentent une certaine forme de différence que vous devez résoudre avant de pouvoir effectuer le rapprochement des comptes bancaires. Situations commerciales typiques pouvant entraîner des différences :

|Différence|Motif|Résolution|
|-|-|
|Une transaction dans le compte bancaire interne ne figure pas sur le relevé bancaire.|La transaction bancaire n’a pas eu lieu alors qu’une validation a été effectuée dans [!INCLUDE[prod_short](includes/prod_short.md)].|Effectuez la transaction d’argent qui n’a pas eu lieu (ou demandez à un débiteur de la faire), puis réimportez le fichier de relevé bancaire ou saisissez la transaction manuellement.|
|Une transaction sur le relevé bancaire n’existe pas en tant que ligne feuille ou document dans [!INCLUDE[prod_short](includes/prod_short.md)].|Une transaction bancaire a été effectuée sans validation correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple la validation d’une ligne feuille pour une dépense.|Créez et validez l’écriture manquante. Pour plus d’informations sur un moyen rapide de lancer cette opération, voir [Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des transactions bancaires](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Une transaction dans le compte bancaire interne correspond à une transaction bancaire, mais certaines informations sont trop différentes pour établir une correspondance.|Des informations, telles que le montant ou le nom du client, ont été saisies différemment concernant la transaction bancaire ou la validation interne.|Vérifiez les informations, puis faites les correspondre manuellement. Corrigez éventuellement la non-concordance des informations.||

Vous devez résoudre les différences, par exemple en créant des écritures manquantes et en corrigeant les informations qui ne correspondent pas, ou en effectuant les transactions d’argent qui n’ont pas eu lieu, jusqu’à ce que le rapprochement du compte bancaire soit terminé et validé.

Vous pouvez renseigner le volet **Lignes relevé bancaire** de la page **Rapprochement bancaire** des manières suivantes :

* Automatiquement, à l’aide de la fonction **Importer le relevé bancaire** pour renseigner le volet **Lignes relevé bancaire** avec des transactions bancaires en fonction d’un flux ou d’un fichier importé fourni par la banque.
* Manuellement, en utilisant la fonction **Proposer lignes** pour renseigner le volet **Lignes relevé bancaire** en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pour renseigner les lignes rapprochement bancaire en important un relevé bancaire

Le volet **Lignes relevé bancaire** sera renseigné avec des transactions bancaires en fonction d’un flux ou d’un fichier importé fourni par la banque.

Pour activer l’importation des relevés bancaires en tant que flux bancaires, vous devez d’abord configurer et activer le service Envestnet Yodlee Bank Feeds, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Rapprochement bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Dans le champ **N° compte bancaire**, sélectionnez le compte bancaire approprié. Les écritures comptables compte bancaire qui existent pour le compte bancaire s’affichent le volet **Écritures comptables compte bancaire**.
4. Dans le champ **Date relevé**, saisissez la date du relevé de banque.
5. Dans le champ **Solde final du relevé**, saisissez le solde du relevé de banque.
6. Si vous avez un fichier de relevé bancaire, sélectionnez l’action **Importer le relevé bancaire**.
7. Localisez le fichier, puis sélectionnez le bouton **Ouvrir** pour importer les transactions bancaires dans le volet **Lignes relevé bancaire** sur la page **Rapprochement bancaire**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pour renseigner les lignes rapprochement bancaire avec la fonction Proposer lignes

Le volet **Lignes relevé bancaire** sera renseigné en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Proposer lignes**.
2. Dans le champ **Date de début**, saisissez la date de validation la plus précoce des écritures comptables à rapprocher.
3. Dans le champ **Date de fin**, saisissez la date de validation la plus tardive des écritures comptables à rapprocher.
4. Cochez la case **Inclure les chèques** pour les écritures comptables chèque proposées au lieu des écriture comptables compte bancaire correspondantes.
5. Cliquez sur le bouton **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pour mettre en correspondance automatiquement des lignes de relevé bancaire avec des écritures comptables compte bancaire

La page **Rapprochement bancaire** propose une fonctionnalité de correspondance automatique basée sur une correspondance entre le texte d’une ligne relevé bancaire (volet gauche) et celui d’une ou de plusieurs écritures comptables compte bancaire (volet droit). Notez que vous pouvez remplacer la correspondance automatique suggérée, et que vous pouvez choisir de ne pas utiliser du tout la correspondance automatique. Pour plus d’informations, voir [Pour faire correspondre manuellement des lignes relevé bancaire avec des écritures comptables compte bancaire](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Faire correspondre automatiquement**. La page **Faire correspondre les écritures bancaires** s’ouvre.
2. Dans le champ **Tolérance date transaction (jours)**, spécifiez le nombre de jours avant et après la date comptabilisation de l’écriture comptable compte bancaire pendant lesquels la fonction recherchera des dates transaction correspondantes dans le relevé bancaire.

    Si vous saisissez 0 ou laissez le champ vide, la fonction **Faire correspondre automatiquement** recherchera uniquement les dates de transaction correspondantes sur la date comptabilisation de l’écriture comptable compte bancaire.
3. Cliquez sur le bouton **OK**.

    Toutes les lignes de relevé bancaire et les écritures comptables compte bancaire qui peuvent être rapprochées deviennent vertes, et la case **Lettré** est cochée.
4. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l’action **Supprimer correspondance**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pour mettre en correspondance des lignes de relevé bancaire avec les écritures comptables compte bancaire manuellement

1. Sur la page **Rapprochement bancaire**, sélectionnez une ligne non lettrée dans le volet **Lignes relevé bancaire**.
2. Dans le volet **Écritures comptables compte bancaire**, sélectionnez une ou plusieurs écritures comptables compte bancaire qui peuvent être mise en correspondance avec la ligne de relevé bancaire sélectionnée. Pour choisir plusieurs lignes, appuyez et maintenez la touche Ctrl enfoncée.
3. Sélectionnez l’action **Faire correspondre manuellement**.

    La ligne de relevé bancaire sélectionnée et les écritures comptables compte bancaire sélectionnées deviennent vertes, et la case à cocher **Lettré** du volet de droite est activée.
4. Répétez les étapes 1 à 3 pour toutes les lignes de relevé bancaire qui ne sont pas mises en correspondance.
5. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l’action **Supprimer correspondance**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des lignes relevé bancaire

Les relevés bancaires comportent parfois des montants correspondant à la facturation d’intérêts ou de frais. Ces lignes relevé bancaire ne peuvent pas être mises en correspondance, car il n’existe aucune écriture comptable associée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous devez ensuite valider une ligne feuille pour chaque transaction afin de créer une écriture comptable associée avec laquelle elle peut être mise en correspondance.

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Transférer vers feuille comptabilité**.  
2. Sur la page **Trans. rappr. banc. -> f. cpta**, indiquez la feuille de comptabilité à utiliser, puis cliquez sur le bouton **OK**.

    La page **Feuille comptabilité** s’ouvre. Elle contient de nouvelles lignes feuille pour toutes les lignes de relevé bancaire dont les écritures comptables sont manquantes.
3. Renseignez la ligne feuille avec les informations appropriées, comme le compte de contrepartie. Pour plus d’informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  
4. Pour examiner le résultat de la validation avant de valider, choisissez l’action **Impression test**. L’état **Relevé bancaire** s’ouvre et affiche les mêmes champs que dans l’en-tête de la page **Rapprochement bancaire**.
5. Sélectionnez l’action **Valider**.

    Lorsque l’écriture est validée, poursuivez en faisant correspondre la ligne relevé bancaire avec celle-ci.
6. Réactualisez ou rouvrez la page **Rapprochement bancaire**. La nouvelle écriture comptable s’affiche dans le volet **Écritures comptables compte bancaire**.
7. Faites correspondre la ligne relevé bancaire à l’écriture comptable compte bancaire, manuellement ou automatiquement.

## <a name="undo-a-bank-account-reconciliation"></a>Annuler un rapprochement bancaire
Si vous découvrez une erreur dans un rapprochement bancaire validé, vous pouvez utiliser l’action **Annuler** sur la page **Rapprochement bancaire** pour corriger l’erreur. Lorsque vous annulez un rapprochement bancaire validé, les écritures sont déplacées vers la page **Rapprochement bancaire** et marquées comme **Ouvertes**, ce qui signifie qu’elles ne sont pas rapprochées. Vous pouvez ensuite corriger le rapprochement bancaire et le valider à nouveau.

> [!NOTE]
> Dans la version des États-Unis, pour utiliser la fonction Annuler pour les rapprochements bancaires et les relevés bancaires validés, vous devez activer le bouton bascule **Rapprochement bancaire avec correspondance automatique** sur la page **Paramètres comptabilité**. La fonction Annuler n’est pas disponible pour les relevés bancaires publiés à partir des feuilles de calcul de rapprochement bancaire.

### <a name="reusing-the-bank-statement-number"></a>Réutilisation du numéro de relevé bancaire
Le numéro de relevé bancaire utilisé pour le nouveau rapprochement bancaire est extrait du compte bancaire, tout comme le dernier relevé de solde. Vous pouvez modifier ces valeurs avant de commencer un nouveau rapprochement bancaire. Cependant, lorsque vous créez un nouveau rapprochement bancaire, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si le numéro de relevé est déjà attribué à un relevé bancaire validé. Si le numéro est utilisé, mais que vous souhaitez que le nouveau relevé bancaire l’utilise à la place, vous pouvez utiliser **Modifier n° relevé** sur la page **Rapprochement bancaire**.

### <a name="examples"></a>Exemples
Voici quelques exemples de la façon de corriger une erreur sur un rapprochement bancaire validé avec ou sans l’utilisation du même numéro de relevé.

#### <a name="example-1"></a>Exemple 1
Vous avez effectué des rapprochements bancaires pour janvier, février et mars. Le numéro de relevé bancaire était 100 pour mars. Plus tard, vous découvrez que mars n’a inclus que les entrées jusqu’au 30, ce qui signifie que les entrées pour le 31 sont manquantes. Vous devez donc refaire le rapprochement bancaire pour mars. Dans ce cas, nous allons ouvrir la page **Relevé bancaire**, choisissez le relevé de mars, puis choisissez **Annuler**. 

Le nouveau rapprochement bancaire porte le numéro de relevé 101. Pour réaffecter le nombre 100, choisissez **Modifier n° relevé** et entrez **100**. 

> [!TIP]
> N’oubliez pas de définir la date de fin de relevé appropriée (dans cet exemple, le 31 mars) et de modifier le champ **Solde dernier relevé**. 

#### <a name="example-2"></a>Exemple 2
Vous avez effectué des rapprochements bancaires pour janvier, février, juin et juillet. Vous découvrez que février était incorrect. Supposons qu’il ait le numéro de déclaration 100. Comme dans l’exemple 1, vous utilisez les actions Annuler et Modifier n° relevé. pour changer le numéro de relevé comme dans l’exemple n° 1 ci-dessus et vous pouvez maintenant refaire le rapprochement bancaire de février.  

Après avoir validé le rapprochement bancaire corrigé pour février, sur la carte de compte bancaire correspondante, le champ **Dernier n° relevé** affichera **100**, et le champ **Solde dernier relevé** affichera le solde de fin du relevé de février. 

Si le prochain rapprochement bancaire que vous effectuez est pour mars, [!INCLUDE[d365fin](includes/d365fin_md.md)] attribuera 101 comme numéro de relevé et lui donnera le bon **Solde dernier relevé**.

Si le prochain rapprochement bancaire que vous effectuez concerne le mois d’août, envisagez de modifier les valeurs dans **N° dernier relevé** et **Solde dernier relevé** sur la fiche **Compte bancaire** avant de créer le prochain rapprochement bancaire ou utilisez l’action Modifier n° relevé. et modifiez également la valeur dans le champ « Solde dernier relevé » sur la page de rapprochement bancaire.

> [!NOTE]
> Le numéro de relevé est important lorsque vous effectuez des rapprochements bancaires avec des fichiers CAMT importés contenant des numéros de relevé ou lorsque vous effectuez un rapprochement sur la base de relevés bancaires imprimés. Si vous téléchargez simplement une série de transactions bancaires depuis votre banque en ligne, le numéro de relevé n’est généralement pas important. 
>
>Le dernier relevé de solde est conservé sur le compte bancaire pour minimiser les erreurs lors des rapprochements bancaires, mais il est également modifiable, vous permettant d’effectuer vos rapprochements bancaires dans l’ordre de votre choix. Cela signifie également que si vous annulez un relevé bancaire, le nouveau solde de clôture peut ne pas être le dernier relevé du solde sur le prochain relevé bancaire. Il n’y a aucune fonctionnalité qui vous permet de transférer un solde vers tous les relevés bancaires suivants, donc soyez conscient de cela lorsque vous utilisez Annuler. 

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
