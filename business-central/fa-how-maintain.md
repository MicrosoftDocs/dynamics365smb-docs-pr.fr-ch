---
title: Mettre à jour des immobilisations
description: Vous conservez un registre de maintenance de toutes les réparations et services sur une immobilisation pour préserver la valeur de cette immobilisation.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets"></a><a name="maintain-fixed-assets"></a>Mettre à jour des immobilisations

Les frais de maintenance sont des coûts périodiques de routine engagés pour préserver la valeur des immobilisations. Contrairement aux améliorations de capital, ils n’augmentent pas les valeurs.

Vous pouvez enregistrer et mettre à jour un fichier sur la maintenance et l’entretien des immobilisations afin d’accéder facilement aux enregistrements de maintenance complets des immobilisations. Chaque fois qu’une immobilisation est envoyée en réparation, vous enregistrez toutes les informations importantes, par exemple la date de réparation, le numéro du fournisseur et le numéro de téléphone de l’intervenant. La saisie de la maintenance est effectuée pour chaque immobilisation à partir de la fiche immobilisation.

L’actualisation permet d’ajuster des valeurs en fonction de modifications générales de niveau de prix. Le traitement par lots **Réévaluer immobilisations** permet de recalculer les coûts de maintenance.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a><a name="to-record-maintenance-work-on-a-fixed-asset"></a>Pour enregistrer les travaux de maintenance sur une immobilisation

Vous pouvez enregistrer chaque tâche de maintenance, telle qu’une visite de service, effectuée pour une immobilisation donnée. Pour cela, utilisez la page **Saisie de la maintenance**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.  
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez enregistrer la maintenance, puis sélectionnez l’action **Saisie de la maintenance**.
3. Sur la page **Saisie de la maintenance**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Pour valider les coûts de maintenance à partir d’une feuille comptabilisation immobilisation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Liste de la loi d’amortissement**, puis choisissez le lien associé.  
2. Sélectionnez la loi d’amortissement qui est attribuée à une immobilisation, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche loi d’amortissement**, veillez à ce que la case **Maintenance** ne soit pas cochée. Cela garantit que les coûts de maintenance ne sont pas validés en comptabilité.
4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilisation immobilisation**, puis choisissez le lien associé.  
5. Créez une feuille comptable initiale et complétez les champs, le cas échéant.
6. Dans le champ **Type compta. immo**, sélectionnez **Maintenance**.
7. Sélectionnez l’action **Insérer contrepartie immo.**. Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de la maintenance.

    > [!NOTE]  
    >   L’étape 7 ne fonctionne que si vous avez configuré ce qui suit : sur la page **Fiche groupe compta. immo.** du groupe de validation de l’immobilisation, le champ **Compte maintenance** contient le compte débit général et le champ **Compte contrepartie maintenance** contient le compte général dans lequel vous souhaitez valider les écritures contrepartie pour réévaluation. Pour plus d’informations, reportez vous à [Pour configurer des groupes de validation immobilisation](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Sélectionnez l’action **Valider**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a><a name="to-follow-up-on-fixed-assets-service-visits"></a>Pour effectuer le suivi des visites d’entretien des immobilisations

Vous pouvez imprimer l’état **Maintenance - Service suivant** afin de connaître les immobilisations pour lesquelles vous avez programmé une visite de service. Vous pouvez également utiliser cet état lorsque vous mettez à jour le champ **Date prochain service** des fiches immobilisation.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Maintenance - Service suivant**, puis choisissez le lien associé.  
2. Renseignez les champs **Date début** et **Date fin**.  
3. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="to-monitor-maintenance-costs"></a><a name="to-monitor-maintenance-costs"></a>Pour surveiller les coûts de maintenance

Vous pouvez visualiser les coûts de maintenance lorsque vous consultez les statistiques d’une immobilisation.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez afficher les coûts de maintenance, puis sélectionnez l’action **Lois d’amortissement**.
3. Sur la page **Lois d’amortissement immobilisation**, sélectionnez la loi d’amortissement immobilisation pertinente, puis sélectionnez l’action **Statistiques**.
4. Sur la page **Statistiques immobilisation**, sélectionnez le champ **Maintenance**.

La page **Écritures comptables maintenance** s’ouvre, affichant les écritures qui constituent le montant dans le champ **Maintenance**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Pour afficher ou imprimer les coûts de maintenance pour plusieurs immobilisations

Dans l’état **Maintenance - Analyse**, vous pouvez choisir de visualiser la maintenance sur un, deux ou trois codes maintenance pour une date ou une période donnée. Vous pouvez également visualiser soit le total de toutes les immobilisations sélectionnées, soit celui de chaque immobilisation.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Maintenance - Analyse**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins.
3. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="to-view-maintenance-ledger-entries"></a><a name="to-view-maintenance-ledger-entries"></a>Pour visualiser des écritures comptables maintenance

Vous pouvez également étudier les coûts de maintenance en visualisant les écritures comptables.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez afficher les écritures comptables, puis sélectionnez l’action **Lois d’amortissement**.
3. Sur la page **Écritures comptables maintenance**, sélectionnez la loi d’amortissement immobilisation pertinente, puis l’action **Statistiques**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Pour afficher ou imprimer les écritures comptables de maintenance pour plusieurs immobilisations

Dans l’état **Maintenance - Détails**, vous pouvez afficher ou imprimer les écritures comptables de maintenance pour un ou plusieurs actifs.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Maintenance - Détails**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins.
3. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/manage-fixed-assets-maintenance-insurances/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d’immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
