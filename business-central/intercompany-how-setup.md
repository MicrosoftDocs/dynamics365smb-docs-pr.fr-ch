---
title: Configurer la validation des transactions intersociétés | Microsoft Docs
description: Créez vos fournisseurs et vos clients intersociétés en tant que partenaires intersociétés, et configurez un plan comptable intersociétés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c323aee8139912e103b09066f2f6a7a25e2832c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786213"
---
# <a name="set-up-intercompany"></a>Configuration des fonctionnalités intersociétés

Pour envoyer une transaction (ligne feuille vente) à partir d’une société et créer automatiquement la transaction correspondante (ligne feuille achat) dans la société partenaire, les sociétés concernées doivent s’accorder sur un plan de compte et un ensemble d’axes analytiques communs à utiliser pour les transactions intersociétés. Le plan de compte intersociété peut être, par exemple, une version simplifiée du plan de compte de la société mère. Chaque société associe son plan de compte au plan de compte intersociété partagé, ainsi que ses axes analytiques aux axes analytiques intersociétés.  

Vous devez également configurer un code partenaire Intersociétés pour chaque société partenaire, ce qui est convenu par toutes les sociétés, puis les affecter respectivement aux fichiers client et fournisseur en renseignant le champ **Code Partenaire Intersociétés**.  

Si vous créez ou recevez des lignes intersociétés contenant des articles, vous pouvez soit utiliser vos propres numéros d’article, soit configurer ceux de votre partenaire pour chaque article concerné, dans le champ **Référence fournisseur** ou **N° article commun** de la fiche article. Vous pouvez également utiliser la fonction **Référence externe article** : pour mapper vos numéros d’article avec vos descriptions de partenaires Intersociétés des articles, ouvrez la fiche de chaque article, puis choisissez l’action **Références externes** afin de configurer les références externes entre vos descriptions d’article et celles du partenaire Intersociétés. Pour plus d’informations, voir [Utiliser les références externes article](inventory-how-use-item-cross-refs.md). 

Si vous créez des transactions de vente intersociétés incluant des ressources, vous devez renseigner le champ **N° cte gén achat parten IC** de la fiche ressource de chaque ressource concernée. Il s’agit du numéro du compte général interentreprise sur lequel le montant de cette ressource va être validé dans la société partenaire. Pour plus d’informations, reportez-vous à [Configuration de ressources](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Pour configurer des sociétés pour les transactions intersociétés
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Informations société**, puis sélectionnez le lien associé.  
2. Sur la page **Informations société**, renseignez les champs **Code Partenaire Intersociétés**, **Type de boîte de réception Intersociétés** et **Détails boîte de réception intersociétés**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Pour paramétrer les partenaires intersociétés
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Partenaires intersociétés**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Partenaire Intersociétés**, renseignez les champs comme nécessaire.

> [!NOTE]
> Dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous ne pouvez pas utiliser les emplacements de fichiers pour transférer des transactions à vos partenaires, car [!INCLUDE[prod_short](includes/prod_short.md)] n’a pas accès à votre réseau local. Par conséquent, si vous choisissez **Emplacement du fichier** dans le champ **Type de transfert**, le champ **Chemin du dossier** n’est pas disponible. Au lieu de cela, le fichier sera téléchargé dans le dossier Téléchargements de votre ordinateur. Vous envoyez ensuite le fichier à une personne de l’entreprise partenaire, par exemple par e-mail. Pour un processus plus direct, nous vous recommandons de choisir **E-mail** plutôt.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Pour paramétrer des fournisseurs et des clients intersociétés
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis sélectionnez le lien associé.
2. Autrement, accédez au fournisseur du champ **N° fournisseur** sur la page **Partenaire Intersociétés**.
3. Ouvrez la fiche d’un fournisseur qui est un partenaire Intersociétés. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).
4. Dans le champ **Code Partenaire Intersociétés**, sélectionnez le code partenaire intersociétés approprié.
5. Répétez les étapes 1 à 4 pour les clients.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Pour configurer le plan comptable intersociété
Pour qu’un groupe de sociétés puisse créer des transactions intersociétés, ses membres doivent convenir du plan comptable qui servira de référence commune. Avec vos sociétés partenaires, vous devez décider des numéros de compte à utiliser pour créer des transactions intersociétés. Par exemple, la société mère du groupe génère une version simplifiée de son propre plan comptable, l’exporte de sa base de données vers un fichier XML et la distribue à chaque société du groupe.  

Si votre société est la société parent et contient le plan comptable intersociétés qui servira de référence commune au groupe, suivez la procédure [Configurer le plan comptable intersociétés de définition](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Si votre société est une filiale et que vous recevez un fichier XML contenant le tableau de compte commun intersociétés, suivez la procédure [Pour importer le plan comptable intersociété](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Pour configurer la définition du plan comptable intersociété
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable intersociété**, puis sélectionnez le lien associé.
2. Sur la page **Plan comptable intersociétés**, saisissez chaque compte sur une ligne de la page.  
3. Si votre plan comptable intersociété est identique ou semblable à celui que vous utilisez habituellement, vous pouvez renseigner la page automatiquement en choisissant l’action **Copier à partir du plan comptable**. Vous pouvez modifier au besoin les nouvelles lignes.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Pour exporter un plan comptable intersociété
Pour permettre à vos partenaires Intersociétés d’importer la définition du plan comptable, vous devez l’exporter vers un fichier.      
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable intersociété**, puis sélectionnez le lien associé.
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Exporter**, puis choisissez le bouton **Enregistrer**.
3. Indiquez le nom et l’emplacement d’enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Pour importer le plan comptable intersociétés  
Lorsqu’un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociétés peuvent l’importer pour vérifier qu’ils ont les mêmes comptes.  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable intersociété**, puis sélectionnez le lien associé.  
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Importer**.  
3. Sélectionnez le nom et l’emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

La page **Plan comptable IC** est remplie avec les lignes nouvelles ou modifiées du compte général en fonction du plan comptable intersociété dans le fichier. Les lignes existantes non connexes présentes sur la page ne changent pas.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Pour associer le plan comptable intersociétés au plan comptable de votre société  
Après avoir défini ou importé le plan comptable intersociété que vos partenaires intersociétés et vous avez décidé d’utiliser, vous devez associer chaque compte général intersociété à l’un des comptes généraux de votre société. Sur la page **Plan comptable IC**, indiquez comment les comptes généraux intersociétés des transactions entrantes doivent être convertis en comptes généraux du plan comptable de votre société.

Si les comptes du plan comptable intersociétés possèdent les mêmes numéros que les comptes correspondants dans le plan comptable, vous pouvez les mapper automatiquement.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable intersociété**, puis sélectionnez le lien associé.  
2. Sélectionnez les lignes à associer automatiquement, puis cliquez sur choisissez l’action **Faire correspondre au compte ayant le même numéro**.  
3. Pour chaque compte général intersociété qui n’a pas été associé automatiquement, renseignez le champ **N° cpte gén pour corres**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Pour configurer des comptes généraux par défaut des partenaires intersociétés  
Lorsque vous créez une ligne vente ou achat intersociété à envoyer comme transaction sortante, vous indiquez un compte du plan comptable intersociété en tant que compte par défaut associé au compte de la société de votre partenaire dans lequel le montant est validé. Sur la page **Plan comptable**, pour les comptes que vous utilisez souvent dans des lignes vente ou achat intersociétés sortantes, vous pouvez spécifier un compte général par défaut de partenaire Intersociétés. Par exemple, pour les comptes client, vous pouvez entrer les comptes fournisseur correspondants du plan comptable intersociété.  

Ensuite, si vous indiquez un compte général dans le champ **N° compte contrepartie** d’une ligne intersociété avec **Partenaire Intersociétés** dans le champ **Type de compte**, le champ **Compte général par défaut des partenaires IC** est renseigné automatiquement.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.  
2. Sur la ligne d’un compte général utilisé pour les transactions intersociétés, dans le champ **Compte général par défaut de partenaire IC**, entrez le compte général intersociété que votre partenaire utilisera lors de la validation du compte général de la ligne.  
3. Répétez l’étape 2 pour chaque compte que vous entrez souvent dans le champ **N° compte contrepartie** d’une ligne dans la feuille ou le document intersociétés.

## <a name="to-set-up-intercompany-dimensions"></a>Pour configurer des comptabilisations intersociétés

Si vos partenaires intersociétés et vous souhaitez pouvoir échanger des transactions auxquelles des axes analytiques sont liés, vous devrez vous entendre sur les axes analytiques que vous allez tous utiliser. Par exemple, la société mère du groupe génère une version simplifiée de ses propres axes analytiques, l’exporte dans un fichier XML et la distribue à chaque société du groupe. Chaque filiale importe ensuite ce fichier XML sur la page **Axes analytiques intersociétés** et associe les axes analytiques intersociétés à ceux figurant dans sa propre page **Axes analytiques**.  

> [!NOTE]
> Chaque entreprise dans [!INCLUDE [prod_short](includes/prod_short.md)] doit mapper les axes analytiques aux axes analytiques intersociétés pour les documents sortants et mapper les axes analytiques intersociétés à leurs propres axes analytiques pour les documents entrants. Cette cartographie permet d’assurer la cohérence entre les entreprises. Pour plus d’informations, consultez la section [Pour mapper les axes analytiques intersociétés aux axes analytiques de votre entreprise](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Si votre société est la société parent et contient l’ensemble de définition des axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure [Définir les axes analytiques intersociétés](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Si votre société est une filiale et que vous recevez un fichier XML contenant les axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure [Importer des axes analytiques intersociétés](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Pour définir les axes analytiques intersociétés
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Axes analytiques intersociété**, puis sélectionnez le lien associé.  
2. Sur la page **Axes analytiques intersociétés**, entrez chaque axe analytique sur une ligne.

    Si vos axes analytiques intersociétés sont identiques ou semblables aux axes analytiques de votre société, vous pouvez renseigner la page automatiquement en utilisant la fonction **Copier à partir des axes analytiques**, puis modifier les lignes ainsi obtenues.  
3. Pour exporter les axes analytiques intersociétés vers un fichier XML afin de le distribuer à vos sociétés partenaires, choisissez l’action **Exporter**.  
4. Indiquez le nom et l’emplacement d’enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-dimensions"></a>Pour importer les axes analytiques intersociétés  
Lorsqu’un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociétés peuvent l’importer pour vérifier qu’ils ont les mêmes axes analytiques.  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Axes analytiques intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Importer**.  
3. Spécifiez le nom et l’emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

Les lignes des pages **Axes analytiques intersociétés** et **Sections analytiques intersociétés** sont importées.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Pour associer les axes analytiques intersociétés aux axes de votre société
Après avoir défini ou importé les axes analytiques que vos partenaires intersociétés et vous avez décidé d’utiliser, vous devez associer chaque axe analytique intersociétés à l’un des axes de votre société, et vice versa. Sur la page **Axes analytiques intersociétés**, indiquez comment les axes analytiques intersociétés des *transactions entrantes* doivent être convertis en axes à partir de la liste des axes analytiques de votre société. Sur la page **Axes analytiques**, précisez comment vos axes analytiques doivent être convertis en axes intersociétés dans les *transactions sortantes*.

Si certains axes analytiques intersociété possèdent le même code que les axes analytiques correspondants de la liste des axes analytiques de votre société, vous pouvez demander à l’application d’associer automatiquement ces comptes.  

Dans les étapes suivantes, vous devez d’abord mapper les axes analytiques intersociétés aux axes analytiques des documents entrants sur la page **Axes analytiques intersociétés**. Ensuite, vous mappez les axes analytiques aux axes analytiques intersociétés pour les documents sortants sur la page **Axes analytiques**.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Axes analytiques intersociétés**, puis sélectionnez le lien associé.
2. Sur la page **Axes analytiques intersociétés**, sélectionnez les lignes à associer automatiquement, puis choisissez l’action **Faire correspondre à l’axe analytique ayant le même code**.
3. Pour chaque axe intersociétés qui n’est pas associé automatiquement, renseignez le champ **Code axe à faire correspondre**.

    Vous devrez peut-être ajouter le champ à votre vue. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).
4. Choisissez l’action **Sections analytiques intersociétés**.
5. Sur la page **Sections analytiques intersociétés**, renseignez le champ **Code section à faire correspondre**.

    Continuez à associer les axes analytiques aux axes analytiques intersociétés en effectuant les mêmes étapes.
6. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Axes analytiques**, puis sélectionnez le lien associé.
7. Sur la page **Axes analytiques**, sélectionnez les lignes à associer automatiquement, puis choisissez l’action **Faire correspondre à l’axe IC ayant le même code**.
8. Pour chaque axe intersociétés qui n’est pas associé automatiquement, renseignez le champ **Code section analytique axe IC à faire correspondre**.
9. Choisissez l’action **Sections analytiques intersociétés**.
10. Sur la page **Sections analytiques**, renseignez le champ **Code section analytique axe IC à faire correspondre**.

## <a name="see-also"></a>Voir aussi

[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]