---
title: Configuration du connecteur de documents électroniques avec des points de terminaison externes
description: Cet article explique comment configurer la fonctionnalité E-Documents lorsqu’elle est connectée à des points de terminaison externes.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
---

# Configuration du connecteur de documents électroniques avec des points de terminaison externes

Cet article explique comment configurer la fonctionnalité E-Documents lorsqu’elle est connectée à des points de terminaison externes.

Avant d’utiliser la fonctionnalité décrite dans cet article, installez l’application **Connecteur de documents électroniques avec des points de terminaison externes** en haut de l’application globale **Base document électronique** . Cette application peut être utilisée pour une intégration par défaut avec les points d’accès externes (tiers) afin d’automatiser le flux de documents électroniques. Étant donné que cette application ne représente que certains des connecteurs sélectionnés, vous n’êtes pas limité aux intégrations existantes. La plupart des connecteurs seront disponibles sur AppSource à l’avenir.

## Configurer la connexion

Pour commencer votre configuration, suivez les étapes décrites dans [Application Base document électronique](finance-how-setup-edocuments.md). Une fois ces étapes terminées, revenez à cet article et procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de document électronique**, puis sélectionnez le lien associé.
2. Dans le champ **Intégration de services**, sélectionnez l’un des codes d’intégration proposés pour la configuration du service de point de terminaison.
3. Sélectionnez **Configurer l’intégration du service**.
4. Sur la page **Configuration de la connexion externe du document électronique**, sélectionnez **Demander un code d’autorisation**. Vous êtes redirigé vers la page Web d’autorisation de service externe et vous êtes invité à saisir vos informations de connexion.
5. Copiez le code d’autorisation dans le champ **Entrer le code d’autorisation** .
6. Sélectionnez **Actualiser le jeton d’accès** pour vous assurer que vous pouvez actualiser le jeton.

    > [!NOTE]
    > Cette mise en relation nécessite une communication avec des prestataires externes qui peuvent être soumis à un paiement complémentaire et nécessiter des contrats avec eux. Pour obtenir toutes les informations d’identification nécessaires, contactez les prestataires de services.

7. Sur la page **Configuration connexion externe document électronique**, renseignez les champs suivants :

    | Nom du champ | Désignation |
    |---|---|
    | URL FileAPI | Spécifiez l’URL de l’API du fichier. |
    | URL des parties de fichier | Spécifiez l’URL des parties de fichier. |
    | URL DocumentAPI | Spécifiez l’URL de l’API du document. |
    | ID société | Spécifiez l’ID de la société. |
    | Mode d’envoi | Spécifiez le mode d’envoi. Vous pouvez sélectionner **Production**, **Test** ou **Certification**. |

    > [!NOTE]
    > Demandez à votre fournisseur de services tous les détails précédents pour établir une connexion avec son point d’accès.

## Configuration des informations société

Avant de commencer à utiliser les documents électroniques, mettez à jour la page **Informations sur l’entreprise** en procédant comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Informations société**, puis cliquez sur le lien associé.
2. En plus de remplir les champs habituels, vous devez également remplir les champs suivants :

    | Nom du champ | Désignation |
    |---|---|
    | Code SWIFT | Spécifiez le code SWIFT (code international d'identification bancaire) de votre banque principale. |
    | Code établissement | Spécifiez le numéro de l'établissement à quatre chiffres de votre banque. |
    | Numéro d’enregistrement TVA | Spécifiez le n° identif. TVA de la société. |

3. Fermez la page.

## Configurer les clients pour recevoir des documents électroniques

Pour permettre aux clients de recevoir vos documents électroniques, procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la fiche **client**.
3. En plus de remplir les champs habituels, dans le champ **GLN** , précisez le client dans le cadre de l’envoi de documents électroniques.
4. Cochez le champ **Utiliser le GLN dans les documents électroniques** pour indiquer si le numéro d’emplacement global (GLN) est utilisé comme numéro d’identification de partie dans les documents électroniques.
5. Fermez la page.

## Autres paramètres

Avant de commencer à travailler avec des documents électroniques, configurez les **workflows** de documents électroniques et **les profils d’envoi de documents** pour utilisez vos flux de travail. Une fois la connexion au service établie, vous pouvez commencer à utiliser votre solution de documents électroniques.

## Fournisseurs de services disponibles

Microsoft souhaite encourager les fournisseurs de points d’accès à ajouter leurs connecteurs par-dessus nos **Base document électronique** cadre.

Actuellement, Pagero est le seul fournisseur de points d’accès couvert par ce système. Microsoft n’a aucune obligation contractuelle avec Pagero. Par conséquent, vous devez conclure un contrat avec eux pour obtenir toutes les informations d’identification nécessaires.

Nous mettrons à jour cette liste au fur et à mesure que nous recevrons de nouveaux fournisseurs de points d’accès pour l’échange de documents électroniques.

## Voir aussi

[Comment configurer des documents électroniques dans Business Central](finance-how-setup-edocuments.md)  
[Comment utiliser des documents électroniques dans Business Central](finance-how-use-edocuments.md)  
[Comment étendre des documents électroniques dans Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestion financière](finance.md)  
[Facturation des ventes](sales-how-invoice-sales.md)  
[Enregistrer les achats avec les factures achat et les commandes](purchasing-how-record-purchases.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
