---
title: "Paramétrer la maintenance des immobilisations| Microsoft Docs"
description: "Pour gérer les réparations et la maintenance des immobilisations, spécifiez les informations de maintenance générale, les codes du type de travail, et un compte de validation pour les coûts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: aef3d672bf01425a36bdd599e18d9ee9dac73b2d
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-maintenance"></a>Configurer la maintenance d'une immobilisation
Pour gérer la maintenance des immobilisations, vous devez configurer tout d'abord certaines informations générales de maintenance, un compte de validation pour les coûts de maintenance et les codes de maintenance pour les types de travaux, tels que le service de routine ou la réparation.

## <a name="to-set-up-general-maintenance-information"></a>Pour configurer les informations générales de maintenance
Si vous configurez les champs pour la maintenance, vous pouvez valider des frais de maintenance à partir d'une feuille immobilisation.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l'immobilisation pour laquelle vous souhaitez définir la couverture d'assurance, puis sélectionnez l'action **Modifier**.
3. Sur le raccourci **Maintenance**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Pour configurer des codes maintenance
Lorsque vous validez des coûts de maintenance à partir d'une feuille comptabilité, vous renseignez le champ **Code maintenance** pour enregistrer le type de maintenance effectuée, telle qu'un service de routine ou une réparation.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Maintenance**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Maintenance**, configurez les codes pour les différents types de travaux de maintenance.

## <a name="to-set-up-maintenance-expense-accounts"></a>Pour configurer des comptes frais de maintenance
Pour valider les coûts de maintenance, vous devez tout d'abord saisir un numéro de compte dans la fenêtre **Groupes compta. immo**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes compta. immo.**, puis sélectionnez le lien associé.
2. Renseignez le champ **Compte frais maintenance** pour chaque groupe comptabilisation.

> [!NOTE]  
>   Pour définir que les coûts de maintenance sont attribués aux départements ou projets, configurez une clé d'allocation. Pour en savoir plus, voir [Configurer des fonctionnalités d'immobilisations](fa-how-setup-general.md).

## <a name="see-also"></a>Voir aussi
[Paramétrage d'immobilisations](fa-setup.md)  
[COMPTES D'IMMOBILISATIONS](fa-manage.md)  
[Finances](finance.md)  
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

