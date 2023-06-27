---
title: Paramétrer les états intracommunautaires
description: Cet article explique comment configurer les fonctionnalités d’états intracommunautaires pour enregistrer les transactions avec des sociétés dans d’autres pays/régions.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# <a name="set-up-intrastat-reporting"></a>Paramétrer les états intracommunautaires

Toutes les sociétés de l’Union européenne (UE) doivent déclarer leurs échanges avec les autres pays/régions de l’Union européenne. Les sociétés doivent déclarer les mouvements de marchandises aux autorités statistiques de leur pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Intrastat est le système de collecte des statistiques du commerce des biens au sein de ces pays/régions. Utilisez un État intracommunautaire pour effectuer des déclarations intracommunautaires périodiques en collectant, enregistrant et déclarant le commerce de biens conformément à la législation locale.

La déclaration des états intracommunautaires est basée sur les réglementations de base de l’UE qui s’appliquent à tous les pays. Cependant, il existe des différences au sein des différents pays. Chaque pays a ses règles édictant quoi déclarer et comment.

> [!NOTE]
> Les informations des états intracommunautaires ne s’appliquent pas au mouvement de services entre pays. Au lieu de cela, les informations ne s’appliquent qu’aux biens tels que les articles et les immobilisations. Si votre gouvernement exige que vous enregistriez le mouvement des services entre les pays, utilisez la fonctionnalité **Déclaration de service**.
>
> Cette fonctionnalité est disponible depuis novembre 2022, sous la forme d’une application que vous pouvez télécharger sur [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Pour utiliser cette fonctionnalité, installez-la sur la page **Gestion des extensions**.

> [!IMPORTANT]
> Cet article couvre la nouvelle expérience des états intracommunautaires disponible à partir de [!INCLUDE[prod_short](includes/prod_short.md)], version 21. Consultez votre administrateur pour savoir quelle version votre entreprise utilise et si vous devez activer la nouvelle fonctionnalité.
>
> Lisez l’article sur la configuration et l’utilisation des états intracommunautaires de la version précédente ici : [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Activer la nouvelle expérience d’états intracommunautaires

Dans la 2è vague de lancement 2022, [!INCLUDE[prod_short](includes/prod_short.md)] inclut une expérience d’échanges intracommunautaires qui fournit des fonctionnalités étendues. Si la nouvelle fonctionnalité d’états intracommunautaires n’est pas activée dans votre environnement, un administrateur peut l’activer manuellement sur la page **Gestion des fonctionnalités**.

> [!IMPORTANT]
> Vous ne pouvez pas utiliser l’ancienne et la nouvelle expérience en parallèle. Avant d’activer l’extension dans un environnement de production, nous vous recommandons de la d’abord dans un environnement sandbox avec une copie de vos données de production. Une fois que vous avez activé une nouvelle expérience utilisateur dans votre environnement de production, vous ne pouvez pas revenir à l’ancienne fonctionnalité d’états intracommunautaires.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des fonctionnalités** et sélectionnez le lien associé.
2. Sur la page **Gestion des fonctionnalités**, sélectionnez la ligne **Mise à jour des fonctionnalités : remplacer la fonctionnalité intracommunautaire existante par la nouvelle extension intracommunautaire**. Pour en savoir plus sur la gestion des fonctionnalités, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Dans la colonne **Activer pour**, sélectionnez **Tous les utilisateurs**.
4. Lisez l’explication concernant la façon dont le système sera mis à niveau, puis sélectionnez **Oui** pour l’accepter.
5. Sélectionnez **Suivant**. Vous obtiendrez la configuration de base pour les états intracommunautaires. Pour en savoir plus sur la configuration des états intracommunautaires, consultez la section [Configuration des états intracommunautaires](#intrastat-configuration) plus loin dans cet article.
6. Une fois la configuration terminée, sélectionnez **Terminer** pour commencer à utiliser la nouvelle expérience des états intracommunautaires.

    > [!NOTE]
    > Selon l’emplacement de votre entreprise, l’activation de la fonctionnalité décrite ci-dessus sera suffisante. Pour les pays dotés de fonctionnalités spécifiques pour la déclaration des états intracommunautaires, activez l’application d’états intracommunautaires spécifique au pays en plus de l’extension principale.

## <a name="intrastat-configuration"></a>Configuration des états intracommunautaires

Avant de pouvoir utiliser les états intracommunautaires, plusieurs configurations doivent être configurées.

### <a name="intrastat-reporting-setup"></a>Paramétrer les états intracommunautaires

Utilisez la page **Paramétrer les états intracommunautaires** pour activer et configurer le comportement par défaut pour les états intracommunautaires. Vous pouvez spécifier si vous devez enregistrer les états intracommunautaires à partir des expéditions (répartitions), des réceptions (arrivées) ou des deux, selon les seuils définis par vos réglementations locales. Vous pouvez également définir des types de transaction par défaut pour les documents classiques et de retour utilisés pour les états de transaction.

Procédez comme suit pour configurer les états intracommunautaires.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les états intracommunautaires**, puis sélectionnez le lien associé.
2. Dans le raccourci **Général**, sélectionnez ou saisissez les informations des champ nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau suivant décrit certains des champs clés.

   | Champ | Désignation |
   | --- | --- |
   | **Réceptions d’état** | Spécifie que vous devez inclure les arrivages de marchandises reçues dans les déclarations d’échanges intracomm. |
   | **Déclarer les expéditions** | Spécifie que vous devez inclure les expéditions de marchandises réparties dans les états intracomm. |
   | **Expéditions basées sur**  | Spécifie le code pays sur la base duquel les lignes des états intracommunautaires sont extraites.  |
   | **N° TVA basé sur** | Spécifie le code client ou fournisseur sur la base duquel le numéro de taxe à la valeur ajoutée (TVA) est utilisé pour l’état intracommunautaire.  |
   | **N° TVA société du fichier** | Spécifie comment le numéro d’immatriculation de TVA de la société est exporté vers le fichier d’état intracommunautaire.  |
   | **N° TVA fournisseur du fichier** | Spécifie comment le numéro d’immatriculation de TVA du fournisseur est exporté vers le fichier d’état intracommunautaire.  |
   | **N° TVA client du fichier** | Spécifie comment le numéro d’immatriculation de TVA du client est exporté vers le fichier d’état intracommunautaire.  |
   | **Obtenir TVA partenaire pour** | Spécifie à partir de quel type de ligne de l’état intracommunautaire le numéro d’immatriculation de TVA du partenaire est mis à jour. En fonction de vos exigences locales, vous pouvez choisir les lignes de réception uniquement, les lignes d’expédition uniquement, ou les deux types de ligne. |

3. Dans le raccourci **Transactions par défaut** , sélectionnez ou saisissez les informations des champ nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau suivant décrit certains des champs clés.

   | Champ | Désignation |
   | --- | --- |
   | **Type de trans. par défaut** | Spécifie le type de transaction par défaut pour les expéditions vente régulières, les expéditions de service et les réceptions achat enregistrées. |
   | **Type de trans. par défaut – Retours** | Spécifie le type de transaction par défaut pour les retours vente, les retours de service et les retours achat. |
   | **N° TVA privée par défaut** | Spécifie le numéro de TVA de la personne privée par défaut, si la personne privée doit avoir un numéro de TVA dédié sur l’état intracommunautaire. |
   | **N° TVA commerciale tierce partie par défaut** | Spécifie le numéro de TVA commerciale de la tierce partie par défaut, si vous n’avez pas son numéro de TVA. |
   | **TVA par défaut pour état inconnu** | Spécifie le numéro de TVA par défaut d’un état inconnu. |
   | **Code pays/région par défaut** | Spécifie le code du pays de réception par défaut. |

4. Dans le raccourci **Déclaration**, sélectionnez ou saisissez les informations des champ nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau suivant décrit certains des champs clés.

   | Champ | Désignation |
   | --- | --- |
   | **Code déf. échge données** | Spécifie le code de définition d’échange de données pour générer le fichier intracommunautaire. Ce champ n’est disponible que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Non**. |
   | **Fractionner les fichiers réceptions/expéditions** | Indique si les réceptions et les expéditions doivent être enregistrées dans deux fichiers séparés. |
   | **Fichier zip (-s)** | Indique si les fichiers d’état doivent être ajoutés au fichier .zip. |
   | **Code déf. échange données – Réception** | Spécifie le code de définition d’échange de données pour générer le fichier d’état intracommunautaire pour les biens reçus. Ce champ n’est disponible que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Oui**. |
   | **Code déf. échange données – Expédition** | Spécifie le code de définition d’échange de données pour générer le fichier d’état intracommunautaire pour les biens expédiés. Ce champ n’est disponible que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Oui**. |

5. Dans le raccourci **Numérotation** , saisissez une valeur dans le champ **N° intracommunautaires**.

### <a name="set-up-a-reporting-file"></a>Configurer un fichier de déclaration

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Définitions d’échange de données** et sélectionnez le lien associé.
2. Sélectionnez **Nouveau** puis, dans le raccourci **Général**, entrez les informations sur la définition d’échange de données, le type de fichier de données, le séparateur de colonnes, les codeunits associée, XMLport et autres champs selon les besoins.
3. Sur le raccourci **Définitions de ligne**, entrez une valeur dans le champ **Type de ligne** pour décrire le formatage des lignes du fichier de données et où vous devez définir le nombre de colonnes pour cette ligne.
4. Sur le raccourci **Définitions de colonne**, remplissez la ligne pour chaque colonne planifiée. Vous pouvez définir des noms de colonnes, des types de données (Texte, Date ou Décimal), la longueur de la ligne à largeur fixe qui contient la colonne si le fichier est de type *Texte fixe*, et quelques autres paramètres.
5. Dans le raccourci **Définitions de ligne**, sélectionnez **Mappage de champ**.
6. Sur la page **Mappage des champs** , créez une nouvelle entrée. 
7. Dans le raccourci **Général** , sélectionnez la valeur **ID de table** (pour **Ligne d’états intracommunautaires**, sélectinnez **4812**), et saisissez les informations de champ suivantes :

   1. Dans le champ **Index de clé**, indiquez l’index de clé pour trier les enregistrements source avant l’exportation.
   2. Dans le champ **Codeunit de mappage**, sélectionnez une valeur.

8. Sur le raccourci **Mappage des champs**, ajoutez les colonnes que vous avez précédemment configurées dans le raccourci **Définitions de colonne**, puis ajoutez les informations des champs suivants :

   1. Spécifiez la valeur **ID de champ** pour chacune des colonnes.
   2. Spécifiez la valeur **Règle de transformation** pour chaque colonne au besoin. Cette valeur spécifie la règle qui transforme un texte importé en valeur prise en charge avant de pouvoir être mappé dans un champ spécifié dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous sélectionnez une valeur dans ce champ, la valeur exacte est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données** . (Inversement, lorsqu’une valeur exacte est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données**, une valeur est choisie dans ce champ.)

9. Si vous devez regrouper des entrées en fonction de certaines colonnes, sur le raccourci **Groupement de champs**, sélectionnez les champs que vous souhaitez utiliser pour le regroupement.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] est livré avec la définition d’échange de données préconfigurée pour les états intracommunautaires pour tous les pays pour lesquels la traduction a été faite. Pour en savoir plus sur la création d’une définition d’échange de données, consultez [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Définir les champs obligatoires avec la liste de contrôle des états intracommunautaires

Dans certains pays, les autorités nécessitent que les états intracommunautaires comprennent, par exemple, le mode d’expédition des achats ou d’autres valeurs lorsque les ventes sont supérieures à un certain seuil.

Pour définir des champs et/ou des valeurs obligatoires sur la page **État intracommunautaire**, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les états intracommunautaires**, puis sélectionnez le lien associé.
2. Sélectionnez **Liste de contrôle des états intracommunautaires**.
3. Procédez comme suit pour ajouter les lignes nécessaires à la vérification :
   1. Définissez le champ **N° champ** sur un champ qui doit être vérifié pour une valeur non vide.
   2. Entrez une valeur dans le champ **Expression de filtre** si nécessaire, selon les règles suivantes :

        1. Lorsque vous ouvrez la **Page de filtres**, sélectionnez le Filtre dont vous avez besoin pour la vérification.
        2. Sélectionnez une valeur associée au filtre sélectionné.
        3. Si vous devez remplir plus de filtres pour le champ choisi, répétez les deux étapes précédentes pour ajouter un autre filtre.
        4. Lorsque vous avez fini de saisir les filtres pour le champ choisi, sélectionnez **OK**.

   3. Cochez la case **Expression filtre inversé** pour indiquer que la vérification des champs n’est exécutée que sur les lignes qui ne correspondent pas à l’expression du filtre. Si la ligne n’est pas filtrée, ce champ est ignoré.

> [!NOTE]
> Lorsque vous ouvrez la **Page des filtres** depuis la ligne **Expression de filtre**, vous pouvez utiliser toutes les expressions de filtre standard liées au champ spécifique que vous souhaitez filtrer.
>
> Soyez prudent lorsque vous configurez des règles de validation, car elles peuvent différer d’un pays à l’autre.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Utiliser des codeunits personnalisés dans les états intracommunautaires

Si vous souhaitez modifier le fonctionnement des états intracommunautaires et que la configuration par défaut ne suffit pas, vous pouvez personnaliser le système en étendant les fonctionnalités standard. Si vous avez besoin de modifier davantage le comportement des états intracommunautaires, vous pouvez développer vos propres codeunits. Lorsque vous créez des codeunits, vous devez apporter des modifications supplémentaires pour les utiliser. Pour configurer le système de manière à utiliser vos propres objets, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration des déclarations de TVA**, puis sélectionnez le lien associé.
2. Dans la page **Configuration des déclarations de TVA**, ajoutez une nouvelle ligne.
3. Dans le champ **Type de déclaration de TVA**, sélectionnez **État intracommunautaire**.
4. Dans le champ **Version de la déclaration de TVA**, indiquez la version de la déclaration.
5. Ajoutez vos codeunits pour les options suivantes :
   1. Dans le champ **ID Codeunit fonction Proposer lignes**, spécifiez le nouveau codeunit pour suggérer des lignes dans les lignes des états intracommunautaires.
   2. Dans le champ **ID Codeunit de contenu**, spécifiez le nouveau codeunit pour exporter les données sous forme de fichier à l’aide d’une définition d’échange de données.
   3. Dans le champ **ID Codeunit fonction Valider**, spécifiez les nouveaux codeunits pour valider les résultats dans les lignes des états intracommunautaires.

> [!IMPORTANT]
> Cette ligne doit être vide si vous utilisez les codeunits standard. Vous ne devez créer une ligne et la configurer que si vous avez développé des codeunits personnalisés.

## <a name="other-intrastat-configurations"></a>Autres configurations des états intracommunautaires

Les fiches client et les fiches fournisseur incluent un champ, **Type de partenaire intracommunautaire**, qui a les mêmes valeurs d’option que le champ **Type de partenaire** : 

- "" (vide)
- *Société*
- *Personne*
    
Le champ **Type de partenaire intracommunautaire** a remplacé le champ **Type de partenaire** dans la déclaration intracommunautaire. Le champ **Type de partenaire** est utilisé dans l’Espace unique de paiement en euros (SEPA) pour définir le schéma de prélèvement SEPA (Core ou B2B). Le champ **Type de partenaire intracommunautaire** est utilisé pour les états intracommunautaires uniquement. Par conséquent, vous pouvez spécifier des valeurs différentes pour les deux champs, si nécessaire.

Si le champ **Type de partenaire dintracommunautaire** est laissé vide, la valeur du champ **Type de partenaire** est utilisée pour la déclaration d’échanges de biens.

En plus des options **Paramétrer les états intracommunautaires**, **Définitions d’échange de données**, et **Liste de contrôle des états intracommunautaires**, vous devez également configurer les paramètres suivants.

| Page | Désignation |
| ---- | ----------- |
| **Pays/Régions** | Sur la page **Pays/Régions**, ajoutez les informations **Code pays/région de l’UE** et **Code intracommunautaire** pour spécifier un code pour le pays/la région avec lequel vous commercez. Ces informations seront utilisées dans les états intracommunautaires. |
| **Nomenclatures produits** | Dans de nombreux pays, les autorités douanières et fiscales établissent des codes à huit chiffres pour divers articles. Pour que les écritures article puissent contenir les informations nécessaires lorsque le programme les importe dans la ligne feuille intracommunautaire, entrez le code article dans la page **Nomenclatures produits**. Trouvez les codes des articles avec lesquels votre société travaille et saisissez-les dans la page **Nomenclatures produits**. |
| **Modes de transport** | Il existe sept codes à un chiffre pour les modes de transport intracommunautaires : **1** pour la mer, **2** pour le rail, **3** pour la route, **4** pour l’air, **5** pour la poste, **7** pour les installations fixes, et **9** pour la propulsion propre (par exemple, transporter une voiture en la conduisant). [!INCLUDE[prod_short](includes/prod_short.md)] ne nécessite pas ces codes spécifiques. Cependant, nous recommandons que les descriptions aient une signification similaire. |
| **Types transaction** | Les pays et les régions ont différents codes pour les types de transactions intracommunautaires, comme l’achat et la vente ordinaires, l’échange de marchandises retournées et l’échange de marchandises non retournées. Configurez tous les codes qui s’appliquent à votre pays/région. Ces codes seront ensuite utilisés sur le raccourci **International** pour les documents achat et vente, et lorsque vous traitez des retours. |
| **Régimes** | Configurez des codes pour compléter les descriptions des types de transaction. |
  
> [!NOTE]
> À partir de janvier 2022, les états intracommunautaires exigent des codes de nature de transaction différent pour les envois aux particuliers ou aux entreprises non assujetties à la TVA et aux entreprises assujetties à la TVA. Pour se conformer à cette exigence, nous vous recommandons de revoir et/ou d’ajouter de nouveaux codes de nature de transaction dans la page **Types de transactions**, selon les exigences de votre pays. Vous devriez également revoir et mettre à jour le champ **Type de partenaire dintracommunautaire** sur *Personne* pour les clients particuliers ou les entreprises non assujetties à la TVA dans la page **Client**. Si vous n’êtes pas sûr du type de partenaire intracommunautaire ou de transaction correct à utiliser, nous vous recommandons de demander à un expert de votre pays ou votre région.

|   Champ   |   Désignation   |
| --------- | --------------- |
| **Poids net** | Le poids est l’une des configurations de base liées aux états intracommunautaires, car le poids total est obligatoire dans les déclarations. Pour être prêt pour cette exigence, entrez une valeur dans le champ **Poids net** sur la fiche de l’article ou de l’immobilisation. |
| **Code pays origine** | Utilisez les codes ISO Alpha à deux lettres sur la fiche article ou immobilisation pour le pays où le bien a été obtenu ou produit. Si le bien a été produit dans plusieurs pays, le pays d’origine est le dernier pays où il a été transformé de manière significative. |
| **Numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation** | Il s’agit du numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation. Le numéro de TVA est également utilisé dans l’échange de données d’exportation intra-UE entre les États membres et permet aux États membres d’attribuer les données reçues à la société importatrice dans leur propre pays. Les unités chargées des déclarations doivent déclarer le numéro de TVA de l’entreprise qui a déclaré l’acquisition intra-Union de biens dans l’État membre d’importation. |

Éventuellement, vous pouvez également configurer :

* **Codes marchandise** : les autorités douanières et fiscales ont établi des codes numériques pour classer les articles et les services. Vous pouvez spécifier ces codes sur les articles.
* **Dépts destination/provenance** : informations supplémentaires sur les pays et les régions.
* **Points d’entrée/sortie** : spécifiez les emplacements dans lesquels vous livrez ou recevez des articles vers ou à partir d’autres pays. Un aéroport est un exemple de point d’entrée ou de sortie. Vous pouvez saisir des points d’entrée et de sortie sur les documents vente et achat sur le raccourci **International**. Ces informations sont copiées à partir des écritures article lorsque vous créez la feuille intracommunautaire.
* **Unité de mesure supplémentaire** : la quantité de marchandises pour l’état intracommunautaire peut être soit le poids net (en kilogrammes), soit une unité supplémentaire. Si des unités supplémentaires sont requises, vous devez les configurer pour les articles et les immobilisations.

#### <a name="set-up-transport-methods"></a>Configurer les modes de transport

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modes de transport**, puis sélectionnez le lien associé.
2. Renseignez les informations des champs si nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Configurer les codes nature de transaction

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Types de transactions**, puis sélectionnez le lien associé.
2. Renseignez les informations des champs si nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Autres configurations associées

Avant d’utiliser la fonction d’états intracommunautaires, vous devez définir des champs sur les fiches article, immobilisation, client et fournisseur.

#### <a name="item-cards"></a>Fiches article

Suivez ces étapes pour configurer toutes les informations nécessaires aux états intracommunautaires sur les fiches article.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé.
2. Sélectionnez l’article que vous souhaitez configurer.
3. Dans le raccourci **Coûts et validation**, dans les champs **Nomenclature produits**, **Unité de mesure supplémentaire** et **Code pays/région d’origine**, entrez une valeur.

    > [!NOTE]
    > Pour utiliser une unité de mesure en complément de l’unité de mesure de base, configurez l’unité de mesure supplémentaire sur la page **Unités article**.

4. Dans le raccourci **Stock**, dans le champ **Poids net**, entrez ue valeur au format décimal.

> [!NOTE]
> Lorsque vous ajoutez la nomenclature produits à une unité de mesure définie pour l’article, [!INCLUDE [prod_short](includes/prod_short.md)] remplit automatiquement le champ **Unité de mesure supplémentaire** en fonction de la configuration de la nomenclature produits. Vous pouvez modifier la valeur du champ **Unité de mesure supplémentaire** selon les besoins.

#### <a name="set-up-fixed-assets-for-intrastat"></a>Configurer les immobilisations pour les états intracommunautaires

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis sélectionnez le lien associé.
2. Sélectionnez l’immobilisation à configurer.
3. Dans le raccourci **Intracommunautaire** dans les champs **Nomenclature produit**, **Poids net** et **Unité de mesure supplémentaire**, entrez une valeur.

> [!NOTE]
> Vous pouvez utiliser différentes unités de mesure comme unité de mesure supplémentaire. Mais quel que **Code Unité de mesure** que vous choisissiez, sa **Quantité** dans les états intracommunautaires sera toujours 1.

#### <a name="set-up-vendors-for-intrastat"></a>Paramétrer les fournisseurs pour les états intracommunautaires

Avant de pouvoir inclure un fournisseur dans les états intracommunautaires, saisissez ses informations sur la page **Fiche fournisseur**. Par exemple, spécifiez une valeur **Code pays/région** et une valeur **Numéro d’immatriculation de TVA**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis sélectionnez le lien associé.
2. Sélectionnez le fournisseur que vous souhaitez configurer.
3. Sur le raccourci **Intracommunautaire**, dans les champs **Type de trans. par défaut**, **Type de trans. par défaut - Retours**, et **Mode de transport par défaut**, définissez une valeur par défaut pour chaque champ.
4. Dans le raccourci **Paiements** , dans le champ **Type de partenaire dintracommunautaire** , indiquez si le fournisseur est une personne ou une entreprise.

#### <a name="set-up-customers-for-intrastat"></a>Paramétrer les clients pour les états intracommunautaires

Avant de pouvoir inclure un client dans les états intracommunautaires, saisissez ses informations sur la page **Fiche client**. Par exemple, vous devez spécifier une valeur **Code pays/région** et une valeur **Numéro d’immatriculation de TVA**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis sélectionnez le lien associé.
2. Sélectionnez le client que vous souhaitez configurer.
3. Sur le raccourci **Intracommunautaire**, dans les champs **Type de trans. par défaut**, **Type de trans. par défaut - Retours**, et **Mode de transport par défaut**, définissez la valeur par défaut pour chaque champ.
4. Dans le raccourci **Paiements** , dans le champ **Type de partenaire dintracommunautaire** , indiquez si le fournisseur est une personne ou une entreprise.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Exclure des articles et des immobilisations d’un état intracommunautaire

S’il existe une raison d’exclure un article ou une immobilisation spécifique de l’état intracommunautaire, modifiez l’option sur sa fiche.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Exclure un article de l’état intracommunautaire

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé.
2. Sélectionnez l’article que vous souhaitez configurer, puis, dans le raccourci **Coût et Comptabilité**, cochez la case **Exclure de l’état intracommunautaire** .

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Exclure une immobilisation d’un état intracommunautaire

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis sélectionnez le lien associé.
2. Sélectionnez l’immobilisation à configurer.
3. Dans le raccourci **Intracommunautaire**, cochez la case **Exclure de l’état intracommunautaire**.

#### <a name="set-up-tariff-numbers"></a>Paramétrer les nomenclatures produits

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Nomenclatures produits**, puis sélectionnez le lien associé.  
2. Dans la page **Nomenclatures produits**, renseignez les champs comme indiqué dans le tableau suivant.

    | Champ | Désignation |  
    |-------|-------------|
    | **N°** | Indique la nomenclature produits. |
    | **Description** | Indique une description de la nomenclature produits associée. |
    | **Unités supplémentaires** | Spécifie si les administrations douanières et fiscales demandent des informations sur la quantité et l’unité de mesure pour cet article. |
    | **Facteur de conversion** | Spécifie le facteur de conversion pour la nomenclature produits. |
    | **Unité** | Spécifie l’unité de la nomenclature produits. |

> [!NOTE]
> Si vous ajoutez une unité de mesure supplémentaire, [!INCLUDE [prod_short](includes/prod_short.md)] vous demande si vous souhaitez mettre à jour les articles associés. Si vous sélectionnez de mettre à jour les articles associés, la valeur **Unité de mesure** sur la page **Unités article** est mise à jour pour tous les articles qui ont la même nomenclature produits.
> 
> Lorsque vous ajoutez une nomenclature produits qui a une valeur **unité de mesure** définie à l’article, [!INCLUDE [prod_short](includes/prod_short.md)] ajoute automatiquement une nouvelle unité de mesure à la valeur **Unités article** de l’article. La valeur **Qté. par unité de mesure** est basée sur le champ **Précision arrondi quantité**.

## <a name="enter-country-specific-intrastat-settings"></a>Saisir les paramètres intracommunautaires spécifiques au pays

Les exigences intracommunautaires sont similaires dans tous les États membres de l’UE, bien qu’il existe des exceptions importantes. En théorie, les règles devraient être appliquées uniformément dans tous les États membres. Cependant, il existe des différences dans leur application car certains États membres fournissent des directives quant à l’application des principes dans des situations particulières (par exemple, les échantillons commerciaux et les retours de marchandises). Ces directives peuvent produire des résultats différents pour diverses situations. Par conséquent, les informations que les pays doivent saisir peuvent différer, tout comme le format de fichier qu’ils doivent utiliser pour les états.

### <a name="austria"></a>Autriche

Les états intracommunautaires en Autriche nécessitent deux fichiers différents pour les réceptions et les expéditions. Pour vérifier que votre configuration est correcte, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les états intracommunautaires**, puis sélectionnez le lien associé.  
2. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné. Si c’est le cas, vous trouverez deux valeurs **Codes déf. échge données** configurées. 
3. Vérifiez que le champ **Fichier(s) zip** est sélectionné pour vous assurer que les fichiers d’état seront ajoutés au fichier zip.

Le processus de travail avec les états intracommunautaires est le même que celui de la fonctionnalité globale.

<!-- ### Belgium-->

### <a name="czech-republic"></a>République tchèque

La nouvelle expérience d’états intracommunautaires pour la République tchèque sera disponible dans la 1e vague de lancement 2023. En attendant, continuez à utiliser la fonctionnalité **Feuille intracomm.**.

### <a name="finland"></a>Finlande

En Finlande, il y a quelques étapes supplémentaires pour configurer les états intracomm. Les états intracommunautaires en Finlande nécessitent deux fichiers différents pour les réceptions et les expéditions. Vous constaterez également qu’il existe deux valeurs **Code déf. échge données** configurées.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les états intracommunautaires**, puis sélectionnez le lien associé.  
2. Sur la page **Configuration des états intracommunautaires**, sur le raccourci **Configuration des fichiers**, renseignez les champs comme indiqué dans le tableau suivant.

    |                 Champ              |            Désignation                |  
    |------------------------------------|---------------------------------------|
    | **Code personnalisé** | Spécifie un code personnalisé pour les informations de configuration du fichier d’échanges intracomm.. |
    | **N° de série de l’entreprise** | Spécifie un numéro de série de l’entreprise pour les informations de configuration du fichier d’échanges intracomm.. |

3. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné.

Le processus de travail avec les états intracomm. est le même que la fonctionnalité globale.

<!-- ### Germany-->

### <a name="italy"></a>Italie

Une nouvelle expérience des états intracommunautaires pour l’Italie sera disponible à partir de février 2023. En attendant, continuez à utiliser la fonctionnalité **Feuille intracomm.**.

<!-- ### France-->

### <a name="sweden"></a>Suède

Les états intracommunautaires en Suède nécessitent deux fichiers différents pour les réceptions et les expéditions. Pour vérifier que votre configuration est correcte, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les états intracommunautaires**, puis sélectionnez le lien associé.  
2. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné. Si c’est le cas, vous trouverez deux valeurs **Codes déf. échge données** configurées.

Le processus de travail avec les états intracommunautaires est le même que dans la fonctionnalité globale.

<!-- ### United Kingdom-->

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Voir aussi

[Génération d’état intracommunautaire dans Business Central](finance-how-report-intrastat.md)  
[Gestion financière](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
