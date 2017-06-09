---
title: "À propos de la configuration de la TVA | Microsoft Docs"
description: "Assurez-vous de calculer, de valider et de déclarer correctement la TVA pour les ventes et les achats."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bf06b41a87e24af9e7657dd0585d7d13e3cad1b2
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---

# <a name="setting-up-included365finlongincludesd365finlongmdmd-to-calculate-and-post-value-added-tax"></a>Configuration de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] pour calculer et valider la TVA
Les clients et les entreprises payent la TVA lorsqu'ils achètent des biens ou des services. Le montant de la TVA à payer peut varier en fonction de plusieurs facteurs. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous configurez la TVA pour spécifier les taux à utiliser pour calculer les montants de taxe sur la base des éléments suivants : 

* À qui vous vendez  
* À qui vous achetez  
* Ce que vous vendez  
* Ce que vous achetez  
  
Vous pouvez configurer manuellement les calculs de la TVA, mais cette procédure peut être délicate et longue. Pour vous faciliter la tâche, nous avons fourni un guide de configuration assistée appelé **Paramètres TVA** pour vous aider. Il est recommandé d'utiliser le guide de configuration assistée pour configurer la TVA.

**Remarque** : vous pouvez utiliser le guide uniquement si vous avez créé un profil Ma société, et si vous n'avez pas validé de transactions incluant la TVA. Sinon, il serait très facile d'utiliser différents taux de TVA par erreur et de générer des états de TVA erronés.  
  
Si vous souhaitez configurer vous-même les calculs de TVA, ou en savoir plus sur chaque étape, cette rubrique contient des descriptions de chaque étape. Ces descriptions indiquent comment :  
  
* Configurer des groupes comptabilisation marché TVA pour définir les taux de TVA des marchés dans lesquels vous opérez. Vous les affectez aux clients et aux fournisseurs.  
* Configurer des groupes comptabilisation produit TVA pour définir les taux de TVA des produits et services que vous achetez ou vendez.  
  
   **Remarque** : les concepts associés aux groupes comptabilisation marché et produit TVA sont similaires aux groupes comptabilisation généraux. Pour plus d'informations, voir [Paramètres du groupe comptabilisation](finance-posting-groups.md).
* Regrouper des groupes comptabilisation marché et produit TVA pour créer les paramètres TVA permettant de calculer les montants de TVA sur les ventes et les achats.  
* Affecter des groupes comptabilisation produit TVA aux comptes généraux que vous utilisez pour les ventes et les achats, ainsi qu'à des articles et des ressources.  

   **Remarque** : pour configurer la TVA pour les ressources, vous devez activer l'expérience utilisateur **Suite** pour votre société. Pour plus d'informations, voir [Personnalisation de votre expérience Dynamics 365 for Financials](ui-experiences.md).
* Utiliser une TVA déductible pour le commerce entre pays/régions de l'UE  
* Comprendre l'arrondi TVA pour les documents  
* Configurer des clauses pour expliquer l'utilisation de taux de TVA non standard
* Vérifier les numéros d'identification TVA

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Utiliser le guide de configuration assistée Paramètres TVA pour configurer la TVA (recommandé)
Il est recommandé d'utiliser le guide de configuration assistée Paramètres TVA pour configurer la TVA dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Pour démarrer le guide de configuration assistée, procédez comme suit :
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche") et entrez **Configuration assistée**.  
2. Choisissez **Paramètres TVA**.

## <a name="set-up-vat-business-posting-groups"></a>Configurer des groupes comptabilisation marché TVA
Les groupes comptabilisation marché TVA doivent représenter les marchés dans lesquels vous faites des affaires avec les clients et fournisseurs, et définissent comment calculer et valider la TVA dans chaque marché. Des exemples de groupes comptabilisation marché TVA sont **France** et **Union Européenne (UE)**.  

Utilisez des codes faciles à retenir et qui décrivent le groupe comptabilisation marché, tels que **UE**, **Non-UE** ou **France**. Le code doit être unique. Vous pouvez créer autant de codes que vous le souhaitez, mais vous ne pouvez pas avoir le même code deux fois dans une table.
  
Pour configurer un groupe comptabilisation marché TVA, procédez comme suit :

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Groupe compta. marché TVA**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

Paramétrez les groupes comptabilisation marché TVA par défaut en les liant à des groupes comptabilisation marché. [!INCLUDE[d365fin](includes/d365fin_md.md)] affecte automatiquement le groupe comptabilisation marché TVA lorsque vous affectez le groupe comptabilisation marché à un client, un fournisseur ou un compte général. 

## <a name="set-up-vat-product-posting-groups"></a>Configurer des groupes comptabilisation produit TVA
Les groupes comptabilisation produit TVA représentent les articles et les ressources que vous achetez ou vendez et déterminent la manière de calculer et de valider la TVA en fonction du type d'article ou de ressource acheté ou vendu.
Il est recommandé d'utiliser des codes faciles à retenir et qui décrivent le taux, par exemple **SANS TVA** ou **Zéro**, **TVA10** ou **Réduite** pour 10 % de TVA, et **TVA25** ou **Standard** pour 25 %.

Pour configurer un groupe comptabilisation marché TVA, procédez comme suit :

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Groupe compta. produit TVA**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Regrouper des groupes comptabilisation TVA dans les paramètres comptabilisation TVA
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcule les montants de TVA sur les ventes et les achats en fonction des paramètres comptabilisation TVA, qui sont des combinaisons de groupes comptabilisation marché et produit TVA. Pour chaque combinaison, vous pouvez spécifier le pourcentage de TVA, le mode calcul TVA et les comptes généraux pour la validation de la TVA pour les achats, les ventes, ainsi que les taxes déductibles. Vous pouvez également indiquer si la TVA doit être recalculée lorsqu'un escompte est appliqué ou reçu.  

Définissez autant de combinaisons que nécessaire. Si vous voulez regrouper des combinaisons de paramètres comptabilisation TVA avec des attributs similaires, vous pouvez définir un **Identifiant TVA** pour chaque groupe et affecter l'identifiant aux membres du groupe.

Pour regrouper des paramètres comptabilisation TVA, procédez comme suit :

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramètres compta. TVA**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Affecter des groupes comptabilisation TVA par défaut à plusieurs entités
Si vous souhaitez appliquer les mêmes groupes comptabilisation TVA à plusieurs entités, vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour le faire par défaut. Plusieurs méthodes sont disponibles :

* Vous pouvez affecter des groupes comptabilisation marché aux groupes comptabilisation marché généraux ou aux modèles client ou fournisseur 
* Vous pouvez affecter des groupes comptabilisation produit TVA aux groupes comptabilisation produit généraux  

Le groupe comptabilisation marché ou produit TVA est affecté lorsque vous choisissez un groupe comptabilisation marché ou produit pour un client, un fournisseur, un article ou une ressource.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Affecter des groupes comptabilisation TVA à des comptes, clients, fournisseurs, articles et ressources individuels
Les sections suivantes décrivent comment affecter des groupes comptabilisation TVA à des entités individuelles.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Pour affecter des groupes comptabilisation TVA à des comptes généraux individuels 
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien associé.  
2. Ouvrez la fiche **Compte général** pour le compte.
3. Sous le raccourci **Comptabilisation**, dans le champ **Type compta. TVA**, choisissez **Vente** ou **Achat**.  
5. Choisissez les groupes comptabilisation TVA à utiliser pour le compte vente ou achat.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Pour affecter des groupes comptabilisation marché TVA à des clients et des fournisseurs  
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Client** ou **Fournisseur**, puis sélectionnez le lien associé.  
2. Sur la fiche **Client** ou **Fournisseur**, développez le raccourci **Facturation**.  
3. Choisissez le groupe comptabilisation marché TVA.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Pour affecter des groupes comptabilisation produit TVA à des articles et des ressources individuels  
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Article** ou **Ressource**, puis sélectionnez le lien associé.  
2. Exécutez l'une des opérations suivantes :
* Sur la fiche **Article**, développez le raccourci **Prix et validation**, puis sélectionnez **Afficher plus** pour afficher .  
* Sur la fiche **Ressource**, développez le raccourci **Facturation**.  
3. Choisissez le groupe comptabilisation produit TVA.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Configurer des clauses pour expliquer l'utilisation de taux de TVA non standard
Vous définissez une clause TVA afin de décrire le type de TVA qui est appliquée. Les informations peuvent être requises par une réglementation gouvernementale. Après avoir configuré une clause TVA et l'avoir associée à un paramètre validation TVA, la clause TVA est affichée sur les documents vente imprimés qui utilisent le groupe de paramètres validation TVA. 

Si nécessaire, vous pouvez également spécifier comment convertir les clauses TVA dans d'autres langues. Ensuite, lorsque vous créez et imprimez un document vente qui contient un identifiant TVA, le document comprend la clause TVA traduite. Le code langue spécifié sur la fiche client détermine la langue.
  
### <a name="to-set-up-vat-clauses"></a>Pour configurer des clauses TVA
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Clauses TVA**, puis sélectionnez le lien associé.  
2. Sur la page **Clauses TVA**, créez une ligne.  
3. Dans le champ **Code**, entrez un identificateur pour la clause. Vous utilisez ce code pour affecter la clause à des groupes comptabilisation TVA.  
4. Dans le champ **Description**, saisissez le texte que vous souhaitez afficher sur les documents pouvant inclure la TVA. Dans le champ **Description 2**, entrez du texte supplémentaire, si nécessaire. Le texte s'affiche sur de nouvelles lignes.  
5. Facultatif : pour affecter immédiatement la clause TVA à un paramètre comptabilisation TVA, sélectionnez **Paramètres**, puis sélectionnez la clause. Si vous souhaitez attendre, vous pouvez affecter la clause ultérieurement dans la page Paramètres comptabilisation TVA.  
6. Facultatif : pour spécifier comment traduire la clause TVA, sélectionnez l'action **Traductions**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Pour affecter une clause TVA à un paramètre comptabilisation TVA
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramètres compta. TVA**, puis sélectionnez le lien associé.  
2. Dans la colonne **Clause TVA**, choisissez la clause à utiliser pour chaque paramètre comptabilisation TVA auquel elle s'applique.  

### <a name="to-specify-translations-for-vat-clauses"></a>Pour spécifier des traductions pour les clauses TVA
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Clauses TVA**, puis sélectionnez le lien associé.  
2. Sélectionnez l'option **Traductions**.  
3. Dans le champ **Code langue**, sélectionnez la langue de traduction.  
4. Dans les champs **Description** et **Description 2**, saisissez les traductions des descriptions. Ce texte s'affiche dans les documents état de TVA traduits.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Créer un paramètre comptabilisation TVA pour traiter la TVA à l'importation
Utilisez la fonction TVA à l'importation pour valider un document dont le montant est en TVA. Elle est utile lorsque vous recevez une facture des autorités fiscales pour la TVA sur les biens importés.  
  
Pour configurer des codes pour la TVA à l'importation, procédez comme suit :  
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Groupe compta. produit TVA**, puis sélectionnez le lien associé.  
2. Sur la page Groupes compta. produit TVA, configurez un groupe comptabilisation produit TVA pour la TVA à l'importation.  
3. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramètres compta. TVA**, puis sélectionnez le lien associé.  
4. Sur la page Paramètres compta. TVA, créez une ligne ou utilisez l'un des groupes comptabilisation marché TVA existants en combinaison avec le nouveau groupe comptabilisation produit TVA créé pour la TVA à l'importation.  
5. Dans le champ **Mode calcul TVA**, sélectionnez **Exclusivement TVA**.  
6. Dans le champ **Compte TVA achat**, indiquez le compte général à utiliser pour valider la TVA à l'importation. Tous les autres comptes sont facultatifs.  
  
## <a name="verify-vat-registration-numbers"></a>Vérifier les numéros d'identification TVA
Il est important que les numéros d'identification TVA des clients, fournisseurs et contacts soient valides. Par exemple, les sociétés modifient parfois leur statut d'assujettissement à la TVA, et dans certains pays, les autorités fiscales peuvent vous demander de fournir des états, tels que l'état Liste des ventes UE, qui répertorient les numéros d'identification TVA à utiliser lorsque vous faites des affaires.  
  
La Commission européenne fournit le service VIES de validation des numéros TVA sur son site Web, qui est public et gratuit. Toutefois, cela nécessite d'accéder au site Web. [!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet de supprimer cette étape et d'utiliser le service VIES pour valider et suivre les numéros de TVA des clients, fournisseurs et contacts directement à partir des fiches client, fournisseur et contact. Le service dans [!INCLUDE[d365fin](includes/d365fin_md.md)] est appelé Identification TVA UE. N° Service de validation. Il est disponible sur la page **Connexions au service**, et vous pouvez commencer à l'utiliser en activant une case à cocher. Le service est gratuit, et l'inscription n'est pas obligatoire.

Lorsque vous utilisez notre service, nous enregistrons un historique des numéros de TVA et des vérifications pour chaque client, fournisseur ou contact dans le **Journal identif. intracomm** pour faciliter le suivi. Le journal est spécifique à chaque client. Par exemple, le journal est utile pour prouver que vous avez vérifié que le numéro de TVA actuel est correct. Lorsque vous vérifiez un numéro de TVA, la colonne **Identificateur de demande** du journal indique que vous avez effectué des actions. 

Vous pouvez afficher le journal d'identification TVA sur les fiches client, fournisseur ou contact, sous le raccourci **Facturation**, en cliquant sur le bouton de recherche dans le champ **N° identif. intracomm.** .  

Notre service peut aussi vous faire gagner un peu de temps lorsque vous créez un client ou un fournisseur. Si vous connaissez le numéro de TVA du client, vous pouvez le saisir dans le champ **N° identif. intracomm.** des fiches client ou fournisseur, et nous compléterons le nom du client pour vous. Certains pays fournissent également les adresses de société dans un format structuré. Dans ces pays, nous compléterons aussi l'adresse.  

**Remarque** : voici quelques points à noter concernant le service VIES de validation de numéros de TVA :

* Le service utilise le protocole http, ce qui signifie que les données transférées via le service ne sont pas cryptées.
* Vous pouvez rencontrer des temps d'arrêt pour ce service dont Microsoft n'est pas responsable. Le service fait partie d'un vaste réseau de l'UE de registres de TVA nationaux.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Utilisation d'une TVA déductible pour le commerce entre pays/régions de l'UE
Certaines sociétés doivent utiliser une TVA déductible dans leurs échanges avec d'autres sociétés. Par exemple, cette règle s'applique aux achats effectués dans des pays/régions de l'Union européenne et les ventes aux pays/régions de l'Union européenne.

**Remarque** : cette règle s'applique aux échanges avec des sociétés enregistrées comme assujetties à la TVA dans un autre pays/région de l'UE. Si vous commercez directement avec des clients dans d'autres pays/régions de l'UE, nous vous recommandons de prendre contact avec votre administration fiscale afin d'obtenir des informations sur les règles applicables en matière de TVA.  

**Conseil** : vous pouvez vérifier qu'une société est enregistrée comme assujettie à la TVA dans un autre pays de l'UE en utilisant le service de validation des numéros d'identification de TVA de l'UE. Le service est disponible gratuitement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir la section _Vérifier les numéros d'identification TVA_ dans cette rubrique.

### <a name="sales-to-eu-countries-or-regions"></a>Ventes dans des pays/régions de l'UE
La TVA n'est pas calculée sur les ventes à des sociétés assujetties à la TVA situées dans d'autres pays/régions de l'UE. Vous devez déclarer la valeur de ces ventes séparément dans votre déclaration de TVA.
Pour calculer correctement la TVA sur les ventes effectuées dans des pays/régions de l'UE, vous devez procéder comme suit :  
  
* Configurez une ligne pour les ventes contenant les mêmes informations que pour les achats. Si vous avez déjà configuré des lignes dans la fenêtre Paramètres compta. TVA pour les achats effectués dans des pays/régions de l'UE, vous pouvez également utiliser ces lignes pour les ventes.  
* Affectez des groupes comptabilisation marché TVA dans le champ **Groupe compta. marché TVA** sur le raccourci **Facturation** de la fiche de chaque client de l'UE. Vous devez également saisir le numéro d'identification de TVA du client dans le champ **N° identif. intracomm.** du raccourci **International**.  

Lorsque vous validez une vente à un client situé dans un autre pays/une autre région de l'UE, le montant de TVA est calculé et une écriture TVA est créée à l'aide des informations sur la TVA déductible et la base TVA (montant utilisé pour calculer la TVA). Aucune écriture n'est validée dans les comptes TVA de la comptabilité.

## <a name="understanding-vat-rounding-for-documents"></a>Comprendre l'arrondi TVA pour les documents
Les montants figurant dans les documents qui n'ont pas encore été validés sont arrondis et affichés de façon à correspondre à l'arrondi final des montants réellement validés. La TVA est calculée pour un document terminé, ce qui signifie que la TVA calculée dans le document est basée sur la somme de toutes les lignes ayant le même identifiant TVA dans le document.

## <a name="see-also"></a>Voir aussi  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)
