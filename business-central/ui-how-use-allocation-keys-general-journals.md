---
title: Utiliser les clés de ventilation dans les feuilles comptabilité | Microsoft Docs
description: En savoir plus sur l’utilisation des clés de ventilation dans les feuilles.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84ea436a7e7edc6851b97b718b66195edddd2da2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760507"
---
# <a name="use-allocation-keys-in-general-journals"></a>Utiliser les clés de ventilation dans les feuilles de comptabilité
Vous pouvez ventiler une écriture dans une feuille comptabilité dans différents comptes lorsque vous validez la feuille. La ventilation peut être effectuée par quantité, pourcentage ou montant.

## <a name="to-set-up-allocation-keys"></a>Pour définir des clés de ventilation
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille abonnement**, puis sélectionnez le lien associé.
2. Sélectionnez le champ **Nom de la feuille** pour ouvrir la page **Noms feuilles comptabilité**.
3. Vous pouvez soit modifier les ventilations sur un lot existant dans la liste ou créer un lot avec des ventilations.
   * Pour créer un lot, sélectionnez l’action **Nouveau**, et passez à l’étape suivante.
   * Pour modifier les ventilations à partir d’une feuille existante, sélectionnez la feuille et passez à l’étape 7.    
4. Dans le champ **Nom**, saisissez le nom du lot, par exemple NETTOYAGE. Dans le champ **Description**, saisissez une description, par exemple Feuille frais de nettoyage.
5. Fermez la page lorsque vous avez terminé. Une nouvelle feuille récurrente vide s’ouvre.
6. Renseignez les champs de la ligne.
7. Sélectionnez l’action **Ventilations**.
8. Ajoutez une ligne pour chaque ventilation. Vous devez renseigner le champ **% ventilation**, **Quantité imputée** ou **Montant**. Vous devez également renseigner le champ **N° compte** et, si vous affectez la transaction à des axes principaux, les champs de ces axes principaux.
9. Si vous saisissez un pourcentage dans une ligne, le montant du champ **Montant** est calculé automatiquement. Ces montants sont dotés du signe opposé à celui du montant total figurant dans le champ **Montant** de la feuille récurrente.
10. Après avoir saisi les lignes de ventilation, cliquez sur **OK** pour revenir à la page **Feuille abonnement**. Le champ **Montant imputé DS** est renseigné et correspond au champ **Montant**.
11. Validez la feuille.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Pour modifier une clé de ventilation déjà configurée
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille abonnement**, puis sélectionnez le lien associé.
2. Sur la page **Feuille récurrente**, sélectionnez la feuille contenant la ventilation.
3. Sélectionnez la ligne de la ventilation, puis sélectionnez l’action **Ventilations**.
4. Modifiez les champs appropriés, puis cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Validation des documents et des feuilles](ui-post-documents-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]