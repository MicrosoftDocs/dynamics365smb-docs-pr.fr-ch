---
title: Accès à Business Central avec les licences Microsoft 365
description: 'Découvrez comment les utilisateurs peuvent accéder aux données de Business Central, par exemple dans les discussions instantanées et canaux Microsoft Teams, avec seulement une licence Microsoft 365, mais pas de licence Business Central.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="business-central-access-with-microsoft-365-licenses"></a><a name="business-central-access-with-microsoft-365-licenses"></a>Accès à Business Central avec les licences Microsoft 365

Les utilisateurs de [!INCLUDE[prod_short](includes/prod_short.md)] se voient attribuer une licence Dynamics 365 Business Central qui leur permet de visualiser, de modifier et d’agir sur leurs données métier à partir de n’importe quelle interface utilisateur. Pour tous les autres employés de l’organisation qui n’ont besoin d’afficher des données qu’occasionnellement, Business Central offre un accès via Microsoft 365.  

Quand une organisation a à la fois un abonnement à Dynamics 365 Business Central et à Microsoft 365, les administrateurs peuvent configurer des environnements pour permettre l’accès avec des licences Microsoft 365, et choisir exactement à quelles tables et autres objets cette catégorie d’utilisateurs aura accès. Quand ils sont configurés, les employés qui ont une licence Microsoft 365, mais aucune licence [!INCLUDE [prod_short](includes/prod_short.md)] ne peuvent afficher les enregistrements [!INCLUDE [prod_short](includes/prod_short.md)] qui sont partagés avec eux dans les discussions instantanées et canaux Microsoft Teams.

## <a name="why-enable-access-with-microsoft-365-licenses"></a><a name="why-enable-access-with-microsoft-365-licenses"></a>Pourquoi accorder l’accès avec les licences Microsoft 365

- Déverrouillez les données de base auxquelles chaque employé de l’organisation devrait avoir accès.

- Donnez aux services qui ne fonctionnent pas sur [!INCLUDE [prod_short](includes/prod_short.md)] les moyens de se servir en accédant aux données clés nécessaires pour effectuer leurs tâches avec succès, éliminant ainsi le besoin de demander continuellement des données à d’autres.

- Améliorez l’efficacité de la collaboration afin que les tâches et les projets qui s’étendent sur plusieurs services se terminent à temps, en éliminant les frictions généralement associées aux erreurs d’accès refusé en raison des licences.

- Augmentez les performances de l’équipe afin que les gens puissent prendre des décisions basées sur les données qui incluent tous les membres du groupe, même s’ils ne travaillent pas dans [!INCLUDE [prod_short](includes/prod_short.md)].

- Atteindre les objectifs budgétaires de licences, en attribuant des licences qui correspondent progressivement aux besoins des employés, avec des licences Microsoft 365 d’accès en lecture seule, des licences Dynamics 365 Business Central Team Member pour un accès en écriture limité, et Dynamics 365 Business Central Essentials ou Premium pour un accès complet en écriture.

- Améliorez la sécurité des données en réduisant le besoin de coller des extraits d’écran des données d’entreprise en dehors des limites de la gouvernance des données.

## <a name="use-rights"></a><a name="use-rights"></a>Droits d’utilisation

Quand une personne accède à [!INCLUDE [prod_short](includes/prod_short.md)] avec une licence Microsoft 365, la licence permet à l’utilisateur de lire (mais pas d’écrire) les données [!INCLUDE [prod_short](includes/prod_short.md)] via une interface utilisateur simplifiée dans Microsoft Teams. Cette section explique ces droits d’utilisation et ces limitations qui vous aident à planifier la configuration et à tirer le meilleur parti de cette fonctionnalité. Pour plus d’informations sur ce type de licence par rapport aux autres licences [!INCLUDE [prod_short](includes/prod_short.md)], consultez le [Guide des licences Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access"></a><a name="client-access"></a>Accès client

Les utilisateurs ont le droit d’accéder aux données de [!INCLUDE [prod_short](includes/prod_short.md)] dans Microsoft Teams. Le tableau suivant récapitule les différentes méthodes d’accès au service [!INCLUDE [prod_short](includes/prod_short.md)] autorisées avec cette licence.

|Client accédant au service Business Central |Accès|
|-|-|
|Application Business Central pour Microsoft Teams|![Oui](media/check.png)|
|Client web Business Central |![Non](media/x-icon.png ) |
|Applications mobiles Business Central|![Non](media/x-icon.png )|
|API Business Central|![Non](media/x-icon.png )|
|Intégrations de Business Central avec d’autres applications Office|![Non](media/x-icon.png )|
|Business Central intégré dans toutes les autres applications |![Non](media/x-icon.png )|

### <a name="data-access"></a><a name="data-access"></a>Accédez aux données

Les utilisateurs ont le droit de lire les données de la table mais ne peuvent pas modifier, créer ou supprimer des enregistrements. La plate-forme [!INCLUDE [prod_short](includes/prod_short.md)] empêche automatiquement l’écriture dans les tables de données.  

### <a name="use-of-objects"></a><a name="use-of-objects"></a>Utilisation des objets

L’accès avec des licences Microsoft 365 ne limitent pas les objets ou les plages d’objets Business Central accessibles. Les utilisateurs ont le droit d’accéder à l’application de base Microsoft et à toutes les extensions telles que les personnalisations et les applications complémentaires.

## <a name="simplified-user-interface"></a><a name="simplified-user-interface"></a>Interface utilisateur simplifiée

Les utilisateurs ont droit à un ensemble réduit de fonctionnalités et de fonctions fournies par [!INCLUDE [prod_short](includes/prod_short.md)] dans Microsoft Teams. Les tableaux ci-dessous indiquent les caractéristiques remarquables. Cette liste n’est pas exhaustive et est susceptible d’évoluer.

Fonctionnalités de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams :

|Fonctionnalité  |Disponible|
|-|-|
|Afficher les fiches [!INCLUDE [prod_short](includes/prod_short.md)]|![Oui](media/check.png)|
|Afficher les détails de la fiche |![Oui](media/check.png) |
|Épingler les détails de la carte sous forme d’onglet |![Oui](media/check.png)|
|Afficher les onglets [!INCLUDE [prod_short](includes/prod_short.md)]|![Oui](media/check.png)|
|Ajouter un onglet [!INCLUDE [prod_short](includes/prod_short.md)]|![Non_](media/x-icon.png )|
|Rechercher des contacts professionnels |![N°](media/x-icon.png )|
|Coller et partager un aperçu de lien sous forme de carte|![N°](media/x-icon.png )|

Fonctions du client [!INCLUDE [prod_short](includes/prod_short.md)] intégré dans Teams :

|Fonction |Disponible|Exemples de fonctions|
|-|-|-|
|Actions du système de manipulation de données |![Non](media/x-icon.png )|Modifier, Créer, Supprimer|
|Fonctions de base dans les listes|![Oui](media/check.png)|Rechercher, trier, modifier la disposition|
|Fonctions avancées dans les listes|![Non](media/x-icon.png )|Volet Filtre, vues|
|Explorer de la liste à la carte |![Oui](media/check.png)||
|Accéder aux données des tables associées|![Non](media/x-icon.png )|Volet Récapitulatif, exploration de champ, coup d’œil, recherche |
|Actions|![Non](media/x-icon.png )|Barre d’action, menus d’action, actions de notification de page|
|Raccourcis à l’échelle du système|![Non](media/x-icon.png )|Mes paramètres, Explorateur de rôles, Recherche Tell Me  |
|Copie|![Oui](media/check.png)|Copier les lignes, copier la valeur du champ, copier le lien vers la page|
|Personnalisation de l’interface utilisateur|![Non](media/x-icon.png )|Personnaliser| 
|Personnalisation en ligne|![Oui](media/check.png)|Redimensionner la colonne, Développer/Réduire, Afficher plus |
|Partage de données |![Non](media/x-icon.png )|Ouvrir ou modifier dans Excel, partager avec Teams|
|Assistance utilisateur en ligne|![Oui](media/check.png) |Info-bulles, liens vers la documentation|
|Assistance utilisateur avancée |![Non](media/x-icon.png )|Conseils pédagogiques sur les pages et les champs, volet d’aide|

## <a name="minimum-requirements"></a><a name="minimum-requirements"></a>Configuration minimale requise

Cette section décrit les conditions requises minimales qui doivent être remplies pour que votre organisation active l’accès avec des licences Microsoft 365, et pour les utilisateurs Microsoft Teams particuliers accèdent aux données de [!INCLUDE [prod_short](includes/prod_short.md)] sans licence [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="requirements-to-enable-access"></a><a name="requirements-to-enable-access"></a>Conditions requises pour activer l’accès

- [!INCLUDE [prod_short](includes/prod_short.md)] en ligne (SaaS).

- Les environnements doivent avoir une plate-forme de version 21.1 ou ultérieure.

### <a name="requirements-for-individual-users-to-access-data-in-teams"></a><a name="requirements-for-individual-users-to-access-data-in-teams"></a>Conditions requises pour que les utilisateurs individuels accèdent aux données dans Teams

- Les données doivent être accessibles à l’aide de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams. Les utilisateurs doivent avoir installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams et doivent utiliser l’un des clients Teams pris en charge. Pour consulter la liste des clients Teams pris en charge par [!INCLUDE [prod_short](includes/prod_short.md)], voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#teams).

- Les utilisateurs doivent être internes à l’organisation, ce qui signifie qu’une identité d’utilisateur provient du même locataire principal où [!INCLUDE [prod_short](includes/prod_short.md)] est déployé et où l’accès est activé. Les identités externes ne sont pas prises en charge. [!INCLUDE [prod_short](includes/prod_short.md)] empêche automatiquement l’accès aux invités.

- Les utilisateurs doivent se voir attribuer une licence Microsoft 365 de l’un des plans suivants.
  
  |Plan pris en charge|ID de produit |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Azure AD Identity) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  La plupart des offres basées sur ces plans sont également prises en charge. Par exemple, si vous souscrivez à Microsoft 365 Business Premium (Tarifs pour les membres des associations), il s’agit d’une offre spécifique pour les organisations à but non lucratif basée sur le plan Microsoft 365 Business Premium, et est donc prise en charge.

  > [!NOTE]
  > Vous ne trouvez pas votre plan dans la liste ? Microsoft recherche en permanence des commentaires sur la manière dont nous pouvons améliorer notre service et étendre notre offre afin que davantage de clients puissent profiter de cette fonctionnalité. Partagez votre idée des plans que nous devrions prendre en charge ensuite à [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Les utilisateurs doivent se voir affecter une licence Microsoft 365 qui a l’application Microsoft Teams activée dans la liste des applications pour cette licence.

  |Applications prises en charge|ID du plan de service|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- L’organisation doit avoir au moins un autre utilisateur auquel une licence Dynamics 365 Business Central est affectée.

## <a name="next-steps"></a><a name="next-steps"></a>Étapes suivantes

- Obtenez une compréhension du flux d’accès des utilisateurs pour vous aider à planifier votre approche et la configuration de Business Central en fonction des besoins de l’entreprise. Voir [Flux d’accès utilisateur](admin-access-with-m365-license-flow.md).
- Configurez votre environnement et vos utilisateurs pour y accéder avec des licences Microsoft 365. Voir [Configuration de l’accès avec les licences Microsoft 365](admin-access-with-m365-license-setup.md).

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
