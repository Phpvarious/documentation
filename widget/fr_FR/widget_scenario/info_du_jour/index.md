
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info du Jour

------------

# Widget [Info du jour] ![Generic badge](https://img.shields.io/badge/Version-4.2%20%7C%204.3%20%7C%204.4%20Full%20JS-green.svg)

<img src="../../../images/info_du_jour/capture1_3.png" alt="Info du jour" />

- Informations disponibles sur le widget :
  - Date du jour.
  - Saint du jour (et du lendemain au survol).
  - Mode Jour/nuit (changement de couleur du Background).
  - Férié (prochain jour férié au survol).
  - Week-end.
  - Vacances (prochaines vacances au survol).
  - Lever/coucher du soleil (avec animation de l'élévation en cours).
  - Saison (représentée par l'image en haut à droite).
  - Infos de phase lunaire (avec animation).

## 1) Téléchargement

  > - <a href="{{site.url_git}}/WIDGET_cmd.info.sting.info_du_jour" target="_blank">Télécharger les sources du Widget pour le Core V4</a>

### Version dashboard

- Déposer le fichier cmd.info.string.Info_du_jour.html dans le dossier :
  - /html/data/customTemplates/dashboard/

  <img src="../../../images/info_du_jour/capture2.png" alt="Téléchargement du widget" />

### Version mobile

- Déposer le fichier cmd.info.string.Info_du_jour.html <b>du dossier mobile</b> dans le dossier :
  - /html/data/customTemplates/mobile/

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegarder (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre,(3, 4 et 5).

<img src="../../../images/info_du_jour/installation_virtuel2.png" alt="Virtuel 1" />
<img src="../../../images/info_du_jour/installation_virtuel3.png" alt="Virtuel 2" />


## Paramètres optionnels

<img src="../../../images/info_du_jour/parametres_3.png" alt="Info du jour" />

---------------------

## 3) Création du scénario

Créer un nouveau scénario puis ajouter un template :

<img src="../../../images/info_du_jour/scenario1.png" alt="Scénario 1" />

- Selectionnez "Charger un template" puis ajoutez le fichier téléchargé précedemment (Info du jour.json):

<img src="../../../images/info_du_jour/scenario2.png" alt="Scénario 2" />


- Une fois chargé, celui-ci devrait apparaître dans le menu de gauche, cliquez dessus :

<img src="../../../images/info_du_jour/scenario3.png" alt="Scénario 3" />

- Dans la nouvelle fenêtre :
  - Recherchez le virtuel créé précedemment (1).
  - Appliquez les modifications (2).
  - Demande de confirmation, cliquez sur OK puis sauvegardez le scénario.

<img src="../../../images/info_du_jour/scenario4.png" alt="Scénario 4" />

Le scénario a un CRON de cinq minutes par défaut.

> **Bug**
>
> Il est possible, après sauvegarde, que le scénario apparaisse vide, actualiser la page, pour faire apparaître le contenu.


## 4) Configuration
Une fois toutes ces étapes accomplies, ouvrez le scénario et modifiez la zone vous concernant pour les vacances scolaires.

<img src="../../../images/info_du_jour/config1_2.png" alt="Config 1" />

Ensuite configurez la zone géographique dans la configuration Jeedom :
- Rendez-vous dans Réglages/Sytème/Configuration.
- Puis dans l'onglet général, en bas renseignez les informations :

<img src="../../../images/info_du_jour/config2.png" alt="Config 2" />

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

### JOUR

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
| tag(dateDuJour) | Autre | Ex : 2022-09-18 |
| tag(dayNumber) | Numérique | |
| tag(weekend) | Binaire | 1=WE |
| tag(ferie) | Binaire | 1=Férié |
| tag(libelleFerie) | Autre | Ex : Toussaint |
| tag(dateProchainFerie) | Autre | Ex : 2022-11-01 |
| tag(libelleProchainFerie) | Autre| Ex : Toussaint |
| tag(nbProchainFerie) | Numérique | Ex : 44 (44jours restant avant prochain jour férié |
| tag(saison) |Autre | Printemps/Eté... |

### SOLEIL

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
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
| tag(dureeJourSeconde) |  Numérique | Exemple : 41203
| tag(dureeJourEcart) | Autre | Exemple : -207 (-207 secondes) |
| tag(modeJourBinaire) | Binaire | 1=Jour |
| tag(modeJour) | Autre | Jour ou Nuit |

### LUNE

| Tag scénario | Type Info virtuel | Détail |
| ------ | ------ | ------ |
| tag(Moon_Phase) | Autre | Croissante ou Décroissante |
| tag(Moon_PhaseName) | Autre | Ex : Premier croissant |
| tag(Moon_Age) | Numérique | Ex : 5.2 |
| tag(Next_Full_Moon) | Autre | Ex : jeudi 06/04/2023 |
| tag(Next_Full_Moon2) | Autre | Ex : vendredi 05/05/2023 |
| tag(Next_New_Moon) | Autre | Ex : jeudi 20/04/2023 |
| tag(Moon_Distance) | Numérique | Ex : 394213 (kms)|
| tag(Moon_Illumination) | Numérique | Ex : 28 (%)|

> **Tip**
>
> Pour mettre à jour le template et récuperer vos "event" :
> - Désactiver le scénario actuel, puis mettre tous les "event" perso dans un seul et meme bloc action.
> - Créer un nouveau scénario et appliquer le nouveau template sur celui-ci.
> - Utiliser le copier/coller pour transférer le bloc action qui contient les "event" perso vers le nouveau scénario (icones en haut a droite du bloc action).
> - Testé le nouveau scénario.
> - Si le test est concluant, supprimer l’ancien scénario.

### Exemple dans le Scénario

<img src="../../../images/info_du_jour/scenario5_1.png" alt="scenario5_1" />

### Changelog

<a href="./changelog">Changelog</a>

---------------------

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info du Jour
