<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_energie">Distribution Energie</a> --> [ChangeLog]

--------------------

# Journal des modifications

     
## 2023
### 02/06/2023 (22h00)
- Ajout d'une condition, pour eviter les erreurs lors de la navigation dans les design (gotoDesign).
- Ajout d'une condition, pour éviter que l'update (refreshValue) de la commande d'origine n'interfére avec l'update du widget.
### 02/06/2023 (16h00)
- Correction d'un bug sur valeur négative pour "Gas", "Water", "Perso1" et "Perso2". (Merci @Bison)

### 07/05/2023 (18h00)
- Correction (workaround) pour supprimer le "overflow: auto;" du core v4.4 qui tronquait le widget lors de l'utilisation de "Scale".
- Correction du "margin-top", celui-ci est désactivé lorsqu'on utilise "BorderWidth"
- Correction d'une erreur causé par "HideGreenValue" qui empechait le refresh des valeurs.
- Ajout d'un paramètre optionnel pour arrondir les valeurs individuellements.
- Tous les paramètres "xxxIcon" peuvent recevoir comme valeur "0", dans ce cas aucune icone ne sera affectée a "xxx".
- Suppression des paramètres "GasInverted" et "WaterInverted" qui a mon sens ne sont pas necessaires.

### 02/05/2023 (20h00)
- Ajout du paramètre optionnel "HideGreenValue" pour masquer le % d'énergie verte.
- Correction de "InvertedCircleWater" qui ne fonctionnait pas lorsque la tuile Gas était affichée.
- Ajout d'un "margin-top" pour remonter la position du widget.
- Ajout d'un "transform-origin: top" pour forcer la position du widget en haut de la tuile.(problème lors d'utilisation de "Scale").

### 01/05/2023 (18h00)
- Ajout de 2 nouvelles tuiles persos optionnelles.
- Masquage de la "ligne" battery <-> Grid.
- Ajout d'un nouveau paramètre pouvant faire clignoter la tuile "Grid" (exemple sur perte secteur).
- Possibilité de, masquer les "lignes" / "points", inverser le sens, sur tous les éléments perso, gaz et water.
- Ajout du % d'energie/consommation verte.
- Possibilité de modifier la taille des textes "Perso1", "Perso2", "Gaz", "Water" et "Solar" (tout ou rien)


### 29/04/2023 (11h00)
  - Update automatique des commandes
    - peux avoir un comportement anormale si les commandes d'origine sont affichées sur la même page que le widget (j'attend vos retours ;-)
  - Ajout d'un paramètre "Scale".
  - Les tuiles Gas et Water peuvent être renommées avec les paramètres optionnels "GasRename" et "WaterRename".
  - Les icones Gas et Water peuvent être personnalisées avec les paramètres optionnels "GasIcon" et "WaterIcon". 
  - Masquage des valeurs si égales à 0, paramètrable avec "HideIfEmpty" (@m.georgein)
  - Le code ayant totalement été réadapté pour l'update auto. il n'est plus possible de forcer le refresh par l'update de la commande du widget.

### 26/04/2023 (23h40)
  - Correction d'une erreur sur les unités. (Merci @Bison)
  - Renommage du paramètre optionnel "GazUnit" en "GasUnit". (Merci @jpty)

### 26/04/2023 (v1)
  - Unité automatique en fonction de l'équipement "Grid" ou "GridConsumption".
  - Ajout d'un paramètre optionnel pour l'unité. (prioritaire sur Unité automatique).
  - Ajout de conversion automatique des unités (2000W -> 2Kw).
  - Les valeurs "Grid" et "Battery" sont convertis en 2 décimales (pas d'arrondi).
  - Les autres valeurs sont convertis en 3 décimales (pas d'arrondi).
  - Ajout d'un nouveau paramètre optionnel "BatteryTemp" pour afficher la température de la batterie.

### 24/04/2023 (v1)
  - Ajout de l'affichage et calcul du ReturnToGrid (retour au réseau) si on utilise le paramètre “Grid”.

### 23/04/2023 (v1)
  - Création.









-------------------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_energie">Distribution Energie</a> --> [ChangeLog]