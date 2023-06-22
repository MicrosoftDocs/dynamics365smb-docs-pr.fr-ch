---
title: Extension d’analyseur Image
description: "Cette extension vous permet d’analyser des photos des contacts et des articles permettant de rechercher des attributs, afin de les trouver rapidement dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
---

# <a name="the-image-analyzer-extension" />Extension d’analyseur Image

L’extension d’analyseur Image utilise les analyses d’image puissantes fournies par l’API Vision par ordinateur d’Azure Cognitive Services pour détecter des attributs dans les images que vous importez pour des articles et des contacts, afin de les examiner et de les affecter facilement. Pour les articles, les attributs peuvent être si l’article est une table ou une voiture et, s’il est rouge ou bleu. Pour les contacts, les attributs peuvent être le sexe ou l’âge.

L’analyseur Image propose des attributs basés sur des balises trouvées par l’API Vision par ordinateur et un niveau de confiance. Par défaut, il propose des attributs uniquement s’il est sûr à au moins 80 % que l’attribut est correct. Vous pouvez définir un autre niveau de confiance, si nécessaire. Pour en savoir plus sur la manière dont les balises et le niveau de confiance sont déterminés, voir [API Vision par ordinateur](https://go.microsoft.com/fwlink/?linkid=851476).  

L’analyseur Image est gratuit dans [!INCLUDE[prod_short](includes/prod_short.md)], mais il existe une limite au nombre d’articles que vous pouvez analyser pendant une période donnée. Par défaut, vous pouvez analyser 100 images par mois.

Après avoir activé l’extension, l’analyseur Image fonctionne chaque fois que vous importez une image à un article ou à un contact. Vous pourrez consulter les attributs, le niveau de confiance et les détails immédiatement, et décider de gérer chaque attribut. Si vous avez importé des images avant d’activer l’extension d’analyseur Image, vous devez consulter la fiche article ou contact et choisir l’action **Analyser l’image**.  

## <a name="privacy-notice" />Déclaration de confidentialité

Cette extension utilise l’API Vision par ordinateur d’Azure Cognitive Services, qui peut avoir différents niveaux d’engagements en matière de conformité par rapport à [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous activez l’extension Analyseur Image, les données client telles qu’une image de contact ou une image d’article sont envoyées à l’API Vision par ordinateur. En installant cette extension, vous acceptez que cet ensemble limité de données soit envoyé à l’API Vision par ordinateur. Notez que vous pouvez désactiver et désinstaller l’extension Analyseur Image à tout moment pour ne plus utiliser cette fonctionnalité. Pour plus d’informations, voir [Centre de gestion de la confidentialité Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements" />Conditions requises

Certaines exigences s’appliquent aux images :

* Formats des images : JPEG, PNG, GIF, BMP  
* Taille maxi. de fichier : inférieure à 4 Mo  
* Dimensions des images : supérieure à 50 x 50 pixels  

## <a name="switch-on-the-image-analyzer-extension" />Activer l’extension d’analyseur Image

L’extension d’analyseur Image est intégrée à [!INCLUDE[prod_short](includes/prod_short.md)]. Vous devez juste l’activer.

> [!NOTE]  
> Pour activer l’extension d’analyseur Image, vous devez être un administrateur. Assurez-vous que vous disposez de l’ensemble d’autorisations d’utilisateur **SUPER**. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

Pour activer l’extension d’analyseur Image, effectuez l’une des actions suivantes :

* Ouvrez une fiche Article ou Contact. Dans la barre de notification, choisissez **Analyser l’image**, puis suivez la procédure du guide de configuration assistée.  
* Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexions de services**, puis choisissez **Configuration de l’analyse d’image**. Activez la case à cocher **Activer l’analyseur Image**, puis suivez la procédure du guide de configuration assistée.  

    > [!TIP]  
    > La page **Configuration de l’analyse de l’image** vous permet également de modifier le degré de confiance des suggestions d’attribut. Par exemple, si vous souhaitez avoir besoin d’un niveau de confiance supérieur, vous pouvez saisir un pourcentage plus élevé.

## <a name="analyze-an-item-image" />Analyser l’image d’un article

Les étapes suivantes décrivent comment analyser une image importée avant que vous ayez activé l’extension d’analyseur Image.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article, puis cliquez sur **Analyser l’image**.  
3. La page **Attributs d’analyseur Image** affiche les attributs détectés, le niveau de confiance, et d’autres détails sur l’attribut. Utilisez les options **Action à effectuer** pour spécifier ce qu’il faut faire avec l’attribut ou choisissez **Ajouter à la description de l’article** pour ajouter le nom de l’attribut à la description de l’article. Par exemple, cette action peut être utile pour ajouter rapidement un détail.

Le champ **Action à effectuer** comporte les options suivantes :

| Action | Désignation |
| ------ | ----------- |
| *Ignorer* | Aucune action ne sera effectuée. |
| *Utiliser comme attribut* | La valeur est ajoutée aux attributs de l’article. En savoir plus sur [Utiliser les attributs d’article](inventory-how-work-item-attributes.md). |
| *Utiliser comme catégorie* | La valeur sélectionnée est ajoutée en tant que catégorie. En savoir plus sur [Classer les articles](inventory-how-categorize-items.md). |
| *Ajouter à la liste de blocage* | Si l’analyse suggère un attribut que vous ne souhaitez pas voir, vous pouvez le bloquer. Faites attention, cependant. Les attributs bloqués ne sont pas non plus suggérés pour les autres articles. Si vous regrettez d’avoir bloqué un attribut, choisissez **Afficher les attributs bloqués**, puis supprimez l’attribut de la liste. |

> [!NOTE]  
> Par défaut **Attributs article** affiche les attributs où **Score de fiabilité** est supérieur à la valeur de **Niveau de score de fiabilité %** définie dans **Configuration de l’analyse d’image**. Pour voir tous les attributs détectés, choisissez laction **Afficher tous les attributs**.

## <a name="analyze-a-contact-person-picture" />Analyser la photo d’un contact

Les étapes suivantes décrivent comment analyser une image importée avant que vous ayez activé l’extension d’analyseur Image.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contacts**, puis sélectionnez le lien associé.  
2. Sélectionnez le contact, puis cliquez sur **Analyser l’image**.  
3. Sur le raccourci **Questionnaire profil**, consultez les suggestions, et faites des corrections si nécessaire. En savoir plus, [Utiliser des questionnaires profil pour classer les contacts professionnels](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > L’API Vision par ordinateur renvoie les attributs suivants :
    >
    > * *âge*
    >
    >     Un « âge visuel » estimé en années. Il s’agit de l’âge que semble avoir une personne par opposition à l’âge biologique réel.
    > * *sexe*
    >
    >    Masculin ou féminin
    >
    > L’API Vision par ordinateur ne renvoie pas le niveau de fiabilité pour les attributs d’âge et de sexe.
  
## <a name="use-your-own-computer-vision-api-account" />Utiliser votre propre compte pour l’API Vision par ordinateur

Vous pouvez également utiliser votre propre compte pour l’API Vision par ordinateur, par exemple, si vous souhaitez analyser plus d’images que ce que permet l’intégration par défaut.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration d’analyse d’image**, puis choisissez le lien associé.
2. Entrez l’**URI d’API** et la **clé d’API** que vous avez reçus pour l’API Vision par ordinateur.  

    > [!NOTE]  
    > Vous devez ajouter **/analyze** à la fin de l’URI d’API, si ce n’est pas déjà le cas. Par exemple, ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period" />Visualiser le nombre d’analyses restant pour la période en cours

Vous pouvez afficher le nombre d’analyses effectué, et le nombre restant, pour la période actuelle.  

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration d’analyse d’image**, puis choisissez le lien associé.
2. **Type limite**, **Valeur limite** et **Analyses effectuées** vous fournissent des informations sur l’utilisation.  

## <a name="stop-using-the-image-analyzer-extension" />Arrêter d’utiliser l’extension d’analyseur Image

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexions de services**, puis choisissez **Configuration de l’analyse d’image**.  
2. Désactivez la case à cocher **Activer l’analyseur Image**.  

Vous pouvez également désinstaller complètement l’extension. Vous pouvez toujours la récupérer à partir de AppSource. Pour plus d’informations, voir [Installation et désinstallation d’extensions dans Business Central](ui-extensions-install-uninstall.md#uninstall-an-app).  

## <a name="see-also" />Voir aussi

[Utiliser les attributs d’article](inventory-how-work-item-attributes.md)  
[Catégoriser des articles](inventory-how-categorize-items.md)  
[Utiliser des questionnaires profil pour classer les contacts professionnels](marketing-create-contact-profile-questionnaire.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
