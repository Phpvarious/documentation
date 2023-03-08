
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info du Jour

------------

# Widget [Info du jour] ![Generic badge](https://img.shields.io/badge/Version-4.2%20%7C%204.3%20%7C%204.4-green.svg)

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/capture1_2.png" alt="Info du jour" />

- Informations disponibles sur le widget :
  - Date du jour.
  - Saint du jour (et du lendemain au survol).
  - Mode Jour/nuit (changement de couleur du Background).
  - Férié (prochain jour férié au survol).
  - Week-end.
  - Vacances (prochaines vacances au survol).
  - Lever/coucher du soleil (avec animation de l'élévation en cours).
  - Saison (représentée par l'image en haut à droite).

## 1) Téléchargement

- Fichier source à récupérer sous :
  - [Télécharger les sources du Widget pour le Core V4]({{site.url_git}}/WIDGET_cmd.info.sting.info_du_jour)

### Version dashboard

- Déposer le fichier cmd.info.string.Info_du_jour.html dans le dossier :
  - /html/data/customTemplates/dashboard/

  <img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/capture2.png" alt="Téléchargement du widget" />

### Version mobile

- Déposer le fichier cmd.info.string.Info_du_jour.html <b>du dossier mobile</b> dans le dossier :
  - /html/data/customTemplates/mobile/

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegarder (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre,(3, 4 et 5).

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/installation_virtuel2.png" alt="Virtuel 1" />
<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/installation_virtuel3.png" alt="Virtuel 2" />


## Paramètres optionnels

     colorBackgroundNight : Couleur du fond lorsque le widget est en Mode nuit [ Exemple : #fffff, white ... (accepte linear-gradient...) ]
     colorBackgroundDay : Couleur du fond lorsque le widget est en Mode jour [ Exemple : #fffff, white ... (accepte linear-gradient...) ]
     colorTextNight : Couleur du texte lorsque le widget est en Mode nuit [ Exemple : #fffff, white ... (Défaut : couleur du core) ]
     colorTextDay : Couleur du texte lorsque le widget est en Mode jour [ Exemple : #fffff, white ... (Défaut : couleur du core) ]
     colorLogoNight : Couleur du logo saison lorsque le widget est en Mode nuit [ Exemple : #fffff, white ... (Défaut : couleur du core) ]
     colorLogoDay : Couleur du logo saison lorsque le widget est en Mode jour [ Exemple : #fffff, white ... (Défaut : couleur du core) ]
     opacityLogo : opacité du logo saison [ Exemple : 10, 20 ... (Défaut : 50) ]
     borderRadius : Taille arrondi du widget [ Exemple : 10, 20 ... (Défaut : 30) ]
     displaySaisonText : Affiche/cache le texte saison [ 1=Afficher, 0=cacher (défaut : 1) ]
     displaySaisonLogo : Affiche/cache le logo saison [ 1=Afficher, 0=cacher (défaut : 1) ]
     displayLeverCoucher : Affiche/cache le div Lever/Coucher du soleil [ 1=Afficher, 0=cacher (défaut : 1) ]
     displayDureeJour : Affiche/cache la durée du jour dans le widget [ 1=Afficher, 0=cacher (défaut : 1) ]
     themeJeedom : Le widget se base sur le theme Jeedom pour basculer en mode Day/Night [ 1=Jeedom, 0=scénario(widget) (défaut : 0) ]

---------------------

## 3) Création du scénario

Créer un nouveau scénario puis ajouter un template :

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/scenario1.png" alt="Scénario 1" />

- Selectionnez "Charger un template" puis ajoutez le fichier téléchargé précedemment (Info du jour.json):

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/scenario2.png" alt="Scénario 2" />


- Une fois chargé, celui-ci devrait apparaître dans le menu de gauche, cliquez dessus :

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/scenario3.png" alt="Scénario 3" />

- Dans la nouvelle fenêtre :
  - Recherchez le virtuel créé précedemment (1).
  - Appliquez les modifications (2).
  - Demande de confirmation, cliquez sur OK puis sauvegardez le scénario.

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/scenario4.png" alt="Scénario 4" />

Le scénario a un CRON de cinq minutes par défaut.

## 4) Configuration
Une fois toutes ces étapes accomplies, ouvrez le scénario et modifiez la zone vous concernant pour les vacances scolaires.

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/config1_2.png" alt="Config 1" />

Ensuite configurez la zone géographique dans la configuration Jeedom :
- Rendez-vous dans Réglages/Sytème/Configuration.
- Puis dans l'onglet général, en bas renseignez les informations :

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/config2.png" alt="Config 2" />

## 5) Options

Il est possible d'extraire plus d'informations du scénario, il faudra créer de nouvelles actions (event) dans celui-ci et ajouter des infos dans votre virtuel :

### VACANCES SCOLAIRE

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
| tag(vacancesEnCours) | Binaire | 1=Vacances |
| tag(vacancesEnCoursLibelle) | Autre | Ex : Vacances de la Toussaint |
| tag(debutVacancesEnCours) |Autre | Ex : 2022-10-22 |
| tag(finVacancesEnCours) | Autre | Ex : 2022-11-07 |
| tag(vacancesPochainesLibelle) | Autre | Ex : Vacances de la Toussaint |
| tag(debutVacancesProchaines) | Autre | Ex : 2022-10-22 |
| tag(finVacancesProchaines) | Autre | Ex : 2022-11-07 |
| tag(nbProchainesVacances) | Numérique | Ex : 34 (34 jours) |

### SAINT DU JOUR

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
| tag(saintJour) | Autre | Saint du jour |
| tag(saintDemain) | Autre| Saint du lendemain |

### SOLEIL / JOUR

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
| tag(dateDuJour) | Autre | Ex : 2022-09-18 |
| tag(daynumber) | Numérique | |
| tag(leverSoleilScenario) | Numérique | Exemple : 831 (8h31) |
| tag(zenithSoleilScenario) | Numérique | Exemple : 1249 (12h49) |
| tag(coucherSoleilScenario) | Numérique | Exemple : 1707 (17h07) |
| tag(aubeCivil)| Numérique | Exemple : 831 (8h31) |
| tag(crepusculeCivil) | Numérique | Exemple : 1707 (17h07) |
| tag(aubeNautique) | Numérique | Exemple : 831 (8h31) |
| tag(crepusculeNautique) | Numérique | Exemple : 1707 (17h07) |
| tag(aubeAstronomique) | Numérique | Exemple : 831 (8h31) |
| tag(crepusculeAstronomique) | Numérique | Exemple : 1707 (17h07) |
| tag(elevation) | Numérique | |
| tag(elevationZenith) | Numérique | |
| tag(dureeJour)| Autre | Exemple : 15:10:51 (hh:mm:ss) |
| tag(dureeJourEcart) | Autre | Exemple : -207 (-207 secondes) |
| tag(modeJourBinaire) | Binaire | 1=Jour |
| tag(weekend) | Binaire | 1=WE |
| tag(ferie) | Binaire | 1=Férié |
| tag(libelleFerie) | Autre | Ex : Toussaint |
| tag(dateProchainFerie) | Autre | Ex : 2022-11-01 |
| tag(libelleProchainFerie) | Autre| Ex : Toussaint |
| tag(nbProchainFerie) | Numérique | Ex : 44 (44jours restant avant prochain jour férié |
| tag(saison) |Autre | Printemps/Eté... |

### Exemple dans le Scénario

<img src="{{site.url}}/documentation/{{site.widget}}/{{site.img}}/info_du_jour/scenario5_1.png" alt="scenario5_1" />

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info du Jour
