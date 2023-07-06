---
title: Acquérir des immobilisations
description: 'Vous pouvez paramétrer une immobilisation, attribuer une loi d’amortissement et enregistrer le coût d’acquisition de l’immobilisation.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="acquire-fixed-assets"></a><a name="acquire-fixed-assets"></a><a name="acquire-fixed-assets"></a>Acquérir des immobilisations

Pour chaque immobilisation, vous devez créer une fiche contenant des informations la concernant. Vous pouvez configurer des bâtiments ou un équipement de production en tant qu’actif principal avec une liste de composants et vous pouvez les regrouper de différentes façons, comme par catégorie, département ou emplacement. Une loi d’amortissement doit être configurée et assignée à chaque immobilisation avant que vous puissiez l’acquérir.

Lorsqu’une immobilisation est configurée et lorsqu’une loi d’amortissement est attribuée, vous devez acquérir l’immobilisation. Pour acquérir une immobilisation, vous enregistrez son coût d’acquisition dans le compte général, le compte bancaire ou le fournisseur pertinent en validant une transaction d’acquisition à partir de la page **Feuille compta. immo.**. Vous pouvez utiliser la page **Acquisition d’immobilisation assistée** pour créer et valider automatiquement les lignes feuille comptabilité requises.

La valeur résiduelle est la valeur restante d’une immobilisation qui est devenue inutilisable. Vous pouvez valider la valeur résiduelle à partir d’une feuille immobilisation lors de la validation du coût d’acquisition. Pour en savoir plus, voir [Amortir des immobilisations](fa-how-depreciate-amortize.md).

L’actualisation permet d’ajuster des valeurs en fonction de modifications générales de niveau de prix. Le traitement par lots **Réévaluer immobilisations** permet de calculer les coûts d’acquisition à des coûts de remplacement.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a><a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a><a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Pour créer une immobilisation et l’acquérir automatiquement

La procédure suivante décrit comment créer une immobilisation, puis l’acquérir via la page **Acquisition d’immobilisation assistée** pour créer et valider les lignes feuille validation immobilisation requises. Vous pouvez également créer et valider les lignes feuille manuellement. Pour en savoir plus, voir [Pour valider manuellement une acquisition d’immobilisation avec la feuille validation immobilisation](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**, puis renseignez les champs du raccourci **Général**, le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sur le raccourci **Loi d’amortissement**, renseignez les champs, le cas échéant. Cette étape attribue une loi d’amortissement à l’immobilisation.  
4. Si vous devez assigner plus d’une loi d’amortissement à l’immobilisation, sélectionnez l’action **Ajouter davantage de lois d’amortissement**. Pour en savoir plus, voir [Pour attribuer une loi d’amortissement à une immobilisation](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Lorsque tous les champs obligatoires pour acquérir une immobilisation sont complétés, la notification **Vous êtes sur le point d’acquérir l’immobilisation. Acquérir** s’affiche en haut de la page.
5. Sélectionnez l’action **Acquérir** dans la notification.
6. Suivez les étapes sur la page **Acquisition d’immobilisation assistée** pour terminer l’acquisition automatique de l’immobilisation.

> [!NOTE]  
>   Vous pouvez également valider le coût d’acquisition en tant qu’avoirs. Dans ce cas, n’oubliez pas que la valeur du champ **Coût d’acquisition TVA incluse** doit comporter un signe moins pour indiquer un avoir.

Lorsque vous sélectionnez **Terminer**, le champ **Valeur comptable** de la page **Fiche immobilisation** est renseigné, indiquant que l’immobilisation a été acquise au coût d’acquisition spécifié.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a><a name="to-set-up-a-component-list-for-a-main-asset"></a><a name="to-set-up-a-component-list-for-a-main-asset"></a>Pour configurer une liste de composants pour une immobilisation principale

Vous pouvez regrouper les immobilisations en immobilisations principales divisées en composants. Par exemple, si vous disposez d’une machine de production composée de différentes pièces, vous pouvez regrouper ces pièces de cette manière.  

Vous devez définir à la fois l’immobilisation principale et ses composants en tant que fiches immobilisation individuelles. Une fois la liste de composants créée, [!INCLUDE[prod_short](includes/prod_short.md)] renseigne automatiquement les champs **Immo. principale/Composant** et **Composant immo. principale** sur les fiches immobilisation.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation principale, puis l’action **Composants immo. principale**.
3. Sur la page **Composants immo. principale**, choisissez **N° immo.**., puis sélectionnez l’immobilisation que vous souhaitez ajouter comme composant de l’immobilisation principale.
4. Fermez la page.
5. Répétez les étapes 3 et 4 pour chaque composant de l’immobilisation que vous souhaitez ajouter.
6. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres immobilisations**, puis choisissez le lien associé.
7. Cochez la case **Compta. immo. princip.**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a><a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a><a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Pour valider manuellement une acquisition d’immobilisation avec une feuille validation immobilisation

La procédure suivante décrit comment acquérir manuellement une immobilisation en créant et en validant des lignes sur la page **Feuille compta. immo.**. Vous pouvez également acquérir automatiquement une immobilisation via la page **Acquisition d’immobilisation assistée**. Pour en savoir plus, voir l’étape 5 de [Pour créer une immobilisation et l’acquérir automatiquement](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Vous pouvez également valider le coût d’acquisition en tant qu’avoirs. Dans ce cas, n’oubliez pas que la valeur du champ **Montant** doit comporter un signe moins pour indiquer un avoir.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilisation immobilisation**, puis choisissez le lien associé.
2. Sur la page **Feuille compta. immo.**, dans le champ **Type compta. immo.**, sélectionnez **Coût acquisition**.
3. Renseignez les champs restants selon vos besoins.
4. Sélectionnez l’action **Valider**.  

> [!TIP]  
>   Si vous renseignez le champ **N° assurance** dans la feuille validation immobilisation lorsque vous validez un coût d’acquisition, [!INCLUDE[prod_short](includes/prod_short.md)] valide également le coût d’acquisition de l’immobilisation dans les écritures assurance. Pour en savoir plus, voir [Assurer des immobilisations](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a><a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a><a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Pour annuler la validation du coût d’une acquisition pour une immobilisation

Si vous faites une erreur lors de la validation d’un coût d’acquisition, vous pouvez supprimer l’écriture à l’aide du traitement par lots **Annuler écritures immo**, puis valider l’écriture d’acquisition correcte. Les écritures erronées sont transférées vers la page **Erreur écritures comptables immo.**.

Par exemple, si vous validez une acquisition avec une date erronée, vous devez la corriger dès que possible, car la date de validation de l’immobilisation est utilisée pour de nombreux calculs.

> [!IMPORTANT]  
> Vous ne pouvez pas utiliser la fonction **Transaction contrepassée** pour les écritures comptables immobilisation.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures comptables immobilisation**, puis sélectionnez le lien associé.  
2. Sur la page **Écritures comptables immobilisation**, sélectionnez la ou les entrées à annuler.  
3. Choisissez le menu **Actions**, puis choisissez l’action **Annuler les entrées**.
4. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Pour lancer le traitement par lots, cliquez sur le bouton **OK**.
6. Lorsqu’une écriture incorrecte ou lorsque plusieurs écritures incorrectes sont annulées, continuez à valider le coût d’acquisition exact.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a><a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a><a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Pour valider la valeur résiduelle ainsi que le coût d’acquisition

Vous pouvez valider la valeur résiduelle avec le coût d’acquisition à partir d’une feuille immobilisation.

> [!NOTE]
> Ce processus peut nécessiter que vous personnalisiez la page Feuilles immobilisations en ajoutant le champ Valeur résiduelle. Par défaut, le champ À ne s’affiche pas sur la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuilles immobilisation**, puis choisissez le lien associé.
2. Sur la page **Feuilles immobilisation**, créez la ligne d’acquisition. Pour en savoir plus, voir [Pour valider manuellement une acquisition d’immobilisation avec la feuille validation immobilisation](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Dans le champ **Valeur résiduelle** de la ligne feuille, saisissez le montant de la valeur résiduelle comme avoir (préfixe du montant avec un signe moins, par exemple, **-** 100).
4. Sélectionnez l’action **Valider**.

> [!NOTE]
> S’il existe une valeur résiduelle pour une immobilisation, celle-ci est utilisée dans la validation de l’amortissement au lieu de la valeur dans le champ **Valeur comptable finale** de la page **Lois d’amortissement immo**. Pour plus d’informations, voir [Pour gérer la valeur comptable finale](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/purchase-fixed-assets/) associée

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d’immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
