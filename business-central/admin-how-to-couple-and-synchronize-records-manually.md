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

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central" />Coupler et synchroniser les enregistrements entre Dataverse et Business Central

Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] avec des enregistrements dans Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Le couplage d’enregistrements permet d’afficher les informations Dataverse depuis [!INCLUDE[prod_short](includes/prod_short.md)], et vice-versa. Le couplage vous permet également de synchroniser les données entre les enregistrements. Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.

> [!NOTE]
> Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l’action **Configurer le couplage**. Si l’action est disponible, les applications sont connectées.

## <a name="video-example" />Exemple vidéo

Cette vidéo montre le couplage et la synchronisation de données dans le cadre d’une intégration avec [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record" />Pour coupler un enregistrement

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  

    Vous pouvez également ouvrir la page de liste et sélectionner l’enregistrement à coupler.  

2. Sélectionnez l’action **Configurer le couplage**.  
3. Renseignez les champs, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record" />Pour synchroniser un enregistrement unique

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  
2. Sélectionnez l’action **Synchroniser maintenant**.  
3. Si un enregistrement peut être synchronisé dans une direction, sélectionnez l’option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record-from-" />Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]

1. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l’enregistrement que vous souhaitez coupler. Par exemple, le formulaire Fiche Compte ou Fiche Contact.  
2. Sélectionnez l’action **[!INCLUDE[prod_short](includes/prod_short.md)]** dans le ruban pour ouvrir et coupler l’enregistrement automatiquement.

    > [!Note]
    > Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l’option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur **Bidirectionnelle** ou **À partir de la table d’intégration** sur la page **Mappage de table d’intégration** pour l’enregistrement. Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling" />Pour coupler plusieurs enregistrements à l’aide du couplage par correspondance

Spécifiez les données à synchroniser pour une entité, telle qu’un client ou un contact, en couplant des enregistrements par correspondance. Affinez les correspondances en rendant la recherche sensible à la casse et en attribuant une priorité à chaque correspondance. Si aucune correspondance n’est trouvée, vous pouvez également spécifier que vous souhaitez créer l’entité dans Dataverse. Pour plus d’informations, accédez à [Personnaliser le couplage par correspondance](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Le processus de couplage basé sur les correspondances ignore les enregistrements qui sont déjà mis en correspondance. Pour inclure ces enregistrements lorsque vous exécutez le couplage basé sur les correspondances, découplez les enregistrements, puis réessayez. Pour en savoir plus sur le découplage des enregistrements, accédez à [Découpler des enregistrements](#uncoupling-records).

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.
2. Sélectionnez l’action **Couplage par correspondance**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records" />Pour synchroniser plusieurs enregistrements

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que les pages Clients ou Contacts.  
2. Sélectionnez l’enregistrement à synchroniser, puis l’action **Synchroniser maintenant**.  
3. Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l’option qui affiche la direction, puis cliquez sur **OK**.  

## <a name="bulk-insert-and-couple-records" />Insertion en bloc et couplage d’enregistrements

Si vous avez un grand nombre d’entités Dataverse qui correspondent à des enregistrements dans [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez les insérer et les coupler en bloc. Par exemple, vous souhaiterez peut-être insérer et coupler des enregistrements en bloc lorsque vous configurez la synchronisation pour la première fois.

Vous utiliserez l’**assistant d’importation de données** dans le **centre d’administration Microsoft Power Platform**.

L’exemple suivant décrit comment insérer en masse et coupler des clients avec des comptes dans Dataverse. Suivez le même processus pour les autres types d’entités, telles que les fournisseurs, les articles et les ressources.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Ouvrir dans Excel** pour ouvrir les données client dans Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Pour mapper et importer des données vers l’entité **Compte** dans Dataverse, suivez les étapes décrites dans [Importer des données (tous les types d’enregistrement ) à partir de plusieurs sources](/power-platform/admin/import-data-all-record-types).  

    Si l’entité Compte a une colonne **bcbi_companyid**, lorsque vous mappez les colonnes de données, assurez-vous que l’importation attribue l’ID de société approprié dans la colonne pour chaque enregistrement importé. Pour trouver l’ID de société dans [!INCLUDE [prod_short](includes/prod_short.md)], procédez comme suit :

    1. Ouvrez la page **Mappages de table d’intégration**.
    2. Sélectionez le mappage **CLIENT**, puis **Modifier la liste**.
    3. Faites défiler vers la droite et sélectionnez le bouton de modification assistée :::image type="icon" source="media/assist-edit-icon.png" border="false"::: dans le champ **Filtre de table d’intégration**. Cela montre le filtre par défaut pour le mappage client, et il contient l’ID de la société. L’ID de la société est la première partie de la valeur. Ne copiez que cette partie et ignorez les 0. L’exemple suivant met en évidence la partie à copier.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Affiche la partie de l’ID de société à copier.":::

    > [!NOTE]
    > Tous les noms des entités Dataverse et des enregistrements Business Central ne correspondent pas. En fonction de ce que vous importez, vérifiez que les colonnes suivantes contiennent les valeurs suivantes après l’importation :
    >
    >* Pour les clients, la colonne **CustomerTypeCode** doit contenir **Client**.
    >* Pour les fournisseurs, la colonne **CustomerTypeCode** doit contenir **Fournisseurs**. 
    >* Pour les articles, la colonne **ProductTypeCode** doit contenir **Stock de vente**.
    >* Pour les ressources, la colonne **ProductTypeCode** doit contenir **Service**.
 
4. Après avoir importé des données dans l’environnement Dataverse, dans [!INCLUDE [prod_short](includes/prod_short.md)], suivez les étapes [Pour coupler plusieurs enregistrements à l’aide du couplage par correspondance](#to-couple-multiple-records-using-match-based-coupling) pour coupler les entités Dataverse avec les enregistrements [!INCLUDE [prod_short](includes/prod_short.md)]. 

## <a name="uncoupling-records" />Découplage des enregistrements

Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**. Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**.

## <a name="see-also" />Voir aussi

[Utiliser Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
