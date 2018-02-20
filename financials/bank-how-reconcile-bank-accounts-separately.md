---
title: "Rapprocher des comptes bancaires séparément| Microsoft Docs"
description: "Décrit la manière dont la valeur du stock fait l'objet d'un rapprochement avec la comptabilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa1225e8467ab805fc14afdd39eef556dc7ad5fc
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Rapprocher des comptes bancaires séparément
Pour rapprocher des comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des relevés reçus de la banque, vous devez renseigner les lignes de la fenêtre **Rapprochement bancaire**.

> [!NOTE]  
>   Vous pouvez également rapprocher des comptes bancaires dans la fenêtre **Feuille rapprochement paiement**. Toutes les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées lorsque vous sélectionnez l'action **Valider les paiements et rapprocher les comptes bancaires**. Cela signifie que le compte bancaire est automatiquement rapproché pour les paiements que vous validez avec le journal. Pour plus d'informations, voir [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

Pour activer l'importation des relevés bancaires en tant que flux bancaires, vous devez d'abord configurer et activer le service de flux de la Envestnet Yodlee Bank, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d'informations, voir [Configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).

Les lignes de la fenêtre **Rapprochement bancaire** sont réparties sur deux volets. Le volet **Lignes relevé bancaire** indique le volet des transactions bancaires importées ou les écritures comptables comportant des arriérés de paiement. Le volet **Écritures comptables compte bancaire** affiche les écritures comptables dans le compte bancaire.

L'activité de recherche et de lettrage des écritures à rapprocher est appelée *mise en correspondance*. Vous pouvez choisir d'effectuer la correspondance automatiquement à l'aide de la fonction **Match Automatically**. Sinon, vous pouvez sélectionner manuellement des lignes dans les deux volets pour lier chaque ligne relevé bancaire à une ou plusieurs écritures comptables compte bancaire correspondantes, puis utiliser la fonction **Faire correspondre manuellement**. La case **Lettré** est cochée sur les lignes pour lesquelles les écritures correspondent.

Vous pouvez renseigner le volet **Lignes relevé bancaire** de la fenêtre **Rapprochement bancaire** comme suit :

* Automatiquement, à l'aide de la fonction **Importer le relevé bancaire** qui renseigne les lignes en fonction des relevés bancaires réels sur la base d'un fichier fourni par la banque.
* Manuellement, en utilisant la fonction **Proposer lignes** pour renseigner les lignes avec les écritures comptables pour les factures comportant des arriérés de paiement.

Lorsque la valeur du champ **Solde final** du volet **Lignes relevé bancaire** est égale à la valeur du champ **Solde à simuler** du volet **Écritures comptables compte bancaire**, vous pouvez sélectionner l'action **Valider** pour rapprocher les écritures comptables compte bancaire lettrées. Toutes les écritures comptables compte bancaire non lettrées restent dans la fenêtre, ce qui indique que les paiements traités pour le compte bancaire ne sont pas répercutés sur le dernier relevé bancaire, ou que certains paiements ont été réceptionnés par chèque.

> [!NOTE]  
>   Si les lignes de relevé bancaire sont liées à des écritures comptables chèque, vous ne pouvez pas utiliser les fonctions de mise en correspondance. Au lieu de cela, vous devez sélectionner l'action **Lettrer écritures**, puis sélectionner l'écriture comptable chèque appropriée avec laquelle mettre en correspondance la ligne de relevé bancaire.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Pour renseigner les lignes rapprochement bancaire en important un relevé bancaire
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Rapprochement bancaire**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N° compte bancaire**, sélectionnez le compte bancaire approprié. Les écritures comptables compte bancaire qui existent pour le compte bancaire s'affichent le volet **Écritures comptables compte bancaire**.
4. Dans le champ **Date relevé**, saisissez la date du relevé de banque.
5. Dans le champ **Solde final du relevé**, saisissez le solde du relevé de banque.
6. Si vous avez un fichier de relevé bancaire, sélectionnez l'action **Importer le relevé bancaire**.
7. Localisez le fichier, puis sélectionnez le bouton **Ouvrir** pour importer les transactions bancaires dans les lignes de la fenêtre **Rapprochement bancaire**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Pour renseigner les lignes rapprochement bancaire avec la fonction Proposer lignes
1. Dans la fenêtre **Rapprochement bancaire**, sélectionnez l'action **Proposer lignes**.
2. Dans le champ **Date de début**, saisissez la date de validation la plus précoce des écritures comptables à rapprocher.
3. Dans le champ **Date de fin**, saisissez la date de validation la plus tardive des écritures comptables à rapprocher.
4. Cochez la case **Inclure les chèques** pour les écritures comptables chèque proposées au lieu des écriture comptables compte bancaire correspondantes.
5. Cliquez sur le bouton **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Pour mettre en correspondance automatiquement des lignes de relevé bancaire avec des écritures comptables compte bancaire
1. Dans la fenêtre **Rapprochement bancaire**, sélectionnez l'action **Faire correspondre automatiquement**. La fenêtre **Faire correspondre les écritures bancaires** s'ouvre.
2. Dans le champ **Tolérance date transaction (jours)**, spécifiez le nombre de jours avant et après la date comptabilisation de l'écriture comptable compte bancaire pendant lesquels la fonction recherchera des dates transaction correspondantes dans le relevé bancaire.

    Si vous saisissez 0 ou laissez le champ vide, la fonction **Faire correspondre automatiquement** recherchera uniquement les dates de transaction correspondantes sur la date comptabilisation de l'écriture comptable compte bancaire.
3. Cliquez sur le bouton **OK**.

    Toutes les lignes de relevé bancaire et les écritures comptables compte bancaire qui peuvent être rapprochées deviennent vertes, et la case **Lettré** est cochée.
4. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Pour mettre en correspondance des lignes de relevé bancaire avec les écritures comptables compte bancaire manuellement
1. Dans la fenêtre **Rapprochement bancaire**, sélectionnez une ligne non lettrée dans le volet **Lignes relevé bancaire**.
2. Dans le volet **Écritures comptables compte bancaire**, sélectionnez une ou plusieurs écritures comptables compte bancaire qui peuvent être mise en correspondance avec la ligne de relevé bancaire sélectionnée. Pour choisir plusieurs lignes, appuyez et maintenez la touche Ctrl enfoncée.
3. Sélectionnez l'action **Faire correspondre manuellement**.

    La ligne de relevé bancaire sélectionnée et les écritures comptables compte bancaire sélectionnées deviennent vertes, et la case à cocher **Lettré** du volet de droite est activée.
4. Répétez les étapes 1 à 3 pour toutes les lignes de relevé bancaire qui ne sont pas mises en correspondance.
5. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Pour créer les écritures comptables manquantes avec lesquelles faire correspondre des transactions bancaires
Les relevés bancaires comportent parfois des montants correspondant à la facturation d'intérêts ou de frais. Ces transactions bancaires ne peuvent pas être mises en correspondance car il n'existe aucune écriture comptable associée dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous devez ensuite valider une ligne feuille pour chaque transaction afin de créer une écriture comptable associée avec laquelle elle peut être mise en correspondance.

1. Dans la fenêtre **Rapprochement bancaire**, sélectionnez l'action **Transférer vers feuille comptabilité**.  
2. Dans la fenêtre **Trans. rappr. banc. -> f. cpta**, indiquez la feuille de comptabilité à utiliser, puis cliquez sur le bouton **OK**.

    La fenêtre **Feuille comptabilité** s'ouvre. Elle contient de nouvelles lignes feuille pour toutes les lignes de relevé bancaire dont les écritures comptables sont manquantes.
3. Renseignez la ligne feuille avec les informations appropriées, comme le compte de contrepartie. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  
4. Sélectionnez l'action **Valider**.

    Lorsque l'écriture est validée, faites-lui correspondre la transaction bancaire appropriée.
5. Réactualisez ou rouvrez la fenêtre **Rapprochement bancaire**. La nouvelle écriture comptable s'affiche dans le volet **Écritures comptables compte bancaire**.
6. Faites correspondre la ligne relevé bancaire à l'écriture comptable compte bancaire, manuellement ou automatiquement.

## <a name="see-also"></a>Voir aussi
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

