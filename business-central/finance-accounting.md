---
title: "Expériences de comptables dans Business\_Central (contient une vidéo)"
description: En savoir plus sur le Tableau de bord Comptable pour le Hub Entreprise qui prennent en charge les comptables internes et externes de la société du client.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 10/19/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="accountant-experiences-in-"></a>Expériences de comptable dans [!INCLUDE[prod_long](includes/prod_long.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Chaque entreprise doit tenir ses comptes et valider sa comptabilité. Certaines sociétés utilisent un comptable externe, et d’autres ont un comptable dans le personnel. Peu importe le type de comptable que vous êtes, vous pouvez utiliser le tableau de bord **Comptable** comme pages d’accueil de [!INCLUDE[prod_short](includes/prod_short.md)]. De là, vous pouvez accéder à toutes les pages nécessaires pour votre travail.  

## <a name="accountant-role-center"></a>Tableau de bord Comptable

Le tableau de bord est un tableau de bord avec des vignettes d’activité qui affichent des chiffres essentiels en temps réel et vous permettent d’accéder rapidement aux données. Dans le ruban en haut de la page, vous avez accès à plusieurs actions, par exemple ouvrir les états et les états financiers les plus couramment utilisés dans Excel. Dans la barre de navigation supérieure, vous pouvez rapidement basculer entre les listes que vous utilisez le plus fréquemment. Ici, vous pouvez visualiser d’autres éléments, tels que **Documents validés** avec divers types de documents que la société a validés.  

Si vous débutez avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez lancer une liste de vidéos depuis votre Tableau de bord. Vous pouvez également lancer une visite de **Mise en route** qui précise des domaines clé.  

## <a name="company-hub"></a>Hub Entreprise

Si vous travaillez dans plusieurs entreprises [!INCLUDE [prod_short](includes/prod_short.md)], vous trouverez peut-être utile d’utiliser la page **Hub Entreprise** pour suivre votre travail.  Pour plus d’informations, voir [Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Inviter votre comptable externe dans votre [!INCLUDE[prod_short](includes/prod_short.md)]

Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, votre administrateur peut l’inviter à votre [!INCLUDE[prod_short](includes/prod_short.md)] afin qu’il puisse travailler avec vous sur vos données fiscales. [!INCLUDE[prod_short](includes/prod_short.md)] comprend trois licences de type Comptable externe. Pour plus d’informations sur la gestion des licences, téléchargez le [Guide des licences Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=866544).

Une fois que votre comptable a accédé à votre [!INCLUDE[prod_short](includes/prod_short.md)], il peut utiliser le tableau de bord **Comptable** qui donne un accès facilité aux pages les plus appropriées pour son travail. Ils peuvent également utiliser le Hub Entreprise de leur propre [!INCLUDE [prod_short](includes/prod_short.md)] pour gérer leur travail. Pour plus d’informations, voir [Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Nous avons simplifié pour vous la façon d’inviter votre comptable externe. Ouvrez simplement la page **Utilisateurs**, puis choisissez l’action **Inviter un comptable externe** dans le ruban. Un e-mail est préparé pour vous afin de vous permettre d’ajouter l’e-mail professionnel de votre comptable et d’envoyer l’invitation.  

> [!Note]  
> Pour cela, il faudrait que vous ayez configuré la messagerie SMTP. Pour plus d’informations, voir [Configurer la messagerie](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> L’adresse électronique du comptable doit être une adresse professionnelle basée sur Microsoft Entra ID. Si le comptable utilise un autre type d’adresse électronique, l’invitation ne peut pas être envoyée.
>
> Cette tâche nécessite un accès à la gestion des utilisateurs et des licences dans Microsoft Entra ID. L’utilisateur qui envoie cette invitation doit se voir attribuer le rôle **Administrateur général** ou **Administrateur utilisateur** dans le centre d’administration Microsoft 365. Pour plus d’informations, voir [À propos des rôles d’administrateur](/microsoft-365/admin/add-users/about-admin-roles) dans le centre d’administration Microsoft 365.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Ajout de votre comptable à votre Microsoft 365 dans le Portail Azure

Si votre administrateur ou partenaire revendeur ne souhaite pas utiliser le guide **Inviter un comptable externe**, il peut ajouter un utilisateur externe dans le Portail Azure et attribuer à cet utilisateur la licence *Comptable externe*. Pour plus d’informations, voir [Démarrage rapide : Ajouter des utilisateurs invités à votre annuaire dans le portail Azure](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Pour ajouter votre comptable en tant qu’utilisateur invité

1. Ouvrez le [Portail Azure](https://portal.azure.com/).
2. Dans le volet gauche, sélectionnez **Microsoft Entra ID**.
3. Sous **Gérer**, sélectionnez **Utilisateurs**.
4. Sélectionnez **Nouvel utilisateur invité**.
5. Sur la page **Nouvel utilisateur**, sélectionnez **Inviter un utilisateur**, puis ajoutez des informations sur votre comptable externe.  

   Vous pouvez éventuellement inclure un message de bienvenue personnel à l’attention du comptable pour l’informer que vous l’ajoutez à votre [!INCLUDE[prod_short](includes/prod_short.md)].

6. Sélectionner **Inviter** pour envoyer automatiquement l’invitation. Une notification apparaît en haut à droite avec le message **Utilisateur invité avec succès**. 
7. Après avoir envoyé l’invitation, le compte utilisateur est automatiquement ajouté au répertoire en tant qu’invité.

Ensuite, vous devez attribuer au nouvel utilisateur invité une licence pour [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-"></a>Pour donner à votre comptable accès à votre [!INCLUDE[prod_short](includes/prod_short.md)]

1. Dans le Portail Azure, pour le nouvel utilisateur ajouté, choisissez **Profil**, puis **Modifier**
2. Mettez à jour le champ **Lieu d’utilisation** et indiquez le pays/région concerné, puis choisissez **Enregistrer**.
3. Choisissez **Licences**, puis ouvrez **Affectations**.
4. Choisissez la licence **Comptable externe Dynamics 365 Business Central**.  
    
    Si cette licence n’est pas disponible, contactez votre revendeur pour ajouter la licence à votre abonnement.

    Plus précisément à des fins d’évaluation dans un locataire d’essai, vous pouvez utiliser une licence **Dynamics 365 Business Central for IW** disponible à la place. Cependant, vous ne pouvez pas utiliser ce type de licence si vous avez déjà acheté [!INCLUDE[prod_short](includes/prod_short.md)]. 
5. Enregistrez l’affectation.

En cas de réussite, la licence est attribuée à l’utilisateur invité et le compte invité est créé.

### <a name="importing-the-new-user-into-"></a>Importation du nouvel utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)]

Le comptable recevra un e-mail l’informant que l’accès à votre Microsoft Entra ID lui a été fourni. Ensuite, vous devez lui donner accès à la bonne société dans [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Pour ajouter le comptable à la bonne société

1. Ouvrez la société [!INCLUDE[prod_short](includes/prod_short.md)] à laquelle vous souhaitez donner accès au comptable sur [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.  
3. Choisissez l’action **Obtenir de nouveaux utilisateurs à partir de Microsoft 365**.

Cela a pour effet d’importer dans la société le compte utilisateur que vous avez créé dans le portail Azure. Pour plus d’informations, voir [Pour ajouter un utilisateur dans Business Central](ui-how-users-permissions.md#adduser).  

Si vous souhaitez donner accès à plusieurs sociétés, vous devez vous connecter à chaque société et répéter ce processus. Vous pouvez également mettre à jour les groupes d’autorisations pour le profil utilisateur du comptable dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple en lui attribuant le groupe d’utilisateurs *D365 Bus Premium*. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utiliser les axes analytiques](finance-dimensions.md)  
[Analyse des états financiers dans Excel](finance-analyze-excel.md)  
[Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configuration d’une analyse de trésorerie](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
