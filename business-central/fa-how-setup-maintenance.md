---
title: Paramétrer la maintenance des immobilisations| Microsoft Docs
description: Pour gérer les réparations et la maintenance des immobilisations, spécifiez les informations de maintenance générale, les codes du type de travail, et un compte de validation pour les coûts.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b437f7508537ec438bf90c3a1239e2620e9db196
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775565"
---
# <a name="set-up-fixed-asset-maintenance"></a>Configurer la maintenance d’une immobilisation
Pour gérer la maintenance des immobilisations, vous devez configurer tout d’abord certaines informations générales de maintenance, un compte de validation pour les coûts de maintenance et les codes de maintenance pour les types de travaux, tels que le service de routine ou la réparation.

## <a name="to-set-up-general-maintenance-information"></a>Pour configurer les informations générales de maintenance
Si vous configurez les champs pour la maintenance, vous pouvez valider des frais de maintenance à partir d’une feuille immobilisation.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Immobilisations**, puis sélectionnez le lien associé.
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez définir la couverture d’assurance, puis sélectionnez l’action **Modifier**.
3. Sur le raccourci **Maintenance**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Pour configurer des codes maintenance
Lorsque vous validez des coûts de maintenance à partir d’une feuille comptabilité, vous renseignez le champ **Code maintenance** pour enregistrer le type de maintenance effectuée, telle qu’un service de routine ou une réparation.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Maintenance**, puis sélectionnez le lien associé.
2. Sur la page **Maintenance**, configurez les codes pour les différents types de travaux de maintenance.

## <a name="to-set-up-maintenance-expense-accounts"></a>Pour configurer des comptes frais de maintenance
Pour valider les coûts de maintenance, vous devez tout d’abord saisir un numéro de compte sur la page **Groupes compta. immo**.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes compta. immo.**, puis sélectionnez le lien associé.
2. Renseignez le champ **Compte frais maintenance** pour chaque groupe comptabilisation.

> [!NOTE]  
>   Pour définir que les coûts de maintenance sont attribués aux départements ou projets, configurez une clé d’allocation. Pour en savoir plus, voir [Configurer des fonctionnalités d’immobilisations](fa-how-setup-general.md).

## <a name="see-also"></a>Voir aussi
[Paramétrage d’immobilisations](fa-setup.md)  
[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]