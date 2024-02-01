---
title: Configurer le reporting panne dans la gestion des services
description: 'Le reporting panne permet d’établir des normes d’enregistrement des informations de panne pour les articles de service avec les codes par défaut, etc.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-fault-reporting"></a>Configurer le reporting panne
Le reporting panne permet d’établir des normes d’enregistrement des informations de panne pour les articles de service. Par exemple, vous pouvez spécifier la nature du problème, les symptômes visibles, le motif du problème et la solution pour le résoudre.  

Les codes panne décrivent les pannes article de service courantes ou les actions effectuées au niveau des articles de service. En fonction du niveau de reporting panne de votre société, il peut être nécessaire de configurer les codes zone panne et symptôme avant les codes panne. Les zones panne décrivent les zones de pannes article de service. Les codes motif panne décrivent le motif des pannes article de service et, si nécessaire, indiquent si les remises garantie et contrat doivent être exclues. Par exemple, vous pouvez être amené à exclure les remises garantie et contrat si le client est responsable de la panne de l’article de service. Vous affectez des codes motif panne aux commandes service. Pour plus d’informations, voir [Travailler sur des tâches service](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting"></a>Pour spécifier le niveau global du reporting panne à utiliser
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres services**, puis choisissez le lien associé.
2. Dans le champ **Niveau reporting panne**, sélectionnez l’une des options décrites dans le tableau suivant.  

    |**Niveau de panne**|**Description**|  
    |------------|-------------|  
    |Aucun | Aucun code reporting n’est utilisé.|  
    |Panne | Les codes sont répertoriés dans la table **Codes panne**. Ils identifient les pannes d’articles de service ou les actions à effectuer sur ces dernières. Vous pouvez regrouper les codes associés en groupements **Code zone panne**.|  
    |Panne + Symptôme | Vous entrez une combinaison de codes dans les tables **Codes panne** et **Codes symptôme**. Les codes symptôme courants incluent des indicateurs qu’un client peut utiliser pour décrire un problème (bruit, qualité, etc).|  
    |Panne + Symptôme + Zone. | Vous utilisez les codes Panne, Symptôme et Zone panne dans le cadre de la mise en œuvre du système International Repair Coding System (IRIS).|  

Pour terminer la configuration du reporting panne, vous pouvez également spécifier les réparations ou solutions associées à une panne ou un défaut. Pour ce faire, utilisez la page **Relations codes panne/solution**, qui vous permet de configurer des combinaisons de codes pour le groupe d’articles de service de l’article de service à partir duquel vous accédez à la fenêtre, ainsi que le nombre d’occurrences de chacune d’elles.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Pour créer des relations codes panne/solution
<!--this needs to go in a working with topic-->
Pour pouvoir visualiser, lors de la maintenance des articles, les modes de réparation les plus courants se rapportant à des pannes article particulières, vous devez regrouper des informations sur les relations codes panne/solution. Utilisez le traitement par lots **Insérer relations codes P/S** pour rechercher toutes les combinaisons de codes panne/solution dans des commandes service validées et les enregistrer dans la page **Relations codes panne/solution**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Insérer relations codes PS**, puis sélectionnez le lien associé.  
2. Saisissez des dates pour définir la période à inclure dans le traitement par lots.  
3. Pour regrouper les relations par groupe d’articles de service, activez la case à cocher **Relations définies à partir des groupes articles de service**.  
4. Pour conserver les enregistrements que vous avez déjà insérés manuellement sur la page **Relations codes panne/solution**, activez la case à cocher **Conserver enreg. insérés manuellement**.  

## <a name="see-also"></a>Voir aussi
[Paramétrage de la gestion des services](service-setup-service.md)  
[Gestion des services](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
