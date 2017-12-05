---
title: "Créer des objets XMLport basés sur des schémas XML | Microsoft Docs"
description: "Utilisez des schémas XML pour configurer l'infrastructure d'échange de documents."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 5b10eaff0d412ee26ead2137a353054c41d05113
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a>Procédure : Utiliser des schémas XML pour préparer des définitions d'échange de données
Pour activer l'importation/exportation des données dans des fichiers XML à travers l'infrastructure d'échange de données de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez utiliser des schémas XML pour définir les éléments de données à échanger avec [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous effectuez ce travail dans la fenêtre **Visionneuse de schéma XML** en chargeant le fichier de schéma XML, en sélectionnant les éléments de données appropriés, puis en initialisant soit une définition d'échange de données ou un XMLport.  

 Lorsque vous avez défini les éléments de données à inclure en fonction du schéma XML, vous pouvez utiliser l'action **Générer XMLport** pour créer l'objet XMLport.  

 Vous pouvez aussi utiliser l'action **Générer définition d'échange de données** pour initialiser une définition d'échange de données basée sur les éléments de données sélectionnés, que vous complétez dans l'infrastructure d'échange de données. Cela crée un enregistrement dans la fenêtre **Définitions échange comptabilité** où vous continuez en définissant quels éléments de la liste des fichiers correspondent à quels champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, reportez vous à [Procédure : configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md).  

 Cette rubrique contient les procédures suivantes :  

-   Charger un fichier de schéma XML  

-   Sélectionner ou supprimer des nœuds dans un schéma XML  

-   Générer une définition d'échange de données basée sur un schéma XML  

-   Générer un XMLport pour le fichier basé sur un schéma XML  

-   Pour importer un XMLport dans l'Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Charger un fichier de schéma XML  

1.  Assurez-vous que le fichier de schéma XML approprié est disponible. L'extension du fichier est .xsd.  

2.  Dans la zone **Rechercher**, entrez **Schémas XML**, puis sélectionnez le lien associé.  

3.  Sous l'onglet **Accueil**, dans le groupe **Nouveau**, choisissez **Nouveau**.  

4.  Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Indiquez un code pour identifier le schéma XML.|  
    |**Description**|Spécifiez une description du schéma XML.|  

     Le champ **Espace de noms cible** spécifie un espace de noms dans le fichier de schéma XML qui a été chargé pour la ligne.  

5.  Sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Charger schéma**, puis sélectionnez le fichier de schéma XML.  

     Lorsque le fichier est chargé, les autres champs de la ligne sont renseignés à l'aide des informations du fichier, et la case **Le schéma est chargé** est cochée.  

    > [!NOTE]  
    >  L'arborescence du schéma XML chargé est réduite par défaut. Vous développez chaque nœud en choisissant le bouton **+** sur le nœud. Pour développer tous les nœuds, sélectionnez **Développer tout** sur le ruban.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Sélectionner ou supprimer des nœuds dans un schéma XML  

1.  Dans la zone **Rechercher**, entrez **Visionneuse de schéma XML**, puis sélectionnez le lien associé.  

2.  Renseignez les champs de l'en-tête, comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code schéma XML**|Spécifiez le fichier schéma XML que vous avez chargé à l'étape 5 dans la section « Pour charger un fichier schéma XML ».|  
    |**Nouveau n° XMLport**|Spécifiez le numéro du XMLport qui est créé pour ce schéma XML lorsque vous sélectionnez l'action **Générer XMLport**.|  

     Les lignes sont à présent remplies avec des nœuds représentant tous les éléments figurant dans le schéma XML. Les nœuds des éléments qui sont obligatoires selon le schéma XML sont activés par défaut.  

3.  Sur la première ligne, dans la colonne **Nom noeud**, développez le nœud **Document**, puis développez progressivement les nœuds sous-jacents que vous souhaitez examiner.  

     Sinon, cliquez avec le bouton droit sur un nœud, puis choisissez **Développer tout**.  

4.  Sous l'onglet **Accueil**, dans le groupe **Affichage**, choisissez l'une des actions suivantes pour modifier les nœuds qui sont affichés.  

    |**Fonction**|Désignation|  
    |----------------|---------------------------------------|  
    |**Afficher tout**|Tous les nœuds sont affichés.|  
    |**Masquer non obligatoire**|Seuls les nœuds représentant les éléments qui sont obligatoires selon le schéma XML sont affichés. Les nœuds sont généralement indiqués par un **1** dans le champ **MinOccurs**.<br /><br /> Choisissez **Afficher tout** pour rétablir l'affichage.|  
    |**Masquer non sélectionné**|Seuls les nœuds dont la case à cocher **Sélectionné** est activée sont affichés.<br /><br /> Choisissez **Afficher tout** pour rétablir l'affichage.|  

5.  Sous l'onglet **Accueil**, dans le groupe **Gestion**, sélectionnez **Modifier**.  

6.  Dans le champ **Sélectionné**, spécifiez pour chaque nœud si vous souhaitez que l'élément soit pris en charge dans la définition d'échange de données pour le fichier bancaire SEPA connexe.  

    > [!NOTE]  
    >  Lorsque vous sélectionnez un nœud enfant obligatoire, tous les nœuds parents au-dessus de lui sont également sélectionnés.  

7.  Sélectionnez l'action **Sélectionner tous les éléments obligatoires** pour resélectionner tous les nœuds représentant des éléments qui sont obligatoires en fonction du schéma XML.  

8.  Sélectionnez l'action **Désélectionner tout** pour désactiver toutes les options.  

     Le champ **Choix** spécifie que le nœud a deux ou plusieurs nœuds frère qui fonctionnent comme options.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Générer une définition d'échange de données basée sur un schéma XML  

1.  Dans la zone **Rechercher**, entrez **Schémas XML**, puis sélectionnez le lien associé.  

2.  Sélectionnez le schéma XML approprié, puis sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Ouvrir visionneuse de schéma XML**.  

3.  Assurez-vous que les nœuds appropriés sont sélectionnés. Pour plus d'informations, reportez-vous à la section « Sélectionner ou supprimer des nœuds dans un schéma XML ».  

4.  Dans la fenêtre **Visionneuse de schéma XML**, sous l'onglet **Accueil**, dans le groupe **Processus**, sélectionnez **Générer définition d'échange de données**.  

 Une définition d'échange de données est créée dans la fenêtre **Définitions échange comptabilité**, que vous pouvez renseigner en indiquant quels éléments du fichier correspondent à quels champs de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, reportez vous à [Procédure : configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Vous pouvez également utiliser la fonction **Extraire structure de fichiers** de la fenêtre **Définitions échange comptabilité**, qui utilise la fonctionnalité de la fenêtre **Visionneuse de schéma XML** pour préremplir le raccourci **Définitions colonne**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Générer un XMLport basé sur un schéma XML  

1.  Dans la zone **Rechercher**, entrez **Schémas XML**, puis sélectionnez le lien associé.  

2.  Sélectionnez le schéma XML approprié, puis sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Ouvrir visionneuse de schéma XML**.  

3.  Dans le champ **Nouveau n° XMLport**, spécifiez le numéro qui sera accordé au nouvel objet XMLport lorsqu'il sera généré.  

4.  Assurez-vous que les nœuds appropriés sont sélectionnés. Pour plus d'informations, reportez-vous à la section « Sélectionner ou supprimer des nœuds dans un schéma XML ».  

5.  Sous l'onglet **Accueil**, dans le groupe **Traitement**, choisissez **Générer XMLPort**, puis enregistrez l'objet en tant que fichier .txt dans un emplacement approprié.  

6. Importez le nouvel objet XMLport dans l'environnement de développement [!INCLUDE[d365fin](includes/d365fin_md.md)] et compilez-le.

## <a name="see-also"></a>Voir aussi  
[Procédure : configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md)   
[Procédure : exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md)   
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[À propos de l'infrastructure d'échange de données](across-about-the-data-exchange-framework.md)

