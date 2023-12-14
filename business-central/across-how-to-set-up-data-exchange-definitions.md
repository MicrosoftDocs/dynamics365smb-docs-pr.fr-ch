---
title: Définir le mode d’échange électronique de documents
description: 'Définissez comment Business Central échange des données avec des fichiers externes tels que des documents électroniques, des données bancaires, des catalogues d’articles, etc.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# Configurer les définitions d’échange de données

Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour échanger des données dans des tables spécifiques avec des données de fichiers externes. Par exemple, pour envoyer et recevoir des documents électroniques, importer et exporter des données bancaires ou d’autres données, telles que les données de paie et des catalogues d’articles. Pour plus d’informations, consultez [Échanger des données par voir électronique](across-data-exchange.md).  

Pour créer une définition d’échange de données pour un fichier ou un flux de données, vous pouvez utiliser le schéma XML associé pour les définir les éléments de données à inclure dans le raccourci **Définitions de colonnes**. Consultez l’étape 6 dans la section [Décrire le formatage de lignes et de colonnes dans un fichier](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Pour plus d’informations, consultez [Utiliser des schémas XML pour préparer des définitions d’échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Normalement, vous configurez des définitions d’échange de données sur la page **Définition d’échange de données**. Cependant, pour mettre à jour les taux de change, il est plus rapide d’utiliser un service de taux de change. Pour plus d’informations, consultez [Mettre à jour des taux de change devise](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Si le fichier converti est au format XML, le terme *« colonne »* de cet article doit être interprété comme *« élément XML contenant des données »*.  

Cet article couvre les procédures suivantes :  

* Créer une définition d’échange de données.
* Exporter une définition d’échange de données au format XML pour utilisation par d’autres.
* Importer un fichier XML pour une définition d’échange de données existante.

## Créer une définition d’échange de données

La création d’une définition d’échange de données implique deux tâches :  

1. Sur la page **Définition d’échange de données**, décrivez la mise en forme des lignes et des colonnes du fichier. Pour plus d’informations, consultez la section [Décrire le formatage de lignes et de colonnes dans un fichier](#formatlinescolumns).  
2. Sur la page **Mappage d’échange de données**, mappez les colonnes du fichier de données aux champs de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez la section [Mapper les colonnes du fichier de données sur les champs de [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name=formatlinescolumns></a>Pour décrire le formatage des lignes et des colonnes dans le fichier

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Définitions d’échange de données**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Sur le raccourci **Général**, décrivez la définition d’échange de données et le type de fichier de données en renseignant les champs comme indiqué dans le tableau suivant.  

    |Champ|Définition|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Saisissez un code pour identifier la définition d’échange de données.|  
    |**Nom**|Saisissez un nom pour la définition d’échange de données.|  
    |**Type de fichier**|Spécifiez le type de fichier pour lequel la définition d’échange de données est utilisée. Vous pouvez sélectionner quatre types de fichiers :<br /><br /> -   **XML** : chaînes multicouches de contenu et de balisage entourées de balises indiquant la fonction.<br />-   **Texte variable** : les enregistrements ont une longueur variable et sont séparés par un caractère, comme une virgule ou un point\-virgule, également désigné sous le nom de *fichier délimité*.<br />-   **Texte fixe** : les enregistrements sont de même longueur, utilisant les caractères du clavier et chaque enregistrement est sur une ligne distincte, également connu sous le nom de *fichier de largeur fixe*.<br />- **Json** : chaînes multicouches de contenu dans JavaScript.|  
    |**Type**|Spécifiez pour quel type d’activité la définition d’échange de données est utilisée, par exemple **Exportation de paiement**.|  
    |**Codeunit gestion données**|Spécifiez le codeunit qui transfère les données dans et hors des tables de [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit validation**|Spécifiez le codeunit utilisé pour valider les données par rapport aux règles d’entreprise prédéfinies.|  
    |**Codeunit lecture/écriture**|Spécifiez le codeunit qui traite les données importées avant le mappage et les données exportées après le mappage.|  
    |**XMLport lecture/écriture**|Spécifiez le XMLport par lequel un fichier de données importées ou un service passe avant le mappage et par lequel des données exportées sortent lors d’une écriture dans un fichier de données ou un service après le mappage.|  
    |**Codeunit gestion données ext.**|Spécifiez le codeunit qui transfère les données externes dans et hors de l’infrastructure d’échange de données.|  
    |**Codeunit retour utilisateur**|Spécifiez le codeunit qui effectue des nettoyages après un mappage, par exemple le marquage des lignes lors de leur importation et la suppression des enregistrements temporaires.|  
    |**Encodage du fichier**|Spécifier l’encodage du fichier. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Séparateur de colonnes**|Spécifiez la manière dont les colonnes dans le fichier de données sont distinctes, si le fichier est de type **Texte variable**.|  
    |**Lignes en-tête**|Indiquez le nombre de lignes d’en-tête qui existent dans le fichier.<br /><br /> Ce paramètre garantit que les données d’en-tête ne sont pas importées. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Étiquette en-tête**|Si une ligne d’en-tête existe à plusieurs endroits dans le fichier, saisissez le texte de la première colonne sur la ligne d’en-tête.<br /><br /> Cette option garantit que les données d’en-tête ne sont pas importées. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Étiquette pied de page**|Si une ligne de pied de page existe à plusieurs endroits dans le fichier, saisissez le texte de la première colonne sur la ligne de pied de page.<br /><br /> Cette option garantit que les données de pied de page ne sont pas importées. **Remarque** : ce champ ne s’applique qu’aux importations.|  

   > [!TIP]
   > Pour voir quels codeunits Microsoft utilise dans les définitions existantes dans le produit standard, consultez les trois champs **Codeunit** sur la page **Mappage des champs**, sous le raccourci **Général**, pour chaque définition.  

4. Sur le raccourci **Définitions des lignes**, décrivez le formatage des lignes dans le fichier de données en renseignant les champs comme indiqué dans le tableau suivant.  

    > [!NOTE]  
    > Pour importer des relevés bancaires, vous créez une seule ligne pour le format de fichier unique du relevé bancaire que vous souhaitez importer.  
    >
    > Pour exporter des règlements, vous pouvez créer une ligne pour chaque type de règlement que vous voulez exporter. Dans ce cas, le raccourci **Définitions des colonnes** affiche des colonnes différentes pour chaque type de paiement.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Type ligne**|Spécifie le type de ligne dans le fichier.|  
    |**Code**|Saisissez un code pour identifier la ligne dans le fichier.|  
    |**Nom**|Saisissez un code décrivant la ligne dans le fichier.|  
    |**Nombre colonnes**|Indiquez le nombre de colonnes que contient la ligne du fichier de données. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Étiquette ligne données**|Indiquez la position dans le schéma XML associé de l’élément qui représente l’écriture principale du fichier de données. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Espace de noms**|Spécifiez l’espace de noms qui est prévu dans le fichier, pour activer la validation de l’espace de noms. Vous pouvez laisser ce champ vide si vous ne souhaitez pas activer la validation d’espace de noms.|  
    |**Code parent**|Spécifiez le parent de la ligne, comme indiqué dans le champ **Code** lorsque la configuration de l’échange de données est définie pour les fichiers avec des écritures parent et enfants, comme un en-tête et des lignes de document.

5. Répétez l’étape 4 pour créer une ligne pour chaque type de fichier de données que vous voulez exporter.  

     Planifiez maintenant de décrire le formatage des colonnes du fichier de données en renseignant les champs du raccourci **Définitions des colonnes** comme indiqué dans le tableau suivant. Vous pouvez utiliser la structure du fichier, par exemple un fichier .xsd pour le fichier de données afin de pré remplir le raccourci avec les éléments appropriés. Pour plus d’informations, consultez [Utiliser des schémas XML pour préparer des définitions d’échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Sur le raccourci **Définitions de colonnes**, sélectionnez l’action **Extraire la structure de fichiers**.  
7. Sur la page **Extraire la structure de fichiers**, sélectionnez la structure de fichier associée, puis sélectionnez **OK**. Les lignes du raccourci **Définitions de colonnes** sont renseignées conformément à la structure du fichier de données.  
8. Dans le raccourci **Définitions des colonnes**, modifiez ou renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N° colonne**|Spécifiez le numéro qui indique la position de la colonne sur la ligne du fichier.<br /><br /> Pour les fichiers XML, spécifiez le numéro qui indique le type d’élément dans le fichier contenant les données.|  
    |**Nom**|Spécifiez le nom de la colonne.<br /><br /> Pour les fichiers XML, spécifiez le balisage qui indique les données à échanger.|  
    |**Type de données**|Spécifiez si les données à échanger sont de type **Texte**, **Date** ou **Décimale**.|  
    |**Format données**|Spécifiez le format des données, le cas échéant. Par exemple, **MM/JJ/AAAA** si le type de données est **Date**. **Remarque :** pour l’exportation, spécifiez le format de données en fonction de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour l’importation, spécifiez le format de données en fonction du .NET Framework. Pour plus d’informations, consultez [Chaînes de format de date et heure standard](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Culture mise en forme données**|Spécifiez le format de données régional, le cas échéant. Par exemple, **en-US** si le type de données est **Décimale** pour être sûr que la virgule est utilisée comme séparateur de .000, conformément au format américain. Pour plus d’informations, consultez [Chaînes de format de date et heure standard](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Longueur**|Spécifiez la longueur de la ligne de longueur fixe qui comporte la colonne si le fichier de données est de type **Texte fixe**.|  
    |**Description**|Spécifie une description de la colonne. Ce champ est purement informatif.|  
    |**Chemin**|Indiquez la position de l’élément dans le schéma XML lié.|  
    |**Identifiant signe négatif**|Saisissez la valeur qui est utilisée dans le fichier de données pour identifier les montants négatifs, dans les fichiers de données qui ne peuvent pas contenir des signes négatifs. Cet identifiant est utilisé pour inverser les montants identifiés aux montants négatifs lors de l’import. **Remarque** : ce champ ne s’applique qu’aux importations.|  
    |**Fixe**|Spécifiez les données à exporter dans cette colonne, telles que les informations supplémentaires sur le type de paiement. **Remarque** : ce champ ne s’applique qu’aux exportations.|  
    |**Remplissage du texte obligatoire**|Spécifie que les données doivent inclure le remplissage du texte.|  
    |**Caractère de remplissage**|Spécifie le caractère de remplissage du texte.|  
    |**Justification**|Spécifie si la colonne est justifiée à gauche ou à droite.|  

9. Répétez l’étape 8 pour chaque colonne ou élément XML du fichier de données qui contient des données que vous souhaitez échanger avec [!INCLUDE[prod_short](includes/prod_short.md)].  

L’étape suivante de la création de la définition d’échange de données consiste à choisir les correspondances entre les colonnes ou les éléments XML du fichier de données et les champs de [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Le mappage spécifique dépend de l’objectif commercial du fichier de données à échanger et des variations locales. Même le standard bancaire SEPA a des variations locales. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge en natif l’importation de fichiers de relevé bancaire SEPA CAMT. Ceci est représenté par le code d’enregistrement de définition d’échange de données **SEPA CAMT** sur la page **Définitions d’échange de données**. Pour plus d’informations sur le mappage de champs spécifique de cette prise en charge de SEPA CAMT, voir [Mappage de champs lors de l’importation de fichiers SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name=mapfields></a>Pour mapper les colonnes du fichier de données aux champs de [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Parfois, les valeurs des champs que vous souhaitez associer sont différentes. Par exemple, le code langue pour les États-Unis est « U.S. » dans une application métier et « US » dans une autre. Cela signifie que vous devez transformer la valeur lorsque vous échangez des données. Cela se fait via les règles de transformation que vous définissez pour les champs. Pour plus d’informations, consultez [Règles de transformation](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Vous pouvez également opérer un regroupement par n’importe quel champ, utiliser l’index clé pour trier les résultats et les nouveaux types de transformation **Arrondi** et **Recherche de champ**.

1. Sur le raccourci **Définitions de lignes**, sélectionnez la ligne pour laquelle vous souhaitez mapper les colonnes aux champs, puis sélectionnez **Mappage de champs**. La page **Mappage d’échange de données** s’ouvre.  
2. Dans le raccourci **Général**, spécifiez les paramètres de mappage en renseignant les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**ID Table**|Indiquez la table qui contient les champs vers lesquels ou à partir desquels des données sont échangées en fonction du mappage.|  
    |**Utiliser comme table intermédiaire**|Spécifiez si la table que vous sélectionnez dans le champ **ID table** est une table intermédiaire de stockage des données importées avant leur mappage vers la table cible.<br /><br /> Vous utilisez généralement une table intermédiaire lorsque la définition d’échange de données est utilisée pour importer et convertir des documents électroniques, tels que des factures fournisseur en factures achat dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Échanger des données par voir électronique](across-data-exchange.md).|  
    |**Nom**|Saisissez un nom pour les paramètres de mappage.|  
    |**Index de clé**|Spécifiez l’index de clé pour trier les enregistrements source avant l’exportation.|
    |**Codeunit pré-mappage**|Spécifiez le codeunit qui prépare le mappage entre les champs dans [!INCLUDE[prod_short](includes/prod_short.md)] et les données externes.|  
    |**Codeunit mappage**|Spécifiez le codeunit qui est utilisé pour mapper les colonnes ou les éléments de données XML spécifiés aux champs dans [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit post-mappage**|Spécifiez le codeunit qui effectue le mappage entre les champs dans [!INCLUDE[prod_short](includes/prod_short.md)] et les données externes. **Remarque :** lors de l’utilisation de l’extension AMC Banking 365 Fundamentals, le codeunit convertit les données exportées depuis [!INCLUDE[prod_short](includes/prod_short.md)] vers un format générique prêt pour l’exportation. Pour l’importation, le codeunit convertit les données externes dans un format prêt à l’importation dans [!INCLUDE[prod_short](includes/prod_short.md)].|
3. Sur le raccourci **Mappage des champs**, spécifiez quelles colonnes correspondent à quels champs dans [!INCLUDE[prod_short](includes/prod_short.md)] en remplissant les champs comme décrit dans les tableaux suivants, selon que le champ **Utiliser comme table intermédiaire** a été activé ou non.  
   * Avec le bouton à bascule **Utiliser comme table intermédiaire** désactivé :

     |Champ|Désignation|  
     |--------------------------------- |---------------------------------------|  
     |**N° colonne**|Spécifiez la colonne dans le fichier de données pour laquelle vous souhaitez définir une fiche.<br /><br /> Vous pouvez uniquement sélectionner les colonnes qui sont représentées par des lignes sur le raccourci **Définitions colonne** de la page **Définition d’échange de données**.|
     |**Légende de colonne**|Spécifie la légende de la colonne du fichier externe qui est mappée au champ sélectionné dans le champ **ID table cible** lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**ID de champ**|Spécifiez à quel champ correspond la colonne dans le champ **N° colonne** .<br /><br /> Vous pouvez uniquement choisir parmi des champs existant dans la table que vous avez spécifiée dans le champ **ID table** du Raccourci **Général**.|
     |**Légende du champ**|Spécifie la légende du champ du fichier externe qui est mappé au champ sélectionné dans le champ **ID table cible** lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**Supplémentaires**|Spécifiez que la correspondance doit être ignorée si le champ est vide. Si vous n’activez pas cette option, une erreur d’exportation aura lieu si le champ est vide.|  
     |**Règle de transformation**|Spécifie la règle qui transforme un texte importé en valeur prise en charge avant de pouvoir être mappé dans un champ spécifié. Lorsque vous choisissez une valeur dans ce champ, la même valeur est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données** et inversement. Consultez la section suivante pour plus d’informations sur les règles de transformation disponibles pouvant être appliquées.|
     |**Remplacer la valeur**|Spécifie que la valeur actuelle va être remplacée par une nouvelle valeur.|
     |**Priorité**|Spécifie l’ordre dans lequel les mappages de champs doivent être traités. Le mappage de champ avec le numéro de priorité le plus élevé sera traité en premier.|
     |**Multiplicateur**|Spécifie un multiplicateur à appliquer aux données numériques, y compris les valeurs négatives.|

   * Avec le bouton à bascule **Utiliser comme table intermédiaire** activé :

     |Champ|Désignation|  
     |---------------------------------|---------------------------------------|  
     |**N° colonne**|Spécifiez la colonne dans le fichier de données pour laquelle vous souhaitez définir une fiche.<br /><br /> Vous pouvez uniquement sélectionner les colonnes qui sont représentées par des lignes sur le raccourci **Définitions colonne** de la page **Définition d’échange de données**.|
     |**Légende de colonne**|Spécifie la légende de la colonne du fichier externe qui est mappée au champ sélectionné dans le champ **ID table cible** lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**ID table cible**|Spécifiez la table à laquelle la valeur du champ **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**Légende de la table**|Spécifiez le nom de la table dans le champ **ID table cible**, qui est la table à laquelle la valeur du champ **Titre colonne** est mappée, lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**ID champ cible**|Spécifiez le champ dans la table cible auquel la valeur du champ **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**Légende du champ**|Spécifiez le nom du champ dans la table cible auquel la valeur de la colonne **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l’importation des données.|
     |**Valider uniquement**|Spécifie que le mappage élément-champ n’est pas utilisé pour convertir les données, mais uniquement pour valider les données.|
     |**Règle de transformation**|Spécifie la règle qui transforme un texte importé en valeur prise en charge avant de pouvoir être mappé dans un champ spécifié. Lorsque vous choisissez une valeur dans ce champ, la même valeur est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données** et inversement. Consultez la section suivante pour plus d’informations sur les règles de transformation disponibles pouvant être appliquées.|
     |**Priorité**|Spécifie l’ordre dans lequel les mappages de champs doivent être traités. Le mappage de champ avec le numéro de priorité le plus élevé sera traité en premier.|

4. Sur le raccourci **Groupement de champs**, spécifiez les règles à utiliser pour regrouper vos champs quand vous créez le fichier en remplissant les champs comme décrit dans le tableau suivant.  

     |Champ|Désignation|  
     |--------------------------------- |---------------------------------------|  
     |**ID de champ**|Spécifiez le numéro du champ du fichier externe utilisé pour le regroupement. Ce champ doit être défini par l’utilisateur.|
     |**Légende du champ**|Spécifiez la légende du champ dans le fichier externe utilisé pour le regroupement.|

## Règles de transformation

Si les valeurs des champs que vous mappez sont différentes, vous devez utiliser des règles de transformation pour les définitions d’échange de données afin de les rendre identiques. Pour définir des règles de transformation pour des définitions d’échange de données, ouvrez une définition existante ou créez-en une nouvelle, puis, sur le raccourci **Définitions de ligne**, choisissez **Gérer**, puis **Mappage de champs**. Des règles prédéfinies sont fournies, mais vous pouvez également créer les vôtres. Le tableau suivant décrit les types de transformations que vous pouvez effectuer.

|Option|Description|
|---------|---------|
|**Majuscules**|Mettre toutes les lettres en majuscules.|
|**Minuscules**|Mettre toutes les lettres en minuscules.|
|**1re lettre des mots en majuscule**|Mettre en majuscules la première lettre de chaque mot.|
|**Supprimer les espaces**|Supprimer les espaces vides avant et après la valeur.|
|**Sous-chaîne**|Transformer une partie spécifique d’une valeur. Pour spécifier où commencer la transformation, choisissez une **Position de départ** ou un **Texte de départ**. La position de départ est un numéro qui représente le premier caractère à transformer. Le texte de départ est la lettre qui vient juste avant la lettre à remplacer. Si vous souhaitez commencer par la première lettre de la valeur, utilisez plutôt une position de départ. Pour spécifier où arrêter la transformation, choisissez **Longueur**, qui correspond au nombre de caractères à remplacer, ou **Texte de fin**, qui correspond au caractère qui vient juste après le dernier caractère à transformer.|
|**Remplacer**|Trouver une valeur et la remplacer par une autre. Cette transformation est utile pour remplacer des valeurs simples, comme un mot spécifique.|
|**Expression régulière - Remplacer**|Utiliser une expression régulière dans le cadre d’une opération de recherche-remplacement. Cette transformation est utile pour remplacer plusieurs valeurs, voire des valeurs plus complexes.|
|**Supprimer les caractères non alphanumériques**|Supprimer les caractères qui ne sont ni des lettres ni des chiffres, tels que des symboles ou des caractères spéciaux.|
|**Mise en forme de la date**|Spécifier comment afficher les dates. Par exemple, vous pouvez transformer JJ-MM-AAAA en AAAA-MM-JJ.|
|**Mise en forme décimale**|Définir des règles pour la position des décimales et la précision de l’arrondi.|
|**Expression régulière - Correspondance**|Utiliser une expression régulière pour trouver une ou plusieurs valeurs. Cette règle est similaire aux options **Sous-chaîne** et **Expression régulière - Remplacer**.|
|**Personnalisé**|Cette règle de transformation et une option avancée qui nécessite l’aide d’un développeur. Elle active un événement d’intégration auquel vous pouvez vous abonner si vous souhaitez utiliser votre propre code de transformation. Si vous êtes développeur et souhaitez utiliser cette option, consultez la section ci-dessous.|
|**Mise en forme de la date et de l’heure**|Définir comment afficher la date actuelle ainsi que l’heure de la journée.|
|**Recherche de champ**|Utilisez des champs de différentes tables. Pour l’utiliser, vous devez suivre certaines règles. Premièrement, utilisez l’**ID de table** pour spécifier l’ID de la table qui contient l’enregistrement pour la recherche de champ. Deuxièmement, dans le champ **ID du champ source**, spécifiez l’ID du champ qui contient l’enregistrement pour la recherche de champ. Troisièmement, dans le champ **ID du champ cible**, spécifiez l’ID du champ pour rechercher l’enregistrement pour la recherche de champ. En option, utilisez le champ **Règle de recherche de champ** pour spécifier le type de recherche de champ. Pour le champ **Cible**, la valeur de l’**ID de champ cible** est utilisée, même si elle est vide. Pour le champ **Original, si Cible est vide**, la valeur d’origine est utilisée si la cible est vide.|
|**Arrondir**|Arrondissez la valeur de ce champ à l’aide de règles supplémentaires. D’abord, dans le champ **Précision**, spécifiez une précision d’arrondi. Ensuite, dans le champ **Direction**, indiquez le sens de l’arrondi.|

> [!NOTE]  
> Pour plus d’informations sur le formatage de la date et de l’heure, consultez [Chaînes de format de date et heure standard](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### Astuce pour les développeurs : exemple d’option personnalisée

L’exemple suivant montre comment implémenter votre propre code de transformation.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Après avoir défini vos règles, vous pouvez les tester. Dans le raccourci **Test**, saisissez un exemple de valeur que vous souhaitez transformer, puis vérifiez les résultats en sélectionnant **Mettre à jour**.

## Exporter une définition d’échange de données au format XML pour utilisation par d’autres

Lorsque vous avez créé la définition d’échange de données pour un fichier de données spécifique, vous pouvez exporter la définition d’échange de données en tant que fichier XML que vous pouvez importer. Cette tâche est décrite dans la procédure suivante.  

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Définitions d’échange de données**, puis sélectionnez le lien associé.  
2. Sélectionnez la définition d’échange de données que vous voulez exporter.  
3. Choisissez l’action **Exporter définition d’échange de données**.  
4. Enregistrez le fichier XML qui représente la définition d’échange de données dans un emplacement approprié.  

    Si une définition d’échange de données a déjà été créée, il vous suffit d’importer le fichier XML dans l’infrastructure d’échange de données. Cette tâche est décrite dans la procédure suivante.  

## Importer une définition d’échange de données existante

1. Enregistrez le fichier XML qui représente la définition d’échange de données dans un emplacement approprié.  
2. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Définitions d’échange de données**, puis sélectionnez le lien associé.  
3. Choisissez l’action **Importer définition d’échange de données**.  
4. Choisissez le fichier que vous avez enregistré à l’étape 1.  

## Voir aussi

[Configurer l’échange de données](across-set-up-data-exchange.md)  
[Configurer l’envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Réaliser des paiements avec l’extension AMC Banking 365 Fundamentals ou le virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
