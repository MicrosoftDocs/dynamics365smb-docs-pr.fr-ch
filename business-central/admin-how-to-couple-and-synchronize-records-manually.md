---
title: Couplage et synchronisation (contient une vidéo)
description: Synchroniser un mappage de table d’intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de la table Dynamics 365 Sales qui sont couplées.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# Couplage et synchronisation des enregistrements entre Dataverse et Business Central

Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] avec des enregistrements dans Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Le couplage d’enregistrements permet d’afficher les informations Dataverse depuis [!INCLUDE[prod_short](includes/prod_short.md)], et vice-versa. Le couplage vous permet également de synchroniser les données entre les enregistrements. Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.

> [!NOTE]
> Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l’action **Configurer le couplage**. Si l’action est disponible, les applications sont connectées.

## Exemple vidéo

Cette vidéo montre le couplage et la synchronisation de données dans le cadre d’une intégration avec [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Pour coupler un enregistrement  

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  

    Vous pouvez également ouvrir la page de liste et sélectionner l’enregistrement à coupler.  

2. Choisissez l’action **Configurer le couplage**.  
3. Renseignez les champs, puis cliquez sur **OK**.  

## Pour synchroniser un enregistrement unique  

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  
2. Choisissez l’action **Synchroniser maintenant**.  
3. Si un enregistrement peut être synchronisé dans une direction, sélectionnez l’option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK**.  

## Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]  

1. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l’enregistrement que vous souhaitez coupler. Par exemple, le formulaire Fiche Compte ou Fiche Contact.  
2. Choisissez l’action **[!INCLUDE[prod_short](includes/prod_short.md)]** dans le ruban pour ouvrir et coupler l’enregistrement automatiquement.

    > [!Note]
    > Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l’option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur Bidirectionnelle ou À partir de la table d’intégration sur la page **Mappage de table d’intégration** pour l’enregistrement. Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).     

## Pour coupler plusieurs enregistrements à l’aide du couplage par correspondance

Spécifiez les données à synchroniser pour une entité, telle qu’un client ou un contact, en couplant des enregistrements par correspondance. Affinez les correspondances en rendant la recherche sensible à la casse et en attribuant une priorité à chaque correspondance. Si aucune correspondance n’est trouvée, vous pouvez également spécifier que vous souhaitez créer l’entité dans Dataverse. Pour plus d’informations, accédez à [Personnaliser le couplage par correspondance](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Le processus de couplage basé sur les correspondances ignore les enregistrements qui sont déjà mis en correspondance. Pour inclure ces enregistrements lorsque vous exécutez le couplage basé sur les correspondances, découplez les enregistrements, puis réessayez. Pour en savoir plus sur le découplage des enregistrements, accédez à [Découpler des enregistrements](#uncoupling-records).

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.
2. Choisissez l’action **Couplage par correspondance**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Pour synchroniser plusieurs enregistrements  

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que les pages Clients ou Contacts.  
2. Sélectionnez l’enregistrement à synchroniser, puis l’action **Synchroniser maintenant**.  
3. Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l’option qui affiche la direction, puis cliquez sur **OK**.  

## Découplage des enregistrements

Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**. Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**.

## Voir aussi  

[Utiliser Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]