---
title: "Procédure : utilisation des codes IGRF au Canada | Microsoft Docs"
description: En savoir plus sur les codes IGRF
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/23/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 03316fe6ad7a63c79a88f540a9c49f61450922f4
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Procédure : utilisation des codes IGRF au Canada
Les informations fiscales peuvent inclure des comptes généraux, des états, des comptes de gestion, des bilans et des relevés des bénéfices non répartis. Les informations fiscales sont classifiées par le biais de codes. L'utilisation de codes aide le gouvernemental à traiter les informations, à préparer l'archivage électronique et à valider les informations fiscales par voie électronique. L'utilisation de codes aide également les organisations statistiques à travailler plus efficacement, en rendant les données financières plus facilement disponibles. Pour plus d'informations, reportez-vous au [site Web de l'Agence de revenu du Canada](http://www.cra-arc.gc.ca/).

L'Agence de revenu du Canada utilise les codes IGRF (Index général des renseignements financiers) pour recueillir, valider et traiter les informations financières et fiscales par voie électronique. Les meilleures pratiques suggèrent d'attribuer des codes IGRF uniquement aux comptes de validation, afin que tous les totaux soient calculés par votre logiciel d'établissement des déclarations fiscales.

Lorsqu'un compte est associé à un code IGRF, il est enregistré auprès de l'Agence de revenus sous ce code. Plusieurs comptes peuvent avoir le même code IGRF, mais chaque compte doit avoir un seul code IGRF.

Vous pouvez exporter les informations de solde par code IGRF et enregistrer le fichier exporté dans Excel, ce qui est utile pour transférer des informations vers votre logiciel d'établissement des déclarations fiscales.

## <a name="to-set-up-gifi-codes"></a>Pour configurer des codes IGRF
Dans Dynamics NAV, vous devez configurer des codes IGRF pour les comptes généraux, les états, les comptes de gestion, les comptes de résultat et les relevés de bénéfices non répartis.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Codes IGRF**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Codes IGRF**, sélectionnez l'action **Nouveau**.
3. Configurer les codes IGRF en renseignant les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Pour associer des codes IGRF avec des comptes généraux
Pour enregistrer des données financières par code IGRF, chaque code IGRF doit être associé aux comptes appropriés dans le plan comptable.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien associé.
2. Sélectionnez un compte général approprié, puis sélectionnez l'action **Modifier**.
3. Sur le raccourci **Comptabilité analytique**, dans le champ **Code IGRF**, sélectionnez un code IGRF approprié.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Pour afficher les soldes de compte à l'aide de l'état de code IGRF
Vous pouvez consulter vos soldes de compte par code IGRF par le biais de l'état **Soldes de compte par code IGRF**.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Soldes de compte par code IGRF**, puis sélectionnez le lien associé.
2. Spécifiez les éléments à inclure dans l'état en renseignant les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Pour exporter les informations de solde à l'aide de codes IGRF
Vous pouvez exporter les informations de solde à l'aide de codes IGRF et enregistrer le fichier exporté dans Excel. Vous pouvez modifier, enregistrer ou supprimer, le fichier. Ce fichier vous permet de transférer des informations vers votre logiciel d'établissement des déclarations fiscales.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Exporter les info IGRF dans Excel**, puis sélectionnez le lien associé.
2. Spécifiez les éléments à exporter vers Excel en renseignant les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Cliquez sur le bouton **OK**.

**Remarque :** le fichier Excel est doté des caractéristiques suivantes :

* Le solde est arrondi au point de pourcentage le plus proche, mais la valeur de la cellule indique le même pourcentage que dans les écritures comptables.
* Les nombres négatifs sont représentés comme des nombres positifs entre parenthèses. Par conséquent, -123 est représenté comme suit : (123).

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)   
[Configuration de Finance](finance-setup-finance.md)

