---
title: "Créer des états Power BI Desktop pour afficher des données Business\_Central | Microsoft Docs"
description: Vous pouvez rendre vos données disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l’état de votre activité.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 09/07/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="building-power-bi-reports-to-display--data"></a>Créer des états Power BI pour afficher des données [!INCLUDE [prod_long](includes/prod_long.md)]

Vous pouvez rendre vos données [!INCLUDE[prod_long](includes/prod_long.md)] disponibles sous forme de source de données dans Power BI Desktop et créer des rapports puissants sur l’état de votre activité.

Cet article aborde la prise en main de Power BI Desktop pour créer des états qui affichent des données [!INCLUDE[prod_long](includes/prod_long.md)].  Après avoir créé des états, vous pouvez les publier dans votre service Power BI ou les partager avec tous les utilisateurs de votre organisation. Une fois que ces états figurent dans le service Power BI, les utilisateurs configurés pour ce dernier peuvent alors afficher les états dans [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Mise en route

- Inscrivez-vous au service Power BI.

  Si vous ne vous êtes pas encore inscrit, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Au moment de votre inscription, utilisez votre adresse e-mail professionnelle et votre mot de passe.

- Téléchargez [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop est une application gratuite que vous installez sur votre ordinateur local. Pour plus d’informations, voir [Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Veillez à ce que les données que vous souhaitez dans le rapport soit disponible en tant que page API ou publiées en tant que service Web.

  Pour plus d’informations, consultez [Exposer les données via des pages API ou des services Web OData](admin-powerbi-setup.md#exposedata).

- Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, obtenez les informations suivantes :

  - L’URL OData pour [!INCLUDE[prod_short](includes/prod_short.md)].
  
    En règle générale, cette URL a le format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, par exemple `https://localhost:7048/BC190/ODataV4`. Si vous disposez d’un déploiement à plusieurs abonnés, incluez le client dans l’URL, par exemple `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Un nom d’utilisateur et une clé d’accès au service Web d’un compte [!INCLUDE[prod_short](includes/prod_short.md)].

    Pour obtenir des données depuis [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utilise l’authentification de base. Vous aurez donc besoin d’un nom d’utilisateur et d’une clé d’accès au service Web pour vous connecter. Le compte peut être votre propre compte utilisateur ou votre organisation peut avoir un compte spécifique à cette fin.

- Téléchargez le thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)] (facultatif).

  Pour plus d’informations, consultez [Utiliser le thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) dans cet article.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power BI Desktop

La première tâche dans le cadre de la création d’états consiste à ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power BI Desktop. Une fois connecté, vous pouvez commencer à créer l’état.

1. Lancez Power BI Desktop.
2. Sélectionnez **Extraire les données**.

    Si vous ne voyez pas **Extraire les données**, sélectionnez le menu **Fichier**, puis **Extraire les données**.
3. Sur la page **Extraire les données**, sélectionnez **Services en ligne**.
4. Dans le volet **Services en ligne**, effectuez l’une des étapes suivantes :

    - Pour se connecter à [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, sélectionnez **Dynamics 365 Business Central**, puis **Connecter**.
    - Pour se connecter à [!INCLUDE [prod_short](includes/prod_short.md)] sur site, sélectionnez **Dynamics 365 Business Central (local)**, puis **Connecter**.

5. Connectez-vous à [!INCLUDE [prod_short](includes/prod_short.md)] (une fois seulement).

    Si vous ne vous êtes jamais connecté à [!INCLUDE [prod_short](includes/prod_short.md)] depuis Power BI Desktop auparavant, vous êtes invité à vous connecter.

    - Pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, sélectionnez **Se connecter**, puis choisissez le compte pertinent. Utilisez le même compte que celui avec lequel vous vous êtes connecté(e) à [!INCLUDE [prod_short](includes/prod_short.md)]. Lorsque vous avez terminé, sélectionnez **Connecter**.

    - Pour [!INCLUDE [prod_short](includes/prod_short.md)] local, saisissez d’abord l’URL OData pour [!INCLUDE[prod_short](includes/prod_short.md)], puis sélectionnez **OK**. Puis, à l’invite, entrez le nom d’utilisateur et le mot de passe du compte à utiliser pour vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Dans la zone **Mot de passe**, entrez la clé d’accès au service Web. Lorsque vous avez terminé, sélectionnez **Connecter**.

    > [!NOTE]  
    > Une fois que vous êtes connecté(e) à [!INCLUDE[prod_short](includes/prod_short.md)], vous n’êtes plus invité(e) à vous connecter. [Comment modifier ou effacer le compte que j’utilise actuellement pour me connecter à Business Central depuis Power BI Desktop ?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Une fois connecté, Power BI se met en contact avec le service Business Central. La fenêtre **Navigateur** apparaît et affiche les sources de données disponibles pour les rapports de construction. Sélectionnez un dossier pour le développer et voir les sources de données disponibles. 

   Ces sources de données représentent tous les services web et les pages API que vous avez publiés à partir de [!INCLUDE [prod_short](includes/prod_short.md)]. Les sources de données sont regroupées par environnements et sociétés Business Central. Avec Business Central Online, **Navigateur** a la structure suivante :

    - **Nom de l’environnement**
      - **Nom de la société**
        - **API avancées**

          Ce dossier répertorie les pages API avancées publiées par Microsoft, comme les [API d’automatisation de Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) et [pages d’API personnalisées pour Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Les pages d’API personnalisées sont en outre regroupées dans des dossiers par propriétés [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) du code source de la page API.

        - **API standards v2.0**

          Ce dossier répertorie les pages API exposées par l’[API Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Services Web \(hérités)**

          Ce dossier répertorie les pages, les unités de code et les requêtes publiées en tant que services Web dans Business Central.

    > [!NOTE]
    > La structure de Business Central en local est différente, car elle ne prend pas en charge les pages API.

7. Sélectionnez la source ou les sources de données que vous souhaitez ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
8. Si vous souhaitez ajouter ultérieurement d’autres données Business Central, vous pouvez répéter les étapes précédentes.

Une fois les données chargées, elles s’affichent dans le volet de navigation à droite dans la page. À ce stade, vous êtes connecté(e) à vos données [!INCLUDE[prod_short](includes/prod_short.md)] et vous êtes prêt(e) à générer votre état Power BI.  

> [!TIP]
> Pour plus d’informations sur l’utilisation de Power BI Desktop, reportez-vous à [Mise en route avec Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Créer des états accessibles

Il est important de rendre vos états utilisables par autant de personnes que possible. Essayez de concevoir des états qui ne nécessitent aucune adaptation particulière pour répondre aux besoins spécifiques des différents utilisateurs. Assurez-vous que la conception permet aux utilisateurs de tirer parti des technologies d′assistance standard, comme les lecteurs d′écran. Power BI comprend diverses fonctionnalités d′accessibilité, des outils et des consignes pour vous aider à atteindre cet objectif. Pour plus d′informations, [Conception d′états Power BI pour l′accessibilité](/power-bi/create-reports/desktop-accessibility-creating-reports) dans la documentation Power BI.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Créer des états pour afficher les données associées à une liste

Vous pouvez créer des états qui s’affichent dans un Récapitulatif d’une liste [!INCLUDE [prod_short](includes/prod_short.md)]. Les états peuvent contenir des données sur l’enregistrement sélectionné dans la liste. La création de ces états est similaire à celle d’autres états, à la différence près que vous devez effectuer quelques actions pour vous assurer que les états s’affichent comme prévu. Pour plus d’informations, consultez [Création d’états Power BI pour afficher les données de la liste dans [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Utilisation du thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)] (facultatif)

Avant de générer votre état, il est préférable de télécharger et d’importer le fichier de thème [!INCLUDE [prod_short](includes/prod_short.md)]. Le fichier de thème crée une palette de couleurs afin de pouvoir établir des états avec le même style de couleur que les applications [!INCLUDE [prod_short](includes/prod_short.md)] sans avoir à définir des couleurs personnalisées pour chaque visuel.

> [!NOTE]
> Cette tâche est facultative. Vous pouvez toujours créer vos états, puis télécharger et appliquer le modèle de style ultérieurement.

### <a name="download-the-theme"></a>Télécharger le thème

Le fichier de thème est disponible sous forme de fichier json sur la galerie de thèmes de la communauté Microsoft Power BI. Pour télécharger le fichier de thème, procédez comme suit :

1. Accédez à la [galerie de thèmes de la communauté Microsoft Microsoft Power BI pour Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Sélectionnez la pièce jointe de téléchargement **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Importer le thème dans un état

Après avoir téléchargé le thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez l’importer dans vos états. Pour importer le thème, sélectionnez **Afficher** > **Thèmes** > **Parcourir les thèmes**. Pour plus d’informations, consultez [Power BI Desktop - Importer des thèmes d’état personnalisés](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Publier des états

Après avoir créé ou modifié un état, vous pouvez le publier dans votre service Power BI et le partager avec d’autres membres de votre organisation. Une fois publié, l’état apparaît dans Power BI. L’état est également disponible pour sélection dans [!INCLUDE[prod_short](includes/prod_short.md)].

Pour publier un état, sélectionnez **Publier** sur l’onglet **Accueil** du ruban ou du menu **Fichier**. Si vous êtes connecté au service Power BI, l’état est publié sur ce service. Sinon, vous êtes invité à vous connecter. 

## <a name="distribute-or-share-a-report"></a>Distribuer ou partager un état

Il existe plusieurs façons de transmettre des états à vos collègues et à d’autres personnes :

- Distribuez les états sous forme de fichiers .pbix.

    Les états sont stockés sur votre ordinateur sous forme de fichiers .pbix. Vous pouvez distribuer le fichier .pbix de l’état aux utilisateurs, comme n’importe quel autre fichier. Ensuite, les utilisateurs peuvent télécharger le fichier sur leur service Power BI. Voir [Télécharger des états à partir de fichiers](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Distribuer les états de cette manière signifie que l’actualisation des données des états sera effectuée individuellement par chaque utilisateur. Cette situation pourrait avoir un impact sur la performance [!INCLUDE[prod_short](includes/prod_short.md)].

- Partager l’état de votre service Power BI

    Si tu as une licence Power BI Pro, vous pouvez partager l’état avec d’autres, directement depuis votre service Power BI. Pour plus d’informations, consultez [Power BI - Partager un tableau de bord ou un état](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems"></a>Résolution des problèmes

### <a name="cannot-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>« Impossible d’insérer un enregistrement. L’intention de connexion actuelle est en lecture seule. » erreur de connexion à la page API personnalisée

> **S’APPLIQUE À :** Business Central Online

À compter de février 2022, les nouveaux rapports qui utilisent les données Business Central se connecteront par défaut à une réplique en lecture seule de la base de données Business Central. Dans de rares cas, selon la conception de la page, vous obtenez une erreur lorsque vous essayez de vous connecter et d’obtenir des données à partir de la page.

1. Lancez Power BI Desktop.
2. Sur le ruban, cliquez sur **Obtenir les données** > **Services en ligne**.
3. Dans le volet **Services en ligne**, sélectionnez **Dynamics 365 Business Central**, puis **Connecter**.
4. Dans la fenêtre **Navigateur**, sélectionnez le point de terminaison d’API à partir duquel vous souhaitez charger les données.
5. Dans le volet d’aperçu sur la droite, vous verrez l’erreur suivante :

   *Dynamics365BusinessCentral : Échec de la requête : le serveur distant a renvoyé une erreur : (400) Requête incorrecte. (Impossible d’insérer un enregistrement. L’intention de connexion actuelle est en lecture seule. CorrelationId : [...]) ».*

6. Sélectionner **Transformer les données** à la place de **Charger** comme vous le feriez normalement.
7. Dans **l’éditeur Power Query**, sélectionnez **Éditeur avancé** du ruban.
8. Dans la ligne qui commence par **Source =**, remplacez le texte suivant :

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   par :

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Cliquez sur **Terminé**.
10. Sélectionner **Fermer et appliquer** à partir du ruban pour enregistrer les modifications et fermer l’éditeur Power Query.

## <a name="see-also"></a>Voir aussi

[Activation de vos données métier pour Power BI](admin-powerbi.md)  
[Veille économique](bi.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
