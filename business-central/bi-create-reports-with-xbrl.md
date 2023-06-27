---
title: "Procédure\_: créer des états avec XBRL"
description: XBRL est basé sur le langage XML et est utilisé pour marquer des données financières et permettre aux sociétés de traiter et de partager leurs données de manière efficace et précise.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="create-reports-with-xbrl" />Création d’états avec XBRL

> [!NOTE]
> Nous sommes en train de supprimer les fonctionnalités de création de rapports XBRL de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Modifications dans la 1re vague de lancement 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**usiness **R**eporting **L**anguage) est basé sur le langage XML et est utilisé pour marquer des données financières et permettre aux sociétés de traiter et de partager leurs données de manière efficace et précise. L’initiative XBRL permet la génération d’états financiers généraux par de nombreux éditeurs de logiciels de planification des ressources de l’entreprise (ERP) et organisations comptables internationales. L’objectif de cette initiative et de fournir un standard pour la génération d’états d’informations financières uniformes pour les banques, les investisseurs et les autorités gouvernementales. Les rapports commerciaux générés de cette manière peuvent inclure :  

* Rapports financiers  
* Informations financières  
* Informations non financières  
* Informations de classement de règlementation, tels que les états financiers annuels et trimestriels.  

> [!NOTE]
> Vous pouvez importer des schémas en relation avec la comptabilité et créer des documents d’instance XBRL en mappant les données de comptabilité du plan comptable à des éléments de taxonomies qui ont été conçus pour les rapports financiers, tels que les bilans, les comptes de gestion, etc.
>
> Les fonctionnalités XBRL de Business Central prennent en charge les taxonomies pour la spécification 2.1. Cependant, les taxonomies peuvent contenir des éléments non pris en charge, tels que des liens ressources de formule ou iXBRL (XBRL en ligne), ou présenter d’autres différences structurelles. Nous vous recommandons de valider la fonctionnalité XBRL avant de l’utiliser pour la génération d’états.
>
> La prise en charge complète des taxonomies peut nécessiter un marquage XBRL et des outils tiers. L’organisation XBRL International dispose d’une liste d’outils et de services ; en fonction des exigences de génération de rapports XBRL pour une taxonomie donnée, vous souhaiterez peut-être explorer ces ressources. Pour plus d’informations, consultez [Mise en route pour les affaires](https://go.microsoft.com/fwlink/?linkid=2153466) et [Outils et services](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language" />Langage XBRL (eXtensible Business Reporting Language)

Les taxonomies XBRL sont tenues à jour par le site www.xbrl.org. Pour télécharger des taxonomies et pour obtenir plus d’informations, reportez-vous au site Web de XBRL.  

Imaginons que quelqu’un veut des informations financières de votre part. Cette personne vous fournit une taxonomie (au format XML) contenant un ou plusieurs schémas, chacun comportant un certain nombre de lignes à renseigner. Ces lignes correspondent aux données financières requises par l’expéditeur. Vous devez importer cette taxonomie, puis remplir les schémas en saisissant le ou les comptes correspondant à chaque ligne et calcul souhaité, par exemple le solde période ou le solde au. Dans certains cas, vous devez saisir une constante, comme le nombre d’employés. Vous pouvez alors renvoyer le document instancié (au format XML) au demandeur. Ainsi, pour les demandes d’informations récurrentes, et à moins que la taxonomie n’ait été modifiée, vous pouvez simplement exporter sur demande de nouveaux documents instanciés correspondant à de nouvelles périodes.

## <a name="xbrl-comprises-the-following-components" />Le langage XBRL contient les composants suivants :

La **spécification** XBRL explique le principe du langage XBRL, et indique comment créer des documents instanciés XBRL et des taxonomies XBRL. La spécification XBRL présente le langage XBRL en termes techniques et est destinée à des spécialistes.  

Les **schémas** XBRL sont les composants de bas niveau fondamentaux du langage XBRL. Un schéma est un fichier physique au format XSD (également nommé Défintion de schéma XML) qui précise comment les documents instanciés et les taxonomies XBRL doivent être construits.

Les **liens ressources** XBRL sont des fichiers physiques au format XML contenant des informations concernant les éléments définis par le schéma XBRL, tels que le nombre de langues d’affichage des libellés, les relations entre ces libellés, comment additionner des éléments entre eux, etc.  

Une **taxonomie** XBRL est une « terminologie » ou un « dictionnaire » créé par un groupe, conformément à la spécification XBRL, dans le but d’échanger des informations d’entreprise.  

Un **document instancié** XBRL est un rapport financier, par exemple un état financier, préparé conformément à la spécification XBRL. La taxonomie donne la signification des valeurs qui apparaissent dans les documents instanciés. En fait, un document instancié a peu d’utilité si vous ignorez la taxonomie qui a servi à le préparer.  

## <a name="layered-taxonomies" />Taxonomies multicouches

Une taxonomie peut consister en une taxonomie de base, par exemple US GAAP (principes comptables généralement reconnus aux États-Unis) ou IAS (normes comptables internationales), puis avoir une ou plusieurs extensions. Ce type de taxonomie illustre cette structure en se référant à des schémas représentant chacun une taxonomie différente. Lorsque les taxonomies supplémentaires sont chargées dans la base de données, les nouveaux éléments sont simplement ajoutés à la suite des éléments existants.  

## <a name="linkbases" />Liens ressources

Dans la spécification 2 du langage XBRL, la taxonomie est décrite dans plusieurs fichiers XML. Le fichier XML principal est le fichier schéma de la taxonomie (fichier .xsd), qui ne contient qu’une liste désordonnée d’éléments ou d’informations à communiquer. Des liens ressources (fichiers .xml) y sont généralement associés. Les liens ressources contiennent des données complémentaires à la taxonomie brute (fichier .xsd). Il existe six types de lien ressources, dont quatre concernent [!INCLUDE[prod_short](includes/prod_short.md)]. Il s’agit des types suivants :

* Liens ressources libellés : Ce lien ressources contient les libellés ou noms des éléments. Ce fichier peut contenir des libellés en plusieurs langues identifiées par l’attribut XML ’lang’. Les identifiants de langue XML sont généralement des abréviations de deux lettres. Ces abréviations sont le plus souvent explicites, mais n’ont aucun lien avec les codes de langue utilisés par Microsoft Windows ou dans les données de démonstration. Ainsi, lorsque vous recherchez les langues d’une taxonomie, vous pouvez visualiser tous les libellés du premier élément de la taxonomie et donc voir les différentes langues utilisées. Une taxonomie peut être associée à plusieurs liens ressources libellés si chaque lien ressource correspond à une langue.  
* Liens ressources présentation : ce lien ressources comprend des informations sur la structure des éléments, ou plus précisément, il explique comment le créateur de la taxonomie propose que l’application présente la taxonomie à l’utilisateur. Le lien ressources affiche une série de liens. Chacun d’entre eux connecte deux éléments, dans une relation parent-enfant. En appliquant tous ces liens, les éléments peuvent s’afficher de manière hiérarchique. Notez que les liens ressources de présentation servent principalement à vous présenter les éléments.
* Lien ressources calcul : ce lien ressources fournit des informations sur les relations qui unissent les éléments. Sa structure est très semblable à celle du lien ressources présentation, mais chaque lien ou « arc » est pondéré. Un lien peut avoir un poids de 1 ou de –1, selon que l’élément doit être ajouté à son parent ou soustrait de ce dernier. Les relations ne sont pas nécessairement conformes à la représentation visuelle de la taxonomie.  
* Lien ressources de référence : ce lien ressources est un fichier xml contenant des informations supplémentaires sur les données requises par le créateur de la taxonomie.

## <a name="set-up-xbrl-lines" />Configurer les lignes XBRL

Une fois que vous avez importé ou mis à jour la taxonomie, les lignes des schémas doivent être renseignées à l’aide des informations requises pour répondre aux exigences spécifiques des états financiers. Ces informations incluent les données de base sur la société, les états financiers actuels, les notes ajoutées aux états financiers, les tableaux d’analyse supplémentaires, etc.  

Pour configurer les lignes XBRL, mappez les données de taxonomie aux données comptables.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Taxonomies XBRL**, puis choisissez le lien associé.  
2. Sur la page **Taxonomies XBRL**, sélectionnez une taxonomie dans la liste.  
3. Sélectionnez l’option **Lignes**.  
4. Sélectionnez une ligne et renseignez les champs.  
5. Pour plus d’informations sur les champs à renseigner, sélectionnez l’action **Informations**.  
6. Pour configurer le mappage des comptes généraux du plan comptable aux lignes XBRL, sélectionnez l’action **Lignes corresp. cpta. gén**.  
7. Pour ajouter des notes à l’état financier, sélectionnez l’action **Notes**.  

   > [!TIP]
   > Pour exclure des lignes des données exportées, choisissez **NON APPLICABLE** comme type de source.

   > [!NOTE]  
   > Vous ne pouvez exporter que les données correspondant à la sélection dans le champ **Type de Source**. Cela comprend des descriptions et des notes.  

   > [!NOTE]  
   > Les taxonomies peuvent contenir des éléments non compatibles avec [!INCLUDE[prod_short](includes/prod_short.md)]. Si un élément n’est pas pris en charge, le champ **Type de Source** affichera **Non applicable** et le champ **Description** affichera un message d’erreur, tel que **Type inattendu : « type spécifique non reconnu »**. Si vous devez exporter l’élément, choisissez un type de source correspondant. En règle générale, il s’agit d’une constante ou d’une description. Cela vous permettra d’entrer et d’exporter des données, cependant, ces éléments peuvent avoir des règles de validation qui ne peuvent pas être vérifiées avant l’exportation.

## <a name="import-an-xbrl-taxonomy" />Importer une taxonomie XBRL

Lorsque vous utilisez la fonctionnalité XBRL, la première étape consiste à importer la taxonomie correspondante dans la base de données de votre société. Une taxonomie est composée d’un ou de plusieurs schémas, et de liens ressources. Une fois l’import des schémas et des liens ressources effectué, et une fois les liens ressources appliqués aux schémas, vous pouvez configurer les lignes et associer les comptes généraux du plan comptable aux lignes taxonomie appropriées.  

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Taxonomies XBRL**, puis choisissez le lien associé.  
2. Sur la page **Taxonomies XBRL**, créez une ligne et entrez le nom et la description de la taxonomie.  
3. Sélectionnez l’action **Schémas**, puis insérez la description du schéma.  
4. Pour importer le schéma, sur la page **Schémas XBRL**, sélectionnez l’action **Importer**, puis exécutez l’une des étapes suivantes pour télécharger le fichier :

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Pour importer le lien ressources, sur la page **Schémas XBRL**, sélectionnez l’action **Liens ressources**, puis exécutez l’une des étapes suivantes pour télécharger le fichier :

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Vous pouvez alors appliquer le lien ressources au schéma. Répétez ces opérations jusqu’à avoir importé tous les liens ressources.  
7. Sélectionnez l’action **Appliquer à la taxonomie** pour appliquer le lien de ressources au schéma.  

> [!IMPORTANT]  
> Au lieu d’appliquer individuellement les liens de ressources après l’importation, attendez que tous les liens de ressources soient importés avant de les appliquer simultanément. Pour cela, sélectionnez **NON** lorsque vous êtes invité(e) à appliquer le lien ressources récemment importé au schéma. Sélectionnez les lignes avec les liens de ressources à appliquer.  

## <a name="update-an-xbrl-taxonomy" />Mettre à jour une taxonomie XBRL

Lorsqu’une taxonomie est modifiée, vous devez mettre à jour la taxonomie actuelle en conséquence. Une mise à jour est nécessaire en cas de modification d’un schéma ou d’un lien ressources, ou en cas de création d’un nouveau lien ressources. Une fois la taxonomie mise à jour, il vous suffit d’ associer les lignes modifiées ou les nouvelles lignes.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Taxonomies XBRL**, puis choisissez le lien associé.  
2. Sur la page **Taxonomies XBRL**, sélectionnez l’action **Schémas**.  
3. Pour mettre un schéma à jour, sélectionnez-le, puis sélectionnez l’action **Importer**.  
4. Pour mettre à jour ou ajouter un nouveau lien de ressources, sélectionnez l’action **Liens ressources**.  
5. Sélectionnez le lien ressources approprié ou sélectionnez <kbd>Ctrl</kbd>+<kbd>N</kbd> pour ajouter une ligne, sélectionnez le type de lien ressources, puis insérez une description.  
6. Pour importer le lien de ressources, sélectionnez l’action **Importer**.  
7. Sélectionnez **Oui** pour appliquer le lien ressources au schéma.  

## <a name="see-related-training-at-microsoft-learn" />Voir la formation associée sur [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also" />Voir aussi

[Décisionnel pour le secteur de la finance](bi.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
