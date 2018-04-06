---
title: "Réponse aux demandes relatives aux données personnelles"
description: "Vous devez répondre aux demandes des sujets des données."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Réponse aux demandes relatives aux données personnelles  
Les sujets des données peuvent demander plusieurs types d'actions concernant leurs données personnelles. Si vous avez classé la sensibilité de vos données et vous êtes sûr de leur exactitude, un administrateur peut répondre aux demandes à l'aide de la feuille Classification des données dans le tableau de bord **Gérer les utilisateurs, les groupes d'utilisateurs et les autorisations** ou, si vous utilisez le client Windows, dans le tableau de bord **Responsable informatique**. Pour plus d'informations sur la classification des données et la classification de la sensibilité des données, voir [Classification des données](/dynamics-nav/classifying-data) et [Classification de la sensibilité des données](admin-classifying-data-sensitivity.md).

Le tableau suivant donne des exemples des types de demandes auxquelles vous pouvez répondre.

> [!Note]
> Nous fournissons des fonctionnalités pour répondre à ces types de demande et permettre l'accès aux données personnelles, mais il vous incombe de veiller à ce que vos données personnelles et sensibles soient stockées et classées de manière appropriée.

|Type requête|Description et réponse suggérée|
|-----|-----|
|Demandes de portabilité|Un sujet des données peut faire une demande de portabilité des données, ce qui signifie que vous devez exporter les données personnelles du sujet des données à partir de vos systèmes et les fournir dans un format couramment utilisé et structuré. Pour répondre à ces demandes, utilisez l'utilitaire de confidentialité des données pour exporter les données personnelles vers un fichier Excel. À l'aide d'Excel, vous pouvez modifier les données personnelles et les enregistrer dans un format couramment utilisé et lisible par machine, par exemple .csv ou .xml. Les administrateurs peuvent également exporter des données à l'aide des packages de configuration Rapid Start, puis configurer les tables de données principales et leurs tables associées contenant des données personnelles. |
|Demandes de suppression|Un sujet des données peut demander la suppression de ses données personnelles. Il existe plusieurs méthodes de suppression des données personnelles à l'aide des fonctions de personnalisation, mais la décision et l'implémentation vous incombent. Dans certains cas, vous pouvez choisir de modifier directement vos données, par exemple en supprimant un contact et en exécutant le traitement par lots Supprimer l'interaction annulée pour supprimer les interactions du contact. <br><br> **Remarque :** si vous avez spécifié une date dans le champ **Autoriser suppr. doc. av.** des pages **Paramètres ventes** ou **Paramètres achats**, vous devrez peut-être modifier la date afin de pouvoir supprimer les documents vente et achat validés que vous avez imprimés et dont les dates comptabilisation sont au plus tard à cette date.|
|Demandes de correction|Un sujet des données peut demander la correction des données personnelles incorrectes. Plusieurs méthodes sont possibles. Dans certains cas, vous pouvez exporter des listes vers Excel afin de modifier en bloc plusieurs enregistrements et importer les données mises à jour. Pour plus d'informations, voir [Exportation de vos données métier vers Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Vous pouvez également modifier manuellement les champs contenant des données personnelles, par exemple modifier les informations sur un client dans la fiche Client. Toutefois, les enregistrements de transaction comme les écritures comptables générales, client et de taxe sont essentiels à l'intégrité du système de planification des ressources de l'entreprise. Si vous stockez des données personnelles dans les enregistrements de transaction, pensez à utiliser les fonctions de personnalisation pour modifier ces données personnelles.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Restreindre le traitement des données pour un sujet des données
Un sujet des données peut demander l'arrêt temporaire du traitement de ses données personnelles. Pour honorer ces demandes, vous pouvez marquer son enregistrement comme bloqué pour des raisons de confidentialité afin d'arrêter le traitement de ses données. Lorsqu'un enregistrement est marqué comme bloqué, vous ne pouvez pas créer des transactions qui utilisent cet enregistrement. Par exemple, vous ne pouvez pas créer une facture pour un client lorsque le client ou le vendeur est bloqué. Pour marquer un sujet des données comme bloqué, ouvrez la fiche correspondante, par exemple les fiches Client, Fournisseur ou Contact, puis activez la case à cocher **Confidentialité bloquée**. Vous devez peut-être choisir **Afficher plus** pour afficher le champ.

## <a name="handling-data-about-minors"></a>Gestion des données concernant les mineurs
Si l'âge d'un contact est inférieur à l'âge de consentement légal défini par les lois de votre région, vous pouvez l'indiquer en activant la case à cocher **Mineur** sur la fiche **Contact**. La case à cocher **Confidentialité bloquée** est alors automatiquement activée. Lorsque vous recevez l'accord du parent ou du tuteur légal du mineur, vous pouvez activer la case à cocher **Accord parental reçu** pour débloquer le contact. Même si vous pouvez traiter les données personnelles des mineurs, vous ne pouvez pas utiliser la fonctionnalité de profilage dans Microsoft Dynamics 365 for Sales.

> [!Note]
> Le journal des modifications peut enregistrer des détails, par exemple quand et par qui la case à cocher **Accord parental reçu** a été activée. Un administrateur peut le configurer en utilisant le guide **Paramètres journal modification** et en activant la case à cocher **Modification du journal pour l'accord parental reçu** sur la fiche **Contact**. Pour plus d'informations, voir [Journalisation des modifications](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Voir aussi
[Classification des données](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Classification de la sensibilité des données](admin-classifying-data-sensitivity.md)  
[Exportation de vos données métier vers Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

