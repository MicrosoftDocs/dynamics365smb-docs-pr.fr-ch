---
title: Paramétrer des feuilles de temps et leur approbation
description: 'Vous paramétrez des feuilles de temps pour suivre le temps consacré aux tâches et aux projets, ce qui vous aide à gérer des projets, à recruter du personnel et à anticiper vos capacités'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Paramétrer des feuilles de temps

Dans [!INCLUDE[prod_short](includes/prod_short.md)], les feuilles de temps gèrent l’enregistrement des heures sur une base hebdomadaire par incrément de sept jours. Elles permettent de suivre le temps consacré à des projets, et vous pouvez les utiliser pour enregistrer les heures ressource. Avant de pouvoir utiliser les feuilles de temps, vous devez spécifier quels utilisateurs en soumettront et comment vous souhaitez les configurer.  

> [!TIP]
> Les personnes qui utilisent des feuilles de temps sont des *ressources*. Par exemple, vous pouvez utiliser des feuilles de temps pour suivre le travail des personnes qui ne font pas partie des employés. Pour suivre le travail des employés ou pour utiliser des feuilles de temps pour suivre l’indisponibilité des employés, vous devez associer des employés à des ressources. Un guide de configuration assistée peut vous aider à le faire. Pour en savoir plus sur le guide, consultez [Paramétrer des feuilles de temps avec le guide de configuration assistée](#set-up-time-sheets-with-the-assisted-setup-guide).  

Si vous le souhaitez, spécifiez si et comment les feuilles de temps sont approuvées. Selon les besoins de votre organisation, vous pouvez désigner :

* un ou plusieurs utilisateurs en tant qu’administrateur et approbateur de feuille de temps pour toutes les feuilles de temps ;
* un approbateur de feuille de temps pour chaque ressource.

Lorsque vous créez des feuilles de temps, vous pouvez en créer pour les ressources, et les ressources peuvent valider les lignes de feuille de temps. Pour pouvez affecter des feuilles de temps à des lignes planning projet. Pour en savoir plus, consultez [Utiliser les feuilles de temps](projects-how-use-time-sheets.md).  

## Paramétrer des feuilles de temps avec le guide de configuration assistée

Un guide de configuration assistée peut vous aider à configurer des feuilles de temps.  

> [!TIP]
> Si vous utilisez une version antérieure à la 1ère vague de lancement 2023 (v22), vous devez activer la fonctionnalité **Mise à jour des fonctionnalités : nouvelle expérience de feuille de temps** dans la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610) pour utiliser cette fonctionnalité.
>
> Ce paramètre vous permet également d’utiliser des feuilles de temps sur des appareils mobiles.

Ouvrez le guide de configuration assistée **Paramétrer des feuilles de temps** sur la page [Configuration assistée](https://businesscentral.dynamics.com/?page=1801).

Le guide de configuration assistée vous guide à travers les étapes suivantes :

1. Configurer les participants aux processus de feuille de temps.

    La première page du guide vous indique le nombre d’utilisateurs de votre [!INCLUDE [prod_short](includes/prod_short.md)]. Elle indique également d’autres informations obligatoires et facultatives.  
2. Spécifier le premier jour d’une semaine de travail dans cette organisation.

    Le premier jour d’une semaine de travail sera le premier jour par défaut pour toutes les feuilles de temps.
3. Spécifier la personne qui administre les feuilles de temps.

    Cette personne peut modifier et supprimer toutes les feuilles de temps. Vous pouvez éventuellement ajouter le même rôle à d’autres personnes dans la page **Paramètres utilisateur**.
4. Configurer les ressources qui utiliseront les feuilles de temps et les personnes qui approuveront les feuilles de temps.

À la fin de la configuration guidée, vous pouvez choisir de laisser [!INCLUDE [prod_short](includes/prod_short.md)] créer des feuilles de temps en fonction de votre configuration. Consultez les nouvelles feuilles de temps sur la page **Feuilles de temps** que vous pouvez ouvrir [ici](https://businesscentral.dynamics.com/?page=951). Vous pouvez également exécuter à nouveau le guide de configuration assistée ou terminer la configuration manuellement.

> [!IMPORTANT]
> Si vous utilisez la 1ère vague de lancement 2023 (v22) ou une version ultérieure, pour garantir que vous pouvez gérer les feuilles de temps sur les appareils mobiles, vous devez activer manuellement l’option **Utiliser la nouvelle expérience de feuille de temps** pour la configuration de la feuille de temps, comme décrit dans la procédure suivante.

## Paramétrer des feuilles de temps manuellement

Les sections suivantes décrivent comment configurer des feuilles de temps si vous n’utilisez pas le guide de configuration assistée **Paramétrer des feuilles de temps**.  

### Pour configurer manuellement des informations générales pour les feuilles de temps

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration des ressources.**, puis choisissez le lien associé.  
1. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Si vous utilisez la 1ère vague de lancement 2023 (v22) ou une version ultérieure, pour garantir que vous pouvez gérer les feuilles de temps sur les appareils mobiles, activez l’option **Utiliser la nouvelle expérience de feuille de temps**.
1. Sélectionnez l’une des options suivantes pour le champ **Feuille de temps par approbation de projet**.

| Option | Désignation |
| --- | --- |
| **Jamais** |L’utilisateur du champ **ID utilisateur de l’approbateur de la feuille de temps** de la fiche ressource approuve la feuille de temps. |
| **Toujours** |L’utilisateur du champ **Responsable** de la fiche projet approuve la feuille de temps. |
| **Poste uniquement** |Si la feuille de temps poste est liée à un projet, alors l’utilisateur du champ **Responsable** spécifié sur la fiche projet approuve la feuille de temps. Si la feuille de temps poste est liée à une ressource, alors l’utilisateur du champ **ID utilisateur de l’approbateur de la feuille de temps** spécifié sur la fiche ressource approuve la feuille de temps. |

### Pour affecter manuellement un administrateur de feuille de temps

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Paramètres utilisateur**, puis choisissez le lien associé.  
3. Sélectionnez l’utilisateur qui deviendra l’administrateur de feuille de temps, puis sélectionnez la case à cocher **Admin. feuille de temps**.  

> [!TIP]  
> Nous vous recommandons de ne désigner qu’un seul utilisateur comme administrateur de feuille de temps dans une société. Dans la procédure suivante, vous devez configurer un propriétaire et un approbateur de feuille de temps et affecter l’approbateur à chaque ressource.  

### Pour affecter manuellement un propriétaire et un approbateur de feuille de temps

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.
2. Sélectionnez la ressource pour laquelle vous souhaitez configurer la possibilité d’utiliser des feuilles de temps, puis sélectionnez la case à cocher **Utiliser la feuille de temps**.  
3. Entrez l’ID du propriétaire de la feuille de temps dans le champ **ID utilisateur du propriétaire de la feuille de temps**. Le propriétaire peut entrer le temps d’utilisation dans une feuille de temps et la soumettre pour approbation. En règle générale, lorsque la ressource est une personne, cette personne est également le propriétaire.  
4. Entrez l’ID de l’approbateur de la feuille de temps dans le champ **ID utilisateur de l’approbateur de la feuille de temps**. L’approbateur peut approuver, rejeter ou rouvrir une feuille de temps.  

> [!NOTE]  
> Vous ne pouvez pas modifier l’ID de l’approbateur de feuille de temps s’il existe des feuilles de temps qui n’ont pas été traitées et dont le statut est **Soumis** ou **En cours**.

## Voir aussi

[Utiliser des feuilles de temps pour des projets](projects-how-use-time-sheets.md)  
[Procédure : créer des feuilles de temps](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Enregistrer la consommation ou l′utilisation pour les projets](projects-how-record-job-usage.md)  
[Configuration de la gestion de projets](projects-setup-projects.md)  
[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
