---
title: Définir le mode d'échange électronique de documents | Microsoft Docs
description: Vous pouvez utiliser un fournisseur externe de services OCR pour convertir des fichiers PDF ou image en documents électroniques.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 382a95a579482a56597ffae053c53dab92f3739a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245158"
---
# <a name="set-up-data-exchange-definitions"></a>Configurer les définitions d'échange de données
Vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour échanger des données de tables spécifiques avec des données de fichiers externes, par exemple pour recevoir et envoyer des documents électroniques, importer et exporter des données bancaires ou d'autres données, telles que les salaires, les taux de change des devises et les catalogues article. Pour plus d'informations, voir [Échanger des données par voir électronique](across-data-exchange.md).  

Afin de vous préparer à créer une définition d'échange de données pour un fichier ou un flux de données, vous pouvez utiliser le schéma XML associé pour les définir les éléments de données à inclure dans le raccourci **Définitions de colonnes**. Consultez l'étape 6 dans la section [Décrire le formatage de lignes et de colonnes dans un fichier](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Pour plus d'informations, voir [Utiliser des schémas XML pour préparer des définitions d'échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Créez des définitions d'échange de données normalement sur la page **Définition d'échange de données**. Néanmoins, lorsque vous déterminez la définition d'échange de données pour le service d'actualisation des taux de change des devises, démarrez le processus sur la page simplifiée **Fiche Paramètres de mise à jour des taux de change**.  

> [!NOTE]  
>  Si le fichier converti est au format XML, le terme *« colonne »* de cette rubrique doit être interprété comme *« élément XML contenant des données »*.  

Cette rubrique couvre les procédures suivantes :  

* Créer une définition d'échange de données  
* Exporter une définition d'échange de données au format XML pour utilisation par d'autres  
* Importer un fichier XML pour une définition d'échange de données existante  

## <a name="to-create-a-data-exchange-definition"></a>Créer une définition d'échange de données  
La création d'une définition d'échange de données implique deux tâches :  

1. Sur la page **Définition d'échange de données**, décrivez la mise en forme des lignes et des colonnes du fichier.  
2. Sur la page **Correspondance échange de données**, associez les colonnes du fichier de données avec les champs de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Ceci est décrit dans les procédures suivantes.  

> [!TIP]
> Pour voir quels codeunits Microsoft utilise dans les définitions existantes dans le produit standard, consultez les trois champs **Codeunit** de l'en-tête de la page **Mappage de champs** pour chaque définition.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Pour décrire le formatage des lignes et des colonnes dans le fichier  
1. Dans la zone **Rechercher**, entrez **Définitions d'échange de données**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Sur le raccourci **Général**, décrivez la définition d'échange de données et le type de fichier de données en renseignant les champs comme indiqué dans le tableau suivant.  

    |Champ|Définition|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Saisissez un code pour identifier la définition d'échange de données.|  
    |**Nom**|Saisissez un nom pour la définition d'échange de données.|  
    |**Type de fichier**|Spécifiez le type de fichier pour lequel la définition d'échange de données est utilisée. Vous pouvez sélectionner quatre types de fichiers :<br /><br /> -   **XML** : chaînes multicouches de contenu et de balisage entourées de balises indiquant la fonction.<br />-   **Texte variable** : les enregistrements ont une longueur variable et sont séparés par un caractère, comme une virgule ou un point\-virgule. Également appelé *fichier délimité*.<br />-   **Texte fixe** : enregistrements de même longueur, utilisant les caractères du clavier et chaque enregistrement est sur une ligne distincte. Également appelé *fichier de longueur fixe*.<br />- **Json** : chaînes multicouches de contenu dans JavaScript.|  
    |**Type**|Spécifiez pour quel type d'activité la définition d'échange de données est utilisée, par exemple **Exportation de paiement**.|  
    |**Codeunit gestion données**|Spécifiez le codeunit qui transfère les données dans et hors des tables de [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit validation**|Spécifiez le codeunit utilisé pour valider les données par rapport aux règles d'entreprise prédéfinies.|  
    |**Codeunit lecture/écriture**|Spécifiez le codeunit qui traite les données importées avant la mise en correspondance et les données exportées après la correspondance.|  
    |**XMLport lecture/écriture**|Spécifiez le XMLport via lequel un fichier de données importées ou un service passe avant la correspondance et via lequel des données exportées sortent lors d'une écriture dans un fichier de données ou un service après correspondance.|  
    |**Codeunit gestion données ext.**|Spécifiez le codeunit qui transfère les données externes dans et hors de l'infrastructure d'échange de données.|  
    |**Codeunit retour utilisateur**|Spécifiez le codeunit qui effectue des nettoyages après un mappage, par exemple le marquage des lignes lors de leur importation et la suppression des enregistrements temporaires.|  
    |**Encodage du fichier**|Spécifier l'encodage du fichier. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Séparateur de colonnes**|Spécifiez la manière dont les colonnes dans le fichier de données sont distinctes, si le fichier est de type **Texte variable**.|  
    |**Lignes en-tête**|Indiquez le nombre de lignes d'en-tête qui existent dans le fichier.<br /><br /> Ceci garantit que les données d'en-tête ne sont pas importées. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Étiquette en-tête**|Si une ligne d'en-tête existe à plusieurs endroits dans le fichier, saisissez le texte de la première colonne sur la ligne d'en-tête.<br /><br /> Ceci garantit que les données d'en-tête ne sont pas importées. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Étiquette pied de page**|Si une ligne de pied de page existe à plusieurs endroits dans le fichier, saisissez le texte de la première colonne sur la ligne de pied de page.<br /><br /> Ceci garantit que les données de pied de page ne sont pas importées. **Remarque** : ce champ ne s'applique qu'aux importations.|  

4. Sur le raccourci **Définitions des lignes**, décrivez le formatage des lignes dans le fichier de données en renseignant les champs comme indiqué dans le tableau suivant.  

    > [!NOTE]  
    >  Pour importer des relevés bancaires, vous créez une seule ligne pour le format de fichier unique du relevé bancaire que vous souhaitez importer.  
    >   
    >  Pour exporter des règlements, vous pouvez créer une ligne pour chaque type de règlement que vous voulez exporter. Dans ce cas, le raccourci **Définitions des colonnes** affiche des colonnes différentes pour chaque type de paiement.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Saisissez un code pour identifier la ligne dans le fichier.|  
    |**Nom**|Saisissez un code décrivant la ligne dans le fichier.|  
    |**Nombre colonnes**|Indiquez le nombre de colonnes que contient la ligne du fichier de données. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Étiquette ligne données**|Indiquez la position dans le schéma XML associé de l'élément qui représente l'écriture principale du fichier de données. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Espace de noms**|Spécifiez l'espace de noms qui est prévu dans le fichier, pour activer la validation de l'espace de noms. Vous pouvez laisser ce champ vide si vous ne souhaitez pas activer la validation d'espace de noms.|  

5. Répétez l'étape 4 pour créer une ligne pour chaque type de fichier de données que vous voulez exporter.  

     Planifiez maintenant de décrire le formatage des colonnes du fichier de données en renseignant les champs du raccourci **Définitions des colonnes** comme indiqué dans le tableau suivant. Vous pouvez utiliser la structure du fichier, par exemple un fichier .XSD pour le fichier de données afin de pré remplir le raccourci avec les éléments appropriés. Pour plus d'informations, voir [Utiliser des schémas XML pour préparer des définitions d'échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. Sur le raccourci **Définitions de colonnes**, sélectionnez **Extraire la structure de fichiers**.  
7. Sur la page **Extraire structure de fichiers**, sélectionnez la structure de fichier associée, puis choisissez le bouton **OK**. Les lignes du raccourci **Définitions de colonnes** sont renseignées conformément à la structure du fichier de données.  
8. Dans le raccourci **Définitions des colonnes**, modifiez ou renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N° colonne**|Spécifiez le numéro qui indique la position de la colonne sur la ligne du fichier.<br /><br /> Pour les fichiers XML, spécifiez le numéro qui indique le type d'élément dans le fichier contenant les données.|  
    |**Nom**|Spécifiez le nom de la colonne.<br /><br /> Pour les fichiers XML, spécifiez le balisage qui indique les données à échanger.|  
    |**Type de données**|Spécifiez si les données à échanger sont de type **Texte**, **Date** ou **Décimale**.|  
    |**Format données**|Spécifiez le format des données, le cas échéant. Par exemple, **MM/JJ/AAAA** si le type de données est **Date**. **Remarque :** pour l'exportation, spécifiez le format de données en fonction de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour l'importation, spécifiez le format de données en fonction du .NET Framework. Pour plus d'informations, voir [Chaînes de format de date et heure standard](https://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Culture mise en forme données**|Spécifiez la culture du format de données, le cas échéant. Par exemple, **en-US** si le type de données est **Décimale** pour être sûr que la virgule est utilisée comme séparateur de .000, conformément au format américain. Pour plus d'informations, voir [Chaînes de format de date et heure standard](https://go.microsoft.com/fwlink/?LinkID=323466). **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Longueur**|Spécifiez la longueur de la ligne de longueur fixe qui comporte la colonne si le fichier de données est de type **Texte fixe**.|  
    |**Description**|Entrez une description de la colonne, à titre d'information.|  
    |**Chemin**|Indiquez la position de l'élément dans le schéma XML lié.|  
    |**Identifiant signe négatif**|Saisissez la valeur qui est utilisée dans le fichier de données pour identifier les montants négatifs, dans les fichiers de données qui ne peuvent pas contenir des signes négatifs. Cet identifiant est utilisé pour inverser les montants identifiés aux montants négatifs lors de l'import. **Remarque** : ce champ ne s'applique qu'aux importations.|  
    |**Fixe**|Spécifiez les données à exporter dans cette colonne, telles que les informations supplémentaires sur le type de paiement. **Remarque** : ce champ ne s'applique qu'aux exportations.|  

9. Répétez l'étape 8 pour chaque colonne ou élément XML du fichier de données qui contient des données que vous souhaitez échanger avec [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 L'étape suivante de la création de la définition d'échange de données consiste à choisir les correspondances entre les colonnes ou les éléments XML du fichier de données et les champs de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  La correspondance spécifique dépend de l'objectif commercial du fichier de données à échanger et des variations locales. Même le standard bancaire SEPA a des variations locales. [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge en natif l'importation de fichiers de relevé bancaire SEPA CAMT. Ceci est représenté par le code d'enregistrement de définition d'échange de données **SEPA CAMT** sur la page **Définitions d'échange de données**. Pour plus d'informations sur le mappage de champs spécifique de cette prise en charge de SEPA CAMT, voir [Mappage de champs lors de l'importation de fichiers SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Pour mapper les colonnes du fichier de données aux champs de [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Sur le raccourci **Définitions de lignes**, sélectionnez la ligne pour laquelle vous souhaitez associer les colonnes avec les champs, puis sélectionnez **Correspondance champ**. La page **Correspondance échange de données** s'ouvre.  
2. Dans le raccourci **Général**, spécifiez les paramètres de mappage en renseignant les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**ID Table**|Indiquez la table qui contient les champs vers lesquels ou à partir desquels des données sont échangées en fonction de la correspondance.|  
    |**Utiliser comme table intermédiaire**|Spécifiez si la table que vous sélectionnez dans le champ **ID table** est une table intermédiaire de stockage des données importées avant leur mappage vers la table cible.<br /><br /> Vous utilisez généralement une table intermédiaire lorsque la définition d'échange de données est utilisée pour importer et convertir des documents électroniques, tels que des factures fournisseur en factures achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Échanger des données par voir électronique](across-data-exchange.md).|  
    |**Nom**|Saisissez un nom pour les paramètres de correspondance.|  
    |**Codeunit pré-mappage**|Spécifiez le codeunit qui prépare la mise en correspondance entre les champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et les données externes.|  
    |**Correspondance Codeunit**|Spécifiez le codeunit qui est utilisé pour mettre en correspondance les colonnes ou les éléments de données XML spécifiés avec les champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit post-mappage**|Spécifiez le codeunit qui effectue la mise en correspondance entre les champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et les données externes. **Remarque :** lors de l'utilisation de la fonction Service de conversion de données bancaires, le codeunit convertit les données exportées de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers un format générique qui est prêt pour l'exportation. Pour l'importation, le codeunit convertit les données externes dans un format prêt à l'importation dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  Sur le raccourci **Correspondance champ**, spécifiez la correspondance entre les colonnes et les champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en renseignant les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N° colonne**|Spécifiez la colonne dans le fichier de données pour laquelle vous souhaitez définir une fiche.<br /><br /> Vous pouvez uniquement sélectionner les colonnes qui sont représentées par des lignes sur le raccourci **Définitions colonne** de la page **Définition d'échange de données**.|  
    |**ID de champ**|Spécifiez à quel champ correspond la colonne dans le champ **N° colonne** .<br /><br /> Vous pouvez uniquement choisir parmi des champs existant dans la table que vous avez spécifiée dans le champ **Table** du Raccourci **General**.|  
    |**Supplémentaires**|Indiquez que la fiche sera ignorée si le champ est vide. **Remarque :** si vous n'activez pas cette case à cocher, une erreur d'exportation aura lieu si le champ est vide. **Remarque** : ce champ ne s'applique qu'aux exportations.|  
    |**ID table cible**|Uniquement visible lorsque la case à cocher **Utiliser comme table intermédiaire** est cochée.<br /><br /> Spécifiez la table à laquelle la valeur du champ **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l'importation des données.|  
    |**Libellé table cible**|Uniquement visible lorsque la case à cocher **Utiliser comme table intermédiaire** est cochée.<br /><br /> Spécifiez le nom de la table dans le champ **ID table cible**, qui est la table à laquelle la valeur du champ **Titre colonne** est mappée, lorsque vous utilisez une table intermédiaire pour l'importation des données.|  
    |**ID champ cible**|Uniquement visible lorsque la case à cocher **Utiliser comme table intermédiaire** est cochée.<br /><br /> Spécifiez le champ dans la table cible auquel la valeur du champ **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l'importation des données.|  
    |**Libellé champ cible**|Uniquement visible lorsque la case à cocher **Utiliser comme table intermédiaire** est cochée.<br /><br /> Spécifiez le nom du champ dans la table cible auquel la valeur de la colonne **Titre colonne** est mappée lorsque vous utilisez une table intermédiaire pour l'importation des données.|  
    |**Supplémentaires**|Uniquement visible lorsque la case à cocher **Utiliser comme table intermédiaire** est cochée.<br /><br /> Spécifiez que la correspondance doit être ignorée si le champ est vide. Si vous n'activez pas cette case à cocher, une erreur d'exportation aura lieu si le champ est vide.|  

La définition d'échange de données est désormais prête à être activée pour les utilisateurs. Pour plus d'informations, voir [Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Configurer des virements SEPA](finance-how-to-set-up-sepa-credit-transfer.md), [Configurer un prélèvement SEPA](finance-how-to-set-up-sepa-direct-debit.md) et [Exécuter les paiements avec le service de conversion de données bancaires ou un virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

Lorsque vous avez créé la définition d'échange de données pour un fichier de données spécifique, vous pouvez exporter la définition d'échange de données en tant que fichier XML qui peut être utilisé pour activer rapidement l'importation du fichier de données en question. Ceci est décrit dans la procédure suivante.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Exporter une définition d'échange de données au format XML pour utilisation par d'autres  
1. Dans la zone **Rechercher**, entrez **Définitions d'échange de données**, puis sélectionnez le lien associé.  
2. Sélectionnez la définition d'échange de données que vous voulez exporter.  
3. Choisissez l'action **Exporter définition d'échange de données**.  
4. Enregistrez le fichier XML qui représente la définition d'échange de données dans un emplacement approprié.  

    Si une définition d'échange de données a déjà été créée, il vous suffit d'importer le fichier XML dans l'infrastructure d'échange de données. Ceci est décrit dans la procédure suivante.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Importer une définition d'échange de données existante  
1. Enregistrez le fichier XML qui représente la définition d'échange de données dans un emplacement approprié.  
2. Dans la zone **Rechercher**, entrez **Définitions d'échange de données**, puis sélectionnez le lien associé.  
3. Sélectionnez l'action **Nouveau**. La page **Définition d'échange de données** s'ouvre.  
4. Choisissez l'action **Importer définition d'échange de données**.  
5. Choisissez le fichier que vous avez enregistré à l'étape 1.  

## <a name="see-also"></a>Voir aussi  
[Configuration de l'échange de données](across-set-up-data-exchange.md)  
[Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurer des virements SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Configurer un prélèvement SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Exécuter les paiements avec le service de conversion de données bancaires ou un virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
