<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/info_du_jour">Info du Jour</a> --> [ChangeLog]

--------------------

# Journal des modifications

> **Important**
>
> N'oubliez pas de reconfigurer le paramètre "$zone" dans le bloc code, si vous mettez à jour le scénario, car celui-ci sera reconfiguré en zone B par défaut.
     
## 2023

### 05/05/2024 12h15

  - Mise à jour de widget version mobile suite a bug d'affichage en 4.4.

### 16/04/2023

  - Mise à jour de widget version mobile. [widget Mobile]
  - Ajout nouveaux paramètres optionnels pour la version mobile. [widget Mobile]

### 11/04/2023

  - Correction d'une erreur sur le tag Next_New_Moon. [scénario]
  - Renommage des Phases : montante et descendante deviennent Croissante, Décroissante.  [scénario]
  - Modification du code, celui-ci est plus précis dans les phases lunaire.  [scénario]
  - Ajout de l'animation de la phase lunaire dans le widget. [widget Dashboard]

### 26/03/2023

  - Ajout d'un bloc code, celui-ci permet de récupérer des informations sur la lune. Thanks @PrFalKeN.  [scénario]

### 08/03/2023

  - Restructuration du code, compatibité Core V4.2 V4.3 V4.4
  - Ajout des dates de vacances jusqu'au 2026/09/01. [scénario]
  - Ajout de l'écart de durée du jour avec la veille. [widget Dashboard]
  - Ajout de tag (aubeCivil, crepusculeCivil, aubeNautique, crepusculeNautique, aubeAstronomique, crepusculeAstronomique) Thanks @PrFalKeN.  [scénario]
  - Ajout tag(dureeJourSeconde) et tag(modeJour) [scénario]
  - En mode themeJeedom, le widget change de thème lors de l'évènement du core, plus besoin d'attendre le lancement du scénario. [widget Dashboard]
  
## 2022

### 18/09/2022

  - Ajout des dates de vacances jusqu'au 2023/09/01. [scénario]
  - Modification de l'affichage : St -> Saint et Ste -> Sainte. [scénario]
  - Affichage de tous les tag disponibles, dans le log. [scénario]
  - mise a dispo du tag « dureeJourEcart » en secondes. [scénario]
  - Restructuration du code, il est possible de désactiver chaque catégorie (vacances, saint, soleil, widget ...) individuellement. [scénario]
  - Affichage de la durée du jour (par paramètre optionnel) entre lever et coucher du soleil. [widget Dashboard]

### 21/06/2022

- Ajouts / Modification des paramètres optionnels [widget Dashboard].

### 20/06/2022

- Ajout de paramètres optionnels. [Demande](https://community.jeedom.com/t/widget-perso-info-du-jour/86118) [widget Dashboard].
- Modification de la taille du widget par défaut [widget Dashboard].
- Bugfix lorsque l'option "Centrage vertical des tuiles" est cochées dans l'interface Jeedom (Merci @jpty) [widget Dashboard].

### 21/02/2022

- Bugfix sur la date du dernier jour de vacances [scénario].
- Rajout des dates de vacances jusqu'au 2023/09/01 [scénario].

### 23/01/2022

- Remplacement de la fonction sun_pos(), qui générait des erreurs dans le log "scenario_execution" par [getSunPosition()](https://github.com/KiboOst/php-sunPos/blob/master/phpSunPos.php) qui est de plus, plus précise. [scénario].

## 2021

### 05/12/2021
- Création.








-------------------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario/info_du_jour">Info du Jour</a> --> [ChangeLog]