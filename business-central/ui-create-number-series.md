---
title: Création des souches de numéros | Microsoft Docs
description: Découvrez comment configurer des souches de numéros qui affectent les codes d’identification uniques aux comptes et aux documents dans Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b61f4fb5cdcee284b183a08c70224348c99530cd
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757632"
---
# <a name="create-number-series"></a>Création des souches de numéros
Pour chaque société que vous configurez, vous devez affecter des codes d’identification uniques aux éléments tels que les comptes généraux, les comptes client et fournisseur, les factures et d’autres documents. La numérotation est importante, pas uniquement pour l’identification. Un système de numérotation bien conçu facilite la gestion et l’analyse de la société et permet de réduire les erreurs de saisie des données.

> [!Important]
> Par défaut, les écarts dans les séries de numéros ne sont pas autorisés car l’historique exact des transactions financières doit être disponible pour audit, conformément à la loi, et doit donc suivre une séquence ininterrompue sans numéros supprimés.<br /><br />
Si vous souhaitez autoriser des écarts dans certaines séries de nombres, commencez par consulter l’auditeur ou le responsable de la comptabilité pour vous assurer de respecter les exigences légales en vigueur dans votre pays/région. Pour plus d’informations, voir [Écarts dans les souches de numéros](ui-create-number-series.md#gaps-in-number-series).

> [!NOTE]  
>   Il est recommandé d’utiliser les mêmes codes souche de numéros que ceux répertoriés sur la page **Liste de souches de numéros** de la société de démonstration CRONUS. Des codes tels que *P-INV+* ne vont pas vous paraître significatifs au premier abord, mais [!INCLUDE[prod_short](includes/prod_short.md)] dispose d’un certain nombre de paramètres par défaut en fonction de ces codes souche de numéros.

Vous créez un système de numérotation en définissant un ou plusieurs codes pour chaque type de données de base ou de document. Par exemple, vous pouvez définir un code pour la numérotation de clients, un code pour la numérotation des factures vente et un autre code pour la numérotation des documents dans les feuilles comptabilité. Une fois que vous avez défini un code, vous devez définir au moins une ligne souche de numéros. Celle-ci contient des informations telles que les premier et dernier numéros de la souche et la date de début. Vous pouvez définir plusieurs lignes souche de numéros par code souche de numéros, avec une date de début différente pour chaque ligne. Les souches sont utilisées de manière consécutive, chaque souche commençant à la date de début respective.

Vous devez généralement définir votre souche de numéros pour insérer automatiquement le numéro suivant sur des fiches ou des documents que vous créez. Toutefois, vous pouvez également définir une souche de numéros pour permettre la saisie manuelle du nouveau numéro. Vous spécifiez cela grâce à la case à cocher **N° manuels**.

Si vous voulez utiliser plusieurs codes souche de numéros pour un type de données de base (par exemple, si vous voulez utiliser différentes souches de numéros pour diverses catégories d’articles), vous pouvez utiliser des liens de souches de numéros.

## <a name="gaps-in-number-series"></a>Écarts dans les souches de numéros
Tous les enregistrements que vous créez dans [!INCLUDE[prod_short](includes/prod_short.md)] ne sont pas des transactions financières qui doivent utiliser une numérotation séquentielle. Les fiches client, les devis, et les activités d’entrepôt sont des exemples d’enregistrements auxquels un numéro d’une série de numéros est attribué, mais qui ne sont pas soumis à l’audit financier et/ou peuvent être supprimés. Pour ces séries de numéros, vous pouvez cocher la case **Autoriser les écarts dans les numéros** sur la page **Lignes souche de n°**. Ce paramètre peut être également modifié après la création de la série de numéros. Pour plus d’informations, voir [Pour créer des souches de numéros](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportement du champ N° sur des documents et des fiches
Sur les documents de vente, d’achat et de transfert ainsi que sur toutes les fiches, le champ **N°** peut être renseigné automatiquement depuis une souche de numéros ou manuellement et peut être configuré pour être invisible.

Le champ **N°** peut être renseigné de trois manières :

1. Si une seule souche de numéros pour le type de document ou de fiche existe pour laquelle **N° par défaut** est cochée et la case à cocher **N° manuels** n’est pas cochée, alors le champ est renseigné automatiquement avec le numéro suivant dans la souche, et le champ **N°** n’est pas visible.

    > [!NOTE]  
    > Si une souche de numéros ne fonctionne pas, par exemple parce qu’elle manque de numéros, le champ **N°** est visible et vous pouvez saisir manuellement un numéro ou résoudre les problèmes sur la page **Souches de n°**.

2. Si plusieurs souches de numéros pour le type de document vente existent, et si la case à cocher **N° par défaut** n’est pas cochée pour la souche de numéros qui est actuellement affectée, le champ **N°** est visible, et vous pouvez accéder à la page **Liste Souche de n°** et sélectionnez la souche de numéros que vous souhaitez utiliser. Le numéro suivant dans la souche sélectionnée est inséré dans le champ **N°** .

3. Si vous n’avez défini aucune souche de numéros pour ce type de document ou fiche ou si le champ **N° manuels** est sélectionné pour la souche de numéros, alors le champ **N°** est visible et vous devez saisir manuellement les numéros. Vous pouvez entrer un maximum de 20 caractères alphanumériques.

Lorsque vous ouvrez un nouveau document ou une nouvelle fiche pour lequel il existe une souche de numéros, la page **Paramètres souche de n°** s’ouvre afin de pouvoir configurer une souche de numéros pour ce type de document ou fiche, avant de continuer avec une autre saisie de donnée.

> [!NOTE]  
> Si vous devez activer la numérotation manuelle, par exemple, les nouvelles fiches article qui ont été créées avec un processus de migration des données pour lesquelles le champ **N°** est masqué par défaut, allez ensuite sur la page **Paramètres stock** et choisissez le champ **N° article** pour ouvrir et définir la souche de numéros sur **N° manuels**.

## <a name="to-create-a-new-number-series"></a>Pour créer des souches de numéros
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Souches de n°**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Sélectionnez l’option **Lignes**.
5. Sur la page **Lignes souche de n°**, remplissez les champs pour définir l’utilisation réelle et le contenu de la série de numéros créée à l’étape 2.
6. Répétez l’étape 5 pour autant d’utilisations différentes de la série de chiffres dont vous avez besoin. Le champ **Date de début** définit quelle ligne de série de numéros est active.

## <a name="to-set-up-where-a-number-series-is-used"></a>Pour définir l’emplacement d’utilisation de la souche de numéros
La procédure suivante indique comment définir des souches de numéros pour la zone Ventes. La procédure est identique pour d’autres secteurs.
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ventes**, puis sélectionnez le lien associé.
2. Sur la page **Ventes**, dans le raccourci **Souche de numéros**, sélectionnez la souche de numéros souhaitée pour chaque fiche ou document vente.

Le numéro sélectionné est désormais utilisé pour renseigner le champ **N°** sur la fiche ou le document en question, en fonction des paramètres définis sur la ligne souche de numéros.

## <a name="to-create-relationships-between-number-series"></a>Pour créer des liens entre des souches de numéros
Si vous avez défini plusieurs codes souche de numéros pour un même type d’informations ou de transactions de base, vous pouvez créer des liens entre ces codes. Cette fonction peut vous aider à choisir parmi ces codes lorsque vous utilisez un numéro.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Souches de n°**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne avec la souche de numéros pour laquelle vous souhaitez créer des relations, puis cliquez sur **Relations**.
3. Dans le champ **Code souche**, entrez le code de la souche de numéros à lier à la souche sélectionnée à l’étape 2.
4. Ajoutez une ligne pour chaque code à lier à la souche de numéros sélectionnée.
5. Fermez la page.

Désormais, pour créer un élément nécessitant un numéro, vous pourrez utiliser les liens ainsi créés et choisir parmi les souches de numéros liées.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
