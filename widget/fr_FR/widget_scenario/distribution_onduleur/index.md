
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Distribution Onduleur

------------

# Widget [Onduleur Distribution] ![Generic badge](https://img.shields.io/badge/Version-4.3%20%7C%204.4%20Full%20JS-green.svg) ![Generic badge](https://img.shields.io/badge/status-stable-green.svg)

<center><img src="../../../images/distribution_onduleur/capture1_1.gif" width="500px" alt="Distribution_energie" /></center>


> **Information**
> - Ce widget est basé sur le travail déja <a href="https://github.com/slipx06/sunsynk-power-flow-card" target="_blank">accompli.</a>
>
> - Pour chaque élément les unités des commandes doivent être identiques.
> 
> - Contrairement au widget <a href="../distribution_energie" target="_blank">Distribution Energie</a> ce widget fait moins de calculs.

## 1) Téléchargement de la source
> - <a href="{{site.url_git}}/WIDGET_cmd.info.string.distribution_onduleur" target="_blank">Téléchargez la source du widget pour le Core V4</a>

### Version dashboard

- Déposez le fichier <b>cmd.info.string.onduleur_distribution</b> dans le dossier <b>/html/data/customTemplates/dashboard/</b>

  <img src="../../../images/distribution_onduleur/capture2.png" alt="Téléchargement du widget" />

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegardez (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre (3, 4 et 5).

<img src="../../../images/distribution_onduleur/installation_virtuel1.png" alt="Virtuel 1" />
<img src="../../../images/distribution_onduleur/installation_virtuel2.png" alt="Virtuel 2" />


## Paramètres optionnels

<img src="../../../images/distribution_onduleur/parametres7.png" alt="Info backup" />

> **Information**
>
> - le paramètre optionnel batteryMaxPower permet, s'il est renseigné, de calculer la durée restante / temps de charge.

## 3) Ajout des données

Ce widget utilise les commandes présentes dans ce même équipement.
Il faut donc utiliser des noms de commande info prédéfinis suivant les tableaux ci-dessous :

### Solaire

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_solar | non | Production solaire quotidienne |
| pv_power <font color="red">*</font> | non | Puissance instantanée totale |
| pv1_power | non | Puissance instantanée PV1 |
| pv1_energy | non | Energie PV1 |
| pv1_voltage | non | Tension PV1 |
| pv1_current | non | Intensité PV1 |

> **Info**
>
> - Dans le tableau ci-dessus l'ajout de PV supplémentaires est infini, exemple pour un 2ème PV, utilisez pv2_power...
> - Si vous possédez 1 seul PV, utilisez avant tout pv1_power.
> - Si aucun des pv*_power n'est renseigné, la partie solaire sera automatiquement masquée.
> - pv_power <font color="red">*</font> : Si cette commande n'existe pas, le widget affichera la somme des pv.

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
> - Si "battery_power" n'est pas renseigné, la partie "batterie" sera automatiquement masquée.

### Aux

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| aux_power | non | Puissance instantanée. |
| daily_aux | non | Production auxiliaire quotidienne. |

> **Info**
>
> - Si "aux_power" n'est pas renseigné, la partie "Aux" sera automatiquement masquée.

### Réseau

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_grid_buy | non | Consommation venant du réseau quotidienne. |
| daily_grid_sell | non | Injection au réseau quotidienne. |
| grid_power | non | Puissance instantanée. (positive = consommation / négative = injection) |
| grid_status | non | État de connexion au réseau. (binaire)|

### Load

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| daily_load | non | Consommation des équipements "Load" quotidienne. |
| load_state | non | Puissance instantanée globale. |
| load1_power | non | Puissance instantanée du récepteur 1. |
| load1_energy | non | Energie récepteur 1. |
| load1_perso | non | Info perso du récepteur 1. |

> **Info**
> - Dans le tableau ci-dessus l'ajout de load supplémentaires est infini, exemple pour un 2ème load, utilisez load2_power...
>
> - Si "load_state" et "loadx_state" ne sont pas renseignés, la partie "Load" sera automatiquement masquée.
>
> - Si load_state n'est pas défini, il sera alors calculé par addition de load1_state + load2_state + ...

### Onduleur

| Nom | Obligatoire ? | Description |
| ------ | ------ | ------ |
| ac_temp | non | Température AC. |
| dc_temp | non | Température DC. |
| voltage_state | non | Tension de l'onduleur. |
| frequency_state | non | Fréquence de l'onduleur. |
| current_state | non | Intensité de l'onduleur. |
| lcd_state | non | Info à afficher dans l'afficheur LCD'. |

## Exemple :

<img src="../../../images/distribution_onduleur/widget_help4.png" alt="Help1" />

> **Légende** : 
> <br><b>Noir :</b> Commandes à renseigner dans l'équipement.
> <br><font color="red"><b>Rouge :</b> Paramètres optionnels.</font>
>
> <b><font color="red">*</font> pv_power :</b> ci cette commande n'existe pas, le widget affichera la somme des pv.

-------------------------

<img src="../../../images/distribution_onduleur/widget_help2.png" alt="Help2" />

## 3) Partie Tempo

### Avec le plugin "rteEcowatt"
- Affichage de la couleur du jour et du lendemain.

Il faudra télécharger le template <a href="{{site.url_git}}/WIDGET_cmd.info.string.distribution_onduleur" target="_blank">distribution_onduleur_tempo.json</a>.<br>
<i>Vous pouvez suivre <a href='../../../../help/fr_FR/template_scenario' target="_blank">l'aide à l'installation d'un template</a>.</i><br>

Commande de remplacement :

<img src="../../../images/distribution_onduleur/instal_template.png" alt="Help1" />

(1) Recherchez la commande sur laquelle vous avez appliqué le widget précédemment.<br>
(2) Appliquez la modification.


### Sans le plugin "rteEcowatt"
- Affichage de la couleur du jour seulement.

Il suffit simplement d'envoyer une des couleurs (RED, WHITE ou BLUE) sur la commande à laquelle vous avez appliqué le widget précédemment.

## 3) Icones dispo :

| ------ | ------ | ------ | ------ | ------ |
| <center>Four<br>(oven)<br><img src="../../../images/distribution_onduleur/svg/oven.svg" alt="oven" /> | <center>Pompe<br>(pump)<br><img src="../../../images/distribution_onduleur/svg/pump.svg" alt="pump" /> | <center>Clim<br>(aircon)<br><img src="../../../images/distribution_onduleur/svg/aircon.svg" alt="aircon" /> | <center>Chaudière<br>(boiler)<br><img src="../../../images/distribution_onduleur/svg/boiler.svg" alt="boiler" /> | <center>Chargeur<br>(charging)<br><img src="../../../images/distribution_onduleur/svg/charging.svg" alt="charging" /> |
| <center>Batterie<br>(battery)<br><img src="../../../images/distribution_onduleur/svg/battery.svg" alt="battery" /> | <center>Prise<br>(plug)<br><img src="../../../images/distribution_onduleur/svg/plug.svg" alt="plug" /> | <center>Piscine<br>(pool)<br><img src="../../../images/distribution_onduleur/svg/pool.svg" alt="pool" /> | <center>Sèche linge<br>(dryer)<br><img src="../../../images/distribution_onduleur/svg/dryer.svg" alt="dryer" /> | <center>Lave vaisselle<br>(dishwasher)<br><img src="../../../images/distribution_onduleur/svg/dishwasher.svg" alt="dishwasher" /> |
| <center>Machine a laver<br>(washing)<br><img src="../../../images/distribution_onduleur/svg/washing.svg" alt="washing" /> | <center>Micro-ondes<br>(microwave)<br><img src="../../../images/distribution_onduleur/svg/microwave.svg" alt="microwave" /> | <center>Grille-pain<br>(toaster)<br><img src="../../../images/distribution_onduleur/svg/toaster.svg" alt="toaster" /> | <center>Réfrigérateur<br>(fridge)<br><img src="../../../images/distribution_onduleur/svg/fridge.svg" alt="fridge" /> | <center>Cafetière<br>(coffee)<br><img src="../../../images/distribution_onduleur/svg/coffee.svg" alt="coffee" /> |
| <center>hotte<br>(hood)<br><img src="../../../images/distribution_onduleur/svg/hood.svg" alt="hood" /> | <center>Lumière<br>(light)<br><img src="../../../images/distribution_onduleur/svg/light.svg" alt="light" /> | <center>Ecran tv<br>(tv)<br><img src="../../../images/distribution_onduleur/svg/tv.svg" alt="tv" /> | <center>Serveur<br>(server)<br><img src="../../../images/distribution_onduleur/svg/server.svg" alt="server" /> | <center>Ordinateur portable<br>(laptop)<br><img src="../../../images/distribution_onduleur/svg/laptop.svg" alt="laptop" /> |
| <center>Console<br>(console)<br><img src="../../../images/distribution_onduleur/svg/console.svg" alt="console" /> | <center>Voiture électrique<br>(ve)<br><img src="../../../images/distribution_onduleur/svg/ve.svg" alt="ve" /> | <center>Logo Tesla<br>(tesla)<br><img src="../../../images/distribution_onduleur/svg/tesla.svg" alt="tesla" /> | <center>Chauffe-eau<br>(water_heater)<br><img src="../../../images/distribution_onduleur/svg/water_heater.svg" alt="water_heater" /> |  |

## Changelog

<a href="./changelog">Changelog</a>


## Todo

- Affichage d'un greenPower.

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Distribution Onduleur
