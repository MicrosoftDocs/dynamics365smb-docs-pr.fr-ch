---
title: FAQ Power BI
description: "Obtenez des réponses à certaines questions courantes sur l’utilisation de Power BI et de Business\_Central."
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
---
# FAQ Power BI

Cet article répond à certaines des questions que vous pourriez vous poser sur l’utilisation de Power BI et [!INCLUDE [prod_short](includes/prod_short.md)].

## [Général](#tab/general)
<!-- 26 -->
### J′ai sélectionné un état pour mon tableau de bord dans Business Central. Si j′apporte ultérieurement des modifications aux éléments visuels de l′état en ligne, le tableau de bord sera-t-il automatiquement mis à jour avec mes modifications ?

Oui, parce que les états sont intégrés à partir de Power BI.

<!-- 3 -->
### Les applications Business Central pour Power BI sont-elles disponibles dans d′autres langues que l′anglais ?

Non. Ces applications ne sont actuellement disponibles qu′en anglais.

<!-- 24 -->
### Une fois qu′un état est publié sur mon espace de travail powerbi.com, puis-je télécharger son pbix ? 

Oui. Pour plus d′informations, voir [Télécharger un état du service Power BI vers Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### Puis-je télécharger les applications sous forme de fichiers pbix ? 

Non. Actuellement, nous ne proposons pas le téléchargement des fichiers pbix pour les applications Power BI officielles car elles sont publiées sur AppSource.

## [Licence](#tab/license)

<!-- 14 -->
### Ai-je besoin d′une licence Power BI Pro pour publier des états ? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Non. Une licence Pro n′est pas nécessaire pour publier des états. La licence Power BI standard (gratuite) suffit. Pour plus d’informations, reportez-vous à la rubrique [Gestion des licences Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### Y a-t-il quelque chose que je ne peux pas faire avec la licence gratuite ?

Vous ne pouvez pas partager d′états ni installer les applications Business Central pour Power BI. En dehors de cela, la licence gratuite permet de créer presque toutes les variations de graphiques et d′états.

<!-- 16 -->
### Si une personne partage un état avec une autre personne, cette dernière a besoin d′une licence Pro pour afficher l′état. Est-il prévu de rendre cette fonction possible avec la licence gratuite ?

Nous n′avons aucun contrôle sur cette exigence. Cette exigence est définie par Power BI. Pour plus d′informations, voir [Partager les tableaux de bord et les états Power BI avec des collègues et autres](/power-bi/collaborate-share/service-share-dashboards).  

## [Concepteur](#tab/designer)

<!-- 7 -->
### Le connecteur fonctionne-t-il avec les pages API ?

Oui. À compter de juin 2021, le nouveau connecteur Power BI prend en charge à la fois les services Web Business Central et les pages API. Pour plus d′informations, voir [Activer le connecteur Power BI pour utiliser les API Business Central plutôt que les services Web uniquement](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### Puis-je établir un état Power BI à l’aide des lignes facture vente ou des API lignes feuille ?

Les enregistrements de ligne les plus couramment utilisés sont disponibles dans les [API Business Central v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Vous pouvez donc les utiliser pour créer des rapports dans Power BI en les sélectionnant dans le connecteur **Dynamics 365 Business Central**. Cependant, les API de **lignes** sont conçues pour être utilisées uniquement avec certains filtres très spécifiques et peuvent ne pas fonctionner dans votre scénario. Vous pouvez obtenir une erreur similaire à « Vous devez spécifier un ID ou un ID document pour obtenir les lignes ». Pour résoudre ce problème, procédez comme suit lors de l’obtention des données de Business Central pour l’état dans Power BI Desktop :

1. au lieu d’inclure la source de données pour l’entité Lignes, ajoutez la source de données parent. Par exemple, ajoutez **Facture vente** à la place de **Lignes facture vente**.
2. Sélectionnez **Transformer les données** dans la barre d’action Power BI Desktop.
3. Sélectionnez la requête que vous venez d’ajouter, par exemple **Factures vente**.
4. Appliquez tout filtrage nécessaire sur les enregistrements pour réduire le nombre d’enregistrements chargés dans votre état.
5. Faites défiler vers la droite jusqu’à ce que vous trouviez une colonne nommée comme les lignes, par exemple **SalesInvoiceLines**.
6. Sélectionnez le bouton Développer dans l’en-tête de la colonne, à côté du nom de la colonne.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Affiche la colonne SalesInvoiceLines dans Power BI Desktop .":::
<!-- 11 --> 
### Est-il possible de choisir depuis quel environnement Business Central obtenir les données pour Power BI, comme un bac à sable ou un environnement de production ? 

Oui. Le choix est facile. Lorsque vous vous connectez à Business Central à l′aide du connecteur, vous devez choisir l′environnement et le nom de l′entreprise.

<!-- 6 --> 
### Puis-je fusionner les données de plusieurs environnements de production du même abonné ?

Oui. Dans Power BI, exécutez à nouveau l′opération d′obtention des données et choisissez l′environnement souhaité.

<!-- 25 -->
### Quelles pages de Business Central contiennent la partie État Power BI ?  

Actuellement, plusieurs pages contiennent un Récapitulatif avec une partie **États Power BI** pour afficher un état. 

Sur les pages de liste, la partie **États Power BI** est filtrée pour afficher les états relatifs aux données de la liste. Voici les pages de type liste qui incluent la partie **États Power BI** :

|ID page|Name|
|-------|----|
|22|Liste des clients|
|27|Liste des fournisseurs|
|31|Liste des articles|
|9305|Liste des commandes vente|
|9308|Factures achat|

Voici les autres pages qui contiennent la partie **États Power BI** étendue et non filtrée :

|ID page|Name|
|-------|----|
|1156|Détail société|
|4013|Informations sur Intelligent Cloud |
|9006|Tableau de bord Préparateur de commandes|
|9008|Feuilles d’inventaire Tableau de bord de base|
|9010|Tableau de bord Gestionnaire de production|
|9015|Tableau de bord Chef de projet|
|9016|Tableau de bord Répartiteur de service|
|9022|Tableau de bord Gestionnaire d′activité|
|9024|Tableau de bord Admin. de sécurité|
|9026|Tableau de bord Responsable Vente et Relations|
|9027|Tableau de bord Comptable|

> [!TIP]
> Nous n′avons pas l′intention de l′ajouter à toutes les pages de liste pour le moment. Cependant, vous pouvez créer une extension de page simple qui ajoute la partie **États Power BI** dans un Récapitulatif. Pour plus d’informations, voir [Ajout des parties États Power BI aux pages](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) dans l′aide dédiée aux développeurs et professionnels de l′informatique.

<!-- 5 -->
### Existe-t-il un moyen de filtrer un ensemble de données à partir de Business Central *avant* de le basculer dans Power BI au lieu d′appliquer ultérieurement des filtres ?

Pour filtrer des ensembles de données plus volumineux, le moyen le plus simple consiste à définir un filtre sur l′état Power BI en modifiant directement la formule Power Query. La plupart des filtres que vous définissez de cette manière sont transmis à Business Central par Query Folding. Voir [Actualisation incrémentielle des ensembles de données](/power-bi/admin/service-premium-incremental-refresh).

Il n′existe actuellement aucun moyen de définir un filtre pour les données d′un service Web à partir de Business Central. Si votre application doit définir un filtre à partir de Business Central, vous devez créer une application Business Central personnalisée à cet effet.

<!-- 10 -->
### Dans Power BI, outre l′utilisation d′une requête, existe-t-il un autre moyen d′obtenir des données à partir des tables Business Central sans page associée ? Comme la table *Correspondance de valeur d′attribut article*.

Non. Pas à ce stade.

<!-- 12 --> 
### Les requêtes publiées sont-elles plus rapides à utiliser que les pages publiées ?

En ce qui concerne les services Web, les requêtes publiées sont généralement plus rapides que les pages publiées équivalentes. La raison en est que les requêtes sont optimisées pour la lecture des données et ne contiennent pas de déclencheurs coûteux comme OnAfterGetRecord.

Les services web sont basés sur des pages ou des requêtes conçues pour un accès à partir du web et généralement non optimisées pour un accès à partir de services externes. Même si le connecteur Business Central prend toujours en charge l’obtention de données à partir des services web, nous vous encourageons à utiliser les pages API au lieu des services web dans la mesure du possible.

<!-- 13 --> 
### Existe-t-il un moyen pour un utilisateur final de créer un service Web avec une colonne qui se trouve dans une table Business Central, mais pas dans une page ? Ou le développeur doit-il créer une requête personnalisée ? 

Il n’existe actuellement aucun moyen d’ajouter un nouveau champ à un service web. Les pages API offrent une flexibilité totale sur la structure de la page, de sorte qu’un développeur peut créer une page API pour répondre à cette exigence. 

<!-- 28 --> 
### Puis-je connecter Power BI à un serveur de base de données en lecture seule de Business Central Online ? 

Cette fonctionnalité sera bientôt disponible. À partir de février 2022, les rapports que vous créez à partir des données de Business Central Online essaieront automatiquement de se connecter à une réplique de base de données en lecture seule. Cela entraînera une actualisation plus rapide de vos rapports et aura moins d’impact sur les performances si vous utilisez Business Central pendant l’actualisation d’un rapport. Nous vous recommandons toujours, dans la mesure du possible, de programmer l’actualisation de vos rapports en dehors des heures normales de travail.

Si vous avez d’anciens rapports basés sur des données Business Central, ils ne se connecteront pas au réplica de base de données en lecture seule.

### <a name="databasemods"></a>J’ai essayé la version préliminaire du nouveau connecteur pour la mise à jour de février 2022. Lorsque je me connecte à ma page API Business Central personnalisée, j’obtiens l’erreur « Impossible d’insérer un enregistrement. L’intention de connexion actuelle est en lecture seule. ». Comment puis-je résoudre ce problème ?

Avec le nouveau connecteur, les nouveaux rapports qui utilisent les données Business Central se connecteront par défaut à une réplique en lecture seule de la base de données Business Central. Ce changement apportera une amélioration des performances. Cependant, dans de rares cas, cela peut provoquer l’erreur. Cette erreur se produit généralement parce que votre API personnalisée apporte des modifications aux enregistrements Business Central alors que Power BI essaie d’obtenir les données. En particulier, cela se produit dans le cadre des déclencheurs AL : OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord et OnAfterGetCurrRecord.

Pour résoudre ce problème en forçant le connecteur Business Central à autoriser ce comportement, consultez [Génération d’états Power BI pour afficher les données Business Central – Résolution des problèmes](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="perms"></a>Comment modifier ou effacer le compte utilisateur que j’utilise actuellement pour me connecter à Business Central depuis Power BI Desktop ?

Dans Power BI Desktop, exécutez l’une des étapes suivantes :

1. Dans le menu Fichier, sélectionnez **Options et paramètres** > **Paramètres de la source de données**.
2. Sélectionnez **Dynamics Business Central** dans la liste, puis sélectionnez **Effacer les autorisations** > **Effacer**.

Ensuite, la prochaine fois que vous vous connecterez à Business Central pour obtenir des données, vous serez invité à vous connecter.

## [Performances](#tab/performance)

<!-- 17 -->

### Est-il plus rapide d′obtenir des données à l′aide des pages API que par les services Web ?

Oui. Nos tests indiquent que les pages API sont jusqu′à 25 % plus performantes que les services Web.

<!-- 18 -->
### Est-il prévu d′avoir un miroir sur l′instance Azure SQL Database pour me connecter directement ?

Non. Pas à ce stade. Vous ne pouvez communiquer qu′avec Business Central par les API.

<!-- 19 -->
### Le chargement des données à partir des services Web de Business Central semble lent. Existe-t-il un moyen d′obtenir les données directement à partir de la table de base de données SQL ?

Non. L′accès direct à la base de données n′est pas possible, mais le basculement vers les pages API (dès la mise à disposition du nouveau connecteur) aidera grandement.

## [Avancé](#tab/advanced)
<!-- 1 -->

### Est-il prévu que le connecteur Power BI prenne en charge les fonctionnalités d′actualisation incrémentielle dans le service Power BI ?

Oui. C′est sur notre feuille de route.

<!-- 2 -->
### Si une solution Business Central sur site n′a pas accès à Internet, puis-je continuer à utiliser Power BI ?
<!-- todo: please explain this one-->

Oui. Dans ce cas, utilisez Power BI Desktop localement et connectez-vous à Business Central sur site. Une fois connecté, vous pouvez créer et afficher des états mais vous ne pouvez tout simplement pas les publier sur le service Power BI. 
<!-- 20 -->
### Est-il prévu de rendre possible la réplication des bases de données Business Central Online afin qu′elles soient accessibles pour les requêtes SQL en lecture seule ? Cette fonction prendrait en charge l′actualisation incrémentielle et serait beaucoup plus rapide que les API ou les services Web.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Oui. Nous avons cette fonctionnalité sur notre feuille de route à long terme. 

<!-- 21 -->
### Si j′utilise Azure Data Factory pour obtenir les données depuis Business Central et les consommer sur Power BI, cela aidera-t-il à augmenter les performances ? 

Oui. Ce scénario avancé aiderait Business Central à rester performant car l′accès aux données se ferait via Azure Data Factory.

<!-- 22 -->
### Est-il prévu de prendre en charge les pipelines de déploiement de Power BI, ou un moyen de créer des pipelines de déploiement pour les états PBI, similaires aux extensions ? Ou peut-être même une API simple dans le Centre d′administration ? 

Nous étudions cette fonctionnalité. Power BI propose des API riches pour contrôler les déploiements d′états. Pour plus d′informations, voir [Introduction aux pipelines de déploiement](/power-bi/create-reports/deployment-pipelines-overview).

### Lorsque je reçois des données de Business Central à utiliser dans mes états Power BI, je vois des valeurs comme « _x0020_ ». Quelles sont ces valeurs ?

Certaines pages API, y compris la plupart des pages API v2.0, ont des champs basés sur les [objets AL Enum](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Les champs basés sur les objets AL Enum doivent avoir des noms cohérents et toujours identiques afin que les filtres de l′état fonctionnent toujours, quels que soient la langue ou le système d′exploitation utilisés. Pour cette raison, les champs basés sur AL Enum ne sont pas traduits et sont codés pour éviter tout caractère spécial dont l′espace. En particulier, chaque fois qu′il y a une option vide dans l′objet AL Enum, elle est codée en « _x0020_ ». Vous pouvez toujours appliquer une transformation à vos données sur Power BI pour afficher une valeur différente pour ces champs, par exemple « Vide ».


---

## Voir la [formation Microsoft](/training/modules/change-documents-dynamics-365-business-central/) associée

## Voir aussi

[Gestion des licences Power BI](admin-powerbi-setup.md#license)  
[Introduction à Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble de l’intégration Power BI](admin-powerbi-overview.md)  
[Activation de Power BI dans Business Central](admin-powerbi-setup.md)  
[Utiliser les états Power BI dans Business Central](across-working-with-powerbi.md)  
[Utiliser des données Business Central dans Power BI](across-working-with-business-central-in-powerbi.md)  
[Création d’états Power BI pour afficher les données Business Central](across-how-use-financials-data-source-powerbi.md)  
[Documentation Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
