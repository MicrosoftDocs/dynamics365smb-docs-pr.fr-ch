---
title: "Procédure : travailler sur des tâches service | Microsoft Docs"
description: "Après avoir créé une commande ou devis service, enregistré des lignes article de service, et affecté des ressources aux articles de service de la commande ou du devis, vous pouvez commencer la réparation et la maintenance des articles de service."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1e6db49370a1fc2d9a2bb99e55d00ed69908d703
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="work-on-service-tasks"></a>Travailler sur des tâches service
Après avoir créé une commande ou devis service, enregistré des lignes article de service, et affecté des ressources aux articles de service de la commande ou du devis, vous pouvez commencer la réparation et la maintenance des articles de service.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inclut une fenêtre **Tâches service** qui offre un aperçu de tous les articles de service nécessitant une attention particulière. Considérez-le comme votre tableau de bord de service : où vous pouvez consulter les commandes en attente, recherchez et enregistrez les pièces de rechange et mettez votre stock à jour.  
  
Pour assurer le suivi des modifications et obtenir une vue graphique de vos activités de service, utilisez les outils de statistiques de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour obtenir des diagrammes et analyses rapides générés automatiquement.  
  
## <a name="to-work-on-a-service-task"></a>Pour travailler sur une tâche service  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Tâches service**, puis sélectionnez le lien connexe. 
2. Pour obtenir la liste des tâches service auxquelles une ressource ou un groupe de ressources est affecté, renseignez le champ **Filtre ressources** ou **Filtre groupe ressources** et appuyez sur Entrée.  
3. Pour obtenir la liste des tâches service ayant certaines dates réponse sur une période de temps donnée, renseignez le champ **Filtre date réponse** et appuyez sur Entrée.  
4. Pour obtenir la liste des tâches service ayant un certain état affectation ou réparation, renseignez le champ **Filtre état affectation** ou **Filtre code état réparation** et appuyez sur Entrée.  
5. Sélectionnez la tâche service que vous souhaitez utiliser. Sous l'onglet **Naviguer**, dans le groupe **Tâches service**, choisissez **Feuille activité article**. La fenêtre **Feuille activité article de service** s'ouvre.  
6. Enregistrez les textes standard, les pièces de rechange, les heures ressource et les coûts à l'aide des options correspondantes dans le champ **Type** : <Blank>, **Article**, **Ressource** et **Coût**.  
7. Dans le champ **Statut réparation**, sélectionnez le statut approprié.  
  
   > [!NOTE]  
   >  Renseignez le champ **État de la réparation** en indiquant le statut **Terminé** ou **Service en partie réalisé** si la maintenance de l'article de service est terminée ou si une autre ressource est encore en service. Le programme sélectionne automatiquement le statut **Terminé** ou **Réaffectation nécessaire** pour l'écriture affectation correspondant à l'article de service.  

## <a name="to-register-service-operations"></a>Pour enregistrer des opérations de service  
Lors de l'exécution d'un service sur une commande service, vous pouvez enregistrer les détails spécifiant les articles utilisés, les coûts exposés et le temps passé. Les données que vous spécifiez sont stockées dans la fenêtre **Feuille activité article de service**. Vous pouvez mettre à jour les données si nécessaire. 
   
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Commandes service**, puis sélectionnez le lien connexe.  
2. Ouvrez la commande service pour laquelle vous voulez enregistrer le service, puis choisissez la ligne article.  
3. Choisissez **Actions**, sélectionnez **Ligne**, puis **Feuille activité article de service**.  
4. Dans les lignes, spécifiez les articles utilisés, les coûts exposés et le temps passé au service.  
  
   > [!NOTE]  
   >  Vous pouvez également enregistrer un service directement dans les lignes service liées à la commande service.  
  
## <a name="to-register-spare-parts"></a>Pour enregistrer les pièces de rechange  
Lorsque vous travaillez sur des articles de service de commandes service, vous pouvez être amené à utiliser des pièces de rechange pour la maintenance. La procédure suivante vous montre comment enregistrer les pièces de rechange utilisées dans la fenêtre **Feuille activité article de service**.  
  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Tâches service**, puis sélectionnez le lien connexe. 
2. Choisissez la ligne comprenant l'article de service approprié, puis sélectionnez l'action **Feuille activité article**.  
3. Entrez une nouvelle ligne service.  
4. Dans le champ **Type**, choisissez **Article**.  
5. Dans le champ **N°**, choisissez la pièce de rechange appropriée.  
6. Dans le champ **Quantité**, saisissez la quantité d'articles que vous souhaitez utiliser.  
  
 Vous pouvez utiliser une procédure similaire pour enregistrer les pièces de rechange dans la page **Lignes service** que vous pouvez ouvrir dans la page **Commande de service**.  
  
## <a name="to-register-spare-parts-from-a-service-order"></a>Pour enregistrer des pièces de rechange à partir d'une commande service  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Commandes service**, puis sélectionnez le lien connexe.  
2. Ouvrez la commande service pour laquelle vous voulez enregistrer des pièces de rechange.  
3. Choisissez la ligne comportant l'article de service approprié. Sélectionnez **Actions**, **Commande**, puis **Lignes service**.  
4. Entrez une nouvelle ligne service.  
  
## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Pour remplacer un article de service ou un composant article de service  
La maintenance d'un article de service constitué de plusieurs composants peut nécessiter le remplacement d'un composant défectueux. Chaque fois que vous saisissez une pièce de rechange pour un article de service constitué de plusieurs composants, vous pouvez remplacer un composant ou en créer un nouveau. Le nouvel article n'est enregistré comme composant de l'article de service qu'après validation de cette ligne service ou de la commande service. 
    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Tâches service**, puis sélectionnez le lien connexe. 
2. Choisissez la ligne comprenant l'article de service, puis sélectionnez l'action **Feuille activité article**.  
3. Entrez une nouvelle ligne service.  
4. Dans le champ **Type**, choisissez **Article**.  
5. Dans le champ **N°**, le champ, sélectionnez le composant à remplacer.  
6. Appuyez sur **Entrée**. La boîte de dialogue qui s'ouvre contient les trois champs suivants : **Remplacer composant**, **Nouveau composant** et **Ignorer**. Le tableau suivant décrit les options.  
  
    |Option | Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Remplacement composant**|Fait passer le statut du composant que vous remplacez sur inactif et le composant s'affiche dans la liste des composants remplacés de l'article de service.|  
    |**Nouveau composant**|Insère le nouveau composant dans la liste des composants de l'article de service.|  
    |**ignorer**|N'apporte aucune modification à la liste des composants de l'article de service.|  
  
7. Cliquez sur **Remplacer composant**.  
8. Choisissez le composant à remplacer, puis choisissez **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Pour modifier le délai de réponse pour une ligne article de service  
Lorsque vous enregistrez des lignes article de service dans une commande ou un devis service, selon que l'article de service se trouve sur un contrat de service, le temps de réponse en heures est automatiquement saisi et la date et l'heure de réponse sont calculées en conséquence. Vous pouvez modifier le délai de réponse en heures, la date et le délai de réponse, si nécessaire.  

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes service** ou **Devis services**, puis choisissez le lien associé.  
2. Choisissez la commande ou le devis service pour ouvrir la fiche.  
3. Sur la ligne d'élément de service pour lequel vous souhaitez modifier le temps de réponse, dans le champ **Délai de réponse (heures)**, ou dans les champs **Date de réponse** et **Délai de réponse**, saisissez les nouvelles heures de réponse ou la date et le délai de réponse souhaités.  

## <a name="to-register-faultresolution-codes"></a>Pour enregistrer des codes panne/solution  
Après avoir réparé un article de service, vous pouvez enregistrer le code panne et le code solution de l'article en sélectionnant une combinaison à partir des relations codes panne/solution existantes. Les codes panne et solution s'affichent dans les champs correspondants de la fenêtre **Feuille activité article de service**. Vous pouvez également enregistrer les codes dans cette fenêtre.  
    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Tâches service**, puis sélectionnez le lien connexe. 
2. Choisissez la ligne comprenant l'article de service approprié, puis sélectionnez l'action **Feuille activité article**.  
3. Sur la page **Feuille activité article de service**, sélectionnez **Relations codes panne/solution**. La fenêtre **Relations codes panne/solution** s'ouvre.  
  
  >  [!Note]
  >  Des filtres sont automatiquement positionnés sur les relations affichées dans la fenêtre en copiant le groupe articles de service et les codes panne de la fenêtre **Feuille activité article de service**.  
  
4. Renseignez la ligne complètement. Choisissez la combinaison de codes panne/solution, puis choisissez **OK** pour la copier sur l'article de service. Si une combinaison appropriée est introuvable, vous pouvez créer une combinaison dans la fenêtre.  

## <a name="see-also"></a>Voir aussi  
[Configurer le reporting panne](service-how-setup-fault-reporting.md)
[Statut affectation et statut réparation](service-allocation-status-and-repair-status.md)  
[Validation de service](service-service-posting.md)  


