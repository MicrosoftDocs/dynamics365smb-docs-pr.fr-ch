---
title: Configurer la validation des transactions intersociétés
description: Découvrez comment mettre en place un partenariat interentreprises.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 01/31/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
---
# <a name="set-up-intercompany-transactions"></a><a name="set-up-intercompany-transactions"></a>Configurer les transactions intersociétés

Les partenariats interentreprises facilitent la gestion des processus comptables lorsque deux ou plusieurs filiales d’une entreprise font fréquemment affaire entre elles. Les partenaires peuvent échanger des transactions, telles que des ventes et des achats, et les gérer manuellement ou automatiquement. Par exemple, lorsqu’un partenaire envoie une ligne de journal des ventes à un autre partenaire, une ligne de journal des achats est créée pour le partenaire destinataire.

Le plan de compte intersociété peut être, par exemple, une version simplifiée du plan de compte du partenaire de synchronisation. Chaque partenaire mappe ses comptes sur le plan comptable intersociétés. Chaque partenaire mappe également ses axes analytiques et sections analytiques aux axes analytiques intersociétés.

> [!NOTE]
> Dans la 1ère vague de lancement 2023, nous avons introduit une page améliorée **Configuration intersociétés**. La nouvelle page facilite la mise en place d’un partenariat intersociétés en regroupant toutes les tâches de mise en place sur une seule page. Si vous êtes un nouveau client [!INCLUDE [prod_short](includes/prod_short.md)], vous utilisez déjà la nouvelle expérience. Si vous êtes un client existant, votre administrateur peut activer la fonctionnalité **Accepter automatiquement les transactions feuille comptabilité intersociétés** sur la page **Gestion des fonctionnalités**.
>
> Les tâches décrites dans cet article supposent que le commutateur de fonctionnalité est activé. Si vous avez déjà mis en place un partenariat intersociétés, vous pouvez continuer à l’utiliser.

## <a name="before-you-start"></a><a name="before-you-start"></a>Avant de commencer

Avant de commencer à mettre en place votre partenariat intersociétés, il y a quelques décisions à prendre.

|Décision  |Description  |
|---------|---------|
|Quel plan comptable doit servir de base au plan comptable intersociétés ?     | Toutes les sociétés du partenariat doivent utiliser le même plan comptable intersociétés. Vous pouvez baser votre plan comptable intersociétés sur le plan comptable de l’une des sociétés du partenariat ou créer un plan comptable intersociétés. Vous mappez les comptes à utiliser dans le partenariat dans les deux sens, afin que chaque partenaire envoie et reçoive des transactions dans les bons comptes. Pour en savoir plus sur la configuration du plan comptable intersociétés, consultez [Configurer les plans comptables intersociétés](#set-up-the-intercompany-charts-of-accounts).         |
|Quels axes analytiques doivent être à la base des axes analytiques inter-sociétés ?     | Si vous utilisez des axes analytiques intersociétés, ils doivent être les mêmes pour toutes les sociétés du partenariat. Après avoir spécifié vos axes analytiques intersociétés, mappez leurs sections analytiques. En savoir plus sur le mappage des sections analytiques dans la rubrique [Configurer les axes analytiques intersociétés](#set-up-intercompany-dimensions).        |
|Quels partenaires sont des clients ou des fournisseurs, ou les deux ?     |  Pour en savoir plus sur la configuration de clients et de fournisseurs dans un partenariat intersociétés, consultez [Configurer des partenaires intersociétés en tant que clients et fournisseurs](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Voulez-vous préciser les comptes bancaires à utiliser dans le partenariat ?| Vous pouvez accélérer le processus d’enregistrement des transactions de paiement en spécifiant le compte bancaire à utiliser pour chaque entreprise partenaire. Pour en savoir plus, consultez [Spécifier les comptes bancaires à utiliser pour les partenaires intersociétés](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Comment souhaitez-vous identifier les sociétés du partenariat ?     | Toutes les parties doivent convenir d’un code d’identification de partenaire intersociété unique pour chaque société. Vous attribuerez le code aux fiches client et fournisseur pour identifier les transactions associées. En savoir plus sur les identifiants sur [Créer une série de numéros](ui-create-number-series.md).        |
|Comment souhaitez-vous traiter les numéros d’article ?     | Si les lignes intersociétés contiennent des articles, vous pouvez soit utiliser vos propres numéros d’article, soit configurer ceux de votre partenaire pour chaque article concerné, dans le champ **Référence fournisseur** ou **N° article commun** de la fiche article. Vous pouvez également utiliser l’action **Référence d’article** pour faire correspondre les numéros de vos articles aux descriptions des articles de vos partenaires intersociétés. Pour en savoir plus sur les références d’articles, accédez à [Utiliser les références d’articles](inventory-how-use-item-cross-refs.md).        |
|Des ressources sont-elles impliquées ?     | Si vous créez des transactions de vente intersociétés incluant des ressources, vous devez renseigner le champ **N° cte gén achat parten IC** de la fiche ressource de chaque ressource concernée. Le champ contient le numéro du compte général interentreprise sur lequel le montant de cette ressource va être validé dans la société partenaire. Pour en savoir plus sur la configuration des ressources, consultez [Configurer des ressources](projects-how-setup-resources.md).<br><br>**REMARQUE**<br>Les transactions d’achat intersociétés qui incluent des ressources, des immobilisations et des frais annexes ne sont pas entièrement prises en charge. Dans la société de votre partenaire, le champ **Type de ligne** sera vide sur les lignes du document achat qui incluent ces entités. Vous devez mettre à jour manuellement le champ.        |

## <a name="overview-of-the-steps-to-get-started"></a><a name="overview-of-the-steps-to-get-started"></a>Présentation des étapes pour commencer

Utilisez la page **Configuration intersociétés** pour configurer les composants suivants des transactions intersociétés :

* Les paramètres intersociétés de votre entreprise.
* L’entreprise qui sera le partenaire de synchronisation.
* Le plan comptable inter-sociétés que tous les partenaires utilisent pour échanger des transactions.
* Les mappages entre les comptes dans le plan comptable et le plan comptable intersociétés pour les transactions entrantes et sortantes pour chaque partenaire.
* Les axes analytiques et sections analytiques à utiliser et comment ils sont mappés aux axes analytiques pour chaque partenaire.
* Les entreprises qui sont les partenaires intersociétés.
* Les entreprises qui sont des fournisseurs ou des clients, ou les deux.

## <a name="set-up-a-synchronization-partner"></a><a name="set-up-a-synchronization-partner"></a>Configurer un partenaire de synchronisation

Tous les partenaires doivent utiliser le même plan comptable inter-sociétés et, si nécessaire, les mêmes axes analytiques inter-sociétés. Vous pouvez gagner du temps lors de la configuration du partenariat en utilisant le plan comptable et les axes analytiques de l’un des partenaires comme référence pour le plan comptable et les axes analytiques intersociétés. La société que vous utilisez comme référence est appelée le *partenaire de synchronisation*. En règle générale, le partenaire de synchronisation est le siège social, mais ce n’est pas obligatoire.

Sur la page **Configuration intersociétés**, chaque partenaire spécifie le partenaire de synchronisation dans le champ **Partenaire de synchronisation**. Par la suite, le plan comptable intersociétés et les axes analytiques intersociétés leur sont automatiquement spécifiés, en fonction de la configuration du partenaire de synchronisation. Les partenaires utilisent ensuite les pages **Mappage de plan de comptes intersociétés** et **Mappage de l’axe analytique intersociétés** pour mapper leur plan comptable et axes analytiques au plan comptable et axes analytiques inter-sociétés, et inversement. 

Lorsque vous êtes prêt à synchroniser les données avec votre partenaire de synchronisation, choisissez l’action **Configuration de la synchronisation**.

> [!NOTE]
> Il est important de mapper les comptes et les axes analytiques dans les deux sens. Autrement dit, à la fois vers le plan comptable et les axes analytiques intersociétés, et de ceux-ci vers vos propres comptes et axes analytiques.

## <a name="set-up-the-intercompany-charts-of-accounts"></a><a name="set-up-the-intercompany-charts-of-accounts"></a>Configurer les plans comptables intersociétés

Tous les partenaires doivent utiliser le même plan comptable intersociétés et y associer les comptes de leur propre plan comptable. Si le plan comptable de votre société définit le plan comptable intersociétés de vos sociétés partenaires, suivez les étapes décrites dans cette section.

Si vous utilisez un fichier XML contenant le plan comptable intersociétés, suivez les étapes décrites dans [Importer ou exporter un plan comptable intersociétés](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Choisissez l’action **Plan comptable IC**.
3. Pour ajouter des comptes, procédez comme suit sur la page **Plan comptable intersociétés** :
    * Choisissez **Nouveau**, puis saisissez chaque compte sur une ligne de la page.  
    * Si votre plan comptable intersociété est identique ou semblable à celui que vous utilisez habituellement, vous pouvez renseigner la page automatiquement en choisissant l’action **Copier à partir du plan comptable**. Vous pouvez modifier au besoin les nouvelles lignes.
    * Si vous avez configuré un plan comptable intersociétés pour un partenaire de synchronisation, utilisez l’action **Configuration de la synchronisation** pour copier ces comptes.

    > [!TIP]
    > Si vous copiez le plan comptable inter-sociétés d’un partenaire de synchronisation, vous pouvez utiliser l’action **Configuration de la synchronisation** pour mettre à jour vos comptes intersociétés avec toute modification apportée par le partenaire aux leurs.

La prochaine étape consiste à mapper votre plan comptable aux plans comptables intersociétés. En savoir plus [Mapper le plan comptable intersociétés aux plans comptables de votre société](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### <a name="import-or-export-an-intercompany-chart-of-accounts"></a><a name="import-or-export-an-intercompany-chart-of-accounts"></a>Importer ou exporter un plan comptable intersociété

La société de synchronisation peut partager son plan comptable avec des partenaires en l’exportant dans un fichier. Les partenaires peuvent importer le fichier pour obtenir le plan comptable.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Choisissez l’action **Plan comptable IC**.
3. Sur la page **Plan comptable intersociétés**, choisissez l’action **Importer/Exporter**, puis choisissez **Importer** ou **Exporter**.
4. Choisissez le fichier à importer ou à exporter.  

La page **Plan comptable IC** est remplie avec les lignes nouvelles ou modifiées du compte général en fonction du plan comptable intersociété dans le fichier. Les lignes existantes non connexes présentes sur la page ne changent pas.

## <a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a><a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Mapper le plan comptable intersociétés au plan comptable de votre société

Lorsque vous avez défini ou importé le plan comptable intersociétés, mappez chaque compte intersociétés avec l’un de vos comptes. Sur la page **Plan comptable IC**, indiquez comment les comptes généraux intersociétés des transactions entrantes doivent être convertis en comptes généraux du plan comptable de votre société.

Si les comptes intersociétés et vos comptes ont les mêmes numéros, vous pouvez mapper les comptes automatiquement.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Plan comptable IC**.

    > [!TIP]
    > Pour accéder aux actions de la page, vous devrez peut-être développer la page en vue de mise en page large.

3. Sur la page **Plan comptable intersociétés**, choisissez l’action **Mappage des plans de compte**.
4. Vous pouvez mapper les comptes manuellement ou automatiquement.

    * Pour créer manuellement le mappage, sur les volets **Plan comptable intersociétés** et **Plan comptable général**, choisissez un compte, puis choisissez un compte dans les champs **N° compte général** et **N° IC** .
    * Pour mapper automatiquement les comptes qui ont les mêmes numéros, sélectionnez les lignes que vous souhaitez mapper, choisissez l’action **Faire correspondre au compte ayant le même numéro**, puis choisissez le plan comptable à mettre à jour.

    > [!TIP]
    > Si vous souhaitez mapper plusieurs ou peut-être tous les comptes, choisissez une ligne, choisissez :::image type="icon" source="media/show-more-options-icon.png" border="false":::, puis choisissez **Sélectionnez plus**.

## <a name="set-up-intercompany-dimensions"></a><a name="set-up-intercompany-dimensions"></a>Configurer des axes analytiques intersociétés

Si les partenaires intersociétés échangent des transactions auxquelles des axes analytiques sont liés, vous devez décider ensemble des axes analytiques que vous allez tous utiliser. Par exemple, la société de synchronisation peut créer une version simplifiée de leurs axes analytiques, les exporter dans un fichier XML qui est distribué à chaque partenaire. Chaque partenaire peut importer le fichier XML sur la page **Axes analytiques intersociétés** , puis associez les axes analytiques intersociétés à leurs axes analytiques. En savoir plus [Mapper les axes analytiques intersociétés aux axes analytiques de votre société](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Chaque société doit mettre en correspondance ses axes analytiques avec les axes analytiques intersociétés pour les documents sortants et les documents entrants. Le mappage des comptes dans les deux sens est importante et permet de maintenir la cohérence entre les entreprises.

Si les partenaires utilisent les axes analytiques intersociétés du partenaire de synchronisation, suivez les étapes de cette section. Si vous souhaitez partager en utilisant un fichier XML contenant les axes analytiques intersociétés, suivez les étapes décrites dans [Importer ou exporter les axes analytiques intersociétés](#import-or-export-intercompany-dimensions).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Axes analytiques IC**.
3. Pour ajouter des axes analytiques, procédez comme suis sur la page **Axes analytiques intersociétés** :
    * Choisissez **Nouveau**, puis saisissez chaque axe analytique sur une ligne.  
    * Si vos axes analytiques intersociétés sont identiques ou semblables à ceux que vous utilisez habituellement, vous pouvez renseigner la page automatiquement en choisissant l’action **Copier à partir des axes analytiques**. Vous pouvez modifier au besoin les nouvelles lignes.
    * Si vous avez configuré des axes analytiques intersociétés spécifiées pour un partenaire de synchronisation, utilisez l’action **Configuration de la synchronisation** pour copier ces axes analytiques.

    > [!TIP]
    > Si vous copiez les axes analytiques inter-sociétés d’un partenaire de synchronisation, vous pouvez utiliser l’action **Configuration de la synchronisation** pour mettre à jour vos axes analytiques intersociétés avec toute modification apportée par le partenaire aux leurs.  

### <a name="import-or-export-intercompany-dimensions"></a><a name="import-or-export-intercompany-dimensions"></a>Importer ou exporter les axes analytiques intersociétés

La société de synchronisation peut partager ses axes analytiques avec des partenaires en les exportant dans un fichier. Les partenaires peuvent importer le fichier pour obtenir les axes analytiques.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Choisissez l’action **Axes analytiques IC**.  
3. Sur la page **Axes analytiques intersociétés**, choisissez l’action **Importer/Exporter**, puis choisissez **Importer** ou **Exporter**.
4. Choisissez le fichier à importer ou à exporter.

La prochaine étape consiste à mapper les axes analytiques aux axes analytiques intersociétés. En savoir plus [Mapper les axes analytiques intersociétés aux axes analytiques de votre société](#map-intercompany-dimensions-to-your-companys-dimensions).

### <a name="map-intercompany-dimensions-to-your-companys-dimensions"></a><a name="map-intercompany-dimensions-to-your-companys-dimensions"></a>Mapper les axes analytiques intersociétés aux axes analytiques de votre société

Après avoir spécifié les axes analytiques intersociétés à utiliser, mappez chaque axe analytique intersociété avec l’un des axes analytiques de votre société, et vice versa. Utilisez la page **Mappage des axes analytiques intersociétés** pour spécifier le mappage. Ensuite, répétez le processus pour les sections analytiques.

* Spécifiez comment les axes analytiques intersociétés des transactions entrantes correspondent aux axes analytiques de la liste des axes analytiques de votre entreprise.
* Spécifiez comment vos axes analytiques doivent être convertis en axes intersociétés dans les *transactions sortantes*.

Si certains axes intersociétés possèdent le même code que les axes correspondants de la table Axe analytique de votre société, vous pouvez demander au programme d’associer automatiquement ces axes.  

Dans les étapes suivantes, vous devez d’abord mapper les axes analytiques intersociétés aux axes analytiques des documents entrants sur le volet **Axes analytiques intersociétés**. Ensuite, vous mappez les axes analytiques aux axes analytiques intersociétés pour les documents sortants sur le volet **Axes analytiques de la société actuelle**.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Choisissez l’action **Axes analytiques IC**.
3. Sur la page **Plan comptable intersociétés**, choisissez l’action **Mappage des axes analytiques**.
4. Vous pouvez mapper les axes analytiques manuellement ou automatiquement.

    * Pour créer manuellement le mappage, dans les volets **Axes analytiques intersociétés** et **Axes analytiques de la société actuelle**, choisissez un axe analytique, puis choisissez un axe analytique dans les champs **Code axe analytique** et **Code axe analytique IC**.
    * Pour mapper automatiquement les axes analytiques qui ont le même code, sélectionnez les lignes que vous souhaitez mapper, choisissez l’action **Mapper les axes analytiques avec le même code**, puis choisissez les axes analytiques à mettre à jour. 

    > [!TIP]
    > Si vous souhaitez mapper plusieurs ou peut-être tous les axes analytiques, choisissez une ligne, choisissez :::image type="icon" source="media/show-more-options-icon.png" border="false":::, puis choisissez **Sélectionnez plus**.

5. Choisissez l’action **Mappage des sections analytiques**.
6. Sur la page **Mappage des sections analytiques intersociétés** , les étapes de création du mappage sont similaires à ce que vous venez de faire pour les axes analytiques.

## <a name="set-up-intercompany-general-journal-templates-and-batches"></a><a name="set-up-intercompany-general-journal-templates-and-batches"></a>Configurer les modèles et lots de feuille intersociétés

Vous devez configurer un modèle de feuille général et un lot de feuilles général à utiliser par défaut pour les transactions intersociétés. Le modèle et le lot sont particulièrement importants si vous acceptez automatiquement les transactions intersociétés de vos partenaires. Pour en savoir plus sur l’acceptation automatique des transactions, accédez à [Accepter automatiquement les transactions des partenaires intersociétés](#auto-accept-transactions-from-intercompany-partners).   

* Les feuilles comptabilité permettent de valider dans les comptes généraux et d’autres comptes tels que les comptes bancaires, clients, fournisseurs et d’immobilisations. La validation avec une feuille comptabilité crée toujours des écritures dans les comptes généraux.  Utilisez la page **Feuille comptabilité intersociétés** pour configurer le lot de feuilles comptabilité à utiliser. Les paramètres spécifiques aux transactions intersociétés sont les comptes que vous spécifiez dans les champs **Type de compte IC** et **N° de compte IC**.
* Les modèles feuille vous permettent de travailler dans une fenêtre feuille conçue dans un but spécifique. En effet, les champs contenus dans chaque modèle feuille sont exactement ceux qui sont nécessaires pour une partie de l’application. Utilisez la page **Modèles feuille comptabilité** pour configurer un modèle à utiliser pour les transactions intersociétés.

Pour en savoir plus sur les modèles et les lots de feuilles comptabilité, accédez à [Utiliser des modèles et des lots de feuille](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="set-up-a-company-for-intercompany-transactions"></a><a name="set-up-a-company-for-intercompany-transactions"></a>Configurer une société pour les transactions intersociétés

Les étapes suivantes supposent qu’un partenaire de synchronisation est configuré avec le plan de comptes et les axes analytiques sur lesquels vous allez baser le plan de comptes et les axes analytiques intersociétés. Vous pouvez les configurer vous-même, mais il est généralement plus rapide de démarrer et la maintenance est plus facile si vous utilisez un partenaire de synchronisation. Pour en savoir plus sur le partenaire de synchronisation, accédez à [Configurer un partenaire de synchronisation](#set-up-a-synchronization-partner).

> [!TIP]
> Il est conseillé de remplir les champs du raccourci **Général** de la page **Configuration intersociétés** pour chaque partenaire avant vous ajoutez leurs partenaires. Lorsque vous ajoutez des entreprises partenaires qui se trouvent dans le même client, [!INCLUDE [prod_short](includes/prod_short.md)] obtient leur code IC et le nom de l’entreprise à partir de leur configuration sur le raccourci général. Le champ **Nom de l’entreprise** vérifie que leur code IC est unique.

> [!NOTE]
> Si vous prévoyez d’utiliser un partenaire de synchronisation, laissez le champ **Partenaire de synchronisation** vide lorsque vous configurez cette société pour le partenariat.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Configuration intersociété**, complétez les champs sur le raccourci **Général**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous ne pouvez pas utiliser les emplacements de fichiers pour transférer des transactions à vos partenaires, car [!INCLUDE[prod_short](includes/prod_short.md)] n’a pas accès à votre réseau local. Par conséquent, si vous choisissez **Emplacement du fichier** dans le champ **Type de transfert**, le champ **Chemin du dossier** n’est pas disponible. Au lieu de cela, le fichier sera téléchargé dans le dossier **Téléchargements** de votre ordinateur. Vous envoyez ensuite le fichier à une personne de l’entreprise partenaire, par exemple par e-mail. Pour un processus plus direct, nous vous recommandons de choisir **E-mail** plutôt.

L’étape suivante consiste à configurer les entreprises partenaires.

## <a name="set-up-intercompany-partners"></a><a name="set-up-intercompany-partners"></a>Paramétrer les partenaires intersociétés

Chaque partenaire doit ajouter toutes les autres sociétés du partenariat en tant que partenaire.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Dans le raccourci **Partenaires intersociétés**, choisissez **Ajouter**.
3. Sur la page **Partenaire intersociété**, renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour toutes les sociétés du partenariat.

> [!NOTE]
> Pour la validation intersociétés, lorsque vous avez activé le bouton à bascule **Accepter automatiquement les transactions** sur la page **Fiche partenaire intersociétés** [!INCLUDE[prod_short](includes/prod_short.md)] supprime les messages d’avertissement concernant les factures d’achat dupliquant l’ordre d’achat d’origine. Il est important d’avoir un processus métier pour gérer les doublons. Par exemple, en supprimant ces bons de commande lorsque la facture d’achat est reçue du partenaire intersociétés.

### <a name="set-up-intercompany-partners-as-customers-and-vendors"></a><a name="set-up-intercompany-partners-as-customers-and-vendors"></a>Configurer les paramètres intersociétés en tant que clients et fournisseurs

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres intersociétés**, puis sélectionnez le lien associé.
2. Dans le raccourci **Partenaires intersociétés**, ouvrez la page de carte du partenaire.
3. En fonction de ce que vous voulez faire, choisissez le client ou le partenaire dans les champs **N° client** ou **N° de fournisseur**.

    > [!NOTE]
    > Si le client ou le fournisseur n’a pas été créé, vous pouvez choisir **+Nouveau** dans le menu déroulant pour les configurer. Pour en savoir plus sur la création de clients et de fournisseurs, accédez à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md) et [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Vous pouvez également préciser un client ou un fournisseur en tant que partenaire intersociété en complétant le champ **Code partenaire IC** sur les pages **Fiche client** et **Fiche fournisseur**.

### <a name="set-up-default-intercompany-partner-general-ledger-accounts"></a><a name="set-up-default-intercompany-partner-general-ledger-accounts"></a>Configurer des comptes généraux par défaut des partenaires intersociétés

Lorsque vous créez une ligne vente ou achat intersociété à envoyer comme transaction sortante, vous indiquez un compte du plan comptable intersociété en tant que compte par défaut associé au compte de la société de votre partenaire dans lequel le montant est validé. Sur la page **Fiche compte général**, pour les comptes que vous utilisez régulièrement dans des lignes vente ou achat intersociétés sortantes, vous pouvez spécifier un compte général par défaut de partenaire intersociété. Par exemple, pour les comptes client, vous pouvez entrer les comptes fournisseur correspondants du plan comptable intersociété. Les comptes clients et fournisseurs sont utilisés comme compte de contrepartie pour le partenaire intersociétés lorsque vous validez des transactions dans les journaux généraux intersociétés.  

Ensuite, si vous indiquez un compte général dans le champ **N° compte contrepartie** d’une ligne intersociété avec **Partenaire Intersociétés** dans le champ **Type de compte**, le champ **Compte général par défaut des partenaires IC** est renseigné automatiquement.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Plan comptable**, puis choisissez le lien associé.  
2. Ouvrez la ligne d’un compte général utilisé pour les transactions intersociétés, dans le champ **Compte général par défaut de partenaire IC**, entrez le compte général intersociété que votre partenaire utilisera lors de la validation du compte général de la ligne.
3. Répétez l’étape 2 pour chaque compte que vous entrez souvent dans le champ **N° compte contrepartie** d’une ligne dans la feuille ou le document intersociétés.

### <a name="auto-accept-transactions-from-intercompany-partners"></a><a name="auto-accept-transactions-from-intercompany-partners"></a>Accepter automatiquement les transactions des partenaires intersociétés

Pour accélérer le traitement des transactions intersociétés, vous pouvez spécifier si cette société crée automatiquement des lignes de journal basées sur les publications d’un partenaire intersociétés à partir de la page **Feuille comptabilité IC**. Pour créer automatiquement des transactions entrantes et sortantes, vous devez activer les boutons à bascule suivantes pour chaque partenaire :

* Pour le partenaire de synchronisation, sur la page **Configuration intersociétés**, activez le bouton à bascule **Envoyer auto. des transactions**. Spécifiez ensuite où créer les transactions de journal intersociétés reçues en remplissant les champs **Modèle feuille gén. IC par défaut** et **Nom feuille gén. IC par défaut**.

    > [!TIP]
    > Si le champ **Modèle feuille gén. IC par défaut** est vide, vous devez configurer un modèle feuille comptabilité à utiliser pour vos feuilles comptabilité intersociétés. Pour en savoir plus sur les modèles et les lots de feuilles comptabilité, accédez à [Configurer des modèles et des lots de feuille comptabilité intersociétés](#set-up-intercompany-general-journal-templates-and-batches)    

* Sur la page **Partenaire intersociété**, activez le bouton à bascule **Accepter auto. les transactions**.

Les lignes feuille sont créées pour vous, mais ne sont pas validées.

> [!NOTE]
> Si votre organisation a utilisé des fonctionnalités intersociétés dans [!INCLUDE [prod_short](includes/prod_short.md)] avant la 1e vague de lancement 1 2022, pour accepter automatiquement les transactions, votre administrateur doit activer la fonctionnalité **Accepter automatiquement les transactions feuille comptabilité intersociétés** sur la page **Gestion des fonctionnalités**.

### <a name="specify-the-bank-accounts-to-use-for-intercompany-partners"></a><a name="specify-the-bank-accounts-to-use-for-intercompany-partners"></a>Spécifier les comptes bancaires à utiliser pour les partenaires intersociétés

Pour faciliter les paiements rapides, spécifiez un ou plusieurs comptes bancaires à utiliser pour les partenaires intersociétés. Lorsqu’un partenaire utilise une feuille comptabilité intersociétés pour effectuer un paiement, il peut spécifier le compte bancaire sur la ligne. Le compte bancaire est utilisé comme compte d’équilibre dans la société réceptrice, ce qui minimise la nécessité de saisir manuellement les transactions.

* Pour spécifier le compte bancaire à utiliser, sur la page **Partenaires intersociétés**, choisissez l’action **Comptes bancaires**. Sur la **Fiche de compte bancaire intersociétés**, entrez les informations du compte.

## <a name="troubleshoot-your-intercompany-setup"></a><a name="troubleshoot-your-intercompany-setup"></a>Dépanner votre configuration intersociété

Sur la page **Configuration intersociété**, le volet **Diagnostics de configuration intersociétés** contient des vignettes qui indiquent si vous avez configuré tous les composants nécessaires pour échanger des transactions intersociétés. Les vignettes sont également disponibles sur le tableau de bord Business Manager. Choisissez les vignettes pour découvrir ce qui manque. Pour un aperçu des composants requis, rendez-vous sur [Présentation des étapes pour commencer](#overview-of-the-steps-to-get-started).

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
