# Changelog plugin powerFlow

>**IMPORTANT**
>
>Pour rappel, s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement la mise à jour de documentation, de traduction ou de texte.

# 27/01/2026

> Passage de la version bêta vers stable.

### **Améliorations**

- Toutes les commandes "power" sont automatiquement converties en W pour simplifier les calculs et éviter les erreurs d'unités.
- Toutes les valeurs "power" passent par une conversion d'unité (comme dans le core).
  - 1000 W -> affichera 1 kW.
- Possibilité de réorganiser les éléments "perso" (sortable).
- Contrôle des liens morts (deadCmd) visible depuis la page **Analyse > Equipements > Commandes orphelines**.
- Possible d'utiliser une variable dans tous les champs `Max` (Utilisez le bouton prévu pour rechercher une variable).
- Possibilité de désactiver les conversions d'unités.
- Choix du nombre de décimales après la virgule.
- Désormais, tous les éléments "power" bénéficient :
  - Max : permet la gestion des gauges.
  - Alerte : permet la gestion des alertes en fonction de la puissance.
- Possibilté de dupliquer un équipement.
- Possibilité d'ajouter des éléments vides (fantômes) dans les récepteurs et les Pvs - Il suffit simplement d'ajouter un élément (Activer) sans commande de puissance.
- Il est désormais possible de changer les couleurs des catégories depuis la commande ```Changement couleur``` disponible dans le plugin.<br>
Cette nouvelle commande permet de modifier en direct (via scénario par ex.) les couleurs des catégories sans avoir besoin de rafraîchir le widget ni de modifier dans le plugin.

  >**IMPORTANT**
  >
  > Si vous utilisez cette nouvelle commande plusieurs fois dans un même scénario, veuillez à inserer une tempo (sleep) entre chaque execution.
  
- Ajout d'un `trim` pour supprimer les espaces dans les unités, ce qui permet de continuer a échapper à la conversion des unités du core pour la commande d’origine tout en gardant la compatibilité avec le plugin.

### **Corrections de bugs**

- La couleur du "power total" suit désormais la couleur paramètrée dans le plugin (`Couleur si valeur = 0` ou `Masquer si valeur = 0`)<br>
*(Sauf si vous utilisez la commande de puissance totale instantanée.)*
- Ajout d'un minimum de `7px` pour les tailles des textes des éléments "persos".
- Unité des **daily load** : Kwh ->  Wh.
- Alerte sur les récepteurs à l'initialisation du widget.
- Décimales sur **daily buy** et **daily sell** du réseau.
- Unité par défaut dans les calculs (récepteurs et solaires).
- Décimales sur les éléments "persos".
- Ajout d'un **uid** pour permettre une utilisation multiple dans un scénario.

# 11/06/2025

- Présentation officielle.