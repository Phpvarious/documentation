# Plugin powerFlow ![Generic badge](https://img.shields.io/badge/Core-Full_js_(dev)-green.svg)

# /!\ EN COURS DE CONSTRUCTION /!\ 


Ce plugin permet d'afficher un widget de distribution (Réseau, solaire, batterie, récepteurs et éléments perso).

<img src="../../../images/powerFlow_exemple.png" width="300" style="display: block;margin: 0 auto;"/>


>**IMPORTANT**
>
>Hormis pour les "max" et "alert" qui autorise l'utilisation d'une variable ou d'une valeur numérique, tous les autres champs accèpte uniquement une commande <i>(#[objet][Equipement][commande]#)</i><br>
>Si vous avez besoin de faire un calcul <i>(Ex: récepteur1 + récepteur2)</i>, il faudra avant tout le faire dans un virtuel pour ensuite insérer cette commande dans le plugin.

>**Tips**
>
>Ne pas hésiter a lire les tooltips (<i class="fas fa-question-circle" style="color: #5078aa !important;"></i> <i class="fas fa-exclamation-triangle" style="color: #c37d28 !important;"></i>) présent dans le plugin.

Dans le plugin vous trouvez plusieurs catégories, il n'est pas obligatoire de renseigner tous les champs :

## Onduleur

Commandes possibles :

- Tension. <sup>*</sup>
- Fréquence. <sup>*</sup>
- Intensité. <sup>*</sup>
- LCD. <sup>*</sup>
- Température AC (alternatif).
- Température DC (continu).

 <sup>*</sup> En cas d'utilisation d'une image perso, toutes ces infos seront déporté à l'exterieur de l'onduleur dans le widget.

| | |
|--- | ---|
| <img src="../../../images/powerFlow_exemple_inverter_noImgCustom.png" height="100" /><br>Sans image perso | <img src="../../../images/powerFlow_exemple_inverter_withImgCustom.png" height="100" /><br>Avec image perso |


## Réseau

Par défaut le widget attend une valeur positive pour la consommation et négative pour l'injection.<br>Mais il est possible d'inverser cette valeur en cochant simplement la case "Inverser".

# FAQ