# Changelog plugin powerFlow

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 03/06/2025

- Présentation officielle.

# 09/06/2025

### Amélioration

- Toutes les commandes "power" sont automatiquement converties en W pour simplifier les calculs et éviter les erreurs d'unités.
- Tous les "power" passent par une conversion d'unité (comme le core).<br><i>1000 W -> affichera 1 kW.</i>
- Possibilité de réorganiser les "persos" (Sortable).

### Bugfix

- La couleur du "power total" suit désormait la couleur paramètré dans le plugin (Couleur si valeur = 0 ou Masquer si valeur = 0)<br>
<i>(Sauf si vous utilisez la commande de puissance totale instantanée)</i>
- Ajout d'un "min" de 7px pour les tailles des textes dans les "persos".

# 12/06/2025

### Amélioration

- Contrôle des liens morts (deadCmd) visible depuis la page Analyse > Equipements > Commandes orphelines.

- Utilisation d'une variable dans tous les champs "Max"  (Utilisez le bouton pour rechercher une variable).

- Possibilité de désactiver les conversions des unités.

- Choix du nombre de décimales après la virgule.