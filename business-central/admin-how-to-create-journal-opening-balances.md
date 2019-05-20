---
title: Procédure de création des soldes ouverts feuille | Microsoft Docs
description: Business Central inclut plusieurs traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée. Vous pouvez facilement transférer ces données avec des validations de feuille.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 535a899ed43e2d7112699fff9aa3ebc6f4289292
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246753"
---
# <a name="create-journal-opening-balances"></a>Créer des soldes ouverts feuille
[!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée. Vous pouvez facilement transférer ces données avec le journal comptes clients, le journal comptes fournisseurs, la feuille article ou la feuille comptabilisation.

La première étape consiste à créer un package configuration incluant les tables de paramétrage pour ces feuilles. La procédure suivante est basée sur l’hypothèse que cette étape est terminée. Pour plus d'informations, voir [Configurer une société](admin-set-up-company-configuration.md). Cette procédure explique les étapes suivantes, comme le lettrage du package qui est fourni par un partenaire.  

Avant de commencer, vérifiez que vous vous trouvez sur la page du tableau de bord Responsable de l'implémentation de RapidStart Services, car elle fournit le contexte correct pour votre travail de configuration. Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Pour lettrer des écritures dans une feuille à une société  
1. Configurez une nouvelle société et appliquez-lui un package configuration. Pour plus d'informations, voir [Configurer une société avec l’assistant RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    La nouvelle société ne contient pas d’informations sur les soldes ouverts feuille.  

2. Ouvrez la feuille configuration et importez les données existantes à propos des clients, des articles, des fournisseurs et de la comptabilité. Pour plus d'informations, voir [Migrer des données client](admin-migrate-customer-data.md).  
3. Choisissez, par exemple, l'action **Créer lignes feuille compta**.  
4. Renseignez le raccourci **Options** de la manière appropriée, puis définissez les filtres selon vos besoins. Par exemple, dans le champ **Modèle feuille**, entrez un nom.  
5. Cliquez sur le bouton **OK**. Les enregistrements se trouvent maintenant dans la feuille, mais les montants sont vides.  
6. Exportez la table feuille vers Excel et entrez manuellement les informations sur le compte contrepartie et validation à partir des données héritées.
7. Importez et appliquez les informations de table dans la nouvelle société. Les lignes feuille sont prêtes pour la validation.  
8. Dans la feuille configuration, sélectionnez la table ligne feuille, puis sélectionnez l'action **Données de base de données**.  
9. Examinez les informations, puis sélectionnez l'action **Valider**.  
10. Répétez les étapes pour importer et valider les autres soldes ouverts.  

## <a name="see-also"></a>Voir aussi  
[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
