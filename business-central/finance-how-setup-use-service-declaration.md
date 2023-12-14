---
title: Configurer et utiliser l’extension de déclaration de service
description: 'Apprendre à configurer et utiliser les fonctionnalités de Déclaration de service (déclaration d’échanges de biens pour les services), et enregistrer les transactions de service avec des sociétés dans d’autres pays/régions de l’UE.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# Extension de déclaration de service

Dans certains pays/régions de l’UE, les autorités exigent que les entreprises déclarent l’exportation de services vers d’autres pays/régions de l’UE. L’extension **Déclaration de service** vous permet de collecter des informations sur le commerce des services dans l’UE et de les signaler aux autorités. Bien qu’elle s’appelle **Déclaration de service**, vous pouvez également l’utiliser comme **Déclaration d’échanges de biens pour les services**. Cette extension est disponible pour tous les pays/régions de l’UE en version W1 et peut être utilisée telle quelle en Belgique. Pour les autres pays.régions, une extension basée sur le pays/la région sera requise. Si un pays/une région n’a besoin que d’un format différent, vous pouvez utiliser la configuration du rapport dans l’**Infrastructure d’échange de données** pour modifier le format.

## Activer l’extension de déclaration de service

Après avoir installé l’extension dans votre environnement, vous devez l’activer.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Gestion des fonctionnalités** et sélectionnez le lien associé.
2. Recherchez **Fonctionnalité : activer l’utilisation de la déclaration de service (déclaration d’échanges de biens pour les services)**, et dans le champ **Activé pour**, choisissez **Tous les utilisateurs**. Découvrez la gestion des fonctionnalités sur [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management) dans le contenu de l’administration.
3. Quand vous activez la fonctionnalité, vous devez suivre les étapes du processus de configuration via l’Assistant Configuration. La plupart des champs sont configurés par défaut.
4. Ajoutez uniquement **Types de transactions de services** à la deuxième étape en choisissant l’option **Ouvrez la page des types de transactions de service pour indiquer la liste des codes**.
5. Avant de commencer, vérifiez le **Nombre total de codes** pour comprendre combien de types de transactions de services ont déjà été spécifiés.
6. Choisissez **Terminer** à la dernière étape pour terminer la configuration.

## Configurer l’extension de déclaration de service

Vous pouvez configurer l’extension manuellement ou en utilisant un fichier de rapport dans les définitions d’échange de données.

### Pour configurer de la déclaration de service manuellement

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres Déclaration de service**, puis choisissez le lien associé.
2. Dans le raccourci **Général**, configurez les champs comme indiqué dans le tableau ci-dessous :

    |Champ  |Désignation  |
    |---------|---------|
    |**Souches de n° de déclaration**     | Spécifie la souche de numéros à utiliser pour attribuer des ID aux nouveaux enregistrements.        |
    |**Déclarer des frais annexes**  | Indique si les frais annexes doivent être déclarés. Si activé, [!INCLUDE [prod_short](includes/prod_short.md)] vérifie le code de transaction de service pour les frais annexes et les inclut dans les déclarations de service.        |
    |**Donneur d’ordre/N° client facturé**     | Spécifie le client à utiliser pour comparer son code de pays avec le code de pays sur la page **Informations société**. Seuls les documents où ces deux codes sont différents seront inclus dans la déclaration de service.<br><br>* **Clients facturés.**  : utilisez le code pays du **Client à facturer** <br<br>* **Donneur d’ordre.**  : utilisez le code pays du **Client Donneur d’ordre**.        |
    |**Fournisseur/N° fournisseur à payer**  | Spécifie le fournisseur à utiliser pour comparer son code de pays avec le code de pays de la page **Informations société**. Seuls les documents où ces deux codes sont différents seront inclus dans la déclaration de service.<br><br> * **De fournisseur.**  : utilisez le code pays du **Fournisseur**. <br><br> * **Paiement.**  : utilisez le code pays du **Fournisseur Paiement**.         |
    |**Code déf. échge données**  | Indique le code de définition d’échange de données utilisé pour générer le fichier exporté pour la déclaration de service.        |
    |**Activer N° identif. fiscale**     |  Indique si le **N° identif. fiscale** est activé pour la déclaration de service.       |

3. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Types de transactions de services**, puis sélectionnez le lien associé.
4. Sur les lignes, spécifiez **Codes** et **Descriptions** pour les types de transactions de service que vous utiliserez.

### Configurer un fichier de déclaration

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Définitions d’échange de données** et sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur le raccourci **Général**, décrivez la définition d’échange de données en spécifiant le type de fichier de données, le séparateur de colonnes, le codeunit associé, XMLport et en remplissant les autres champs.
4. Sur le raccourci **Définitions de ligne**, décrivez le formatage des lignes du fichier de données en remplissant les champs en fonction du champ **Type de ligne**, et où vous devez définir le nombre de colonnes pour cette ligne.
5. Sur le raccourci **Définitions de colonne**, remplissez la ligne pour chaque colonne planifiée.
6. Sélectionnez l’action **Mappage des champs**dans le raccourci **Définitions de ligne** pour ouvrir la page **Mappage des champs**.
7. Créez une entrée, et sur le raccourci **Général**, sélectionnez l’**ID de table** approprié (pour **Ligne de déclaration de service**, choisissez **5024**), puis remplissez les champs comme suit :
   1. Dans le champ **Index clé**, spécifiez l’index de clé pour trier les enregistrements source avant l’exportation.
   2. Sélectionnez le **Codeunit de mappage**.
8. Sur le raccourci **Mappage des champs**, ajoutez les colonnes que vous avez précédemment configurées dans le raccourci **Définitions de colonne** et ajoutez ce qui suit :
   1. Spécifiez **l’ID de champ** pour chacune des colonnes.
   2. Spécifiez la **Règle de transformation** pour chaque colonne au besoin. La règle transforme un texte importé en valeur prise en charge avant de pouvoir être mappé dans un champ spécifié dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous choisissez une valeur dans ce champ, la valeur exacte est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données**  et inversement.
9. Pour regrouper des entrées en fonction des colonnes, sur le raccourci **Groupement de champs**, choisissez les champs que vous souhaitez utiliser pour le regroupement.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] est livré avec une définition d’échange de données pré-configurée pour la **Déclaration de service** pour tous les pays/régions pour lesquels la traduction a été faite. Découvrez plus d’informations sur la création d’une définition d’échange de données dans [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

## Autres configurations associées

Avant d’utiliser l’extension de déclaration de service, configurez certains champs pour les articles, les ressources et les frais annexes.

### Articles

Configurez les informations relatives à la déclaration de service sur les pages Fiche article :

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article que vous souhaitez configurer.
3. Développez le raccourci **Article** et configurez les champs suivants :
   1. Dans le champ **Type**, choisissez **Service**.
   2. Dans le champ **Code type de transaction de service**, spécifiez le code pour un **Type de transaction de service**.
   3. Si vous ne souhaitez pas inclure cet élément de service dans les déclarations de service, choisissez le champ **Exclure de la déclaration de service**.

### Ressources

Configurez les informations relatives à la déclaration de service sur les pages Fiche ressource :

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Ressources** et choisissez le lien associé.
2. Sélectionnez la ressource que vous souhaitez configurer.
3. Développez le raccourci **Général** et configurez les champs suivants :
   1. Dans le champ **Code type de transaction de service**, spécifiez le code pour un **Type de transaction de service**.
   2. Si vous ne souhaitez pas inclure cette ressource de service dans les déclarations de service, choisissez le champ **Exclure de la déclaration de service**.

### Frais annexes

Configurez les informations relatives à la déclaration de service pour les frais annexes :

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Frais annexes**, puis choisissez le lien associé.
2. Sélectionnez les frais annexes que vous souhaitez configurer.
3. Dans le champ **Code type de transaction de service**, spécifiez le code pour un **Type de transaction de service**.
4. Si vous ne souhaitez pas inclure ces frais annexes dans les déclarations de service, choisissez le champ **Exclure de la déclaration de service**.

## Créer une déclaration de service

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Déclarations de services**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Renseignez les champs suivant sur le raccourci **Général** :
    1. Dans le champ **Code config.**, spécifiez le code de configuration qui est utilisé pour suggérer des lignes et créer des fichiers. Vous devez en choisir un comme **Déclaration de service**.
    2. Dans les champs **Date de début** et **Date de fin**, indiquez les dates de début et de fin de la période à inclure dans le déclaration de services.
4. Choisissez l’action **Suggérer des lignes** pour démarrer un traitement par lots qui collecte les lignes des documents et remplit les lignes de déclaration de service.

Le traitement par lots récupère toutes les écritures des documents d’achat et de vente applicables dans la période requise et les ajoute sur les lignes de déclaration de service. Positionnez le curseur sur les champs dans les lignes pour lire une brève description.

## Modifier une déclaration de service

Si nécessaire, vous pouvez modifier les lignes ou en ajouter de nouvelles.

1. Sur la page **Déclaration de service**, sur le raccourci **Lignes**, sélectionnez l’action **Nouvelle ligne**.
2. Dans le champ **Type de document**, choisissez l’option associée aux documents que vous souhaitez utiliser.
3. Selon le **Type de document**, remplissez le champ **N° document**.
4. Renseignez les champs restants.

## Présentation des lignes de déclaration de service

Après avoir créé une déclaration de service, utilisez l’action **Aperçu** pour obtenir un aperçu des lignes de déclaration de service. Vous pouvez regrouper et résumer les lignes de la même manière que le fichier exporté. Vous pouvez également ouvrir les lignes dans Excel.

## Faire figurer la déclaration de service dans un fichier

Vous pouvez soumettre la déclaration de service sous forme de fichier en fonction des exigences des différentes autorités locales. Pour créer un fichier :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Déclarations de services**, puis sélectionnez le lien associé.
2. Choisissez la déclaration de service que vous souhaitez déclarer sous forme de fichier.
3. Si ce n’est déjà fait, renseignez la déclaration de service manuellement ou sélectionnez l’action **Proposer lignes**.
4. Choisissez l’action **Créer fichier**.
5. Le fichier de déclaration de service sera enregistré au format souhaité.

## Autres considérations

Quand vous utilisez l’extension **Déclaration de service**, vous devez prendre en compte quelques éléments supplémentaires. Par exemple, il est important que vos groupes correspondent aux exigences des autorités. Il est également important que les services soient correctement inclus dans les documents vente et achat.

### Regrouper des lignes

Sur les lignes de déclaration de service, il n’y a pas de regroupement par champ. Toutes les écritures sont copiées à partir du document d’origine en tant que source.

Le regroupement requis par les autorités sera fourni dans le fichier exporté. Vous devez configurer les groupes dans la **Définition d’échange de données**, qui est entièrement configurable. Pour plus d’informations, consultez [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

### Utilisation des services dans les lignes de document

Quand vous créez une facture achat, vente ou service, vous trouverez deux champs liés aux déclarations de service sur leurs lignes. Les deux champs sont renseignés avec les valeurs par défaut de vos configurations d’article, de ressource ou de frais annexes.

- **Code type de transaction de service** – spécifiez le code pour un Type de transaction de service.
- **S’applique à la déclaration de service** – Indique si un article ou une ressource est applicable à une déclaration de service.

Vous pouvez modifier les valeurs dans ces champs, mais si vous sélectionnez le champ **S’applique à la déclaration de service**, vous devez spécifier une valeur dans le champ **Code du type de transaction de service**. Si vous ne le faites pas, vous ne pouvez pas publier le document.

Si vous sélectionnez une valeur dans le champ **Code de type de transaction de service**, mais que vous ne sélectionnez pas le champ **S’applique à la déclaration de service**, vous pouvez publier le document, mais la ligne ne sera pas calculée.

## Voir aussi

[Paramétrer les états intracommunautaires](finance-how-setup-report-intrastat.md)
[États intracommunautaires dans Business Central](finance-how-report-intrastat.md)  
[Gestion financière](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
