<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/distribution_energie">Distribution Energie</a> --> [ChangeLog]

--------------------

# Journal des modifications

     
## 2023

### 26/04/2023 (23h40)
  - Correction d'une erreur sur les unités. (Merci @Bison)
  - Modification du paramètre optionnel GazUnit en GasUnit. (Merci @jpty)
  
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