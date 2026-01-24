# Plugin powerFlow ![Generic badge](https://img.shields.io/badge/Core-Full_js_(dev)-green.svg)

# /!\ EN COURS DE CONSTRUCTION /!\ 


Ce plugin permet d'afficher un widget de distribution (réseau, solaire, batterie, récepteurs et éléments personnalisés).

<img src="../../../images/powerFlow_exemple.png" width="300" style="display: block;margin: 0 auto;"/>


>**IMPORTANT**
>
>Hormis pour les champs Max et Alerte, qui autorisent l'utilisation d'une variable ou d'une valeur numérique, tous les autres champs n'accèptent qu'une commande <i>(#[objet][Equipement][commande]#)</i><br>
>Si vous avez besoin d'effectuer un calcul <i>(Ex: récepteur 1 + récepteur 2)</i>, il faudra d'abord le faire dans un virtuel, puis insérer la commande résultante dans le plugin.

>**Tips**
>
>N'hésitez pas à lire les info-bulles (<i class="fas fa-question-circle" style="color: #5078aa !important;"></i> <i class="fas fa-exclamation-triangle" style="color: #c37d28 !important;"></i>) présentent dans le plugin.

Dans le plugin, vous trouvez plusieurs catégories, il n'est pas obligatoire de renseigner tous les champs.

## Onduleur

Commandes possibles :

- Tension. <sup>*</sup>
- Fréquence. <sup>*</sup>
- Intensité. <sup>*</sup>
- LCD. <sup>*</sup>
- Température AC (alternatif).
- Température DC (continu).

 <sup>*</sup> En cas d'utilisation d'une image personnalisée, toutes ces informations seront affichées en dehors de l'onduleur dans le widget.

| | |
|--- | ---|
| <img src="../../../images/powerFlow_exemple_inverter_noImgCustom.png" height="100" /><br>Sans image perso | <img src="../../../images/powerFlow_exemple_inverter_withImgCustom.png" height="100" /><br>Avec image perso |


## Réseau

<img src="../../../images/powerFlow_exemple_grid.png"/>

### Configuration

#### Couleur

Choisissez la couleur par défaut des éléments "Réseau" (bleu par défaut).

### Puissance instantanée

#### Puissance
Ajoutez simplement la commande qui contient la puissance instantanée du réseau.

>**Tips**
>
>Par défaut le widget attend une valeur positive pour la consommation et négative pour l'injection.<br>Cependant, il est possible d'inverser cette logique en cochant simplement la case "Inverser".

#### Max (en w) :
Indiquez la valeur maximale que peut accepter le réseau.<br>Cette valeur permet de gérer la gauge en fonction de la puissance instantanée (variable acceptée).

#### Alerte (en w) :

Indiquez le seuil d'alerte souhaité. (variable acceptée)<br>
Lorsque la consommation instantanée atteindra ce seuil, le rectangle d'affichage de la consommation clignotera et changera de couleur (couleur et clignotement paramétrables dans la configuration de l'équipement).

### Energie quotidienne

#### Energie vente & Energie achat
Ajoutez simplement les commandes qui contiennent les énergies à afficher.

>**Tips**
>
>Lorsque les énergies sont activées, il existe une interaction de couleurs.<br>Par exemple : si vous choisissez une couleur orange pour "Energie achat" et que vous êtes actuellement en consommation (donc energie achat), le widget affichera toutes les informations liées au "réseau" en orange.<br>
<img src="../../../images/powerFlow_exemple_grid_2.png" width="200px;"/>

#### Panne de courant
Si vous disposez d'une commande (binaire) qui permet de connaître l'état du réseau vous pouvez la renseigner afin de l'afficher dans le widget comme ci-dessous :<br>
<img src="../../../images/powerFlow_exemple_grid_3.png" width="200px;"/>

## Solaire
<img src="../../../images/powerFlow_exemple_solar_1.png"/>

### Configuration
#### Couleur

Choisissez la couleur par défaut des éléments "Solaire" (orange par défaut).

#### Max (en w) :
Indiquez la valeur maximale que peut produire la totalité des panneaux solaires.<br>Cette valeur permet de gérer la gauge en fonction de la puissance totale (variable acceptée).

#### Alerte (en w) :

Indiquez le seuil d'alerte souhaité. (variable acceptée)<br>
Lorsque la puissance totale instantanée des panneaux atteindra ce seuil, le rectangle d'affichage de la puissance clignotera et changera de couleur (couleur et clignotement paramétrables dans la configuration de l'équipement).

### Puissance totale instantanée

#### Puissance totale

Si vous disposez déjà d'une commande contenant la puissance totale des panneaux, vous pouvez renseigner ce champs.<br>
Dans le cas contraire, laissez ce champs vide, le widget fera automatiquement le calcul de la somme de tous les panneaux réunis.
### Energie quotidienne

#### Energie

Ajoutez simplement la commande qui contient l'énergie à afficher.

### Panneaux solaires
#### Couleur si valeur = 0
lorsqu'un panneau ne produit pas,
Vous pouvez choisir une couleur différente qui permettra de visualiser rapidement .
Vous avez aussi la possibilté de ne pas afficher le panneau en cochant la case "Masquer si valeur = 0". (prioritaire sur la couleur)

#### Ajout de panneaux solaires
>**Information**
>
>A partir de 7 panneaux solaires, l'affichage de ceux-ci sur le widget, passe en horizontal au dessus des récepteurs.<br>
Vous pouvez réorganiser l'ordre d'affichage en déplacant ceux-ci verticalement. (drag and drop)<br>

⚠️Pour chaque panneau ajouté, le champs "Puissance" est obligatoire.<br>

Il est possible d'afficher l'énergie, l'intensité ainsi que la tension pour chaque panneaux (pas obligatoire).

Comme les autres éléments, chaque panneaux disposent d'une gauge et d'un seuil d'alerte. (Max et Alerte en w.)

>**Tips**
>
>Vous pouvez ajouter des panneaux "fantômes", c'est a dire des panneaux qui ne s'afficheront pas mais qui prendront quand même la place prévu dans le widget.<br>Pour cela, ajoutez un panneau, et laissez vide tous les champs.<br>
Exemple pour 5 panneaux sans éléments "fantôme" :<br>
<img src="../../../images/powerFlow_exemple_solar_2.png"/><br>
Toujours 5 panneaux, mais avec un élément "fantôme" inséré entre le 2ème et 3ème panneau :<br>
<img src="../../../images/powerFlow_exemple_solar_3.png"/><br>

## Batterie
<img src="../../../images/powerFlow_exemple_battery_1.png"/>

### Configuration
#### Couleur
Choisissez la couleur par défaut des éléments "Batterie" (rose par défaut).
#### Capacité
Indiquer la capacité de la batterie. (variable autorisée)<br>
Cette valeur permet au widget de calculer et d'afficher la durée restante avant décharge complète ou pleine charge en fonction du % de batterie restant.

### Puissance instantanée
Ajoutez simplement la commande qui contient la puissance instantanée de la batterie.

>**Tips**
>
>Par défaut le widget attend une valeur positive pour la décharge et négative pour la charge.<br>Cependant, il est possible d'inverser cette logique en cochant simplement la case "Inverser".

### Panneau solaire (mppt)
Si vous possèdez un panneau dédié a la batterie, renseignez ces champs pour l'afficher sur le widget :<br>
<img src="../../../images/powerFlow_exemple_battery_2.png"/><br>

### Energie quotidienne
Ajoutez simplement les commandes qui contiennent les énergies à afficher.
>**Tips**
>
>Lorsque les énergies sont activées, il existe aussi une interaction de couleurs dans le widget.<br>voir exemple dans la section "réseau".

### Autres
Permet d'afficher la tension, l'intensité ainsi que la température. (pas obligatoire)

### État de charge

#### État SOC
Choississez la commande qui contient l'état de charge de la batterie en %.

#### SOC Shutdown. (%)
Choissisez la valeur a laquelle la batterie passe a l'arrêt.<br>
Attention, cette valeur est prise en compte sur le calcul du temps restant avant décharge complète, affiché sur le widget.

#### SOC Min. (%)
Choissisez la valeur a laquelle la batterie est considéré vide.<br>
Attention, cette valeur est prise en compte sur l'affichage de l'icone et la gestion des couleurs.

#### SOC Max. (%)
Choissisez la valeur a laquelle la batterie est considéré pleine.<br>
Attention, cette valeur est prise en compte sur l'affichage de l'icone et la gestion des couleurs.

#### Icône
Vous pouvez choisir une icone personnalisée en remplacement de l'icone batterie.<br>

>**⚠️**
>
> Si vous utilisez une icône personnalsée ou une icône intégrée, la gestion des couleurs ci-dessous sera désactivée.<br><br>

#### Couleurs personnalisées
Choisissez une couleur personnalisée en fonction du seuil restant de la batterie.


# FAQ