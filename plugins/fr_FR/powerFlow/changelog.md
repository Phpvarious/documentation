# Changelog plugin powerFlow

>**IMPORTANT**
>
>Pour rappel, s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement la mise à jour de documentation, de traduction ou de texte.

# 26/02/2026

### Améliorations

- Refresh automatique du widget après sauvegarde de l'équipement.
- Ajout d'une option permettant de prendre en compte la puissance du mppt dans le calcul du temps de charge/décharge.
- Modification des seuils pour affichage de l'icône batterie :
  -  % < 25 --> 0 barre (vide)
  - 25 <= % < 50 --> 1 barre
  - 50 <= % < 75 --> 2 barres
  - 75 <= % < 100 --> 3 barres
  - % = 100 --> 4 barres (pleine)
- Modification des seuils pour affichage de la couleur de la batterie (même principe que ci-dessus).

  ### Corrections de bugs
  - Correction d'une erreur js lors d'utilisation de simple quote (`'`) dans les textes des éléments de catégorie "Perso".

# 27/01/2026

> Passage de la version bêta vers stable.

### Améliorations

- Toutes les commandes de ***puissance*** sont automatiquement converties en W pour afin d'unifier les calculs et éviter les erreurs d'unités.
- Toutes les valeurs de "puissance" passent par une conversion d'unité (comportement identique du core Jeedom).
  - *1000 W -> affiche 1 kW.*
- Possibilité de réorganiser les éléments personnalisés (glisser-déposer).
- Détection des **commandes orphelines** (`deadCmd`) accessible depuis **Analyse > Equipements > Commandes orphelines**.
- Utilisation possible d'une **variable Jeedom** dans tous les champs `Max` (sélecteur via bouton).
- Option permettant de désactiver les conversions automatiques d'unités.
- Paramètrage du nombre de décimales à afficher.
- Tous les éléments de "puissance" disposent désormais de :
  - **Max** : gestion des jauges.
  - **Alerte** : gestion des alertes basées sur la puissance.
- Possibilté de dupliquer un équipement.
- Possibilité d'ajouter des éléments vides (fantômes) dans les ***récepteurs*** et les équipements ***solaires*** 
  - Ajoutez simplement un élément vide (sans commande de puissance) et activé.
- Ajout d'une commande ```Changement couleur``` permettant de modifier dynamiquement la couleurs de chaque catégorie.
  - Cette commande est utilisable via scénario sans rechargement du widget ni modification dans le plugin

  >**IMPORTANT**
  >
  > Si vous utilisez cette nouvelle commande plusieurs fois dans un même scénario, veuillez à inserer une tempo (sleep) entre chaque execution.
  
- Ajout d'un `trim` sur les unités afin de supprimer les espaces, ce qui permet de continuer a échapper à la conversion des unités du core pour la commande d’origine (pour ceux qui utilise ce moyen de contournement) tout en gardant la compatibilité avec le plugin.

### Corrections de bugs

- La couleur de la **puissance totale** de la catégorie "solaire" respecte désormais la couleur configurée dans le plugin (`Couleur si valeur = 0` ou `Masquer si valeur = 0`)<br>
*(Exception :  si vous utilisez la commande de puissance totale instantanée)*
- Taille minimale des textes des éléments personnalisés fixée a `7px`.
- Correction des alertes sur les récepteurs à l'initialisation du widget.
- Correction sur l'affichage des décimales sur les **énergie vente** et **énergie achat** du réseau ainsi que pour les éléments **personnalisés**.
- Correction de l'unité par défaut dans les calculs (récepteurs et solaires).
- Ajout d'un **uid** pour permettre une utilisation multiple dans les scénarios.

# 11/06/2025

- Présentation officielle.