---
title: Déplacer des articles non planifiés dans les configurations de stockage de base
description: Cet article explique les mouvements internes non planifiés entre emplacements sans demande d’un document origine.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# Déplacer des articles en interne dans les configurations de stockage de base

Vous souhaiterez peut-être déplacer des articles entre emplacements sans demande d’un document origine. Par exemple, dans le cadre des activités suivantes :

* Réorganiser votre entrepôt.
* Apporter des articles à une zone d’inspection.
* Déplacer des articles supplémentaires vers et depuis une zone de production. 

Le mode de prélèvement des articles dépend de la configuration de l’entrepôt en tant que magasin. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans les configurations d’entrepôt où le bouton à bascule de configuration **Emplacement obligatoire** est activé, mais pas **Prélèvement et rangement dirigés**, vous pouvez enregistrer des mouvements non planifiés sur les pages suivantes :  

* Sur la page **Mouvement interne**.
* Sur la page **Feuille reclassement article**.  

## Mouvements internes

La page **Mouvements internes** vous permet de spécifier des lignes Prendre et Placer lorsqu’il n’y a pas de demande d’un document origine. La page Mouvement interne est comme une feuille de travail pour organiser les choses. Vous ne pouvez pas traiter le mouvement réel directement à partir de celle-ci. Lorsqu’une ligne est remplie, utilisez l’action **Créer un mouvement stock** pour envoyer la ligne à la page **Mouvement stock**, où vous traitez et enregistrez le mouvement.

### Pour déplacer des articles en tant que mouvement interne

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mouvements internes**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Assurez-vous que le champ **N°** du raccourci **Général** est rempli.
3. Dans le champ **Code magasin**, entrez le magasin où le mouvement a lieu.  

    Si le magasin est votre magasin par défaut en tant que magasinier, le code magasin est inséré automatiquement.  
4. Dans le champ **Code emplacement de destination**, entrez le code de l’emplacement vers lequel vous souhaitez déplacer les articles.

    Par exemple, en production, l’emplacement peut être l’emplacement atelier ouvert défini sur la fiche magasin ou dans le centre de charge.  
5. Dans le champ **Date d’échéance**, entrez la date à laquelle terminer le mouvement.  
6. Sur chaque ligne, renseignez les champs selon vos besoins. Les documents de mouvement interne comportent une ligne par mouvement. La ligne contient à la fois les actions prendre et placer.
7. Choisissez le champ **N° article** pour ouvrir la page **Liste des contenus emplacement**. Sélectionnez l’article à déplacer en fonction de sa disponibilité dans les emplacements. Vous pouvez également choisir l’action **Extraire contenu emplacement** pour remplir les lignes de mouvements internes en fonction de vos filtres.  

    Après avoir sélectionné l’article, le champ **Code emplacement de provenance** est automatiquement renseigné en fonction du contenu de l’emplacement sélectionné. Vous pouvez choisir n’importe quel emplacement où l’article est disponible. Les champs **N° article** et **Code emplacement de provenance** sont liés. La modification de la valeur d’un champ peut modifier la valeur de l’autre.  

    Le champ **Code emplacement de destination** est rempli avec la valeur que vous avez saisie dans l’en-tête. Vous pouvez le changer sur la ligne pour tout autre code emplacement qui n’est pas bloqué ou dédié à des fins particulières. Learn more at [Le champ Réservé](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Après avoir défini les emplacements depuis ou vers lesquels que vous souhaitez déplacer les articles, entrez la quantité à déplacer dans le champ **Quantité**.  

    > [!NOTE]  
    > La quantité doit être disponible dans l’emplacement spécifié dans le champ **Code emplacement de provenance**.  

9. Lorsque vous êtes prêt à traiter le mouvement, choisissez l’action **Créer mouvement de stock**.  

    > [!NOTE]  
    >  Après avoir créé le mouvement, les lignes de mouvement internes sont supprimées.  

Exécutez le reste du mouvement non planifié sur la page **Mouvement de stock** de la même manière que pour un mouvement basé sur des documents origine.

### Pour enregistrer le mouvement stock

1. Sur la page **Mouvement stock**, ouvrez le document pour lequel enregistrer le mouvement.  
2. Dans le champ **Code emplacement** sur les lignes mouvement, l’emplacement à partir duquel les articles doivent être prélevés est celui où les articles sont disponibles. Si nécessaire, vous pouvez modifier l’emplacement.
3. Exécutez le mouvement et saisissez les informations pour la quantité déplacée dans le champ **Quantité à traiter**. La valeur sur les lignes prélèvement et emplacement doit être la même. Sinon, vous ne pouvez pas enregistrer le mouvement.

    Si vous devez prélever les articles d’une ligne à partir de plusieurs emplacements, par exemple parce que la quantité totale n’est pas dans l’emplacement, utilisez l’action **Fractionner la ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.  
4. Sélectionnez l’action **Enregistrer mouvement de stock**.  

Voici ce qui se passe pendant le processus de validation :

* Les écritures magasin indiquent que la quantité est transférée des emplacements « prendre » vers les emplacements « placer ».

## Pour déplacer des articles avec la feuille reclassement article

Au lieu d’utiliser des documents de mouvement, vous pouvez enregistrer des mouvements en reclassant les codes d’emplacement sur les articles. Learn more at [Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Les mouvements validés avec des feuilles de reclassement ne rendent pas les documents de mouvement prêts pour le déplacement.  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille reclassement article**, puis choisissez le lien associé.  
2. Sur chaque ligne feuille, définissez les emplacements depuis et vers lesquels déplacer les articles en renseignant les champs **Code emplacement** et **Nouveau code emplacement**.  

    1. Pour déplacer tout le contenu d’un emplacement à un autre, choisissez l’action **Extraire contenu emplacement**.  
    2. Utilisez les filtres pour trouver l’emplacement qui contient les éléments que vous souhaitez déplacer, puis choisissez **OK**. Les lignes feuille sont renseignées avec le contenu de l’emplacement.  
3. Renseignez les autres champs de chaque ligne feuille.
4. Valider la feuille reclassement.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Voir la [formation Microsoft](/training/modules/manage-internal-warehouse-processes/) associée

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
