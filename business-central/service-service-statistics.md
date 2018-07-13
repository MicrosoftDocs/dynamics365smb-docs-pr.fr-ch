---
title: Statistiques service | Microsoft Docs
description: "Obtenez un aperçu rapide du contenu des documents service comme les commandes, devis, factures ou avoirs, ainsi que les détails des lignes service spécifiques et les articles de service."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 30f93593985140abd49c6cd4f90a992da793b164
ms.contentlocale: fr-ch
ms.lasthandoff: 06/01/2018

---

# <a name="viewing-service-statistics"></a>Affichage des statistiques service
Vous pouvez utiliser des statistiques pour analyser les documents service et évaluer la bonne gestion de vos processus de service. Vous pouvez analyser les contrats de service, articles, devis, commandes, factures et avoirs en choisissant l'action **Statistiques**. Pour les articles et contrats de service, vous pouvez également utiliser les champs **Trendscape article de service** ou **Trendscape contrat** pour afficher un résumé des écritures comptables service pour un article de service spécifique.   

## <a name="viewing-statistics-for-service-orders"></a>Affichage des statistiques pour les commandes service
Ces fonctions-ci donnent un aperçu rapide du contenu de l'ensemble de la commande service, des informations sur les lignes service spécifiques, la facturation, la livraison et la consommation, et du solde du client.  

Les données statistiques relatives à une commande service sont affichées dans la fenêtre **Statistiques commande service** pour la commande concernée. Vous pouvez ouvrir la fenêtre statistiques à partir d'une commande service. Dans la fenêtre **Commandes service**, choisissez **Statistiques**. Les raccourcis de cette fenêtre affichent des informations telles que la quantité, le montant, la TVA, le coût, la marge, et le crédit autorisé pour le client. Les montants figurant dans la fenêtre sont exprimés dans la devise de la commande service, sauf indication contraire.  

### <a name="view-totals-for-a-service-order"></a>Afficher les totaux d'une commande service  
Vous pouvez afficher le montant total des lignes service, avec et sans TVA, la partie TVA, le coût et la marge des lignes service. La fenêtre affiche également des informations spécifiques à l'article, telles que le poids, le volume et la quantité de colis.  

### <a name="view-shipping-information"></a>Afficher les informations d'expédition  
Vous pouvez afficher des informations sur les articles, les ressources ou les coûts liés à la livraison. Pour fournir ces informations, le programme utilise les valeurs spécifiées dans le champ **Qté à expédier** de chaque ligne service de la commande.  

### <a name="view-order-details"></a>Afficher les détails de commande  
Vous pouvez afficher des informations sur les articles, les heures et les coûts ressource à facturer et consommer. Le tableau suivant décrit ces informations.  

|Colonne | Désignation|  
|------------|---------------------------------------|  
|**Facturation**|affiche des montants à valider comme facturés à partir de la commande service.|  
|**Consommation**|Affiche la quantité et le coût des articles ou ressources qui seront validés comme consommés.|  
|**Total**|Affiche les montants totaux figurant sur la commande service, qui résultent de l'ajout des montants facturés aux montants consommés.|  

### <a name="analyze-service-order-lines"></a>Analyser les lignes commande de service  
Vous pouvez analyser les informations en fonction des types de lignes service incluses dans la commande service. Les montants sont présentés séparément pour les éléments suivants :  

* Articles  
* Ressources  
* Comptes de gestion et Comptabilité  

### <a name="view-customer-information"></a>Afficher les informations client  
Affichez le solde du compte du client, en complément du crédit maximum qui peut être accordé au client pour lequel vous avez créé le document service.

## <a name="viewing-service-item-statistics"></a>Affichage des statistiques article service
Dans la fenêtre **Statistiques article service**, vous pouvez visualiser les toutes dernières informations relatives à un article de service en fonction des types d'écriture comptable service suivants :  

* Ressources  
* Articles  
* Coût service  
* Contrats de service  
* Total  

Pour chaque type d'écriture, vous pouvez visualiser le montant facturé, l'activité (montant), le coût total, la quantité, la quantité facturée et la quantité consommée, le montant de la marge et son pourcentage. Le pourcentage de marge est calculé selon la formule suivante :  

* (Montant facturé - activité (coût)) x 100 / montant facturé  

## <a name="using-trendscapes"></a>Utilisation des trendscapes
Pour les articles de service et les contrats de service, les fenêtres **Trendscape article de service** ou **Trendscape contrat de service** affichent une liste déroulante des écritures comptables service sur une période pour un article ou contrat de service spécifique. Pour afficher le trendscape, ouvrez l'article de service ou le contrat de service, choisissez l'action **Statistiques**, puis **Trendscape**.

Lorsque vous faites défiler la liste, les montants sont calculés en devise société en fonction de l'intervalle spécifié. Tous les montants sont calculés à partir d'écritures comptables service, c'est-à-dire des écritures qui sont crées lorsque vous validez des commandes service ou des factures service.

Vous pouvez filtrer la liste en spécifiant les articles de service à inclure.  

> [!Tip]  
>  Si vous avez choisi **Jour** comme intervalle de temps et que vous voulez passer en revue une longue période, vous pouvez le faire plus rapidement en utilisant un intervalle plus grand, par exemple **Trimestre**. Lorsque vous avez trouvé la période souhaitée, vous pouvez repasser à l'intervalle de départ pour visualiser les données plus en détail.   

## <a name="viewing-gains-and-losses-on-contracts"></a>Affichage des gains et pertes sur les contrats  
Une écriture gain/perte contrat est générée lorsqu'un devis contrat est converti en contrat de service, lors de l'ajout ou de la suppression de lignes contrat dans un contrat de service et lors de l'annulation d'un contrat. Vous pouvez visualiser les gains/pertes contrat sur les pages suivantes.  

|Page | Désignation|  
|----------------|---------------------------------------|  
|**Gain/Perte contrat (contrats)**|Pour visualiser les écritures gain/perte contrat par contrat de service.|  
|**Gain/Perte contrat (groupes)**|Pour visualiser les écritures gain/perte contrat par groupe de contrat de service.|  
|**Gain/Perte contrat (clients)**|Pour visualiser les écritures gain/perte contrat par client.|  
|**Gain/Perte contrat (motifs)**|Pour visualiser les écritures gain/perte contrat par code motif.|  
|**Gain/Perte contrat ctre gest.**|Pour visualiser les écritures gain/perte contrat par centre de gestion.|  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez le nom de la page à afficher, puis sélectionnez le lien connexe.  
2. Renseignez les filtres à appliquer. Par exemple, dans la fenêtre **Gain/perte contrat (motifs)**, choisissez une valeur pour **Filtre code motif**.  
3. Choisissez l'action **Afficher matrice**.

## <a name="viewing-statistics-for-posted-service-documents"></a>Affichage des statistiques pour les documents service validés
La fonctionnalité des statistiques service vous permet d'obtenir un aperçu statistique du contenu des documents service validés, tels qu'une expédition validée, une facture validée et un avoir validé.  

Les informations statistiques sont affichées dans la fenêtre statistiques du document service validé correspondant. Vous pouvez ouvrir la fenêtre statistiques sur la fiche de l'expédition service validée, de la facture service validée ou des avoirs service validés. Pour chacun de ces types de document, sous l'onglet **Accueil**, dans le groupe **Traitement**, choisissez **Statistiques**. Par exemple, dans la fenêtre **Factures service enreg.**, sous l'onglet **Accueil**, dans le groupe **Traitement**, choisissez **Statistiques**.  

### <a name="posted-service-shipment-statistics"></a>Statistiques expédition service enreg.  
La fenêtre **Statistiques expédition service** donne un aperçu d'une expédition service validée. Cela inclut notamment des informations sur le contenu physique de l'expédition, par exemple la quantité des articles expédiés, les heures ou les coûts ressource, ainsi que le poids et le volume des articles expédiés.  

### <a name="posted-service-invoice-statistics"></a>Statistiques facture service enreg.  
vous pouvez voir un résumé statistique sur une facture service validée dans la fenêtre **Statistiques facture service**. Vous pouvez afficher les totaux de la facture service validée. Les données englobent le montant total des lignes service (avec et sans TVA) qui a été validé et facturé, la partie TVA, le coût et la marge de la facture validée. La fenêtre affiche également des informations sur les éléments suivants :  

* Les articles sur les lignes facture service, par exemple le poids, le volume et la quantité de colis.  
* Le solde du compte du client, et le crédit maximum que vous pouvez accorder au client.  

### <a name="posted-service-credit-memo-statistics"></a>Statistiques avoir service enreg.  
La fenêtre **Statistiques avoir service** permet d'obtenir un aperçu statistique des lignes figurant dans un avoir service validé. L'aperçu peut inclure :

* Les montants totaux de l'avoir validé, avec des informations comme la quantité, le montant, la TVA, le coût et la marge. L'aperçu affiche également des informations spécifiques sur les articles figurant sur les lignes service de l'avoir validé, telles que la quantité, le poids et le volume.  
* Des informations générales sur le client, comme son crédit autorisé et le solde de son compte.  

## <a name="see-also"></a>Voir aussi  
[Créer commande service](service-how-to-create-service-orders.md)   
[Créer des articles de service](service-how-to-create-service-items.md)   
[Services de planification](service-plan-service.md)  

