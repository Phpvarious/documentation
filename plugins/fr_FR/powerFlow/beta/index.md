# Plugin powerFlow ![Generic badge](https://img.shields.io/badge/Version-beta-orange.svg) ![Generic badge](https://img.shields.io/badge/Core-Full_js-green.svg)


Ce plugin permet d'afficher un widget de distribution (réseau, solaire, batterie, récepteurs et éléments personnalisés).

<img src="../../../images/powerFlow_exemple.png" width="400" style="display: block;margin: 0 auto;"/>


>**Important**
>
>Hormis pour les champs ```Max``` et ```Alerte```, qui autorisent l'utilisation d'une variable ou d'une valeur numérique, tous les autres champs n'accèptent qu'une commande (`#[objet][Equipement][commande]#`)<br>
> Si vous avez besoin d'effectuer un calcul <i>(p.ex. : récepteur 1 + récepteur 2)</i>, il faudra avant tout le faire dans un virtuel, puis insérer la commande résultante dans le plugin.

> **Conseil** : N'hésitez pas à lire les info-bulles (<i class="fas fa-question-circle" style="color: #5078aa !important;"></i> <i class="fas fa-exclamation-triangle" style="color: #c37d28 !important;"></i>) présentent dans le plugin.

>**Information global**<br>
> Tous les champs ```Max``` permettent au plugin d'afficher une gauge en fonction de la puissance instantanée.<br>
> <img src="../../../images/powerFlow_exemple_global_1.png"/><br>
>Tous les champs ```Alerte``` permettent d'indiquer une seuil.<br>
>Lorsque la consommation instantanée atteint ce seuil, le rectangle d'affichage de la consommation clignotera et changera de couleur (couleur et clignotement paramétrables dans les paramètres spécifiques).<br>
><img src="../../../images/powerFlow_exemple_global_2.gif"/>

Dans le plugin, vous trouvez plusieurs catégories, il n'est pas obligatoire de renseigner tous les champs.

## Paramètres spécifiques

- Clignotement : active/désactive le clignotement des éléments en Alerte.<br>
- Couleur Warning : couleur du contour des éléments en alerte.
- Gauges : active/désactive toutes les gauges.
- Formate milliers : active/désactive le formattage des milliers. (5000 -> 5 000)
- Conversion unités : active/désactive la conversion des unités. (5000w -> 5kw)
- Décimales : nombre de décimale a afficher àprès la virgule.
- Couleur arrière-plan : ajoute un arrière plan au widget.
- Debug widget : active/désactive les log en console de developpement du navigateur.

## Onduleur

### Configuration onduleur

Choisissez la couleur par défaut des éléments "onduleur" (gris par défaut).<br>
Il est possible de remplacer l'image de l'onduleur par défaut par une icône/image personnalisée, ou même remplacer par un simple cadre en activant la case "Aucun".

### Autres commandes

Commandes possibles :
- Tension. <sup>*</sup>
- Fréquence. <sup>*</sup>
- Intensité. <sup>*</sup>
- LCD.
- Température AC (alternatif).
- Température DC (continu).

 <sup>*</sup> <i> En cas d'utilisation d'une icône/image personnalisée, toutes ces informations seront affichées en dehors de l'onduleur.</i>

| | |
|--- | ---|
| <img src="../../../images/powerFlow_exemple_inverter_noImgCustom.png" height="100" /><br>Sans image personnalisée | <img src="../../../images/powerFlow_exemple_inverter_withImgCustom.png" height="100" /><br>Avec image personnalisée |

### Couleur texte intérieur

Vous pouvez choisir la couleur du texte situé a l'interieur de l'onduleur (tension, fréquence et intensité).<br>
<img src="../../../images/powerFlow_exemple_inverter_1.png" height="100" />

> ⚠️ Cette couleur sera automatiquement désactivée si vous utilisez une icône/image personnalisée.


## Réseau

<img src="../../../images/powerFlow_exemple_grid_1.png"/>

### Configuration des éléments "réseau"

Choisissez la couleur par défaut des éléments "Réseau" (bleu par défaut).

### Puissance réseau instantanée

Ajoutez simplement la commande qui contient la puissance instantanée du réseau.

> *Par défaut le plugin attend une valeur positive pour la consommation et négative pour l'injection.*
> *Cependant, il est possible d'inverser cette logique en cochant simplement la case "Inverser".*

### Energie réseau quotidienne

#### Energie vente & Energie achat

Ajoutez simplement les commandes qui contiennent les énergies à afficher.

>**Tips**
>
>Lorsque les énergies sont activées, il existe une interaction de couleurs.<br>
> Par exemple, si vous choisissez une couleur orange pour "Energie achat" et que vous êtes actuellement en consommation, le widget affichera toutes les informations liées au "réseau" en orange.<br>
> <img src="../../../images/powerFlow_exemple_grid_2.png" width="200px;"/><br>

Vous avez la possibilité d'afficher un texte personnalisé (```Texte à afficher```) :<br>
<img src="../../../images/powerFlow_exemple_grid_4.png"/><br>
*Exemple : VENTE JOUR*

#### Panne de courant

Si vous disposez d'une commande (binaire) qui permet de connaître l'état du réseau vous pouvez la renseigner afin de le représenter dans le widget, la couleur est aussi personnalisable.<br>
<img src="../../../images/powerFlow_exemple_grid_3.png" width="200px;"/>


## Solaire

<img src="../../../images/powerFlow_exemple_solar_1.png"/>

### Configuration des éléments "solaire"

Choisissez la couleur par défaut des éléments "Solaire" (orange par défaut).

### Puissance totale instantanée

Si vous disposez déjà d'une commande contenant la puissance totale des panneaux, vous pouvez la renseigner dans ce champ.<br>
Dans le cas contraire, laissez ce champ vide, le widget fera automatiquement la somme de tous les panneaux réunis.

### Energie solaire quotidienne

Ajoutez simplement la commande qui contient l'énergie ainsi que le texte a afficher.

### Ajout de panneaux solaires

#### Paramètres globals
##### Couleur si valeur = 0

Vous pouvez choisir une couleur différente pour permettre une visualisation rapide lorsqu'un panneau ne produit rien.<br>
<img src="../../../images/powerFlow_exemple_solar_4.png"/><br>
Vous pouvez aussi de ne pas afficher (masquer) le panneau en cochant la case "Masquer si valeur = 0". (prioritaire sur la couleur)<br>
<img src="../../../images/powerFlow_exemple_solar_5.png"/><br>

>**Information**
>
> A partir de 7 panneaux solaires, l'affichage de ceux-ci sur le widget passe en horizontal au dessus des récepteurs.<br>
<img src="../../../images/powerFlow_exemple_solar_6.png"/><br><br>
*Vous pouvez dans le plugin, réorganiser l'ordre d'affichage en les déplacant verticalement. (drag and drop)*<br>

> ⚠️Pour chaque panneau ajouté, le champ "Puissance" est obligatoire.<br>

Il est possible d'afficher l'énergie, l'intensité ainsi que la tension pour chaque panneaux (pas obligatoire).

Comme les autres catégories, chaque panneaux disposent d'une gauge et d'un seuil d'alerte. (Max et Alerte en w.)

>**Tips**
>
> Vous pouvez ajouter des panneaux "fantômes", c'est a dire des panneaux qui ne s'afficheront pas mais qui prendront quand même la place prévu dans le widget.<br>Pour cela, ajoutez un panneau, et laissez vide tous les champs.<br>
Exemple pour 5 panneaux sans éléments "fantôme" :<br>
<img src="../../../images/powerFlow_exemple_solar_2.png"/><br>
Toujours 5 panneaux, mais avec un élément "fantôme" inséré entre le 2ème et 3ème panneau :<br>
<img src="../../../images/powerFlow_exemple_solar_3.png"/><br>

## Batterie

<img src="../../../images/powerFlow_exemple_battery_1.png"/>

### Configuration des éléments "Batterie"

Choisissez la couleur par défaut des éléments "Batterie" (rose par défaut).

#### Capacité
Indiquez la capacité de la batterie (En Wh).<br>
Cette valeur permet au widget de calculer et d'afficher la durée restante avant décharge complète ou pleine charge, en fonction du pourcentage de batterie restant.<br>
<img src="../../../images/powerFlow_exemple_battery_4.png"/>

### Puissance instantanée de la batterie
Ajoutez simplement la commande qui contient l'énergie ainsi que le texte a afficher.

> *Par défaut le plugin attend une valeur positive pour la décharge et négative pour la charge.*
> Cependant, il est possible d'inverser cette logique en cochant simplement la case "Inverser".*

### Panneau solaire (mppt)
Si vous possèdez un panneau dédié a la batterie, renseignez ces champs pour l'afficher sur le widget :<br>
<img src="../../../images/powerFlow_exemple_battery_2.png"/><br>

### Energie quotidienne de la batterie
Ajoutez simplement les commandes qui contiennent les énergies à afficher.
>**Tips**
>
>Lorsque les énergies sont activées, il existe aussi une interaction de couleurs dans le widget.<br>voir exemple dans la section "réseau".

### Autres
Permet d'afficher la tension, l'intensité ainsi que la température. (pas obligatoire)

### État de charge

#### État SOC
Choississez la commande qui contient l'état de charge de la batterie en pourcentage.

#### SOC Shutdown. (%)
Choissisez la valeur à laquelle la batterie passe a l'arrêt.<br>
Attention, cette valeur est prise en compte sur le calcul du temps restant avant décharge complète, affiché sur le widget.

#### Icône
Vous pouvez choisir une icône personnalisée pour remplacer de l'icône batterie.<br>
<img src="../../../images/powerFlow_exemple_battery_3.png"/><br>

>**⚠️** Si vous utilisez une icône personnalsée ou une icône intégrée, la gestion des couleurs ci-dessous sera désactivée.<br>

#### Couleurs personnalisées

<!--
#### SOC Min. (%)
Choissisez la valeur à laquelle la batterie est considérée vide.<br>
Attention, cette valeur est prise en compte sur l'affichage de l'icone et la gestion des couleurs.

#### SOC Max. (%)
Choissisez la valeur à laquelle la batterie est considérée pleine.<br>
Attention, cette valeur est prise en compte sur l'affichage de l'icône et la gestion des couleurs.
-->

Choisissez une couleur personnalisée en fonction du seuil restant de batterie.

## Récepteurs

<img src="../../../images/powerFlow_exemple_load_1.png"/>

### Configuration des éléments "Récepteur"

Choisissez la couleur par défaut des éléments "Récepteur" (vert par défaut).

### Puissance totale instantanée des récepteurs

Si vous disposez déjà d'une commande contenant la puissance totale des récepteurs, vous pouvez la renseigner dans ce champ.<br>
Dans le cas contraire, laissez ce champ vide, le widget fera automatiquement la somme de tous les récepteurs.

### Energie quotidienne des récepteurs

Ajoutez simplement la commande qui contient l'énergie ainsi que le texte a afficher.<br>
<img src="../../../images/powerFlow_exemple_load_2.png"/>

### Ajout de récepteurs

<img src="../../../images/powerFlow_commande_load_1.png"/><br>

#### Paramètres globaux
Désactiver les animations : Cochez cette case si vous souhaitez masquer les animations des récepteurs.<br>
Forcer 4 recépteurs par colonne : Permet d'afficher jusqu'a 4 récepteurs par colonnes :<br>
<img src="../../../images/powerFlow_exemple_load_3.png" height="250px"/><br>
>**⚠️** Si vous utilisez plus que 6 panneaux solaires, cette option sera automatiquement désactivée.<br>
> Pour chaque récepteur ajouté, le champ "Puissance" est obligatoire.<br>

Il est possible d'afficher l'énergie ainsi qu'une commande personnalisée pour chaque récepteurs (pas obligatoire).

Comme les autres catégories, chaque récepteur disposent d'une gauge et d'un seuil d'alerte. (Max et Alerte en w.)

Vous pouvez ajouter jusqu'a 2 icônes ou images par récepteur.<br>
<img src="../../../images/powerFlow_exemple_load_4.png"/>

>**Tips**
>
> Vous pouvez aussi ajouter des recepteurs "fantômes". Voir section "solaire" pour plus d'informations.

## Générateur
<img src="../../../images/powerFlow_exemple_generateur_1.png"/>

### Configuration des éléments "Générateur"

Choisissez la couleur par défaut des éléments "Générateur" (violet par défaut).

### Puissance totale instantanée du générateur

> ⚠️Commande obligatoire pour afficher les éléments "générateur".<br>

Comme les autres catégories, chaque récepteur disposent d'une gauge et d'un seuil d'alerte. (Max et Alerte en w.)

### Energie quotidienne du générateur
Ajoutez simplement la commande qui contient l'énergie ainsi que le texte a afficher.

## Perso
<img src="../../../images/powerFlow_exemple_perso_1.png"/><br>
Cette section vous permet d'ajouter une commande personnalisée a afficher sur le widget a l'emplacement que vous souhaitez.

### Ajout d'une commande personnalisée

<img src="../../../images/powerFlow_commande_perso_1.png"/><br>
>**⚠️** Les champs ```commande```, ```X``` et ```Y``` sont obligatoires pour afficher l'élément sur le widget.<br>

#### Emplacement X et Y
Permet de placer l'élément horizontalement (X) et verticalement (Y).<br>
Par exemple, pour l'image de présentation ci-dessus, j'ai configuré ```X``` = 530 et ```Y``` = 234.<br>
Il faut parfois tâtonner un peu pour cibler l'emplacement souhaité...

#### Tailles

Possibilté de choisir la taille de police d'écriture de la commande ainsi que celle du texte a afficher.

>**⚠️** Si la ```position``` séléctionnée est "En ligne", seul la taille de la commande sera prise en compte.<br>
<img src="../../../images/powerFlow_exemple_perso_2.png"/><br>

# FAQ