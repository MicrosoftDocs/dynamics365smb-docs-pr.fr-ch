---
author: brentholtorf
ms.topic: include
ms.date: 02/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Vous pouvez utiliser des relances pour rappeler aux clients les soldes échus. Vous pouvez également utiliser les relances pour calculer les intérêts de retard tels que les intérêts ou les frais et les inclure dans la relance.

Avant de pouvoir créer des relances, vous devez configurer des conditions relance et les affecter à vos clients. Pour plus d’informations, voir [Configurer les conditions et niveaux de relance](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Le contenu de la page **Conditions intérêts de retard** détermine si les intérêts sont calculés dans la relance.  

Vous pouvez exécuter périodiquement le traitement par lots **Création de relances** afin de créer des relances pour tous les clients ayant des soldes échus. Vous pouvez également créer manuellement une relance pour un client spécifique et demander à ce que les lignes soient calculées et renseignées automatiquement.  

Une fois que vous avez créé les relances, vous pouvez les modifier. Le texte apparaissant au début et à la fin de chaque relance est déterminé par les conditions niveau de relance de la colonne **Désignation**. Si un montant calculé a été inséré automatiquement dans le texte de début ou de fin, ce texte ne sera pas ajusté si vous supprimez des lignes. Vous devez alors utiliser la fonction **Mettre à jour texte relance**.  

Une écriture comptable client pour laquelle le champ **En attente** est renseigné ne génèrera pas la création d’une relance. Néanmoins, si une relance est créée à partir d’une autre écriture, une écriture échue en attente d’approbation est incluse dans la relance. Les intérêts ne sont pas calculés sur les lignes avec ces écritures.

Après avoir créé les relances et effectué toutes les modifications souhaitées, vous pouvez lancer les impressions test ou émettre les relances, en général par e-mail.

### <a name="to-create-a-reminder-automatically"></a>Pour créer automatiquement une relance

Une relance est identique à une facture. Lorsque vous créez une relance, un en-tête relance, ainsi qu’une ou plusieurs lignes relance, doivent être renseignés. Vous pouvez utiliser une fonction pour créer des relances pour tous les clients automatiquement.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 0.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Relances**, puis sélectionnez le lien associé.
2. Sur la page **Relance**, cliquez sur l’action **Créer relance**.
3. Sur la page **Créer relances**, renseignez les champs pour définir comment et pour qui les relances sont créées.
4. Choisissez le bouton **OK**.

### <a name="to-create-a-reminder-manually"></a>Pour créer une relance manuellement

Sur la page **Relance**, vous pouvez renseigner le raccourci **Général** manuellement et ensuite renseigner les lignes automatiquement.

1. Sélectionnez l’icône en forme ![d’ampoule qui rouvre la fonction Tell Me 2.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Relances**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire.
4. Choisissez l’action **Proposer lignes relance**.
5. Dans le traitement par lots **Proposer lignes relance**, renseignez les champs pour définir comment et pour qui les relances sont créées.
6. Activez la case à cocher **Inclure les écritures en attente** si vous souhaitez que les relances contiennent des écritures ouvertes impayées qui sont en attente.
7. Activez la case à cocher **Seulement écritures dont l’échéance est dépassée** si vous souhaitez que les relances contiennent uniquement des écritures ouvertes impayées qui sont en attente. Seuls les factures et les paiements seront affichés car ce sont les écritures pour lesquelles les paiements de vos clients peuvent être en retard.

    > [!Important]
    > Les écritures ouvertes en attente sont insérées, indépendamment du paramètre de la case à cocher **Seulement écritures dont l’échéance est dépassée**.

8. Cliquez sur le bouton **OK**.

### <a name="to-replace-reminder-texts"></a>Pour remplacer les textes relance

Vous pouvez déterminer de plusieurs manières le texte devant figurer sur la relance imprimée. Dans certains cas, vous pouvez remplacer les textes début et fin définis pour le niveau actuel par ceux d’un autre niveau.

1. Sélectionnez l’icône en forme ![d’ampoule qui rouvre encore la fonction Tell Me 3.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Relances**, puis sélectionnez le lien associé.
2. Ouvrez la relance appropriée, puis cliquez sur l’action **Mettre à jour texte relance**.
3. Sur la page **Mettre à jour texte relance**, entrez le niveau requis dans le champ **Niveau relance**.
4. Cliquez sur le bouton **OK** pour que le programme mette à jour les textes début et fin.

### <a name="to-issue-a-reminder"></a>Pour émettre une relance

Après avoir créé les relances et effectué toutes les modifications souhaitées, vous pouvez lancer les impressions test ou émettre les relances.

Lorsque vous émettez une relance, les données sont transférées dans une page séparée pour les relances émises. Les écritures relance sont simultanément validées. Si des intérêts ou des frais supplémentaires ont été calculés, les écritures sont validées dans les écritures client et dans la comptabilité.

Lorsqu’une relance est émise, les écritures sont validées selon les spécifications de la page **Conditions de relance**. Cette spécification détermine si les intérêts et les frais supplémentaires sont validés sur le compte client et dans la comptabilité. La configuration sur la page **Groupes compta. client** détermine les comptes qui seront utilisés.

Pour chaque écriture comptable client de la facture d’intérêts, une écriture est créée sur la page **Ecr. relance/fact. intérêts**.

Si les cases à cocher **Comptabiliser intérêts** ou le champ **Compta. frais supplémentaires** de la page **Conditions de relance** sont activées, les écritures suivantes sont aussi créées :

- Une écriture sur la page **Écritures comptables client**,
- Une écriture client sur le compte général approprié,
- Une écriture intérêts et/ou une écriture frais supplémentaires sur le compte général approprié.

De plus, émettre une facture d’intérêts peut créer des écritures de TVA.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre ici aussi la fonction Tell Me 4.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Relances**, puis sélectionnez le lien associé.
2. Sélectionnez la relance concernée, puis cliquez sur l’action **Émission**.
3. Sur la page **Emettre relances**, renseignez les champs selon vos besoins.
4. Cliquez sur le bouton **OK**.

La relance est imprimée pour être envoyé à un e-mail spécifié en tant que document joint PDF.

### <a name="to-cancel-an-issued-reminder"></a>Pour annuler les relances émises

Si des relances ont été émises par erreur, vous pouvez les annuler avant leur envoi. Vous pouvez les annuler une par une ou par lots.

1. Sur la page **Relances émises**, sélectionnez une ou plusieurs lignes pour les relances émises que vous souhaitez annuler, puis choisissez l’action **Annuler**.
2. Sur la page **Annuler les relances émises**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.


