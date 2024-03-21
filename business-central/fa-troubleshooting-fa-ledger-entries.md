---
title: L’extension Dépannage des écritures comptables immobilisation
description: Il est plus facile de travailler avec des nombres entiers. Utilisez cette extension pour arrondir les montants des immobilisations dans les écritures comptables immobilisation.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# L’extension Dépannage des écritures comptables immobilisation
Utilisez l’extension Dépannage des écritures comptables immobilisation pour arrondir les montants d’amortissement et d’acquisition dans les écritures comptables immobilisation à des nombres entiers. Par exemple, pour arrondir un montant de 30 000,44 à 30 000. Les causes habituelles des problèmes d’arrondi sont la migration des données, le démarrage soudain de la validation de montants dans la comptabilité ou les personnalisations que vous avez apportées à votre [!INCLUDE[prod_short](includes/prod_short.md)].

L’extension Dépannage des écritures comptables immobilisation est pré-installée et prête à l’emploi. Si vous supprimez l’extension, mais que vous souhaitez la réinstaller, vous pouvez la trouver sur AppSource.

## Dépannage des écritures comptables immobilisation
Lorsque vous ouvrez la page **Fiche immobilisation** pour la première fois, l’entrée de file d’attente de tâches **Analyser les écritures comptables immobilisation** est programmée pour surveiller les montants tous les dimanches. Si des montants que vous souhaitez peut-être arrondir sont trouvés, une notification s’affichera la prochaine fois que vous ouvrirez la page Fiche immobilisation. La notification fournit une option **Voir plus** qui ouvre la page **Écritures comptables immo. avec des erreurs d’arrondis**, qui répertorie les entrées comportant des montants que vous souhaitez peut-être arrondir. Pour arrondir les montants, choisissez les écritures, puis choisissez l’action **Accepter la sélection**. Vous pouvez utiliser l’action **Rechercher des écritures avec des erreurs** pour mettre à jour la liste avec les nouveaux problèmes survenus après l’exécution de l’entrée de la file d’attente des tâches le dimanche précédent.

## Voir aussi
[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Gestion des immobilisations](fa-manage.md)  
[Mettre à jour des immobilisations](fa-how-maintain.md)  
[Personnalisation de Business Central Online à l’aide d’extensions](ui-extensions.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



