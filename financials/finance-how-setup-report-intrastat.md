---
title: "Procédure : configurer et enregistrer un état intracommunautaire | Microsoft Docs"
description: "Apprendre à configurer les fonctionnalités d'état intracommunautaire, et comment enregistrer les transactions avec des sociétés dans d'autres pays/régions."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b4fde6f005c992b63856ec4afadbb689532ac16
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="how-to-set-up-and-report-intrastat"></a>Procédure : configurer et enregistrer un état intracommunautaire
Toutes les sociétés de l'Union européenne doivent déclarer leurs échanges avec les autres pays/régions de l'Union européenne. Vous devez déclarer les mouvements de marchandises aux autorités statistiques de votre pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Cette déclaration est appelée D.E.B. La page **Feuille intracomm.** permet de remplir des déclarations D.E.B. périodiques.  

## <a name="required-and-optional-setups"></a>Paramètres obligatoires et facultatifs
Avant d'utiliser la feuille intracommunautaire pour enregistrer des informations intracommunautaires, plusieurs éléments doivent être configurés :  

* **Modèles de feuilles intracommunautaires** : Vous devez configurer les modèles et les feuilles intracommunautaires que vous utiliserez. Comme l'état intracommunautaire doit être généré mensuellement, vous devez créer 12 feuilles intracommunautaires basées sur le même modèle.  
* **Codes marchandise** : les autorités douanières et fiscales ont établi des codes numériques pour classer les articles et les services. Vous spécifiez ces codes sur les articles.
* **Codes nature de transaction** : les pays et les régions ont différents codes pour les types de transactions intracommunautaires, comme l'achat et la vente ordinaires, l'échange de marchandises retournées et l'échange de marchandises non retournées. Configurez tous les codes qui s'appliquent à votre pays/région. Utilisez ces codes dans les documents achat et vente, et lorsque vous traitez des retours.  
* **Modes de transport**: Il existe, de sept codes à un chiffre pour les modes de transport intracommunautaire. **1** Mer, **2** Chemin de fer, **3** Route, **4** Air **5** Voie postale, **7** Transports fixes et **9** Propulsion propre (par exemple le transport en voiture en la conduisant). [!INCLUDE[d365fin](includes/d365fin_md.md)] ne requiert pas ces codes, cependant, il est préférable que les descriptions offrent une signification similaire.  

Éventuellement, vous pouvez également configurer :

* **Régimes** : Vous pouvez les utiliser pour renseigner les descriptions des types de transaction.  
* **Dépts destination/provenance** : Vous pouvez les utiliser pour renseigner des informations sur les pays et les régions.  
* **Pays destination/provenance** : Vous pouvez les utiliser pour spécifier les emplacements dans lesquels vous livrez ou recevez des articles vers ou à partir d'autres pays. L'aéroport de Heathrow est un exemple de pays destination/provenance. Vous pouvez saisir des points d'entrée et de sortie sur les documents vente et achat sur le raccourci **International**. Ces informations sont également copiées à partir des écritures article lorsque vous créez la feuille intracomm..  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Pour configurer des modèles et des feuilles intracommunautaires
Les lots de feuilles intracommunautaires incluent uniquement des écritures articles et non des écritures comptables. Si certaines écritures comptables doivent être inclues dans la D.E.B. vous devez les saisir manuellement. Par exemple, si vous achetez un ordinateur dans un autre pays/région de l'UE, cet ordinateur n'est pas comptabilisé dans le stock, mais validé dans un compte général. Vous devez saisir manuellement ce type d'écriture dans la feuille intracommunautaire.  

Vous pouvez exporter les écritures vers un fichier que vous pouvez envoyer à vos administrations intracommunautaires. Vous pouvez également imprimer un état, saisir manuellement les informations sur les formulaires de vos administrations, et envoyer les informations.

>  [!Note]
> Nous vous recommandons de configurer un seul lot de feuilles intracommunautaires par mois.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Modèles feuille intracomm.**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Créez un modèle pour chaque formulaire de D.E.B que vous utilisez.  
3. Pour créer des feuilles, choisissez l'onglet **Naviguer**, puis choisissez **Noms feuilles**.  
4. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Créez un modèle pour chaque formulaire de D.E.B que vous utilisez.  

> [!Note]
> Dans le champ **Période statistique**, entrez la période statistique sous la forme d'un nombre à quatre chiffres, les deux premiers chiffres représentant l'année et les deux suivants, le mois. Par exemple, saisissez 1706 pour juin 2017.

### <a name="to-set-up-commodity-codes"></a>Pour configurer des codes marchandise
Tous les articles que vous achetez ou vendez doivent avoir un code marchandise.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Codes marchandise**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Pour affecter un code marchandise à un article, accédez à la page **Fiche article**, développez le raccourci **Coûts et validation**, puis saisissez le code dans le champ **Code marchandise**.   

### <a name="to-set-up-transaction-nature-codes"></a>Pour configurer des codes nature de transaction
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Codes nature de transaction**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Si vous utilisez souvent un code nature de transaction spécifique, vous pouvez le définir comme valeur par défaut. Pour ce faire, accédez à la page **Configuration intracomm.** et choisissez le code.

### <a name="to-set-up-transport-methods"></a>Pour configurer des modes de transport
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Modes de transport**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-report-intrastat"></a>Pour enregistrer un état communautaire
Après avoir renseigné la feuille intracommunautaire, vous pouvez imprimer l'état **Liste de contrôle** pour vérifier que toutes les informations de la feuille sont correctes. Ensuite, vous pouvez imprimer un état intracommunautaire en tant que formulaire, ou créer un fichier à envoyer à l'administration fiscale de votre pays/région.  

### <a name="to-fill-in-intrastat-journals"></a>Pour renseigner des feuilles intracommunautaires  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille intracomm.**, puis sélectionnez le lien connexe.  
2. Sur la page **Feuille intracomm.**, dans le champ **Nom de la feuille**, sélectionnez la feuille concernée, puis sélectionnez **OK**.  
3. Choisissez l'action **Proposer lignes**. Les champs **Date début** et **Date fin** contiennent déjà les dates spécifiées sur la feuille pour la période statistique.  
4. Dans le champ **% régulation coût**, entrez un pourcentage pour couvrir le transport et l'assurance. Lorsque vous saisissez un pourcentage, la valeur du champ **Valeur statistique** de la feuille augmente proportionnellement.  
5. Cliquez sur **OK** pour démarrer le traitement par lots.  

Le traitement par lots récupère toutes les écritures article de la période statistique et les insère sous forme de lignes dans la feuille intracommunautaire. Vous pouvez modifier au besoin les nouvelles lignes.  

> [!IMPORTANT]  
>  Le traitement par lots récupère uniquement les écritures qui contiennent un code pays/région pour lequel un code intracommunautaire a été entré dans la page **Pays/Régions**. Vous devez donc entrer les codes intracommunautaires correspondant aux codes pays pour lesquels vous allez lancer le traitement par lots.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Enregistrer un état intracommunautaire sur un formulaire ou un fichier
Pour obtenir les informations requises sur le formulaire de D.E.B. à partir des autorités statistiques, vous devez imprimer l'état **D.E.B. : Formulaire**. Avant d'effectuer cette opération, vous devez préparer la feuille intracommunautaire et la renseigner. Si vous avez à la fois des transactions d'achat et de vente, vous devez compléter un formulaire distinct pour chaque type et donc imprimer l'état deux fois.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille intracomm.**, puis sélectionnez le lien connexe.  
2. Sur la page **Feuille intracomm.**, choisissez la feuille concernée dans le champ **Nom de la feuille**.  
3. Si ce n'est déjà fait, renseignez la feuille manuellement ou sélectionnez **Proposer lignes**.  
4. Choisissez l'action **Imprime la feuille intracomm.**.  
5. Sur le raccourci **Ligne feuille intracomm.**, ajoutez un filtre **Type**, puis spécifiez s'il s'agit d'une **Réception** ou d'une **Expédition**.  
6. Choisissez **Envoyer à** pour imprimer l'état.  

### <a name="report-intrastat-in-a-file"></a>Enregistrer un état intracommunautaire sur un fichier
Vous pouvez envoyer la déclaration d'échanges de biens en tant que fichier. Avant de créer le fichier, vous pouvez imprimer la liste de contrôle contenant les mêmes informations que le fichier.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille intracomm.**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Feuille intracomm.**, sélectionnez la feuille concernée dans le champ **Nom de la feuille**.  
3. Si ce n'est déjà fait, renseignez la feuille manuellement ou en sélectionnant **Proposer lignes**.  
4. Choisissez l'action **Créer fichier**.  
5. Dans la fenêtre de traitement par lots, choisissez **OK**.  
6. Choisissez **Enregistrer**.  
7. Sélectionnez l'emplacement d'enregistrement du fichier, entrez son nom, puis choisissez **Enregistrer**.

## <a name="reorganize-intrastat-journals"></a>Réorganiser les feuilles intracommunautaires
Parce que vous devez soumettre une D.E.B. chaque mois et créer une feuille pour chaque état, il peut donc exister de nombreuses feuilles. Les lignes feuille ne sont pas supprimées automatiquement. Vous pouvez réorganiser régulièrement les feuilles. Pour cela, il suffit de supprimer les feuilles dont vous n'avez plus besoin. Les lignes de ces feuilles sont également supprimées.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille intracomm.**, puis sélectionnez le lien connexe.  
2. Pour afficher les options, choisissez le champ **Nom de la feuille**.  
3. Cliquez sur les feuilles à supprimer, puis choisissez **Supprimer**.  

## <a name="see-also"></a>Voir aussi
[Gestion financière](finance.md)

