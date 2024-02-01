---
title: Configurer la tarification et les coûts des services
description: 'Découvrez comment utiliser les fonctions de tarification pour configurer et personnaliser votre application afin d’appliquer et d’ajuster la tarification des articles de service, réparations et commandes.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-pricing-and-additional-costs-for-services"></a>Configurer la tarification et les frais supplémentaires pour les services
Les fonctions de tarification de [!INCLUDE[prod_short](includes/prod_short.md)] permettent de configurer et de personnaliser votre application afin d’appliquer et d’ajuster la tarification des articles de service, réparations et commandes. Les décisions en matière de tarification sont alors facilement transmises au processus de facturation.  
  
Selon les besoins de votre installation, vous pouvez configurer les groupes de prix et les mapper à des périodes, clients ou devises spécifiques. Vous pouvez configurer le tarif fixé, minimal, ou maximal, selon les contrats service établis avec les clients. Enfin, tandis que vous ajustez vos prix, vous pouvez consulter et approuver les modifications avant de les valider en comptabilité.  

## <a name="to-set-up-a-service-price-group"></a>Pour configurer des groupes tarifs de service
Vous pouvez configurer des groupes contenant des articles de service qui doivent recevoir le même tarif service spécial. Vous pouvez affecter des groupes prix service à des articles de service sur les lignes article de service. Vous pouvez aussi affecter des groupes prix service aux groupes articles de service.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes prix de service**, puis sélectionnez le lien associé.  
2. Créez un groupe tarifs service.  
3. Renseignez les champs **Code** et **Désignation**.  
4. Sélectionnez l’action **Configuration**.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Les champs **Type ajustement** et **Montant** fonctionnent ensemble pour spécifier si un ajustement concerne un montant fixe ou s’il s’applique uniquement lorsque le prix service total est supérieur ou inférieur au montant du champ **Montant**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Pour configurer un groupe ajustement prix service
Vous pouvez configurer les groupes ajustement prix afin d’ajuster la tarification service des articles de service. Par exemple, vous pouvez configurer des groupes ajustement prix qui ajustent le prix du fret ou des pièces de rechange.  
  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes ajustement prix de service**, puis sélectionnez le lien associé.  
2. Créez un groupe ajustement prix service.  
3. Renseignez les champs **Code** et **Désignation**.  
4. Dans le champ **Type**, saisissez le type de l’écriture que vous voulez ajuster.  
  
    * Pour ajuster une écriture spécifique, saisissez le numéro de cette écriture dans le champ **N°** . Lorsque vous laissez ce champ vide, le groupe ajustement ajuste toutes les écritures du type défini dans le champ **Type**.  
    * Pour ajuster les prix service associés à un service spécifique, renseignez le champ **Type travail**. Lorsque vous laissez ce champ blanc, il sera ignoré.  
  
5. Dans le champ **Désignation**, entrez une description brève de l’ajustement prix service.  
6. Pour ajuster les prix de service associés à un groupe comptabilisation produit spécifique, renseignez le champ **Groupe compta. produit**.

> [!Tip]
> Vous pouvez choisir **Détails** pour ajouter des informations supplémentaires sur le groupe ajustement. Par exemple, vous pouvez spécifier l’article qui appartient au groupe ajustement prix service, et s’il s’agit d’un article, une ressource, un groupe ressources ou des frais forfaitaires.  

## <a name="to-set-up-additional-costs-for-services"></a>Pour configurer des frais supplémentaires pour les services
Lorsque vous utilisez des articles de service et des commandes service, vous devrez peut-être enregistrer des frais supplémentaires, tels que les frais de déplacement vers des zones de service spécifiques ou les frais forfaitaires. Lorsque vous créez une commande service, vous pouvez insérer ces coûts, et une ligne avec le type **Coût** sera ajoutée à la commande. Sinon, si vous souhaitez appliquer le coût à toutes les commandes service, vous pouvez configurer un coût par défaut. Par exemple, si vous souhaitez toujours appliquer des frais forfaitaires.
  
### <a name="to-set-up-service-costs"></a>Pour configurer des coûts service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Coûts de service**, puis choisissez le lien associé. 
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Pour spécifier un coût par défaut pour les commandes service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres services**, puis choisissez le lien associé. 
2. Dans le champ **Frais forfait. commande service**, sélectionnez le coût service approprié.

## <a name="see-also"></a>Voir aussi
[Paramétrage de la gestion des services](service-setup-service.md)  
[Gestion des services](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
