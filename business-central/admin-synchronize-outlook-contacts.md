---
title: Partager des contacts entre Business Central et Outlook
description: 'Ce service a une intégration étroite avec Microsoft 365, ce qui vous permet de partager des contacts entre Outlook et Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synchroniser les contacts de Business Central avec les contacts de Microsoft Outlook

Vous pouvez configurer la synchronisation des contacts afin que vos contacts dans [!INCLUDE[prod_short](includes/prod_short.md)] aient les mêmes informations que vos contacts dans Microsoft Outlook. Par exemple, si vous êtes un vendeur, vous pouvez travailler dans Outlook et dans [!INCLUDE[prod_short](includes/prod_short.md)] simultanément. Si les contacts sont les mêmes dans les deux emplacements, votre travail est plus simple.  

Par défaut, les contacts que vous synchronisez sont conservés dans un dossier **Business Central** dans vos favoris sur le volet des dossiers dans Outlook. Le dossier Business Central peut faciliter l’identification des contacts que vous synchronisez. Vous pouvez définir des filtres pour synchroniser uniquement des contacts spécifiques à partir de [!INCLUDE[prod_short](includes/prod_short.md)] vers Outlook. Après avoir configuré la synchronisation, vous pouvez synchroniser manuellement ou automatiser le processus pour synchroniser à des intervalles planifiés.  

## <a name="prerequisites"></a>Conditions préalables

- Votre profil utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)] doit spécifier votre compte de messagerie Microsoft 365.

  Vous pouvez vérifier ce paramètre dans la section **Authentification Microsoft 365** de votre profil utilisateur dans la liste **Utilisateurs**.
- Avec [!INCLUDE[prod_short](includes/prod_short.md)], vous avez configuré la synchronisation des contacts comme décrit dans [Configurer la synchronisation des contacts avec Outlook pour Business Central sur site](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a>Configurer la synchronisation

Vous configurez le mode de synchronisation des contacts avec Outlook sur la page **Configuration de la synchronisation Exchange** de [!INCLUDE[prod_short](includes/prod_short.md)]. 

Sur la page **Configuration de la synchronisation Exchange**, vous pouvez valider que la connexion à Exchange fonctionne avant de configurer la synchronisation des contacts. À partir de la page **Configuration de la synchronisation Exchange**, vous pouvez ouvrir la page **Paramètres synch. contacts** page et lancer la synchronisation. Vous pouvez définir un filtre pour spécifier les contacts à synchroniser. Par exemple, vous pouvez filtrer par nom, type, société, etc. Vous pouvez également modifier le nom par défaut du dossier dans Outlook avec lequel les contacts seront synchronisés.  

Chacun de vos collègues peut également configurer sa propre synchronisation Exchange et définir ses propres filtres de synchronisation des contacts.  

Après avoir configuré la synchronisation, vous pouvez synchroniser manuellement les modifications apportées au contact ou automatiser le processus en configurant une entrée de file d’attente des tâches. Pour plus d’informations sur l’automatisation, consultez la section suivante de cet article.

### <a name="automate-synchronization"></a>Automatiser la synchronisation

Vous pouvez créer une entrée de file d’attente de tâches qui synchronisera les contacts selon un calendrier que vous définissez. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md). 

Le tableau suivant répertorie les paramètres de la page **Fiche écriture file d’attente des travaux** qui servent à synchroniser les contacts :

|Champ|Paramètre de synchronisation des contacts|
|-----|-----|
|Type objet à exécuter|Codeunit|
|ID objet à exécuter|6700|

## <a name="synchronize-contacts"></a>Synchroniser les contacts

Si vous avez l’habitude d’utiliser les contacts dans [!INCLUDE[prod_short](includes/prod_short.md)], il vous sera facile de synchroniser manuellement au moment qui vous convient à partir de la liste **Contacts**. Vous pouvez synchroniser vos contacts de deux manières :

* **Synchronisation avec Microsoft 365**

  Synchroniser toutes les modifications de Microsoft 365 vers [!INCLUDE[prod_short](includes/prod_short.md)] effectuées après la dernière synchronisation, en fonction de la dernière date de modification. Les nouveaux contacts dans Microsoft 365 seront également synchronisés dans [!INCLUDE[prod_short](includes/prod_short.md)]. En règle générale, cette action est plus rapide qu’une synchronisation complète. 

* **Synchronisation complète avec Microsoft 365**

  Synchroniser tous les contacts dans les deux directions, indépendamment de la dernière date de synchronisation et de la dernière date de modification.  

Dans les deux cas, les contacts sont uniquement synchronisés à partir d’Outlook si les champs obligatoires sont renseignés. Les champs obligatoires à synchroniser avec Microsoft 365 sont **Nom**, **Adresse e-mail** et le contact doit être **Personne**. [!INCLUDE[prod_short](includes/prod_short.md)] est la source des informations de contact, les informations de contact [!INCLUDE[prod_short](includes/prod_short.md)] seront donc enregistrées en cas de doublons.  

> [!NOTE]
> Si vous supprimez un contact dans Outlook, mais que vous le conservez dans [!INCLUDE[prod_short](includes/prod_short.md)], le contact sera recréé dans Outlook lors de la synchronisation suivante. 

## <a name="see-also"></a>Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser des contacts (personnes) dans Outlook sur le Web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
