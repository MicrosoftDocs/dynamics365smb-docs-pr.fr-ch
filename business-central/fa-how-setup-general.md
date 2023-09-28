---
title: Définir des informations générales relatives aux immobilisations
description: 'Avant d’utiliser des immobilisations, vous devez paramétrer des comptes généraux par défaut, des groupes de validation, des clés de ventilation, des feuilles et des modèles feuille, ainsi que les codes classe.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-general-fixed-assets-information"></a>Configurer des informations générales pour les immobilisations

Avant de pouvoir gérer les immobilisations, vous devez configurer les comptes généraux par défaut, les clés de ventilation, les modèles feuille et les lots pour la validation et le reclassement des immobilisations. Vous pouvez classer les immobilisations par catégorie, telles que Corporelles et Incorporelles.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Pour configurer des valeurs générales par défaut pour les immobilisations

Vous définissez le comportement général ou la fonctionnalité immobilisation et configurez les souches de numéros document sur la page **Paramètres immobilisations**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres immobilisations**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Pour configurer des groupes de validation immobilisation

Les groupes comptabilisation permettent de définir des groupes d’immobilisations. Les écritures de ces groupes comptabilisation sont validées dans les mêmes comptes généraux.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. immo.**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Fiche groupe compta. immo.**, renseignez les champs, le cas échéant.

    > [!NOTE]  
    >   Pour veiller à ce que les comptes de contrepartie pour différentes validations d’immobilisation soient automatiquement insérés lorsque vous sélectionnez l’action **Insérer contrepartie immo.** sur les lignes feuille, procédez comme suit, selon la validation de réévaluation.
4. Sur le raccourci **Compte contrepartie**, dans le champ **Contrep. réévaluation**, sélectionnez le compte général dans lequel vous souhaitez valider les écritures contrepartie pour la réévaluation.

Pour en savoir plus sur l’utilisation de l’action **Insérer contrepartie immo.** sur les lignes feuille compta. immo., voir, par exemple, [Réévaluer les immobilisations](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Pour configurer les clés de ventilation d’immobilisations

Vous pouvez ventiler les transactions en départements ou en projets sur la base de clés de ventilation paramétrables. Vous pouvez, par exemple, définir une clé de ventilation pour répartir les coûts d’amortissement des véhicules entre le service administratif pour 35 % et le service commercial pour 65 %. Pour plus d’informations, reportez vous à [Répartition des coûts et du revenu](year-allocate-costs-income.md).

Les clés de ventilation s’appliquent à des classes d’immobilisations et non à des immobilisations individuelles.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. immo.**, puis choisissez le lien associé.  
2. Sur la page **Groupes compta. immo.**, sélectionnez l’action **Ventilations**, puis choisissez un type de validation.
3. Sur la page **Ventilations immo.**, renseignez les champs selon vos besoins.
4. Répétez les étapes 2 et 3 pour chacun des types de validation pour lesquels vous souhaitez définir des clés de ventilation.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Pour configurer les modèles feuille immobilisation

Un modèle est une présentation de feuille prédéfinie. Le modèle affiche des informations sur les codes suivi, les états et les souches de numéros. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crée automatiquement un modèle feuille immobilisation la première fois que vous ouvrez la page **Feuille immobilisation**. Vous pouvez cependant définir d’autres modèles feuille.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuille immo.**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Pour configurer des lots feuille immobilisation

Vous pouvez définir plusieurs feuilles, c’est-à-dire des feuilles individuelles pour chaque modèle feuille. Par exemple, chaque employé peut avoir sa propre feuille dont le nom correspond à ses initiales. Pour en savoir plus, consultez [Utiliser des feuilles comptabilité](ui-work-general-journals.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuille immo.**, puis sélectionnez le lien associé.  
2. Sélectionnez le modèle feuille pertinent, puis l’action **Lots**.
3. Sur la page **Lots feuille immo.**, renseignez les champs selon vos besoins.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Pour configurer des modèles feuille reclassement immobilisation

Vous pouvez utiliser les feuilles reclassement dédiées lorsque vous devez transférer, fractionner ou regrouper des immobilisations. [!INCLUDE[prod_short](includes/prod_short.md)] crée automatiquement un modèle feuille reclassement immobilisation la première fois que vous ouvrez la page **Feuille reclass. immo**. Vous pouvez paramétrer d’autres modèles feuille reclassement. Pour en savoir plus, consultez [Utiliser des feuilles comptabilité](ui-work-general-journals.md).  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuille reclass. immo.**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Pour configurer les lots feuille reclassement immobilisation

Vous pouvez définir plusieurs feuilles, c’est-à-dire des feuilles individuelles pour chaque modèle feuille reclassement. Par exemple, chaque employé peut avoir sa propre feuille reclassement dont le nom correspond à ses initiales. Pour en savoir plus, consultez [Utiliser des feuilles comptabilité](ui-work-general-journals.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuille reclass. immo.**, puis sélectionnez le lien associé.  
2. Sélectionnez le modèle feuille pertinent, puis l’action **Lots**.
3. Sur la page **Nom feuilles reclass. immo.**, renseignez les champs selon vos besoins.

## <a name="to-set-up-fixed-asset-class-codes"></a>Pour configurer les codes classe immobilisation

Les codes classe immobilisation peut être utilisé pour grouper des immobilisations, par exemple les immobilisations corporelles et les immobilisations incorporelles.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Classes immo.**, puis choisissez le lien associé.
2. Saisissez les codes et les noms des classes que vous souhaitez créer.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Pour configurer les codes sous-classe immobilisation

Le code sous-classe immobilisation permet de regrouper des immobilisations en catégories, comme les bâtiments, les véhicules, le mobilier et les machines.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sous-classes immo.**, puis choisissez le lien associé.
2. Saisissez les codes et les noms des classes que vous souhaitez créer.

## <a name="to-set-up-fixed-asset-location-codes"></a>Pour configurer les codes emplacement immobilisation

Les codes emplacement immobilisation permettent d’enregistrer l’emplacement de l’immobilisation, tel que le service commercial, l’accueil, l’administration, la production ou un entrepôt. Ces informations sont utiles pour les assurances et le suivi du stock.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements immo.**, puis choisissez le lien associé.
2. Saisissez les codes et les noms des emplacements immobilisation que vous souhaitez créer.

## <a name="to-register-opening-entries"></a>Pour enregistrer des écritures ouvertes

Si vous utilisez les immobilisations dans [!INCLUDE[prod_short](includes/prod_short.md)] pour la première fois, vous devez d’abord paramétrer le module de comptabilité avant de définir des immobilisations. La manière de procéder est différente si les immobilisations sont intégrées en comptabilité.  

 La procédure suivante est utilisée si les transactions immobilisation doivent être validées en comptabilité.  

1. Assurez-vous que vous avez suivi les procédures de configuration de base pour les immobilisations.  
2. Créez une fiche immobilisation pour chaque immobilisation existante.  
3. Créez une loi d’amortissement d’une immobilisation pour chaque type d’amortissement (par exemple les états financiers). Pour chaque loi d’amortissement, vous devez définir des conditions, par exemple l’intégration en comptabilité.  

    Activez l’intégration comptable en procédant comme suit. Premièrement, assurez-vous que l’intégration du grand livre est désactivée pour toutes les lois d’amortissement, puis validez les écritures ouvertes, et enfin activez l’intégration en comptabilité.  
4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Lois d’amortissement**, puis choisissez le lien associé.  
5. Sélectionnez la fiche de loi d’amortissement pertinente, puis sélectionnez l’action **Modifier** pour ouvrir la page **Fiche Lois d’amortissement**.
6. Sur le raccourci **Intégration**, assurez-vous que tous les champs sont vides en retirant toutes les coches. Si vous disposez de plusieurs lois d’amortissement, désactivez l’intégration en comptabilité pour chacune d’elles.  
7. Dans la feuille immobilisation, entrez les lignes suivantes pour chaque immobilisation :
   * Ligne avec le coût d’acquisition.
   * Une ligne avec l’amortissement cumulé jusqu’à la fin de l’exercice comptable précédent.
   * Une ligne avec l’amortissement cumulé du début de l’exercice comptable en cours jusqu’à la date à laquelle [!INCLUDE[prod_short](includes/prod_short.md)] est défini pour démarrer le calcul de l’amortissement.

    Si vous disposez d’autres soldes ouverts, vous pouvez également les saisir maintenant, (dépréciation, réévaluation, par exemple).  
8. Une fois que vous avez saisi et validé les lignes feuille pour chaque immobilisation, activez l’intégration en comptabilité dans les lois d’amortissement.

Si les immobilisations ne sont pas intégrées en comptabilité, omettez les étapes 6 et 8.

## <a name="see-also"></a>Voir aussi

[Paramétrage d’immobilisations](fa-setup.md)  
[Immobilisations](fa-manage.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
