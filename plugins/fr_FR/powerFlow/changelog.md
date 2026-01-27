# Changelog plugin powerFlow

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 27/01/2026

> Béta vers stable

### Amélioration

- Toutes les commandes "power" sont automatiquement converties en W pour simplifier les calculs et éviter les erreurs d'unités.
- Tous les "power" passent par une conversion d'unité (comme le core).<br><i>1000 W -> affichera 1 kW.</i>
- Possibilité de réorganiser les "persos" (Sortable).
- Contrôle des liens morts (deadCmd) visible depuis la page Analyse > Equipements > Commandes orphelines.
- Utilisation d'une variable dans tous les champs "Max"  (Utilisez le bouton pour rechercher une variable).
- Possibilité de désactiver les conversions des unités.
- Choix du nombre de décimales après la virgule.
- Désormais, tous les "power" bénéficient :
  - Max : permet la gestion des gauges.
  - Alerte : permet la gestion des alertes en fonction de la puissance.
- Possibilté de dupliquer un équipement.
- Possibilité d'ajouter des éléments vides (fantôme) dans les récepteurs et les Pvs.<br>Il suffit simplement d'ajouter un élément (Activer) sans commande de puissance.
- Il est désormait possible de changer les couleurs des catégories depuis la commande ```Changement couleur``` disponible dans le plugin, celle-ci modifiera la couleur configurée.<br>Cette nouvelle commande permet de modifier en direct (via scénario par ex.) les couleurs sans avoir besoin de rafraichir le widget, ni même modifier dans le plugin.<br>

  >**IMPORTANT**
  >
  > Si vous utilisez cette nouvelle commande plusieurs fois dans un même scénario, veuillez à inserer une tempo (sleep) entre chaque execution.
  
- ajout d'un trim pour supprimer les espaces dans les unités, ce qui permet de continuer a échapper a la conversion des unités du core pour la commande d’origine tout en gardant la compatibilité pour le plugin.

### Bugfix

- La couleur du "power total" suit désormait la couleur paramètré dans le plugin (Couleur si valeur = 0 ou Masquer si valeur = 0)<br>
<i>(Sauf si vous utilisez la commande de puissance totale instantanée)</i>
- Ajout d'un "min" de 7px pour les tailles des textes dans les "persos".
- Unité des daily load Kwh ->  Wh.
- Alerte sur les récepteurs a l'initialisation.
- Décimales sur daily buy et daily sell du réseau.
- unité par défaut dans les calculs (récepteurs et solaires)
- Décimales sur les persos.
- Ajout uid pour utilisation multiple dans un scénario.

# 11/06/2025

- Présentation officielle.