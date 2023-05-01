<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_energie">Distribution Energie</a> --> [ChangeLog]

--------------------

# Journal des modifications

     
## 2023
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