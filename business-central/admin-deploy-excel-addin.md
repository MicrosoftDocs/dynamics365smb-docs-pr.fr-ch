---
title: Obtention du complément Business Central pour Excel
description: Découvrez comment fournir aux utilisateurs le complément Business Central pour Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-excel" />Obtenir le complément Business Central pour Excel

[!INCLUDE[prod_short](includes/prod_short.md)] inclut un complément pour Excel qui permet aux utilisateurs de sélectionner une action **Modifier dans Excel** sur certaines pages pour ouvrir les données dans une feuille de calcul Excel. Cette action est différente de l’action **Ouvrir dans Excel** car elle permet aux utilisateurs d’apporter des modifications dans Excel, puis de publier de retour les modifications dans [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview" />Aperçu

### <a name="about-the-add-in" />À propos du complément

Le complément s’appelle **Complément Office Microsoft Dynamics** et il est disponible pour l’installation à partir de l’[Office Store (AppSource)](https://appsource.microsoft.com/). Une fois le complément installé, l’action **Modifier dans Excel** est disponible sur la plupart des pages de liste et de liste partielle à l’aide de l’icône **Partager** ![Partager une page dans une autre application.](media/share-icon.png). Pour plus d’informations sur l’utilisation du complément, voir [Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md).

> [!NOTE]
> Le complément fonctionne uniquement sur Windows, pas sur macOS.

### <a name="about-deployment-as-an-admin" />À propos du déploiement en tant qu’administrateur

[!INCLUDE[prod_short](includes/prod_short.md)] en ligne comprend quelques options de déploiement pour fournir le complément aux utilisateurs. Une option est l’*acquisition individuelle*, où vous laissez les utilisateurs installer eux-mêmes le complément. Avec cette option, les utilisateurs doivent avoir accès au téléchargement de fichiers depuis l’Office Store. Une autre option consiste à configurer le *Déploiement centralisé* dans le centre d’administration de Microsoft 365 pour déployer automatiquement le complément sur l’ensemble de votre organisation, ou pour des groupes ou des utilisateurs spécifiques. Le déploiement centralisé fournit un moyen de mettre le complément à disposition des utilisateurs si votre organisation ne leur donne pas accès à l’Office Store.

Pour l’utilisateur final, l’expérience d’installation est différente dans les deux scénarios de déploiement :

- Avec l’acquisition individuelle, la première fois que l’utilisateur choisit l’action **Modifier dans Excel**, le volet **Nouveau complément Office** s’ouvre dans Excel. Pour installer le complément, l’utilisateur choisit **Faire confiance à ce complément**, ce qui a pour effet d’installer le complément directement depuis l’Office Store. L’utilisateur se connecte ensuite à [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide de son nom d’utilisateur et de son mot de passe.

- Avec le déploiement centralisé, la première fois que l’utilisateur choisit l’action **Modifier dans Excel**, le complément est automatiquement installé dans Excel à partir du déploiement centralisé, pas de l’Office Store. La seule chose que les utilisateurs ont à faire est de se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]

Avec ces deux options de déploiement, le complément est automatiquement configuré pour se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Une troisième option de déploiement est l’installation manuelle du complément directement à partir d’Excel. Avec cette option, l’utilisateur doit configurer le complément pour se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="a-nameswitchaswitching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around" /><a name="switch"></a>Passage de l’acquisition individuelle au déploiement Centralisé, ou inversement

Lorsque vous passez de l’acquisition individuelle du complément au déploiement centralisé, ou vice versa, les fichiers Excel créés par les utilisateurs avant la transition sont affectés. Après la transition, les utilisateurs peuvent toujours ouvrir toutes les feuilles de calcul Excel précédemment créées à l’aide de l’action **Modifier dans Excel** ou créés manuellement en configurant le complément Excel. Mais ils ne peuvent pas mettre à jour les données du fichier provenant de Business Central ni de transmettre les mises à jour à Business Central

Cette situation est causée par le fait que chaque fichier Excel se voit attribuer un identifiant de « complément ». Lors de la transition vers ou depuis le déploiement centralisé, un ID différent est attribué, de sorte que l’ID précédent est bloqué.

## <a name="preparation-on-premises-only" />Préparation (sur site uniquement)

[!INCLUDE[prod_short](includes/prod_short.md)] sur site nécessite que votre environnement soit configuré pour le complément. Si ce n’est pas le cas, l’action **Modifier dans Excel** ne sera pas disponible pour les utilisateurs. Pour plus d’informations, consultez [Configuration du complément Excel pour la modification des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) dans l’Aide pour les développeurs et les professionnels de l’informatique.

## <a name="deploy-the-add-in-by-using-centralized-deployment" />Déployer le complément à l’aide du déploiement centralisé

Le déploiement centralisé est une fonctionnalité du centre d’administration de Microsoft 365 que vous utilisez pour installer automatiquement des compléments dans les applications Office des utilisateurs, comme Excel. Pour vous aider dans le déploiement centralisé, [!INCLUDE[prod_short](includes/prod_short.md)] comprend la configuration assistée **Déploiement centralisé du complément Excel**.

### <a name="before-you-begin" />Avant de commencer

- Pour savoir comment empêcher les utilisateurs de réaliser des téléchargements à partir de l’Office Store, voir [Gérer les compléments dans le centre d’administration](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Vérifiez que le déploiement centralisé fonctionnera pour votre organisation. Pour plus d’informations, consultez [Déterminer si le déploiement centralisé des compléments fonctionne pour votre organisation](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Si vous passez de l’acquisition individuelle à une autre méthode, consultez [Passer de l’acquisition individuelle au déploiement centralisé](#switch)

> [!NOTE]
> L’activation du déploiement centralisé affecte les fonctionnalités qui utilisent le complément Excel, telles que l’action **Modifier dans Excel**. Cela n’a aucun effet sur les autres fonctionnalités et/ou autorisations liées à Excel et attribuées aux utilisateurs dans [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in" />Configurer le déploiement centralisé du complément

Vous travaillerez à la fois dans [!INCLUDE[prod_short](includes/prod_short.md)] et dans le centre d’administration de Microsoft 365.

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], sélectionnez l’![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Déploiement centralisé du complément Excel**, puis sélectionnez le lien associé.
2. Lisez les informations de la page **Configuration du complément Business Central pour Excel** et sélectionnez **Suivant**.
3. Connectez-vous au [Centre d’administration Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967), puis accédez à **Applications intégrées**<!--**Add-ins**-->.

    Effectuez les étapes suivantes pour configurer le complément à déployer à partir de l’Office Store : 
    1. Sélectionnez **Obtenir des applications** pour ouvrir l’Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Recherchez le **Complément Office Microsoft Dynamics**, puis sélectionnez **Obtenir maintenant**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Sur la page **Ajouter des utilisateurs**, spécifiez les utilisateurs pour lesquels vous souhaitez déployer le complément, puis sélectionnez **Suivant**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Examinez **Accepter les demandes d’autorisation**, puis sélectionnez **Suivant** > **Terminer le déploiement**.
    5. Attendez que la coche verte à côté de **Déployé** apparaisse pour le complément, puis sélectionnez **Terminé**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Le complément apparaît sur la page **Compléments**. Pour plus d’informations sur le déploiement de compléments dans le centre d’administration Microsoft 365, voir [Déployer des compléments dans le centre d’administration](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Revenez à la configuration assistée du **Déploiement centralisé du complément Excel** dans [!INCLUDE[prod_short](includes/prod_short.md)] et choisissez **Suivant**.
5. Activez **Utiliser le déploiement centralisé**, et choisissez **Terminer**.

    Si vous n’activez pas ce bouton à bascule, [!INCLUDE[prod_short](includes/prod_short.md)] obtiendra le complément directement depuis l’Office Store.

Une fois terminé, vous pouvez toujours modifier le déploiement dans le centre d’administration Microsoft 365, par exemple en affectant plus d’utilisateurs. Pour plus d’informations sur le déploiement de compléments dans le centre d’administration, voir [Déployer des compléments dans le centre d’administration](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Si vous avez plusieurs environnements, vous devez exécuter la configuration assistée du **Déploiement centralisé du complément Excel** sur chaque environnement pour lequel vous souhaitez utiliser le déploiement centralisé. Cependant, vous n’avez pas besoin de configurer à nouveau le déploiement centralisé dans Microsoft 365. La seule chose que vous avez à faire est d’activer le bouton à bascule **Utiliser le déploiement centralisé** dans la configuration assistée. 

> [!NOTE]
> Il peut s’écouler jusqu’à 24 heures avant que le complément ne se déploie automatiquement dans l’instance Excel des utilisateurs.

## <a name="a-nameinstallaindividual-acquisition-install-the-add-in-manually-for-your-own-use" /><a name="install"></a>Acquisition individuelle : installer le complément manuellement pour votre propre usage

Dans la plupart des cas, lorsque vous ouvrez Excel à partir de Business Central, le complément sera soit installé automatiquement pour vous, soit vous serez invité à l’installer. Cependant, il peut arriver que vous deviez installer manuellement le complément.

1. Ouvrez Excel, puis ouvrez n’importe quel classeur Excel.
2. Dans le menu **Insérer**, choisissez **Compléments** > **Obtenir des compléments**
3. Accédez à **Géré par l’administrateur** et cherchez **Complément Office Microsoft Dynamics**. Si vous l’y voyez, sélectionnez-le, puis choisissez **Ajouter**. Si vous ne le voyez pas, allez au **Store**, puis recherchez *Complément Office Microsoft Dynamics* et suivez les instructions à l’écran pour l’ajouter.

Lorsque le complément est installé, il apparaît sous forme de volet dans Excel. À présent, configurez la connexion.

### <a name="configure-the-business-central-connection" />Configurer la connexion Business Central

Si un utilisateur ne parvient pas à se connecter automatiquement, vous pouvez le débloquer en lui demandant de suivre ces étapes :

1. Dans le volet de complément **Microsoft Dynamics** dans Excel, choisissez **Ajouter des informations sur le serveur**. Si vous ne le voyez pas, choisissez le ![bouton Autres options dans Excel.](media/cogwheel.png) en haut pour ouvrir la boîte de dialogue des options. 
2. Pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, définissez **URL du serveur** sur `https://exceladdinprovider.smb.dynamics.com`. Pour [!INCLUDE[prod_short](includes/prod_short.md)] local, définissez l’URL du client web, comme `https://myBCserver/190`.
3. Sélectionnez **OK**, puis vérifiez que l’application se recharge.
4. À l’invite, connectez-vous à Business Central avec votre nom d’utilisateur et votre mot de passe.
5. En option, choisissez l’environnement et la société auxquels vous souhaitez vous connecter.

Le complément est maintenant connecté à [!INCLUDE [prod_short](includes/prod_short.md)] et vous pouvez modifier les données et publier les modifications dans [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in" />Préparer les appareils et le réseau pour le complément Excel

Les services réseau tels que les proxys ou les pare-feu doivent autoriser le routage entre tous les appareils clients sur lesquels le complément est installé et de nombreux points de terminaison de service. Pour obtenir la liste des points de terminaison, consultez [Préparation de votre réseau pour le complément Excel](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting" />Incident

Parfois, les utilisateurs rencontrent des problèmes avec le complément Excel. Cette section donne quelques conseils sur la façon de débloquer des utilisateurs dans certaines circonstances.

|Problème  |Solution ou contournement  |Commentaires  |
|---------|---------|---------|
|Le complément ne démarre pas <br><br>Par exemple, l’utilisateur reçoit le message "Avertissement de complément : ce complément n’est plus disponible." quand vous essayez d’utiliser le complément. Ce problème particulier peut se produire si le déploiement centralisé est correctement configuré, mais que l’accès n’a pas été attribué à l’utilisateur.|Vérifiez si le complément est déployé de manière centralisée. Sinon, vérifiez si l’utilisateur n’est pas autorisé à l’installer localement. | L’administrateur peut configurer Office de sorte que les utilisateurs ne puissent pas acquérir de compléments. Dans ces cas, l’administrateur doit déployer le complément de manière centralisée. Pour plus d’informations, consultez [Déployer des compléments dans le centre d’administration](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Les données ne se chargent pas dans Excel|Testez la connexion en ouvrant une autre liste dans Excel à partir de [!INCLUDE [prod_short](includes/prod_short.md)]. Sinon, ouvrez le classeur dans Excel dans un navigateur.|Si l’utilisateur a spécifié un nom de société contenant des caractères spéciaux, le complément ne peut pas se connecter. |
|Les données ne peuvent pas être republiées sur [!INCLUDE [prod_short](includes/prod_short.md)].|Testez la connexion en ouvrant le classeur dans Excel dans un navigateur. |Parfois, une extension peut bloquer le travail de publication. Si la page est étendue ou personnalisée, supprimez les extensions, puis réessayez.|
|Les dates sont fausses  |Excel peut afficher les heures et les dates dans un format différent de celui de [!INCLUDE [prod_short](includes/prod_short.md)]. Cette situation ne les rend pas erronées, et les données contenues dans [!INCLUDE [prod_short](includes/prod_short.md)] ne seront pas compromises.|         |
|Pour certaines pages de liste, la modification de plusieurs lignes dans Excel provoque systématiquement des erreurs. Cette situation peut se produire si des appels OData incluent des FlowFields et des champs hors de contrôle du répéteur.|Sur la page **Services web**, cochez les cases **Exclure les FlowFields non modifiables** et **Exclure les champs hors de contrôle du répéteur** pour la page publiée. La sélection de ces cases à cocher exclut les champs FlowFields et non modifiables du calcul de l’eTag. |Ces cases à cocher sont masquées par défaut. Pour les afficher sur la page **Services web**, utilisez la [personnalisation](/dynamics365/business-central/ui-personalization-user). |
|Les utilisateurs ne peuvent plus se connecter au complément. Lorsqu’ils essaient de se connecter, le processus s’arrête sans s’achever.| Ce problème peut être causé par une mise à jour que nous avons apportée au complément, en juillet 2022. Pour obtenir plus d’informations et un correctif, voir [Modifier la configuration du complément Excel pour prendre en charge la mise à jour de juillet 2022](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|S’applique à [!INCLUDE [prod_short](includes/prod_short.md)] sur site uniquement|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online" />Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users" />To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally" />To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics--business-centralindex" />Voir la [formation Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Utiliser Business Central](ui-work-product.md)  
[Améliorations de l’intégration d’Excel dans la 2e vague de lancement 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
