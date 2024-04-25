
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