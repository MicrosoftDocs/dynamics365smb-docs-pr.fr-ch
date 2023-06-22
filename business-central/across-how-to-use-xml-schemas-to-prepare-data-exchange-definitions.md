---
title: "Schémas\_XML pour préparer des définitions d’échange de données"
description: Utilisez des schémas XML pour configurer l’infrastructure d’échange de données afin de définir les éléments de données avec lesquels vous souhaitez échanger.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions" />Utiliser des schémas XML pour préparer des définitions d’échange de données

Pour activer l’importation/exportation des données dans des fichiers XML à travers l’infrastructure d’échange de données de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez utiliser des schémas XML pour définir les éléments de données à échanger avec [!INCLUDE[prod_short](includes/prod_short.md)]. Vous effectuez ce travail sur la page **Visionneuse de schéma XML** en chargeant le fichier de schéma XML, en sélectionnant les éléments de données appropriés, puis en initialisant une définition d’échange de données.  

 Lorsque vous avez défini quels éléments de données inclure selon le schéma XML, vous pouvez utiliser l’action **Générer définition d’échange de données** pour initialiser une définition d’échange de données basée sur les éléments de données sélectionnés, que vous complétez dans l’infrastructure d’échange de données. Cela crée un enregistrement sur la page **Définitions échange comptabilité** où vous continuez en définissant quels éléments de la liste des fichiers correspondent à quels champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

 Cette rubrique contient les procédures suivantes :  

- Charger un fichier de schéma XML  

- Sélectionner ou supprimer des nœuds dans un schéma XML  

- Générer une définition d’échange de données basée sur un schéma XML  

## <a name="to-load-an-xml-schema-file" />Charger un fichier de schéma XML

1. Assurez-vous que le fichier de schéma XML approprié est disponible. L’extension du fichier est .xsd.  

2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Schémas XML**, puis choisissez le lien associé.  

3. Sélectionnez l’action **Nouveau**.  

4. Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Indiquez un code pour identifier le schéma XML.|  
    |**Description**|Spécifiez une description du schéma XML.|  

     Le champ **Espace de noms cible** spécifie un espace de noms dans le fichier de schéma XML qui a été chargé pour la ligne.  

5. Sélectionnez l’action **Charger le schéma**, puis sélectionnez le fichier de schéma XML.  

     Lorsque le fichier est chargé, les autres champs de la ligne sont renseignés à l’aide des informations du fichier, et la case **Le schéma est chargé** est cochée.  

    > [!NOTE]  
    >  L’arborescence du schéma XML chargé est réduite par défaut. Vous développez chaque nœud en choisissant le bouton **+** sur le nœud. Pour développer tous les nœuds, sélectionnez **Développer tout** sur le ruban.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema" />Sélectionner ou supprimer des nœuds dans un schéma XML

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Visionneuse de schéma XML**, puis choisissez le lien associé.  

2. Renseignez les champs de l’en-tête, comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code schéma XML**|Spécifiez le fichier de schéma XML que vous avez chargé à l’étape 5 dans la section « Charger un fichier de schéma XML ».|  
    |**Nouveau n° de XMLport**|Spécifiez le numéro du XMLport qui est créé pour ce schéma XML lorsque vous sélectionnez l’action **Générer XMLport**.|  

     Les lignes sont à présent remplies avec des nœuds représentant tous les éléments figurant dans le schéma XML. Les nœuds des éléments qui sont obligatoires selon le schéma XML sont activés par défaut.  

3. Sur la première ligne, dans la colonne **Nom noeud**, développez le nœud **Document**, puis développez progressivement les nœuds sous-jacents que vous souhaitez examiner.  

     Sinon, cliquez avec le bouton droit sur un nœud, puis choisissez **Développer tout**.  

4. Sélectionnez l’une des actions suivantes pour modifier les nœuds qui sont affichés.  

    |**Fonction**|Désignation|  
    |----------------|---------------------------------------|  
    |**Afficher tout**|Tous les nœuds sont affichés.|  
    |**Masquer non obligatoire**|Seuls les nœuds représentant les éléments qui sont obligatoires selon le schéma XML sont affichés. Les nœuds sont généralement indiqués par un **1** dans le champ **MinOccurs**.<br /><br /> Choisissez **Afficher tout** pour rétablir l’affichage.|  
    |**Masquer non sélectionné**|Seuls les nœuds dont la case à cocher **Sélectionné** est activée sont affichés.<br /><br /> Choisissez **Afficher tout** pour rétablir l’affichage.|  

5. Choisissez l’action **Modifier**.  

6. Dans le champ **Sélectionné**, spécifiez pour chaque nœud si vous souhaitez que l’élément soit pris en charge dans la définition d’échange de données pour le fichier bancaire SEPA connexe.  

    > [!NOTE]  
    >  Lorsque vous sélectionnez un nœud enfant obligatoire, tous les nœuds parents au-dessus de lui sont également sélectionnés.  

7. Sélectionnez l’action **Sélectionner tous les éléments obligatoires** pour resélectionner tous les nœuds représentant des éléments qui sont obligatoires en fonction du schéma XML.  

8. Sélectionnez l’action **Désélectionner tout** pour désactiver toutes les options.  

     Le champ **Choix** spécifie que le nœud a deux ou plusieurs nœuds frère qui fonctionnent comme options.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema" />Générer une définition d’échange de données basée sur un schéma XML

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Schémas XML**, puis choisissez le lien associé.  

2. Sélectionnez le schéma XML approprié, puis sélectionnez l’action **Ouvrir la visionneuse de schéma XML**.  

3. Assurez-vous que les nœuds appropriés sont sélectionnés. Pour plus d’informations, reportez-vous à la section « Sélectionner ou supprimer des nœuds dans un schéma XML ».  

4. Sur la page **Visionneuse de schéma XML**, sélectionnez l’action **Générer définition d’échange de données**.  

 Une définition d’échange de données est créée sur la page **Définitions échange comptabilité**, que vous pouvez renseigner en indiquant quels éléments du fichier correspondent à quels champs de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Vous pouvez également utiliser la fonction **Extraire structure de fichiers** de la page **Définitions échange comptabilité**, qui utilise la fonctionnalité de la page **Visionneuse de schéma XML** pour préremplir le raccourci **Définitions colonne**.  

> [!NOTE]
> Dans la vague 1 du lancement de la version 2019 et versions antérieures, vous pouviez générer un XMLport basé sur le schéma, puis l’importer dans votre solution. Cela n’est plus possible.

## <a name="see-also" />Voir aussi

[Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md)  
[Exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[À propos de l’infrastructure d’échange de données](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
