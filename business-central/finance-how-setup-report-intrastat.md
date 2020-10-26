---
title: 'Procédure : configurer et enregistrer un état intracommunautaire | Microsoft Docs'
description: Apprendre à configurer les fonctionnalités d’état intracommunautaire, et comment enregistrer les transactions avec des sociétés dans d’autres pays/régions.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f0c10948aef6db58474de5c627e1ce82f0a13102
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920537"
---
# <a name="set-up-and-report-intrastat"></a>Configurer et enregistrer un état intracommunautaire
Toutes les sociétés de l’Union européenne doivent déclarer leurs échanges avec les autres pays/régions de l’Union européenne. Vous devez déclarer les mouvements de marchandises aux autorités statistiques de votre pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Cette déclaration est appelée D.E.B. La page **Feuille intracomm.** permet de remplir des déclarations D.E.B. périodiques.  

## <a name="required-and-optional-setups"></a>Paramètres obligatoires et facultatifs
Avant d’utiliser la feuille intracommunautaire pour enregistrer des informations intracommunautaires, plusieurs éléments doivent être configurés :  

* **Configuration intracomm.**  : la page Configuration intracomm. permet d’activer la D.E.B. et de définir des valeurs par défaut. Vous pouvez spécifier si vous devez enregistrer la D.E.B. à partir des expéditions (répartitions), des réceptions (arrivées) ou des deux, selon les seuils définis par vos réglementations locales. Vous pouvez également définir des types de transaction par défaut pour les documents classiques et de retour, utilisés pour la nature des états de transaction.
* **Modèles de feuilles intracommunautaires**  : Vous devez configurer les modèles et les feuilles intracommunautaires que vous utiliserez. Comme l’état intracommunautaire doit être généré mensuellement, vous devez créer 12 feuilles intracommunautaires basées sur le même modèle.  
* **Codes marchandise**  : les autorités douanières et fiscales ont établi des codes numériques pour classer les articles et les services. Vous spécifiez ces codes sur les articles.
* **Codes nature de transaction**  : les pays et les régions ont différents codes pour les types de transactions intracommunautaires, comme l’achat et la vente ordinaires, l’échange de marchandises retournées et l’échange de marchandises non retournées. Configurez tous les codes qui s’appliquent à votre pays/région. Utilisez ces codes dans les documents achat et vente, et lorsque vous traitez des retours.  
* **Modes de transport** : Il existe, de sept codes à un chiffre pour les modes de transport intracommunautaire. **1** Mer, **2** Chemin de fer, **3** Route, **4** Air **5** Voie postale, **7** Transports fixes et **9** Propulsion propre (par exemple le transport en voiture en la conduisant). [!INCLUDE[d365fin](includes/d365fin_md.md)] ne requiert pas ces codes, cependant, il est préférable que les descriptions offrent une signification similaire.  

Éventuellement, vous pouvez également configurer :

* **Régimes** : Vous pouvez les utiliser pour renseigner les descriptions des types de transaction.  
* **Dépts destination/provenance** : Vous pouvez les utiliser pour renseigner des informations sur les pays et les régions.  
* **Pays destination/provenance** : Vous pouvez les utiliser pour spécifier les emplacements dans lesquels vous livrez ou recevez des articles vers ou à partir d’autres pays. L’aéroport de Heathrow est un exemple de pays destination/provenance. Vous pouvez saisir des points d’entrée et de sortie sur les documents vente et achat sur le raccourci **International** . Ces informations sont également copiées à partir des écritures article lorsque vous créez la feuille intracomm..  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Pour configurer des modèles et des feuilles intracommunautaires
Les lots de feuilles intracommunautaires incluent uniquement des écritures articles et non des écritures comptables. Si certaines écritures comptables doivent être inclues dans la D.E.B. vous devez les saisir manuellement. Par exemple, si vous achetez un ordinateur dans un autre pays/région de l’UE, cet ordinateur n’est pas comptabilisé dans le stock, mais validé dans un compte général. Vous devez saisir manuellement ce type d’écriture dans la feuille intracommunautaire.  

Vous pouvez exporter les écritures vers un fichier que vous pouvez envoyer à vos administrations intracommunautaires. Vous pouvez également imprimer un état, saisir manuellement les informations sur les formulaires de vos administrations, et envoyer les informations.

> [!Note]
> Nous vous recommandons de configurer un seul lot de feuilles intracommunautaires par mois.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles feuille intracomm.** , puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Créez un modèle pour chaque formulaire de D.E.B que vous utilisez.  
3. Pour créer des lots, sélectionnez l’action **Lots** .  
4. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Créez un modèle pour chaque formulaire de D.E.B que vous utilisez. 

> [!Note]
> Dans le champ **Période statistique** , entrez la période statistique sous la forme d’un nombre à quatre chiffres, les deux premiers chiffres représentant l’année et les deux suivants, le mois. Par exemple, saisissez 1706 pour juin 2017.

### <a name="to-set-up-commodity-codes"></a>Pour configurer des codes marchandise
Tous les articles que vous achetez ou vendez doivent avoir un code marchandise.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes marchandise** , puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Pour affecter un code marchandise à un article, accédez à la page **Fiche article** , développez le raccourci **Coûts et validation** , puis saisissez le code dans le champ **Code marchandise** .   

### <a name="to-set-up-transaction-nature-codes"></a>Pour configurer des codes nature de transaction
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes nature de transaction** , puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Si vous utilisez souvent un code nature de transaction spécifique, vous pouvez le définir comme valeur par défaut. Pour ce faire, accédez à la page **Configuration intracomm.** et choisissez le code.

### <a name="to-set-up-transport-methods"></a>Pour configurer des modes de transport
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modes de transport** , puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Pour configurer les champs de la D.E.B. obligatoires
Dans certains pays, tels que l’Espagne et le R-U, les autorités nécessitent que les états Intracomm. comprennent, par exemple, le mode d’expédition des achats ou d’autres valeurs lorsque les ventes sont supérieures à un certain seuil. Sur la page **Configuration intracomm.** , vous pouvez sélectionner pour faire **Paramètres liste de contrôle de la déclaration d’échanges de biens** pour définir les champs obligatoires sur la page **Feuille intracomm.** .

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration intracomm.** , puis sélectionnez le lien associé.
2. Choisissez l’action **Paramètres liste de contrôle de la déclaration d’échanges de biens** .
3. Sur la page **Paramètres liste de contrôle de la déclaration d’échanges de biens** , cliquez dans **Nom de champ** pour prélever le champ de déclaration d’échanges de biens que vous souhaitez rendre obligatoire.

## <a name="to-report-intrastat"></a>Pour enregistrer un état communautaire
Après avoir renseigné la feuille intracommunautaire, vous pouvez exécuter l’action **État : Liste de contrôle** pour vérifier que toutes les informations de la feuille sont correctes. Champs obligatoires que vous avez définis sur la page **Paramètres liste de contrôle de la déclaration d’échanges de biens** qui sont des valeurs manquante, seront affichés dans le récapitulatif des erreurs et d’avertissement de la page **Feuille intracomm.** . Ensuite, vous pouvez imprimer un état intracommunautaire en tant que formulaire, ou créer un fichier à envoyer à l’administration fiscale de votre pays/région.  

### <a name="to-fill-in-intrastat-journals"></a>Pour renseigner des feuilles intracommunautaires  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille intracomm.** , puis sélectionnez le lien associé.  
2. Sur la page **Feuille intracomm.** , dans le champ **Nom de la feuille** , sélectionnez la feuille concernée, puis sélectionnez **OK** .  
3. Choisissez l’action **Proposer lignes** . Les champs **Date début** et **Date fin** contiennent déjà les dates spécifiées sur la feuille pour la période statistique.  
4. Dans le champ **% régulation coût** , entrez un pourcentage pour couvrir le transport et l’assurance. Lorsque vous saisissez un pourcentage, la valeur du champ **Valeur statistique** de la feuille augmente proportionnellement.  
5. Cliquez sur **OK** pour démarrer le traitement par lots.  

Le traitement par lots récupère toutes les écritures article de la période statistique et les insère sous forme de lignes dans la feuille intracommunautaire. Vous pouvez modifier au besoin les nouvelles lignes.  

> [!IMPORTANT]  
>  Le traitement par lots récupère uniquement les écritures qui contiennent un code pays/région pour lequel un code intracommunautaire a été entré dans la page **Pays/Régions** . Vous devez donc entrer les codes intracommunautaires correspondant aux codes pays pour lesquels vous allez lancer le traitement par lots.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Enregistrer un état intracommunautaire sur un formulaire ou un fichier
Pour obtenir les informations requises sur le formulaire de D.E.B. à partir des autorités statistiques, vous devez imprimer l’état **D.E.B. : Formulaire** . Avant d’effectuer cette opération, vous devez préparer la feuille intracommunautaire et la renseigner. Si vous avez à la fois des transactions d’achat et de vente, vous devez compléter un formulaire distinct pour chaque type et donc imprimer l’état deux fois.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles intracomm.** , puis sélectionnez le lien associé.  
2. Sur la page **Feuille intracomm.** , choisissez la feuille concernée dans le champ **Nom de la feuille** .  
3. Si ce n’est déjà fait, renseignez la feuille manuellement ou sélectionnez l’action **Proposer lignes** .  
4. Choisissez l’action **Imprime la feuille intracomm.** .  
5. Sur le raccourci **Ligne feuille intracomm.** , ajoutez un filtre **Type** , puis spécifiez s’il s’agit d’une **Réception** ou d’une **Expédition** .  
6. Choisissez **Envoyer à** pour imprimer l’état.  

### <a name="report-intrastat-in-a-file"></a>Enregistrer un état intracommunautaire sur un fichier
Vous pouvez envoyer la déclaration d’échanges de biens en tant que fichier. Avant de créer le fichier, vous pouvez imprimer la liste de contrôle contenant les mêmes informations que le fichier.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille intracomm.** , puis sélectionnez le lien associé.  
2. Sur la page **Feuille intracomm.** , sélectionnez la feuille concernée dans le champ **Nom de la feuille** .  
3. Si ce n’est déjà fait, renseignez la feuille manuellement ou sélectionnez l’action **Proposer lignes** .  
4. Choisissez l’action **Créer fichier** .  
5. Dans la page de tâche par lot, sélectionnez le bouton **OK** .  
6. Choisissez **Enregistrer** .  
7. Sélectionnez l’emplacement d’enregistrement du fichier, entrez son nom, puis choisissez **Enregistrer** .

## <a name="reorganize-intrastat-journals"></a>Réorganiser les feuilles intracommunautaires
Parce que vous devez soumettre une D.E.B. chaque mois et créer une feuille pour chaque état, il peut donc exister de nombreuses feuilles. Les lignes feuille ne sont pas supprimées automatiquement. Vous pouvez réorganiser régulièrement les feuilles. Pour cela, il suffit de supprimer les feuilles dont vous n’avez plus besoin. Les lignes de ces feuilles sont également supprimées.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles intracomm.** , puis sélectionnez le lien associé.  
2. Pour afficher les options, choisissez le champ **Nom de la feuille** .  
3. Cliquez sur les feuilles à supprimer, puis sélectionnez le bouton **Supprimer** .  

## <a name="tariff-numbers"></a>Nomenclatures produits

Dans de nombreux pays, les autorités douanières et fiscales établissent des codes article à huit unités pour divers articles. Pour que les écritures article comportent les informations nécessaires lorsque le programme les importe vers la ligne feuille intracommunautaire, vous devez avoir saisi les informations concernant la nomenclature produit dans la page **Nomenclatures produits** . Trouvez les codes des articles avec lesquels votre société travaille et saisissez-les dans la fenêtre **Nomenclatures produits** .

Ajoutez tous les codes que vous utilisez dans la page **Nomenclatures produit** . Vous devez saisir les codes sur la fiche article avant de commencer à valider. Lorsque vous avez créé ces codes, saisissez-les dans le champ **Nomenclature produits** de la fiche article. Vous devez également renseigner le champ **Poids net** de la fiche article.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Gestion financière](finance.md)
