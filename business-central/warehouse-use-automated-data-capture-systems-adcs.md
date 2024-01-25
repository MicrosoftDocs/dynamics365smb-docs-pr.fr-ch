---
title: Utilisation de la base des systèmes de saisie automatisée (ADCS)
description: Apprenez à utiliser votre système de saisie automatique des données (ADCS) pour enregistrer le mouvement des articles dans l’entrepôt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814'
---
# <a name="use-automated-data-capture-systems-adcs-foundation"></a>Utilisation de la base des systèmes de saisie automatisée (ADCS)

> [!Important]
> La solution ADCS offre un moyen pour [!INCLUDE[prod_short](includes/prod_short.md)] de communiquer avec des appareils portables via des services Web. Vous devez travailler avec un partenaire Microsoft qui peut fournir le lien entre le service Web et l’appareil portable spécifique. 

Vous pouvez utiliser votre système de saisie automatisée pour enregistrer le mouvement des articles de l’entrepôt et certaines activités de la feuille, notamment les ajustements de quantité de la feuille article entrepôt et les inventaires. ADCS implique généralement la numérisation des codes à barres.

Pour utiliser votre système de saisie automatisée, vous devez attribuer un identifiant article à chaque article de l’entrepôt. Vous devez également configurer les écrans, fonctions de portable, échanges de données, et spécifier des paramètres pour les champs contrôlant l’ADCS. Vous spécifiez s’il faut utiliser l’ADCS sur la fiche magasin d’un entrepôt.

En fonction des besoins de votre entrepôt, définissez la quantité d’informations affichées sur le terminal de saisie portable lors de la configuration des écrans pour un terminal de saisie portable donné. Voici des exemples d’informations que vous pouvez afficher :  

- Données des tables dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple la liste des documents prélèvement à partir desquels l’utilisateur peut effectuer une sélection.  
- Trier les informations.  
- Messages affichant les confirmations ou erreurs sur les activités effectuées et enregistrées par l’utilisateur de périphérique mobile.

## <a name="to-enable-web-services-for-adcs"></a>Pour activer les services Web pour ADCS

Pour utiliser Automated Data Capture System, vous devez activer le service Web ADCS. Vous devez travailler avec un partenaire Microsoft qui peut implémenter un service Web pour ocnnecter ADCS et un appareil portable spécifique. Vous pouvez en savoir plus sur le service web pour ADCS en examinant les codeunit 7714 suivants : 
 
## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Pour configurer le module Gestion d’entrepôt

Pour utiliser le système de saisie automatisée, vous devez indiquer quels entrepôts utilisent cette technologie.  

> [!NOTE]  
> Il est recommandé de ne pas configurer un entrepôt pour utiliser la saisie automatisée si cet entrepôt utilise également une stratégie de capacité d’emplacement.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Emplacements**, puis choisissez le lien associé.
2. Sélectionnez l’entrepôt pour lequel vous souhaitez activer la saisie automatisée, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche magasin**, activez le bouton à bascule **Utiliser ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Pour spécifier un article pour utiliser votre système de saisie automatisée

À chaque article entrepôt que vous souhaitez utiliser avec le système de saisie automatisée doit être affecté un code d’identification pour le lier à son numéro. Par exemple, vous pouvez utiliser le code barre de l’article comme code d’identification. Un article peut également avoir plusieurs codes d’identification. Cela peut s’avérer utile dans le cas où un article est disponible dans plusieurs unités de mesure (par exemple, des pièces et des palettes). Dans ce cas, il convient d’affecter un code à chaque identifiant.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez un élément dans la liste qui fait partie de votre solution ADCS, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche article**, sélectionnez l’action **Identificateurs**.
4. Sur la page **Identifiants article**, sélectionnez l’action **Nouveau**.
5. Dans le champ **Code**, spécifiez l’identifiant de l’article. Par exemple, il peut s’agir du numéro de code-barres de l’article.  

    Vous pouvez également entrer un **code variante** et le code **unité de mesure**.  

6. Si nécessaire, entrez plusieurs codes pour chaque article.
7. Cliquez sur le bouton **OK**.  
8. Pour consulter les informations, choisissez le champ **Code identifiant** pour ouvrir la page **Identifiants article**.

## <a name="to-add-an-adcs-user"></a>Pour ajouter un utilisateur ADCS

Vous pouvez ajouter n’importe quel utilisateur à un système de saisie automatique. Dans ce cas, l’utilisateur doit fournir un mot de passe. Éventuellement, vous pouvez également indiquer une connexion qui identifie l’utilisateur ADCS en tant que magasinier. Le mot de passe de l’utilisateur du système ADCS peut être différent de son mot de passe de connexion. En savoir plus sur [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs ADCS**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Nom**, entrez un nom pour l’utilisateur. Le nom ne peut pas contenir plus de 20 caractères, espaces compris.  
4. Entrez un mot de passe dans le champ **Mot de passe**.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Pour spécifier qu’un magasinier est un utilisateur ADCS

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2. Si nécessaire, ajoutez un nouveau magasinier. Learn more at [Configurer des employés d’entrepôt](warehouse-how-to-set-up-warehouse-employees.md).  
3. Choisissez l’action **Modifier la liste**.  
4. Sélectionnez un magasinier dans la liste. Dans le champ **Utilisateur ADCS**, choisissez le nom d’un utilisateur ADCS dans la liste.  

> [!NOTE]  
> L’entrepôt par défaut du salarié doit utiliser la saisie automatisée.

## <a name="to-create-and-customize-miniforms"></a>Pour créer et personnaliser les écrans

Vous utilisez des écrans pour décrire les informations que vous souhaitez présenter sur un terminal de saisie portable. Par exemple, vous pouvez créer des écrans pour prendre en charge l’activité entrepôt de prélèvement des articles. Après avoir créé un écran, vous pouvez lui ajouter des fonctions pour les actions qu’un utilisateur effectue couramment avec des terminaux de saisie portables, par exemple, déplacer une ligne vers le haut ou vers le bas.  

> [!NOTE]
> Pour appliquer ou modifier la fonctionnalité d’une fonction d’écran, vous devez créer un codeunit pour le champ **Traité par Codeunit** pour exécuter l’action ou la réponse requise. Vous pouvez en savoir plus sur la fonctionnalité ADCS en examinant les codeunits suivants :
>
> * 7705
> * 7706
> * 7712
> * 7713  

### <a name="to-create-a-miniform-for-adcs"></a>Pour créer un écran de saisie automatisée

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écrans**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Code**, saisissez le code de l’écran. Entrez éventuellement des valeurs dans tous les autres champs.  

    Activez le bouton à bascule **Mettre à la volée l’écran** pour indiquer que l’écran est le premier formulaire que l’utilisateur voit à l’ouverture de session.  

4. Sur le raccourci **Lignes**, définissez les champs figurant sur l’écran. L’ordre dans lequel vous saisissez les lignes est celui dans lequel les lignes apparaîtront sur le terminal de saisie portable.  

Après avoir créé un écran, vous devez créer des fonctions et associer une fonctionnalité aux différentes entrées de clavier.  

### <a name="to-customize-miniform-functions"></a>Pour personnaliser les fonctions d’écran

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écrans**, puis choisissez le lien associé.  
2. Sélectionnez un écran dans la liste, puis sélectionnez l’action **Modifier**.  
3. Choisissez l’action **Fonctions**.  
4. Dans la liste déroulante **Code fonction**, sélectionnez le code pour représenter la fonction que vous souhaitez associer à l’écran. Par exemple, vous pouvez sélectionner **Échap** pour associer une fonctionnalité à la touche **Échap**.  

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
