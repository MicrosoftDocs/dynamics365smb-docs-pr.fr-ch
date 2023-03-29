---
title: "Procédure\_: créer des articles de service"
description: "Découvrez les différentes manières de créer des articles de service dans Business\_Central, par exemple dans une commande de service ou lors de l’expédition d’articles."
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# Créer des articles de service

Dans [!INCLUDE[prod_short](includes/prod_short.md)], le terme « article de service » fait référence à un équipement ou un article nécessitant une maintenance. Lorsque vous créez une commande service, vous spécifiez les articles nécessitant une maintenance. Dans la commande, vous pouvez lier un article de service à un article en stock ou à un groupe articles de service.    

Lorsque vous recevez un article nécessitant une maintenance, vous pouvez l’enregistrer en tant qu’article de service. Plusieurs méthodes sont possibles. Par exemple, vous pouvez créer un article de service sur la page **Articles de service**, ou dans le cadre d’un autre traitement, par exemple en utilisant une commande service.   

## Pour créer un article de service

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles de service**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Pour créer des articles de service dans des commandes service

Lorsque vous recevez des articles que vous souhaitez enregistrer comme articles de service, vous pouvez les créer en tant que tels sur la page **Commande service** ou **Devis service**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Choisissez l’action **Créer article de service**.  

    Un numéro est affecté à l’article de service et une fiche article de service est créée. Le champ **N° article de service** est rempli par le numéro du nouvel article de service.

## Pour créer un article de service lors de l’expédition d’articles

Si vous expédiez des articles en validant les commandes vente ou les factures vente, ces articles sont enregistrés automatiquement en tant qu’ articles de service si la condition suivante est remplie. Les articles doivent appartenir à un groupe articles de service et la case à cocher **Créer article de service** doit être activée. Si ces articles portent des numéros de série enregistrés sur la page Lignes traçabilité, cette information est copiée automatiquement dans le champ **N° de série** de la fiche article de service, lorsque les articles de service sont créés.  

La procédure suivante explique comment créer des articles de service lorsque vous expédiez des articles de commandes vente.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Ouvrez la commande vente appropriée.  
3. Sélectionnez l’action **Valider** ou **Valider et imprimer**.  
4. Choisissez l’action **Expédier** ou **Livrer et facturer**.  
5. Les articles de service sont automatiquement créés pour les articles de la commande pour autant qu’ils appartiennent à un groupe articles de service que vous avez configuré pour créer des articles de service. Si vous avez enregistré des numéros de série précis sur la page **Lignes traçabilité**, ceux-ci sont affectés à ces articles de service.  

> [!NOTE]  
>  Si un article est une nomenclature et que vous ayez éclaté cette nomenclature, les articles de la nomenclature éclatée sont traités comme des articles normaux. Des articles de service sont créés à partir des mêmes conditions (groupe articles de service et numéro de série). En outre, si le programme crée un article de service pour un article nomenclature éclatée composé d’autres composants nomenclature, ces articles sont créés comme composants d’article de service de l’article de service de la nomenclature éclatée.  
>   
>  Si un article est une nomenclature que vous n’avez pas éclatée, un article de service est créé à partir des mêmes conditions (groupe articles de service et numéro de série).  

## Pour insérer des frais forfaitaires pour un article service

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tâches service**, puis choisissez le lien associé.
2. Sélectionnez l’action **Feuille activité article**.
3. Choisissez la ligne service, puis sélectionnez **Actions**, **Fonctions**, puis l’action **Insérer frais forfaitaires**.  

    Une ligne service de type **Coût** est insérée avec les frais forfaitaires. Les frais forfaitaires s’appliquent à l’article de service sélectionné.

## Voir la [formation Microsoft](/training/modules/create-items/) associée

## Voir aussi

[Configurer les articles de service et les composants article de service](service-how-setup-service-items.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  
[Gestion des services](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
