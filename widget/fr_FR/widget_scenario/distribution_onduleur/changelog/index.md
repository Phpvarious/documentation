<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_onduleur">Distribution Onduleur</a> --> [ChangeLog]

--------------------

# Journal des modifications

## 2024
### 08/03/2024 (18h45)
- Widget
  - Nombre de pv illimité.
  - Nombre de load illimité.
  - Nouvelle info pouvant être affiché dans le lcd de l'onduleur (lcd_state).
  - Ajout de nouveaux icones 
    - tesla, water_heater (Merci @eyme2000)
  - Erreurs affichés dans le widget lorsqu'il est détecté une mauvaise config (unités différentes entre calculs)

### 25/03/2025 (18h30)
- Widget :
  - Restructuration du code.
  - Prise en compte de la puissance du "mppt battery" pour déterminer le sens du flux.
  - Les seuils d'alarme sont valables aussi pour "grid_power", "load_state", "aux_power", ainsi que les "load".
  - Il est possible maintenant de remplacer l'icone "battery" par un icon perso. (voir liste dans les load)
  - Ajout d'une info perso sur chaque "load". (load1_perso, load2_perso...)
  - Ajout d'une partie "tempo". (voir doc pour le fonctionnement)
  - Ajout de l'icone "ve".
- Ajout paramètres optionnels :
  - batteryIcone : Remplace l'icone de "battery" (Voir liste présente dans les "load").



### 30/01/2024 (23h30)
- Ajout paramètres optionnels :
  - Ajout de 5 nouvelles icones pour les loads (light, tv, server, laptop, console).
  - Ajout de seuils d'alarme sur tous les loads. Pour utiliser cette fonction veuillez renseigner les nouveaux paramètres ("load1MaxPower", "load2MaxPower" ...), si la puissance du load atteind la valeur renseigné dans ce paramètre, le rectangle sera colorisé en rouge (ou la couleur de son choix renseigné dans le paramètre "colorDanger"), il est aussi possible de faire clignoter le rectangle en mettant le paramètre "blink" a 1.

  Merci @bison pour les seuils.

### 29/01/2024 (21h40)
- Ajout paramètres optionnels :
  - Ajout de 5 nouvelles icones pour les loads (microwave, toaster, fridge, coffee, hood).

### 29/01/2024 (19h30)
- Widget :
  - Ajout de 4 nouveaux load (load5_state, load6_state, load7_state, load8_state) ainsi que les energy (load5_energy, load6_energy, load7_energy, load8_energy).
  - Possibilité d’ajouter sa propre valeur du calcul des Pv (pv_power).
- Ajout paramètres optionnels :
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