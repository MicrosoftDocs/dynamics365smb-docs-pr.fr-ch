---
title: "Procédure : mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique| Microsoft Docs"
description: "Procédure : Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7c6f79959027625a33961d42abe26514bc94e81e
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Procédure : Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique
Dans la fenêtre **Correspondance texte et compte** à laquelle vous accédez à partir de la fenêtre **Feuille rapprochement bancaire**, vous pouvez configurer des mappages entre le texte des paiements et des comptes de débit, de crédit et de contrepartie spécifiques afin que ces paiements soient validées dans les comptes spécifiés lorsque vous validez la feuille rapprochement bancaire.

**Remarque** : la rubrique s'applique également lorsque vous utilisez la fonction **Mapper le texte** avec le compte à partir d'un enregistrement document entrant pour accompagner la conversion des documents électroniques reçus des services externes en documents dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour en savoir plus, voir [Procédure : utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md).   

Une fonctionnalité similaire existe pour rapprocher les montants en excédent sur les lignes feuille rapprochement bancaire de façon ponctuelle. Pour plus d'informations, reportez-vous à [Procédure : rapprocher les paiements qui ne peuvent pas être lettrés automatiquement](receivables-how-reconcile-payments-cannot-apply-auto.md).

Les paiements validés basés sur le mappage de texte à compte ne sont pas appliqués aux écritures ouvertes, mais sont simplement validés dans les comptes spécifiés en plus de créer des écritures comptables compte bancaire. Par conséquent, le mappage de texte à compte est approprié pour les recettes ou dépenses récurrentes en liquide, notamment les achats fréquents de carburant pour les voitures ou les frais et intérêts bancaires, qui apparaissent régulièrement sur le relevé bancaire et n'ont pas besoin d'un document d'entreprise lié. Pour en savoir plus, voir « Exemple – Mappage de texte à compte pour les frais de carburant » dans cette rubrique.

**Remarque** : les paiements sur les lignes feuille rapprochement bancaire sont uniquement définies sur validation en fonction du mappage de texte à compte si la fonction de lettrage automatique peut fournir un taux de fiabilité correspondance **Faible** ou **Moyen**. Si la fonction de lettrage automatique fournit un taux de fiabilité correspondance Élevé, alors le paiement est automatiquement lettré à une ou plusieurs écritures ouvertes, et le paiement n'est pas validé dans les comptes spécifiés dans la fenêtre **Correspondance texte et compte**. En d'autres termes, une confiance de correspondance **Élevée** outrepasse un mappage de texte à compte.

Sur une ligne feuille rapprochement bancaire dont le paiement a été défini sur validation en fonction du mappage de texte à compte, le champ **Fiabilité correspondance** contient la valeur **Élevé – Mappage de texte à compte**, et les champs **Type compte** et **N° compte** contiennent les comptes mappés.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Pour associer le texte sur les paiements récurrents aux comptes pour un rapprochement automatique
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuilles rapprochement bancaire**, puis sélectionnez le lien associé.
2. Ouvrez une feuille de rapprochement de paiement. Pour plus d'informations, reportez-vous à [Procédure : rapprocher les paiements à l'aide de l'application automatique](receivables-how-reconcile-payments-auto-application.md).
3. Sélectionnez l'action **Mapper le texte avec le compte**. La fenêtre **Correspondance texte et compte** s'affiche.
4. Dans le champ **Correspondance texte**, saisissez n'importe quel texte se produisant sur les paiements que vous souhaitez valider dans les comptes spécifiés sans les appliquer à une écriture ouverte. Vous pouvez entrer jusqu'à 50 caractères.

    **Remarque** : si aucun autre paiement ni document entrant n'existe avec le texte de mappage en question, le mappage du texte avec le compte surviendra uniquement lorsqu'une seule partie du texte de paiement ou du document entrant existe en tant que texte de mappage.
5. Dans le champ **N° fournisseur** , saisissez le fournisseur pour lequel des documents entrants contenant le texte de mappage seront créés, ou pour lequel des paiements seront validés. Pour en savoir plus, voir [Procédure : utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md).      
6. Dans le champ **N° cpte débit** saisissez le numéro de compte dans lequel les paiements contenant le texte de mappage sont validés s'il s'agit de paiements entrants. Pour les paiements entrants, le signe de la valeur du champ **Montant relevé** est positif.
7. Dans le champ **N° cpte crédit** saisissez le compte dans lequel les paiements contenant le texte de mappage sont validés s'il s'agit de paiements sortants. Pour les paiements sortants, le signe de la valeur du champ **Montant relevé** est négatif.
8. Dans le champ **Type origine solde**, indiquez si le paiement est validé dans un compte général ou dans un compte client ou fournisseur.
9. Dans le champ **N° origine solde**, indiquez le compte dans lequel le paiement est validé, en fonction de votre sélection dans le champ **Type origine solde**.
10. Répétez les étapes 4 à 8 pour tout le texte sur les paiements que vous souhaitez mapper à des comptes pour une validation directe sans application.

La prochaine fois que vous importez un fichier de relevé bancaire ou sélectionnez l'action **Lettrer automatiquement** dans la fenêtre **Feuille rapprochement bancaire**, les lignes feuille pour les paiements qui contiennent le texte de mappage spécifié contiendront les comptes mappés dans les champs **Type compte** et **N° compte**. . Le champ **Fiabilité correspondance** contient **Élevée - Correspondance texte et compte**. Ce, à condition que la fonction de lettrage automatique ne puisse fournir qu'une fiabilité de correspondance **Basse** ou **Moyenne**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Exemple : mappage de texte à compte pour les frais de carburant
Pour toujours valider les frais de carburant encourus aux stations service Shell dans le compte général pour l'essence (compte 8510), renseignez une ligne de la fenêtre **Correspondance texte et compte** comme suit.

| Correspondance texte | Cpte débit N° | Cpte crédit N° | Contrepartie Type origine | Contrepartie N° origine |
| --- | --- | --- | --- | --- |
| Shell |VIDE |8510 |Compte général |VIDE |

**Conseil** : pour plus d'informations sur l'utilisation des champs et des colonnes, voir [Utilisation de [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md). Pour plus d'informations sur la recherche de pages spécifiques, reportez-vous à [Rechercher](ui-search.md)..

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Procédure : configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

