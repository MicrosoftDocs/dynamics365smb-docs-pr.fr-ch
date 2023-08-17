---
title: "Démarrer par une version en version préliminaire de Business\_Central pour Copilot"
description: Explique comment obtenir un environnement Business Central avec la nouvelle capacité d’IA pour générer des suggestions de texte pour les descriptions d’articles/produits.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# <a name="get-started-with-a-business-central-preview-version-for-copilot"></a>Démarrer par une version en version préliminaire de Business Central pour Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Vous pouvez essayer le texte marketing d’articles alimenté par l’IA avec Copilot, que vous soyez un client existant de Business Central ou un client potentiel, c’est-à-dire quelqu’un qui souhaite simplement explorer Business Central et essayer la nouvelle fonctionnalité. Pour commencer, vous devez avoir accès à une version préliminaire de Business Central Online qui prend en charge la nouvelle fonctionnalité. Remplissez la section ci-dessous qui s’applique à vous.

## <a name="your-organization-already-uses-business-central"></a>Votre organisation utilise déjà Business Central

En tant que client ou partenaire existant, vous aurez besoin d’un administrateur ayant accès au centre d’administration de Business Central pour configurer un environnement qui exécute la version préliminaire qui inclut Copilot. Une fois que l’environnement est opérationnel, les utilisateurs peuvent essayer la nouvelle fonctionnalité.

Si vous êtes un administrateur d’environnement, procédez comme suit :

1. Connectez-vous au centre d’administration Business Central.
2. Sélectionner **Environnements** > **Nouveau**.
3. Dans le volet **Créer un environnement** , spécifiez un nom pour le nouvel environnement dans le champ **Nom de l’environnement**.
4. Définissez **Type d’environnement** sur **Sandbox** ou **Production**.
5. Définissez **Pays** sur n’importe quel pays/région de la liste, mais sachez que dans la version préliminaire, le texte marketing généré par l’IA à partir de Copilot est uniquement en anglais.
6. Dans la zone **Version**, choisissez une version 22 ou ultérieure depuis la liste.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Sélectionnez **Créer**.  

Pour plus d’informations sur la création d’environnements, accédez à [Créer un environnement](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Si vous avez des bacs à sable en version préliminaire qui s’exécutent sur **22.0.54157.54311 (Version préliminaire - édition Copilot)**, sachez que ces environnements ne sont disponibles que jusqu’au 1er mai 2023. Après cette date, vous devrez mettre en service un nouvel environnement ou mettre à niveau l’un de vos autres environnements vers la version 22.0 ou ultérieure pour continuer à essayer la version préliminaire du texte marketing d’articles alimenté par l’IA.

## <a name="your-organization-doesnt-use-business-central"></a>Votre organisation n’utilise pas Business Central

Si vous n’êtes pas client de Business Central, inscrivez-vous pour un essai gratuit afin d’essayer les nouvelles fonctionnalités d’IA. L’inscription à l’essai est simple. Vous serez guidé à travers quelques étapes où vous devrez fournir certaines informations, telles que votre adresse e-mail, votre numéro de téléphone et votre nom. Pour obtenir l’essai, procédez comme suit :

1. Accédez à [ce site d’essai](https://go.microsoft.com/fwlink/?linkid=2227167) pour commencer le processus d’inscription.
2. Suivez les instructions affichées à l’écran.

   Vous êtes invité à fournir des informations telles que votre adresse e-mail, votre nom et votre numéro de téléphone. L’expérience exacte peut varier en fonction des informations que vous fournissez. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Pour votre adresse e-mail, utilisez votre adresse e-mail professionnelle ou scolaire. Nous établirons votre essai sur le compte de votre organisation. Vous ne pouvez pas utiliser les adresses e-mail fournies par les services de messagerie grand public ou les fournisseurs de télécommunications, comme outlook.com, hotmail.com, gmail.com, etc.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Quand vous arrivez à l’étape **Détails de la confirmation**, vous êtes prêt à commencer l’essai.

   - Pour accéder directement à Business Central, sélectionnez **Ignorer et accédez à Dynamics 365 Business Central** > **Commencer**.
   - Vous avez également la possibilité d’inviter d’autres membres de votre organisation à l’essai gratuit également. Entrez simplement les adresses e-mail de chaque personne, puis sélectionnez **Envoyer des invitations**. Sélectionnez **Commencer** pour accéder à Business Central.  

   Vous serez redirigé vers votre essai sur [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). La préparation de la version d’essai peut prendre plusieurs minutes à votre première connexion.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Une fois connecté, vous verrez la page d’accueil de Business Central, appelée le tableau de bord, qui ressemble à la figure suivante :

   [![Affiche le tableau de bord Business Central et la liste de contrôle pour Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Pour obtenir une introduction guidée à la création de texte marketing d’articles basé sur l’IA avec Copilot, sous **Votre liste de contrôle** en haut de la page, sélectionnez **Créer avec Copilote** > **Commencer la visite**. Ensuite, suivez simplement les instructions à l’écran.

   > [!TIP]
   > Si vous ne voyez pas **Votre liste de contrôle**, sélectionnez le bouton **Afficher les visites de démonstration** en premier.

## <a name="next-steps"></a>Étapes suivantes

Les fonctionnalités d’intelligence artificielle fournies par Copilot doivent être activées avant que vous ou toute autre personne puissiez utiliser Copilot. Pour activer les fonctionnalités d’IA, un administrateur doit accepter les termes et conditions de [la version préliminaire](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) et de [la Déclaration de confidentialité Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) au nom de l’organisation.

> [!NOTE]
> Si vous utilisez une version d’essai, vous être administrateur. Si vous avez invité d’autres personnes de votre organisation à l’essai à l’inscription, elles ne pourront pas utiliser Copilot tant que vous n’aurez pas accepté les conditions générales.

Il existe deux façons de consentir en tant qu’administrateur :

- Le plus simple est d’utiliser Copilot. La première fois que vous utilisez Copilot en tant qu’administrateur, vous êtes invité à consulter les conditions générales, puis à accepter ou non. Pour apprendre à utiliser Copilot, rendez-vous sur [Ajouter du texte marketing aux articles](item-marketing-text.md).  

- L’autre façon est d’utiliser la page **Statut des avis de confidentialité** dans Business Central et acceptez l’intégration **Azure OpenAI** pour tous les utilisateurs. Pour en savoir plus, rendez-vous sur [Consentement aux termes et conditions](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble du texte marketing article optimisé par l’IA avec Copilot](ai-overview.md)  
[Configuration du texte marketing article optimisé par l’IA avec Copilot en tant qu’administrateur](enable-ai.md)  
[Créer un texte marketing pour les articles à l’aide de Copilot](item-marketing-text.md)  
[FAQ sur le texte marketing article optimisé par l’IA (version préliminaire) avec Copilot](ai-faq.md)  
