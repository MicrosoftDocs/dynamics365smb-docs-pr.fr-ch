---
title: "Acquérir des immobilisations| Microsoft Docs"
description: "Vous pouvez paramétrer une immobilisation, attribuer une loi d'amortissement et enregistrer le coût d'acquisition de l'immobilisation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a5ce3c514ff649b5ad4a901f257816ae1a59d58
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="acquire-fixed-assets"></a>Acquérir des immobilisations
Pour chaque immobilisation, vous devez créer une fiche contenant des informations la concernant. Vous pouvez configurer des bâtiments ou un équipement de production en tant qu'actif principal avec une liste de composants et vous pouvez les regrouper de différentes façons, comme par catégorie, département ou emplacement. Une loi d'amortissement doit être configurée et assignée à chaque immobilisation avant que vous puissiez l'acquérir.

Lorsqu'une immobilisation est configurée et lorsqu'une loi d'amortissement est attribuée, vous devez acquérir l'immobilisation. Pour acquérir une immobilisation, vous enregistrez son coût d'acquisition dans le compte général, le compte bancaire ou le fournisseur pertinent en validant une transaction d'acquisition à partir de la fenêtre **Feuille compta. immo.**. Vous pouvez utiliser la fenêtre **Acquisition d'immobilisation assistée** pour créer et valider automatiquement les lignes feuille comptabilité requises.

La valeur résiduelle est la valeur restante d'une immobilisation qui est devenue inutilisable. Vous pouvez valider la valeur résiduelle à partir d'une feuille immobilisation lors de la validation du coût d'acquisition. Pour en savoir plus, voir [Amortir des immobilisations](fa-how-depreciate-amortize.md).

L'actualisation permet d'ajuster des valeurs en fonction de modifications générales de niveau de prix. Le traitement par lots **Réévaluer immobilisations** permet de calculer les coûts d'acquisition à des coûts de remplacement.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Pour créer une immobilisation et l'acquérir automatiquement
La procédure suivante décrit comment créer une immobilisation, puis l'acquérir via la fenêtre **Acquisition d'immobilisation assistée** pour créer et valider les lignes feuille validation immobilisation requises. Vous pouvez également créer et valider les lignes feuille manuellement. Pour en savoir plus, voir la section « Pour valider manuellement une acquisition d'immobilisation avec la feuille validation immobilisation ».

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.  
2. Sélectionnez l'action **Nouveau**, puis renseignez les champs du raccourci **Général**, le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sur le raccourci **Loi d'amortissement**, renseignez les champs, le cas échéant. Cette étape attribue une loi d'amortissement à l'immobilisation.  
4. Si vous devez assigner plus d'une loi d'amortissement à l'immobilisation, sélectionnez l'action **Ajouter davantage de lois d'amortissement**. Pour en savoir plus, voir la section « Assigner une loi d'amortissement à une immobilisation » dans [Définir l'amortissement d'immobilisation](fa-how-setup-depreciation.md).

    Lorsque tous les champs obligatoires pour acquérir une immobilisation sont complétés, la notification **Vous êtes sur le point d'acquérir l'immobilisation. Acquérir** s'affiche en haut de la page.
5. Sélectionnez l'action **Acquérir** dans la notification.
6. Suivez les étapes dans la fenêtre **Acquisition d'immobilisation assistée** pour terminer l'acquisition automatique de l'immobilisation.

> [!NOTE]  
>   Vous pouvez également valider le coût d'acquisition en tant qu'avoirs. Dans ce cas, n'oubliez pas que la valeur du champ **Coût d'acquisition TVA incluse** doit comporter un signe moins pour indiquer un avoir.

Lorsque vous sélectionnez **Terminer**, le champ **Valeur comptable** de la fenêtre **Fiche immobilisation** est renseigné, indiquant que l'immobilisation a été acquise au coût d'acquisition spécifié.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Pour configurer une liste de composants pour une immobilisation principale
Vous pouvez regrouper les immobilisations en immobilisations principales divisées en composants. Par exemple, si vous disposez d'une machine de production composée de différentes pièces, vous pouvez regrouper ces pièces de cette manière.  

Vous devez définir à la fois l'immobilisation principale et ses composants en tant que fiches immobilisation individuelles. Une fois la liste de composants créée, [!INCLUDE[d365fin](includes/d365fin_md.md)] renseigne automatiquement les champs **Immo. principale/Composant** et **Composant immo. principale** sur les fiches immobilisation.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l'immobilisation principale, puis l'action **Composants immo. principale**.
3. Dans la fenêtre **Composants immo. principale**, choisissez **N° immo.**., puis sélectionnez l'immobilisation que vous souhaitez ajouter comme composant de l'immobilisation principale.
4. Fermez la fenêtre.
5. Répétez les étapes 3 et 4 pour chaque composant de l'immobilisation que vous souhaitez ajouter.
6. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres immobilisations**, puis sélectionnez le lien associé.
7. Cochez la case **Compta. immo. princip.**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Pour valider manuellement une acquisition d'immobilisation avec une feuille validation immobilisation
La procédure suivante décrit comment acquérir manuellement une immobilisation en créant et en validant des lignes dans la fenêtre **Feuille compta. immo.**. Vous pouvez également acquérir automatiquement une immobilisation via la fenêtre **Acquisition d'immobilisation assistée**. Pour en savoir plus, voir l'étape 5 de la section « Pour créer une immobilisation et l'acquérir automatiquement ».

> [!NOTE]  
>   Vous pouvez également valider le coût d'acquisition en tant qu'avoirs. Dans ce cas, n'oubliez pas que la valeur du champ **Montant** doit comporter un signe moins pour indiquer un avoir.

1. Choisissez l'icône de ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilisation immobilisation**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Feuille compta. immo.**, dans le champ **Type compta. immo.**, sélectionnez **Coût acquisition**.
3. Renseignez les champs restants selon vos besoins.
4. Sélectionnez l'action **Valider**.  

> [!TIP]  
>   Si vous renseignez le champ **N° assurance** dans la feuille validation immobilisation lorsque vous validez un coût d'acquisition, [!INCLUDE[d365fin](includes/d365fin_md.md)] valide également le coût d'acquisition de l'immobilisation dans les écritures assurance. Pour en savoir plus, voir [Assurer des immobilisations](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Pour annuler la validation du coût d'une acquisition pour une immobilisation
Si vous faites une erreur lors de la validation d'un coût d'acquisition, vous pouvez supprimer l'écriture à l'aide du traitement par lots **Annuler écritures immo**, puis valider l'écriture d'acquisition correcte. Les écritures erronées sont transférées vers la fenêtre **Erreur écritures comptables immo.**.

Par exemple, si vous validez une acquisition avec une date erronée, vous devez la corriger dès que possible, car la date de validation de l'immobilisation est utilisée dans de nombreux calculs essentiels.

> [!IMPORTANT]  
>   Vous ne pouvez pas utiliser la fonction **Transaction contrepassée** pour les écritures comptables immobilisation.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Annuler écritures immo.**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour lancer le traitement par lots, cliquez sur le bouton **OK**.
4. Lorsqu'une écriture incorrecte ou lorsque plusieurs écritures incorrectes sont annulées, continuez à valider le coût d'acquisition exact.

Pour annuler les écritures comptables pour plusieurs immobilisations à la fois, utilisez le traitement par lots **Annuler les écritures comptables immobilisation**.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Pour valider la valeur résiduelle ainsi que le coût d'acquisition
Vous pouvez valider la valeur résiduelle avec le coût d'acquisition à partir d'une feuille comptable immobilisation.    

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Annuler écritures immo.**, puis sélectionnez le lien associé.
2. Créez la ligne feuille d'acquisition. Pour en savoir plus, voir la section « Pour valider manuellement une acquisition d'immobilisation avec la feuille validation immobilisation ».
3. Dans le champ **Valeur résiduelle** de la ligne feuille, saisissez le montant de la valeur résiduelle comme avoir (avec un signe moins).
4. Sélectionnez l'action **Valider**.

> [!NOTE]  
>   Le type de validation **Valeur résiduelle** est une option disponible uniquement dans la fenêtre **Feuille immo.** Elle n'est pas disponible dans la fenêtre **Feuille compta. immo.**, car la valeur résiduelle n'est jamais affichée en comptabilité.

## <a name="see-also"></a>Voir aussi
[COMPTES D'IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d'immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

