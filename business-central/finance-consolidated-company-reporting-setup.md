---
title: Configurer la consolidation de la société
description: "Découvrez comment vous pouvez configurer la manière dont les données de différentes sociétés dans Business\_Central sont transmises à une société de consolidation."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-company-consolidation" />Configurer la consolidation de la société

Avant de pouvoir consolider les écritures comptables de deux ou plusieurs sociétés distinctes (filiales) dans une société consolidée, vous devez préparer le plan comptable et la société de consolidation.  

En fonction de la complexité de vos entreprises, il existe deux façons de configurer la consolidation :

* Si les paramètres avancés ne sont pas nécessaires, par exemple l’ajout d’une société que vous détenez en partie, vous pouvez utiliser le guide de configuration assistée **Consolidation de la société** pour configurer rapidement une consolidation. Le guide vous aide à effectuer les étapes de base.
* Si des paramètres plus avancés sont nécessaires, vous pouvez configurer vous-même la société consolidée et les centres de profit.
  * Dans chaque centre de profit, spécifiez les comptes généraux devant être inclus dans la consolidation, et spécifiez la méthode de conversion de la consolidation pour chaque compte.
  * Dans la société consolidée, configurez une fiche centre de profit pour chaque société devant être inclue dans la consolidation. La fiche centre de profit contient des informations, telles que les dates de l’exercice comptable du centre de profit et le pourcentage de chaque compte devant être inclus dans la consolidation.

## <a name="simple-consolidation-setup" />Configuration d’une consolidation simple

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Si votre consolidation est simple, car vous détenez en totalité les centres de profit à consolider, le guide de configuration assistée **Consolidation de la société** vous aide à effectuer les étapes suivantes :

* Choisissez si vous souhaitez créer une société consolidée, ou consolider les données dans une société que vous avez déjà créée pour la consolidation. La société ne doit pas contenir de transactions.
* Affichez un aperçu des résultats. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie que les données de base et les transactions peuvent être transférées avec succès vers la société consolidée.

Pour utiliser le guide de configuration assistée, procédez comme suit :

1. Dans le tableau de bord **Comptable**, choisissez l’action **Configuration assistée**.
2. Choisissez **Configurer la création d’états de consolidation**, puis effectuez chaque étape du guide de configuration assistée.

## <a name="advanced-consolidation-setup" />Configuration d’une consolidation avancée

Si des paramètres plus avancés sont nécessaires pour votre consolidation, vous pouvez configurer manuellement la consolidation. Par exemple, si vous détenez partiellement des sociétés, ou si vous ne souhaitez pas inclure des sociétés dans la consolidation.  

### <a name="set-up-the-consolidated-company" />Configurer la société consolidée

D’abord, vous devez définir la société consolidée. Vous configurez la société consolidée de la même manière que vous configurez d’autres sociétés. Pour plus d’informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).  

La liste suivante illustre les principaux aspects de la société consolidée.

1. Configurer le plan comptable

    Pour plus d’informations, voir [Configuration ou modification du plan comptable](finance-setup-chart-accounts.md).  

    Le plans comptable peut être identique entre un centre de profit et la société consolidée, ou la société consolidée peut avoir un autre plan comptable. Si le plan comptable d’un centre de profit est différent de celui de la société consolidée, vous devez spécifier le mappage entre les comptes sur les comptes du centre de profit. Pour plus d’informations, voir la section [Préparer les comptes généraux pour la consolidation](#glacc).

2. Ajouter des centres de profit

    Pour consolider les données financières de plusieurs sociétés dans une société consolidée, vous devez entrer des informations sur la filiale, telles que les centres de profit à inclure et la mesure dans laquelle leurs chiffres seront inclus.

    Pour plus d’informations, voir la section [Ajouter des centres de profit](#busunit).
3. Vous pouvez spécifier des taux de change lors de la consolidation des états financiers de centres de profit si les états financiers sont en devise étrangère.

    Les trois taux de change utilisés sont **Taux moyen (manuel)**, **Taux de clôture** et **Dernier taux de clôture**. Pour plus d’informations, voir la section [Spécifier les taux de change pour les consolidations](#exchrates).
4. Vous pouvez consolider des informations analytiques et des comptes généraux.

    Pour plus d’informations, voir la section [Inclure ou exclure des axes analytiques](#dim).

### <a name="a-namebusunitaadd-business-units" /><a name="busunit"></a>Ajouter des centres de profit

[!INCLUDE[prod_short](includes/prod_short.md)] vous permet de créer une liste de centres de profit à consolider, de vérifier les données comptables avant leur consolidation, d’importer des fichiers et de générer des états de consolidation.  

1. Connectez-vous à la société consolidée.
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de profit**, puis choisissez le lien associé.  
3. Sélectionnez **Nouveau**, puis renseignez les champs requis. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Lorsque vous renseignez les champs **Date début** et **Date de fin**, assurez-vous de vous conformer aux règles GAAP concernant les périodes fiscales du centre de profit par rapport à la société mère.
4. Répétez l’étape 3 pour chaque centre de profit supplémentaire

Si votre centre de profit utilise une devise étrangère, indiquez le taux de change à utiliser dans la consolidation. Vous devez également entrer des informations de consolidation sur les comptes généraux du centre de profit. Ces processus sont décrits dans les sections suivantes.

### <a name="a-nameglaccaprepare-general-ledger-accounts-for-consolidation" /><a name="glacc"></a>Préparer les comptes généraux pour la consolidation

Le plan comptable d’une société qui sera consolidée doit spécifier des comptes pour consolidation. Vous devez spécifier chaque compte général de validation de chaque société dans la société consolidée vers laquelle le solde sera transféré lors de la consolidation. Il s’agit d’un mappage permettant la consolidation de sociétés dont les plans comptables diffèrent.

Si le plan comptable du centre de profit diffère de celui de la société consolidée, vous devez préparer les comptes généraux pour la consolidation. Vous pouvez spécifier les comptes sur lesquels valider les débits et crédits et la méthode à utiliser pour convertir des devises dans la société consolidée. Par exemple, cela est utile si vous exécutez souvent l’état.

1. Dans chaque unité commerciale [!INCLUDE [prod_short](includes/prod_short.md)], sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Ouvrez la fiche du compte, puis renseignez les champs du raccourci **Consolidation**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="a-nameexchratesaspecify-exchange-rates-for-consolidations" /><a name="exchrates"></a>Indiquer des taux de change pour les consolidations

Si un centre de profit utilise une devise différente de celle de la société consolidée, vous devez spécifier des méthodes de conversion de taux de change pour chaque compte avant la consolidation. Pour chaque compte, la valeur du champ **Consolider la méthode de traduction** détermine le taux de change. Dans la société consolidée, sur chaque fiche centre de profit, dans le champ **Table Taux de change devise**, vous spécifiez si la consolidation utilise les taux de change du centre de profit ou de la société consolidée. Si vous utilisez les taux de change de la société consolidée, vous pouvez les modifier pour un centre de profit. Pour les centres de profit, si le champ **Table Taux de change devise** de la fiche centre de profit contient la valeur **Local**, vous pouvez modifier le taux de change à partir de la fiche centre de profit. Les taux de change sont copiés à partir de la table **Taux de change devise**, mais vous pouvez les modifier avant la consolidation.

Le tableau suivant décrit les méthodes de conversion de taux de change que vous pouvez utiliser pour les comptes.

|Taux de change | Utilisation courante |
|---|---|
|Taux moyen (manuel) | Vous calculez manuellement le taux moyen pour la période à consolider. Calculez une moyenne arithmétique ou une estimation au plus près, puis spécifiez le résultat pour chaque centre de profit. Utilisé pour les comptes résultats.|
|Taux de clôture | Utilisé pour les comptes de bilan.|
|Dernier taux de clôture | Taux valide sur le marché des changes à la date pour laquelle le bilan ou l’exercice comptable est préparé. Entrez ce taux pour chaque centre de profit. Utilisé pour les comptes de bilan.|
|Taux historique | Taux de change valide au moment de la transaction.|
|Taux composite | Les montants de la période en cours sont convertis au taux moyen et ajoutés au solde précédemment enregistré dans la société consolidée. Cette méthode est généralement utilisée pour les comptes bénéfices non répartis, car ils incluent des montants provenant de périodes différentes et constituent donc un composé des montants convertis avec différents taux de change.|
|Taux des fonds propres | Il est similaire au **Taux composite**. Les différences sont validées sur des comptes généraux distincts.|

Pour spécifier des taux de change pour les centres de profit, procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de profit**, puis choisissez le lien associé.  
2. Sur la page **Liste des centres de profit**, choisissez le centre de profit, puis choisissez l’action **Taux moyen (manuel)**.  
3. Sur la page **Modifier taux de change**, la valeur du champ **Montant taux de change lié** est copiée à partir de la table **Taux de change devise**, mais vous pouvez la modifier. Fermez la page.  
4. Choisissez l’action **Taux de clôture**.  
5. Dans le champ **Montant taux de change lié**, saisissez le taux de change.

### <a name="a-namedimainclude-or-exclude-dimensions" /><a name="dim"></a>Inclure ou exclure des axes analytiques

Vous pouvez consolider des informations analytiques et des comptes généraux.

* Sur les axes analytiques pertinents, spécifiez le champ **Code de consolidation**, ou laissez-le vide
  * Pour exclure un axe analytique de la consolidation, laissez le champ **Code de consolidation** vide sur l’axe analytique et ne choisissez pas les axes analytiques dans les champs **Copier les axes analytiques** dans toutes les fonctions ou états de consolidation.
  * Pour inclure les informations d’axe analytique dans la consolidation, laissez le champ **Code de consolidation** vide. Toutefois, la consolidation ne fonctionne que si les valeurs d’axe analytique du centre de profit sont les mêmes que celles de la société consolidée.
  * Pour consolider le code section dans le centre de profit doit être consolidé en un autre code section analytique dans la société consolidée renseigner que le champ **Code consolidé**.  
* Ajouter les axes analytiques pertinentes aux comptes généraux pertinents

### <a name="a-nameexcludeaexclude-a-company-from-consolidation" /><a name="exclude"></a>Exclure une société de la consolidation

Si vous ne souhaitez pas inclure un centre de profit dans la consolidation, vous pouvez l’exclure. Pour ce faire, accédez à la fiche centre de profit et désactivez la case à cocher **Consolider**.

### <a name="a-nameincludeainclude-a-partially-owned-company-in-consolidation" /><a name="include"></a>Inclure une société partiellement détenue dans la consolidation

Si vous détenez une société en partie, vous pouvez ajouter un pourcentage de chaque transaction qui correspond au pourcentage de la société que vous détenez. Par exemple, si vous possédez 70 % de la société, la consolidation inclut 70 USD d’une facture de 100 USD. Pour spécifier le pourcentage de la société que vous détenez, accédez à la fiche centre de profit et saisissez le pourcentage dans le champ **% consolidation**.  

## <a name="see-also" />Voir aussi

[Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md)  
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportation de vos données métier vers Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
