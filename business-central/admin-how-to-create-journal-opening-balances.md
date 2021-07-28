---
title: 'Procédure : créer des soldes ouverts feuille'
description: Les traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée. Vous pouvez facilement transférer ces données avec des validations de feuille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: ac7fea479237d985204820d54953689566f5c2ac
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/30/2021
ms.locfileid: "6319553"
---
# <a name="create-journal-opening-balances"></a>Créer des soldes ouverts feuille

[!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée. Vous pouvez facilement transférer ces données avec le journal comptes clients, le journal comptes fournisseurs, la feuille article ou la feuille comptabilisation.

La première étape consiste à créer un package configuration incluant les tables de paramétrage pour ces feuilles. La procédure suivante est basée sur l’hypothèse que cette étape est terminée. Pour plus d’informations, voir [Configurer une société](admin-set-up-company-configuration.md). Cette procédure explique les étapes suivantes, comme le lettrage du package qui est fourni par un partenaire.  

Avant de commencer, vérifiez que vous utilisez la page Tableau de bord Administration, car elle fournit le contexte correct pour votre travail de configuration. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Pour lettrer des écritures dans une feuille à une société

1. Configurez une nouvelle société et appliquez-lui un package configuration. Pour plus d’informations, voir [Configurer une société avec l’assistant RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    La nouvelle société ne contient pas d’informations sur les soldes ouverts feuille.  

2. Ouvrez la feuille configuration et importez les données existantes à propos des clients, des articles, des fournisseurs et de la comptabilité. Pour plus d’informations, voir [Migrer des données client](admin-migrate-customer-data.md).  

    Les données de base sont maintenant en place. Ensuite, vous ajoutez les soldes d’ouverture. Les étapes suivantes décrivent comment créer des lignes feuille pour les comptes généraux, mais la même procédure s’applique à la création de lignes feuille pour les clients, les fournisseurs et les articles.  
3. Choisissez l’action **Créer lignes feuille compte général**.  
4. Renseignez le raccourci **Options** de la manière appropriée, puis définissez les filtres selon vos besoins. Par exemple, dans le champ **Modèle feuille**, entrez un nom.  
5. Cliquez sur le bouton **OK**. Les enregistrements se trouvent maintenant dans la feuille, mais les montants sont vides.  
6. Exportez la table feuille vers Excel et entrez manuellement les informations sur le compte contrepartie et validation à partir des données héritées.
7. Importez et appliquez les informations de table dans la nouvelle société. Les lignes feuille sont prêtes pour la validation.  
8. Dans la feuille configuration, sélectionnez la table ligne feuille, puis sélectionnez l’action **Données de base de données**.  
9. Examinez les informations, puis sélectionnez l’action **Valider**.  
10. Répétez les étapes pour importer et valider les autres soldes ouverts.  

> [!TIP]
> Vous pouvez utiliser les mêmes traitements par lots pour ajouter des soldes d’ouverture chaque fois que vous enregistrez un nouveau client ou fournisseur avec lequel vous avez déjà traité mais qui n’est pas enregistré dans [!INCLUDE [prod_short](includes/prod_short.md)]. Recherchez simplement la tâche appropriée, puis choisissez le lien approprié.

## <a name="see-also"></a>Voir aussi

[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]