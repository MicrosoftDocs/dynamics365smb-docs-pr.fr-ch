---
title: Réponse aux demandes relatives aux données personnelles de l’utilisateur
description: Cet article explique comment répondre aux demandes concernant les données personnelles.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="responding-to-requests-about-users-personal-data"></a>Réponse aux demandes relatives aux données personnelles de l’utilisateur

Les personnes concernées peuvent demander plusieurs types d’actions concernant leurs données personnelles. Par exemple, dans le cadre de certaines lois et réglementations sur la confidentialité, elles ont le droit de demander l’exportation, la suppression et la modification de leurs données personnelles. Ces demandes sont appelées *Demandes de la personne concernée*. Si vous avez classé la confidentialité de vos données et vous êtes sûr qu’elles sont correctes, un administrateur peut répondre aux demandes en utilisant les options de l’onglet **Confidentialité des données** dans le tableau de bord **Responsable informatique**. 
<!--
For more information about classifying data and data sensitivity in [!INCLUDE[prod_long](includes/prod_long.md)], go to the following articles:

* [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->

## <a name="types-of-requests"></a>Types de demandes

Le tableau suivant donne des exemples des types de demandes auxquelles les administrateurs pouvez répondre.

> [!Note]
> Nous fournissons des fonctionnalités pour répondre à ces types de demande et permettre l’accès aux données personnelles, mais il vous incombe de veiller à ce que vos données personnelles et sensibles soient stockées et classées de manière appropriée.

|Type requête|Description et réponse suggérée|
|-----|-----|
|Demandes de portabilité|Une personne concernée peut faire une demande de portabilité des données. Vous devez exporter les données personnelles de la personne concernée à partir de vos systèmes et les fournir dans un format couramment utilisé et structuré. Pour répondre à ces demandes, vous pouvez utiliser l’**Utilitaire de confidentialité des données** pour exporter les données personnelles vers un fichier Excel ou un package de configuration RapidStart. À l’aide d’Excel, vous pouvez modifier les données personnelles et les enregistrer dans un format couramment utilisé et lisible par machine, par exemple .csv ou .xml. Pour les packages de configuration RapidStart, vous pouvez configurer les tables de données principales et leurs tables associées contenant des données personnelles. <br><br> **Remarque :** lorsque vous exportez des données, vous spécifiez un niveau de confidentialité minimal. L’exportation inclut le niveau de confidentialité minimal et tous les niveaux de confidentialité au-dessus de celui-ci. Par exemple, si vous exportez des données classées comme personnelles, l’exportation inclut également les données classées comme sensibles. <br><br>Lors de l’exportation des données associées à une personne concernée, l’**Utilitaire de confidentialité des données** recherche des relations directes entre la personne concernée et les données qui lui sont associées. Les relations indirectes entre les données associées à la personne concernée et les autres données ne sont pas exportées automatiquement par l’**Utilitaire de confidentialité des données**. Par exemple, la table Contact a directement associé les données Réponses profil contact, et la table Réponses profil contact est ensuite associée aux données Questions profil. Si vous souhaitez exporter également les questions de profil, vous devez ajouter manuellement cette table en tant que ligne avec les filtres appropriés dans le package de configuration créé par l’**Utilitaire de confidentialité des données**.|
|Demandes de suppression|Une personne concernée peut demander la suppression de ses données personnelles. Il existe plusieurs méthodes de suppression des données personnelles à l’aide des fonctions de personnalisation, mais la décision et l’implémentation vous incombent. Dans certains cas, vous pouvez choisir de modifier directement vos données. Par exemple, supprimez un contact, puis exécutez le traitement par lots Supprimer l’interaction annulée pour supprimer les interactions du contact. <br><br> **Remarque :** si vous avez spécifié une date dans le champ **Autoriser suppr. doc. av.** des pages **Paramètres ventes** ou **Paramètres achats**, vous devrez peut-être modifier la date afin de pouvoir supprimer les documents vente et achat validés dont les dates de validation sont au plus tard à cette date.|
|Demandes de correction|Une personne concernée peut demander la correction des données personnelles incorrectes. Plusieurs méthodes sont possibles. Dans certains cas, vous pouvez exporter des listes vers Excel afin de modifier en bloc plusieurs enregistrements et importer les données mises à jour. Pour plus d’informations, voir [Exportation de vos données métier vers Excel](about-export-data.md). Vous pouvez également modifier manuellement les champs contenant des données personnelles, par exemple modifier les informations sur un client dans la fiche Client. Cependant, les enregistrements tels que les écritures générales, de clients et fiscales sont importantes. Si vous stockez des données personnelles dans les enregistrements de transaction, pensez à utiliser les fonctions de personnalisation pour modifier ces données personnelles.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Restreindre le traitement des données pour une personne concernée

Une personne concernée peut demander l’arrêt temporaire du traitement de ses données personnelles. Pour honorer ces demandes, vous pouvez marquer son enregistrement comme bloqué pour des raisons de confidentialité afin d’arrêter le traitement de ses données. Lorsqu’un enregistrement est marqué comme bloqué, vous ne pouvez pas créer des transactions qui utilisent cet enregistrement. Par exemple, vous ne pouvez pas créer une facture pour un client lorsque le client ou le vendeur est bloqué. Pour marquer une personne concernée comme bloquée, ouvrez la fiche correspondante, par exemple les fiches Client, Fournisseur ou Contact, puis activez la case à cocher **Confidentialité bloquée**. Vous devez peut-être choisir **Afficher plus** pour afficher le champ.  

## <a name="handling-data-subject-requests-when-using-a-trial-version"></a>Gestion des demandes de la personne concernée lors de l’utilisation d’une version d’essai

Certains types de données personnelles font partie d’un compte Microsoft 365, et seuls les administrateurs peuvent exporter les données. Le processus de gestion des demandes de la personne concernée diffère selon le type d’abonné [!INCLUDE[prod_short](includes/prod_short.md)].

Si vous disposez d’un abonnement payant pour [!INCLUDE[prod_short](includes/prod_short.md)], les utilisateurs doivent contacter l’administrateur abonné de leur organisation pour créer une demande de la personne concernée. Les administrateurs disposent des droits et outils d’administration pour traiter les demandes de la personne concernée.

Si vous vous êtes inscrit à [!INCLUDE[prod_short](includes/prod_short.md)] à partir de la page [Essais](https://trials.dynamics.com/) et que vous utilisez toujours la version d’essai, les utilisateurs peuvent télécharger et exporter leurs propres données dans la page [Confidentialité au travail et à l’école dans le portail Azure](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Sur la page Confidentialité au travail et à l’école, vous pouvez également fermer votre compte. Cependant, nous vous recommandons d’exporter et de supprimer d’abord toutes les données. La suppression de votre compte signifie que vous perdez l’accès à [!INCLUDE[prod_short](includes/prod_short.md)].

Vous pouvez toujours marquer des personnes comme bloquées pour des raisons de confidentialité et exporter, modifier ou supprimer des transactions, comme expliqué ailleurs dans cet article.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Exportation de données à partir de tables non classées par la personne concernée

Si vous devez exporter des données non classées de manière à pouvoir les exporter automatiquement, par exemple les données de la table Réponses profil, vous devez effectuer les actions suivantes :

* Déterminez si vous devez vraiment exporter des données supplémentaires qui ne sont pas directement liées au contact.
* Ajoutez manuellement la table et la relation au package Rapid Start et exportez-les directement à partir du package Rapid Start. Nous générons un package Rapid Start pour vous, afin que vous puissiez le modifier dans de telles situations.

## <a name="handling-data-about-minors"></a>Gestion des données concernant les mineurs

Si l’âge d’un contact est inférieur à l’âge de consentement légal défini par les lois de votre région, vous pouvez l’indiquer en activant la case à cocher **Mineur** sur la fiche **Contact**. La case à cocher **Confidentialité bloquée** est alors automatiquement activée. Lorsque vous recevez l’accord du parent ou du tuteur légal du mineur, vous pouvez activer la case à cocher **Accord parental reçu** pour débloquer le contact. Même si vous pouvez traiter les données personnelles des mineurs, vous ne pouvez pas utiliser la fonctionnalité de profilage dans Dynamics 365 Sales.

> [!Note]
> Le journal des modifications peut enregistrer des détails, par exemple quand et par qui la case à cocher **Accord parental reçu** a été activée. Un administrateur peut le configurer en utilisant le guide **Paramètres journal modification** et en activant la case à cocher **Modification du journal pour l’accord parental reçu** sur la fiche **Contact**. Pour plus d’informations, voir [Journalisation des modifications](across-log-changes.md).  

### <a name="see-also"></a>Voir aussi

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Exportation de vos données métier vers Excel](about-export-data.md)  
[Journalisation des modifications](across-log-changes.md)  
[Demandes de la personne concernée](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
