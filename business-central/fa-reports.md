---
title: États et analyses des immobilisations
description: Découvrez les états et analyses disponibles dans la version standard de Business Central afin que vous puissiez suivre vos immobilisations.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543419"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>États et analyses d’immobilisation dans Business Central

Pour vous aider à gérer vos immobilisations dans [!INCLUDE [prod_short](includes/prod_short.md)], des états et des analyses standard sont intégrés. Ils vont au-delà des contraintes des rapports traditionnels pour vous aider à concevoir efficacement divers types de rapports.  

## <a name="reports"></a>États

Le tableau suivant décrit certains des principaux états dans les états d’immobilisation.

| État | ID d’objet | Description |
|--|--|--|
| **Liste des immobilisations** | 5 601 | Affiche la liste des immobilisations et leurs informations de configuration pour une loi d’amortissement donnée. |
| **Immo. - Liste des acquisitions** | 5608 | Répertoriez tous les actifs acquis dans une plage de dates donnée. Vous pouvez également inclure des immobilisations créées, mais pas encore acquises. |
| **Détails de l’immobilisation** | 5604 | Affiche les écritures comptables des immobilisations pour les immobilisations. |
| **Analyse de l’immobilisation** | 5600 | Rapport d’analyse où vous pouvez spécifier deux colonnes de date et trois colonnes de données à afficher dans l’état. Par exemple, pour générer un état à utiliser pour le rapprochement avec le grand livre, ajoutez des colonnes pour le coût d’acquisition à la date finale, l’amortissement à la date finale et la valeur comptable à la date finale. Un rapport de contrôle peut comporter des acquisitions/solde période, une dépréciation/solde période et une réévaluation/solde période de sorte que chaque modification apportée aux immobilisations puisse être vérifiée si nécessaire. Si vous sélectionnez le champ **État budget** et spécifiez une date finale ultérieure, l’état calcule l’amortissement ultérieur et peut donner des estimations pour l’amortissement ultérieur et les valeurs comptables, si vous avez sélectionné ces champs comme colonnes d’état. |
| **Valeur projetée de l’immobilisation** | 5607 | Affiche les montants d’amortissement projetés et la valeur comptable pour une période ultérieure des actifs. Cet état est très pratique si vous utilisez différentes méthodes d’amortissement pour vos actifs et si vous souhaitez estimer l’amortissement de l’année prochaine, par exemple. Utilisez l’état pour créer les montants budgétaires pour l’amortissement en sélectionnant un budget et le champ **Copier vers budget comptable**. |
| **Immo. Valeur comptable 01** | 5605 | Affiche des informations détaillées concernant le coût d’acquisition, la valeur d’amortissement et la valeur comptable à la fois pour les immobilisations individuelles et les groupes d’immobilisations. Pour ces trois types de montants, les calculs sont effectués au début et à la fin d’une période spécifique et pour la période elle-même. Si vous sélectionnez le champ **État budget**, l’état calcule l’amortissement prévu pour la période. Saisissez un *type de groupe* si vous souhaitez que l’état regroupe les immobilisations et imprime des sous-totaux. Par exemple, si vous avez configuré six classes immobilisation, sélectionnez l’option *Classe immobilisation* pour que les totaux de groupe soient imprimés pour chaque code des six classes.|
| **Immo. Valeur comptable 02** | 5606 |Affiche la répartition de la valeur comptable des immobilisations en fonction des variations d’acquisition, d’amortissement et de réévaluation au cours de la période, avec une ventilation supplémentaire par acquisitions et cessions au cours de la période. Utilisez cet état pour décrire les changements dans les immobilisations pour une période donnée lorsque de nombreux changements différents se produisent dans le groupe d’immobilisations. Si vous sélectionnez le champ **État budget**, l’état calcule l’amortissement prévu pour la période. Saisissez un *type de groupe* si vous souhaitez que l’état regroupe les immobilisations et imprime des sous-totaux. Par exemple, si vous avez configuré six classes immobilisation, sélectionnez l’option *Classe immobilisation* pour que les totaux de groupe soient imprimés pour chaque code des six classes. |
| **Analyse comptabilité immobilisation**| 5610 |Affiche une analyse de vos immobilisations en incluant divers types de données, pour les immobilisations et les classes d’immobilisations. Vous pouvez positionner des filtres sur le raccourci Immobilisation pour n’inclure que certaines immobilisations dans l’état. Dans le raccourci Options, personnalisez l’état pour répondre à vos besoins spécifiques. L’état est similaire à l’état **Analyse de l’immobilisation**, mais notamment pour le rapprochement avec la comptabilité et notamment pour la validation des écritures de cession. L’état suppose que vous connaissiez les comptes généraux spécifiés dans la configuration de validation. |
| **Hist. transactions immo.** |5603  |Affiche les écritures comptables immobilisation validées triées et réparties par numéro d’historique. Vous pouvez déterminer les écritures affichées en positionnant un filtre. Il est important de positionner un filtre ; dans le cas contraire, l’état risque en effet d’afficher de nombreuses informations. |

## <a name="see-also"></a>Voir aussi

[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Gestion des immobilisations](fa-manage.md)  
[Vue d’ensemble des fonctionnalités locales](about-localization.md)  
[Expériences de comptable dans [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
