---
title: Gérer les clients utilisant Dynamics 365 for Sales | Microsoft Docs
description: Vous pouvez utiliser Dynamics 365 for Sales depuis Business Central pour mapper les données et avoir une intégration et une synchronisation parfaites dans le processus allant du prospect à l'encaissement.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 30396e25dbf251e674744d1ba797c100b5762a46
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "915205"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Utilisation de Dynamics 365 for Sales depuis Business Central
Si vous utilisez Dynamics 365 for Sales for Customer Engagement, bénéficiez de l'intégration parfaite dans le processus allant du prospect à l'encaissement à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour les activités principales, telles que le traitement des commandes, la gestion des stocks et de vos finances.

> [!NOTE]
> Cette rubrique suppose que vous utilisiez les versions en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)] et de Sales. Vous pouvez mélanger les versions en ligne et locale, mais cela nécessite une configuration spécifique. Pour plus d'informations, voir [Préparation de l'intégration à Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Intégrer les applications vous permet d'accéder aux données dans Sales depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et dans certains cas, inversement. Vous pouvez utiliser et synchroniser les types de données communs aux deux services, par exemple clients, contacts et informations de vente, et mettre à jour les données dans les deux applications.  

Par exemple, un vendeur dans Sales peut utiliser les tarifs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'il crée une commande vente. Lorsqu'il ajoute l'article à la ligne commande vente dans Sales, il peut également visualiser le niveau de stock (disponibilité) de l'article dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Inversement, les préparateurs de commandes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] peuvent gérer les commandes vente qui sont automatiquement ou manuellement transférées depuis Sales. Par exemple, ils peuvent créer et valider des lignes de commande vente pour les articles ou les ressources saisies dans Sales comme produits hors-catalogue. Pour plus d'informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] s'intègre uniquement à Dynamics 365 for Sales. Les autres applications Dynamics 365 qui modifient le flux de travail ou le modèle de données standard dans Sales, par exemple Project Service Automation, peuvent désactiver l'intégration entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.

### <a name="coupling-records"></a>Enregistrements couplage
Le guide de configuration assistée vous permet de choisir les données à synchroniser. Ultérieurement, vous pouvez également configurer la synchronisation pour les enregistrements spécifiques. C'est ce qu'on appelle le *couplage*. Par exemple, vous pouvez associer un compte spécifique dans Sales avec un client spécifique dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette rubrique décrit ce qu'il convient de prendre en compte lorsque vous couplez des enregistrements.

Par exemple, si vous souhaitez afficher les comptes dans Sales en tant que clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez coupler les deux types d'enregistrements. Pour ce faire, sur la page de la liste **Clients** dans [!INCLUDE[d365fin](includes/d365fin_md.md)], utilisez l'action **Configurer le couplage**. Puis vous devez spécifier quels clients [!INCLUDE[d365fin](includes/d365fin_md.md)] correspondent à quels comptes dans Sales.

Vous pouvez également créer (et coupler) un compte dans Sales selon, par exemple, l'enregistrement client dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un compte dans Dynamics 365 for Sales**, ou vice-versa, à l'aide de l'option **Créer un client dans [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Lorsque vous configurez un couplage entre deux enregistrements, vous pouvez également demander manuellement que l'enregistrement actuel, par exemple un client, soit remplacé immédiatement par les données de compte depuis Sales (ou depuis [!INCLUDE[d365fin](includes/d365fin_md.md)]) à l'aide de l'action **Synchroniser maintenant**. L'action**Synchroniser maintenant** vous demandera de remplacer les données dans Sales ou les données d'enregistrement [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dans certains cas, vous devez coupler certains ensembles de données avant d'autres ensembles de données, comme l'indique le tableau suivant.

|Données|Ce qu'il convient de coupler tout d'abord|
|-----|----|
|Clients et comptes|Coupler des vendeurs avec des utilisateurs Sales|
|Articles et ressources|Coupler des unités de mesure avec des groupes d'unités Sales|
|Prix des articles et des ressources|Coupler des groupes tarifs client avec des prix Sales|

> [!NOTE]  
> Si vos prix ou clients utilisent des devises étrangères, assurez-vous de coupler des devises avec des devises de transaction Sales.

Dans Sales, les commandes vente dépendent d'informations comme les clients, les unités de mesure, les devis, les groupes tarifs client, les articles et/ou les ressources. Pour assurer une intégration avec les commandes vente, vous devez coupler des clients, des unités de mesure, des devises, des groupes tarifs client, des articles et/ou des ressources.

### <a name="fully-synchronizing-records"></a>Synchronisation complète des enregistrements
À la fin du guide de configuration assistée, vous pouvez sélectionner l'action **Exécuter une synchronisation complète** pour démarrer la synchronisation de tous les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] avec tous les enregistrements associés dans Sales. Sur la page **Révision synchronisation complète Dynamics 365 for Sales**, choisissez l'action **Démarrer**. La synchronisation complète peut prendre un certain temps, mais vous pouvez continuer à travailler dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant qu'elle fonctionne à l'arrière-plan.

Pour vérifier la progression de divers projets dans le cadre d'une synchronisation complète, sur la page **Révision synchronisation complète Dynamics 365 for Sales**, choisissez un enregistrement pour afficher les détails. Pour mettre à jour le statut pendant la synchronisation, actualisez la page.

Sur la page **Paramétrage de la connexion Microsoft Dynamics 365**, vous pouvez obtenir des détails sur la synchronisation complète à tout moment. À partir de cette page, vous pouvez aussi ouvrir la page **Correspondances table intégration** pour afficher les détails des tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et dans Sales à synchroniser.

## <a name="handling-sales-order-data"></a>Gestion des données de commandes vente
Les commandes vente que les vendeurs envoient dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférées automatiquement vers [!INCLUDE[d365fin](includes/d365fin_md.md)] si vous sélectionnez la case à cocher **Créer automatiquement des commandes vente** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les commandes vente envoyées depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l'aide de l'action **Créer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponible sur la page **Commandes vente - Dynamics 365 for Sales**.
Pour ces commandes vente, le champ **Nom** de la commande d'origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ceci peut également fonctionner si la commande vente d'origine indique les biens hors catalogue, c'est-à-dire les articles ou les ressources qui ne sont enregistrés dans aucune application. Dans ce cas, vous devez renseigner les champs **Type produit hors catalogue** et **N° produit hors catalogue** sur la page **Paramètres ventes**, de sorte que ces ventes de produits non enregistrées soient mappées à un nombre donné d'articles/de ressources pour l'analyse financière.

Si la désignation de l'article sur la commande vente d'origine est très longue, alors une ligne commande vente supplémentaire de type **Commentaire** est créée pour stocker le texte intégral de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Les mises à jour vers les champs d'en-tête de commande vente, tels que Date dernière expédition ou Date livraison demandée, qui sont mappés dans COMMANDEVENTE-COMMANDE **Mappage de table d'intégration** sont synchronisées régulièrement vers [!INCLUDE[crm_md](includes/crm_md.md)]. Les processus tels que lancer une commande vente et expédier ou facturer une commande vente sont validés vers la chronologie de commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, voir [Introduction aux flux d'activité](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

## <a name="handling-sales-quotes-data"></a>Gestion des données de devis
Les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférés automatiquement vers [!INCLUDE[d365fin](includes/d365fin_md.md)] si vous sélectionnez la case à cocher **Traiter automatiquement les devis** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les devis envoyés depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l'aide de l'action **Traiter dans [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponible sur la page **Devis - Dynamics 365 for Sales**.
Pour ces devis, le champ **Nom** du devis d'origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. En outre, le champ **Applicable jusqu'à** du devis est transféré et mappé vers le champ **Devis valide jusqu'à** du devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Les devis subissent de nombreuses révisions avant d'être finalisés. Le traitement automatique et manuel des devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)] garantit que les versions précédentes des devis sont archivées avant traitement des nouvelles révisions de devis depuis [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="see-also"></a>Voir aussi
[Préparation pour intégrer à Dynamics 365 for Sales On-premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Gestion des relations](marketing-relationship-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)    
[Intégrer l'organisation et les utilisateurs dans Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
