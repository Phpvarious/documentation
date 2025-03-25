
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Distribution Onduleur

------------

# Widget [Onduleur Distribution] ![Generic badge](https://img.shields.io/badge/Version-4.3%20%7C%204.4%20Full%20JS-green.svg) ![Generic badge](https://img.shields.io/badge/status-stable-green.svg)

<center><img src="../../../images/distribution_onduleur/capture1_1.gif" width="500px" alt="Info backup" /></center>


> **Information**
>- Ce widget est basé sur le travail déja <a href="https://github.com/slipx06/sunsynk-power-flow-card" target="_blank">accomplie.</a>
>
> - Pour chaques éléments les unités des commandes doivent être identiques.
> 
> - Contrairement au widget <a href="../distribution_energie" target="_blank">Distribution Energie</a> ce widget fait moins de calculs.

## 1) Télécharger la source
> - <a href="{{site.url_git}}/WIDGET_cmd.info.string.distribution_onduleur" target="_blank">Télécharger la source du widget pour le Core V4</a>

### Version dashboard

- Déposer le fichier <b>cmd.info.string.onduleur_distribution</b> dans le dossier <b>/html/data/customTemplates/dashboard/</b>

  <img src="../../../images/distribution_onduleur/capture2.png" alt="Téléchargement du widget" />

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegarder (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre,(3, 4 et 5).

<img src="../../../images/distribution_onduleur/installation_virtuel1.png" alt="Virtuel 1" />
<img src="../../../images/distribution_onduleur/installation_virtuel2.png" alt="Virtuel 2" />


## Paramètres optionnels

<img src="../../../images/distribution_onduleur/parametres1.png" alt="Info backup" />

> **Information**
>
> - le paramètre optionnel batteryMaxPower permet , si il est renseigné, de calculer la durée restante / temps de charge.

## 3) Ajout des données

Ce widget utilise les commandes présentent dans ce même équipement.
Il faut donc utiliser des noms de commandes infos prédéfinis suivant les tableaux ci-dessous :

### Solaire

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_solar | non | Production solaire quotidienne |
| pv_power <font color="red">*</font> | non | Puissance instantanée Total |
| pv1_power | non | Puissance instantanée Pv1 |
| pv1_energy | non | Energie PV1 |
| pv1_voltage | non | Tension Pv1 |
| pv1_current | non | Intensité Pv1 |

> **Info**
>
> - Dans le tableau ci-dessus l'ajout de PV supplémentaires est infini, exemple pour un 2ème pv, utilisation de pv2_power...
> - Si vous possèdez 1 seul PV, utilisez avant tout pv1_power.
> - Si aucun des pv power n'est renseigné, la partie solaire sera automatiquement masqué.
> - pv_power <font color="red">*</font> : Si cette commande n'est pas existante, le widget affichera la somme des pv.

### Batterie

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| battery_state | non | Pourcentage de batterie. |
| battery_temp | non | Température de la batterie. |
| battery_voltage | non | Tension de la batterie. |
| battery_current | non | Intensité de la batterie. |
| battery_power | non | Puissance instantanée. (positive = décharge / négative = charge)|
| daily_battery_charge | non | Consommation de charge quotidienne. |
| daily_battery_discharge | non | Consommation de décharge quotidienne. |
| battery_mppt_power | non | Puissance instantanée du mppt de la batterie. |
| battery_mppt_energy | non | Consommation du mppt de la batterie. |

> **Info**
>
> - Si "battery_power" n'est renseigné, la partie "batterie" sera automatiquement masquée.
>

### Aux

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| aux_power | non | Puissance instantanée. |
| daily_aux | non | Production auxiliaire quotidienne. |

> **Info**
>
> - Si "aux_power" n'est renseigné, la partie "Aux" sera automatiquement masquée.
>

### Réseau

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_grid_buy | non | Consommation venant du réseau quotidienne. |
| daily_grid_sell | non | Injection au réseau quotidienne. |
| grid_power | non | Puissance instantanée. (positive = conso / négative = injection) |
| grid_status | non | État de connexion au réseau. (binaire)|

### Load

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_load | non | Consommation des équipements "Load" quotidien. |
| load_state | non | Puissance instantanée globale. |
| load1_power | non | Puissance instantanée du recepteur 1. |
| load1_energy | non | Energie recepteur 1. |
| load1_perso | non | Info perso du load1. |

> **Info**
> - Dans le tableau ci-dessus l'ajout de load supplémentaires est infini, exemple pour un 2ème load, utilisation de load2_power...
>
> - Si "load_state" et "loadx_state" ne sont pas renseignés, la partie "Load" sera automatiquement masquée.
>
> - Si load_state n'est pas défini, il sera alors calculé par addition de load1_state + load2_state + ...
>
>

### Onduleur

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| ac_temp | non | Température AC. |
| dc_temp | non | Température DC. |
| voltage_state | non | Tension de l'onduleur. |
| frequency_state | non | Fréquence de l'onduleur. |
| current_state | non | Intensité de l'onduleur. |
| lcd_state | non | Info a indiquer dans le lcd. |

## Exemple :

<img src="../../../images/distribution_onduleur/widget_help1.png" alt="Help1" />

> **Légende** : 
> <br><b>Noir :</b> Commandes a renseigner dans l'équipement.
> <br><font color="red"><b>Rouge :</b> Paramètres optionnels.</font>
>
> <b><font color="red">*</font> pv_power :</b> ci cette commande n'est pas existante, le widget affichera la somme des pv.

-------------------------

<img src="../../../images/distribution_onduleur/widget_help2.png" alt="Help2" />

## 3) Partie Tempo

### Avec le plugin "rteEcowatt"
- Affichage de la couleur du jour et du lendemain.

Il faudra télécharger le template <a href="{{site.url_git}}/WIDGET_cmd.info.string.distribution_onduleur" target="_blank">distribution_onduleur_tempo.json</a>.<br>
<i>Vous pouvez suivre <a href='../../../../help/fr_FR/template_scenario' target="_blank">l'aide a l'installation d'un template</a>.</i><br>

Commande de remplacement :

<img src="../../../images/distribution_onduleur/instal_template.png" alt="Help1" />

(1) Recherchez la commande sur laquelle vous avez appliqué le widget précédemment.<br>
(2) Appliquer la modification.


### Sans le plugin "rteEcowatt"
- Affichage seulement de la couleur du jour

Il suffit simplement d'envoyer une des couleurs (RED,WHITE ou BLUE) sur la commande ou vous avez appliqué le widget précédemment.

## 3) Icones dispo :

| ------ | ------ | ------ | ------ | ------ |
| <center>Four<br>(oven)<br><img src="../../../images/distribution_onduleur/svg/oven.svg" alt="oven" /> | <center>Pompe<br>(pump)<br><img src="../../../images/distribution_onduleur/svg/pump.svg" alt="pump" /> | <center>Clim<br>(aircon)<br><img src="../../../images/distribution_onduleur/svg/aircon.svg" alt="aircon" /> | <center>Chaudière<br>(boiler)<br><img src="../../../images/distribution_onduleur/svg/boiler.svg" alt="boiler" /> | <center>Chargeur<br>(charging)<br><img src="../../../images/distribution_onduleur/svg/charging.svg" alt="charging" /> |
| <center>Batterie<br>(battery)<br><img src="../../../images/distribution_onduleur/svg/battery.svg" alt="battery" /> | <center>Prise<br>(plug)<br><img src="../../../images/distribution_onduleur/svg/plug.svg" alt="plug" /> | <center>Piscine<br>(pool)<br><img src="../../../images/distribution_onduleur/svg/pool.svg" alt="pool" /> | <center>Sèche linge<br>(dryer)<br><img src="../../../images/distribution_onduleur/svg/dryer.svg" alt="dryer" /> | <center>Lave vaisselle<br>(dishwasher)<br><img src="../../../images/distribution_onduleur/svg/dishwasher.svg" alt="dishwasher" /> |
| <center>Machine a laver<br>(washing)<br><img src="../../../images/distribution_onduleur/svg/washing.svg" alt="washing" /> | <center>Micro-ondes<br>(microwave)<br><img src="../../../images/distribution_onduleur/svg/washing.svg" alt="microwave" /> | <center>Grille-pain<br>(toaster)<br><img src="../../../images/distribution_onduleur/svg/toaster.svg" alt="toaster" /> | <center>Réfrigérateur<br>(fridge)<br><img src="../../../images/distribution_onduleur/svg/fridge.svg" alt="fridge" /> | <center>Cafetière<br>(coffee)<br><img src="../../../images/distribution_onduleur/svg/coffee.svg" alt="coffee" /> |


## Changelog

<a href="./changelog">Changelog</a>


## Todo

- Affichage d'un greenPower.

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Distribution Onduleur
