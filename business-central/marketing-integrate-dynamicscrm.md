---
title: Gérer les clients à l'aide de Dynamics 365 Sales | Microsoft Docs
description: Vous pouvez utiliser Dynamics 365 Sales depuis Business Central pour mapper les données et avoir une intégration et une synchronisation parfaites dans le processus allant du prospect à l'encaissement.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 1e45a480e8fdcc508de8ac82a6d2860147d76cec
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991799"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Utilisation de Dynamics 365 Sales depuis Business Central
Si vous utilisez Dynamics 365 Sales for Customer Engagement, bénéficiez de l'intégration parfaite dans le processus allant du prospect à l'encaissement à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour les activités principales, telles que le traitement des commandes, la gestion des stocks et de vos finances.

Avant de pouvoir utiliser les fonctionnalités d’intégration, vous devez configurer la connexion et définir les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, reportez-vous à la rubrique [Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Ces étapes décrivent le processus d'intégration des versions en ligne de [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations sur la configuration sur site, voir [Préparation de l'intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Intégrer les applications vous permet d'accéder aux données dans Sales depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et dans certains cas, inversement. Vous pouvez utiliser et synchroniser les types de données communs aux deux services, par exemple clients, contacts et informations de vente, et mettre à jour les données dans les deux applications.  

Par exemple, un vendeur dans Sales peut utiliser les tarifs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'il crée une commande vente. Lorsqu'il ajoute l'article à la ligne commande vente dans Sales, il peut également visualiser le niveau de stock (disponibilité) de l'article dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Inversement, les préparateurs de commandes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] peuvent gérer les commandes vente qui sont automatiquement ou manuellement transférées depuis Sales. Par exemple, ils peuvent créer et valider des lignes de commande vente pour les articles ou les ressources saisies dans Sales comme produits hors-catalogue. Pour plus d'informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] s'intègre à Dynamics 365 Sales uniquement. Les autres applications Dynamics 365 qui modifient le flux de travail ou le modèle de données standard dans Sales, par exemple Project Service Automation, peuvent désactiver l'intégration entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.

### <a name="coupling-records"></a>Enregistrements couplage
Le guide de configuration assistée vous permet de choisir les données à synchroniser. Ultérieurement, vous pouvez également configurer la synchronisation pour les enregistrements spécifiques. C'est ce qu'on appelle le *couplage*. Par exemple, vous pouvez associer un compte spécifique dans Sales avec un client spécifique dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette rubrique décrit ce qu'il convient de prendre en compte lorsque vous couplez des enregistrements.

Par exemple, si vous souhaitez afficher les comptes dans Sales en tant que clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez coupler les deux types d'enregistrements. Pour ce faire, sur la page de la liste **Clients** dans [!INCLUDE[d365fin](includes/d365fin_md.md)], utilisez l'action **Configurer le couplage**. Puis vous devez spécifier quels clients [!INCLUDE[d365fin](includes/d365fin_md.md)] correspondent à quels comptes dans Sales.

Vous pouvez également créer (et coupler) un compte dans Sales selon, par exemple, l'enregistrement client dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un compte dans Dynamics 365 Sales** ou vice-versa, à l'aide de l'option **Créer un client dans [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

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
À la fin du guide de configuration assistée, vous pouvez sélectionner l'action **Exécuter une synchronisation complète** pour démarrer la synchronisation de tous les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] avec tous les enregistrements associés dans Sales. Sur la page **Révision synchronisation complète Dynamics 365 Sales**, sélectionnez l'action **Démarrer**. La synchronisation complète peut prendre un certain temps, mais vous pouvez continuer à travailler dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant qu'elle fonctionne à l'arrière-plan.

Pour vérifier la progression de divers projets dans le cadre d'une synchronisation complète, sur la page **Révision synchronisation complète Dynamics 365 Sales**, choisissez un enregistrement pour afficher les détails. Pour mettre à jour le statut pendant la synchronisation, actualisez la page.

Sur la page **Paramétrage de la connexion Microsoft Dynamics 365**, vous pouvez obtenir des détails sur la synchronisation complète à tout moment. À partir de cette page, vous pouvez aussi ouvrir la page **Correspondances table intégration** pour afficher les détails des tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et dans Sales à synchroniser.

## <a name="handling-sales-order-data"></a>Gestion des données de commandes vente
Les commandes vente que les vendeurs envoient dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférées automatiquement vers [!INCLUDE[d365fin](includes/d365fin_md.md)] si vous sélectionnez la case à cocher **Créer automatiquement des commandes vente** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les commandes vente envoyées depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l'aide de l'action **Créer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponible sur la page **Commandes vente - Dynamics 365 for Sales**.
Pour ces commandes vente, le champ **Nom** de la commande d'origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ceci peut également fonctionner si la commande vente d'origine indique les biens hors catalogue, c'est-à-dire les articles ou les ressources qui ne sont enregistrés dans aucune application. Dans ce cas, vous devez renseigner les champs **Type produit hors catalogue** et **N° produit hors catalogue** sur la page **Paramètres ventes**, de sorte que ces ventes de produits non enregistrées soient mappées à un nombre donné d'articles/de ressources pour l'analyse financière.

Si la désignation de l'article sur la commande vente d'origine est très longue, alors une ligne commande vente supplémentaire de type **Commentaire** est créée pour stocker le texte intégral de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Les mises à jour vers les champs d'en-tête de commande vente, tels que Date dernière expédition ou Date livraison demandée, qui sont mappés dans COMMANDEVENTE-COMMANDE **Mappage de table d'intégration** sont synchronisées régulièrement vers [!INCLUDE[crm_md](includes/crm_md.md)]. Les processus tels que lancer une commande vente et expédier ou facturer une commande vente sont validés vers la chronologie de commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, voir [Introduction aux flux d'activité](/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!NOTE]  
> La synchronisation périodique basée sur le **Mappage de table d'intégration** COMMANDEVENTE-COMMANDE fonctionne uniquement lorsque l'intégration de la commande vente est activée. Pour plus d'informations, voir [Se connecter à Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md). Seules les commandes vente créées à partir des commandes vente envoyées dans [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisées. Pour plus d'informations, voir [Activer l'intégration du traitement des commandes vente](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Gestion des données de devis
Les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférés automatiquement vers [!INCLUDE[d365fin](includes/d365fin_md.md)] si vous sélectionnez la case à cocher **Traiter automatiquement les devis** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les devis envoyés depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l'aide de l'action **Traiter dans [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponible sur la page **Devis - Dynamics 365 Sales**.
Pour ces devis, le champ **Nom** du devis d'origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. En outre, le champ **Applicable jusqu'à** du devis est transféré et mappé vers le champ **Devis valide jusqu'à** du devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Les devis subissent de nombreuses révisions avant d'être finalisés. Le traitement automatique et manuel des devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)] garantit que les versions précédentes des devis sont archivées avant traitement des nouvelles révisions de devis depuis [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Gestion des factures vente enregistrées, des paiements client et des statistiques
Après l'exécution d'une commande vente, les factures associées seront créées. Lorsque vous facturez une commande vente, vous pouvez transférer la facture vente enregistrée dans [!INCLUDE[crm_md](includes/crm_md.md)] si vous cochez la case **Créer une facture dans [!INCLUDE[crm_md](includes/crm_md.md)]** sur la page **Facture vente enregistrée**. Les factures enregistrées sont transférées dans [!INCLUDE[crm_md](includes/crm_md.md)] avec le statut **Facturé**.

Une fois que le paiement client est reçu pour la facture vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le statut de la facture vente sera modifié en **Payé** avec la **raison du statut** définie sur **Partielle** si elle est partiellement payée, ou **Totale** si elle est totalement payée, lorsque vous exécutez **Mettre à jour les statistiques compte** sur la page du client dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. La fonction **Mettre à jour les statistiques compte** actualisera également des valeurs telles que le **solde** et les **ventes totales** dans le **récapitulatif Statistiques compte [!INCLUDE[d365fin](includes/d365fin_md.md)]** dans [!INCLUDE[crm_md](includes/crm_md.md)]. Sinon, les projets planifiés (statistiques client et POSTEDSALESINV-INV) peuvent exécuter automatiquement ces deux processus en arrière-plan.

## <a name="see-also"></a>Voir aussi
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gestion des relations](marketing-relationship-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)    
[Vue d'ensemble de Sales et du centre des ventes](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
