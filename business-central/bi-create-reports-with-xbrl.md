---
title: Procédure de création d'états avec XBRL | Microsoft Docs
description: XBRL, qui signifie eXtensible Business Reporting Language, est basé sur le langage XML et est utilisé pour marquer des données financières et permettre aux sociétés de traiter et de partager leurs données de manière efficace et précise.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4fd911a708a929a9c73270c05b7729d17d84ec13
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186155"
---
# <a name="create-reports-with-xbrl"></a>Création d'états avec XBRL
XBRL, qui signifie eXtensible Business Reporting Language, est basé sur le langage XML et est utilisé pour marquer des données financières et permettre aux sociétés de traiter et de partager leurs données de manière efficace et précise. L'initiative XBRL permet la génération d'états financiers généraux par de nombreux éditeurs de logiciels ERP et organisations comptables internationales. L'objectif de cette initiative et de fournir un standard pour la génération d'états d'informations financières uniformes pour les banques, les investisseurs et les autorités gouvernementales. Les rapports commerciaux générés de cette manière peuvent inclure :  

 • des états financiers ;  
 • des informations financières ;  
 • des informations non financières ;  
 • des informations de classement de règlementation, tels que les états financiers annuels et trimestriels.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] permet aux sociétés d'implémenter des données en XBRL, et de bénéficier de la flexibilité et de l'automatisation que ce langage offre en matière de collecte et de partage des données.  

## <a name="extensible-business-reporting-language"></a>Langage XBRL (eXtensible Business Reporting Language)
Le langage XBRL (e **X** tensible **B** usiness **R** eporting **L** anguage) est basé sur le langage XML pour la génération d'états financiers. Le langage XBRL offre une norme pour la génération de documents financiers de toute sorte. Cette uniformisation de l'information financière profite à tous les acteurs du secteur, comme les sociétés privées et publiques, les experts comptables, les organismes de réglementation, les analystes, les investisseurs, les acteurs des marchés financiers et les sociétés de prêt, ainsi que les professions tierces telles que les développeurs de logiciel et les personnes chargées du traitement des données.  

Les taxonomies sont tenues à jour par le site www.xbrl.org. Pour télécharger des taxonomies ou pour obtenir plus d'informations, reportez-vous au site Web de XBRL.  

Par exemple, une personne souhaitant obtenir des informations financières à votre sujet peut vous fournir une taxonomie (au format XML) contenant un ou plusieurs schémas, chacun comportant un certain nombre de lignes à renseigner. Ces lignes correspondent aux données financières requises par l'expéditeur. Vous devez importer cette taxonomie dans l'application, puis remplir les schémas en saisissant les comptes correspondant à chaque ligne et le type de période à utiliser, par exemple solde période ou solde au. Dans certains cas, vous devez saisir une constante, comme le nombre d'employés. Vous pouvez alors renvoyer le document instancié (au format XML) à la personne qui vous a demandé les informations. Ainsi, pour les demandes d'informations récurrentes, et à moins que la taxonomie n'ait été modifiée, vous pouvez simplement exporter sur demande de nouveaux documents instanciés correspondant à de nouvelles périodes.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>Le langage XBRL se présente de la manière suivante :  
La **spécification** XBRL explique le principe du langage XBRL, et indique comment créer des documents instanciés XBRL et des taxonomies XBRL. La spécification XBRL présente le langage XBRL en termes techniques et est destinée à des spécialistes.  

Les **schémas** XBRL sont les composants de bas niveau fondamentaux du langage XBRL. Un schéma est un fichier physique au format XSD qui précise comment les documents instanciés et les taxonomies doivent être construits.  

Les **liens ressources** XBRL sont des fichiers physiques au format XML contenant diverses informations concernant les éléments définis par le schéma XBRL, tels que le nombre de langues d'affichage des libellés, les relations entre ces libellés, comment additionner des éléments entre eux, etc.  

Une **taxonomie** XBRL est une « terminologie » ou un « dictionnaire » créé par un groupe, conformément à la spécification XBRL, dans le but d'échanger des informations financières.  

Un **document instancié** XBRL est un rapport financier, par exemple un état financier, préparé conformément à la spécification XBRL. La taxonomie donne la signification des valeurs qui apparaissent dans les documents instanciés. Un document instancié a peu d'utilité si vous ignorez la taxonomie qui a servi à le préparer.  

## <a name="layered-taxonomies"></a>Taxonomies multicouches  
Une taxonomie peut se composer d'une taxonomie de base, par exemple les taxonomies USGAAP ou IAS, ainsi que d'une ou de plusieurs extensions. Ce type de taxonomie illustre cette structure en se référant à des schémas représentant chacun une taxonomie différente. Lorsque les taxonomies supplémentaires sont chargées dans la base de données, les nouveaux éléments sont simplement ajoutés à la suite des éléments existants.  

## <a name="linkbases"></a>Liens ressources  
 Dans la spécification 2 du langage XBRL, la taxonomie est décrite dans plusieurs fichiers XML. Le fichier XML principal est le fichier schéma de la taxonomie (fichier .xsd), qui ne contient qu'une liste désordonnée d'éléments ou d'informations à communiquer. Des liens ressources (fichiers .xml) y sont généralement associés. Les liens ressources contiennent des données complémentaires à la taxonomie brute (fichier .xsd). Il existe six types de lien ressources, dont quatre concernent le langage XBRL pour nom de produit. Il s'agit des types suivants :  

-   Liens ressources libellés : Ce lien ressources contient les libellés ou noms des éléments. Ce fichier peut contenir des libellés en plusieurs langues identifiées par l'attribut XML 'lang'. Les identifiants de langue XML sont généralement des abréviations de deux lettres. Ces abréviations sont le plus souvent explicites, mais n'ont aucun lien avec les codes de langue utilisés par Windows ou dans les données de démonstration. Ainsi, lorsque l'utilisateur recherche les langues d'une taxonomie, il peut visualiser tous les libellés du premier élément de la taxonomie et donc voir les différentes langues utilisées. Une taxonomie peut être associée à plusieurs liens ressources libellés si chaque lien ressources correspond à une langue.  

-   Liens ressources présentation : Ce lien de ressources comprend des informations sur la structure des éléments, ou plus précisément, il explique comment le créateur de la taxonomie propose que l'application présente la taxonomie à l'utilisateur. Le lien de ressources affiche une série de liens. Chacun d'entre eux connecte deux éléments, dans une relation parent-enfant. En appliquant tous ces liens, les éléments peuvent s'afficher de manière hiérarchique. Notez que les liens de ressources de présentation servent principalement à présenter les éléments à l'utilisateur.  

-   Lien ressources calcul : Ce lien ressources fournit des informations sur les éléments et sur les relations qui les unissent. Sa structure est très semblable à celle du lien ressources présentation, mais chaque lien ou « arc » est pondéré. Un lien peut avoir un poids de 1 ou de 1, selon que l'élément doit être ajouté à son parent ou soustrait de ce dernier. Les relations ne sont pas nécessairement conformes à la représentation visuelle de la taxonomie.  

-   Lien ressources de référence : Ce lien ressources est un fichier xml contenant des informations supplémentaires sur les données requises par le créateur de la taxonomie.

## <a name="to-set-up-xbrl-lines"></a>Pour configurer les lignes XBRL  
Une fois que vous avez importé ou mis à jour la taxonomie, les lignes des schémas doivent être renseignées à l'aide des informations requises. Ces informations peuvent inclure les données de base sur l'entreprise, les états financiers, les remarques ajoutées aux états financiers, les tableaux d'analyse supplémentaires et toute autre information requise pour la génération d'états financiers.  

Pour configurer les lignes XBRL, mappez les données de taxonomie aux données comptables.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Taxonomies XBRL**, puis sélectionnez le lien associé.  
2.  Sur la page **Taxonomies XBRL**, sélectionnez une taxonomie dans la liste.  
3.  Sélectionnez l'option **Lignes**.  
4.  Sélectionnez une ligne et renseignez les champs.   
5.  Pour plus d'informations sur les champs à renseigner, sélectionnez l'action **Informations**.  
6.  Pour configurer le mappage des comptes généraux du plan comptable aux lignes XBRL, sélectionnez l'action **Lignes corresp. cpta. gén**.  
7.  Pour ajouter des notes à l'état financier, sélectionnez l'action **Notes**.  

> [!NOTE]  
>  Pour pouvoir exporter des données incluant des descriptions et des remarques, vous devez sélectionner les types origine correspondants dans le champ **Type origine**.  

> [!NOTE]  
>  Vous pouvez indiquer le type ligne **NON APPLICABLE** aux lignes inutiles, afin qu'elles ne soient pas exportées.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Pour importer une taxonomie XBRL  
Lorsque vous utilisez la fonctionnalité XBRL, la première étape consiste à importer la taxonomie correspondante dans la base de données de votre société. Une taxonomie est composée d'un ou de plusieurs schémas, et de liens ressources. Une fois l'import des schémas et des liens ressources effectué, et une fois les liens ressources appliqués aux schémas, vous pouvez configurer les lignes et associer les comptes généraux du plan comptable aux lignes taxonomie appropriées.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Taxonomies XBRL**, puis sélectionnez le lien associé.  
2.  Sur la page **Taxonomies XBRL**, créez une ligne et entrez le nom et la description de la taxonomie.  
3.  Sélectionnez l'action **Schémas**, puis insérez la description du schéma.  
4.  Pour importer le schéma, sur la page **Schémas XBRL**, sélectionnez l'action **Importer**, puis sélectionnez un dossier et un fichier XSD. Cliquez sur le bouton **Ouvrir**.  
5.  Pour importer le lien de ressources, sur la page **Schémas XBRL**, sélectionnez l'action **Liens ressources**, puis sélectionnez un dossier et un fichier XML. Cliquez sur le bouton **Ouvrir**.  
6.  Vous pouvez alors appliquer le lien ressources au schéma. Répétez ces opérations jusqu'à avoir importé tous les liens ressources.  
7. Sélectionnez l'action **Appliquer à la taxonomie** pour appliquer le lien de ressources au schéma.  

> [!IMPORTANT]  
>  Au lieu d'appliquer individuellement les liens de ressources après l'importation, attendez que tous les liens de ressources soient importés avant de les appliquer simultanément. Pour cela, cliquez sur le bouton **NO** lorsque vous êtes invité(e) à appliquer le lien de ressources récemment importé au schéma. Sélectionnez les lignes avec les liens de ressources à appliquer.  

## <a name="to-update-an-xbrl-taxonomy"></a>Pour mettre à jour une taxonomie XBRL  
Lorsqu'une taxonomie est modifiée, vous devez mettre à jour la taxonomie actuelle en conséquence. Une mise à jour est nécessaire en cas de modification d'un schéma ou d'un lien ressources, ou en cas de création d'un nouveau lien ressources. Une fois la taxonomie mise à jour, il vous suffit d' associer les lignes modifiées ou les nouvelles lignes.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Taxonomies XBRL**, puis sélectionnez le lien associé.  
2.  Sur la page **Taxonomies XBRL**, sélectionnez l'action **Schémas**.  
3.  Pour mettre un schéma à jour, sélectionnez-le, puis sélectionnez l'action **Importer**.  
4.  Pour mettre à jour ou ajouter un nouveau lien de ressources, sélectionnez l'action **Liens ressources**.  
5.  Sélectionnez le lien de ressources approprié ou appuyez sur Ctrl+N pour ajouter une ligne, sélectionnez le type de lien de ressources, puis insérez un description.  
6.  Pour importer le lien de ressources, sélectionnez l'action **Importer**.  
7.  Cliquez sur le bouton **Oui** pour appliquer le lien de ressources au schéma.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)    
[Veille économique](bi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
