---
title: "Création des souches de numéros | Microsoft Docs"
description: "Découvrez comment configurer des souches de numéros qui affectent les codes d'identification uniques aux comptes et aux documents dans Business Central."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 03/27/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: 4d7e554300f0b445816ef9dd7fb81ea54fd25bf7
ms.contentlocale: fr-ch
ms.lasthandoff: 03/28/2018

---
# <a name="create-number-series"></a>Création des souches de numéros
Pour chaque société que vous configurez, vous devez affecter des codes d'identification uniques aux éléments tels que les comptes généraux, les comptes client et fournisseur, les factures et d'autres documents. La numérotation est importante, pas uniquement pour l'identification. Un système de numérotation bien conçu facilite la gestion et l'analyse de la société et permet de réduire les erreurs de saisie des données.

> [!NOTE]  
>   Il est recommandé d'utiliser les mêmes codes souche de numéros que ceux répertoriés dans la fenêtre **Liste de souches de numéros** de la société de démonstration CRONUS. Des codes tels que *P-INV+* ne vont pas vous paraître significatifs au premier abord, mais [!INCLUDE[d365fin](includes/d365fin_md.md)] dispose d'un certain nombre de paramètres par défaut en fonction de ces codes souche de numéros.

Vous créez un système de numérotation en définissant un ou plusieurs codes pour chaque type de données de base ou de document. Par exemple, vous pouvez définir un code pour la numérotation de clients, un code pour la numérotation des factures vente et un autre code pour la numérotation des documents dans les feuilles comptabilité. Une fois que vous avez défini un code, vous devez définir au moins une ligne souche de numéros. Celle-ci contient des informations telles que les premier et dernier numéros de la souche et la date de début. Vous pouvez définir plusieurs lignes souche de numéros par code souche de numéros, avec une date de début différente pour chaque ligne. Les souches sont utilisées de manière consécutive, chaque souche commençant à la date de début respective.

Vous devez généralement définir votre souche de numéros pour insérer automatiquement le numéro suivant sur des fiches ou des documents que vous créez. Toutefois, vous pouvez également définir une souche de numéros pour permettre la saisie manuelle du nouveau numéro. Vous spécifiez cela grâce à la case à cocher **N° manuels**.

Si vous voulez utiliser plusieurs codes souche de numéros pour un type de données de base (par exemple, si vous voulez utiliser différentes souches de numéros pour diverses catégories d'articles), vous pouvez utiliser des liens de souches de numéros.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportement du champ N° sur des documents et des fiches
Sur les documents de vente, d'achat et de transfert ainsi que sur toutes les fiches, le champ **N°** peut être renseigné automatiquement depuis une souche de numéros ou manuellement et peut être configuré pour être invisible.

Le champ **N°** peut être renseigné de trois manières :

1. Si une seule souche de numéros pour le type de document ou de fiche existe pour laquelle **N° par défaut** est cochée et la case à cocher **N° manuels** n'est pas cochée, alors le champ est renseigné automatiquement avec le numéro suivant dans la souche, et le champ **N°** n'est pas visible.

    > [!NOTE]  
    > Si une souche de numéros ne fonctionne pas, par exemple parce qu'elle manque de numéros, le champ **N°** est visible et vous pouvez saisir manuellement un numéro ou résoudre les problèmes dans la fenêtre **Liste de souches de numéros**.

2. Si plusieurs souches de numéros pour le type de document vente existent, et si la case à cocher **N° par défaut** n'est pas cochée pour la souche de numéros qui est actuellement affectée, le champ **N°** est visible, et vous pouvez accéder à la fenêtre **Liste Souche de n°** et sélectionnez la souche de numéros que vous souhaitez utiliser. Le numéro suivant dans la souche sélectionnée est inséré dans le champ **N°** .

3. Si vous n'avez défini aucune souche de numéros pour ce type de document ou fiche ou si le champ **N° manuels** est sélectionné pour la souche de numéros, alors le champ **N°** est visible et vous devez saisir manuellement les numéros. Vous pouvez entrer un maximum de 20 caractères alphanumériques.

Lorsque vous ouvrez un nouveau document ou une nouvelle fiche pour lequel il existe une souche de numéros, la fenêtre **Paramètres souche de n°** s'ouvre afin de pouvoir configurer une souche de numéros pour ce type de document ou fiche, avant de continuer avec une autre saisie de donnée.

> [!NOTE]  
> Si vous devez activer la numérotation manuelle, par exemple, les nouvelles fiches article qui ont été créées avec un processus de migration des données pour lesquelles le champ **N°** est masqué par défaut, allez ensuite dans la fenêtre **Paramètres stock** et choisissez le champ **N° article** pour ouvrir et définir la souche de numéros sur **N° manuels**.

## <a name="to-create-a-new-number-series"></a>Pour créer des souches de numéros
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Souches de n°**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Pour définir l'emplacement d'utilisation de la souche de numéros
La procédure suivante indique comment définir des souches de numéros pour la zone Ventes. La procédure est identique pour d'autres secteurs.
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Souches de n°**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Ventes**, dans le raccourci **Souche de numéros**, sélectionnez la souche de numéros souhaitée pour chaque fiche ou document vente.

Le numéro sélectionné est désormais utilisé pour renseigner le champ **N°** sur la fiche ou le document en question, en fonction des paramètres définis sur la ligne souche de numéros.

## <a name="to-create-relationships-between-number-series"></a>Pour créer des liens entre des souches de numéros
Si vous avez défini plusieurs codes souche de numéros pour un même type d'informations ou de transactions de base, vous pouvez créer des liens entre ces codes. Cette fonction peut vous aider à choisir parmi ces codes lorsque vous utilisez un numéro.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Souches de n°**, puis sélectionnez le lien connexe.
2. Sélectionnez la ligne avec la souche de numéros pour laquelle vous souhaitez créer des relations, puis cliquez sur **Relations**.
3. Dans le champ **Code souche**, entrez le code de la souche de numéros à lier à la souche sélectionnée à l'étape 2.
4. Ajoutez une ligne pour chaque code à lier à la souche de numéros sélectionnée.
5. Fermez la fenêtre.

Désormais, pour créer un élément nécessitant un numéro, vous pourrez utiliser les liens ainsi créés et choisir parmi les souches de numéros liées.

## <a name="see-also"></a>Voir aussi
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

