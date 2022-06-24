---
title: Extension de gestion du groupe TVA pour le Royaume-Uni
description: Vous pouvez vous engager avec d’autres entreprises pour former un groupe TVA où tous les membres déclarent la TVA dans une seule déclaration.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841935"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Extension de gestion du groupe TVA pour le Royaume-Uni

Vous pouvez connecter une ou plusieurs entreprises de votre pays pour combiner la déclaration de TVA sous un numéro d’enregistrement unique. Ce type d’arrangement est connu sous le nom de *Groupe TVA*. Vous pouvez vous engager avec le groupe en tant que membre ou société représentante du groupe.

## <a name="forming-a-vat-group"></a>Formation d’un groupe TVA
Les membres du groupe TVA et la société représentante du groupe peuvent utiliser le guide de configuration assisté **Configuration de la gestion des groupes TVA** pour définir leur engagement avec le groupe et créer une connexion entre leurs locataires [!INCLUDE[prod_short](includes/prod_short.md)]. Les membres du groupe utiliseront la connexion pour soumettre leurs déclarations de TVA à la société représentante du groupe. La société représentante utilisera une seule déclaration de TVA pour soumettre la TVA aux autorités fiscales pour le groupe. 

## <a name="license-requirements"></a>Licences requises
Les participants du groupe doivent être autorisés à utiliser [!INCLUDE[prod_short](includes/prod_short.md)]. Vous ne pouvez pas utiliser de comptes d’invité dans les groupes TVA. 

* Pour calculer et soumettre des déclarations de TVA, un utilisateur doit être un utilisateur complet de Business Central.
* La licence Team Member Dynamics 365 Business Central vous permet de vous connecter et d’effectuer des tâches de base, telles que la création de comptes.

## <a name="vat-group-constellations"></a>Constellations du groupe TVA
La communication se fait entre les membres du groupe et la société représentante. La société représentante du groupe expose une URL d’API qui permet aux membres de soumettre leurs déclarations de TVA à la société représentante du groupe TVA. 
[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les déclarations de TVA inter-groupes pour les entreprises utilisant [!INCLUDE[prod_short](includes/prod_short.md)] sur site ou en ligne, et dans n’importe quelle combinaison. La configuration de la communication dépend de la constellation. Cet article décrit diverses constellations de groupes.

La liste suivante montre l’ordre recommandé des étapes de configuration d’un groupe TVA :

1. Créez la configuration dans Azure Active Directory. Pour plus d’informations, voir [Configuration requise pour l’authentification](ui-extensions-vat-group.md#requirements-for-authentication).
2. Partagez les informations techniques dont les membres du groupe TVA et la société représentante ont besoin pour connecter leur locataires [!INCLUDE[prod_short](includes/prod_short.md)]. Habituellement, la société représentante du groupe TVA dispose de ces informations, telles que le nom de l’environnement de la société représentante du groupe TVA auquel les membres du groupe TVA soumettront la TVA.
3. Créez des utilisateurs que les membres du groupe TVA peuvent utiliser pour s’authentifier lorsqu’ils se connectent au [!INCLUDE[prod_short](includes/prod_short.md)] de la société représentante du groupe TVA. Les utilisateurs doivent disposer de licences d’utilisation complètes pour [!INCLUDE[prod_short](includes/prod_short.md)].
4. Exécutez le guide de configuration assistée **Configurer la gestion des groupes TVA** pour connecter les membres du groupe TVA.

  Le guide requiert certaines informations de la société représentante du groupe TVA. Pour plus d’informations, voir [Configurer des membres du groupe TVA](#set-up-vat-group-members). Prenez note de **l’ID de membre du groupe** pour chaque membre du groupe TVA. La société représentante a besoin de ces ID pour ajouter les sociétés au groupe TVA.
5. Configurez l’extension de gestion du groupe TVA dans le [!INCLUDE[prod_short](includes/prod_short.md)] de la société représentante du groupe TVA en utilisant le guide de configuration assistée **Configurer la gestion des groupes TVA**. 

> [!NOTE]
> Pour se connecter à la société représentante du groupe TVA, les membres du groupe doivent disposer d’un compte utilisateur pouvant accéder au [!INCLUDE[prod_short](includes/prod_short.md)] de la société représentante du groupe TVA. La société représentante du groupe TVA doit créer au moins un utilisateur pour cela, cependant, pour des raisons de sécurité, nous vous recommandons de créer un utilisateur pour chaque membre du groupe TVA. Assurez-vous de distribuer les informations d’identification de ces utilisateurs aux membres du groupe TVA de manière sécurisée. Il s’agit d’un compte utilisateur système qui n’est pas lié à une personne réelle.

## <a name="about-the-vat-group-management-setup"></a>À propos de la configuration de la gestion des groupes TVA

La société représentante du groupe TVA expose une API aux membres du groupe. Les membres utilisent l’API pour se connecter au locataire [!INCLUDE[prod_short](includes/prod_short.md)] et soumettre les déclarations de TVA. Les membres du groupe TVA utilisent souvent [!INCLUDE[prod_short](includes/prod_short.md)] dans des locataires Azure Active Directory séparés. Par conséquent, une configuration est nécessaire pour connecter le membre du groupe TVA et le [!INCLUDE[prod_short](includes/prod_short.md)] de la société représentante. 
  
Les membres du groupe TVA se connectent à la société représentante en appelant un service web sur le locataire de la société représentante du groupe TVA. L’appelant doit être authentifié à l’aide d’OAuth2. Lorsque l’extension de gestion du groupe TVA est configurée, il vous sera demandé de vous authentifier auprès de la société représentante du groupe TVA pour obtenir et enregistrer un jeton d’accès. Ce jeton d’accès est utilisé lors de la soumission des déclarations de TVA à la société représentante du groupe TVA. 

## <a name="construct-the-api-url"></a>Construire l’URL de l’API
1. Dans le centre d’administration Business Central du locataire de la société représentante, choisissez l’onglet **Environnements**.
2. Dans la section **Détails**, copiez l’**URL**.
3. Ouvrez le Bloc-notes et collez l’URL. Remplacez **https://businesscentral.dynamics.com** par **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Configuration requise pour l’authentification 
> [!NOTE]
> Cela nécessite des informations d’identification pour un compte administrateur disposant d’une licence utilisateur complète pour [!INCLUDE[prod_short](includes/prod_short.md)].

Lorsque la société représentante du groupe TVA utilise [!INCLUDE[prod_short](includes/prod_short.md)] en ligne ou sur site, les membres du groupe TVA utilisent Azure Active Directory pour authentifier les utilisateurs lorsqu’ils soumettent des déclarations de TVA à la société représentante du groupe TVA. Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, les membres doivent configurer l’authentification unique. Pour plus d’informations, voir [Configurer l’authentification Azure Active Directory avec WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Si les membres du groupe TVA utilisent également [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, le membre du groupe TVA peut s’authentifier à l’aide des informations d’identification de l’utilisateur désignées et des informations sur le point de terminaison. Pour plus d’informations, voir [Configurer des membres du groupe TVA](ui-extensions-vat-group.md#set-up-vat-group-members).

Les membres du groupe TVA qui ont [!INCLUDE[prod_short](includes/prod_short.md)] sur site doivent configurer une inscription d’application dans Azure Active Directory pour le locataire [!INCLUDE[prod_short](includes/prod_short.md)] de la société représentante du groupe TVA. L’enregistrement de l’application permet au [!INCLUDE[prod_short](includes/prod_short.md)] en ligne de la société représentante du groupe TVA d’authentifier le membre du groupe. Pour plus d’informations, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app).

Lorsque vous créez l’inscription de l’application dans Azure Active Directory, vous devez spécifier les informations suivantes.

* Dans la section **Authentification**, ajoutez **Web** comme plateforme et utilisez les éléments **URL de redirection** suivants : https://businesscentral.dynamics.com/OAuthLanding.htm.
* Dans la section **Authentification**, dans l’option de sélection **Types de compte pris en charge**, sélectionnez **Comptes dans n’importe quel annuaire organisationnel (tout annuaire Azure AD – multi-locataires)**.
* Dans la section **Certificats et secrets**, créez un secret client et notez la valeur. Les membres du groupe TVA auront besoin du secret pour configurer la connexion à la société représentante du groupe.
* Dans la section **Autorisations API**, ajoutez des autorisations à [!INCLUDE[prod_short](includes/prod_short.md)]. Activez l’accès délégué à **Finances.ReadWrite.All** et **user_impersonation**.
* Dans la section **Aperçu**, notez l’**ID de l’application (client)**. Les membres du groupe TVA auront besoin de l’ID pour configurer la connexion à la société représentante du groupe. 

## <a name="set-up-vat-group-members"></a>Configurer des membres du groupe TVA
> [!IMPORTANT]
> Les sociétés membres du groupe TVA n’ont pas besoin de se connecter au HMRC, car elles rendent compte par l’intermédiaire de la société représentante du groupe.

Avant de commencer, contactez la société représentante du groupe TVA pour obtenir les informations suivantes sur leur locataire [!INCLUDE[prod_short](includes/prod_short.md)] :

* L’URL de l’API
* Le nom de leur société 
* L’ID client
* Le secret du client
* Les informations d’identification de connexion pour l’utilisateur dédié 

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configurer la gestion des groupes TVA**, puis choisissez le lien associé.
2. Dans le champ **Rôle du groupe TVA**, spécifie si vous êtes membre du groupe ou sa société représentante. Choisissez **Membre** pour agir en tant que membre du groupe et soumettre vos déclarations de TVA à la société représentante du groupe plutôt qu’à l’administration fiscale, puis choisissez **Suivant**.
3. Copiez la valeur de l **ID de membre du groupe**, puis partagez-le avec la société représentante du groupe TVA afin qu’elle puisse ajouter votre société en tant que membre approuvé du groupe.
4. Dans le champ **Version produit de la société représentante du groupe**, spécifiez la version de [!INCLUDE[prod_short](includes/prod_short.md)] que la société représentante utilise.
5. Dans le champ **Société représentante du groupe**, saisissez la raison sociale de la société représentante du groupe TVA. Par exemple, **CRONUS UK Ltd**.
6. Dans le champ **Type d’authentification**, choisissez **OAuth2**. Si la société représentante du groupe TVA utilise [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, précisez que **La société représentante du groupe utilise Business Central Online**, puis choisissez **Suivant**. Selon que la société représentante utilise ou non [!INCLUDE[prod_short](includes/prod_short.md)] en ligne ou sur site, suivez les étapes de la section [La société représentante du groupe TVA utilise Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) ou de la section [La société représentante du groupe TVA utilise Business Central sur site](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>La société représentante du groupe TVA utilise Business Central Online
1. Entrez les informations d’identification de l’utilisateur qui ont été fournies par la société représentante du groupe TVA et ajoutez les autorisations requises.
2. Choisissez la configuration des déclarations de TVA actuellement utilisée pour soumettre les déclarations de TVA aux autorités fiscales. Une fois la configuration terminée, [!INCLUDE[prod_short](includes/prod_short.md)] créera une nouvelle configuration basée sur ce choix et utilisera la configuration pour soumettre les déclarations de TVA à la société représentante du groupe TVA.  
3. Ajoutez l’**URL de l’API** de la société représentante du groupe TVA. En règle générale, l’URL est mise en forme comme suit : `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Par exemple, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>La société représentante du groupe TVA utilise Business Central sur site
1. Dans le champ **ID client**, indiquez l’ID client de l’enregistrement d’application dans Azure Active Directory.
2. Dans le champ **Secret client**, indiquez le secret client de l’enregistrement d’application dans Azure Active Directory.
3. Dans le champ **Point de terminaison d’autorité OAuth 2.0**, entrez `https://login.microsoftonline.com/common/oauth2`.
4. Dans le champ **URL de ressource OAuth 2.0**, entrez `https://api.businesscentral.dynamics.com/`.
5. Dans le champ **URL de redirection OAuth 2.0**, entrez `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Lorsque vous avez spécifié les différents champs, choisissez **Suivant**, puis saisissez les informations d’identification de l’utilisateur fournies par la société représentante du groupe TVA.
7. Choisissez la configuration de déclaration de TVA que vous utilisez pour déclarer la TVA aux autorités de votre pays.

## <a name="set-up-the-vat-group-representative"></a>Configurer la société représentante du groupe TVA
> [!NOTE]
> Pour la version sur site, nous ne prenons en charge qu’une seule instance de locataire de la société représentante du groupe.

> [!IMPORTANT]
> La société représentante doit activer la connexion du service **Configuration de la TVA HMRC** sur la page **Connexions de services**. Les sociétés représentantes doivent également télécharger les périodes de déclaration de TVA à partir du HMRC.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configurer la gestion des groupes TVA**, puis choisissez le lien associé.
2. Dans le champ **Rôle du groupe TVA**, spécifie si vous êtes membre du groupe ou sa société représentante. Choisissez **Société représentante** pour agir en tant que société représentante du groupe TVA et soumettre les déclarations de TVA à l’administration fiscale pour le groupe, puis choisissez **Suivant**.
3. Dans le champ **Compte déclaration de TVA**, spécifiez le compte que vous utilisez pour les déclarations de TVA.
4. Dans le champ **N° zone TVA due**, spécifiez la zone qui représente le montant total de la TVA due à partir d’une soumission de groupe TVA.
5. Dans le champ **Modèle feuille comptabilité déclaration de groupe**, spécifiez le modèle feuille comptabilité utilisé pour le document pour valider la TVA groupe sur le compte de déclaration.
6. Le champ **Membres approuvés** indique le nombre de membres du groupe configurés pour soumettre les déclarations de TVA à la société représentante. Pour ajouter de nouveaux membres, choisissez le numéro pour ouvrir la page **Membres approuvés**.
7. Pour ajouter de nouveaux membres, ajoutez les informations suivantes sur la page **Membres approuvés du groupe TVA** :
    1. Dans le champ **ID de membre du groupe**, entrez un identifiant pour le membre du groupe.
    2. Dans le champ **Nom du membre du groupe**, indiquez le nom du membre du groupe. 
    3. Dans le champ **Société**, indiquez la société à partir de laquelle le membre du groupe soumettra les déclarations de TVA dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, **CRONUS UK Ltd**.
    4. Spécifiez les informations de contact de la société.

## <a name="use-the-vat-group-management-features"></a>Utiliser des fonctionnalités de gestion du groupe TVA
Les membres du groupe TVA utilisent les processus standard pour préparer les déclarations de TVA. La seule différence est de choisir la version de déclaration **VATGROUP**, qui soumet la déclaration de TVA à la société représentante du groupe TVA plutôt qu’aux autorités. Pour plus d’informations, voir [À propos de la déclaration de retours de TVA](finance-how-report-vat.md#vatreturn).

Les sections suivantes décrivent les tâches que les sociétés représentantes du groupe TVA doivent effectuer.

### <a name="vat-group-submissions"></a>Soumissions groupe TVA

La page **Soumissions groupe TVA** répertorie les déclarations de TVA que les membres ont soumises. La page sert d’emplacement provisoire pour les soumissions jusqu’à ce que la société représentante du groupe TVA les inclue dans une déclaration de TVA pour le groupe. Vous pouvez ouvrir les soumissions pour consulter la TVA pour les cases individuelles déclarées par le membre du groupe TVA. 

> [!TIP]
> Sur la page **Périodes de retour de TVA**, le champ **Soumission des membres du groupe** indique le nombre de déclarations soumises par les membres. Pour vous assurer que ce nombre est à jour, choisissez l’action **Obtenir les déclarations de TVA**.

### <a name="creating-a-group-vat-return"></a>Création d’une déclaration de TVA de groupe

Pour déclarer la TVA pour le groupe, sur la page **Retours de TVA**, créez une déclaration de TVA pour votre entreprise uniquement. Ensuite, incluez les dernières soumissions de TVA des membres du groupe TVA en choisissant l’action **Inclure la TVA du groupe**.  

Lorsque la déclaration de TVA de la société représentante du groupe TVA a été soumise aux autorités pour l’ensemble du groupe, vous exécuterez normalement l’action **Calculer et comptabiliser la TVA**. Cette action ferme les écritures TVA ouvertes et transfère les montants vers le compte de déclaration de TVA. Actuellement, cette action ne prend pas en compte les soumissions de groupe. <!--Has this changed?--> Seules les écritures de TVA de la société représentante du groupe TVA seront enregistrées. Les montants de soumission des membres du groupe TVA doivent être imputés manuellement au montant du règlement de la TVA, de sorte que le compte de règlement de la TVA de la société représentante du groupe TVA reflète la responsabilité de ce qui a été déclaré aux autorités. Ce comportement changera dans une prochaine mise à jour de [!INCLUDE[prod_short](includes/prod_short.md)], de sorte que la totalité de la TVA du groupe (le montant total sur les lignes de la déclaration de TVA) sera réglée. <!--Has this behavior changed?-->

> [!NOTE]
> Les membres du groupe TVA peuvent corriger les déclarations de TVA soumises tant que la société représentante du groupe n’a pas validé la déclaration de TVA du groupe. Pour effectuer une correction, le membre du groupe TVA doit créer une déclaration de TVA pour la période de déclaration de TVA et la soumettre à la société représentante du groupe TVA. Du côté de la société représentante du groupe TVA, la dernière déclaration de TVA sera incluse dans la page **Retours de TVA**. 

> [!IMPORTANT]
> La fonctionnalité de groupe TVA n’est prise en charge que sur les marchés où [!INCLUDE[prod_short](includes/prod_short.md)] utilise une infrastructure de TVA composé de déclarations de TVA et de périodes de déclaration de TVA. Vous ne pouvez pas utiliser de groupes TVA sur d’autres marchés ayant d’autres implémentations de déclaration de TVA locale, tels que l’Autriche, l’Allemagne, l’Italie, l’Espagne et la Suisse. 

## <a name="see-also"></a>Voir aussi
[Fonctionnalité locale du Royaume-Uni dans la version britannique](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Numériser les taxes au Royaume-Uni](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Configuration de la TVA](finance-setup-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
