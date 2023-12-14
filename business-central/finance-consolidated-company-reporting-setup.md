---
title: Configurer la consolidation de la société
description: "Découvrez comment vous pouvez configurer la manière dont les données de différentes sociétés dans Business\_Central sont transmises à une société de consolidation."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
---

# Configurer la consolidation de la société

Avant de pouvoir consolider les écritures comptables de deux ou plusieurs sociétés (filiales) dans une société consolidée, vous devez préparer les plans comptables et la société de consolidation.  

En fonction de la complexité de vos entreprises, il existe deux façons de configurer la consolidation :

* Si les paramètres avancés ne sont pas nécessaires, par exemple inclure une société que vous détenez en partie, vous pouvez utiliser le guide de configuration **Consolidation de la société** pour configurer rapidement une consolidation. Le guide vous aide à effectuer les étapes de base.
* Si des paramètres plus avancés sont nécessaires, vous pouvez configurer vous-même la société consolidée et les centres de profit.
  * Dans chaque centre de profit, spécifiez les comptes généraux à inclure dans la consolidation et la méthode de conversion pour chaque compte.
  * Dans la société consolidée, configurez une fiche centre de profit pour chaque société à inclure dans la consolidation. La fiche centre de profit contient des informations, telles que les dates de l’exercice comptable du centre de profit et le pourcentage de chaque compte à inclure dans la consolidation.

## Configuration d’une consolidation simple

Si votre consolidation est simple, car vous détenez en totalité les centres de profit à consolider, le guide de configuration **Consolidation de la société** vous aide à effectuer les étapes suivantes :

* Créez une nouvelle société consolidée ou consolidez une société que vous avez déjà créée. La société ne doit pas contenir de transactions.
* Affichez un aperçu des résultats. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie que vous pouvez transférer correctement les données principales et les transactions vers la société consolidée.

Pour utiliser le guide de configuration assistée, procédez comme suit :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Configuration assistée**, puis choisissez le lien associé.
2. Choisissez **Traiter les consolidations**, puis effectuez chaque étape du guide de configuration assistée Consolidation de la société.

## Configuration d’une consolidation avancée

Si des paramètres plus avancés sont nécessaires pour votre consolidation, vous pouvez configurer manuellement la consolidation. Par exemple, si vous détenez partiellement des sociétés ou si vous ne souhaitez pas inclure des sociétés.  

### Configurer la société consolidée

D’abord, vous devez définir la société consolidée. Vous configurez la société consolidée de la même manière que vous configurez d’autres sociétés. Pour en savoir plus sur la configuration d’une société, consultez [Se préparer à faire des affaires](ui-get-ready-business.md).  

La liste suivante illustre les principaux aspects de la société consolidée.

1. Configurez le plan comptable.

    Pour en savoir plus sur la configuration d’un plan comptable, consultez [Configuration ou modification du plan comptable](finance-setup-chart-accounts.md).  

    Le plans comptable peut être identique entre un centre de profit et la société consolidée, ou la société consolidée peut avoir un autre plan comptable. Si le plan comptable d’un centre de profit diffère de celui de la société consolidée, vous devez mapper les comptes à ceux du centre de profit. Pour en savoir plus, consultez la section [Préparer les comptes généraux pour la consolidation](#glacc).

2. Ajoutez des centres de profit.

    Pour consolider les données de plusieurs sociétés, vous devez configurer les filiales en tant que centres de profit et spécifier la quantité de leurs soldes à inclure. Pour en savoir plus sur les centres de profit, consultez la section [Ajouter des centres de profit](#busunit).

3. Spécifiez les taux de change, si nécessaire.

    Spécifiez les taux de change si vous consolidez les données des centres de profit qui utilisent des devises différentes. Les trois taux de change que vous pouvez utiliser sont : **Taux moyen (manuel)**, **Taux de clôture** et **Dernier taux de clôture**. Pour en savoir plus sur les taux de change, consultez la section [Spécifier les taux de change pour les consolidations](#exchrates).

4. Consolidez les informations analytiques et les comptes généraux.

    Pour en savoir plus, consultez la section [Inclure ou exclure des axes analytiques](#dim).

### <a name="busunit"></a>Ajouter des centres de profit

Dans la société consolidée, configurez chaque société dont vous souhaitez consolider les données en tant que centre de profit. Avant d’exécuter une consolidation et de générer votre rapport de consolidation, il est recommandé de vérifier les données financières dans chaque centre de profit.

Une grande partie de la configuration du centre de profit consiste à spécifier comment le centre de profit partage ses données financières avec la société consolidée. Il existe des options manuelles et automatisées :

* Pour utiliser un processus manuel, pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne et local, vous pouvez exporter un fichier .xml contenant les écritures comptables du centre de profit. Ensuite, importez le fichier dans la société consolidée.
* Pour automatiser l’échange de données, pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez utiliser une API fournie par [!INCLUDE [prod_short](includes/prod_short.md)] pour partager des données entre les environnements. Si vos sociétés se trouvent dans le même environnement, vous pouvez utiliser l’option **Base de données**.

> [!NOTE]
> L’option API vous permet également de partager les écritures comptables d’autres environnements [!INCLUDE [prod_short](includes/prod_short.md)]. Pour utiliser l’option API, l’utilisateur qui configure la consolidation doit avoir l’autorisation d’accéder aux écritures comptables. Par exemple, les ensembles d’autorisations D365 Basic et D365 Read fournissent l’accès.

1. Connectez-vous à la société consolidée.
2. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Centres de profit**, puis choisissez le lien associé.  
3. Choisissez **Nouveau**, puis remplissez les champs obligatoires dans les raccourcis **Général** et **Comptes généraux**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Lorsque vous renseignez les champs **Date début** et **Date de fin**, assurez-vous de vous conformer aux règles GAAP concernant les périodes fiscales du centre de profit par rapport à la société mère.
4. Dans le raccourci **Importation de données**, dans le champ **Importation de données par défaut**, spécifiez comment vous partagez les écritures comptables avec la société consolidée :

   * Pour partager des données entre des sociétés dans le même environnement, choisissez **Base de données**.
   * Pour partager des données entre des sociétés dans des environnements différents, choisissez **API**, puis remplissez le champ **Point de terminaison de l’API**.
        
        Pour obtenir l’URL du point de terminaison, dans le [!INCLUDE [prod_short](includes/prod_short.md)] de la société du centre de profit, ouvrez la page **Fiche centre de profit** et choisissez l’action **Configurer**. 
   * Pour exporter un fichier .xml et le partager manuellement, choisissez **Format de fichier**.

### <a name="glacc"></a>Préparer les comptes généraux pour la consolidation

Le plan comptable d'une société qui sera consolidée doit spécifier des comptes pour consolidation. Pour chaque compte général de validation dans chaque société, vous devez spécifier le compte général dans la société consolidée vers laquelle transférer le solde. Ce mappage vous permet de consolider des sociétés avec des plans comptables différents.

Si le plan comptable du centre de profit diffère de celui de la société consolidée, vous devez préparer les comptes généraux pour la consolidation. Vous pouvez spécifier les comptes sur lesquels valider les débits et crédits et la méthode à utiliser pour convertir des devises dans la société consolidée.

1. Dans chaque unité commerciale [!INCLUDE [prod_short](includes/prod_short.md)], sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Ouvrez la fiche du compte, puis renseignez les champs du raccourci **Consolidation**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="exchrates"></a>Indiquer des taux de change pour les consolidations

Si un centre de profit utilise une devise différente de celle de la société consolidée, vous devez spécifier des méthodes de conversion de taux de change pour chaque compte avant la consolidation. Pour chaque compte, la valeur du champ **Consolider la méthode de traduction** détermine le taux de change. Dans la société consolidée, sur chaque fiche centre de profit, dans le champ **Table Taux de change devise**, vous spécifiez si la consolidation utilise les taux de change du centre de profit ou de la société consolidée. Si vous utilisez les taux de change de la société consolidée, vous pouvez les modifier pour un centre de profit. Pour les centres de profit, si le champ **Table Taux de change devise** de la fiche centre de profit contient la valeur **Local**, vous pouvez modifier le taux de change à partir de la fiche centre de profit. Les taux de change sont copiés à partir de la table **Taux de change devise**, mais vous pouvez les modifier avant la consolidation.

Le tableau suivant décrit les méthodes de conversion de taux de change que vous pouvez utiliser pour les comptes.

|Taux de change | Utilisation courante |
|---|---|
|Taux moyen (manuel) | Vous calculez manuellement le taux moyen pour la période à consolider. Calculez une moyenne arithmétique ou une estimation au plus près, puis spécifiez le résultat pour chaque centre de profit. Utilisez-le pour les comptes de résultats.|
|Taux de clôture | Utilisé pour les comptes de bilan.|
|Dernier taux de clôture | Taux valide sur le marché des changes à la date pour laquelle le bilan ou l’exercice comptable est préparé. Entrez ce taux pour chaque centre de profit. Utilisez-le pour les comptes de bilan.|
|Taux historique | Taux de change valide au moment de la transaction.|
|Taux composite | Les montants de la période en cours sont convertis au taux moyen et ajoutés au solde précédemment enregistré dans la société consolidée. Vous utilisez généralement cette méthode pour les comptes de bénéfices non répartis. Ces comptes incluent des montants de différentes périodes, ils contiennent donc des montants convertis avec différents taux de change.|
|Taux des fonds propres | Cette option est similaire au **Taux composite**. Les différences sont validées sur des comptes généraux distincts.|

Pour spécifier des taux de change pour les centres de profit, procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de profit**, puis choisissez le lien associé.  
2. Sur la page **Liste des centres de profit**, choisissez le centre de profit, puis choisissez l’action **Taux moyen (manuel)**.  
3. Sur la page **Modifier taux de change**, la valeur du champ **Montant taux de change lié** est copiée à partir de la table **Taux de change devise**, mais vous pouvez la modifier. Fermez la page.  
4. Choisissez l’action **Taux de clôture**.  
5. Dans le champ **Montant taux de change lié**, saisissez le taux de change.

### <a name="dim"></a>Inclure ou exclure des axes analytiques

Vous pouvez consolider des informations analytiques et des comptes généraux.

* Sur les axes analytiques, spécifiez le champ **Code de consolidation** ou laissez-le vide.
  * Pour exclure un axe analytique de la consolidation, laissez le champ **Code de consolidation** vide sur l’axe analytique et ne choisissez pas d’axes analytiques dans les champs **Copier les axes analytiques** dans toutes les fonctions ou états de consolidation.
  * Pour inclure les informations d’axe analytique dans la consolidation, laissez le champ **Code de consolidation** vide. Toutefois, la consolidation ne fonctionne que si les valeurs d’axe analytique du centre de profit sont les mêmes que celles de la société consolidée.
  * Pour consolider le code section analytique dans le centre de profit avec un autre code section analytique dans la société consolidée, renseignez le champ **Code de consolidation** dans les axes analytiques.  
* Ajoutez les axes analytiques aux comptes généraux.

### <a name="exclude"></a>Exclure une société de la consolidation

Si vous ne souhaitez pas inclure un centre de profit dans la consolidation, vous pouvez l’exclure. Pour ce faire, accédez à la fiche centre de profit et désactivez la case à cocher **Consolider**.

### <a name="include"></a>Inclure une société partiellement détenue dans la consolidation

Si vous détenez une société en partie, vous pouvez ajouter un pourcentage de chaque transaction qui reflète le pourcentage que vous détenez. Par exemple, si vous possédez 70 % de la société, la consolidation inclut 70 USD d’une facture de 100 USD. Pour spécifier le pourcentage de la société que vous détenez, accédez à la fiche centre de profit et saisissez le pourcentage dans le champ **% consolidation**.  

## Voir aussi

[Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md)  
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportation de vos données métier vers Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]