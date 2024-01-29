<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_onduleur">Distribution Onduleur</a> --> [ChangeLog]

--------------------

# Journal des modifications

## 2024     

### 29/01/2024 (xxhxx)
- Widget :
  - Ajout de 4 nouveaux load (load5_state, load6_state, load7_state, load8_state) ainsi que les energy (load5_energy, load6_energy, load7_energy, load8_energy).
  - Possibilité d’ajouter sa propre valeur du calcul des Pv (pv_power).
- Ajout paramètre optionnel :
  - Possibilité d’afficher un VE a la place de la batterie (batteryIconeVe).
  - Ajout de 6 nouvelles icones pour les loads (battery, plug, pool, dryer, dishwasher, washing).

## 2023

### 21/09/2023 (23h00)
- Widget :
  - Ajout 'aux_power' pour afficher un générateur auxiliaire.
  - daily_aux (energie du générateur).
  - battery_mppt_power pour afficher un Pv sur la batterie.
  - battery_mppt_energy pour afficher lénergie du Pv de la batterie.
- Ajout paramètre optionnel :
  - mpptName (nom du générateur auxiliaire)
  - auxColor (Couleur des éléments de catégorie "aux").
- Modification du visuel :
  - Modification onduleur.
  - deplacement V, A, Hz dans l'onduleur'.
  - déplacement des incones "Load" sur la droite.
  - Masque de la tuile "Load" si aucune commande n'est renseignée.
  - Masque de la tuile "Batterie" si aucune commande n'est renseignée.

### 17/09/2023 (16h00)
- Widget
  - Ajout de 2 "load" supplémentaires.
  - Possibilité d'afficher l'energie de chaque "load".
  - Possibilité d'afficher l'energie de chaque "pv".
  - Ajout d'animation sur les "load".
- Ajout paramètre optionnel :
  - loadAnimate qui permet de désactiver l'animation des "Load".
  - load3Icon (Choix icone a afficher).
  - load4Icon (Choix icone a afficher).
  - load3Name (Nom du Load3).
  - load4Name (Nom du Load3).

### 12/09/2023 (15h30)
- Ajout paramètre optionnel :
  - load1Icon (Choix icone a afficher).
  - load2Icon (Choix icone a afficher).
  - batterySocShutdown (SOC mini pour calcul de durée restante).
  - solarColor (Couleur des éléments de catégorie "solaire").
  - batteryColor (Couleur des éléments de catégorie "batterie").
  - gridColor (Couleur des éléments de catégorie "réseau").
  - inverterColor (Couleur des éléments de catégorie "onduleur").
  - loadColor (Couleur des éléments de catégorie "load").
  - noGridColor (Couleur du logo lorsque l'onduleur est déconnecté du réseau).
- Modification du visuel :
  - Diminution de taille des "pv_power" pour laisser place au nom (#pv1Name#) au dessus.
  - Affichage des "daily" avec 3 décimales max.
  - ajout des commandes :
    - pv1_voltage, pv2_voltage, pv3_voltage, pv4_voltage
    - pv1_current, pv2_current, pv3_current, pv4_current
- Bugfix :
  - Problème d’affichage quand Centrage vertical des tuiles est actif (verticalAlign).
  - Paramètres optionnels des daily n’accepte pas les '

### 09/09/2023 (v1)
  - Création.










-------------------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_onduleur">Distribution Onduleur</a> --> [ChangeLog]