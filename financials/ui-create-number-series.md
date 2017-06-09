---
title: "Procédure : création des souches de numéros | Microsoft Docs"
description: "Découvrez comment créer une souche de numéros dans Dynamics 365 for Financials."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d5a6da604634540abdb67dcf4a82737f2db58b0b
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-number-series"></a>Procédure : création des souches de numéros
Pour chaque société que vous configurez, vous devez affecter des codes d'identification uniques aux éléments tels que les comptes généraux, les comptes client et fournisseur, les factures et d'autres documents. La numérotation est importante, pas uniquement pour l'identification. Un système de numérotation bien conçu facilite la gestion et l'analyse de la société et permet de réduire les erreurs de saisie des données.

**Remarque** : il est recommandé d'utiliser les mêmes codes souche de numéros que ceux répertoriés dans la fenêtre **Liste de souches de numéros** de la société de démonstration CRONUS. Des codes tels que *P-INV+* ne vont pas vous paraître significatifs au premier abord, mais [!INCLUDE[d365fin](includes/d365fin_md.md)] dispose d'un certain nombre de paramètres par défaut en fonction de ces codes souche de numéros.

Vous créez un système de numérotation en définissant un ou plusieurs codes pour chaque type de données de base ou de document. Par exemple, vous pouvez définir un code pour la numérotation de clients, un code pour la numérotation des factures vente et un autre code pour la numérotation des documents dans les feuilles comptabilité. Une fois que vous avez défini un code, vous devez définir au moins une ligne souche de numéros. Celle-ci contient des informations telles que les premier et dernier numéros de la souche et la date de début. Vous pouvez définir plusieurs lignes souche de numéros par code souche de numéros, avec une date de début différente pour chaque ligne. Les souches sont utilisées de manière consécutive, chaque souche commençant à la date de début respective.

Vous devez généralement définir votre souche de numéros pour insérer automatiquement le numéro suivant sur des fiches ou des documents que vous créez. Toutefois, vous pouvez également définir une souche de numéros pour permettre la saisie manuelle du nouveau numéro. Vous devez spécifiez cela dans **N° manuels** .

Si vous voulez utiliser plusieurs codes souche de numéros pour un type de données de base (par exemple, si vous voulez utiliser différentes souches de numéros pour diverses catégories d'articles), vous pouvez utiliser des liens de souches de numéros.

## <a name="to-create-a-new-number-series"></a>Pour créer des souches de numéros
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Souches de n°**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**ASTUCE** : pour permettre la saisie manuelle d'un numéro sur de nouvelles fiches ou de nouveaux documents, désélectionnez **N° par défaut** et sélectionnez **N° manuels** .

Désormais, lorsque vous créez une fiche ou un document configuré pour utiliser la souche de numéros en question, vous pouvez renseigner manuellement le champ **N°** avec n'importe quelle valeur.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Pour définir l'emplacement d'utilisation de la souche de numéros
La procédure suivante indique comment définir des souches de numéros pour la zone Ventes. La procédure est identique pour d'autres secteurs.
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Ventes**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Ventes**, dans le raccourci **Souche de numéros**, sélectionnez la souche de numéros souhaitée pour chaque fiche ou document vente.

Le numéro sélectionné est désormais utilisé pour renseigner le champ **N°** sur la fiche ou le document en question, en fonction des paramètres définis sur la ligne souche de numéros.

## <a name="to-create-relationships-between-number-series"></a>Pour créer des liens entre des souches de numéros
Si vous avez défini plusieurs codes souche de numéros pour un même type d'informations ou de transactions de base, vous pouvez créer des liens entre ces codes. Cette fonction peut vous aider à choisir parmi ces codes lorsque vous utilisez un numéro.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Souches de n°**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne avec la souche de numéros pour laquelle vous souhaitez créer des relations, puis cliquez sur **Relations**.
3. Dans le champ **Code souche**, entrez le code de la souche de numéros à lier à la souche sélectionnée à l'étape 2.
4. Ajoutez une ligne pour chaque code à lier à la souche de numéros sélectionnée.
5. Fermez la fenêtre.

Désormais, pour créer un élément nécessitant un numéro, vous pourrez utiliser les liens ainsi créés et choisir parmi les souches de numéros liées.

## <a name="see-also"></a>Voir aussi
[Configuration [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

