
<a href="{{site.url}}/documentation">Accueil</a> --> Custom CSS pour v4.4

------------

# Custom CSS V4.4

<div class="alert alert-info"><i class="fa-solid fa-triangle-exclamation"></i> <strong>Attention : </strong> L’utilisation de règles CSS inappropriées peu casser l’affichage de votre Jeedom.</div>

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
### Changement de loading (Effet 1)

<center><img src="img/effet1.gif" alt="Téléchargement du widget" /></center>

```
/* Changement de loading (Effet 1) */
#div_jeedomLoading .loadingSpinner {
  position: relative;
  left: calc(50% - 102px);
  border-radius: 16px;
  width: 205px;
  height: 90px;
  padding: 4px;
  background: rgba(255, 255, 255, 0.4);
  border-top: unset; 
  -webkit-animation: unset;
  animation: unset;
}
#div_jeedomLoading .loadingSpinner:before {
  content: "";
  position: absolute;
  border-radius: 16px;
  width: 82px;
  height: 82px;
  left: 0;
  background: #FFF;
  background: var(--logo-primary-color);
  background: no-repeat center / 100% url(../../core/img/jeedom_home_Light.png);
  -webkit-animation: push_loadingSpinner1 1s infinite ease-in-out;
  animation: push_loadingSpinner1 1s infinite ease-in-out;
  border-top-color: unset;
  top: unset;
  bottom: unset;
  right: unset;
  border: unset;
}
#div_jeedomLoading .loadingSpinner:after { content: none; }
```

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> Custom CSS pour v4.4