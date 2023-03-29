---
title: Configuration de gestion de prix
description: 'La gestion des prix de service vous permet de configurer des groupes de prix de service, la tarification des services, l’ajustement des prix de service, etc.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Configuration de gestion de prix
La fonctionnalité de gestion de la tarification des services vous permet d’appliquer le meilleur prix à des commandes service, de configurer des accords prix service personnalisés pour des clients, d’améliorer le rendement des salariés de la maintenance et d’accélérer le processus de facturation.  
  
La gestion de la tarification des services vous permet de configurer différents groupes tarifs service, pour pouvoir examiner l’article de service (ou le groupe articles de service), ainsi que le type de panne concerné par la tâche service. Vous pouvez configurer ces groupes pour une période de temps limitée ou pour un client ou une devise spécifique. Vous pouvez utiliser des structures de calcul de prix comme modèles pour affecter un prix particulier à une tâche service donnée.  
  
Par exemple, vous pouvez affecter des articles particuliers inclus dans le prix service, en complément du type de travail inclus. Vous pouvez également utiliser différents montants TVA et montants remise pour différents groupes tarifs service. Pour vous assurer que les prix corrects ont été appliqués, vous pouvez appliquer des prix fixes, minimums ou maximums en fonction des accords établis avec les clients.  
  
Avant d’ajuster le prix d’un article de service sur une commande service, un aperçu des résultats de l’ajustement du prix est fourni. Vous pouvez approuver ces résultats ou effectuer des changements supplémentaires si vous souhaitez obtenir un résultat différent. L’ajustement entier est effectué ligne par ligne, ce qui signifie qu’aucune ligne supplémentaire n’est créée.  
  
Pour finir, les statistiques de groupes tarifs service et les états standard vous permettent d’effectuer le suivi de la rentabilité de chaque groupe tarifs service.  
  
## Groupes ajustement prix service  
Vous utilisez les groupes ajustement prix service pour configurer différents types d’ajustement de prix pour des lignes service. Par exemple, vous pouvez configurer un groupe ajustement prix service qui ajuste des pièces de rechange, un groupe qui ajuste les prix pour la ressource, un autre qui ajuste les prix pour les coûts, etc. Vous pouvez également indiquer si l’ajustement de prix doit être appliqué à un article ou à une ressource spécifique uniquement, ou à tous les articles ou ressources.  
  
La fonction d’ajustement prix service ne s’applique pas aux articles de service dans les conditions suivantes :

* L’article appartient à des contrats de service. Vous pouvez ajuster uniquement les prix service des articles faisant partie d’une commande service. 
* Si l’article de service a une garantie. 
* Si la ligne service a été validée en tant que facture, en totalité ou en partie.  
  
Lorsque vous exécutez la fonction d’ajustement prix service, toutes les remises de la commande sont remplacées par les valeurs de l’ajustement prix service.  
  
## Groupes prix service  
Vous pouvez configurer des groupes tarifs service pour créer des groupes articles de service qui reçoivent le même tarif service spécial. Une fois que vous avez configuré des groupes tarifs service, vous pouvez ensuite les affecter à des articles de service sur des lignes article de service. Vous pouvez aussi affecter des groupes prix service aux groupes articles de service.  
  
Avant d’affecter un groupe tarifs service à un article de service, vous devez déterminer la zone panne, la devise ou le groupe ajustement prix service auquel s’applique le groupe tarifs service. Vous devez déterminer le montant auquel le prix service doit être ajusté et indiquer si ce montant doit inclure la TVA et les remises. Vous devez également déterminer si cet ajustement concerne un montant fixe ou s’il doit être appliqué uniquement sous certaines conditions.  
  
Lorsque vous affectez un groupe tarifs service à un article de service, tous les prix service spéciaux que vous avez configurés dans ce groupe s’appliquent pour cet article de service.  
  
## Tarification service  
Paramétrez les types de tarification service (prix et type d’ajustement prix) pour une combinaison de groupes prix service et de groupes prix client. Pour chaque type de tarification service, sélectionnez un groupe ajustement prix service. Vous pouvez aussi spécifier le type ajustement prix service (fixe, maximum ou minimum) et le prix réel.  
  
Par exemple, vous pouvez paramétrer les types de tarifications service d’un groupe tarifs service radio. Dans le cas de clients qui ne sont associés à aucun groupe prix, vous pouvez décider d’appliquer une tarification service impliquant le prix maximum sur la main-d’œuvre, qui est le groupe ajustement prix main-d’œuvre. Dans le cas de clients associés à un groupe prix précis, vous pouvez décider d’appliquer une tarification service avec un prix fixe sur la main-d’œuvre, e même groupe ajustement prix main-d’œuvre.  

#### [Expérience actuelle](#tab/current-experience)
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles de service**, puis choisissez le lien associé.  
2. Sélectionnez l’article de service, développez le raccourci **Prix et ventes**, choisissez l’action **Ressource**, **Article** ou **Compte général**.
3. Sur la page **Prix ressource projet**, **Prix article projet** ou **Prix compte général projet**, remplissez les champs selon vos besoins.

  
## Groupe ajustement prix service  
L’ajustement prix service vous permet d’ajuster le prix d’un article, d’une ressource, d’un compte général ou d’un coût sur une commande service.  
  
Une fois que vous avez entré un article sur la ligne article de service, vous entrez toutes les informations relatives aux coûts de cet article sur les lignes service. Lorsque vous exécutez la fonction Ajuster prix service, vous pouvez afficher un aperçu des ajustements prix. Vous pouvez effectuer des modifications, si nécessaire. Lorsque vous approuvez les modifications, les ajustements sont calculés, puis transférés aux lignes service. Vous validez ensuite la commande service.  
  
En fonction du type d’ajustement prix service, le montant total des ajustements est calculé.  
  
Le tableau suivant décrit les calculs.  
  
|Option | Désignation |  
|----------------------------------|---------------------------------------|  
|**Prix Fixe**|cela signifie que vous facturez un prix fixe pour l’article de service, la ressource, le compte général ou le coût, sans prendre en compte les coûts réels ou les frais ordinaires. Si vous sélectionnez cette option, l’ajustement prix service atteint le montant exact indiqué dans le groupe tarifs service.|  
|**Maximum**|Cela signifie que vous définissez une limite supérieure à la charge de votre client, indépendamment des coûts réels ou des frais ordinaires. La sélection de cette option signifie que l’ajustement prix service est effectué uniquement si le prix total dépasse le montant spécifié dans le groupe tarifs service.|  
|**Minimum**|Cela signifie que vous définissez une limite inférieure à la charge de votre client, quels que soient les coûts réels ou les frais ordinaires. La sélection de cette option signifie que l’ajustement prix service est effectué uniquement si le montant total est inférieur au montant spécifié dans le groupe tarifs service.|  
  
## Voir aussi  
[Configurer la tarification et les frais supplémentaires pour les services](service-how-setup-service-costs-pricing.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]