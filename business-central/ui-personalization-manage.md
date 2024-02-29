---
title: Personnalisation des pages pour les rôles
description: Découvrez comment personnaliser l’interface utilisateur d’un profil (rôle) de sorte que tous les utilisateurs de ce rôle voient un espace de travail personnalisé.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Personnalisation des pages pour les profils


Business Central fournit à la fois une [personnalisation](ui-personalization-user.md) pour les utilisateurs et une personnalisation pour les administrateurs. La personnalisation permet aux utilisateurs d’adapter leur espace de travail en ajustant les mises en page en fonction de leurs propres préférences. Les administrateurs peuvent personnaliser les dispositions de page pour un profil spécifique, en fonction des rôles ou départements, afin que tous les utilisateurs auxquels le profil est attribué voient la présentation de page personnalisée. Alors que la personnalisation permet aux utilisateurs d’afficher, masquer et déplacer des champs et des actions sur une page, la personnalisation offre des fonctionnalités supplémentaires. Par exemple, la personnalisation vous permet d’afficher les champs qui se trouvent dans la table source ou les tables d’extension de la page, mais qui ne sont pas définis sur l’objet de la page&mdash;ce qui n’est pas une personnalisation possible.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> L’utilisation professionnelle classique d’un profil est un rôle. Un profil est donc nommé *Profil (rôle)* dans l’interface utilisateur.

La personnalisation de la page commence à partir de la page **Profils (rôles)**, le point de départ de l’administrateur pour la gestion des profils d’utilisateurs sur des fiches de profil individuelles. Outre la personnalisation de la mise en page, vous pouvez contrôler divers autres paramètres pour les profils sur la page **Profil (rôle)** pour chaque profil. Pour plus d’informations, voir [Gérer les profils](admin-users-profiles-roles.md).

## Conditions préalables

- Votre compte Business Central doit disposer de l’ensemble d’autorisations **Gestion profil D365** ou d’autorisations équivalentes. 

   L’ensemble d’autorisations **Gestion profil D365** inclut l’autorisation d’exécution sur l’objet système **9026 Ajouter un champ à la table**. Si vous ne disposez pas de cette autorisation, vous n’êtes pas autorisé à ajouter des champs sur la page à moins qu’ils ne soient définis sur l’objet de la page. 

## Personnaliser les pages pour un profil

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Profils (Rôles)**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne du profil pour lequel vous souhaitez personnaliser des pages, puis sélectionnez l’action **Modifier**.
3. Choisissez l’action **Personnaliser les pages**.

    [!INCLUDE[prod_short](includes/prod_short.md)] ouvre un nouvel onglet de navigation pour le profil sélectionné avec la bannière **Personnalisation** activée. La bannière **Personnalisation** offre les mêmes fonctionnalités que la bannière **Personnalisation** disponible pour les utilisateurs.

4. Personnalisez les pages en fonction des besoins du rôle ou du service en question, comme le ferait un utilisateur lors de la personnalisation. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

    > [!NOTE]
    > Pour naviguer pendant la personnalisation, utilisez <kbd>Ctrl</kbd>+<kbd>Clic</kbd> sur une action si elle est mise en surbrillance par la pointe de la flèche.

5. Lorsque vous avez fini de modifier la mise en page sur une ou plusieurs pages, choisissez le bouton **Terminé** sur la bannière **Personnalisation**.
6. Fermez l’onglet du navigateur.

La personnalisation des pages est maintenant enregistrée pour le profil.

## Afficher tous les pages personnalisées pour un profil

Vous pouvez obtenir un aperçu des pages personnalisées pour un profil, par exemple pour planifier celles à personnaliser ou à supprimer.

- Sur la page **Profil (rôle)**, choisissez l’action **Gérer les pages personnalisées**.

Sur la page **Pages personnalisées**, vous pouvez supprimer les personnalisations et vous pouvez résoudre les problèmes en recherchant les problèmes potentiels.  

## Supprimer toutes les personnalisations d’un profil

Vous pouvez annuler toutes les personnalisations apportées à un profil. Les personnalisations introduites avec une extension et celles effectuées par un utilisateur ne sont pas supprimées. Vous pouvez supprimer toutes les personnalisations avec une autre action. Pour plus d’informations, voir [Pour supprimer toutes les personnalisations effectuées par un utilisateur](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Sur la page **Profil (rôle)** d’un profil personnalisé, choisissez l’action **Effacer les pages personnalisées**.

La disposition sur les pages du profil est réinitialisée sur celle par défaut.  

## Supprimer la personnalisation de pages spécifiques pour un profil

Vous pouvez supprimer des personnalisations de page individuelles effectuées pour un profil. Les personnalisations introduites avec une extension et celles effectuées par un utilisateur ne sont pas supprimées. Vous pouvez supprimer des personnalisations de pages spécifiques avec une autre action. Pour plus d’informations, voir [Pour supprimer des personnalisations pour des pages spécifiques](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Sur la page **Profil (rôle)**, choisissez l’action **Gérer les pages personnalisées**.
2. Sur la page **Pages personnalisées**, sélectionnez une ou plusieurs lignes pour les personnalisations de page que vous souhaitez supprimer, puis choisissez l’action **Supprimer**.

La disposition sur les pages sélectionnées reflète désormais les modifications que vous avez apportées.

## Ajouter un champ

Vous ajoutez des champs à la page à partir du volet **Ajouter un champ à la page**, que vous ouvrez en sélectionnant l’action **+ Champ** en mode personnalisation. Il est important de comprendre que le volet **Ajouter un champ à la page** est utilisé pour afficher les champs qui existent déjà&mdash;soit sur la page et ses tables sources,&mdash;mais sont actuellement cachés. Vous ne pouvez pas en créer de nouveaux.

Le volet **Ajouter un champ à la page** présente tous les champs pouvant être affichés sur la page. Les champs sont divisés dans les catégories suivantes, déterminées par la conception sous-jacente de la page elle-même, sa table source et ses extensions :

|Catégorie|Désignation|
|-|-|
|Champs de table ne figurant pas sur l’objet de page|Inclut les champs définis dans la table de base ou les tables d’extension, mais qui ne sont pas définis sur la page. L’info-bulle de ces champs inclut le libellé **Défini par la table**.<br><br>|
|Champs de page liés à une table|Inclut les champs définis dans la table de base ou les extensions de table et qui sont également définis sur la page comme étant affichés ou masqués. L’info-bulle de ces champs inclut le libellé **Défini par la page**.|
|Les champs de page qui ne sont pas liés à une table| Les champs qui sont uniquement définis sur la page, mais pas dans la table de base ou les tables d’extension. Ces champs sont généralement utilisés pour les variables ou les calculs. L’info-bulle de ces champs inclut le libellé **Défini par la page**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Utilisez le bouton de filtre au-dessus de la liste pour modifier la catégorie de champs présentant le volet **Ajouter un champ à la page**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Affiche le bouton de filtre dans le volet Ajouter un champ en mode personnalisation.":::
 
### Ajouter un champ de table ne figurant pas sur l’objet de page

Si vous souhaitez rendre un champ de table uniquement disponible sur une page pour les utilisateurs, vous devez d’abord l’ajouter à la page. Une fois que vous avez ajouté le champ, les utilisateurs peuvent choisir d’afficher ou de masquer le champ grâce à la personnalisation. Il existe plusieurs façons d’ajouter un champ.

- Une solution consiste à le faire glisser depuis le volet **Ajouter un champ à la page** à la position souhaitée.
- Une autre façon consiste à sélectionner le champ dans le volet pour afficher l’emplacement recommandé sur la page. Accédez ensuite à l’emplacement du champ sur les pages, sélectionnez la pointe de flèche, puis sélectionnez **Ajouter**. 

Une fois le champ ajouté, l’info-bulle du champ dans le volet **Ajouter un champ à la page** passe sur **Défini par la page**.

> [!NOTE]
> Le champ ajouté ne peut pas être modifié et ne peut pas être déverrouillé.

## Supprimer un champ

Si vous avez ajouté un champ de table qui ne figurait pas initialement dans l’objet de page, vous pouvez le supprimer à nouveau. Supprimer un champ est différent de le masquer. Lorsque vous masquez un champ, les utilisateurs peuvent toujours l’afficher sur leur espace de travail grâce à la personnalisation. Cependant, si vous supprimez un champ, celui-ci ne peut plus être affiché ou masqué par les utilisateurs. Si le champ est actuellement affiché sur l’espace de travail d’un utilisateur, il disparaît de son espace de travail lorsque vous le supprimez. 

Pour supprimer un champ, sélectionnez la pointe de flèche sur le champ dans la page, puis cliquez sur **Supprimer**. Si vous ne trouvez pas le champ, sélectionnez-le dans le volet **Ajouter un champ à la page** pour indiquer son emplacement masqué. 

> [!IMPORTANT]
> Supprimer un champ ne supprime pas les données stockées dans le champ ni ses tables sources. Cela supprime simplement le champ de la vue. 

## Verrouiller et déverrouiller la modification

La personnalisation vous permet de verrouiller (autoriser la modification) ou de déverrouiller la modification (empêcher la modification) de la plupart des champs d’une page. Pour verrouiller ou déverrouiller la modification, sélectionnez le champ sur la page, sélectionnez la pointe de flèche, puis sélectionnez **Verrouiller la modification** ou **Déverrouiller la modification**. Il est important de garder à l’esprit quelques règles concernant le verrouillage et le déverrouillage des champs :

- Les champs qui ne figuraient pas à l’origine sur l’objet de page, mais qui ont été ajoutés à la page par personnalisation sont toujours verrouillés et ne peuvent pas être déverrouillés à l’aide de la personnalisation ou de la personnalisation.
- La conception du champ peut également empêcher sa modification. Si le développeur AL a défini la [propriété modifiable](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) du champ sur `false`, celle-ci est toujours verrouillée et ne peut pas être déverrouillée.
- Il est important de noter que la fonction d’édition des verrous est destinée à contribuer à l’exactitude, à la cohérence et à la fiabilité des données. Il n’est pas destiné à garantir l’intégrité des données.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Informations et conseils importants 

- Tous les champs de la table ne peuvent pas être personnalisés à partir du volet **Ajouter un champ à la page**. Le développeur d’une table peut choisir d’empêcher l’affichage d’un champ lors de la personnalisation en définissant la [propriété AllowInCustomization](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) du champ sur `false`.
- Vous ne pouvez pas personnaliser une page en [mode d’analyse](analysis-mode.md). Le commutateur **Analyser** est désactivé. Si vous passez en mode personnalisation alors que la page est en mode analyse, le mode analyse est automatiquement désactivé. 
- Certaines pages comportent plusieurs champs de page qui correspondent à la même table source. Le volet **Ajouter un champ à la page** affiche tous ces champs de page indépendamment. Vous pouvez afficher, masquer ou déplacer ces champs indépendamment sans affecter les autres.
- Si une pièce ou un groupe est masqué, vous pouvez toujours identifier les champs masqués à l’intérieur de la pièce ou du groupe, mais vous ne pouvez pas ajouter, déplacer ou afficher les champs de la pièce ou du groupe tant qu’ils ne sont pas rendus visibles. 
## Voir aussi

[Personnalisation de votre espace de travail](ui-personalization-user.md)  
[Gestion des profils](admin-users-profiles-roles.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
