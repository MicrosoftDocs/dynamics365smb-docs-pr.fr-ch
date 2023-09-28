---
title: Création des souches de numéros
description: "Découvrez comment configurer des souches de numéros qui affectent les codes d’identification uniques aux comptes et aux documents dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: bholtorf
---
# <a name="create-number-series"></a>Création des souches de numéros

Pour chaque société que vous configurez, vous devez affecter des codes d’identification uniques aux éléments tels que les comptes généraux, les comptes client et fournisseur, les factures et d’autres documents. La numérotation est importante, pas uniquement pour l’identification. Un système de numérotation bien conçu facilite la gestion et l’analyse de la société et permet de réduire les erreurs de saisie des données.

> [!Important]
> Par défaut, les écarts dans les souche de numéros ne sont pas autorisés car l’historique exact des transactions financières doit être disponible pour audit, conformément à la loi, et doit donc suivre une séquence ininterrompue sans numéros supprimés.
> 
> Si vous souhaitez autoriser des écarts dans certaines séries de nombres, commencez par consulter l’auditeur ou le responsable de la comptabilité pour vous assurer de respecter les exigences légales en vigueur dans votre pays/région. Pour plus d’informations, voir la section [Écarts dans les souches de numéros](#gaps-in-number-series).

> [!NOTE]  
> Il est recommandé d’utiliser les mêmes codes souche de numéros que ceux répertoriés sur la page **Liste de souches de numéros** de la société de démonstration CRONUS. Des codes tels que *P-INV+* ne vont pas vous paraître significatifs au premier abord, mais [!INCLUDE[prod_short](includes/prod_short.md)] dispose d’un certain nombre de paramètres par défaut en fonction de ces codes souche de numéros.

Vous créez un système de numérotation en définissant un ou plusieurs codes pour chaque type de données de base ou de document. Par exemple, vous pouvez définir un code pour la numérotation de clients, un code pour la numérotation des factures vente et un autre code pour la numérotation des documents dans les feuilles comptabilité. Une fois que vous avez défini un code, vous devez définir au moins une ligne souche de numéros. Celle-ci contient des informations telles que les premier et dernier numéros de la souche et la date de début. Vous pouvez définir plusieurs lignes souche de numéros par code souche de numéros, avec une date de début différente pour chaque ligne. Les souches sont utilisées de manière consécutive, chaque souche commençant à la date de début respective.

> [!NOTE]
> La longueur maximale d’un nombre dans une souche de numéros est de 20 caractères. Il y a des situations où [!INCLUDE[prod_short](includes/prod_short.md)] ajoutera un numéro avec un ID généré par le système. Par exemple, lorsque des documents tels que des factures sont utilisés pour appliquer des transactions, telles que des paiements, [!INCLUDE[prod_short](includes/prod_short.md)] génère des identificateurs pour les transactions appliquées. L’identificateur est composé d’un numéro d’une souche de numéros et d’un identificateur à six caractères attribué par le système, tel que -12345. Si vous prévoyez de traiter plus de 9 999 documents dans des journaux bancaires ou GIRO, ou dans des journaux de reçus de caisse, configurez des souches de numéros pour ces types de documents pour inclure moins de 14 caractères.

Vous devez généralement définir votre souche de numéros pour insérer automatiquement le numéro suivant sur des fiches ou des documents que vous créez. Toutefois, vous pouvez également définir une souche de numéros pour permettre la saisie manuelle du nouveau numéro. Vous spécifiez cela grâce à la case à cocher **N° manuels**.

Si vous voulez utiliser plusieurs codes souche de numéros pour un type de données de base (par exemple, si vous voulez utiliser différentes souches de numéros pour diverses catégories d’articles), vous pouvez utiliser des liens de souches de numéros.

## <a name="gaps-in-number-series"></a>Écarts dans les souches de numéros
Tous les enregistrements que vous créez dans [!INCLUDE[prod_short](includes/prod_short.md)] ne sont pas des transactions financières qui doivent utiliser une numérotation séquentielle. Les fiches client, les devis, et les activités d’entrepôt sont des exemples d’enregistrements auxquels un numéro d’une souche de numéros est attribué, mais qui ne sont pas soumis à l’audit financier et/ou peuvent être supprimés. Pour ces souches de numéros, vous pouvez cocher la case **Autoriser les écarts dans les numéros** sur la page **Lignes souche de n°**. Ce paramètre peut être également modifié après la création de la souche de numéros. Pour plus d’informations, voir [Pour créer des souches de numéros](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportement du champ N° sur des documents et des fiches

Sur les documents de vente, d’achat et de transfert ainsi que sur toutes les fiches, le champ **N°** peut être renseigné automatiquement depuis une souche de numéros prédéfinie ou vous pouvez l’ajouter manuellement. Cependant, dans certaines circonstances, le champ **N°** est invisible pour vous empêcher de le modifier.  

Le champ **N°** peut être renseigné de trois manières :

1. Si une seule souche de numéros pour le type de document ou de fiche existe, et que le champ **N° par défaut** est sélectionné, et le champ **N° manuels** n’est pas sélectionné pour cette souche de numéros, alors le champ est renseigné automatiquement avec le numéro suivant dans la souche. Le champ **N°** ne sera pas visible sur la fiche ou le document.  

    Même si vous définissez des modèles avec différentes souches de numéros pour les clients, si la souche de numéros définie sur la page **Paramètres ventes** est configurée de cette manière, le champ **N°** sera invisible sur la fiche client, quel que soit le modèle que vous utilisez. Il en va de même pour les autres types de fiches et de documents.  

    > [!NOTE]  
    > Si une souche de numéros ne fonctionne pas, par exemple parce qu’elle manque de numéros, le champ **N°** est visible et vous pouvez saisir manuellement un numéro ou résoudre les problèmes sur la page **Souches de n°**.

2. Si plusieurs souches de numéros pour le type de document vente existent, et si la case à cocher **N° par défaut** n’est pas cochée pour la souche de numéros qui est actuellement affectée, le champ **N°** est visible, et vous pouvez accéder à la page **Liste Souche de n°** et sélectionnez la souche de numéros que vous souhaitez utiliser. Le numéro suivant dans la souche sélectionnée est inséré dans le champ **N°** .

3. Si vous n’avez défini aucune souche de numéros pour ce type de document ou fiche ou si le champ **N° manuels** est sélectionné pour la souche de numéros, alors le champ **N°** est visible et vous devez saisir manuellement les numéros. Vous pouvez entrer un maximum de 20 caractères alphanumériques.

Lorsque vous ouvrez un nouveau document ou une nouvelle fiche pour lequel il existe une souche de numéros, la page **Paramètres souche de n°** s’ouvre afin de pouvoir configurer une souche de numéros pour ce type de document ou fiche, avant de continuer avec une autre saisie de donnée.

> [!NOTE]  
> Si vous devez activer la numérotation manuelle, par exemple, les nouvelles fiches article qui ont été créées avec un processus de migration des données pour lesquelles le champ **N°** est masqué par défaut, allez ensuite sur la page **Paramètres stock** et choisissez le champ **N° article** pour ouvrir et définir la souche de numéros sur **N° manuels**.

## <a name="to-create-a-new-number-series"></a>Pour créer des souches de numéros

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Souches de n°**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.  
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sélectionnez l’option **Lignes**.  
5. Sur la page **Lignes souche de n°**, remplissez les champs pour définir l’utilisation réelle et le contenu de la souche de numéros créée à l’étape 2.  
6. Répétez l’étape 5 pour autant d’utilisations différentes de la série de chiffres dont vous avez besoin. Le champ **Date de début** définit quelle ligne de souche de numéros est active.  

> [!TIP]
> Pour permettre aux utilisateurs de spécifier manuellement des numéros lorsqu’ils enregistrent un nouveau client ou fournisseur, par exemple, choisissez le champ **Numéros manuels** sur la série de nombres elle-même. Pour interdire le numéro manuel, effacez le champ.

Vous pouvez attribuer des souches de numéros aux modèles que vous configurez pour les différents types de clients et de fournisseurs que vos commerciaux et acheteurs ajoutent le plus souvent à votre fichier [!INCLUDE [prod_short](includes/prod_short.md)]. Dans ce cas, configurez la souche de numéros appropriée, liez-la via des relations, puis ajoutez la première souche de numéros dans la relation appropriée à la page de configuration appropriée. Ensuite, lorsqu’un utilisateur crée un client, il choisit le modèle approprié et le nouveau client reçoit un numéro attribué à partir de la souche de numéros définie pour ce modèle.  

## <a name="to-create-relationships-between-number-series"></a>Pour créer des liens entre des souches de numéros

Si vous avez défini plusieurs codes souche de numéros pour un même type d’informations ou de transactions de base, vous pouvez créer des liens entre ces codes. Cette fonction peut vous aider à choisir parmi ces codes lorsque vous utilisez un numéro. Lorsque vous établissez un lien entre plusieurs souches de numéros, vous associez toutes les souches de numéros liées à un code souche de numéros. Ensuite, vous pouvez entrer ce code dans un champ sur le Raccourci **Numérotage** dans l’une des pages de configuration pertinentes, telles que **Paramètres ventes**.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Souches de n°**, puis choisissez le lien associé.
2. Sélectionnez la ligne avec la souche de numéros pour laquelle vous souhaitez créer des relations, puis cliquez sur **Relations**.
3. Dans le champ **Code souche**, entrez le code de la souche de numéros à lier à la souche sélectionnée à l’étape 2.
4. Ajoutez une ligne pour chaque code à lier à la souche de numéros sélectionnée.
5. Fermez la page.

Désormais, pour créer un élément nécessitant un numéro, vous pourrez utiliser les liens ainsi créés et choisir parmi les souches de numéros liées.

## <a name="to-set-up-where-a-number-series-is-used"></a>Pour définir l’emplacement d’utilisation de la souche de numéros

La procédure suivante indique comment définir des souches de numéros pour la zone Ventes. La procédure est identique pour d’autres secteurs.  

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.
2. Sur la page **Ventes**, dans le raccourci **Souche de numéros**, sélectionnez la souche de numéros souhaitée pour chaque fiche ou document vente.

Le numéro sélectionné est désormais utilisé pour renseigner le champ **N°** sur la fiche ou le document en question, en fonction des paramètres définis sur la ligne souche de numéros.  

## <a name="see-also"></a>Voir aussi

[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
