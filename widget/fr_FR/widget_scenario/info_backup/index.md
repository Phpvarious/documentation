
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info backup

------------

# Widget [Info backup] ![Generic badge](https://img.shields.io/badge/Version-4.2%20%7C%204.3%20%7C%204.4%20Full%20JS-green.svg)

<img src="../../../images/info_backup/capture2_2.png" alt="Info backup" />
<img src="../../../images/info_backup/capture2.gif" alt="Info backup" />

- Informations disponibles sur le widget :
  - Etat de la sauvegarde local.
  - Etat de la sauvegarde samba (si activée).
  - Nom de la sauvegarde.

## 1) Télécharger la source

> - <a href="{{site.url_git}}/WIDGET_cmd.info.sting.info_backup" target="_blank">Télécharger les sources du Widget pour le Core V4</a>

### Version dashboard

- Déposer le fichier <b>cmd.info.string.Info_backup.html</b> dans le dossier <b>/html/data/customTemplates/dashboard/</b>

  <img src="../../../images/info_backup/capture3.png" alt="Téléchargement du widget" />

------------------------

## 2) Création d'un virtuel

- Ajoutez une commande Info/Autre, puis sauvegarder (1).
- Attention, ne pas historiser (2).
- Associez le widget à la commande Info/Autre,(3, 4 et 5).

<img src="../../../images/info_backup/installation_virtuel2.png" alt="Virtuel 1" />
<img src="../../../images/info_backup/installation_virtuel3.png" alt="Virtuel 2" />


## Paramètres optionnels

<img src="../../../images/info_backup/parametres.png" alt="Info backup" />

---------------------

## 3) Création du scénario

Créer un nouveau scénario puis ajouter un template :

<img src="../../../images/info_backup/scenario1.png" alt="Scénario 1" />

- Selectionnez "Charger un template" puis ajoutez le fichier téléchargé précedemment (Info backup.json):

<img src="../../../images/info_backup/scenario2.png" alt="Scénario 2" />


- Une fois chargé, celui-ci devrait apparaître dans le menu de gauche, cliquez dessus :

<img src="../../../images/info_backup/scenario3.png" alt="Scénario 3" />

- Dans la nouvelle fenêtre :
  - Recherchez le virtuel créé précedemment (1).
  - Appliquez les modifications (2).
  - Demande de confirmation, cliquez sur OK puis sauvegardez le scénario.

<img src="../../../images/info_backup/scenario4.png" alt="Scénario 4" />

> **Bug**
>
> Il est possible, après sauvegarde, que le scénario apparaisse vide, actualiser la page, pour faire apparaître le contenu.

## 4) Configuration
Une fois toutes ces étapes accomplies, ouvrez le scénario et modifiez, DANS LE BLOC CODE ,la taille mini de la sauvegarde en octet pour déclencher une erreur. [Défaut : 100Mo]

<img src="../../../images/info_backup/config1.png" alt="Config 2" />

## 5) Options

Il est possible d'extraire plus d'informations du scénario, il faudra créer de nouvelles actions (event) dans celui-ci et ajouter des infos dans votre virtuel :

| Tag scénario | subType | Désignation | Valeurs |
| --- | --- | --- | --- |
| tag(action) | Autre| Etape de la sauvegarde| startBackup, endBackup |
| tag(errorScenario) | Binaire | Erreur dans le scenario | 0-->ok, 1-->erreur |
| tag(errorLog) | Binaire | Erreur dans le log | 0-->ok, 1-->erreur |
| tag(errorLocal) | Binaire | Etat backup local | 0-->ok, 1-->erreur |
| tag(errorSize) | Binaire | Erreur taille de la backup | 0-->ok, 1-->erreur |
| tag(errorSamba) | Binaire | Etat backup samba | 0-->ok, 1-->erreur, -1-->Désactivé |
| tag(errorMarket) | Binaire | Etat backup market | 0-->ok, 1-->erreur, -1-->Désactivé |

### Exemple dans le Scénario

<img src="../../../images/info_backup/scenario5.png" alt="scenario5" />

### Changelog

<a href="./changelog">Changelog</a>

---------------------

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/widget_scenario">Widgets / Scénarios</a> --> Info backup
