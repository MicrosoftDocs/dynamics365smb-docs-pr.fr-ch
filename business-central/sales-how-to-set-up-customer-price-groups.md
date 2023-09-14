---
title: Configurer des groupes tarifs client
description: Découvrez comment configurer des groupes tarifs client et créer des prix de vente pour ces groupes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: bholtorf
---

# <a name="set-up-customer-price-groups"></a>Configurer des groupes tarifs client
  
Vous pouvez affecter des prix de vente différents selon les groupes de clients que vous approvisionnez. C’est ce que l’on appelle des groupes tarifs client.

Avant de configurer des groupes tarifs client, vous devez décider de leur nombre et identifier les clients auxquels vous allez associer chacun d’eux.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>Comment créer des prix de vente pour un groupe de clients

Lorsque vous avez convenu du prix à appliquer à un groupe de clients pour certains articles, enregistrez l’accord relatif à chaque article sur les lignes de la page **Prix vente**.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Pour créer des prix de vente pour un groupe de clients

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes tarifs clients**, puis sélectionnez le lien associé.  

2. Sélectionnez la ligne pour le groupe tarifs client. Si une ligne n’existe pas déjà, vous pouvez en créer une nouvelle. Sélectionnez **Nouveau** pour créer une nouvelle entité et lui donner un nom.  
    
    Pour la ligne sélectionnée, vérifiez le contenu des champs **Autoriser remise ligne**, **Autoriser remise facture**, **Prix incluant la taxe** et **Gpe compta. marché TVA (prix)**. 
  
3. Sélectionnez l’action **Naviguer** et choisissez **Prix vente**. La page **Prix vente** s’affiche. Le champ **Type de vente** sera rempli avec le **Groupe tarifs client**.  
  
4. Remplissez le **Code vente** avec le code vente que vous avez sélectionné à la page précédente.  
  
5. Dans les champs des différentes lignes, indiquez le **Numéro article**, le **Code unité** et le **Prix unitaire** établi. Vous pouvez également afficher la colonne **Code variante** et spécifier le **code variante** s’il existe plusieurs variantes de l’article.  
  
6. Si le groupe de clients doit acheter une quantité minimum pour pouvoir bénéficier du prix convenu, renseignez le champ **Quantité minimum**.  

7. Si nécessaire, saisissez la **Date début** et la **Date fin** de l’accord de prix.  
  
8. Au besoin, vous pouvez spécifier le **code devise**.

Répétez les étapes 4 à 8 pour chacun des articles pour lesquels vous souhaitez créer un prix de vente.

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>Comment entrer des codes groupe tarifs client sur des fiches client

Une fois ces groupes tarifs client définis, vous pouvez entrer les codes correspondants sur les fiches client.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Pour entrer des codes groupe tarifs client sur une fiche client

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  

2. Ouvrez la **fiche client** correspondant au client que vous voulez associer à un groupe tarifs client.  

3. Sur le raccourci **Facturation**, dans le champ **Groupe tarifs client**, sélectionnez le code **Groupe tarifs client**.  


## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Enregistrer les prix de vente spéciaux et les remises](sales-how-record-sales-price-discount-payment-agreements.md)  
[Configuration des groupes remises client](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
