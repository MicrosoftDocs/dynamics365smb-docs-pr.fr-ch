---
title: Configurer la validation des transactions intersociétés
description: Créez vos fournisseurs et vos clients intersociétés en tant que partenaires intersociétés, et configurez un plan comptable intersociétés.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 398f5bbbe30730057093f8550cef27a514cbc20a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515552"
---
# <a name="set-up-intercompany-transaction-posting"></a>Configurer la validation des transactions intersociétés

Les comptabilisations intersociétés facilitent la comptabilité de deux sociétés ou plus pour un service financier centralisé et pour les comptables des sociétés partenaires intersociétés. Pour envoyer une transaction (ligne feuille vente) à partir d’une société et créer automatiquement la transaction correspondante (ligne feuille achat) dans la société partenaire, les sociétés concernées doivent s’accorder sur un plan comptable et un ensemble d’axes analytiques communs à utiliser pour les transactions intersociétés. Le plan de compte intersociété peut être, par exemple, une version simplifiée du plan de compte de la société mère. Chaque société associe son plan de compte au plan de compte intersociété partagé, ainsi que ses axes analytiques aux axes analytiques intersociétés.  

Vous devez également configurer un code partenaire intersociété pour chaque société [!INCLUDE [prod_short](includes/prod_short.md)], décidé avec toutes les sociétés, puis l’attribuer à la fiche client et à la fiche fournisseur, respectivement.  

Si vous créez ou recevez des lignes intersociétés contenant des articles, vous pouvez soit utiliser vos propres numéros d’article, soit configurer ceux de votre partenaire pour chaque article concerné, dans le champ **Référence fournisseur** ou **N° article commun** de la fiche article. Vous pouvez également utiliser la fonction **Référence article** : pour mapper vos numéros d’article avec vos descriptions de partenaires Intersociétés des articles, ouvrez la fiche de chaque article, puis choisissez l’action **Références article** afin de configurer les références entre vos descriptions d’article et celles du partenaire Intersociétés. Pour plus d’informations, voir [Utiliser les références article](inventory-how-use-item-cross-refs.md). 

Si vous créez des transactions de vente intersociétés incluant des ressources, vous devez renseigner le champ **N° cte gén achat parten IC** de la fiche ressource de chaque ressource concernée. Il s’agit du numéro du compte général interentreprise sur lequel le montant de cette ressource va être validé dans la société partenaire. Pour plus d’informations, reportez-vous à [Configuration de ressources](projects-how-setup-resources.md). 

> [!NOTE]
> Les transactions d’achat intersociétés qui incluent des ressources, des immobilisations et des frais annexes ne sont pas entièrement prises en charge. Dans la société de votre partenaire intersociété, le champ **Type de ligne** sera vide sur les lignes du document achat qui incluent ces entités. Vous devez mettre à jour manuellement le champ. 

## <a name="to-set-up-a-company-for-intercompany-transactions"></a>Pour configurer une société pour les transactions intersociétés

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Paramètres intersociétés**, renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

  > [!NOTE]
  > La 1re vague de lancement 2022 introduit une nouvelle page **Paramètres intersociétés** afin que vous puissiez également spécifier si cette société doit créer automatiquement des lignes de journal basées sur les validations d’un partenaire intersociété à partir de la page **Feuille comptabilité IC**. Si votre organisation a utilisé [!INCLUDE [prod_short](includes/prod_short.md)] avant cette vague de lancement, vous devez activer la nouvelle expérience dans la page **Gestion des fonctionnalités**. Pour plus d’informations, voir [Accepter automatiquement les transactions pour les feuilles intersociétés](/dynamics365-release-plan/2022wave1/smb/dynamics365-business-central/intercompany-postings-have-auto-accept-transaction-enabled-intercompany-general-journals).

Dans les versions antérieures à la 1re vague de lancement 2022, vous devez remplir trois champs intersociétés sur la page **Informations société** à la place.  

## <a name="to-set-up-intercompany-partners"></a>Pour paramétrer les partenaires intersociétés

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Partenaires intersociété**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Partenaire Intersociétés**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour toutes les autres sociétés faisant partie de ces paramètres intersociétés.

> [!NOTE]
> Dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous ne pouvez pas utiliser les emplacements de fichiers pour transférer des transactions à vos partenaires, car [!INCLUDE[prod_short](includes/prod_short.md)] n’a pas accès à votre réseau local. Par conséquent, si vous choisissez **Emplacement du fichier** dans le champ **Type de transfert**, le champ **Chemin du dossier** n’est pas disponible. Au lieu de cela, le fichier sera téléchargé dans le dossier Téléchargements de votre ordinateur. Vous envoyez ensuite le fichier à une personne de l’entreprise partenaire, par exemple par e-mail. Pour un processus plus direct, nous vous recommandons de choisir **E-mail** plutôt.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Pour paramétrer des fournisseurs et des clients intersociétés
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Autrement, accédez au fournisseur du champ **N° fournisseur** sur la page **Partenaire Intersociétés**.
3. Ouvrez la fiche d’un fournisseur qui est un partenaire Intersociétés. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).
4. Dans le champ **Code Partenaire Intersociétés**, sélectionnez le code partenaire intersociétés approprié.
5. Répétez les étapes 1 à 4 pour les clients.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Pour configurer le plan comptable intersociété
Pour qu’un groupe de sociétés puisse créer des transactions intersociétés, ses membres doivent convenir du plan comptable qui servira de référence commune. Avec vos sociétés partenaires, vous devez décider des numéros de compte à utiliser pour créer des transactions intersociétés. Par exemple, la société mère du groupe génère une version simplifiée de ses propres plans comptables, l’exporte dans un fichier XML qui est distribué à chaque société du groupe.  

Si le plan comptable de votre société définit le plan comptable intersociétés de vos sociétés partenaires, suivez le processus décrit dans [Pour configurer la définition du plan comptable intersociété](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Si votre société est une filiale et que vous recevez un fichier XML contenant le plan comptable commun intersociété, suivez la procédure [Pour importer le plan comptable intersociété](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Pour configurer la définition du plan comptable intersociété
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable intersociété**, puis choisissez le lien associé.
2. Sur la page **Plan comptable intersociétés**, saisissez chaque compte sur une ligne de la page.  
3. Si votre plan comptable intersociété est identique ou semblable à celui que vous utilisez habituellement, vous pouvez renseigner la page automatiquement en choisissant l’action **Copier à partir du plan comptable**. Vous pouvez modifier au besoin les nouvelles lignes.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Pour exporter un plan comptable intersociété
Pour permettre à vos partenaires Intersociétés d’importer la définition du plan comptable, vous devez l’exporter vers un fichier.      
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable intersociété**, puis choisissez le lien associé.
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Exporter**, puis choisissez le bouton **Enregistrer**.
3. Indiquez le nom et l’emplacement d’enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Pour importer le plan comptable intersociétés  
Lorsqu’un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociété peuvent l’importer pour vérifier qu’ils ont les mêmes comptes.  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable intersociété**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Importer**.  
3. Sélectionnez le nom et l’emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

La page **Plan comptable IC** est remplie avec les lignes nouvelles ou modifiées du compte général en fonction du plan comptable intersociété dans le fichier. Les lignes existantes non connexes présentes sur la page ne changent pas.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Pour associer le plan comptable intersociétés au plan comptable de votre société  
Après avoir défini ou importé le plan comptable intersociété que vos partenaires intersociétés et vous avez décidé d’utiliser, vous devez associer chaque compte général intersociété à l’un des comptes généraux de votre société. Sur la page **Plan comptable IC**, indiquez comment les comptes généraux intersociétés des transactions entrantes doivent être convertis en comptes généraux du plan comptable de votre société.

Si les comptes du plan comptable intersociétés possèdent les mêmes numéros que les comptes correspondants dans le plan comptable, vous pouvez les mapper automatiquement.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable intersociété**, puis choisissez le lien associé.  
2. Sélectionnez les lignes à associer automatiquement, puis cliquez sur choisissez l’action **Faire correspondre au compte ayant le même numéro**.  
3. Pour chaque compte général intersociété qui n’a pas été associé automatiquement, renseignez le champ **N° cpte gén pour corres**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Pour configurer des comptes généraux par défaut des partenaires intersociétés  
Lorsque vous créez une ligne vente ou achat intersociété à envoyer comme transaction sortante, vous indiquez un compte du plan comptable intersociété en tant que compte par défaut associé au compte de la société de votre partenaire dans lequel le montant est validé. Sur la page **Plan comptable**, pour les comptes que vous utilisez régulièrement dans des lignes vente ou achat intersociétés sortantes, vous pouvez spécifier un compte général par défaut de partenaire intersociété. Par exemple, pour les comptes client, vous pouvez entrer les comptes fournisseur correspondants du plan comptable intersociété.  

Ensuite, si vous indiquez un compte général dans le champ **N° compte contrepartie** d’une ligne intersociété avec **Partenaire Intersociétés** dans le champ **Type de compte**, le champ **Compte général par défaut des partenaires IC** est renseigné automatiquement.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la ligne d’un compte général utilisé pour les transactions intersociétés, dans le champ **Compte général par défaut de partenaire IC**, entrez le compte général intersociété que votre partenaire utilisera lors de la validation du compte général de la ligne.  
3. Répétez l’étape 2 pour chaque compte que vous entrez souvent dans le champ **N° compte contrepartie** d’une ligne dans la feuille ou le document intersociétés.

## <a name="to-set-up-intercompany-dimensions"></a>Pour configurer des comptabilisations intersociétés

Si vos partenaires intersociétés et vous souhaitez échanger des transactions auxquelles des axes analytiques sont liés, vous devez décider ensemble des axes analytiques que vous allez tous utiliser. Par exemple, la société mère du groupe génère une version simplifiée de son propre ensemble d’axes analytiques, l’exporte dans un fichier XML qui est distribué à chaque société du groupe. Chaque filiale importe ensuite ce fichier XML sur la page **Axes analytiques intersociétés** et associe les axes analytiques intersociétés à ceux figurant dans sa propre page **Axes analytiques**.  

> [!NOTE]
> Chaque entreprise dans [!INCLUDE [prod_short](includes/prod_short.md)] doit mapper les axes analytiques aux axes analytiques intersociétés pour les documents sortants et mapper les axes analytiques intersociétés à leurs propres axes analytiques pour les documents entrants. Cette cartographie permet d’assurer la cohérence entre les entreprises. Pour plus d’informations, consultez la section [Pour mapper les axes analytiques intersociétés aux axes analytiques de votre entreprise](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Si votre société est la société parent et contient l’ensemble de définition des axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure [Définir les axes analytiques intersociétés](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Si votre société est une filiale et que vous recevez un fichier XML contenant les axes analytiques intersociétés qui serviront de référence commune au groupe, suivez la procédure [Importer des axes analytiques intersociétés](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Pour définir les axes analytiques intersociétés
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dimensions intersociété**, puis sélectionnez le lien associé.  
2. Sur la page **Axes analytiques intersociétés**, entrez chaque axe analytique sur une ligne.

    Si vos axes analytiques intersociétés sont identiques ou semblables aux axes analytiques de votre société, vous pouvez renseigner la page automatiquement en utilisant la fonction **Copier à partir des axes analytiques**, puis modifier les lignes ainsi obtenues.  
3. Pour exporter les axes analytiques intersociétés vers un fichier XML afin de le distribuer à vos sociétés partenaires, choisissez l’action **Exporter**.  
4. Indiquez le nom et l’emplacement d’enregistrement du fichier XML, puis cliquez sur le bouton **Enregistrer**.  

### <a name="to-import-the-intercompany-dimensions"></a>Pour importer les axes analytiques intersociétés  
Lorsqu’un fichier existe pour la définition du plan comptable intersociété, les partenaires intersociétés peuvent l’importer pour vérifier qu’ils ont les mêmes axes analytiques.  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dimensions intersociété**, puis sélectionnez le lien associé.  
2. Sur la page **Plan comptable intersociétés**, choisissez l’action **Importer**.  
3. Spécifiez le nom et l’emplacement du fichier XML, puis cliquez sur le bouton **Ouvrir**.  

Les lignes des pages **Axes analytiques intersociétés** et **Sections analytiques intersociétés** sont importées.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Pour associer les axes analytiques intersociétés aux axes de votre société
Après avoir défini ou importé les axes analytiques que vos partenaires intersociétés et vous avez décidé d’utiliser, vous devez associer chaque axe analytique intersociétés à l’un des axes de votre société, et vice versa. Sur la page **Axes analytiques intersociétés**, indiquez comment les axes analytiques intersociétés des *transactions entrantes* doivent être convertis en axes à partir de la liste des axes analytiques de votre société. Sur la page **Axes analytiques**, précisez comment vos axes analytiques doivent être convertis en axes intersociétés dans les *transactions sortantes*.

Si certains axes analytiques intersociété possèdent le même code que les axes analytiques correspondants de la liste des axes analytiques de votre société, vous pouvez demander à l’application d’associer automatiquement ces comptes.  

Dans les étapes suivantes, vous devez d’abord mapper les axes analytiques intersociétés aux axes analytiques des documents entrants sur la page **Axes analytiques intersociétés**. Ensuite, vous mappez les axes analytiques aux axes analytiques intersociétés pour les documents sortants sur la page **Axes analytiques**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dimensions intersociété**, puis sélectionnez le lien associé.
2. Sur la page **Axes analytiques intersociétés**, sélectionnez les lignes à associer automatiquement, puis choisissez l’action **Faire correspondre à l’axe analytique ayant le même code**.
3. Pour chaque axe analytique intersociété qui n’est pas associé automatiquement, renseignez le champ **Code axe à faire correspondre**.

    Vous devrez peut-être ajouter le champ à votre vue. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).
4. Choisissez l’action **Sections analytiques intersociétés**.
5. Sur la page **Sections analytiques intersociétés**, renseignez le champ **Code section à faire correspondre**.

    Continuez à associer les axes analytiques aux axes analytiques intersociétés en effectuant les mêmes étapes.
6. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dimensions**, puis sélectionnez le lien associé.
7. Sur la page **Axes analytiques**, sélectionnez les lignes à associer automatiquement, puis choisissez l’action **Faire correspondre à l’axe IC ayant le même code**.
8. Pour chaque axe analytique intersociété qui n’est pas associé automatiquement, renseignez le champ **Code sect an. axe IC => corres**.
9. Choisissez l’action **Sections analytiques intersociétés**.
10. Sur la page **Sections analytiques**, renseignez le champ **Code section analytique axe IC à faire correspondre**.

## <a name="see-also"></a>Voir aussi

[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]