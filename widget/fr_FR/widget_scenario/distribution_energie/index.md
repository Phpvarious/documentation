
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Energie Distribution

------------

# Widget [Energie Distribution] ![Generic badge](https://img.shields.io/badge/Version-4.2%20%7C%204.3%20%7C%204.4%20Full%20JS-green.svg) ![Generic badge](https://img.shields.io/badge/status-beta-orange.svg)

<center><img src="../../../images/distribution_energie/capture1_2.gif" width="300px" alt="Info backup" /></center>

> **---- BETA ----**
>
> - Ce widget est en version béta.
> - Il est basé sur le travail déja <a href="https://github.com/ulic75/power-flow-card" target="_blank">accomplie.</a>
>
> Je ne maitrise pas la totalité du fonctionnement sur les calculs... , je compte sur vous pour me faire des retours d'améliorations, et des retours sur le fonctionnement.

> **Information**
>
> - Il n'y a pour le moment aucun refresh automatique du widget, il se mettra a jour seulement au refresh de la page.
> - Toutes les valeurs d'énergie doivent être sur la même unité.
> - Evidemment sur l'image d'exemple, la totalité des infos sont affichés, mais si vous n'utilisez pas d'équipement gaz par exemple, le widget s'adaptera et masquera l'animation gaz.

## 1) Télécharger la source
> - <a href="{{site.url_git}}/WIDGET_cmd.info.string.distribution_energy" target="_blank">Télécharger les sources du Widget pour le Core V4</a>

### Version dashboard

- Déposer le fichier <b>cmd.info.string.distribution_energy</b> dans le dossier <b>/html/data/customTemplates/dashboard/</b>

  <img src="../../../images/distribution_energie/capture2.png" alt="Téléchargement du widget" />

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegarder (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre,(3, 4 et 5).

<img src="../../../images/distribution_energie/installation_virtuel1.png" alt="Virtuel 1" />
<img src="../../../images/distribution_energie/installation_virtuel2.png" alt="Virtuel 2" />


## Paramètres optionnels

<img src="../../../images/distribution_energie/parametres1_2.png" alt="Info backup" />

## Exemples :

si j'ai bien compris :-)
### Réseau
Si vous avez un équipement, ou déja un virtuel qui calcul votre energie venant du réseau (Grid) :
- Utilisation du paramètre "Grid" avec l'ID de l'équipement.
  - Si cet équipement peut renvoyer des valeurs négatives, il est possible d'utiliser le paramètre "GridInverted" en le passant a 1.

Si vous avez déja 1 ou 2 équipements qui présentent déja des valeurs sur la consommation / production (que des valeurs positives !) :
- Utiliser plutôt le paramètre "GridConsumption", si vous avez un autre équipement qui calcul la production (que des valeur positives !), vous pouvez utiliser le paramètre "GridProduction" (pas obligatoire)

### Batterie
Si vous avez un équipement, ou déja un virtuel qui calcul votre energie de la batterie :
- Utilisation du paramètre "Battery" avec l'ID de l'équipement.
  - Si cet équipement peut renvoyer des valeurs négatives, il est possible d'utiliser le paramètre "BatteryInverted" en le passant a 1.

Si vous avez déja 2 équipements qui présentent déja des valeurs sur la consommation / production (que des valeurs positives !) :
- Utiliser plutôt les paramètres "BatteryProduction" et "BatteryConsumption", attention dans ce cas les 2 paramètres sont obligatoires !

### Changelog

<a href="./changelog">Changelog</a>

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Energie Distribution