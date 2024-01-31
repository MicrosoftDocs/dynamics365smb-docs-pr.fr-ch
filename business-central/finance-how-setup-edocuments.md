---
title: Configurer des documents électroniques
description: Découvrez comment configurer la fonctionnalité de documents électroniques.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Configurer des documents électroniques

> [!IMPORTANT]
> Le module de base de documents électroniques est une infrastructure. Par défaut, il n’y a pas de champ **Intégration des services**. Si vous retrouvez les options **Format du document** par défaut, sachez qu’elles sont proposées à titre d’exemple et que la localisation doit fournir un format détaillé. Ces détails font partie des applications de localisation, car ils sont spécifiques aux exigences locales.

> [!NOTE]
> Depuis la version 23.2, un format de document PEPPOL standard est ajouté comme format global dans le champ **Format de document**. Gardez à l’esprit que vous ne pourrez probablement pas utiliser ce format tel quel. Il s’agit d’un format W1 fourni pour montrer comment utiliser cette fonctionnalité. Nous vous recommandons de tester le format PEPPOL existant avant de commencer à utiliser ce format.

La première étape de la configuration des documents électroniques (e-documents) consiste à configurer le service Documents électroniques dans lequel vous configurez le comportement complet de votre système en ce qui concerne la communication par documents électroniques.

## Configurer le service de documents électroniques

Suivez ces étapes pour configurer le service de documents électroniques.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de document électronique**, puis sélectionnez le lien associé.
2. Sélectionnez **Nouveau**, puis, sur la page **Service de document électronique**, sur le récapitulatif **Général**, configurez les champs comme décrit dans le tableau suivant.

    | Champ | Désignation |
    |-------|-------------|
    | Code | Sélectionnez le code de configuration de l’exportation électronique. |
    | Désignation | Saisissez une brève description de la configuration de l’exportation électronique. |
    | Format de document | <p>Format d’exportation de la configuration de l’exportation électronique.</p><p>Par défaut, il y a deux option dans ce champ. Vous pouvez sélectionner **PEPPOL BIS 3** comme format générique basé sur du code ou **Échange de données** lorsque vous devez configurer des pré-documents de formats spécifiques sur le Raccourci **Définition d’échange de données**.</p> |
    | Intégration de service | Sélectionnez le code d’intégration pour la configuration de l’exportation électronique. Dans la 1e vague, la seule option est **Aucune intégration**. |
    | Utiliser le traitement par lots | Spécifiez si le service utilise le traitement par lots pour l’exportation. |

3. Dans le récapitulatif **Paramètres importés**, configurez les champs comme indiqué dans le tableau ci-dessous.

    | Champ | Désignation |
    |-------|-------------|
    | Valider société réceptrice | Indiquez si les informations de la société destinataire doivent être validées pendant l’importation. |
    | Résoudre l’unité de mesure | Indiquez si l’unité de mesure doit être résolue au cours de l’importation. |
    | Rechercher référence article | Indiquez si un article doit être recherché par référence d’article pendant l’importation. |
    | Rechercher le GTIN de l’article | Indiquez si un article doit être recherché par numéro d’identification de commerce mondial (GTIN) pendant l’importation. |
    | Recherche de mappage de compte | Indiquez si un compte doit être recherché dans le **Mappage de compte** selon le texte entrant pendant l’importation. |
    | Valider remise ligne | Indiquez si une remise ligne doit être validée pendant l’importation. |
    | Lettrer remise facture | Indiquez si une remise facture doit être lettrée lors de l’import. |
    | Vérifier totaux | Indiquez si un total de facture doit être vérifié lors de l’import. |
    | Mettre à jour la commande | Indiquez si la commande achat correspondante doit être mise à jour. |
    | Créer des lignes feuille | Indiquez si la ligne feuille doit être créée à la place d’un document achat. Sélectionnez cette option lorsque vous souhaitez utiliser les journaux comme destination de vos factures. |
    | Nom du modèle feuille comptabilité | Spécifiez le nom du modèle feuille comptabilité utilisé pour la création de la ligne feuille. Ce champ est applicable lorsque vous souhaitez utiliser les journaux comme destination de vos factures. |
    | Nom feuille comptabilité | Spécifiez le nom de la feuille comptabilité utilisée pour la création de la ligne feuille. Ce champ est applicable lorsque vous souhaitez utiliser les journaux comme destination de vos factures. |
    | Importation automatique | Spécifiez s’il faut importer automatiquement les documents à partir du service. |
    | Heure de début du lot | Spécifiez l’heure de début des tâches d’importation. |
    | Délai entre les exécutions (en minutes) | Spécifiez le nombre de minutes entre deux exécutions de la tâche d’importation. |

4. Si vous avez sélectionné **Échange de données** dans le **Format du document** dans le champ Raccourci **Général**, utilisez la Raccourci **Définition d’échange de données** pour définir les champs suivants.

    | Champ | Désignation |
    |-------|-------------|
    | Type de document | Spécifiez le type de document qui utilise l’échange de données pour importer et exporter les données. Exemples : **facture de vente**, **note de crédit de vente** et **facture d’achat**. |
    | Importer code déf. échange données | Spécifiez le code d’échange de données utilisé pour importer les données. Utilisez ce champ uniquement pour recevoir un document dans le processus d’achat. |
    | Exporter code déf. échange données | Spécifiez le code d’échange de données utilisé pour exporter les données. Utilisez ce champ uniquement pour livrer des documents dans le processus de vente. |

> [!NOTE]
> Il existe des définitions d’échange de données préparées pour le format PEPPOL qui sont liées au document vente et achat standard. Cependant, vous ne pourrez probablement pas utiliser ces définitions telles quelles. Ce sont tous des formats W1 fournis pour montrer comment utiliser cette fonctionnalité. Nous vous recommandons de tester le format PEPPOL existant avant de commencer à les utiliser.

Si vous avez configuré le format **Définition d’échange de données** dans votre localisation, vous pouvez ajouter une ligne pour chaque type de document dont vous avez besoin. Ajoutez des lignes qui correspondent à l’exemple d’échange de données par défaut pour le format W1 PEPPOL. Cependant, d’abord sélectionner l’option **Type de document** pour chaque ligne dont vous avez besoin. Pour chaque type de données, sélectionnez la valeur **Importer le code de déf. d’échange de données** ou **Exporter le code de déf. d’échange de données** que vous souhaitez utiliser.

Si vous n’utilisez pas le format **Définition d’échange de données**, vous pouvez créer et configurer des formats à l’aide de l’ [interface](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Ajustez les informations sur les lignes **Exporter un mappage** et **Importer un mappage**, où vous trouverez les tables et champs à configurer les règles de transformation. Dans ce cas, vous devez ajouter une nouvelle option dans le champ **Format du document** liée à votre format.  

### Types de document pris en charge 

Les types de documents pris en charge sont basés sur le **format de document choisi**. Pour vérifier quels types de documents sont pris en charge, sur la page **Service documents électroniques** , exécutez l’action **Types de documents pris en charge** . Les **Types de documents sources pris en charge par le service de documents électroniques** s’ouvrent et dans la colonne **Type de document source** , vous pouvez trouver tous les types de documents pris en charge.  

## Configurer un profil d’envoi de documents

Vous pouvez configurer une méthode préférée d’envoi des documents de vente pour chacun de vos clients. De cette façon, vous n’avez pas besoin de sélectionner une option d’envoi à chaque fois que vous sélectionnez l’action **Publier et envoyer**. Sur la page **Profils d’envoi de documents**, configurez différents profils d’envoi que vous pouvez sélectionner dans le champ **Profil d’envoi de documents** d’une fiche client. Vous pouvez cocher la case **Par défaut** pour spécifier que le profil d’envoi du document est le profil par défaut pour tous les clients, sauf pour les clients dont le champ **Profil d’envoi de documents** est renseigné avec un autre profil d’envoi.

Cette fonctionnalité permet de mettre en place l’automatisation de la facturation électronique. Lorsque vous sélectionnez l’action **Valider et envoyer** dans un document vente, la boîte de dialogue **Valider et envoyer la confirmation** affiche le profil d’envoi utilisé, soit celui créé pour le client, soit le profil par défaut pour tous les clients.

Suivez la procédure pour configurer un profil d’envoi de documents.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Profils d’envoi de documents**, puis choisissez le lien associé.
2. Sur la page **Profils d’envoi de documents**, sélectionnez **Nouveau**.
3. Sous le raccourci **Général**, entrez les informations suivantes.
4. Sous le raccourci **Options d’envoi**, configurez les champs comme indiqué dans le tableau ci-dessous.

    | Champ | Désignation |
    |-------|-------------|
    | Document électronique | Spécifiez si le document est envoyé en tant que document électronique que le client peut importer dans son système lorsque vous choisissez le bouton **Valider et envoyer**. Pour utiliser cette option, vous devez également définir le champ **Format** ou **Code de flux de service de documents électroniques**. Sinon, le fichier peut être enregistré sur une disquette. |
    | Format | Spécifiez le format à utiliser pour envoyer un document électronique. Ce champ est requis si vous sélectionnez **Via le service d’échange de documents**, sélectionnez **Document électronique**. |
    | Code flux de service document électronique | Spécifiez le flux de service électronique utilisé pour envoyer des documents. Ce champ est requis si vous sélectionnez **Flux de services document électronique étendu**, sélectionnez **Document électronique**. |

    > [!NOTE]
    > Si vous sélectionnez **Flux de services document électronique étendu** dans le champ **Document électronique**, vous devez déjà avoir configuré le flux de travail pour vos documents électroniques.

## Configurer le flux de travail

Suivez cette procédure pour configurer le flux de travail utilisé dans la fonctionnalité de document électronique.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles de flux de travail**, puis sélectionnez le lien associé.
2. Si vous ne trouvez pas de **Modèles de flux de travail de document électronique** sur la page **Modèles de flux de travail**, sélectionnez **Réinitialiser les modèles Microsoft**. **Modèles de flux de travail de document électronique** devrait alors s’afficher. Fermez la page.
3. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.
4. Exécutez l’action **Créer flux de travail à partir du modèle** pour sélectionner un modèle pour le processus de documents électroniques. Les modèles disponibles sont **Envoyer à un service** et **Envoyer à plusieurs services**.
5. Sélectionnez **OK** pour terminer la configuration du flux de travail.
6. Dans le champ **Alors, réponse**, sélectionnez **Envoyer le document électronique à l’aide de la configuration** pour configurer les réponses du flux de travail.
7. Sélectionnez le service de documents électroniques que vous avez créé en option, sélectionnez **OK**, puis activez le flux de travail.

> [!NOTE]
> Vous pouvez créer votre propre flux de travail pour les documents électroniques sans utiliser de modèles de flux de travail prédéfinis. Si vous disposez de plus de services, vous pouvez utiliser différents flux de travail.

Pour utiliser davantage de workflows, configurez-les via les profils d’envoi de documents pour différents clients. Lorsque vous configurez le flux de travail, spécifiez le profil d’envoi du document dans la colonne **Sur condition** de l’onglet Raccourci **Étapes du flux de travail**, car vous ne pouvez pas avoir deux services qui utilisent le même profil d’envoi de documents dans les flux de travail.

Lorsque vous configurez votre workflow sur la page **Workflow** , pointez sur le champ **Sur condition** sur le Raccourci **Étapes du workflow**. Sur la page **Conditions d’événement** , dans le champ **Filtre** , sélectionnez le profil d’envoi de documents que vous souhaitez utiliser.

## Mettre en place une stratégie de rétention des documents électroniques

Les documents électroniques peuvent faire l’objet de différentes législations locales liées à la durée de conservation des documents électroniques. Par conséquent, nous avons ajouté une configuration de stratégie de rétention pour toutes les informations importantes liées aux documents électroniques. Les administrateurs peuvent définir des stratégies de rétention qui spécifient la fréquence à laquelle Dynamics 365 Business Central supprime les enregistrements obsolètes liés aux documents électroniques. Pour en savoir plus sur les stratégies de rétention, accédez à [Définir des stratégies de rétention](admin-data-retention-policies.md).

Pour configurer des stratégies de rétention liées aux documents électroniques, procédez comme suit.

1. Sur la page **Services documents électroniques** , exécutez l’action **Stratégie de rétention**.
2. Une fois l’action terminée, sélectionnez l’une des stratégies de rétention suivantes à configurer :

    - Journal de documents électroniques
    - Journal d’intégration des documents électroniques
    - Journal du mappage de document électronique
    - Stockage des données du document électronique

## Voir aussi

[Comment utiliser des documents électroniques dans Business Central](finance-how-use-edocuments.md)  
[Comment étendre des documents électroniques dans Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestion financière](finance.md)  
[Facturation des ventes](sales-how-invoice-sales.md)  
[Enregistrer les achats avec les factures achat et les commandes](purchasing-how-record-purchases.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
