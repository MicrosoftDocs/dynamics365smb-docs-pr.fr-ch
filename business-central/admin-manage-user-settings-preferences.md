---
title: Gérez les paramètres et les préférences de l’utilisateur dans Dynamics 365 Business Central
description: Gérez les paramètres et les préférences de l’utilisateur dans Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 25b3c8a795c1a3f9d08ae0971da88b78e4d29b25
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752590"
---
# <a name="manage-user-settings-and-preferences"></a>Gérer les paramètres et les préférences de l’utilisateur

En tant qu’administrateur, vous pouvez définir les paramètres utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)], semblable à la façon dont les utilisateurs individuels peuvent gérer leurs propres préférences sur la page **Mes paramètres**.  

## <a name="types-of-user-settings"></a>Types de paramètres utilisateur

*Paramètres utilisateur* n’est pas la même chose que *configuration utilisateur*, qui concerne l’utilisateur en tant qu’entité et l’accès de l’utilisateur dans le système. En outre, les paramètres utilisateur n’ont rien à voir avec la personnalisation d’un utilisateur, comme les modifications légères de l’interface utilisateur. Les paramètres utilisateur déterminent les préférences de l’utilisateur dans divers aspects de la façon dont l’application se présente à l’utilisateur. Le paragraphe suivant répertorie les cinq types de paramètres et préférences de l’utilisateur qui peuvent être définis par l’individu ou de manière centralisée par l’administrateur :

- **Société**  

  Ce paramètre détermine la société à laquelle se connecter lors de la prochaine connexion. Un utilisateur peut avoir accès à plusieurs sociétés et peut être actif dans plusieurs sociétés.

- **Profil (rôles)**  

  Le profil décrit la fonction de l’utilisateur dans la société, comme *Directeur commercial*, *Comptable*, ou *Agent d’achat*. Le profil détermine ensuite le tableau de bord de l’utilisateur, la page d’accueil que les utilisateurs verront lorsqu’ils se connecteront. Le profil n’a pas d’impact sur les droits d’accès aux fonctionnalités de [!INCLUDE[prod_short](includes/prod_short.md)].  

- **ID de paramètres régionaux**  

  Définit la façon dont les dates et les nombres sont présentés dans le client [!INCLUDE[prod_short](includes/prod_short.md)], par exemple s’il faut utiliser des formats de date européen ou américain, ou comment afficher le signe décimal et le séparateur des milliers dans les montants. Si les utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] sont synchronisés à partir de Microsoft 365, les paramètres régionaux de Microsoft 365 sont utilisés, en supposant que l’utilisateur souhaite utiliser les mêmes paramètres dans les produits Office et [!INCLUDE[prod_short](includes/prod_short.md)]. Un administrateur ou un utilisateur peut modifier ces paramètres manuellement dans [!INCLUDE[prod_short](includes/prod_short.md)], mais ils seront réinitialisés à la valeur de Microsoft 365 une fois la prochaine synchronisation effectuée.

- **Langue**  

  Définit la langue d’application dans laquelle [!INCLUDE[prod_short](includes/prod_short.md)] présente du texte, des légendes et des messages d’erreur. Si les utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] sont synchronisés à partir de Microsoft 365, les paramètres de langue de Microsoft 365 sont utilisés, en supposant que l’utilisateur souhaite utiliser les mêmes paramètres dans les produits Office et [!INCLUDE[prod_short](includes/prod_short.md)]. Un administrateur ou un utilisateur peut modifier ces paramètres manuellement dans [!INCLUDE[prod_short](includes/prod_short.md)], mais ils seront réinitialisés à la valeur de Microsoft 365 une fois la prochaine synchronisation effectuée.

  Si le paramètre de langue de Microsoft 365 correspond à une langue prise en charge dans [!INCLUDE[prod_short](includes/prod_short.md)], cette langue sera choisie pour l’utilisateur.  

  > [!NOTE]
  > Vous devrez peut-être installer une application de langue pour que [!INCLUDE[prod_short](includes/prod_short.md)] affiche correctement la langue. Par conséquent, il est recommandé d’installer les applications de langue nécessaires avant qu’un utilisateur ne se connecte pour la première fois afin qu’il ait une bonne expérience dès le premier jour. Pour plus d’informations, consultez la liste des [langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Fuseau horaire**  

  Définit le fuseau horaire dans lequel se trouve l’utilisateur. Actuellement, ce n’est pas synchronisé à partir de Microsoft 365 et doit être réglé manuellement.  

> [!NOTE]
> Si une synchronisation des utilisateurs Microsoft 365 est effectuée pendant que les utilisateurs sont connectés à [!INCLUDE[prod_short](includes/prod_short.md)], ces utilisateurs doivent actualiser le navigateur ou se déconnecter et se reconnecter à [!INCLUDE[prod_short](includes/prod_short.md)] pour voir une langue potentiellement différente définie par l’action de synchronisation.

## <a name="overview-of-all-user-settings"></a>Aperçu de tous les paramètres utilisateur

Les administrateurs ont la possibilité de définir ou de modifier ces paramètres pour les utilisateurs de chaque société. Cela se fait sur la page **Personnalisations utilisateur**. Les enregistrements sur cette page refléteront les choix de l’utilisateur individuel pour les paramètres ci-dessus, un enregistrement par utilisateur. Lorsque les utilisateurs modifient leurs paramètres sur la page **Mes paramètres**, ces changements seront reflétés dans la liste **Personnalisations utilisateur**. Les administrateurs peuvent également définir ces paramètres pour les utilisateurs avant qu’ils ne se connectent pour la première fois, afin que les utilisateurs n’aient pas à le faire eux-mêmes, ce qui leur offre une meilleure expérience de *mise en route*.

> [!NOTE]
> Les personnalisations utilisateur n’ont rien à voir avec les modifications légères *personnelles* qu’un utilisateur peut apporter à l’expérience utilisateur.

## <a name="to-review-or-make-changes-to-user-settings"></a>Pour consulter ou modifier les paramètres utilisateur

1. Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Personnalisations utilisateur**, puis sélectionnez le lien associé.
2. Cela montre la liste des utilisateurs et leurs paramètres. Pour modifier les paramètres d’un utilisateur, cliquez sur l’**ID utilisateur** ou choisissez **Gérer** puis **Modifier**.
3. La carte **Personnalisation utilisateur** pour les paramètres spécifiques de l’utilisateur s’affiche et les modifications souhaitées peuvent être apportées.  

## <a name="see-also"></a>Voir aussi

[Mise en route](product-get-started.md)  
[Disponibilité par pays/région et langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Modification de la langue et des paramètres régionaux](about-locale-language.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]