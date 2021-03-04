---
title: Utiliser des profils pour classer les contacts
description: Configurer des questionnaires profil pour classer vos contacts professionnels
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2020
ms.openlocfilehash: 65c27bee86d273c467709f1e238b996829d73f37
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755457"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Utiliser des questionnaires profil pour classer les contacts professionnels
Vous pouvez configurer des questionnaires profil à utiliser au moment d’entrer des informations sur les profils de vos contacts. Dans chaque questionnaire, vous pouvez configurer les questions à poser à vos contacts.  

Vous pouvez également exécuter le questionnaire pour répondre automatiquement à certaines de ces questions en fonction des données contact, client ou fournisseur.  

## <a name="to-add-a-profile-questionnaire"></a>Pour ajouter un questionnaire profil
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres questionnaire**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Pour ajouter des questions à un questionnaire profil
1.  Choisissez le questionnaire profil approprié, puis sélectionnez l’action **Modifier paramètres questionnaire**.  
2.  Sur la première ligne vide, dans le champ **Type**, choisissez **Question**, puis tapez la question dans le champ **Désignation**. Renseignez les autres champs sur cette ligne.  
3.  Sur la ligne vide suivante, dans le champ **Type**, choisissez **Réponse**, puis tapez la réponse dans le champ **Désignation**.  
4.  Dans le champ **Priorité**, sélectionnez la priorité. Dans les champs **Valeur début** et **Valeur fin**, définissez une plage de points. Les contacts obtenant un nombre de points compris dans la plage définie recevront la réponse.  

Répétez ces étapes pour entrer toutes les questions et réponses du questionnaire profil.

Après avoir créé un questionnaire, vous devez créer des évaluations contact pour classer vos contacts. Vous pouvez également définir des questions qui sont évaluées automatiquement en fonction des informations de la fiche contact.  

> [!NOTE]
> Si vous entrez une question dont la réponse est automatique, choisissez <STRONG>Ligne</STRONG>, puis <STRONG>Questionnaire</STRONG> pour entrer les critères de réponse automatique.

## <a name="the-automatic-classification-of-contacts"></a>Classification automatique des contacts
Vous pouvez configurer le programme pour qu’il classe automatiquement les contacts en fonction des données client, fournisseur et contact. Pour cela, configurez des questions profil à réponse automatique sur la page **Paramètres questionnaires profil**.  

> [!NOTE]
> Vous ne pouvez affecter une classification basée sur les données contact qu’aux contacts enregistrés en tant que clients. De même, seuls les contacts enregistrés en tant que fournisseurs peuvent se voir affecter une classification basée sur les données fournisseur. La classification automatique n’est pas mise à jour automatiquement. Par conséquent, vous pouvez être amené à mettre à jour les questionnaires profil après avoir mis à jour les données client, fournisseur ou contact dont ils dépendent.  

Une fois que vous avez configuré les questions profil à réponse automatique, affectez à un contact le questionnaire profil qui les contient. [!INCLUDE[prod_short](includes/prod_short.md)] répond ensuite automatiquement aux questions.  

## <a name="example"></a>Exemple :
Vous pouvez classer vos contacts en fonction du montant de leurs achats :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Réponse</strong></th>
<th><strong>Doc. lettrage</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>contacts ayant effectué des achats pour une somme supérieure ou égale à 500 000 DS</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>contacts ayant effectué des achats pour une somme comprise entre 100 000 et 499 999 DS</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>contacts ayant effectué des achats pour une somme inférieure ou égale à 99 999 DS</p></td>
</tr>
</tbody>
</table>

Pour cela, renseignez la page **Paramètres questionnaires profil** comme suit :


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Type</strong></th>
<th><strong>Description</strong></th>
<th><strong>Classification automatique</strong></th>
<th><strong>Valeur début</strong></th>
<th><strong>Valeur fin</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Question</p></td>
<td><p>Classification ABC</p></td>
<td><p>Cochez la ligne appropriée.</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Réponse</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Réponse</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Réponse</p></td>
<td><p>C</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Renseignez ensuite la page **Questionnaire profil** comme suit :
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Champ</strong></th>
<th><strong>Valeur</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Champ de classification des clients</strong></td>
<td><emphasis>Ventes DS</emphasis></td>
</tr>
<tr>
<td><strong>Méthode classification</strong></td>
<td><emphasis>Valeur définie</emphasis></td>
</tr>
</tbody>
</table>

Lorsque vous affectez le questionnaire profil contenant cette question à un contact, l’application insère automatiquement la réponse correspondante dans les lignes profil de la fiche contact.

## <a name="see-also"></a>Voir aussi
[Création de contacts](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]