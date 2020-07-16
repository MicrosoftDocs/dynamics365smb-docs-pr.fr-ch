---
title: Spécifier la mise en page d'un chèque| Microsoft Docs
description: Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8346e8a868f73d3de729a56e86530048c58229aa
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/17/2020
ms.locfileid: "3458948"
---
# <a name="select-a-check-layout"></a>Sélectionner une mise en page de chèque
Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales. Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.

Les chèques sont conçus pour être imprimés aux formats d'image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.

## <a name="to-select-a-check-layout"></a>Pour sélectionner une mise en page de chèque
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Sélection des états : Compte bancaire**, puis sélectionnez le lien associé.
2. Sur la page **Sélection des états : Banque**, dans le champ **Utilisation**, sélectionnez **Chèque**
3. Sélectionnez l'un des ID état suivants.

| ID état | Nom état | Description |
| --- | --- | --- |
| 1401 |Activer |Il s'agit de l'état par défaut. |
| 10411 |Chèque (Talon/Talon/Chèque) |Cet état est conçu pour imprimer des chèques au format talon/talon/chèque. |
| 10412 |Chèque (Talon/Chèque/Talon) |Cet état est conçu pour imprimer des chèques au format talon/chèque/talon. |
| 10413 |Trois chèques par page |Cet état est conçu pour imprimer trois chèques sur chaque page. |

Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la page **Feuille paiement**. Pour plus d'informations, reportez-vous à [Utilisation des chèques](payables-how-work-checks.md).

Pour modifier l'une de ces mises en page de chèque par défaut, utilisez l'intégration Word ou RDLC. Pour plus d'informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Utilisation des polices de sécurité et MICR
La version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)] contient des polices préinstallées sur les serveurs qui peuvent être utilisées lors de la définition des mises en page de chèque. Ci-après, découvrez les polices disponibles et des liens vers des informations détaillées fournies par les fournisseurs tiers de polices.

> [!Important]
> Les polices de sécurité de chèque et MICR de Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] sont concédées sous licence dans un package de polices d'IDAutomation.com, Inc. Ces produits ne peuvent être utilisés que dans le cadre et en relation avec Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dans la mise à jour 15.3 et les versions ultérieures, les polices MICR sont installées et disponibles à l'utilisation. Les normes E-13B et CMC-7 sont prises en charge. En plus des polices MICR, des polices de sécurité spéciales sont disponibles pour générer du texte, des noms, des montants et les symboles monétaires Dollar, Euro, Pound et Yen, qui sont difficiles à modifier une fois qu'un chèque a été imprimé.

> [!NOTE]
> Pour des raisons de sécurité et juridiques, vous ne pouvez pas télécharger de polices personnalisées sur l'environnement [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="micr-e-13b-specifications"></a>Spécifications MICR E-13B
Voici un résumé des spécifications des polices MICR E-13B qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.

![Spécifications MICR E-13B](media/font_MICR_E-13B_Specifications.png "Spécifications MICR E-13B")

### <a name="delimiter-characters"></a>Caractères séparateurs
![Caractères séparateurs](media/font-micr-letters.png "Caractères séparateurs")

La spécification complète des polices MICR E-13B est disponible dans la documentation du fournisseur ici : (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>Spécifications MICR CMC-7
Les polices CMC-7 suivantes sont disponibles dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en ligne :

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

Voici un résumé des spécifications des polices MICR CMC-7 qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.

![Spécifications MICR CMC-7](media/font_MICR_CMC-7_Specifications.png "Spécifications MICR CMC-7")

### <a name="delimiter-characters"></a>Caractères séparateurs
![Caractères séparateurs](media/font-cmc7-letters.png "Caractères séparateurs")

La spécification complète des polices MICR CMC-7 est disponible dans la documentation du fournisseur ici : (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Spécifications des polices sécurisées
Voici un résumé des spécifications des polices de sécurité des chèques qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.

![Spécifications des polices de sécurité des chèques](media/font_check-security-font_Specifications.png "Spécifications des polices de sécurité des chèques")

La spécification complète des polices de sécurité des chèques est disponible dans la documentation du fournisseur ici : (https://www.idautomation.com/security-fonts/).

Les polices à d'autres fins sont également disponibles dans [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d'informations, voir [Polices disponibles](ui-fonts.md)

## <a name="see-also"></a>Voir aussi
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Polices de Business Central](ui-fonts.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)   
[Exécution des processus de clôture d'exercice](year-how-complete-period-end-processes.md)  
[Utilisation de [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)
