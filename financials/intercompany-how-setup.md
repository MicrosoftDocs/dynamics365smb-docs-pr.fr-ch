---
title: "Configurer la validation des transactions intersociétés | Microsoft Docs"
description: "Créez vos fournisseurs et vos clients intersociétés en tant que partenaires intersociétés, et configurez un plan comptable intersociétés."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7a23f0ba28ab4c7bc9e028375246ea2e57d32764
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-intercompany"></a>Configuration des fonctionnalités intersociétés
Pour envoyer une transaction (ligne feuille vente) à partir d'une société et créer automatiquement la transaction correspondante (ligne feuille achat) dans la société partenaire, les sociétés concernées doivent s'accorder sur un plan de compte et un ensemble d'axes analytiques communs à utiliser pour les transactions intersociétés. Le plan de compte intersociété peut être, par exemple, une version simplifiée du plan de compte de la société mère. Chaque société associe son plan de compte au plan de compte intersociété partagé, ainsi que ses axes analytiques aux axes analytiques intersociétés.  

Vous devez également configurer un code partenaire Intersociétés pour chaque société partenaire, ce qui est convenu par toutes les sociétés, puis les affecter respectivement aux fichiers client et fournisseur en renseignant le champ **Code Partenaire Intersociétés**.  

Si vous créez ou recevez des lignes intersociétés contenant des articles, vous pouvez soit utiliser vos propres numéros d'article, soit configurer ceux de votre partenaire pour chaque article concerné, dans le champ **Référence fournisseur** ou **N° article commun** de la fiche article. Vous pouvez également utiliser la fonction **Référence externe article** : pour mapper vos numéros d'article avec vos descriptions de partenaires Intersociétés des articles, ouvrez la fiche de chaque article, puis choisissez l'action **Références externes** afin de configurer les références externes entre vos descriptions d'article et celles du partenaire Intersociétés.  

Si vous créez des transactions de vente intersociétés incluant des ressources, vous devez renseigner le champ **N° cte gén achat parten IC** de la fiche ressource de chaque ressource concernée. Il s'agit du numéro du compte général interentreprise sur lequel le montant de cette ressource va être validé dans la société partenaire. Pour plus d'informations, voir .  

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Pour configurer des sociétés pour les transactions intersociétés
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Informations société**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Informations société**, renseignez les champs **Code Partenaire Intersociétés**, **Type de boîte de réception Intersociétés** et **Détails boîte de réception intersociétés**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Pour paramétrer les partenaires intersociétés
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Partenaires Intersociétés**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Dans la fenêtre **Partenaire Intersociétés**, renseignez les champs comme nécessaire.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Pour paramétrer des fournisseurs et des clients intersociétés
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Autrement, accédez au fournisseur du champ **N° fournisseur** dans la fenêtre **Partenaire Intersociétés**.
3. Ouvrez la fiche d'un fournisseur qui est un partenaire Intersociétés. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).
4. Dans le champ **Code Partenaire Intersociétés**, sélectionnez le code partenaire intersociétés approprié.
5. Répétez les étapes 1 à 4 pour les clients.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Pour configurer le plan comptable intersociété
Pour qu'un groupe de sociétés puisse créer des transactions intersociétés, ses membres doivent convenir du plan comptable qui servira de référence commune. Avec vos sociétés partenaires, vous devez décider des numéros de compte à utiliser pour créer des transactions intersociétés. Par exemple, la société mère du groupe génère une version simplifiée de son propre plan comptable, l'exporte de sa base de données vers un fichier XML et la distribue à chaque société du groupe.  

Si votre société est la société parent et contient le plan comptable intersociétés qui servira de référence commune au groupe, suivez la procédure « Configurer le plan comptable intersociétés ».  

Si votre société est une filiale et que vous recevez un fichier XML contenant le tableau de compte commun intersociétés, suivez la procédure « Pour importer le plan comptable intersociété ».  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Pour configurer la définition du plan comptable intersociété
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable IC**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Plan comptable IC**, saisissez chaque compte sur une ligne de la fenêtre.  
3. Si votre plan comptable intersociété est identique ou semblable à celui que vous utilisez habituellement, vous pouvez renseigner la fenêtre automatiquement en choisissant l'action **Copier à partir du plan comptable**. Vous pouvez modifier au besoin les nouvelles lignes.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Pour exporter un plan comptable intersociété
Pour permettre à vos partenaires Intersociétés d'importer la définition du plan comptable, vous devez l'exporter vers un fichier.      
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable IC**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Plan comptable IC**, choisissez l'action **Exporter**, puis choisissez le bouton **Enregistrer**.
3. Indiquez le nom et l'emplacement d'enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Pour importer le plan comptable intersociétés  
Lorsqu'un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociétés peuvent l'importer pour vérifier qu'ils ont les mêmes comptes.  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable IC**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Plan comptable IC**, choisissez l'action **Importer**.  
3. Sélectionnez le nom et l'emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

La fenêtre **Plan comptable IC** est rempli avec les lignes nouvelles ou modifiées du compte général en fonction du plan comptable intersociété dans le fichier. Les lignes existantes non connexes présentes dans la fenêtre ne changent pas.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Pour associer le plan comptable intersociétés au plan comptable de votre société  
Après avoir défini ou importé le plan comptable intersociété que vos partenaires intersociétés et vous avez décidé d'utiliser, vous devez associer chaque compte général intersociété à l'un des comptes généraux de votre société. Dans la fenêtre **Plan comptable IC**, indiquez comment les comptes généraux intersociétés des transactions entrantes doivent être convertis en comptes généraux à partir du plan comptable de votre société.

Si les comptes du plan comptable intersociétés possèdent les mêmes numéros que les comptes correspondants dans le plan comptable, vous pouvez les mapper automatiquement.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable IC**, puis sélectionnez le lien connexe.  
2. Sélectionnez les lignes à associer automatiquement, puis cliquez sur choisissez l'action **Faire correspondre au compte ayant le même numéro**.  
3. Pour chaque compte général intersociété qui n'a pas été associé automatiquement, renseignez le champ **N° cpte gén pour corres**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Pour configurer des comptes généraux par défaut des partenaires intersociétés  
Lorsque vous créez une ligne vente ou achat intersociété à envoyer comme transaction sortante, vous indiquez un compte du plan comptable intersociété en tant que compte par défaut associé au compte de la société de votre partenaire dans lequel le montant est validé. Dans la fenêtre **Plan comptable**, pour les comptes que vous utilisez souvent dans des lignes vente ou achat intersociétés sortantes, vous pouvez spécifier un compte général par défaut de partenaire Intersociétés. Par exemple, pour les comptes client, vous pouvez entrer les comptes fournisseur correspondants du plan comptable intersociété.  

Ensuite, si vous indiquez un compte général dans le champ **N° compte contrepartie** d'une ligne intersociété avec **Partenaire Intersociétés** dans le champ **Type de compte**, le champ **Compte général par défaut des partenaires IC** est renseigné automatiquement.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.  
2. Sur la ligne d'un compte général utilisé pour les transactions intersociétés, dans le champ **Compte général par défaut de partenaire IC**, entrez le compte général intersociété que votre partenaire utilisera lors de la validation du compte général de la ligne.  
3. Répétez l'étape 3 pour chaque compte que vous entrez souvent dans le champ **N° compte contrepartie** d'une ligne dans la feuille ou le document intersociétés.

## <a name="to-set-up-intercompany-dimensions"></a>Pour configurer des comptabilisations intersociétés
Si vos partenaires intersociétés et vous souhaitez pouvoir échanger des transactions auxquelles des axes analytiques sont liés, vous devrez vous entendre sur les axes analytiques que vous allez tous utiliser. Par exemple, la société mère du groupe génère une version simplifiée de ses propres axes analytiques, l'exporte dans un fichier XML et la distribue à chaque société du groupe. Chaque filiale importe ensuite ce fichier XML dans la fenêtre **Axes analytiques intersociétés** et associe les axes analytiques intersociétés à ceux figurant dans sa propre fenêtre **Axes analytiques**.  

Si votre société est la société parent et contient l'ensemble de définition des axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure « Définir les axes analytiques intersociétés ».

Si votre société est une filiale et que vous recevez un fichier XML contenant les axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure « Importer des axes analytiques intersociétés ».

### <a name="to-define-the-intercompany-dimensions"></a>Pour définir les axes analytiques intersociétés
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Axes analytiques intersociétés**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Axes analytiques intersociétés**, entrez chaque axe analytique sur une ligne.

    Si vos axes analytiques intersociétés sont identiques ou semblables aux axes analytiques de votre société, vous pouvez renseigner la fenêtre automatiquement en utilisant la fonction **Copier à partir des axes analytiques**, puis modifier les lignes ainsi obtenues.  
3. Pour exporter les axes analytiques intersociétés vers un fichier XML afin de le distribuer à vos sociétés partenaires, choisissez l'action **Exporter**.  
4. Indiquez le nom et l'emplacement d'enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-dimensions"></a>Pour importer les axes analytiques intersociétés  
Lorsqu'un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociétés peuvent l'importer pour vérifier qu'ils ont les mêmes axes analytiques.  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Axes analytiques intersociétés**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Plan comptable IC**, choisissez l'action **Importer**.  
3. Spécifiez le nom et l'emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

Les lignes des fenêtres **Axes analytiques intersociétés** et **Sections analytiques intersociétés** sont importées.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Pour associer les axes analytiques intersociétés aux axes de votre société
Après avoir défini ou importé les axes analytiques que vos partenaires intersociétés et vous avez décidé d'utiliser, vous devez associer chaque axe analytique intersociétés à l'un des axes de votre société, et vice versa. Dans la fenêtre **Axes analytiques intersociétés**, indiquez comment les axes analytiques intersociétés des transactions entrantes doivent être convertis en axes à partir de la liste des axes analytiques de votre société. Dans la fenêtre **Axes analytiques**, précisez comment vos axes analytiques doivent être convertis en axes intersociétés dans les transactions sortantes.

Si certains axes analytiques intersociété possèdent le même code que les axes analytiques correspondants de la liste des axes analytiques de votre société, vous pouvez demander au programme d'associer automatiquement ces comptes.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Axes analytiques intersociétés**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Axes analytiques intersociétés**, sélectionnez les lignes à associer automatiquement, puis choisissez l'action **Faire correspondre à l'axe analytique**.
3. Pour chaque axe intersociétés qui n'est pas associé automatiquement, renseignez le champ **Code axe à faire correspondre**.
4. Choisissez l'action **Sections analytiques intersociétés**.
5. Dans la fenêtre **Sections analytiques intersociétés**, renseignez le champ **Code section à faire correspondre de chaque section analytique IC**.

    Continuez à associer les axes analytiques aux axes analytiques intersociétés en effectuant les mêmes étapes.
6. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Axes analytiques**, puis sélectionnez le lien connexe.
7. Dans la fenêtre **Axes analytiques intersociétés**, sélectionnez les lignes à associer automatiquement, puis choisissez l'action **Faire correspondre à l'axe IC ayant le même code**.
8. Pour chaque axe intersociétés qui n'est pas associé automatiquement, renseignez le champ **Code section analytique axe IC à faire correspondre**.
9. Choisissez l'action **Sections analytiques intersociétés**.
10. Dans la fenêtre **Sections analytiques intersociétés**, renseignez le champ **Code section analytique axe IC à faire correspondre**.

## <a name="see-also"></a>Voir aussi
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

