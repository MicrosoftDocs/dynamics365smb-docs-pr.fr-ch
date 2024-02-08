---
title: Statistiques service
description: 'Obtenez un aperçu rapide du contenu et des statistiques des documents service comme les commandes, devis, factures ou avoirs, ainsi les lignes service spécifiques et les articles de service.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Affichage des statistiques service
Vous pouvez utiliser des statistiques pour analyser les documents service et évaluer la bonne gestion de vos processus de service. Vous pouvez analyser les contrats de service, articles, devis, commandes, factures et avoirs en choisissant l’action **Statistiques**. Pour les articles et contrats de service, vous pouvez également utiliser les champs **Trendscape article de service** ou **Trendscape contrat** pour afficher un résumé des écritures comptables service pour un article de service spécifique.   

## Affichage des statistiques pour les commandes service
Ces fonctions-ci donnent un aperçu rapide du contenu de l’ensemble de la commande service, des informations sur les lignes service spécifiques, la facturation, la livraison et la consommation, et du solde du client.  

Les données statistiques relatives à une commande service sont affichées sur la page **Statistiques commande service** pour la commande concernée. Vous pouvez ouvrir la page de statistiques à partir d’une commande service. Sur la page **Commandes service**, choisissez **Statistiques**. Les raccourcis de cette page affichent des informations telles que la quantité, le montant, la TVA, le coût, la marge, et le crédit autorisé pour le client. Les montants figurant sur la page sont exprimés dans la devise de la commande service, sauf indication contraire.  

### Afficher les totaux d’une commande service  
Vous pouvez afficher le montant total des lignes service, avec et sans TVA, la partie TVA, le coût et la marge des lignes service. La page affiche également des informations spécifiques à l’article, telles que le poids, le volume et la quantité de colis.  

### Afficher les informations d’expédition  
Vous pouvez afficher des informations sur les articles, les ressources ou les coûts liés à la livraison. Pour fournir ces informations, le programme utilise les valeurs spécifiées dans le champ **Qté à expédier** de chaque ligne service de la commande.  

### Afficher les détails de commande  
Vous pouvez afficher des informations sur les articles, les heures et les coûts ressource à facturer et consommer. Le tableau suivant décrit ces informations.  

|Colonne | Désignation|  
|------------|---------------------------------------|  
|**Facturation**|affiche des montants à valider comme facturés à partir de la commande service.|  
|**Consommation**|Affiche la quantité et le coût des articles ou ressources qui seront validés comme consommés.|  
|**Total**|Affiche les montants totaux figurant sur la commande service, qui résultent de l’ajout des montants facturés aux montants consommés.|  

### Analyser les lignes commande de service  
Vous pouvez analyser les informations en fonction des types de lignes service incluses dans la commande service. Les montants sont présentés séparément pour les éléments suivants :  

* Articles  
* Ressources  
* Comptes de gestion et Comptabilité  

### Afficher les informations client  
Affichez le solde du compte du client, en complément du crédit maximum qui peut être accordé au client pour lequel vous avez créé le document service.

## Affichage des statistiques article service
Sur la page **Statistiques article service**, vous pouvez visualiser les toutes dernières informations relatives à un article de service en fonction des types d’écriture comptable service suivants :  

* Ressources  
* Articles  
* Coût service  
* Contrats de service  
* Total  

Pour chaque type d’écriture, vous pouvez visualiser le montant facturé, l’activité (montant), le coût total, la quantité, la quantité facturée et la quantité consommée, le montant de la marge et son pourcentage. Le pourcentage de marge est calculé selon la formule suivante :  

* (Montant facturé - activité (coût)) x 100 / montant facturé  

## Utiliser des trendscapes
Pour les articles de service et les contrats de service, les pages **Trendscape article de service** ou **Trendscape contrat de service** affichent une liste déroulante des écritures comptables service sur une période pour un article ou contrat de service spécifique. Pour afficher le trendscape, ouvrez l’article de service ou le contrat de service, choisissez l’action **Statistiques**, puis **Trendscape**.

Lorsque vous faites défiler la liste, les montants sont calculés en devise société en fonction de l’intervalle spécifié. Tous les montants sont calculés à partir d’écritures comptables service, c’est-à-dire des écritures qui sont crées lorsque vous validez des commandes service ou des factures service.

Vous pouvez filtrer la liste en spécifiant les articles de service à inclure.  

> [!Tip]  
>  Si vous avez choisi **Jour** comme intervalle de temps et que vous voulez passer en revue une longue période, vous pouvez le faire plus rapidement en utilisant un intervalle plus grand, par exemple **Trimestre**. Lorsque vous avez trouvé la période souhaitée, vous pouvez repasser à l’intervalle de départ pour visualiser les données plus en détail.   

## Affichage des gains et pertes sur les contrats  
Une écriture gain/perte contrat est générée lorsqu’un devis contrat est converti en contrat de service, lors de l’ajout ou de la suppression de lignes contrat dans un contrat de service et lors de l’annulation d’un contrat. Vous pouvez visualiser les gains/pertes contrat sur les pages suivantes.  

|Page | Désignation|  
|----------------|---------------------------------------|  
|**Gain/Perte contrat (contrats)**|Pour visualiser les écritures gain/perte contrat par contrat de service.|  
|**Gain/Perte contrat (groupes)**|Pour visualiser les écritures gain/perte contrat par groupe de contrat de service.|  
|**Gain/Perte contrat (clients)**|Pour visualiser les écritures gain/perte contrat par client.|  
|**Gain/Perte contrat (motifs)**|Pour visualiser les écritures gain/perte contrat par code motif.|  
|**Gain/Perte contrat ctre gest.**|Pour visualiser les écritures gain/perte contrat par centre de gestion.|  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez le nom de la page à afficher, puis choisissez le lien associé.  
2. Renseignez les filtres à appliquer. Par exemple, sur la page **Gain/perte contrat (motifs)**, choisissez une valeur pour **Filtre code motif**.  
3. Choisissez l’action **Afficher matrice**.

## Affichage des statistiques pour les documents service validés
La fonctionnalité des statistiques service vous permet d’obtenir un aperçu statistique du contenu des documents service validés, tels qu’une expédition validée, une facture validée et un avoir validé.  

Les informations statistiques sont affichées sur la page de statistiques du document service validé correspondant. Vous pouvez ouvrir la page de statistiques sur la fiche de l’expédition service validée, de la facture service validée ou des avoirs service validés. Pour chacun de ces types de document, choisissez l’action **Statistiques**. Par exemple, dans la page **Factures service enreg.**, sélectionnez l’action **Statistiques**.  

### Statistiques expédition service enreg.  
La page **Statistiques expédition service** donne un aperçu d’une expédition service validée. Cela inclut notamment des informations sur le contenu physique de l’expédition, par exemple la quantité des articles expédiés, les heures ou les coûts ressource, ainsi que le poids et le volume des articles expédiés.  

### Statistiques facture service enreg.  
vous pouvez voir un résumé statistique sur une facture service validée sur la page **Statistiques facture service**. Vous pouvez afficher les totaux de la facture service validée. Les données englobent le montant total des lignes service (avec et sans TVA) qui a été validé et facturé, la partie TVA, le coût et la marge de la facture validée. La page affiche également des informations sur les éléments suivants :  

* Les articles sur les lignes facture service, par exemple le poids, le volume et la quantité de colis.  
* Le solde du compte du client, et le crédit maximum que vous pouvez accorder au client.  

### Statistiques avoir service enreg.  
La page **Statistiques avoir service** permet d’obtenir un aperçu statistique des lignes figurant dans un avoir service validé. L’aperçu peut inclure :

* Les montants totaux de l’avoir validé, avec des informations comme la quantité, le montant, la TVA, le coût et la marge. L’aperçu affiche également des informations spécifiques sur les articles figurant sur les lignes service de l’avoir validé, telles que la quantité, le poids et le volume.  
* Des informations générales sur le client, comme son crédit autorisé et le solde de son compte.  

## Voir aussi  
[Créer commande service](service-how-to-create-service-orders.md)   
[Créer des articles de service](service-how-to-create-service-items.md)   
[Services de planification](service-plan-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]