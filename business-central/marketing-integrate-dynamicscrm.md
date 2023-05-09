---
title: Gérer les clients à l’aide de Dynamics 365 Sales (contient une vidéo) | Microsoft Docs
description: "Vous pouvez utiliser Dynamics\_365 Sales depuis Business Central avec une intégration et une synchronisation parfaites dans le processus allant du prospect à l’encaissement."
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
---
# Utiliser Dynamics 365 Sales depuis Business Central
Si vous utilisez Dynamics 365 Sales for Customer Engagement, bénéficiez de l’intégration parfaite dans le processus allant du prospect à l’encaissement à l’aide de [!INCLUDE[prod_short](includes/prod_short.md)] pour les activités principales, telles que le traitement des commandes, la gestion des stocks et de vos finances.

Avant de pouvoir utiliser les fonctionnalités d’intégration, votre administrateur système doit configurer la connexion et définir les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, reportez-vous à la rubrique [Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Ces étapes décrivent le processus d’intégration des versions en ligne de [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations sur la configuration sur site, voir [Préparation de l’intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Intégrer les applications vous permet d’accéder aux données dans Sales depuis [!INCLUDE[prod_short](includes/prod_short.md)], et dans certains cas, inversement. Vous pouvez utiliser et synchroniser les types de données communs aux deux services, par exemple clients, contacts et informations de vente, et mettre à jour les données dans les deux applications.  

Par exemple, un vendeur dans [!INCLUDE[crm_md](includes/crm_md.md)] peut utiliser les tarifs dans [!INCLUDE[prod_short](includes/prod_short.md)] lorsqu’il crée une commande vente. Lorsqu’il ajoute l’article à la ligne commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)], il peut également visualiser le niveau de stock (disponibilité) de l’article dans [!INCLUDE[prod_short](includes/prod_short.md)].

Inversement, les préparateurs de commandes dans [!INCLUDE[prod_short](includes/prod_short.md)] peuvent gérer les commandes vente qui sont automatiquement ou manuellement transférées depuis [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, ils peuvent créer et valider des lignes de commande vente pour les articles ou les ressources saisies dans [!INCLUDE[crm_md](includes/crm_md.md)] comme produits hors catalogue. Pour plus d’informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] s’intègre uniquement à [!INCLUDE[crm_md](includes/crm_md.md)]. Les autres applications Dynamics 365 qui modifient le flux de travail ou le modèle de données standard dans [!INCLUDE[crm_md](includes/crm_md.md)], par exemple Project Service Automation, peuvent désactiver l’intégration entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].

## Enregistrements couplage
Le guide de configuration assistée vous permet de choisir les données à synchroniser. Ultérieurement, vous pouvez également configurer la synchronisation pour les enregistrements spécifiques. C’est ce qu’on appelle le *couplage*. Par exemple, vous pouvez coupler un compte spécifique dans [!INCLUDE[crm_md](includes/crm_md.md)] avec un client spécifique dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cette rubrique décrit ce qu’il convient de prendre en compte lorsque vous couplez des enregistrements.

Par exemple, si vous souhaitez afficher les comptes [!INCLUDE[crm_md](includes/crm_md.md)] en tant que clients dans [!INCLUDE[prod_short](includes/prod_short.md)], vous devez coupler les deux types d’enregistrements. Pour ce faire, sur la page de la liste **Clients** dans [!INCLUDE[prod_short](includes/prod_short.md)], utilisez l’action **Configurer le couplage**. Puis vous devez spécifier quels clients [!INCLUDE[prod_short](includes/prod_short.md)] correspondent à quels comptes dans [!INCLUDE[crm_md](includes/crm_md.md)].

Vous pouvez également créer (et coupler) un compte dans [!INCLUDE[crm_md](includes/crm_md.md)] selon, par exemple, un enregistrement client dans [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide de l’option **Créer un compte dans Dynamics 365 Sales** ou vice-versa, à l’aide de l’option **Créer un client dans [!INCLUDE[prod_short](includes/prod_short.md)]**.

Lorsque vous configurez un couplage entre deux enregistrements, vous pouvez également demander manuellement que l’enregistrement actuel, par exemple un client, soit remplacé immédiatement par les données de compte depuis Sales (ou depuis [!INCLUDE[prod_short](includes/prod_short.md)]) à l’aide de l’action **Synchroniser maintenant**. L’action**Synchroniser maintenant** vous demandera de remplacer les données dans Sales ou les données d’enregistrement [!INCLUDE[prod_short](includes/prod_short.md)].

Dans certains cas, vous devez coupler certains ensembles de données avant d’autres ensembles de données, comme l’indique le tableau suivant.

|Données|Ce qu’il convient de coupler tout d’abord|
|-----|----|
|Clients et comptes|Coupler des vendeurs avec des utilisateurs [!INCLUDE[crm_md](includes/crm_md.md)]|
|Articles et ressources|Coupler des unités de mesure avec des groupes d’unités [!INCLUDE[crm_md](includes/crm_md.md)]|
|Prix des articles et des ressources|Coupler des groupes tarifs client avec des prix [!INCLUDE[crm_md](includes/crm_md.md)]|

> [!NOTE]  
> Si vos prix ou clients utilisent des devises étrangères, assurez-vous de coupler des devises avec des devises de transaction Sales.

Dans [!INCLUDE[crm_md](includes/crm_md.md)], les commandes vente dépendent d’informations comme les clients, les unités de mesure, les devis, les groupes tarifs client, les articles et/ou les ressources. Pour assurer une intégration avec les commandes vente, vous devez coupler des clients, des unités de mesure, des devises, des groupes tarifs client, des articles et/ou des ressources.

## Synchronisation complète des enregistrements
À la fin du guide de configuration assistée, vous pouvez sélectionner l’action **Exécuter une synchronisation complète** pour démarrer la synchronisation de tous les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] avec tous les enregistrements associés dans [!INCLUDE[crm_md](includes/crm_md.md)]. Sur la page **Révision synchronisation complète Dynamics 365 Sales**, sélectionnez l’action **Démarrer**. La synchronisation complète peut prendre un certain temps, mais vous pouvez continuer à travailler dans [!INCLUDE[prod_short](includes/prod_short.md)] pendant son exécution en arrière-plan.

Pour vérifier la progression de divers projets dans le cadre d’une synchronisation complète, sur la page **Révision synchronisation complète Dynamics 365 Sales**, choisissez un enregistrement pour afficher les détails. Pour mettre à jour le statut pendant la synchronisation, actualisez la page.

Sur la page **Paramétrage de la connexion Microsoft Dynamics 365**, vous pouvez obtenir des détails sur la synchronisation complète à tout moment. À partir de cette page, vous pouvez aussi ouvrir la page **Mappages de table d’intégration** pour afficher les détails des tables dans [!INCLUDE[prod_short](includes/prod_short.md)] et dans Sales à synchroniser.

## Gestion des données de commandes vente
Les commandes vente que les vendeurs envoient dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférées automatiquement vers [!INCLUDE[prod_short](includes/prod_short.md)] si vous sélectionnez la case à cocher **Créer automatiquement des commandes vente** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les commandes vente envoyées depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l’aide de l’action **Créer dans [!INCLUDE[prod_short](includes/prod_short.md)]** disponible sur la page **Commandes vente - Dynamics 365 for Sales**.
Pour ces commandes vente, le champ **Nom** de la commande d’origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[prod_short](includes/prod_short.md)].

Ceci peut également fonctionner si la commande vente d’origine indique les biens hors catalogue, c’est-à-dire les articles ou les ressources qui ne sont enregistrés dans aucune application. Dans ce cas, vous devez renseigner les champs **Type produit hors catalogue** et **N° produit hors catalogue** sur la page **Paramètres ventes**, de sorte que ces ventes de produits non enregistrés soient mappées à un nombre donné d’articles ou de ressources.

> [!NOTE]
> Vous ne pouvez pas mapper une écriture à un élément ou une ressource dans [!INCLUDE[prod_short](includes/prod_short.md)] qui est couplé à un produit dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour autoriser les écritures, nous vous recommandons de créer un article ou une ressource spécifiquement à cette fin et de ne pas le coupler avec un produit dans [!INCLUDE[crm_md](includes/crm_md.md)]. 

Si la désignation de l’article sur la commande vente d’origine est très longue, alors une ligne commande vente supplémentaire de type **Commentaire** est créée pour stocker le texte intégral de la commande vente dans [!INCLUDE[prod_short](includes/prod_short.md)].

Les mises à jour vers les champs d’en-tête commande vente, tels que Date dernière expédition ou Date livraison demandée, qui sont mappés dans le mappage de tables d’intégration **COMMANDEVENTE-COMMANDE**, sont synchronisées régulièrement avec [!INCLUDE[crm_md](includes/crm_md.md)]. Les processus tels que lancer une commande vente et expédier ou facturer une commande vente sont validés vers la chronologie de commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, voir [Introduction aux flux d’activité](/dynamics365/sales-enterprise/manage-activities). Pour activer la publication et les activités des commandes dans [!INCLUDE[crm_md](includes/crm_md.md)], voir [Configurer le contrôle Notes pour accéder aux informations sur les publications d’une entité personnalisée](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) dans la documentation Customer Engagement. L’article fait référence à Customer Engagement (on-premises), mais les étapes sont les mêmes pour la version en ligne. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> La synchronisation périodique basée sur le mappage de tables d’intégration **COMMANDEVENTE-COMMANDE** fonctionne uniquement lorsque l’intégration de la commande vente est activée. Pour en savoir plus, consultez [Paramètres de connexion sur la page Paramètres de connexion Sales](admin-prepare-dynamics-365-for-sales-for-integration.md). Seules les commandes vente créées à partir des commandes vente envoyées dans [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisées. Pour plus d’informations, voir [Activer l’intégration du traitement des commandes vente](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## Gestion des données de devis
Les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)] seront transférés automatiquement vers [!INCLUDE[prod_short](includes/prod_short.md)] si vous sélectionnez la case à cocher **Traiter automatiquement les devis** sur la page **Paramètres de la connexion Microsoft Dynamics 365**.
Sinon, vous pouvez convertir manuellement les devis envoyés depuis [!INCLUDE[crm_md](includes/crm_md.md)] à l’aide de l’action **Traiter dans [!INCLUDE[prod_short](includes/prod_short.md)]** disponible sur la page **Devis - Dynamics 365 Sales**.
Pour ces devis, le champ **Nom** du devis d’origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[prod_short](includes/prod_short.md)]. En outre, le champ **Applicable jusqu’à** du devis est transféré et mappé vers le champ **Devis valide jusqu’à** du devis dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Les devis subissent de nombreuses révisions avant d’être finalisés. Le traitement automatique et manuel des devis dans [!INCLUDE[prod_short](includes/prod_short.md)] garantit que les versions précédentes des devis sont archivées avant traitement des nouvelles révisions de devis depuis [!INCLUDE[crm_md](includes/crm_md.md)].

Quand vous choisissez **Traitement** dans [!INCLUDE[prod_short](includes/prod_short.md)] pour un devis dans un état **Conclu**, une commande vente est créée dans [!INCLUDE[prod_short](includes/prod_short.md)] uniquement si une commande vente correspondante est soumise dans [!INCLUDE[crm_md](includes/crm_md.md)]. Sinon, le devis n’est publié que dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si une commande vente correspondante est envoyée dans [!INCLUDE[crm_md](includes/crm_md.md)] plus tard, et qu’une commande vente en est créée, le **N° devis** est mis à jour sur la commande vente et le devis est archivé.

## Gestion des factures vente enregistrées, des paiements client et des statistiques
Après l’exécution d’une commande vente, les factures associées seront créées. Lorsque vous facturez une commande vente, vous pouvez transférer la facture vente enregistrée dans [!INCLUDE[crm_md](includes/crm_md.md)] si vous cochez la case **Créer une facture dans [!INCLUDE[crm_md](includes/crm_md.md)]** sur la page **Facture vente enregistrée**. Les factures enregistrées sont transférées dans [!INCLUDE[crm_md](includes/crm_md.md)] avec le statut **Facturé**.

Une fois que le paiement client est reçu pour la facture vente dans [!INCLUDE[prod_short](includes/prod_short.md)], le statut de la facture vente sera modifié en **Payé** avec la **raison du statut** définie sur **Partielle** si elle est partiellement payée, ou **Totale** si elle est totalement payée, lorsque vous exécutez **Mettre à jour les statistiques compte** sur la page du client dans [!INCLUDE[prod_short](includes/prod_short.md)]. La fonction **Mettre à jour les statistiques compte** actualisera également des valeurs telles que le **solde** et les **ventes totales** dans le récapitulatif **Statistiques compte [!INCLUDE[prod_short](includes/prod_short.md)]** dans [!INCLUDE[crm_md](includes/crm_md.md)]. Sinon, les projets planifiés (statistiques client et POSTEDSALESINV-INV) peuvent exécuter automatiquement ces deux processus en arrière-plan. 

## Gestion des prix de vente
> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons lancé des processus rationalisés pour la configuration et la gestion des prix et des remises. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Les étapes pour terminer le processus diffèrent selon que votre administrateur a activé la nouvelle expérience de tarification. 

> [!NOTE]
> Si la synchronisation des prix standard ne fonctionne, nous vous recommandons d′utiliser les fonctions de personnalisation de l′intégration. Pour plus d′informations, voir [Personnalisation d′une intégration avec Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Expérience actuelle](#tab/current-experience/)
Dans l′expérience de tarification actuelle, [!INCLUDE[prod_short](includes/prod_short.md)] synchronise les prix de vente qui : 

* S′appliquent à tous les clients. Les listes prix vente par défaut sont créées à partir du prix indiqué dans le champ **Prix unitaire** sur la page **Fiche article** pour les articles.
* S′appliquent à un groupe prix client spécifique. Par exemple, les prix de vente pour vos clients de vente en gros ou de détail. Pour synchroniser les prix à partir d′un groupe prix client, procédez comme suit :

    1. Couplez les articles pour lesquels les prix sont fixés par le groupe prix client.
    2. Sur la page **Groupes prix client**, couplez le groupe prix client en choisissant **Connexe**, puis **Dynamics 365 Sales**, **Couplage**, puis **Configurer le couplage**. Le couplage crée une liste de prix active dans [!INCLUDE[prod_short](includes/prod_short.md)] avec le même nom que le groupe prix client dans [!INCLUDE[crm_md](includes/crm_md.md)] et synchronise automatiquement tous les articles pour lesquels le groupe prix client définit le prix.

:::image type="content" source="media/customer-price-group.png" alt-text="Page Groupe prix client.":::

#### [Nouvelle expérience](#tab/new-experience/)  

La nouvelle expérience de tarification synchronise les listes de prix qui répondent aux critères suivants :

* L′option **Autoriser la mise à jour des valeurs par défaut** est désactivée.
* Le type de prix est Vente.
* Le type de montant est Prix.
* Le type de produit sur les lignes doit être Article ou Ressource. 
* Une quantité minimale n′est pas spécifiée.

[!INCLUDE[prod_short](includes/prod_short.md)] synchronise les prix de vente qui s′appliquent à tous les clients. Les listes prix vente par défaut sont créées à partir du prix indiqué dans le champ **Prix unitaire** sur la page **Fiche article** pour les articles.

Pour synchroniser les listes de prix, sur la page **Liste prix vente**, choisissez **Connexe**, **Dynamics 365 Sales**, **Couplage**, puis **Configurer le couplage**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Page Liste prix vente.":::

---


## Voir aussi
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gestion des relations](marketing-relationship-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)    
[Vue d’ensemble de Sales et du centre des ventes](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]