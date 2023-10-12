---
title: Obtenir le complément Business Central pour Outlook
description: Découvrez comment installer le complément Business Central pour Outlook pour votre organisation ou pour votre propre usage.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 04/27/2022
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Obtenir le complément Business Central pour Outlook

Avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez gérer les interactions commerciales avec vos clients et fournisseurs, directement dans Microsoft Outlook. Avec le complément [!INCLUDE[prod_short](includes/prod_short.md)] pour Outlook, vous pouvez voir les données financières relatives aux clients et aux fournisseurs. Vous pouvez également créer et envoyer des documents financiers, tels que des devis et des factures.  

Il existe deux manières d’installer le complément Business Central pour Outlook, en fonction de votre rôle dans l’organisation :

- En tant qu’administrateur Microsoft 365, utilisez le *Déploiement centralisé* pour installer le complément automatiquement pour l’ensemble de l’organisation, des groupes ou des utilisateurs spécifiques.

- En tant qu’utilisateur quelconque, installez le complément pour votre propre usage, si votre administrateur ne l’a pas déjà déployé pour vous.

## <a name="about-the-business-central-add-in-for-outlook"></a>À propos du complément Business Central pour Outlook

Le complément Business Central pour Outlook se compose de deux compléments plus petits :

- Panorama des contacts

    Ce complément fournit aux utilisateurs des informations [!INCLUDE[prod_short](includes/prod_short.md)] sur le client ou le fournisseur dans les e-mails Outlook et les rendez-vous du calendrier. Il vous permet également de créer et d’envoyer des documents professionnels [!INCLUDE[prod_short](includes/prod_short.md)], tels que des devis et des factures, à un contact. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Affichage de document

    Lorsqu’un e-mail fait référence à un numéro de document commercial dans le corps de l’e-mail, ce complément fournit un lien direct, en ligne, entre le corps de l’e-mail et le document commercial réel dans [!INCLUDE[prod_short](includes/prod_short.md)].

Pour plus d’informations sur les possibilités des compléments, voir [Utiliser Business Central en tant que boîte de réception professionnelle dans Outlook](work-outlook-addin.md).

Chaque complément est fourni sous forme de fichier XML, appelé *manifeste*, qui doit être installé dans Outlook pour toute personne souhaitant cette fonctionnalité. Ces fichiers décrivent comment activer les compléments et se connecter à Business Central lorsqu’ils sont utilisés dans Outlook. Ces fichiers sont généralement utilisés par un administrateur. En tant qu’utilisateur normal, dans la plupart des cas, vous n’aurez pas à gérer directement ces fichiers. Soit votre administrateur configurera le complément pour qu’il s’installe automatiquement pour vous, soit vous utiliserez la configuration assistée intégrée pour gérer l’installation.

> [!IMPORTANT]
> Utilisation de plusieurs environnements ? Le complément Business Central pour Outlook est conçu pour fonctionner avec un seul environnement Business Central. Lorsque le complément est installé, le nom de l’environnement est inclus dans le manifeste du complément. Cette configuration signifie que le complément se connectera uniquement à l’environnement à partir duquel il a été installé. Pour utiliser le complément avec un autre environnement, ouvrez l’environnement et réinstallez le complément.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Déployer le complément à l’aide du déploiement centralisé en tant qu’administrateur

Le déploiement centralisé est une fonctionnalité du centre d’administration de Microsoft 365 que vous utilisez pour installer automatiquement des compléments dans les applications Office des utilisateurs, comme Outlook. C’est la méthode recommandée aux administrateurs pour déployer des compléments Office pour les utilisateurs et les groupes au sein de l’organisation.

> [!NOTE]
> Pour Business Central local, voir [Configuration du complément pour l’intégration d’Outlook avec Business Central local](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) dans le contenu administratif (en anglais uniquement).

### <a name="prerequisites"></a>Conditions préalables

- Un abonnement Microsoft 365  
- Les utilisateurs se voient attribuer une licence Microsoft 365  
- Votre compte Microsoft 365 a le rôle *Administrateur global* ou *Administrateur Exchange*

### <a name="deploy-the-add-in"></a>Déploiement du complément

1. Dans Business Central, sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonctionnalité Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration assistée**, puis choisissez le lien associé.
2. Sélectionnez **Déploiement centralisé du complément Outlook** pour démarrer le guide de configuration assistée.
3. Passez en revue la première page et sélectionnez **Suivant** pour ouvrir la page de téléchargement des compléments.
4. Dans la colonne **Déployer**, cochez la case des compléments que vous souhaitez déployer, puis sélectionnez **Télécharger et continuer**.

    Un fichier nommé *OutlookAddins.zip* est téléchargé sur votre appareil.

5. À ce stade, vous avez terminé le travail que vous devez effectuer dans Business Central, vous pouvez donc sélectionner **Terminé**.

   >[!TIP]
   > Avant de sélectionner **Suivant**, sélectionnez le lien **Accéder à Microsoft 365 (s’ouvre dans une nouvelle fenêtre)** pour ouvrir le centre d’administration Microsoft 365 et s’y connecter dans une nouvelle fenêtre de navigateur. Vous devrez de toute façon accéder au centre d’administration Microsoft 365 à une étape ultérieure.

6. Allez dans le dossier où OutlookAddins.zip a été téléchargé et extrayez les fichiers **Contact Insights.xml** et **Document View.xml** du .zip dans un dossier de votre choix.

    Pour plus d’informations, consultez [Compresser et décompresser des fichiers et dossiers](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Connectez-vous au Centre d’administration Microsoft 365, puis accédez à [Applications intégrées](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Sélectionnez **Charger des applications personnalisées**.
9. Sur la page **Charger les applications à déployer**, sélectionnez **Charger le fichier manifeste (.xml) depuis l’appareil** > **Choisir le fichier**.
10. Sélectionnez l’un des fichiers de complément que vous avez extraits précédemment, par exemple, **Contact Insights.xml**.
11. Suivez les instructions pour affecter des utilisateurs et déployer le complément.
12. Répétez les étapes 9 à 11 pour l’autre fichier de complément si vous le souhaitez.

> [!IMPORTANT]
> Une coche verte apparaît lorsque le complément est déployé dans le centre d’administration. Cependant, il peut falloir jusqu’à 24 heures avant que les utilisateurs voient le complément dans l’application Outlook. Les utilisateurs devront peut-être également redémarrer Outlook.

Une fois terminé, vous pouvez toujours modifier le déploiement dans le centre d’administration Microsoft 365, par exemple en affectant plus d’utilisateurs. Pour plus d’informations sur le déploiement de compléments dans le centre d’administration, voir [Déployer des compléments dans le centre d’administration](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Installer le complément pour votre propre usage

Si votre organisation le permet, vous pouvez installer le complément Business Central pour votre propre compte. Si vous n’êtes pas sûr, demandez à votre administrateur.

1. Dans Business Central, accédez à l’icône en forme ![d’ampoule qui ouvre la fonctionnalité Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Obtenir le complément Outlook**, puis sélectionnez le lien associé.
2. Lisez la page et sélectionnez **Suivant** quand vous êtes prêt.
3. Si vous souhaitez recevoir un e-mail de bienvenue de Business Central avec une présentation de l’utilisation du complément, activez **Envoyer un exemple de message électronique**.
4. Choisissez **Terminer** pour effectuer l’installation.

Business Central se connectera à votre serveur de messagerie et installera le complément dans votre instance d’Outlook. Cela ne prendra pas longtemps. Vous êtes maintenant prêt à commencer à utiliser le complément dans Outlook.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>Pour Business Central local

Si vous utilisez Business Central sur site, l’installation du complément peut être légèrement différente.

1. Dans Business Central, accédez à l’icône en forme ![d’ampoule qui ouvre la fonctionnalité Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Obtenir le complément Outlook**, puis sélectionnez le lien associé.
2. Lisez la page et sélectionnez **Suivant** quand vous êtes prêt.
3. Effectuez l’une des étapes suivantes, selon la page que vous voyez :

    - Si vous voyez le bouton **Installer dans mon Outlook**, sélectionnez-le, et vous avez terminé.
    - Si vous voyez le bouton **Suivant**, sélectionnez-le. Sur la page suivante, si vous souhaitez recevoir un e-mail de bienvenue de Business Central avec une présentation de l’utilisation du complément, activez **Envoyer un exemple de message électronique**. Sélectionnez ensuite **Terminé** et vous avez terminé.
    - Si vous voyez le bouton **Télécharger le complément**, sélectionnez-le, puis passez à l’étape suivante.
4. Lorsque vous sélectionnez **Télécharger le complément**, un fichier portant le nom *OutlookAddins.zip* est téléchargé sur votre appareil. Vous devez voir le fichier en haut du navigateur.

   Allez dans le dossier où OutlookAddins.zip a été téléchargé et extrayez les fichiers **Contact Insights.xml** et **Document View.xml** du .zip dans un dossier de votre choix. Pour plus d’informations sur l’extraction de fichiers, consultez [Compresser et décompresser des fichiers et dossiers](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Ouvrez Outlook et sélectionnez **Télécharger des compléments** dans le ruban. Sinon, si vous utilisez Outlook sur le Web, sélectionnez le menu déroulant sur tout message électronique nouveau ou existant, puis sélectionnez **Télécharger les compléments**.
6. Sélectionnez **Mes compléments** > **Ajouter un complément personnalisé** > **Ajouter à partir d’un fichier**.
7. Choisissez l’un des fichiers .xml que vous avez extraits, comme **Contact Insights.xml**, puis sélectionnez **Ouvrir** > **Installer**.
8. Répétez les étapes 6 et 7 pour l’autre fichier .xml, si vous l’avez téléchargé.

Vous êtes maintenant prêt à commencer à utiliser le complément dans Outlook.

## <a name="see-also"></a>Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Obtention de Business Central sur mon périphérique mobile](install-mobile-app.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Configuration minimale requise pour Outlook](product-requirements.md#outlook)  
[Utiliser des compléments dans Outlook sur le Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
