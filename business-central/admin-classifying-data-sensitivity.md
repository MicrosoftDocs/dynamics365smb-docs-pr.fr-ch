---
title: Classification de la sensibilité des données
description: Vous devez spécifier le type de données que vous stockez sur les personnes afin de pouvoir répondre aux demandes des sujets des données.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
ms.service: dynamics-365-business-central
---

# <a name="classifying-data-sensitivity-fields"></a>Champs Classification de la sensibilité des données

Pour classer les champs contenant des données sensibles ou personnelles, un partenaire Microsoft peut définir la propriété ```DataClassification``` des champs. Cela nécessite un accès aux tables de base de données, par le biais de l’environnement de développement ou en exécutant un script Windows PowerShell. Pour plus d’informations, voir [Classification des données](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

En tant que client, vous pouvez ajouter un deuxième niveau de classification en spécifiant des niveaux de sensibilité pour les données que vous stockez dans les champs standard et personnalisés. La classification de la sensibilité des données vous permet de savoir où vous conservez vos informations personnelles dans votre système, et de répondre facilement aux demandes des sujets des données. Par exemple, si un contact ou un client vous demande d’exporter ses données personnelles. Pour plus d’informations, voir [Réponse aux demandes relatives aux données personnelles](admin-responding-to-requests-about-personal-data.md).

> [!Important]  
> Microsoft fournit cette fonction de classification de la sensibilité des données pour votre convenance uniquement. Il vous incombe de classer les données de manière appropriée et de vous conformer aux lois et réglementations qui vous concernent. Microsoft décline toute responsabilité en cas de réclamations liées à votre classification des données.  

Le tableau suivant décrit les niveaux de sensibilité des données que vous pouvez affecter.

|Sensibilité|Désignation|
|----|----|
|Sensible | Informations sur l’origine raciale ou ethnique, les opinions politiques, les croyances religieuses, l’engagement syndical, la santé physique ou mentale, la sexualité d’un sujet des données, ou encore des détails sur les infractions criminelles. |
|Personnel | Informations permettant d’identifier un sujet des données, directement ou en combinaison avec d’autres données ou informations.|
|Confidentiel | Données métier que vous utilisez à des fins comptables ou à d’autres fins commerciales et que vous ne souhaitez pas exposer à d’autres entités. Cela peut inclure, par exemple, les écritures comptables.|
|Normal | Données générales qui n’appartiennent pas aux autres catégories.|

## <a name="how-do-i-classify-my-data"></a>Comment classer mes données ?

Classer la sensibilité d’un grand nombre de champs un par un peut prendre beaucoup de temps. Pour aider à accélérer le processus, nous fournissons des outils qui permettent de classer en bloc la sensibilité des champs et d’affiner les classifications pour des champs spécifiques. Vous trouverez les outils dans la feuille Classification des données, qui est disponible dans le tableau de bord Administration des utilisateurs, des groupes d’utilisateurs et des autorisations. Vous devez être un administrateur système pour utiliser la feuille.
 
> [!Important]  
> La feuille Classification des données est vide lorsque vous l’ouvrez pour la première fois. Vous devez exécuter le guide de classification des données pour générer la liste des champs. Pour démarrer le guide, choisissez l’action **Configuration des classifications de données**.

Par exemple, la feuille Classification des données vous permet d’effectuer les opérations suivantes :  

* Utilisez le guide de classification des données pour exporter les champs vers une feuille de calcul Excel dans laquelle vous pouvez les classer en bloc. L’utilisation de la feuille Excel est particulièrement utile si vous collaborez avec un partenaire Microsoft. Après avoir mis à jour la feuille, vous pouvez utiliser le guide pour importer et appliquer les classifications. Vous pouvez également utiliser le guide pour classer manuellement les champs.  
* Choisissez un champ, puis filtrez la liste pour rechercher des champs similaires susceptibles d’appartenir à la même classification que le champ sur lequel est basée la recherche.  
* Examinez un champ en affichant son contenu.  

> [!Tip]  
> Nous avons défini des exemples de classifications de la sensibilité pour les tables et les champs de la société de démonstration Cronus. Vous pouvez vous inspirer de ces classifications lorsque vous classez vos propres tables et champs.

## <a name="see-also"></a>Voir aussi

<!-- [Classifying Data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data) -->
[!INCLUDE[footer-include](includes/footer-banner.md)]
