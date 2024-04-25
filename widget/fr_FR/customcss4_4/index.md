
<a href="{{site.url}}/documentation">Accueil</a> --> Custom CSS pour v4.4

------------

# Custom CSS V4.4

> **Attention**
>
>L’utilisation de règles CSS inappropriées peu casser l’affichage de votre Jeedom.

## Tuiles

### Titre des tuiles sur 2 lignes :

```
/* titres des tuiles sur 2 lignes */
div.eqLogic.eqLogic-widget .widget-name, div.scenario-widget .widget-name {
  max-height: 45px;
  min-height: 24px;
  text-overflow: unset;
  white-space: unset;
  height: unset;
}
```

### Ajouter un saut de ligne (espace) entre 2 commandes :
> **Fonctionnement**
>
> Pour que ce code fonctionne il faut :
> - ajouter un saut de ligne après le widget.
> - et sur l'autre commande ajouter saut de ligne avant le widget.
```
/* Ajouter un saut de ligne (espace) entre 2 commandes */
div.eqLogic-widget div.break + div.break {
  height: 10px !important;
}
```
### Masquer la lettre (d, m ...) sur le graph d'un équipement :
```
/* Masquer la lettre (d, m ...) sur le graph d'un équipement */
.eqLogicGraphPeriod {
  opacity: 0;
}
```

### Rendre transparent le fond des graph des équipements :
```
/* Rendre transparent le fond des graph des équipements */
.eqlogicbackgraph .highcharts-container .highcharts-root .highcharts-series.highcharts-series-0.highcharts-areaspline-series path.highcharts-area {
  fill: transparent;
}
```

## Dashboard

### Ajouter un espace après le nom de l'objet
```
/* Ajouter un espace après le nom de l'objet */
.div_object legend .objectDashLegend {
  margin-bottom: 5px;
}
```

## Vues

### Aligner titres a gauche :
```
/* Aligner titres a gauche sur les vues */
div.div_viewZone legend.lg_viewZone {
  text-align: left !important;
}
```



-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> Custom CSS pour v4.4