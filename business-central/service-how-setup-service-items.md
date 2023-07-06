---
title: Articles de service et composants article de service
description: 'Découvrez les éléments que vous devez configurer avant de pouvoir utiliser des articles de service, notamment les valeurs par défaut telles que le délai de réponse et le groupe tarifs service.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-service-items-and-service-item-components"></a><a name="set-up-service-items-and-service-item-components"></a><a name="set-up-service-items-and-service-item-components"></a>Configurer les articles de service et les composants article de service
Pour utiliser les articles de service, vous devez configurer

* les groupes articles de service suivants.
* En option

## <a name="to-set-up-service-item-groups"></a><a name="to-set-up-service-item-groups"></a><a name="to-set-up-service-item-groups"></a>Pour configurer des groupes articles de service
Vous pouvez configurer les groupes articles relatifs à la réparation et à la maintenance. Vous pouvez définir des valeurs par défaut des articles de service d’un groupe articles de service, telles que le délai de réponse, le pourcentage remise contrat et le groupe tarifs service. Dans le cas d’articles appartenant à un groupe articles de service, ceux-ci peuvent être, à votre demande, enregistrés automatiquement en tant qu’articles de service lorsqu’ils sont vendus.  

Vous pouvez affecter des groupes articles de service à des articles sur la fiche **Article** et à des articles de service sur la fiche **Article de service**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes articles de service**, puis sélectionnez le lien associé.  
2. Créez un groupe articles de service.  
3. Renseignez les champs **Code** et **Désignation**.  
4. Dans le champ **% remise contrat par défaut**, saisissez le pourcentage remise contrat par défaut que vous souhaitez attribuer aux articles de service du groupe.  
5. Dans le champ **Code gpe tarifs serv. par déf**, saisissez le code groupe tarifs service par défaut à attribuer aux articles de service du groupe.  
6. Dans le champ **Délai de réponse par déf. (heures)**, saisissez le délai de réponse par défaut (en heures) que vous souhaitez attribuer aux articles de service du groupe.  
7. Sélectionnez le champ **Créer article de service** si vous souhaitez enregistrer les articles du groupe en tant qu’articles de service lorsqu’ils sont vendus.  

## <a name="to-set-up-service-item-components"></a><a name="to-set-up-service-item-components"></a><a name="to-set-up-service-item-components"></a>Pour configurer des composants article de service
Un article de service peut être constitué de plusieurs composants pouvant être remplacés par des pièces de rechange lors de la maintenance de l’article. Vous pouvez configurer ces composants dans la page **Liste composants art. service**. En outre, si vous souhaitez configurer des composants pour des articles de service qui sont des nomenclatures, vous pouvez copier les articles de nomenclature et les créer en tant que composants article de service.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles de service**, puis choisissez le lien associé.
2. Ouvrez l’article de service pour lequel vous voulez configurer des composants.  
3. Sélectionnez l’action **Composants**. La page **Liste composants art. service** s’ouvre.  
4. Ajouter un nouveau composant.  
5. Dans le champ **Type**, choisissez **Article de service** si le composant est lui-même un article de service enregistré. Sinon, choisissez **Article**.  
6. Dans le champ **N°**, choisissez l’article ou l’article de service qui est un composant de l’article de service.  

## <a name="to-set-up-service-item-components-from-a-bom"></a><a name="to-set-up-service-item-components-from-a-bom"></a><a name="to-set-up-service-item-components-from-a-bom"></a>Pour configurer des composants article de service à partir de nomenclatures
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles de service**, puis choisissez le lien associé.  
2. Ouvrez l’article de service pour lequel vous voulez configurer des composants à partir d’une nomenclature.  
3. Sélectionnez l’action **Composants**. La page **Liste composants art. service** s’ouvre.  
4. Choisissez l’action **Copier à partir de nomenclature**.  

    Si l’article auquel est lié l’article de service est une nomenclature, les composants pour tous les articles de la nomenclature sont créés automatiquement.  

## <a name="to-set-up-a-service-shelf"></a><a name="to-set-up-a-service-shelf"></a><a name="to-set-up-a-service-shelf"></a>Pour configurer un rayon service
Vous pouvez configurer des rayons service qui identifient l’emplacement de stockage de vos articles de service. Vous pouvez affecter des rayons service à des articles de service dans les pages **Commande service** et **Feuille activité article de service**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rayons service**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Configurer des codes prestations standards](service-how-setup-service-coding.md)   
[Configurer les processus incident](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
