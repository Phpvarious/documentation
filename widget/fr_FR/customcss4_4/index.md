
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

### Ajouter une marge en haut des tuiles :

```
/* Ajouter une marge en haut des tuiles */
.eqLogic.eqLogic-widget > .widget-name {
  margin-bottom: 5px;
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

### Rendre fixe de la barre de recherche :

```
/* rendre fixe de la barre de recherche */
#dashTopBar {
    position: fixed;
    top: 46px;
    z-index: 500;
    width: calc(100% - 27px) !important;
    left: 7px;
}
#div_displayObject .row > div:not(.hideByObjectSel) :first-child legend {
  margin-top: 37px !important;
}
[data-page="dashboard"] #dashOverviewPrev.overview {
  margin-top: 32px;
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

## UI

### Masquage du lien "synthèse" du menu :
```
/* Masquage du lien "synthèse" du menu */
#jeedomMenuBar > div > nav > ul:nth-child(1) > li:nth-child(1) > ul > li:nth-child(1) {
  display: none;
}
```
### Supprime l'animation (loading) lors du chargement d'une' page :
```
/* Supprime l'animation (loading) lors du chargement d'une page  */
#div_jeedomLoading .loadingSpinner {
  display: none;
}
```
### Changement de loading

```
/* Changement de loading */
/* Prochainement :-) */
```

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> Custom CSS pour v4.4